## Welcome to mdjing's GitHub Pages
## Vue实现原理 - 如何实现双向绑定mvvm

```markdown
Syntax highlighted code block

## 几种实现双向数据绑定的方法

1、发布者-订阅者模式（backbone.js）

2、脏值检查（angular.js） 

3、数据劫持（vue.js）

### 发布者-订阅者模式
  一般通过sub, pub的方式实现数据和视图的绑定监听，更新数据方式通常做法是 vm.set('property', value)
  
### 脏值检查
  angular.js 是通过脏值检测的方式比对数据是否有变更，来决定是否更新视图，最简单的方式就是通过 setInterval() 定时轮询检测数据变动，当然Google不会这么low，angular只有在指定的事件触发时进入脏值检测，大致如下：

    1、DOM事件，譬如用户输入文本，点击按钮等。( ng-click )
    2、XHR响应事件 ( $http )
    3、浏览器Location变更事件 ( $location )
    4、Timer事件( $timeout , $interval )
    5、执行 $digest() 或 $apply()

### 数据劫持
    vue.js 则是采用数据劫持结合发布者-订阅者模式的方式，通过Object.defineProperty()来劫持各个属性的setter，getter，在数据变动时发布消息给订阅者，触发相应的监听回调。
    
   <img src=' https://github.com/Tie-Dan/mvvm/raw/master/img/2.png'>
   - Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/mdjing/mdjing.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
