# dynamic-card
使用纯css实现的弹性卡片组件
## 预览
 ![image](http://github.com/qhclf/dynamic-card/src/assets/card1.png)

![image](http://github.com/qhclf/dynamic-card/src/assets/card2.png)


## 使用方式
###### 1.下载组件：
npm  install dynamic-card
###### 2添加到组件中
例如：
<card :width="200" :height="300"></card>
根据一下数据格式为其添加属性，为添加则表示使用默认：
<br>
        卡片的宽: width: {type: Number,  default: 370}
        <br>
        卡片的高: height:{
            type: Number,
            default: 430
        },
          <br>
        卡片中的图片链接：imgSrc: {
            type: String,
            default: 'https://hbimg.huabanimg.com/1ccac3a5bdc74168e8b91d886a12be75471e82ce40b19-MoLdbk_fw658'
        },
          <br>
        卡片内容中的大标题title:{
            type: String,
            default: '越努力，越幸运!' 
        },
          <br>
        卡片内容中的小标题 subtitle:{
            type: String,
            default: 'QHMILK' 
        },
          <br>
        卡片内容中的文本: desc:{
            type: String,
            default: '正文的详细内容描述,越努力，越幸运,机不可失，失不再来。正文的详细内容描述,越努力，越幸运,机不可失，失不再来'
        },
          <br>
         尾部文字： footer_text:{
            type: String,
            default: '此组件由QHMILK设计'
        },
          <br>
        尾部链接： footer_link:{
            type:String,
            default: '#'
        }


