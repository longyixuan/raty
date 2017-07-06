## raty
> 强大的评星插件，兼容各版本浏览器

### 安装
首先下载[raty](https://github.com/longyixuan/raty)插件
### 引用
``` html
<script src="js/jquery.js"></script>
<script src="js/jquery.raty.min.js"></script>
```
路径根据你的项目路径更正
### Html结构
``` html
<div style="width:500px; margin:100px auto;">
  <div class="demo">
    <div id="function-demo" class="target-demo"></div>
    <div id="function-hint" class="hint"></div>
  </div>
</div>
```
### js调用
```javascript
$(function(){
  $.fn.raty.defaults.path = 'img'; //设置图片路径，即星星图片
  $('#function-demo').raty({
        number: 5, //多少个星星设置
        targetType: 'hint', //类型选择，number是数字值，hint，是设置的数组值
        path: 'img',
        hints: ['差', '一般', '好', '非常好', '全五星'],
        cancelOff: 'cancel-off-big.png',
        cancelOn: 'cancel-on-big.png',
        size: 24,
        starHalf: 'star-half-big.png',
        starOff: 'star-off-big.png',
        starOn: 'star-on-big.png',
        target: '#function-hint',
        cancel: false,
        targetKeep: true,
        targetText: '请选择评分',
        click: function(score, evt) {
            alert('ID: ' + $(this).attr('id') + "\nscore: " + score + "\nevent: " + evt.type);
        }
    });
})
```
### 更多参数
> cancel			: false,
> cancelHint		: 'cancel this rating!',
> cancelOff		: 'cancel-off.png',
> cancelOn		: 'cancel-on.png',
> cancelPlace		: 'left',
> click			: undefined,
> half			: false,
> halfShow		: true,
> hints			: ['bad', 'poor', 'regular', 'good', 'gorgeous'],
> iconRange		: undefined,
> mouseover		: undefined,
> noRatedMsg		: 'not rated yet',
> number			: 5,
> path			: 'img/',
> precision		: false,
> round			: { down: .25, full: .6, up: .76 },
> readOnly		: false,
> score			: undefined,
> scoreName		: 'score',
> single			: false,
> size			: 16,
> space			: true,
> starHalf		: 'star-half.png',
> starOff			: 'star-off.png',
> starOn			: 'star-on.png',
> target			: undefined,
> targetFormat	: '{score}',
> targetKeep		: false,
> targetText		: '',
> targetType		: 'hint',
> width			: undefined

### 改变样式
做一组图片，放在img下，对应图片的引用路径即可
