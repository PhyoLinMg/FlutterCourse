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


