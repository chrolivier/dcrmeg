v1.0.6.1
========

Bug Fixes:
1. Configuration Record does not display list of entities. Dynamics 365 Online version 1612 (8.2.1.207)
2. Synchronuoos Associating records Web API call was missing a parameter

Additions:
1. Added an option to the configuration to set the minimum width of the columns. Default 15 px. The grid will attempt to display all columns within the viewable area. If a column width is specified in the configuration, it will be used as long as it is not less than the minimum column width specified in the configuration. Better browser horizontal resize handling.
2. Added an option to the configuration to allow using a custom identifier for each grid. The custom identifier is passed to all the JS call backs. This is for cases where multiple grids exist on the same form and a need to identify originating grid for the JS call backs.
3. Added borders to grid cells and teawked CSS based on the browser.

v1.0.6.0
========

Bug Fix:

1. DCrmEgGridOnBeforeFetchRecords JS callback was throwing "Unable to get property 'Label' of undefined or null reference".
2. JS error "cas" is undefined or null

v1.0.5.9
========

Bug Fixes:
1. Unable to add more than 27 fields in the configuration.
2. Opening more than one sub grid and refreshing one of them within the main grid was destroying the other sub grids. (V 1.0.5.8 Grid layout is being destroyed on refresh)
3. Issue with window.parent.DCrmEgGridOnload. Unable to set the last option set to read-only.
4. Was unable to remove a selected field from the grid configuration if the field was deleted from the selected entity.

Additions:
1. Web API support for CRM 2016 and Dynamics 365. For CRM versions prior to 2016, the grid uses soap end points (XrmServiceToolkit). For Web API, I have added WEBAPI-SDK.js. Minimum API version supported v8.1. This version number is updated after during the grid initialization to match current Web API version in your CRM environment via a call to versionNumber function.
2. Now you can preset aggregates for numeric fields from the configuration. I have also added the functionality to the grid to auto update aggregate values that were not preset (manually invoked using the aggregate button menu) in the configuration (after an update, delete, and clone operations).
3. Sticky header and footer. The grid header and footer remain static during scrolling.
4. Enforced minimum width for column headers 100px. Horizontal scroll bar is visible if the width of the grid is greater than it's container
