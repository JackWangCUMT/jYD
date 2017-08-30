# jYD
Javascript library like jQuery Api but smaller (14KB)
## Usage
```html
<script src="jYD.js"></script>
```
## Dom
```javascript
jYD.$("#txt2").ele().value
jYD.$("#frm input").ele()
jYD.$("input:checked").ele()[0].value
jYD.$("input[type=text]").ele()[0].value
jYD.$(".classname").ele()[0].value
jYD.$(".classname").first().ele()
```
## Form
```javascript
var _json = {
    "name3": "name3",
    "name6": "name6",
    "name7": "name7",
    "name2": "2017-08-08",
    "name1": "audi",
    "ajdsfa": false,
    "Fruit": "桃子",
    "fruit1": "香蕉",
    "hobby": ["音乐", "游泳"],
};
jYD.$("#frm").bindJson(_json)
jYD.$("#frm").serialize() //name3=name3&name6=name6&name7=name7&name2=2017-08-08
jYD.$("#frm").reset()
jYD.$("input").disabled()
jYD.$("select").disabled()
jYD.$("button").disabled()
jYD.$("input").enable()
jYD.$("select").enable()
jYD.$("button").enable()
```


