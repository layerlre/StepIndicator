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
            <version>0.9.1</version>
            <type>pom</type>
        </dependency>

or Gradle:

    compile 'com.layer-net:step-indicator:0.9.1'
