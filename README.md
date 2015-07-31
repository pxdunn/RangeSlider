RangeSlider for Angular & Foundation
====================================

Range Sliders for Angular & Foundation5. The only real dependency outside of Angular is Foundation RangeSlider SSS

 - should work on Firefox,Chrome,Safari with mouse,keyboard and touchscreen, does not work on old version of IE.

Project :
 - demo: http://breizhme.net/rangeslider/demo/
 - home: https://github.com/fulup-bzh/RangeSlider

This RangeSlider is Angular ported version for http://foundation.zurb.com/docs/components/range_slider.html

Installation
-------------

```
$ bower install RangeSlider --save
```


Usage  <range-slider>
---------------------
```
   <range-slider
      id="my-slider-name"                     // only use as an argument to callback
      class="my-custom-class"                 // default class is bzm-range-slider
      placeholder="Track Date Selection"      // place holder for date readonly input zone

      <!-- Foundation classes -->
      class="radius"                          // check Zurn foundation doc for further info.
      class="bzm-handle-display"              // increase handle width to hold slider current value

      <!-- Angular Scope Variables -->
      callback="myCallBack"                    // $scope.myCallBack(sliderhandle) is called when ever slider handle blur
      formatter="SliderFormatCB"               // $scope.myFormatter(value, sliderid) when exist is call when ever slider handle moves. Should return external form of slider value.
      ng-model="xxxxxx"                        // xxx Must be defined, script will store a new RangerObject within provided ng-model variable.
      start-at="ScopeVar"                      // Dynamic limitation when slider is constrains by an external componant [ex: check in/out]
      stop-at="ScopeVar"                       // Idem but for end.

      <!-- Angular Directive Attributes -->
      not-less="integer"                       // Fixed starting value for slider [default 0]
      not-more="integer"                       // Fixed end value for sliders [default 100]
      by-step="+-integer"                      // If by-step is >0 then slider use it as step-value, when negative use it for decimal precision
      display-target="handle"                  // display slider external formated value in the handle [requirer calss="bzm-handle-display"]
      dual-handles='true'                      // add a second handle to slider for min/max range
      initial='value|[start/stop]'             // slider initial value [dual-handles] may have initial values

   /></range-slider>


   within JS app ng-model=xxxx is a RangerObject.

    xxxx.getValue(0|1)    return current value of RangeSlider for chosen handle [default is handle:0]
    xxxx.getView(0|1)     equivalement to getValue but for external representation of handle value after formatter callback
    xxxx.setValue(0|1)    set the value for a chosen handle
    xxxx.getRelative(0|1) return relative position of chosen handle



```
