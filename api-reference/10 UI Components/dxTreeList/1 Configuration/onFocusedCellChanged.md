---
id: dxTreeList.Options.onFocusedCellChanged
type: function(e)
default: null
---
---
##### shortDescription
A function that is executed after the focused cell changes. Applies only to cells in data rows.

##### param(e): ui/tree_list:FocusedCellChangedEvent
Information about the event that caused the function's execution.

##### field(e.cellElement): DxElement
#include common-ref-elementparam with { element: "focused cell" }

##### field(e.column): dxTreeListColumn
The column's properties.

##### field(e.columnIndex): Number
The index of the cell's column.

##### field(e.component): {WidgetName}
The UI component's instance.

##### field(e.element): DxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.model): any
Model data. Available only if you use Knockout.

##### field(e.row): dxTreeListRowObject
The row's properties.

##### field(e.rowIndex): Number
The index of the cell's row.

---

#####See Also#####
- [focusedRowIndex](/api-reference/10%20UI%20Components/GridBase/1%20Configuration/focusedRowIndex.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#focusedRowIndex') | [focusedRowKey](/api-reference/10%20UI%20Components/GridBase/1%20Configuration/focusedRowKey.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#focusedRowKey')
- [focusedColumnIndex](/api-reference/10%20UI%20Components/GridBase/1%20Configuration/focusedColumnIndex.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#focusedColumnIndex')