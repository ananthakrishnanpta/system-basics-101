# PowerShell Scripting Basics

## 1. What is PowerShell?

PowerShell is a command-line shell and scripting language used for
automation, system administration, and DevOps tasks. It is object-based.

------------------------------------------------------------------------

## 2. Script File

-   Extension: `.ps1`

Run:

    .\script.ps1

------------------------------------------------------------------------

## 3. Execution Policy

    Get-ExecutionPolicy
    Set-ExecutionPolicy RemoteSigned

------------------------------------------------------------------------

## 4. Variables

    $name = "Anantha"
    $age = 25
    Write-Output $name

------------------------------------------------------------------------

## 5. Data Types

    $num = 10
    $price = 99.99
    $isValid = $true

------------------------------------------------------------------------

## 6. Operators

    $a = 10
    $b = 5

    $a + $b
    $a -gt $b
    $a -eq $b

------------------------------------------------------------------------

## 7. Conditionals

    if ($age -ge 18) {
        Write-Output "Adult"
    } else {
        Write-Output "Minor"
    }

------------------------------------------------------------------------

## 8. Loops

### For

    for ($i = 1; $i -le 5; $i++) {
        Write-Output $i
    }

### Foreach

    $items = "A","B","C"
    foreach ($item in $items) {
        Write-Output $item
    }

### While

    $i = 1
    while ($i -le 3) {
        Write-Output $i
        $i++
    }

------------------------------------------------------------------------

## 9. Functions

    function Say-Hello {
        param($name)
        Write-Output "Hello $name"
    }

    Say-Hello "Anantha"

------------------------------------------------------------------------

## 10. File Operations

    New-Item file.txt
    "Hello World" > file.txt
    Get-Content file.txt

------------------------------------------------------------------------

## 11. Cmdlets

    Get-Process
    Get-Service
    Get-ChildItem

------------------------------------------------------------------------

## 12. Pipeline

    Get-Process | Where-Object {$_.CPU -gt 100}

------------------------------------------------------------------------

## 13. Objects

    Get-Process | Select-Object Name, CPU

------------------------------------------------------------------------

## 14. Example Script

    $file = "test.txt"

    if (Test-Path $file) {
        Write-Output "File exists"
    } else {
        Write-Output "File not found"
    }
