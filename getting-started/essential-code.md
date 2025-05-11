# Essential code

Every Alicorn app needs to:

* inform the window manager it is ready to be shown to the user;
* forward global keyboard shortcuts to the window manager.

For that, you will have to:

* initialize the SDK;
* load the Alicorn keyboard handler;
* call the `alicorn.ready()` SDK method.

It is recommended that you use the following code, which will properly initialize the app when the DOM is done loading:

```javascript
window.addEventListener('load', async () => {
    window.alicorn = (await AlicornSDK.init())
    eval(AlicornKeyboardHandler);
    
    // Run your loading code here
    
    alicorn.ready();
})
```

After this code is executed, the `alicorn` object is accessible from everywhere, and the app is shown to the user.

{% hint style="info" %}
Keep in mind that all methods in the Alicorn SDK are called asynchronously (they return a Promise); you may use an `async` function to handle them synchronously
{% endhint %}
