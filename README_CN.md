# marquee_text

一个支持文本和富文本的文本跑马灯控件。支持设置滚动速度并且使用方式和Flutter中的Text和RichText控件保持一致

## 截图
<img src="https://github.com/bytedance/marquee_text/blob/master/doc/image.gif" width="320">

## 例子

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


