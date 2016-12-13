# Abe tag

> You can add abe tag to you template following simple rules

## Abe DOM element

This abe tag will display `text` on the document

TEMPLATE

```html
<html>
	<head>
	</head>
	<body>
		{{abe type='text' key='text_dom'}}
	</body>
</html>
```

RENDER

```html
<html>
	<head>
	</head>
	<body>
		Hello
	</body>
</html>
```

## Abe DOM Attributes

This example will be added to `body > class` html attributes

TEMPLATE

```html
<html>
	<head>
	</head>
	<body class="{{abe type='text' key='text_class'}}">
		
	</body>
</html>
```

RENDER

```html
<html>
	<head>
	</head>
	<body class="class-hello">
		
	</body>
</html>
```

## More examples

#### multiple attributes
multiple attributes are allowed on the same html DOM object

```html
<html>
	<head>
	</head>
	<body class="{{abe type='text' key='text_class'}}" id="{{abe type='text' key='text_id'}}">
		
	</body>
</html>
```

#### concatenate with attribute

```html
<html>
	<head>
	</head>
	<body class="my-body-class {{abe type='text' key='text_class'}}">
		
	</body>
</html>
```

#### if handlebars

On the next example if variable `text_class` is not empty use `text_class` otherwise use `my-default-class`

```html
<html>
	<head>
	</head>
	<body class="{{#if text_class}}{{abe type='text' key='text_class'}}{{else}}my-default-class{{/if}}">
		
	</body>
</html>
```

# [ WARNING ] THE FOLLOWING EXAMPLE ARE NOT IMPLEMENTED YET

Multiple abe attribute into the same html tag

```html
<html>
	<head>
	</head>
	<body class="{{abe type='text' key='text_1'}}{{abe type='text' key='text_2'}}">
		
	</body>
</html>
```
