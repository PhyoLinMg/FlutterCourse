### What is JSON? AND Explaining API 

Json ဆိုတာဘာလဲက အရင်စဖွင့်ကြတာပေ့ါ။

JSon is JavaScript Object Notation ပါ။

မြင်ဖူးလည်း မြင်ဖူးကြမယ်ထင်ပါတယ်။ မမြင်ဖူးလည်းပြမှာမို့ စိတ်မပူပါနဲ့။

```json
{
	"userId": 1,
	"id": 1,
	"title": "delectus aut autem",
	"completed": false
}
```

Json ရဲ့ အစမှာ တွန့်ကွင်း("{") တွေဟာ အစတစ်ခုကိုဖော်ပြတာဖြစ်ပြီး ("}") ကတော့ အဆုံးကို ဖော်ပြထားတာဖြစ်ပါတယ်။

ပြီးရင် attribute key တွေအကုန်လုံးဟာ String ပဲဖြစ်ရပါမယ်။ Value တွေကတော့ String တွေ, int တွေ , boolean တွေ သုံးလို့ရပါတယ်။

တစ်ခုပြီးတိုင်း comma(",") လေးခြားပြီး ရေးလို့ရပါတယ်။

ပြီးတော့ {},{} တွေကို စုထားပြီး List("[]") လုပ်ပြလို့ရပါသေးတယ်။

ဒီလိုမျိုးပေါ့

```json
[
  {
    "userId": 1,
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
    "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
  },
  {
    "userId": 1,
    "id": 2,
    "title": "qui est esse",
    "body": "est rerum tempore vitae\nsequi sint nihil reprehenderit dolor beatae ea dolores neque\nfugiat blanditiis voluptate porro vel nihil molestiae ut reiciendis\nqui aperiam non debitis possimus qui neque nisi nulla"
  },
  {
    "userId": 1,
    "id": 3,
    "title": "ea molestias quasi exercitationem repellat qui ipsa sit aut",
    "body": "et iusto sed quo iure\nvoluptatem occaecati omnis eligendi aut ad\nvoluptatem doloribus vel accusantium quis pariatur\nmolestiae porro eius odio et labore et velit aut"
  },
  {
    "userId": 1,
    "id": 4,
    "title": "eum et est occaecati",
    "body": "ullam et saepe reiciendis voluptatem adipisci\nsit amet autem assumenda provident rerum culpa\nquis hic commodi nesciunt rem tenetur doloremque ipsam iure\nquis sunt voluptatem rerum illo velit"
  },
  {
    "userId": 1,
    "id": 5,
    "title": "nesciunt quas odio",
    "body": "repudiandae veniam quaerat sunt sed\nalias aut fugiat sit autem sed est\nvoluptatem omnis possimus esse voluptatibus quis\nest aut tenetur dolor neque"
  }
]
```

ဒီအပေါ် မှာပြထားတဲ့ example တစ်ခုက Model တစ်ခုကို ကိုယ်စားပြုပါတယ်။

မျက်လုံးထဲနည်းနည်းမြင်သွားအောင် ဒီလိုလေး လုပ်ကြရအောင်။

[ဒီကို](https://javiercbk.github.io/json_to_dart/) သွားပြီး အ‌ပေါ်က json ကိုကူးပြီးသွားထည့်ကြည့်ပါ။

ရလာတဲ့ result က ဒီလိုလေး ပြနေပါလိမ့်မယ်။

```dart
class Post {
  int userId;
  int id;
  String title;
  String body;

  Post({this.userId, this.id, this.title, this.body});

  Post.fromJson(Map<String, dynamic> json) {
    userId = json['userId'];
    id = json['id'];
    title = json['title'];
    body = json['body'];
  }

  Map<String, dynamic> toJson() {
    final Map<String, dynamic> data = new Map<String, dynamic>();
    data['userId'] = this.userId;
    data['id'] = this.id;
    data['title'] = this.title;
    data['body'] = this.body;
    return data;
  }
}
```

#### Network Layer

အခုဆိုရင် ကျွန်တော်တို့ က အင်တာနက်ကနေပဲ အလုပ်အများဆုံး လုပ်ကြတယ်။ မပါမဖြစ် လည်း အရေးကြီးတဲ့ အတွက် ကျွန်တော်တို့ ဒီမှာ ထည့်သင်ပါမယ်။

ကျွန်တော်တို့ API Architecture မှာ အသုံးများတဲ့ အရာတွေကို ပြောသွားမယ်။

- REST API
- SOAP
- GraphQL

ကျွန်တော် တို့ အခုသုံးမှာသည် REST API ကိုပဲသုံးသွားမှာ ဖြစ်တယ်။

HTTP မှာ Response Status code တွေ ရှိပါတယ်။ 

1. Informational responses (100–199)
2.  Successful responses (200–299) 
3. Redirects (300–399) 
4. Client errors (400–499) 
5. Server errors (500–599)

အဲမှာ အသုံးများတဲ့ အရာတွေကို ပြောသွားပါမယ်။



Successful responses    

a. **200** OK    

b. **201** Created  

c. **202** Accepted    

d. **203** Non-Authoritative Information    

e. **204** No Content    

f. **205** Reset Content    

g. **206** Partial Content  



Client error responses    

a. **400** Bad Request    

b. **401** Unauthorized    

c. **402** Payment Required     

d. **403** Forbidden   

 e. **404** Not Found    

f. **405** Method Not Allowed    

g. **406** Not Acceptable    

h. **407** Proxy Authentication Required    

i. **408** Request Timeout 

j. **409** Conflict 

k. **410** Gone    

l. **411** Length Required    

m. **412** Precondition Failed    

n. **413** Payload Too Large    

o. **414** URI Too Long



Server error responses    

a. **500** Internal Server Error    

b. **501** Not Implemented    

c. **502** Bad Gateway    

d. **503** Service Unavailable    

e. **504** Gateway Timeout    

f. **505** HTTP Version Not Supported    

g. **506** Variant Also Negotiates    

h. **507** Insufficient Storage (WebDAV)    

i. **508** Loop Detected (WebDAV)    

j. **510** Not Extended    

k. **511** Network Authentication Required

  

အဲတော့ကျွန်တော်တို့ REST API  Method တွေ အကြောင်း နည်းနည်း ရှင်းပြပါမယ်။ 

- GET
- POST
- PUT
- DELETE
- PATCH

###### GET

GET ကတော့ information only ကို ဆွဲချင်ရင် သုံးပါတယ်။ဒါပေမဲ့  ပြုပြင်လို့မရနိုင်ပါဘူး။

သူက အခြား method က ‌ဒေတာတွေကို မပြင်သေးသရွေ့ ကြိုက်တဲ့အချိန် ကြိုက်သလိုခေါ် ဘယ်တော့မှ မပြောင်းလဲဘူး။

အကုန်အဆင်ပြေတယ်ဆို Status Code 200 ကို ပြပါတယ်။

အဆင်မပြေဘူး ဒီ endpoint ကို ရှာလို့မရဘူးဆိုရင် Status Code 404 ကို ပြပါတယ်။

```http
HTTP GET http://www.appdomain.com/users
HTTP GET http://www.appdomain.com/users?size=20&page=5
HTTP GET http://www.appdomain.com/users/123
HTTP GET http://www.appdomain.com/users/123/address
```

###### POST

POST ကတော့ information တွေကို update ချင်တယ် or အသစ်ထပ်ထည့်ချင်တယ် ဆိုရင် သုံးပါတယ်။

ကျွန်တော်တို့ POST Method ကို ပို့လို့  အောင်မြင်တယ်ဆိုရင်  201 created ဖြစ်ပါတယ်။

```http
HTTP POST http://www.appdomain.com/users
HTTP POST http://www.appdomain.com/users/123/accounts
```

###### PUT

PUT ကို ရှိပြီးသားdata ကို update လုပ်ချင်တဲ့ အချိန်မှာသုံးပါတယ်။

တကယ်လို့ ဒီပေးလိုက်တဲ့ DATA တွေ ရှိတဲ့ အချိန်မှာ အသစ်ပြန်ဆောက်ပေးတယ်။ အဲအခါကျရင် 201 CREATED ပြန်ပေးတယ်။

modified ဖြစ်ရင်တော့ ကျွှန်တော် တို့ 200(Ok) ပြန်ပြပေးတယ်။

> POST နဲ့ PUT ရဲ့ ခြားနားချက်က ဘာလဲဆိုတော့ POST Body သည် resource collection နဲ့ လုပ်ရမယ် PUT ကတော့ single Resource တစ်ခုပဲဖြစ်တယ်။

```http
HTTP PUT http://www.appdomain.com/users/123
HTTP PUT http://www.appdomain.com/users/123/accounts/456
```

###### DELETE

ဒီနာမည် ပြောတဲ့အတိုင်း ရှိနေတဲ့ data ကို ဖျက်တာပါ။

Response အိုကေတယ်ဆိုရင် 200(OK) ပြန်ပါတယ်။ မရသွားရင်တော့ 204(No Content ) ပေါ်ပါတယ်။

```http
HTTP DELETE http://www.appdomain.com/users/123
HTTP DELETE http://www.appdomain.com/users/123/accounts/456
```



အဲလောက်ဆို ကျွန်တော်တို့ ဆက်သွားဖို့ အဆင်ပြေပါပြီ။





