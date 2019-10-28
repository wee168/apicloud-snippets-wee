# APICloud Snippets
# 2019-10-28
# 其于beiluo的代码继续封装新的命令

# 使用示例
---
__api-alert__ <kbd>Tab</kbd>

```js
api.alert({
    title: '${1:this}', 
    msg: ${2:this}
});
```

__uiscrollpicture-open__ <kbd>Tab</kbd>
```js
uiscrollpicture.open({
    rect: {
        x: ${1:0},
        y: ${2:0},
        w: ${3:320},
        h: ${4:480}
    },
    data: {
        paths: ['${5:image_path1}', '${6:image_path2}', '${7:image_path3}'],
        captions: ['${8:title1}', '${9:title2}', '${10:title3}']
    },
    styles: {
        caption: {
            height: ${11:35},
            color: '${12:color}',
            size: ${13:13},
            bgColor: '${14:bg_color}',
            position: '${15:position}'
        },
        indicator: {
            align: '${16:align_mode}',
            color: '${17:color}',
            activeColor: '${18:active_color}'
        }
    },
    placeholderImg: '${19:placeholder_image_path}',
    contentMode: '${20:content_mode}',
    interval: ${21:3},
    loop: ${22:true},
    fixedOn: '',
    fixed: ${23:false}
}, function(ret, err){
     if(ret.status){
        if(ret.eventType == 'click'){
            //点击图片的操作
            alert(ret.index);
        }
     }
});
```