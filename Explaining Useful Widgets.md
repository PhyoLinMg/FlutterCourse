### Explaining Useful Widgets

- [Container](#container)
-  [Padding](#padding)
-  [Margin](#margin)
- [Scaffold](#scaffold)
- [Button(ImageButton, OutlineButton)](#buttonimagebutton-outlinebutton)
- [MaterialApp](#materialapp) 
- [Text](#text) 
- [Image(Both Network and Asset)](#imageboth-network-and-asset) 
- [Expanded](#expanded) 
- [Rows and Columns](#rows-and-columns)
-  [ListView/GridView](#listviewgridview)
-  [SingleChildScrollView](#singlechildscrollview)

## Container

Container တွေဆိုတာက margin,padding , width, height တွေစတဲ့ attribute တွေကို သူ့ရဲ့ နောက်မျိုုးဆက် widget တွေကို support ပေးတဲ့ widget ပါ။

မျက်လုံးထဲမြင်အောင်ပြောရရင် ဒီလိုမျိုုးပါ။





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

```
Padding(
)
```





## Margin

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

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

## Button(ImageButton, OutlineButton)

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

## MaterialApp

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

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

## Image(Both Network and Asset)

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

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

Helo world

gg

wee

jefkjek

kejfkejf

efkjekfj

kfjekfjek

ekjfkejfkej

fkejfkejfkej

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