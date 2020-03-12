HTML과 JavaScript 연결

1. HTML 내부에 정의

```html
<head>
    <script>
    	function multi(){
            var firstNum = document.forms[0].firstnumber.value;
            var secondNum = document.forms[0].secondnumber.value;
            var multiValue = firstNum*secondNum;
            document.forms[0].value.value = multiValue
        }
    </script>
</head>
<body>
    <h3>곱셈 계산기</h3>
    <form>
        <input type="number" name="firstnumber" value="0">x
        <input type="number" name="secondnumber" value="0">=
        <input type="text" name="value">
	    <input type="button" value="계산하기" onClick="multi()">        
    </form>
</body>
```

2. 외부 JavaScript 파일 HTML에 연결

   ```html
   <head>
       <script src="script.js"></script>
   </head>
   ```

   