# marquee_text

Flutter Text widget that scrolls infinitely. Provides speed that scroll 
and the Way of use just like Text and RichText in in Flutter.

## Screen
<img src="https://github.com/bytedance/marquee_text/blob/master/doc/image.gif" width="320">


## Example

```
import 'package:flutter/material.dart';
import 'package:marquee_text/marquee_text.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: HomePage(),
    );
  }
}

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return new Scaffold(
        appBar: new AppBar(
          title: new Text("跑马灯"),
        ),
        body:  Container(
          alignment: Alignment.center,
          child:  Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              MarqueeText("跑马灯控件，默认字体和颜色"),
              MarqueeText.rich(TextSpan(
                  text: "跑马灯控件，设置字体和颜色",
                  style: TextStyle(fontSize: 11.0, color: Colors.red)))
            ],
          ),
        ));
  }
}
```



