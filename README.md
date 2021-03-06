### Forked from and based on [bootstrap-datepicker](https://github.com/eternicode/bootstrap-datepicker/)

### Requirements

1. Notice that to use this very fork, a `data-date-format` attribute __MUST__ be presented in the `html` node in DOM. It's format could be, for example, `d/m/Y`.

2. Livety `Date` module is required.

3. This library MUST to be compiled/packed as a part of entries in Webpack.


### Changes

In addition to the original method and options, this fork provided:

#### Options:

* `parent`

jQuery selector to the parent node of which the date picker is to be appended to.

#### Method:

* `.datepicker('setMinViewMode', minView)`

Set min view mode for the selected date picker. Parameter `minView` indicates min view mode, i.e. 0 === day, 1 === month, 2 === year.

* `.datepicker('setLastDayOfMonth', trueOrFalse)`

When `setLastDayOfMonth` is set to `true`, date picker will automatically calculate and append the last date of the selected month to the return/output date value. Otherwise, the first date will be appended.

* `.datepicker('setStartDate', ceaseChangeDateEvent)` & `.datepicker('setEndDate', ceaseChangeDateEvent)`

An extra optional `ceaseChangeDateEvent` parameter is provided to `setStartDate` and `setEndDate` to prevent date picker instances from triggering `changeDate` event when start/end date get changed.

* `.datepicker('allowNotSureDate', trueOrFalse)`

When `trueOrFalse` is set to `true`, date picker adds a `not sure exact date` button to day view.

* `.datepicker('notSureDateText', text)`

Set the text shown on `not sure exact day` button.

* `.datepicker('beforeNotSureDate', function)`

Set the function to be triggered before date picker set-value event is triggered when clicking `not sure exact day` button.

* `.datepicker('afterNotSureDate', function)`

Set the function to be triggered after date picker set-value event is triggered when clicking `not sure exact day` button.

* `.datepicker('onSelectDate', function)`

Set the function to be triggered when selected a date.

* `.datepicker('setActiveMonth', monthNum)`

Highlight a month. `monthNum` is a 1-based month index.

* `.datepicker('setActiveYear', year)`

Limit the year when highlighting month.


* `.datepicker('setDatesDisabled', [dateString])`

Disable the given dates.

* `.datepicker('updateMonth', dateString, ceaseEvent)`

Update date in month mode. Notice that `dateString` has to be in dashed format, i.e. YYYY-mm-dd

If `ceaseEvent` is `true`, the `change` event will not be triggered.

* `.datepicker('clear')`

Clear the date picker.
