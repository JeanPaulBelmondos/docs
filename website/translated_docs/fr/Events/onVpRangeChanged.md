---
id: onVpRangeChanged
title: On VP Range Changed
---

| Code | Peut être appelé par                                    | Définition                                                                                            |
| ---- | ------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| 61   | [4D View Pro Area](FormObjects/viewProArea_overview.md) | The 4D View Pro cell range has changed (e.g., a formula calculation, value removed from a cell, etc.) |


## Description


This event is generated when a change occurs within a cell range in the 4D View Pro document.

The object returned by the FORM Event command contains:

| Propriété    | Type        | Description                                                                                                                                                                                                                                                                  |
| ------------ | ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| objectName   | Texte       | 4D View Pro area name                                                                                                                                                                                                                                                        |
| code         | entier long | On VP Range Changed                                                                                                                                                                                                                                                          |
| description  | Texte       | "On VP Range Changed"                                                                                                                                                                                                                                                        |
| sheetName    | Texte       | Name of the sheet of the event                                                                                                                                                                                                                                               |
| range        | object      | Cell range of the change                                                                                                                                                                                                                                                     |
| changedCells | object      | Range containing only the changed cells. It can be a combined range.                                                                                                                                                                                                         |
| action       | Texte       | The type of operation generating the event:<p><p><li>"clear" - A clear range value operation</li><li>"dragDrop" - A drag and drop operation</li><li>"dragFill" - A drag fill operation</li><li>"evaluateFormula" - Setting a formula in a specified cell range</li><li>"paste" - A paste operation</li><li>"setArrayFormula" - Setting a formula in a specified cell range</li><li>"sort" - Sorting a range of cells</li> |
> See also [On After Edit](onAfterEdit.md).	
