<html>
<head>
    <!--从assert中加载的中文网页会出现乱码，解决办法就是给html指定编码-->
    <meta http-equiv="content-type" content="text/html;charset=gb2312">
    <title>
    </title>


</head>
<body>
这是html页面 <br/>
<button onclick="s()">点击调用本地方法</button>
<a href="file:///android_asset/js_java_interaction.html">点击跳转到原生页面</a>
<p id="p"></p>

<script type="text/javascript">

            //有参有返回值的方法
            function sum(a,b) {
                <!--gygguuuiu-->
                return a+b;
            }

            //有参无返回值的方法
            function alertMessage(message) {
                alert(message);
            }

            //无参无返回值的方法
            function show(){
                //显示hello world
                document.getElementById("p").innerHTML="hello world";
            }

            function s() {
                //调用原生的方法，android为约定的别名；back()为原生的方法
                var result=window.android.back();
                //将返回结果显示在id为p的控件上
                document.getElementById("p").innerHTML=result;
            }
        </script>
</body>
</html>
