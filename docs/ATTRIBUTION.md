# PartnerJam – Attribution

For app attribution, you need to insert a code snippet containing the APP_ID and the MyShopify domain parameter.

This snippet can be placed in your "base" component or template to ensure it renders on all pages of your application. This will ensure that attribution is sent to PartnerJam eventually. Additionally, it doesn’t matter if the attribution is sent multiple times—PartnerJam is equipped to handle that.

As an alternative, a more advanced solution is to place the snippet on a standalone page, which the merchant visits only after installation. In this case, you can use the onComplete callback to ensure the attribution is sent before redirecting the user to any other page.

**Subscription discount**: If you want to use the discount feature, please ensure you also implement the [subscription discount request](/docs/SUBSCRIPTION_DISCOUNT.md).

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
| myshopifyDomain | required | STRING   | Dynamically inserted myshopify.com domain of the store using your app |
| debug           | optional | BOOLEAN  | Enables debugging messages to JS console |
| onComplete      | optional | FUNCTION | Called when attribution was finished     |

