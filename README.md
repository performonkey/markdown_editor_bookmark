markdown_editor_bookmark
========================

Markdown编辑器书签

    data:text/html,
    <style type="text/css">
        .e{
            position:absolute;
            top:0;
            right:50%;
            bottom:0;
            left:0;
        } 
     
        .c{
            position:absolute;
            overflow:auto;
            top:0;
            right:0;
            bottom:0;
            left:50%;
        }
    </style>
     
    <div class="e" id="editor"></div>
    <div class="c"></div>
     
    <script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" 
            type="text/javascript" 
            charset="utf-8"></script>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/showdown/0.3.1/showdown.min.js"></script>
     
    <script> 
        function showResult(e){
            consoleEl.innerHTML=e
        }
        
        var e=ace.edit("editor");
        e.setTheme("ace/theme/monokai");
        e.getSession().setMode("ace/mode/markdown");
        document.getElementById('editor').style.fontSize='14px';
        var consoleEl = document.getElementsByClassName("c")[0];
        var converter = new Showdown.converter;
        
        e.on("change",function(){
            var n=e.getSession().getMode().$id;
            if(n == "ace/mode/markdown"){
                showResult(converter.makeHtml(e.getValue()))
            }
        });
    </script>

将以下代码保存与书签中即可。
    data:text/html,<style type="text/css">.e{position:absolute;top:0;right:50%;bottom:0;left:0;} .c{position:absolute;overflow:auto;top:0;right:0;bottom:0;left:50%;}</style><div class="e" id="editor"></div><div class="c"></div><script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" type="text/javascript" charset="utf-8"></script><script src="http://cdnjs.cloudflare.com/ajax/libs/showdown/0.3.1/showdown.min.js"></script><script> function showResult(e){consoleEl.innerHTML=e}var e=ace.edit("editor");e.setTheme("ace/theme/monokai");e.getSession().setMode("ace/mode/markdown");var consoleEl=document.getElementsByClassName("c")[0];var converter=new Showdown.converter;e.on("change",function(){var n=e.getSession().getMode().$id;if(n=="ace/mode/markdown"){showResult(converter.makeHtml(e.getValue()))}});</script>
