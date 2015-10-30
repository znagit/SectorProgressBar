#SectorProgressBar

### Examples
Here are some examples of how these progressbars could look like:

![example](http://h.hiphotos.baidu.com/image/pic/item/37d3d539b6003af32501de92332ac65c1138b68c.jpg)

## Usage
### Gradle
This library now works with gradle and will soon be available on the central maven repository. For the moment its on jCenter at [Bintray](https://bintray.com/mrwonderman/maven/squareprogressbar/view). Just add the following repository to your root build.gradle:

    allprojects {
        repositories {
            jcenter()
            maven { url "https://jcenter.bintray.com" }
        }
    }

Then in your app build.gradle:

    dependencies {
        // other repos ...
        compile 'com.github.znacloud:sectorprogressbar:1.0.0'
    }

### Code
After adding the gradle depedency from above you can go to your xml layout and add the following code for a squareprogressbar:

    <com.github.znacloud.SectorProgressBar xmlns:app="http://schemas.android.com/apk/res-auto"
            android:id="@+id/spb_progress"
            android:layout_width="48dp"
            android:layout_height="48dp"
            app:progress="0"
            app:borderWidth="2dp"
            app:borderColor="@color/colorPrimary"
            app:sectorBackgroundColor="@color/colorAccent"
            app:sectorColor="@color/colorPrimaryDark"
            app:showTextProgress="true"/>
    
To set some basic settings use the following java-code:

    mCirclePbr = (SectorProgressBar) findViewById(R.id.spb_progress);
    //set custom attribute
    mCirclePbr.setSectorBackgroundColor(Color.parseColor("#55000000"));
    mCirclePbr.setBorderColor(Color.GRAY);
    mCirclePbr.setBorderWidth(4);
    mCirclePbr.setShowTextPercent(true);
    mCirclePbr.setProgress(20);
    

    
    