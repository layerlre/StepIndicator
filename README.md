[![Build Status](https://api.travis-ci.org/layerlre/StepIndicator.svg?branch=master)](https://api.travis-ci.org/layerlre/StepIndicator) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.layer-net/step-indicator/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.layer-net/step-indicator) [![Methods Count](https://img.shields.io/badge/Methods and size-110 | 24 KB-e91e63.svg)](http://www.methodscount.com/?lib=com.layer-net%3Astep-indicator%3A1.0.0) 
# Android StepIndicator

Interactive step paging indicator widget, compatible with the ViewPager

![StepIndicator](https://github.com/layerlre/StepIndicator/raw/master/images/port4.gif)![StepIndicator](https://github.com/layerlre/StepIndicator/raw/master/images/port6.gif)
![StepIndicator](https://github.com/layerlre/StepIndicator/raw/master/images/land6.gif)
# Usage
  1. Include one of the widgets in your view. This should usually be placed
     adjacent to the `ViewPager` it represents.

        <com.layer_net.stepindicator.StepIndicator
            android:id="@+id/step_indicator"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="16dp"
            app:siBackgroundColor="@color/background_default"
            app:siStepColor="@color/step_default" />

  2. In your `onCreate` method (or `onCreateView` for a fragment), bind the
     indicator to the `ViewPager`.

           //Set the pager with an adapter
           ViewPager pager = (ViewPager)findViewById(R.id.pager);
           pager.setAdapter(new TestAdapter(getSupportFragmentManager()));

           //Bind the step indicator to the adapter
           StepIndicator stepIndicator = (StepIndicator) findViewById(R.id.step_indicator);
           stepIndicator.setupWithViewPager(pager);


**Public method on StepIndicator**
```java
    void setStepsCount(int stepCount)
    int getStepsCount()
    void setCurrentStepPosition(int currentStepPosition)
    int getCurrentStepPosition()
    void setRadius(int radius)
    int getRadius()
    void setupWithViewPager(ViewPager viewPager)
```

# Customization
 * `siStepColor` Color of the step indicator
 * `siCurrentStepColor` Color of the current step
 * `siBackgroundColor` Background color of the step indicator
 * `siTextColor` Background color of the step indicator
 * `siSecondaryTextColor` Background color of the step indicator
 * `siRadius` Radius of the step indicator
 * `siStrokeWidth` Stroke Width of a current step
 * `siStepCount` Size of step (With out ViewPager)

# Download
Download via Maven

        <dependency>
            <groupId>com.layer-net</groupId>
            <artifactId>step-indicator</artifactId>
            <version>1.0.0</version>
            <type>pom</type>
        </dependency>

or Gradle:

    compile 'com.layer-net:step-indicator:1.0.0'


# License

    Copyright 2016 layerlre

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

## Welcome to Fork.

For contributor, check `TODO` list.

1. Develop on **your branch** start from lasted commit on **[master](https://github.com/layerlre/StepIndicator)** branch.
2. Create pull request to **[dev](https://github.com/layerlre/StepIndicator/tree/dev)** branch.
