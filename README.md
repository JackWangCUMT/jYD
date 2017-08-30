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
## Event
```javascript
jYD.$("#btnok").off("click").on("click", function(e) {
      console.log(decodeURIComponent(jYD.$("#frm").serialize()));
});
//custom Event
var sender = jYD.$("#cediv").ele();
var target = jYD.$("#btnce").ele();
jYD.createCE(sender, "divbtnclick", {
     detail: {
            tag: sender,
             msg: "hello"
      }

}, target, "click");
 //冒泡
jYD.$("#cediv").on("divbtnclick", function(e) {
      console.log(e);
});
```

## CSS
```javascript
jYD.$(".clss").addClass("red").removeClass("clss")
jYD.$("#txt2").css({"backgroundColor":"#eee"});
```
## Ajax
```javascript
 jYD.post('/api/api3.ashx')
     .params(jYD.$("#frm").serialize() + "&table=22")
     .success(function (data) {
           console.log(data);
     }).error(function (data) {
           console.log("eror" + data);
     })
     .send();
```
## Other
```javascript
jYD.is.Number(99)
jYD.isElement(document.getElementById("frm"))
jYD.is.Array([])
```
