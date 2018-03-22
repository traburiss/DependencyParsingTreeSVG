# DependencyParsingTreeSVG
Create DependencyParsingTree SVG by javascript

一个使用javascript创建句法依存树svg的模块，仅依赖jquery

改造自[这里](http://x-algo.cn/index.php/2016/03/13/293/)，找不到原作者的名字（希望原作者能联系指教），本人进行了一些代码格式、参数外置，bug优化的工作

>### 使用方法:
>1. 直接将DependencyParsingTree.js复制到适当的工程目录下
>2. 将DependencyParsingTree.js引入项目中
>3. 调用GDepParser方法，传递参数：
>   ```
>   var node_list = [
>        {id:0,fid:0,word:'测试0',post:'test1',dep_type:'TEST1'},
>        {id:1,fid:0,word:'测试1',post:'test2',dep_type:'TEST2'}
>    ];
>    GDepParser({
>        node_list: node_list,//列表，必选
>        select: '#dependencySvg',//放置svg的容器，必选
>         error: function(error){
>
>             //显示错误信息，可选
>         },
>         node_params:{//参数集合，可选 
>            word_height:40,//词的高度，默认值40
>            zh_word_width:16,//词的宽度，默认值16
>            arrow_width:10,//箭头宽度，默认值16
>            word_left_space:20, //每个词之间的空格，默认值20
>            edge_height:20,//边之间的高度，每个箭头边之间的高度，默认值20
>            svg_min_width:500,//最小宽度，默认值500
>            svg_top_margin:10,//实际是上下的margin，默认值10
>            svg_left_margin:10,//实际是左右的margin，默认值10
>            one_lable_width:10,//一个lable的横向宽度，默认值10
>            one_lable_height:16, //lable标签的高度，默认值16
>            word_top_margin:5,//词部分上面的margin，默认值5
>            array_direction:'child'//箭头节点的指向，'child'指向子节点,'parent'指向父节点，默认指向子节点 
>         }
>    });
>   ```
