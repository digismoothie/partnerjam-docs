# PartnerJam - Attribution


## Simple solution

For app attribution we have put a code snippet to base file with APP_ID and MyShopify domain parameter.

### Example:
```html
<script type='text/javascript'>
  (function(d,o) {
    var sc="https://cdn.partnerjam.com/sdk/pj.umd.js",
    h=d.getElementsByTagName('head')[0],s=d.createElement('script');
    s.async=true;s.charset='utf-8';s.type='text/javascript';
    s.onload=function(){PJ.init(o)};s.src=sc;h.appendChild(s);
    })(document, {
      debug: false,
      appId: 123456789,
      myshopifyDomain: "example.myshopify.com",
      onComplete: function() {
        console.log("onComplete");
      }
  });
</script>
```

### Options
| KEY             | REQUIRED | TYPE     | DESCRIPTION                              |
| --------------- | -------- | -------- | ---------------------------------------- |
| appId           | required | INT      | Shopify App ID                           |
| myshopifyDomain | required | STRING   | MyShopify domain                         |
| debug           | optional | BOOLEAN  | enables debugging messages to JS console |
| onComplete      | optional | FUNCTION | Called when attribution was finished     |


## Advanced solution

For the attribution you can call the PJ Init function from the window object.

```html
<script type="application/javascript" src="https://cdn.partnerjam.com/sdk/pj.umd.js"></script>

<script type="text/javascript">
  window.PJ.init({
    debug: true,
    appId: 123456789,
    myshopifyDomain: "example.myshopify.com",
    onComplete: function() {
      console.log("onComplete");
    },
  });
</script>
```