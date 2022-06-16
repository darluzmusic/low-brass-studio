    <style type="text/css">
body,input
    {
    font-family:"Trebuchet ms",arial;font-size:0.9em;
    color:#333;
    }
.spoiler
    {
    border:1px solid #ddd;
    padding:3px;
    }
.spoiler .inner
    {
    border:1px solid #eee;
    padding:3px;margin:3px;
    }
    </style>
    <script type="text/javascript">
function showSpoiler(obj)
    {
    var inner = obj.parentNode.getElementsByTagName("div")[0];
    if (inner.style.display == "none")
        inner.style.display = "";
    else
        inner.style.display = "none";
    }
    </script>

<div class="spoiler">
    <img onclick="showSpoiler(this);" src="https://pbs.twimg.com/profile_images/858514627/eppaa_bigger.jpg" />
    <div class="inner" style="display:none;">
    This is a spoiler!
    </div>
</div>
