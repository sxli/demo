# demo
第一个demo
<!DOCTYPE HTML>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>nextSibling</title>
</head>
<body>
<ul id="u1">   
            <li id="a">javascript</li>   
            <li id="b">jquery</li>   
            <li id="c">html</li>   
        </ul>   
        <ul id="u2">   
            <li id="d">css3</li>   
            <li id="e">php</li>   
            <li id="f">java</li>   
        </ul>   
<script type="text/javascript">
    function get_nextSibling(n){
        var x=n.nextSibling;
        while (x && x.nodeType!=1){
            x=x.nextSibling;
        }
        return x;
    }

    var x=document.getElementsByTagName("li")[0];
    document.write(x.nodeName);
    document.write(" = ");
    document.write(x.innerHTML);
    
    var y=get_nextSibling(x);
    
    if(y!=null){
        document.write("<br />nextsibling: ");
        document.write(y.nodeName);
        document.write(" = ");
        document.write(y.innerHTML);
    }else{
      document.write("<br>已经是最后一个节点");      
    }

</script>
</body>
</html>
