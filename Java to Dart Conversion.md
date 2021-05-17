### Java to Dart Conversion

ဒီနေရာမှာတော့ နည်းနည်းပဲပြောပါမယ် ဘာလို့လဲဆိုတော့ Java to dart ကအရမ်းကွာတာမဟုတ်လို့ပဲ syntax ကိုပြောတာပါ။စဥ်းစားပုံ စဥ်းစားနည်းကတော့ ကွာပါတယ်။ 

**ဘာကြောင့်ကွာတာလဲ**

Java သည် imperative ပါ။ ရှင်းရှင်းလင်းလင်းပြောရရင် တစ်ဆင့် ပြီးမှ တစ်ဆင့် သွားရတာဖြစ်တယ်။ ဒီဟာ အကုန်ပြီးတော့မှ နောက်အလုပ်ကိုဆက်လုပ်ဆိုတဲ့ ပုံစံမျိုးပါ။

Dart သည် Declarative ပါ။ သူကကျ Result တွေကို ကြိုစဥ်းစားပေးရတယ် ဖြစ်နိုင်တဲ့ အခြေအနေတွေကို ကြိုရေးထားပေးရတယ်။ 

ကဲ Intro တွေဘာတွေ၀င်ပြီးပြီဆိုတော့ ကျန်တာလေးတွေစလိုက်ကြမယ်

Syntax လေးကွာဟမှုကိုတစ်ချက်လောက်လိုက်ကြည့်ကြမယ် 

Example scenario ကတော့ ကျွှန်တော်တို့ List တစ်ခုကို random နံပါတ်တွေနဲ့ တည်ဆောက်ကြမယ် ပြီးရင် Print ထုတ်ပြမယ်ပေါ့

ဒါက java နဲ့ရေးထားတာ

```java
List<Integer> intList=new ArrayList<Integer>(10);
for(int i=0;i<10;i++){
  //Casting double to Int
  intList.add((int)(Math.random() * 10));
}
//looping an array to show the items of the list
for(int item: intList){
  System.out.println(item);
}
```

ဒါက Dart နဲ့ရေးထားတာ

```dart
//This is generating a list of random numbers
var list=List<int>.generate(10, (int index) {
  return Random().nextInt(10);
}); 
//looping list to show the items of the list
list.forEach((item){
  print(item);
});
```



 ## Tip for Language Conversion

တတ်နိုင်ရင် မမှတ်ထားပါနဲ့ syntax တွေလိုက်မှတ်ထားနေရင် ခေါင်းအရမ်းလေးပါလိမ့်မယ်။ ပြီးတော့ ကျွန်တော်ကိုယ်တိုင်လည်း စမ်းကြည့်ပြီးသားမလို့ပါ။

ကျွန်တော်Java စလုပ်ခဲ့တယ်။ ပြီးတော့ Kotlin, PHP, အခု Dart ပေါ့။ အဲမှာတင် လေးခုလောက်ဖြစ်နေပြီ။ ကျန်တဲ့ JSတို့ Swift တို့မပါသေးဘူး။ 

အကုန်လိုက်မှတ်ထားလို့ကတော့ မလွယ်ရေးချမလွယ်ပဲ။

လုပ်ရမှာသည် Google ကောင်းကောင်းရှာတတ်ဖို့ပါပဲ။ အပေါ်က Scenario မှာဆို လက်တန်းချရေးနိုင်တာမဟုတ်ပါဘူး။

ဒီမှာကျွန်တော်စလုပ်လိုက်တာက  List စကြေညာတာပါ  

အဲတော့ ကျွန်တော် စလုပ်တာက  google မှာ java declare list dart declare list ဆိုပြီးရှာလိုက်တယ် အဲအခါကျ‌တော့ Language အလိုက် ဘယ်လိုလုပ်ရမလဲဆိုတာကိုမြင်သွားတယ်ဗျာ

ဒီမှာတော့ အကုန်မရှင်းပြတော့ပဲ  Video Lecture ကြည့်ရင်တော့ ပိုမြင်လိမ့်မယ်ထင်တယ်

[Video Link]() ရရင် ပြန် Update ပေးပါမယ်