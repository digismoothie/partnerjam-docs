# PartnerJam - Subscription Discount

⚠️️ To get the value of the discount, you must first make the [attribution](./ATTRIBUTION.md). You can make sure that attribution was finished by subscribing to onComplete  callback.

If we provide a discount for new users comming from PartnerJam we have to send request to PartnerJam with myshopify domain and our APP_ID.

This request return amount of discount if myshopify domain with APP_ID exists in PartnerJam database.

## Request

**Method:** GET \
**Path:** https://be-app.partnerjam.com/api/v1/discount-check/

**Params:**
| Name             | Example               |
| ---------------- | --------------------- |
| app_id           | 123456789             |
| myshopify_domain | example.myshopify.com |

**Example - request:** \
https://be-app.partnerjam.com/api/v1/discount-check/?app_id=123456789&myshopify_domain=example.myshopify.com

**Example - response:**
```json
{
  "discount": 80
}
```