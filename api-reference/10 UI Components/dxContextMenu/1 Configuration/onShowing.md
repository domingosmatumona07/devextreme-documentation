---
id: dxContextMenu.Options.onShowing
type: function(e)
default: null
---
---
##### shortDescription
A function that is executed before the ContextMenu is shown.

##### param(e): ui/context_menu:ShowingEvent
Information about the event.

##### field(e.cancel): Boolean
Allows you to cancel UI component showing.

##### field(e.component): {WidgetName}
The UI component's instance.

##### field(e.element): DxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.model): any
Model data. Available only if you use Knockout.

---
