# NoteList

在任务中，做了一个 PC 端的 NoteList 应用。并将它优化，以适应移动端设备。

## NoteList 


* [源代码](https://github.com/sunzheng987/NoteList)
* [在线 demo](http://sunzheng987.github.io/NoteList)
* 手机查看 ↓ 二维码 ↓
    
    ![todoWebApp](http://qr.api.cli.im/qr?data=https%253A%252F%252Fsunzheng987.github.io%252FNoteList%252F&level=H&transparent=false&bgcolor=%23ffffff&forecolor=%23000000&blockpixel=12&marginblock=1&logourl=&size=280&kid=cliim&key=07b45b9231d628bca12a3c57b56ecfb8)



## Details

* **数据存储**

    以 JSON 模拟数据表的形式存储于 LocalStorage 中

         使用数据库的思想，构建3张表。
         cateJson 分类
         childCateJson 子分类
         taskJson 任务
         
         分类表 cate
         ----------------------
         id* | name | child(FK)
         ----------------------
         
         子分类表 childCate
         --------------------------------
         id* | pid(FK) | name | child(FK)
         --------------------------------
         
         任务表 task
         ----------------------------------------------
         id* | pid(FK) | finish | name | date | content
         ----------------------------------------------

* **响应式布局**
    
    针对手机端细节做了很多调整，更符合手机上的视觉交互习惯。


* **模块化**
    
    使用 requireJS 模块化 JavaScript 代码。重构 JavaScript 代码。优化之前写的耦合性高的绑定事件，重新绑定事件，降低耦合性。期间根据具体需求重写了事件代理的代码。

* **前端工程化**
    
    使用 gulp，自动编译 Sass，压缩 CSS 和 JavaScript 代码。并且配置了自动流程。

