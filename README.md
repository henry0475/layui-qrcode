# layui.qrcode.js

The LayUI plugin of layui.qrcode.js is based on the project of <a href='http://jeromeetienne.github.com/jquery-qrcode'>jquery.qrcode.js</a>.

It just changed a little bit to be suitable for generating QR codes in webpages which build on the framework of LayUI, especially for **LayUIAdmin**.

It contains all features from the original project of "jquery-qrcode".

## How to Use It

First, you should put the file of "layui.qrcode.min.js" into the directory of "modules" (Actually, you can put this file to anywhere, but it will be more convenient and clear if you put it into the directory of "modules")

Then, creating a DOM element which is going to contain the generated QR code image is necessary.

    <div id="container"></div>

For now, you should include the module of *layui.qrcode* and generate a code in script.

    <script> 
    layui.config({
            base: './layuiadmin/'
        }).extend({
            qrcode: 'layui.qrcode.min'
        }).use(['qrcode'], function(){
            var $ = layui.$;
    
            // Generate a QR code in a DIV containner which ID is "container".
            $('#container').qrcode({
                render: "canvas",           // default but the parameter of "table" is avaiable
                text: "some information",
                width: 256,                 // default
                height: 256                 // default
            });
        });
    </script>

There is an example if you do not understand how to use it. Please click <a href="https://github.com/henry0475/layui-qrcode/blob/master/examples/demo.html" target="_blank">here</a> to find out.

## Conclusion

I just combine two files from the original project, which are *jquery.qrcode.js* and *qrcode.js*, followed by the module rule of LayUI. 

Just ONE more thing I think you should know that JQuery is already integrated into LayUI, so you may not add any other codes for importing the framework of JQuery.

UNDER <a href='https://github.com/henry0475/layui-qrcode/blob/master/LICENSE'>MIT license</a>. Thus, please feel free to fork, and have fun with it.