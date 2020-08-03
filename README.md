# WPFDataGridSorted

This demo app presents a WPF DataGrid that can be sorted using the keyboard, and which sets programmatically accessible information about the current sort order. This enables screen readers such as Narrator to announce the current sort information.

The first image below shows the Accessibility Insights for Windows tool reporting the UI Automation (UIA) properties of a column header in the demo DataGrid. The UIA ItemStatus property is "Ascending", which matches the visuals shown in the app. 

The second image below shows the Accessibility Insights for Windows tool reporting that a UI Automation (UIA) PropertyChanged event is raised by a column header when the column is resorted. The property associated with the PropertyChanged event is ItemStatus, and the new value of the property is "Ascending".

When the Narrator screen reader encounters the column header, it will announce the current ItemStatus value. There may be a slight pause before the ItemStatus announcement. Narrator's "Read item advanced" command (CapsLock+0) can also be used to have the ItemStatus announced. If Narrator is located at the header when the sort order changes, Narrator will announce the new sort order at that time. 

Note that in some cases Narrator may announce the change in state, and then announce the new state again. That duplication of announcement is not something an app builder should spend time on trying to avoid.


![Alt text](WPFDataGridSorted/Assets/WPFDataGrid_AIWinProperties.png?raw=true "The AIWin tool reporting the UIA properties of a column header.")


![Alt text](WPFDataGridSorted/Assets/WPFDataGrid_AIWinEvents.png?raw=true "The AIWin tool reporting that a UIA PropertyChanged event is raised when a column is re-sorted.")
