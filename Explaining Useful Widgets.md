

### Explaining Useful Widgets

- [Container](#container)
-  [Padding](#padding)
-  [Card](#card)
- [Scaffold](#scaffold)
- [Button](#button)
- [TextFiled](#textfield) 
- [Text](#text) 
- [Image(Both Network and Asset)](#imageboth-network-and-asset) 
- [Expanded](#expanded) 
- [Rows and Columns](#rows-and-columns)
-  [ListView/GridView](#listviewgridview)
-  [SingleChildScrollView](#singlechildscrollview)

## Container

Container တွေဆိုတာက margin,padding ,background color, width, height တွေစတဲ့ attribute တွေကို သူ့ရဲ့ နောက်မျိုုးဆက် widget တွေကို support ပေးတဲ့ widget ပါ။

မျက်လုံးထဲမြင်အောင်ပြောရရင် ဒီလိုမျိုုးပါ။

![Container](https://static.javatpoint.com/tutorial/flutter/images/flutter-container.png)

```dart
Container(
	width: 200.0,  
    height: 100.0,  
    color: Colors.green,   
    padding: EdgeInsets.all(35),  
    margin: EdgeInsets.all(20),  
    child:Text("Hello world"),
)
```

ပြီးတော့ ကျန်တဲ့ Properties တွေကို လိုက်လုပ်ကြည့်ကြမယ်

**Alignment**

Container ရဲ့ Alignment ကိုညှိတာပါ။ 

```dart
Container(
	color:Colors.green,
    alignment:Alignment.center,
    child:Text("Hello")
)
```

**Decoration**

Containerရဲ့ Decoration ကတော့ သူ့ရဲ့ နောက်မျိုးဆက် Widget ကို နောက်က‌နေ Decorate လုပ်ပေးတာပေါ့

ဘယ်လိုမျိုုးလဲဆိုတော့

```dart
Container(
	decoration:BoxDecoration(
		border: Border.all(color: Colors.black, width: 4),  
    borderRadius: BorderRadius.circular(8),  
    boxShadow: [  
            new BoxShadow(color: Colors.green, 					offset: new Offset(6.0, 6.0),),  
        ],
	),
	child:Text("Hello world")
)
```

BoxDecoration အကြောင်းသိချင်ရင်တော့ [ဒီမှာ](https://www.woolha.com/tutorials/flutter-using-boxdecoration-examples) ကြည့်လို့ရပါတယ်

အကယ်၍မှ Container အကြောင်း အသေးစိတ်သိချင်သေးတယ်ဆိုရင်တော့ [ဒီမှာ](https://www.javatpoint.com/flutter-container) ဆက်လေ့လာလို့ရပါတယ်။

ဆရာအနေနဲ့ လိုက်ပြပေးတာပိုကောင်းပါလိမ့်မယ်။ Lecture မှာ။



## Padding

ကိုဘယ်လိုအချိန်မှာသုံးသလဲဆိုတော့ widget တစ်ခုနဲ့ တစ်ခုကို နေရာလေးခြားချင်တဲ့‌ နေရာကျရင် သုံးပါတယ်။

```dart
Padding(
    padding:EdgeInsets.all(8),
	child:Text("Hello world")
)
```

ဒီ ကုဒ်ကို ကြည့်လိုက်ရင် ကျွန်တော်တို့သည် Text("Hello world")ရဲ့ ဘေးမှာ 8 စီခြားသွားတာပေါ့

all လည်းရှိသေးသလို direction နဲ့လည်းသွားလို့ရပါသေးတယ် သီးသန့် ဘယ်ကိုပဲ နေရာခြားချင်တယ် အပေါ်ကိုပဲ ခြားချင်တယ်ဆိုလည်းရပါတယ်။

```
//This is the one with directions(horizontal and vertical)
Padding(
	padding:EdgeInsets.symmetrics(horizontal:2,vertical:8)
	child:Text("Hello world")
)
```

![alt text](https://i1.wp.com/androidride.com/wp-content/uploads/2020/09/flutter-padding-symmetric.png?resize=440%2C369)



ပြီးတော့ တစ်ခုချင်းဆီဆို only နဲ့သုံးလို့ရတယ်

```dart
Padding(
	 padding: const EdgeInsets.only(
      left: 40,
      top: 20,
      right: 40,
      bottom: 20,
    ),
	child:Text("Hello world")
)
```



## Card

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

## Scaffold

Flutter Scaffold ကို‌တော့ application ရဲ့ အခြေခံ layout လို့ပြောလို့ရပါတယ်။ Device Screen တစ်ခုလုံးကို ရယူနိုင်ထားပါတယ်။ သူ့ဆီကနေမှ သူ့နောက်မျိုးဆက် widget တွေဟာ UI လှလှနဲ့ ဆက်ပြီးအလုပ်လုပ်နိုင်နေတာဖြစ်ပါတယ်။

သူ့ရဲ့ main သုံးတဲ့ လူသုံးအရမ်းများတဲ့ အရာတွေရှိပါတယ်။ ဒါတွေကတော့

- AppBar
- Body
- Floating Action Button
- Drawer
- Bottom Navigation Bar

**AppBar **

Appbar ကတော့ ဒီလိုပုံစံမျိုးဖြစ်တယ်။

![Appbar](https://res.cloudinary.com/practicaldev/image/fetch/s--GEMZUPIX--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/745oviezhc20albt7vtc.jpg)

ဒါမျိုးကိုဘယ်လိုရေးမလဲဆိုတော့ အောက်ကလိုရေးလို့ရတယ်။

```dart
Widget build(BuildContext context)   
{  
  return Scaffold(  
    appBar: AppBar(  
      title: Text('First Flutter Application'),  
    ), );  
}  
```

**Body**

body ကတော့ appbar အောက်က အဖြူရောင်နေရာလေးပါ။ အဲမှာ widget တွေထပ်တိုးပြီးရေးလို့ရပါတယ်။

```dart
Widget build(BuildContext context) {   
return Scaffold(   
    appBar: AppBar(   
    title: Text('First Flutter Application'),   
    ),   
    body: Center(   
    child: Text("Welcome to Javatpoint",   
        style: TextStyle( color: Colors.black, fontSize: 30.0,   
        ),   
         ),   
    ),  
}  
```

**Floating Action Button**

ပုံတွေနဲ့ ပြတာပိုမြင်မယ်လို့ ယူဆတဲ့အတွက် ပြထားတာဖြစ်ပါတယ်

![Floating action button](https://miro.medium.com/max/1580/1*8SWhPZtGxC1jSij4lGGHWQ.png)

ဘယ်လိုရေးမလဲဆိုတာကတော့ အောက်မှာပြပေးထားပါတယ်။

```dart
Widget build(BuildContext context) {   
  return Scaffold(   
    appBar: AppBar(title: Text('First Flutter Application')),   
    body: Center(   
        child: Text("Welcome!!"),   
    ),   
    floatingActionButton: FloatingActionButton(   
        elevation: 8.0,   
        child: Icon(Icons.add),   
        onPressed: (){   
           print('I am Floating Action Button');  
        }   
    );   
}  
```

**Drawer**

သူကဘယ်လိုမျိုးလဲဆိုတော့ ဒီလိုမျိုုးလေး

![Drawer](https://miro.medium.com/max/1440/1*GLtBR5juNDdlp0u2NAGv-g.png)

ဘယ်လို ရေးမလဲဆိုရင် Scaffold ထဲက drawer(parameter) ရှိတယ်။ အဲမှာ ‌ရေးရမှာပေါ့နော်

```dart
Scaffold(
	drawer:Drawer(
    	child:Widgets()
  	)
)
```



**Bottom Navigation Bar**

Bottom Navigation bar ကို ပုံပဲပြထားဦးမယ်။ နည်းနည်းခက်လို့ ရေးရမှာ

![Bottom Navigation Bar](https://brainsandbeards.com/static/d189b48add3cbd63d126aafb3e81320d/d3ba7/bottom_nav.png)



## Button

Flutter မှာ Button ခလုတ်တွေအများကြီးရှိပါတယ်

- Flat Button
- Raised Button
- Floating Button
- Drop Down Button
- Icon Button
- Outline Button
- PopupMenu Button

**Flat Button**

Text Label ပဲပါတဲ့ Button တစ်ခုဖြစ်တယ်။ ဘာမှ Decoration လောက်လောက်လားလား မပါပဲနဲ့ Elevation ခေါ်တဲ့ ‌ဖောင်းကြွ လည်းမပါဘူး။ 

```dart
FlatButton(  
     child: Text('SignUp', style: TextStyle(fontSize: 20.0),),  
     onPressed: () {},  
)
```

Result ကတော့

![Flat Button Example](https://static.javatpoint.com/tutorial/flutter/images/flutter-buttons.png)





**Raised Button**

ဒါကတော့ Material Widget ပေါ်မှာ အခြေခံထားတဲ့ Flat Button နဲ့ ဆင်တူတဲ့ Button တစ်ခုဖြစ်တယ်။ ဒါပေမဲ့ မတူတာတစ်ချက် က Elevation ခေါ်တဲ့ ဖောင်းကြွ ပါလာတယ်။ ပြီးတော့ attribute တွေလည်းပိုပါလာတယ်။Flat Button ထက်စာရင်။

ထူးခြားတာက onPressed() အပြင် onLongPress() ဆိုတဲ့ ခလုတ်နှိပ်တဲ့အခါ ခေါ်တဲ့ method 

```dart

```



![Raised Button Example]()

**Drop Down Button**

```dart

```

![Drop Down Button](https://static.javatpoint.com/tutorial/flutter/images/flutter-buttons6.png)

![Drop Down Button Selecting](https://static.javatpoint.com/tutorial/flutter/images/flutter-buttons7.png)

**Icon Button**

```dart

```

![Icon Button](https://static.javatpoint.com/tutorial/flutter/images/flutter-buttons8.png)

**Popup Menu Button**

```dart

```

![Popup Menu Button](https://static.javatpoint.com/tutorial/flutter/images/flutter-buttons10.png)

![Popup Menu Button Selecting](https://static.javatpoint.com/tutorial/flutter/images/flutter-buttons11.png)

**Outline Button**

```dart
```

![Outline Button](https://static.javatpoint.com/tutorial/flutter/images/flutter-buttons12.png)



အပြည့်အစုံ ကို [ဒီမှာ](https://www.javatpoint.com/flutter-buttons) ကြည့်လို့ရပါတယ်။





## TextField

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

## Text

Text ဆိုတဲ့ widget ကတော့ စာသားတွေကို ပြတဲ့နေရာမှာ သုံးတာပေါ့။ ဘယ်နေရာမှာပဲဖြစ်ဖြစ် စာကပြရတာကြီးပဲဆိုတော့ Text ကတော့ အရေးပါတဲ့ အရာပေါ့။

အဲတော့ တစ်ချက်လောက်ဘယ်လိုသုံးတယ်ဆိုတာ ကြည့်ကြည့်ရအောင်။

```dart
Widget build(BuildContext context) {  
    return Scaffold(  
      appBar: AppBar(  
          title:Text("Text Widget Example")  
      ),  
      body: Center(  
          child:Text("Welcome to Javatpoint")  
      ),  
    );  
}  
```

Text မှာ ဘာတွေပါလဲဆိုတာကိုတစ်ချက် List ထုတ်ပြပါမယ်။

အဲမှာတစ်ချက်ပြောချင်လာတာက Flutter က open-source ဖြစ်တယ်။ အဲတာမလို့ source code ကိုတတ်နိုင်သလောက်၀င်ဖတ်ကြည့်ပါ။ ပညာရတာပေါ့။

အခုချိန်(စာရေးနေတဲ့အချိန် အရေးအခင်းဖြစ်နေတဲ့အချိန်ဆိုတော့ စာလည်းလုပ်ချင်စိတ်မရှိ စာဖတ်ဖို့နေရာ‌လေးတစ်ခုဖန်တီးပေးချင်လို့သာ ကြိုးစားရေးနေတာပါ) မှာ လုပ်ချင်စိတ်မရှိကြပါဘူး။

အဲတော့ ပြောချင်တာလည်း ရှည်သွားပြီဆိုတော့ ပြန်စကြရအောင်။

```dart
const Text(String data,{  
    Key key,  
    TextStyle style,  
    StrutStyle strutStyle,  
    TextAlign textAlign,  
    TextDirection textDirection,  
    TextOverflow overflow,  
    bool softWrap,  
    double textScaleFactor,  
    int maxLines,  
    String semanticsLabel,  
    TextWidthBasis textWidthBasis,  
    TextHeightBehavior textHeightBehavior  
    }  
)  
```

 ကျွန်တော် ဒီမှာ လူသုံးများတဲ့ အရာတွေဖြစ်တဲ့ Text Style,Text Align , TextDirection, maxLines, TextOverFlow တွေကို ပြောသွားရှင်းသွားမှာဖြစ်ပါတယ်။

**Text Style**

- background->Text ရဲ့ နောက်ခံအနေနဲ့ လုပ်ချင်တာရှိရင် ဒီဟာကို သုံးလို့ရတယ်။
- fontWeight->Text ရဲ့ အထူကို သတ်မှတ်တာပါ။
- fontSize->Text Font အရွယ်အစား ကိုချိန်ချင်ရင် သုံးတယ်
- fontFamily->Text Font အမျိုးအစားတွေကို ပြောင်းချင်ရင်သုံးတယ်။လုပ်နည်း အပြည့်အစုံကို [ဒီမှာ](https://www.youtube.com/watch?v=fDRtpjHfOuw) ကြည့်နိုင်ပါတယ်။
- fontStyle->Font ရဲ့ စတိုင်ပေါ့။ နမူနာအနေနဲ့ဆိုရင် (Bold, italic)
- Color->Text ရဲ့ အရောင် ကိုပြောင်းချင်တဲ့အခါကျရင် သုံးရပါမယ်၊
- letterSpacing->စာတစ်လုံးချင်းရဲ့ အကွာအ‌ေ၀းကို သတ်မှတ်ပေးတာပါ။
- shadows->Text ရဲ့ နောက်မှာ shadow ထည့်တာပါ

**Text Align**

Text ကိုဘယ်နေရာမှာ ထားမလဲဆိုတာ ဒီလိုမျိုးပါ။

```dart
Text("text",textAlign:TextAlign.left)
```

**maxLines**

Text widget မှာထည့်မယ့် String တစ်ခုဟာ အရမ်းရှည်နေပြီဆိုရင် ပြမဲ့ line limit ကို ကန့်သတ်လိုက်တာပေါ့့

```dart
Text("Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime mollitia,
molestiae quas vel sint commodi repudiandae consequuntur voluptatum laborum
numquam blanditiis harum quisquam eius sed odit fugiat iusto fuga praesentium
optio, eaque rerum! Provident similique accusantium nemo autem", maxLines:2)
```



**TextOverFlow**

အပေါ် ကလို maxLines ထည့်လိုက်ရင် ကျန်တဲ့ စာသားတွေကို ဘယ်လို ပြမလဲဆိုတဲ့မေးခွန်းက ၀င်လာမယ်။ အဲမေးခွန်းအတွက် ဒီ TextOverFlow ကဖြေရှင်းပေးထားတယ်။

အဲမှာ အသုံးများတဲ့ အရာလေးတွေကို ပြထားပါမယ်။ [လက်တွေ့]()  ပြထားတာရှိရင် ပိုနားလည်ရလွယ်ပါလိမ့်မယ်။

စာနဲ့လည်းရေးထားပါမယ်။clip, ellipsis , fade နဲ့ visible တို့ဖြစ်ပါတယ်။

```DART
Text("Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime mollitia,
molestiae quas vel sint commodi repudiandae consequuntur voluptatum laborum
numquam blanditiis harum quisquam eius sed odit fugiat iusto fuga praesentium
optio, eaque rerum! Provident similique accusantium nemo autem", maxLines:2,overflow:TextOverflow.ellipsis,)
```



## Image(Both Network and Asset)

Image တွေကတော့ Photo တွေပြဖို့အတွက် သုံးတဲ့ widget ပဲဖြစ်ပါတယ်။ သူ့မှာ နှစ်မျိုးရှိပါတယ်။ AssetImage ဆိုတာ မိမိဖုန်းထဲမှာ ရှိနေတဲ့ ပုံ သို့ application မှာထည့်ထားတဲ့ ပုံတွေကို ပြဖို့သုံးတာဖြစ်ပါတယ်။ ရေးနည်းကိုလည်း အောက်မှာတစ်ခါတည်းရှင်းသွားပါမယ်။ ထည့်ပေးရမှာကတော့ ပြချင်တဲ့ ပုံရဲ့ ပတ်လမ်းကြောင်းကို ထည့်ပေးရမှာပါ။

Image ကို Locally ပြချင်ရင်

Folder structure assets-> images ကိုဆောက်, images အောက်မှာ ပုံတွေထည့့်

pubsepc.yaml မှာ ဒီလိုလေးသွားရေးပေး

```dart
flutter:
   assets:
     - assets/images/
```

ပြီးရင် ကျန်တာဆက်ရေးလို့ ရပြီ။

```dart
Image.asset('assets/images/my_profile.png')
```

Network Imageဆိုတာ အင်တာနက်မှာရှိတဲ့ ပုံတွေကိုပြမှာဖြစ်ပါတယ်။ လိုအပ်တာကတော့ အင်တာနက်မှာ ရှိတဲ့ image url ကို ထည့်ပေးရပါမယ်။ အင်တာနက်ကနေ ဆွဲပြရတာကြောင့် ပုံပေါ် ဖို့ ခဏတော့စောင့်ရပါလိမ့်မယ်။

ရေးရင်တော့ ဒီလိုရေးရပါလိမ့်မယ်။

```dart
Image.network("https://static.wikia.nocookie.net/haikyuu/images/a/a4/Haikyu_S4.jpg/revision/latest?cb=20200111012854")
```

ပြီး container နောက်မှာ decoration အနေနဲ့ image တွေထားပြလို့ရပါသေးတယ်။ အဲမှာတော့ တစ်ခါတည်း နှစ်ခုလုံးလုပ်ပြသွားပါမယ်။

ဒီတစ်ခုက AssetImage အတွက်ပါ။

```DART
Container(
	height: 120.0,
    width: 120.0,
    decoration: BoxDecoration(
      	image: DecorationImage(
          image: AssetImage(
              'assets/images/my_profile.png'),
        ),
      ),
)
```

 ဒီတစ်ခုကတော့ NetworkImage အတွက်ပါ။

```dart
Container(
	height: 120.0,
    width: 120.0,
    decoration: BoxDecoration(
      	image: DecorationImage(
          image: NetworkImage( "https://static.wikia.nocookie.net/haikyuu/images/a/a4/Haikyu_S4.jpg/revision/latest?cb=20200111012854"),
        ),
      ),
)
```





## Expanded

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

## Rows and Columns

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

## ListView/GridView

ListView , GridView တွေဟာ ကျွန်တော်တို့ပြစရာ အရှည်ကြီး ရှိတဲ့ ဟာတွေ ပြချင်ရင် သုံးပါတယ်။

TIP::ကျွန်တော်ကတော့ သူတို့ရဲ့ လုပ်ပုံ လုပ်နည်းလေးတွေသိချင်လို့ရင် Flutter Widget of the week ကဟာတွေကြည့်ဖြစ်တယ်။ Listview နဲ့ GridView အကြောင်းလေးတွေ ကြည့်ကြည့်ပါ။









## SingleChildScrollView

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej