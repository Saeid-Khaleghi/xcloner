# xCloner

xCloner is a jQuery plugin help you to add key-value pairs to your bootstrap projects dynamically.

- jQuery support: 1.11+
- Bootstrap support: 3

### Installation

Include files:

```html
<link rel="stylesheet" href="/path/to/bootstrap.min.css" type="text/css"/>

<script src="/path/to/jquery.js"></script><!-- jQuery is required -->
<script src="/path/to/bootstrap.min.js"></script>
<script src="/path/to/xcloner.js"></script>
```

### Usage

HTML:
```html
<div class="col-sm-4">
	<div class="input-group xcloner" id="my_cloner">
		<div class="input-group-btn">
			<button aria-expanded="false" aria-haspopup="true" data-toggle="dropdown"
					class="btn btn-default dropdown-toggle" type="button">
				<span class="selected-choice"></span>
				<span class="caret"></span>
			</button>
			<ul class="dropdown-menu">
				<li><a data-value="1" href="#">Weight</a></li>
				<li><a data-value="2" href="#">Height</a></li>
				<li><a data-value="3" href="#">Color</a></li>
				<li><a data-value="4" href="#">Dimention</a></li>
			</ul>
		</div>
		<input type="text" class="form-control text-center main-input" value="" name="field_"/>
		<span class="input-group-btn remove-field hidden">
			<button type="button" class="btn btn-danger"> -</button>
		</span>
		<span class="input-group-btn add-field">
			<button type="button" class="btn btn-success"> +</button>
		</span>
	</div>
</div>
```

Initialize with .xcloner() method:
```html
$('.xcloner').xcloner();
```

To get its values as object
```html
var obj = $('.xcloner').xcloner().val();
obj is an object of {index_of_field_1 : value_you_choose_1, index_of_field_2 : value_you_choose_2,...}
```

To initialize with some data:
```html
$('.xcloner').xcloner().add({index_of_field_1 : value_you_choose_1, index_of_field_2 : value_you_choose_2,...});
```

To reset xcloner and delete all nodes
```html
$('.xcloner').xcloner().reset()
```
### Options:
```html
	margin: 0; 				// Set margin around each nodes
	chooseText:"Choose",	// Default text to select keys
	inputs:{}, 				// Assigning key-value pairs
	del_exist_inputs:false, // Delete all exist selectable choices
```
For **downloads**, see:
https://github.com/saeid-khaleghi/xcloner/releases/

### xCloner Credits

- Concept and development, design and repository maintained by __Saeid Khaleghi__ for [ParsTarnavard](http://parstarnavard.ir/).

### View

![xCloner usage](https://cloud.githubusercontent.com/assets/13361616/12661022/7e8ac778-c62c-11e5-8dd1-40c3ada3a4ea.png)