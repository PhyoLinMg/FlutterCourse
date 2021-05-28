### Dart Basics

ဒီမှာ လုပ်သွားမယ့် video သင်ခန်းစာတွေကို [ဒီမှာ]() ကြည့်နိုင်ပါတယ်။ နှစ်ခု လုံး ပြန်ကြည့်လို့ရအောင် လွယ်အောင်လုပ်ပေးထားပါမယ်။

ရေးသွားတဲ့ [Code]() တွေကို လည်း ထည့်ပေးသွားမှာ ဖြစ်ပါတယ်။

**Sound Non Nullability**

**Sound Non Nullability**

Nullability ဆိုတာ null ဖြစ်မဖြစ်ကို စစ်ပေးနိုင်တဲ့ အရာပေါ့။ နဂိုက variable တစ်ခုက Null ဖြစ်နေတယ်ဆိုတာ Run Time မှာမှ သိခဲ့ကြတယ်။

Dart ရဲ့ Non-Nullability ကို သုံးမယ်ဆိုရင်တော့ Compile Time Error အနေနဲ့ပြပေးလိမ့်မယ်။

ဘယ်လို မျိုးလဲဆိုတာ ပြပေးပါမယ်၊

```dart
String impossible;//ordinary string declaration
print(impossible.length);
//If it is executed, the error will occur for sure.
```

dart's non nullability ကို သုံးလိုက်မယ်ဆိုရင်

```dart
String? impossible; // non nullability string declaration
print(impossible.length);//compile time error will occur here
```

**Variable Declaration**

String တို့ int တို့ float တို့ ကြေညာတာကတော့ အရင်အတိုင်းပါပဲ။

var လည်း dynamic type ပဲ။

ဒါပေမဲ့ တစ်ခုဗဟုသုတ အနေနဲ့ ပြောပြချင်တာက dynamic ဆိုတဲ့ အရာပဲ။

dynamic နောက်မှာ ကြိုက်တာလာလို့ရတယ်။ Kotlin ရဲ့ any ကို အားကျပြီးလိုက်လုပ်ထားတာပေါ့။

```dart
dynamic dota="ဗိုလ်စွပ်ကျယ်"
```

**Function Declaration**

Java နဲ့ ပုံစံဆင်တယ်။ void methodName() နဲ့ လည်းသွားလို့ရတယ်။

ပြီးတော့ ပြန်ပေးချင်တဲ့type methodName() နဲ့ သွားတယ်။

တစ်ခုပြောစရာရှိလာတာက parameter

ကျွန်တော်တို့ java မှာ လုပ်ခဲ့တဲ့ Function တွေမှာ parameter အနေနဲ့int ,string တွေထည့်ခဲ့ကြတယ်။

ဒီလိုမျိုုးပေါ့

```java
String getFullName(String firstName,String secondName){
    return firstName+" "+secondName;
}
```

 dart မှာလည်း ပုံစံတူရေးလို့ရပါတယ်။ ပြောစရာရှိလာတာက သူ့မှာ Optional Parameter ဆိုပြီးပါလာတယ်။

{ } နဲ့ရေးရတယ်။

ကျန်တာ ဘာမှ မထည့်ထားရင် ထည့်ကို ထည့်ပေးရတယ်။  { } ပါရင် ထည့်ချင်ထည့် မထည့်ချင်လည်းနေလို့ရတယ်။

```dart
int calculateSum({int firstNumber=1,int secondNumber=3}){
    return firstNumber+secondNumber;
}
```

```dart
print(calculateSum(firstNumber:3,secondNumber:4));//7
print(calculateSum());//4
```

