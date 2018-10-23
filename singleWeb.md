### pattern model

```javascript

// when just use this function once, means a temperory func so we dont save this to a variable like this, maybe more simple.
var prison = (function(){
    return "Mike is noob";
})();

// up one is same to the follow function

function MakePrison(){
    return "Mike is idiot";
}

var prison = MakePrison();
```
- another example

```javascript

// automatically, assign "prisoner" and "sentence" to variable prison.
var prison = (function(){
    var prison_name = "Mike Mikowski",
        jail_term = "20 yeast term";

    return{
        prisoner: prisoner_name + " - " + jail_term;
        sentence: jail_term
    };
})();

// output: undefined, can't assess or just deleted after function run
console.log(prison.prisoner_name);
// output: "Mike Mikowski - 20 years term"
console.log(prison.prisoner);
// output: "20 year term"
console.log(prison.sentence);

```

### shell 
- 飞机中的引擎？
- 文件结构 js jq css 分成部分结构组合
- jquery ok, urianchor what this shit does
- 在单网页应用中在网页的body前预先加载css javascript, 通常网页的话, 放在body后应该会更快加载页面。 但是由于单网页应用的页面也是由于javascript生成的所以没有意义.

#### css
- 通常由于不信任浏览器的默认格式，会在css开头重置.

```css
/** begin reset */
*{
    margin: 0;
    padding: 0;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}
h1, h2, h3, h4, h5, h6, p{ margin-bottom:  10px;}
o1, u1, d1 {list-style-position: inside;}
```
#### jsLint
- 这玩意有什么用？
- 可以检查js的错误 挺有用的 哈哈

```
/*jslint           browser : true,   continue : true,
  devel  : true,    indent : 2,       maxerr  : 50,
  newcap : true,     nomen : true,   plusplus : true,
  regexp : true,    sloppy : true,       vars : false,
  white  : true
*/
```

#### layout.html
- 在设计单网页应用的时候，先在一个layout里面设计css和html代码, 样式符合要求后再分割。 书上说这是最高效的.

