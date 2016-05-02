# scrolltop-next-element

```html

<div id="up" style="background-color:orange;height:100px;overflow:hidden;"></div>
<div id="container" style="height:120px;overflow:scroll;width:100%;position:relative;">
    <input id="1" type="text" class="input" placeholder="input 1" />
    <br/>
    <input id="2" type="text" class="input" placeholder="input 2" />
    <br/>
    <input id="3" type="text" class="input" placeholder="input 3" />
    <br/>
    <input id="4" type="text" class="input" placeholder="input 4" />
    <br/>
    <input id="5" type="text" class="input" placeholder="input 5" />
    <br/>
    <input id="6" type="text" class="input" placeholder="input 6" />
    <br/>
    <input id="7" type="text" class="input" placeholder="input 7" />
    <br/>
    <input id="8" type="text" class="input" placeholder="input 8" />
    <br/>
    <input id="9" type="text" class="input" placeholder="input 9" />
    <br/>
    <input id="10" type="text" class="input" placeholder="input 10" />
    <br/>
    <input id="11" type="text" class="input" placeholder="input 11" />
    <br/>
    <input id="12" type="text" class="input" placeholder="input 12" />
    <br/>
    <input id="13" type="text" class="input" placeholder="input 13" />
    <br/>
    <input id="14" type="text" class="input" placeholder="input 14" />
    <br/>
    <input id="15" type="text" class="input" placeholder="input 15" />
    <br/>
    <input id="16" type="text" class="input" placeholder="input 16" />
    <br/>
    <input id="17" type="text" class="input" placeholder="input 17" />
    <br/>
    <input id="18" type="text" class="input" placeholder="input 18" />
    <br/>
    <input id="19" type="text" class="input" placeholder="input 19" />
    <br/>
    <input id="20" type="text" class="input" placeholder="input 20" />
    <br/>
    <input id="21" type="text" class="input" placeholder="input 21" />
    <br/>
    <input id="22" type="text" class="input" placeholder="input 22" />
    <br/>
</div>
<div id="bottom" style="background-color:green;height:100px;overflow:auto;position:relative;"></div>

```

```javascript
$('input').on('focus', function () {
    console.log($(this).offset());
    console.log($(this).position());
    console.log($('#container').scrollTop());
    $('input').removeAttr('style');
    var ot=parseInt($(this).offset().top),
        pt=parseInt($(this).position().top);
    var st=ot-108;//108 is height of up div
    if(st-pt>0){
        st=st-pt;
    }
    if(st<0){st=ot-108}
    console.log(st,ot,pt);
    $('#container').animate({
        scrollTop: st+$('#container').scrollTop()
    },200);
});
'''

