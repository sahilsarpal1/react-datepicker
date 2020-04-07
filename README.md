### DateRangePickerComponent

It is a custom component used for the integration of Date Range. It is available inside the shared folder. No environment changes required. 

#### Steps to integrate:
- Install the required dependencies using the following command:
`$ npm install`

- Add the following import to the component (relative path to the component) like:
`import DateRangePickerComponent from '../../shared/component/date_range_component';`

- The most basic use of the DateRangePickerComponent can be described with (use inside the render method):
`<DateRangePickerComponent updateDatesChange = {this.updateDatesChange}/>`
                    
####Properties & Values:
Below details some helpful properties and values that are available:

| Property  | Data Type | Description |  Default  | Required |
| :---------- |:-----------:| -------------:| ----------:| -----------:|
| startDate  | momentObj | Start date of the date range |null | yes |
| endDate   | momentObj        |   End date of the date range |null | yes |
| error         | boolean        |    Check failed validation, true for success and false for failure |false| no |
| minDate   | momentObj        |   The minimum selectable date |null | no |
| maxDate  | momentObj      |    The maximum selectable date |null | no |
| updateDatesChange   | function       |   Callback method to set start and end date |N/A |yes |

####Example:
Use following example to integrate the component:

#####Callback method that sets states:
```javascript
updateDatesChange = (startDate, endDate) => {
		this.setState({
    			startDate: startDate,
    			endDate: endDate
  		})
}
```
#####Integration in render method:
```javascript
<DateRangePickerComponent
		startDate = {moment()}
		endDate = {null}
		minDate = {null}
		maxDate = {null}
		error = {false}
		updateDatesChange = {this.updateDatesChange}/>
```

