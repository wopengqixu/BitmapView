# BitmapView
Android library, display any resolution JPG PNG pictures, support rotate gesture

## Features
- scale
- scroll and fling
- rotate
- use BitmapRegionDecoder to support any resolution JPG/PNG

# Gradle Dependency
```gradle
dependencies {
    compile 'org.qiibeta.views:bitmapview:1.0.0'
}
```
## Sample Application
see sample

## Sample Usage
```java

@Override
public void onCreate(Bundle savedInstanceState) {
  super.onCreate(savedInstanceState);
	setContentView(R.layout.activity_main);

  String path=""; //the actual file path
  Bitmap thumbnailBitmap=null;
  GestureBitmapView bitmapView=(GestureBitmapView)findViewById(R.id.bv);
  bitmapView.setBitmapSource(BitmapSource.newInstance(Uri.parse(path),thumbnailBitmap));
}
```

## Issues With ViewPager
```java
public class FixViewPager extends ViewPager {
    public FixViewPager(Context context) {
        super(context);
    }

    public FixViewPager(Context context, AttributeSet attrs) {
        super(context, attrs);
    }

    @Override
    public boolean onInterceptTouchEvent(MotionEvent ev) {
        try {
            return super.onInterceptTouchEvent(ev);
        } catch (Exception ignored) {

        }
        return false;
    }
}
```
## License

    Copyright 2016 qii

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.