# radar_scan


Step 1. Add it in your root build.gradle at the end of repositories:


    allprojects {
		repositories {
			...
			maven { url 'https://www.jitpack.io' }
		}
	}
	
  
  
  
  
  
  
   Step 2. Add the dependency
  
  
  
  
  
  
  
  
	dependencies {
	        implementation 'com.github.posakya:radar_scan:0.1'
	}
  
  Step 3. use this in colors.xml to change the circle stroke color (optional) by default it's white
  
  
     <color name="stroke_color">#your_color_code</color>
  
  
  Step 4. Add this to your xml file
  
      <com.ar_tech.radar_scan_view.RadarView
        android:layout_centerInParent="true"
        android:id="@+id/radarView"
        android:layout_width="300dp"
        android:layout_height="300dp"
        />
        
  Step 5. Add this to your activity or use it on fragment to show circle and control the animation
     
      
       RadarView mRadarView = null;
       mRadarView = findViewById(R.id.radarView);
       mRadarView.setShowCircles(true);
      
       /*
       to start animation
       */
       
       if (mRadarView != null)
         mRadarView.startAnimation();
                    
       /*
       to stop animation
       */
       
       if (mRadarView != null)
         mRadarView.stopAnimation();
      
      
