## AngularJS slider directive - Range List Fork

This is a fork of the original AngularJS slider directive by rzajac found here: https://github.com/rzajac/angularjs-slider

This repository is only stable for use as a Range List slider as detailed below.  This fork is not verified to work with other variations of the slider directive documented in the original repository.

This repository only offers one alternate use of the slider directive and is not meant to be merged back into the original library.

## Range List Slider

The Range List Slider version of the slider directive provides one new use case offering the following features/changes:

 - adds new rz-slider-range-list attribute which provides an array of strings representing custom values to be used as steps in slider
 - adds slider pips with labels - customizable for labeling every step or only first/last step
 - moves slider labels below to align with pips
 - removes use of ceil and floor values, instead using first and last array positions from rz-slider-range-list
 - sets the step value to 1 to correspond with each item in rz-slider-range-list array

## Example

```javascript
// In your controller
$scope.rangeSlider = {
    min: 1,
    max: 3,
    rangeList: ['0%', '50%', '75%', '90%', '100%' ]
};
```

```html
<rzslider
    rz-slider-model="rangeSlider.min"
    rz-slider-high="rangeSlider.max"
    rz-slider-range-list="rangeSlider.rangeList"
    rz-slider-tpl-url="rzSliderTpl.html"></rzslider>
```

## Directive attributes

**rz-slider-range-list**

> Array of strings representing custom values for slider range.  Min/Max values correspond to items in array while translations display string value of items in array.

**rz-slider-model**

> Model for low value slider. Corresponds to an item in rz-slider-range-list array

**rz-slider-high**

> Model for low value slider. Corresponds to an item in rz-slider-range-list array

**rz-show-mid-labels**

> boolean value to determine if middle pip labels are displayed.  Use when lables are very long strings
and you only want the cieling and floor values displayed.  Defaults to "true" if value is omitted.  Set to "false" to turn off middle pip labels.

## License

Licensed under the MIT license
