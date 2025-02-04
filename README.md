![VanillaToasts](http://puu.sh/iwxpd/eeee838c88.png)
-------

Create toasts & notifications on your website with ease. This library is extremely lightweight and depends on no other library. Simply load the script and css to your page, and use the simple API to start launching toasts on your page.

This version with bug fix of author's code.

Author's version: http://alexkvazos.github.io/VanillaToasts/

# Installing

Create in root folder file ```.npmrc``` and set next line:
```
@filtitov2001:registry=https://npm.pkg.github.com
```

Use this command in Terminal:

```
npm install @filtitov2001/vanillatoasts@1.5.0
```

Add this variable before using method ```create()```

```
var VanillaToasts = require('vanillatoasts');
```


Don't forget to include the CSS file!
```
 <link rel="stylesheet" href="/path/to/vanillatoasts/vanillatoasts.css">
```

# Usage

```

// Create a toast
let toast = VanillaToasts.create({
  title: 'Welcome to my site',
  text: 'This toast will hide after 5000ms or when you click it',
  type: 'warning', // success, info, warning, error   / optional parameter
  icon: '/img/alert-icon.jpg', // optional parameter
  timeout: 5000, // hide after 5000ms, // optional parameter
  callback: function() { ... } // executed when toast is clicked / optional parameter
});

// Hides the toast instantly
toast.hide()

// Timeout a toast at a later time
VanillaToasts.setTimeout(toast.id, 1000);

```

## Positioning the toast
To set a different position for the toast, use the `positionClass` property on the options of VanillaToast.

```
// Create a toast
let toast = VanillaToasts.create({
  title: 'Welcome to my site',
  text: 'This toast will hide after 5000ms or when you click it',
  positionClass: 'bottomLeft'
});

```

You can use any of the following values for the `positionClass` property:
* topRight
* topLeft
* topCenter
* bottomRight
* bottomLeft
* bottomCenter
