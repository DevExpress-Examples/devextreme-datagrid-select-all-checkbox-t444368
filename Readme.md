<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128583254/23.1.3%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T444368)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->

# DataGrid for DevExtreme - How to implement a three-state "Select All" CheckBox in a group row 

This example demonstrates how to implement a custom "Select All" CheckBox in a group row to select all rows in this group. This CheckBox can have three states: unchecked, checked, or undetermined (when only several of the group members are checked).

This example supports the [DataGrid.remoteOperations](https://js.devexpress.com/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/remoteOperations/) option.

DataGrid may query all data when selecting a group row with many data records. You can use the **DataGrid.selection.maxFilterLengthInRequest** private option to increase this threshold but it may result in Error 400. Make sure that your server supports long URLs. Also, make sure to test **maxFilterLengthInRequest** after every DevExtreme upgrade since we may change this private API without notifications.

![image](https://github-production-user-asset-6210df.s3.amazonaws.com/13280527/255941324-813d1328-2a2b-4ebc-bbfe-e3291b7df6ee.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20241225%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20241225T121223Z&X-Amz-Expires=300&X-Amz-Signature=b6a12674b67d29d5df9175e3e8d911466505818989b7c7cce7220825cace6010&X-Amz-SignedHeaders=host)

## Files to Review

- **jQuery**
    - [index.js](jQuery/index.js)
    - [GroupSelectionBehavior.js](jQuery/GroupSelectionBehavior.js)
- **Angular**
    - [GroupRowSelectionHelper.ts](Angular/src/app/GroupRowSelection/GroupRowSelectionHelper.ts)
    - [group-row.component.html](Angular/src/app/GroupRowSelection/GroupSelectionBehavior.js)
    - [group-row.component.ts](Angular/src/app/GroupRowSelection/group-row.component.ts)
- **React**
    - [GroupRowComponent.tsx](React/src/GroupRowSelection/GroupRowComponent.tsx) 
    - [GroupRowSelectionHelper.tsx](React/src/GroupRowSelection/GroupRowSelectionHelper.tsx)
- **Vue**
    - [GroupRowComponent.vue](Vue/src/components/GroupRowSelection/GroupRowComponent.vue)
    - [GroupRowSelectionHelper.ts](Vue/src/components/GroupRowSelection/GroupRowSelectionHelper.ts)
      
## Implementation details

The GroupSelectionBehavior class uses the [customizeColumns](https://js.devexpress.com/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/#customizeColumns) function to specify [groupCellTemplate](https://js.devexpress.com/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/columns/#groupCellTemplate) for all columns. This template creates a CheckBox for every group row.

## Documentation

- [CheckBox - API Reference](https://js.devexpress.com/Documentation/ApiReference/UI_Components/dxCheckBox/)
- [DataGrid - API Reference](https://js.devexpress.com/Documentation/ApiReference/UI_Components/dxDataGrid/)

## More Examples

- [DataGrid Multiple Record Selection API Demo](https://js.devexpress.com/Demos/WidgetsGallery/Demo/DataGrid/MultipleRecordSelectionAPI)
<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=devextreme-datagrid-select-all-checkboxes&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=devextreme-datagrid-select-all-checkboxes&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
