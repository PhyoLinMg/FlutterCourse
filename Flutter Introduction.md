## Flutter Introduction

Flutter ဆိုတာဘာကြီးလဲ ဘာလုပ်တာလဲ ဘာတွေနဲ့ ဖွဲ့ထားသလဲ နောက်ကွယ်ကအလုပ်လုပ်ပုံ အကျဥ်းတွေကို မိတ်ဆက်သွားမှာဖြစ်ပါတယ်

#### What is Flutter?

Flutter  ဆိုတာ mobile(Android,iOS)နဲ့ Desktop Application(Windows,Linux) တွေမှာ သုံးနိုင်မယ့် application တွေကို ဖန်တီးနိုင်ဖို့အတွက်  google ကထွင်ထားပေးတဲ့ Framework တစ်မျိုးပါ။ အဓိကအသုံးပြုတဲ့ Language ကတော့ Dart ပဲဖြစ်ပါတယ်။

Native Performance ရလို့လည်း နာမည်ကြီးလာတာလို့ ပြောလို့ရပါတယ်

#### Flutter ကို ဘာတွေနဲ့ ဖွဲ့ထားတာတုန်း

Flutterကို widgetတွေနဲ့ပဲဖွဲ့စည်းထားပါတယ်။ Flutter မှာပြောလေ့ရှိတာက Everything is a widget ပါ။ အဲတော့ အဲတာကြီးကဘာကြီးတုန်း???။

###### What is A widget?

Widget ဆိုတာကတော့ ဒီနေရာမှာ UI  တစ်ခုတည်းလို့သတ်မှတ်လို့မရတော့ဘူး။ Button, Text,Image, ပဲရှိတာမဟုတ်ပဲနဲ့ Flutter app အလုပ်လုပ်ဖို့ရှိသမျှ အရာအားလုံးဟာ Widget ဖြစ်တယ်။

Padding ဟာလည်း WIDGETပဲ။ Margin လည်းအတူတူပဲ။

###### Types of widget

Widget အမျိုးအစားကတော့ နှစ်ခုပဲရှိပါတယ်။ Stateful Widget နဲ့ Stateless Widget ပါ။

အဲနှစ်ခုကိုမြင်အောင်ပြောရရင်

Stateless Widget ကအသေပါ။ App Lifecycle မှာ ပြန်ပြောင်းလို့မရနိုင်ပါဘူး

Stateful Widget ကတော့အရှင်ပါ။ Value တွေပြောင်းပေးနိုင်တယ်။ UI state တွေပြောင်းပေးနိုင်တယ်။

အဲအကြောင်း Medium ဆောင်းပါး အပြည့်ကို [ဒီမှာ](https://medium.com/jay-tillu/4-what-is-widget-in-flutter-lets-clear-the-basics-first-82f501c8d0f0#:~:text=In%20flutter%2C%20Widget%20is%20a%20way%20to%20declare%20and%20construct%20UI.&text=A%20widget%20might%20display%20Something,and%20columns%20are%20also%20widgets.) ဖတ်ရှုနိုင်ပါတယ်။။



#### How Flutter works

Flutter ကဘယ်လို အလုပ်လုပ်လဲဆိုတာကို အကုန် ပြောပြနေရင် အရမ်းများသွားလိမ့်မယ်။ နားမလည်မှာလည်း များမယ်ထင်တယ်။



အကျဥ်းချုပ်ပြောမယ်ဆိုရင်တော့

1. Dart Engine ကိုသုံးပြီး Android နဲ့ iOS code တွေကို ပြောင်းလိုက်တယ်။
2. Flutter runner တွေက သက်ဆိုင်ရာ platform  ရဲ့ complier နဲ့ app ထုတ်ပေးတယ်။ ပြောင်းလိုက်တဲ့  code တွေကိုလည်း ပေါင်းထည့်ပေးနိုင်တယ်။
3. UI ကို Skia ဆိုတဲ့ 2D Graphics Rendering Library သုံးထားတဲ့ အတွက် GPU ကို အသုံးပြုတယ်။

အပြည့်အစုံဖတ်ချင်ရင်တော့ လေ့လာချင်ရင် [Official Documentation](https://flutter.dev/docs/resources/architectural-overview) နဲ့ [article](https://flutter.dev/docs/resources/architectural-overview) မှာကြည့်လို့ရပါတယ်။

