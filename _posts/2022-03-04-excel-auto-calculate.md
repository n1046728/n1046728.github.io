---
itle: How to fix excel formula auto-calculate
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-04 14:22:08 +0800
categories: [excel, function]
tags: [excel , vba]     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
Excel third-party addin help us to solve complicated numeric problem.Sometimes all cells refresh by add-in but some cells need to using f2 + Enter to enforce it refresh.This article tell u how to solve it.
<!--more-->

## solution
### vba
```vb
Selection.Value = Selection.FormulaR1C1
```
### function
* your cell add now function 
> f() + now()*0

## reference 
* [Force "F2"+"Enter" on range of cells - **stackoverflow Thomas F.** ](https://stackoverflow.com/questions/24060831/force-f2enter-on-range-of-cells)
* [How to Fix Excel Formulas that are Not Calculating or Updating - **EXCEL Campus**](https://www.excelcampus.com/functions/formulas-not-calculating/)
