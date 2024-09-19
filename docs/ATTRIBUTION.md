# PartnerJam - Attribution

For app attribution you have to insert a code snippet with APP_ID and MyShopify domain parameter.

The snippet can be placed in your "base" component / template so that it renders on all pages of your application. This way it will make sure that attribution will be sent to PartnerJam sooner or later. At the same time it doesn't matter if the attribution will be send repeatedly - PartnerJam is ready for that.

As an alternative (more advanced solution) the snippet can be placed on a standalone page that is visited by the merchant only after the installation. In such case you can use the `onComplete` callback to make sure the attribution was sent before redirecting user to any other page. 



## Code snippet:
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
