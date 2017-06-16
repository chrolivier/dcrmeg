v1.0.5.9

Bugs:

Unable to add more than 27 fields in the configuration.

Openning more than one sub grid and refreshing one of them within the main grid was destroying the other sub grids. (V 1.0.5.8 Grid layout is being destroyed on refresh)
Issue with window.parent.DCrmEgGridOnload. Was unable to set the last option set to read-only.

Issue with window.parent.DCrmEgGridOnload. Unable to set the last option set to read-only.

Was unable to remove a selected field from the grid configuration if the field was deleted from the selected entity.

Additions:

Web API support for CRM 2016 and Dynamics 365. For CRM versions prior to 2016, the grid uses soap end points (XrmServiceToolkit). For Web API, I have added WEBAPI-SDK.js. Minimum API version supported v8.1. This version number is updated after during the grid initialization to match current Web API version in your CRM environment via a call to versionNumber function.

Now you can pre set aggregates for numeric fields from the configuration. I have also added the functionality to the grid to auto update aggregate values that were not pre set (manually invoked using the aggregate button menu) in the configuration (after an update, delete, and clone operations).



