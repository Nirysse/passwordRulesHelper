# PasswordRulesHelper 1.0.5

# Introduction

_passwordRulesHelper_ is a JQuery plugin to help users to indicate a right password in your form.
There are 5 defaults rules, but you can add custom's rules.

https://codepen.io/Nirysse/pen/KgrJEN

# Installing

https://www.npmjs.com/package/passwordruleshelper

```
npm install passwordruleshelper
```

### Step 1 : Link required files

```html
<!-- jQuery library (served from Google) -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
<!-- passwordRulesHelper Javascript file -->
<script src="dist/js/passwordRulesHelper.min.js"></script>
<!-- passwordRulesHelper CSS file -->
<link href="/dist/css/passwordRulesHelper.min.css" rel="stylesheet" />
```

### Step 2 : Create HTML

```html
<input type='password' name='passwordField' id='passwordField'/>
```

### Step 3 : Call the PasswordRulesHelper

```javascript
$(function() {
    $('#passwordField').passwordRulesValidator();
});
```

##Configuration options

**rules**
Array where are all rules for password.

There are 5 rules already initialize : 

```
'rules' : {
    'length' : {
        'regex': '.{8,}',
        'name': 'length',
        'message': '8 characters',
        'enable': true
    },
    'lowercase' :{
        'regex': '[a-z]{1,}',
        'name': 'lowercase',
        'message': '1 lowercase',
        'enable': true
    },
    'uppercase' : {
        'regex': '[A-Z]{1,}',
        'name': 'uppercase',
        'message': '1 uppercase',
        'enable': true
    },
    'number' : {
        'regex': '[0-9]{1,}',
        'name': 'number',
        'message': '1 digit',
        'enable': true
    },
    'specialChar' : {
        'regex': '[^a-zA-Z0-9]{1,}',
        'name': 'special-char',
        'message': '1 special character',
        'enable': true
    }
}
```
You can add your own rules and change parmeters of existing rules.


**msgRules**
It's the message which displays above rules.

```
default: 'Your password must contain :'
```

**container**

The container where rules are display. If not specified, container was created under the password's field.
An object is expected.

```
default : null
example : container : $('#myCustomContainer')
```

**containerClass**

Add class to container.

```
default : null
example : containerClass : 'class'
```

**containerId**

Change id of container.

```
default : 'checkRulesList'
example : containerId : 'newId'
```

**okClass**

Add class to validate rules.

```
default : null
example : okClass : 'class'
```

**koClass**

Add class to invalid rules.

```
default : null
example : koClass : 'class'
```

**onLoad**

Executes before initialize PasswordRulesHelper

```
default : null
example : onLoad : function(){}
```


# Changelog

# License

Released under the MIT license - http://opensource.org/licenses/MIT

Let's get on with it!

