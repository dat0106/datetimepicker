Official source:

https://android.googlesource.com/platform/frameworks/opt/datetimepicker/
(Android 4.3+)

#DateTimePicker 

DateTimePicker is a library which contains the beautiful DatePicker and TimePicker that can be seen in the new Google Agenda app.

**This picker is available for 2.1+**

You have a recurrence picker in the same style [here](https://github.com/Shusshu/Android-RecurrencePicker).

## WARNING

* Requires android-support-v4 and [NineOldAndroids][5]
* Accessibility is missing for DatePicker on all devices and Below ICS devices for TimePicker.
* Scroll adjustment is missing below ICS devices for TimePicker and DatePicker.

## Description

This library reproduces as much as possible the original picker contained in the new Google Agenda app.

![Example Image][1]

Or browse the [source code of the sample application][3] for a complete example of use.

## Including in your project

Last version is 0.0.5

Just add the following in your build.gradle

```groovy
repositories{
    maven {
        url "https://jitpack.io"
    }
}

dependencies {
     compile 'com.github.dat0106:datetimepicker:0.0.5'
}
```

## Usage

1. **Basic**

  Date Picker
  ```java
  DatePickerDialog datePickerDialog = DatePickerDialog.newInstance(new OnDateSetListener() {...}, year, month, day);
  ```

  Time Picker
  ```java
  TimePickerDialog timePickerDialog = TimePickerDialog.newInstance(new TimePickerDialog.OnTimeSetListener() {...}, hourOfDay, minute, is24HourMode);
  ```
  For more info look at the source code of the provided sample [here][4]

2. **Change Dialog Primary Color**

  Override the following colors in your project

  ```xml
  <color name="datepicker_primary">#ff4CAF50</color>
  <color name="datepicker_primary_dark">#ff388E3C</color>
  ```

3. **Set Min/Max Date**
  ```java
  datePickerDialog.setMinDate(new SimpleMonthAdapter.CalendarDay(2015, 4, 17));
  datePickerDialog.setMaxDate(new SimpleMonthAdapter.CalendarDay(2015, 4, 20));
  ```

4. **Change Dark Theme Dialog **

   ![Example Image][7] ![Example Image][8]
  Override the following colors in your project

  ```xml
    <color name="white">#424242</color>
    <color name="grey">#303030</color>
    <color name="circle_background">#303030</color>
    <color name="line_background">#303030</color>
    <color name="done_text_color_normal">@color/datepicker_primary</color>
    <color name="done_text_color_disabled">#ffcccccc</color>
    <color name="date_picker_text_normal">#ff999999</color>
    <color name="calendar_header">@color/datepicker_primary_dark</color>
    <color name="date_picker_view_animator">#424242</color>

    <color name="ampm_text_color">#8c8c8c</color>
    <color name="numbers_text_color">#8c8c8c</color>

    <color name="transparent_white">#7F000000</color>
    <color name="transparent_black">#7F000000</color>

    <color name="datepicker_primary">#ff009688</color>
    <color name="datepicker_primary_dark">#ff00796b</color>
  ```

## Acknowledgements

* Thanks to Google for this beautiful picker

## License

    Copyright 2013 Flavien Laurent (DatePicker) edisonw (TimePicker)

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

 [1]: https://raw.githubusercontent.com/dat0106/datetimepicker/master/graphics/img1.png
 [3]: https://github.com/dat0106/datetimepicker/tree/master/datetimepicker-sample
 [4]: https://github.com/dat0106/datetimepicker/blob/master/datetimepicker-sample/src/com/fourmob/datetimepicker/sample/MainActivity.java
 [5]: http://nineoldandroids.com/
 [6]: https://raw.githubusercontent.com/dat0106/datetimepicker/master/document/device-2015-07-16-221229.png
 [7]: https://raw.githubusercontent.com/dat0106/datetimepicker/master/document/device-2015-07-16-224523.png
 [8]: https://raw.githubusercontent.com/dat0106/datetimepicker/master/document/device-2015-07-16-224546.png
