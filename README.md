Markdown编辑器书签
========================

###代码：
    data:text/html,
    <style type="text/css">
        #e{
            position:absolute;
            top:0;
            right:50%;
            bottom:0;
            left:0;
        } 
     
        #c{
            position:absolute;
            overflow:auto;
            top:0;
            right:0;
            bottom:0;
            left:50%;
        }
    </style>
     
    <div id="e"></div>
    <div id="c"></div>
     
    <script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" 
            type="text/javascript" 
            charset="utf-8"></script>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/showdown/0.3.1/showdown.min.js"></script>
     
    <script> 
        function showResult(e){
            consoleEl.innerHTML=e
        }
        
        var e=ace.edit("e");
        e.setTheme("ace/theme/monokai");
        e.getSession().setMode("ace/mode/markdown");
        document.getElementById('e').style.fontSize='14px';
        var consoleEl = document.getElementById("c");
        var converter = new Showdown.converter;
        
        e.on("change",function(){
            var n=e.getSession().getMode().$id;
            if(n == "ace/mode/markdown"){
                showResult(converter.makeHtml(e.getValue()))
            }
        });
    </script>

###使用方法：
将「bookmark」文件内容保存与书签中即可。
