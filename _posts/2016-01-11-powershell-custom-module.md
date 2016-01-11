---
layout: post
title: Creating a custom PowerShell module
published: true
tags: powershell
---

Here's a single script that will show you how to create a custom PowerShell module from a file in an arbitrary location, execute a function within that module, and then remove the module.

{% highlight powershell %}

## Build a file path ready to save our custom module, with path based on current execution directory
$invocation = (Get-Variable MyInvocation).Value
$thisdirectorypath = Split-Path $invocation.MyCommand.Path
$custommodulefilepath = $thisdirectorypath + "AddNumbersModule.psm1"

## Hard coded, literal string, of the Module that we're adding
$AddNumbersModuleDefinition = 
"Function Add-TwoNumbers
{
	`$first = `$args[0]
	`$second = `$args[1]

	return `$first + `$second
}"

## Put the Module in to a file ready to import
$AddNumbersModuleDefinition >> $custommodulefilepath 

## Import the custom module (from the location we just saved it to)
Import-Module $custommodulefilepath 

## Let's use the new function from the custom module, to prove that it works!
Add-TwoNumbers 1 5

## When the module is imported it is dynamically given a name based partly on the file location, 
##   |_ which in this script will change based on the current execution directory. 
##   |_ In order to remove the module when we're finished, we need that name.
$addedModuleName = Get-Module | where {$_.Name -like "*AddNumbersModule*"} | Select -ExpandProperty Name

## ..and we can remove it again, using the name we fetched earlier.
Remove-Module $addedModuleName

{% endhighlight %}

NB: You will need to have the correct execution policy set in order to be able to import custom modules. If you don't have this set already, you'll need to execute the following command:

{% highlight powershell %}

Set-ExecutionPolicy Unrestricted

{% endhighlight %}