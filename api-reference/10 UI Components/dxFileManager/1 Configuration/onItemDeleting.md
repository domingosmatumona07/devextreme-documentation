---
id: dxFileManager.Options.onItemDeleting
type: function(e)
default: null
---
---
##### shortDescription
A function that is executed before a file or folder is deleted.

##### param(e): Object
Information about the event.

##### field(e.cancel): Boolean | Promise<void>
Allows you to cancel the file or folder deletion.

##### field(e.component): dxFileManager
The UI component's instance.

##### field(e.element): DxElement
#include common-ref-elementparam with { element: "component" }

##### field(e.errorCode): Number
#include filemanager-error-codes

##### field(e.errorText): String
Allows you to specify the error message.

##### field(e.item): FileSystemItem
The file or folder to be deleted.

##### field(e.model): any
Model data. Available only if you use Knockout.

---

Select a file/folder and click the **Delete** context menu or toolbar item to delete this file/folder. The FileManager component displays a delete confirmation message. The **onItemCopying** function is executed when you click  **Delete** in the dialog.

![DevExtreme File Manager - Copy File or Folder](/images/FileManager/delete-confirmation-dialog.png)

---

##### jQuery

    <!-- tab: index.js -->
    $(function() {
        $("#file-manager").dxFileManager({
            // ...
            onItemDeleting: function (e) {
                // your code
            }
        });
    }); 

##### Angular

    <!--TypeScript-->
    import { DxFileManagerModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        onItemDeleting(e) {
            // your code
        }
    }
    @NgModule({
        imports: [
            // ...
            DxFileManagerModule
        ],
        // ...
    })

    <!--HTML-->
    <dx-file-manager ...
        (onItemDeleting)="onItemDeleting($event)">
    </dx-file-manager>

##### Vue

    <!-- tab: App.vue -->
    <template>
        <DxFileManager
            ...
            @on-item-deleting="onItemDeleting"
        />
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import DxFileManager from 'devextreme-vue/file-manager';
  
    export default {
        components: {
            DxFileManager
        },
        methods: {
            onItemDeleting(e) {
                // your code
            }
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import FileManager from 'devextreme-react/file-manager';

    const App = () => {
        const onItemDeleting = (e) => {
            // your code
        };

        return (
            <FileManager ...
                onItemDeleting={onItemDeleting} />            
        );
    }

    export default App;

##### ASP.NET MVC Controls

    <!--Razor C#-->
    @(Html.DevExtreme().FileManager()
        .ID("file-manager")
        // ...
        .OnItemDeleting("fm_itemDeleting_handler")
    )
    <script>
        function fm_itemDeleting_handler(e) {
            // your code
        }
    </script>

##### ASP.NET Core Controls

    <!--Razor C#-->
    @(Html.DevExtreme().FileManager()
        .ID("file-manager")
        // ...
        .OnItemDeleting("fm_itemDeleting_handler")
    )
    <script>
        function fm_itemDeleting_handler(e) {
            // your code
        }
    </script>

---

#####See Also#####
- [itemDeleting](/Documentation/ApiReference/UI_Components/dxFileManager/Events/#itemDeleting)