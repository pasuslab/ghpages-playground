## abandonedCart

#### Type: object

*_*

| Name    | Type    | Description | Example |
| ------- | ------- | ----------- | ------- |
| orderId | *string* | Order/Transaction ID | `"example"` |
| abandonedCartUrl | *string* | The URL to recover the abandoned cart<br/>**format: **`uri` | `"http://www.example.com/example"` |
| storeCode | *string* | Store or affiliation from which this transaction occurred | `"example"` |
| [amount](#amount) | *object* | Details of transaction | `{...}` |
| [products](#products) | *array[object]* | Details of transaction | `[{...}, {...}]` |
| [extraProperties](#extraproperties) | *object* | Extra pieces of information you can tie to events you track | `{...}` |

*****

## amount

#### Type: object

*Details of transaction*

| Name    | Type    | Description | Example |
| ------- | ------- | ----------- | ------- |
| total | *number* | Total is calculated adding revenue, shipping and tax amount and eliminating discounts amount | `42.0` |
| revenue | *number* | Revenue is calculated by multiplying the price at which products or services are sold by the number of units or amount sold | `42.0` |
| shipping | *number* | Shipping cost | `42.0` |
| tax | *number* | Total tax amount | `42.0` |
| discount | *number* | Total discount amount | `42.0` |
| [local](#local) | *object* | Currency local section | `{...}` |

*****

## local

#### Type: object

*Currency local section*

| Name    | Type    | Description | Example |
| ------- | ------- | ----------- | ------- |
| currency | *string* | Currency of the transaction | `"example"` |
| exchangeRate | *number* | Rate of exchange currency between default currency to local currency of the event | `42.0` |

*****

## products

#### Type: object

*_*

| Name    | Type    | Description | Example |
| ------- | ------- | ----------- | ------- |
| discount | *number* | The discount amount of order line | `42.0` |
| quantity | *number* | Quantity of a product | `42.0` |
| subtotal | *number* | The total amount of order line | `42.0` |
| price | *number* | Price of the product | `42.0` |
| name | *string* | Name of the product | `"example"` |
| sku | *string* | Sku of the product | `"example"` |
| type | *string* | The type of order line<br/>**one of: **`"sale"`, `"return"` | `"sale"` |
| [classifications](#classifications) | *array[object]* | The list of classifications of the product | `[{...}, {...}]` |
| category | *array[string]* | Categories list of the product | `["example", "example"]` |
| shortDescription | *string* | Short description of the product | `"example"` |
| linkUrl | *string* | The online catalogue of the product<br/>**format: **`uri` | `"http://www.example.com/example"` |
| imageUrl | *string* | The image of online catalogue of the product<br/>**format: **`uri` | `"http://www.example.com/example"` |
| coupon | *string* | Coupon code associated with a product | `"example"` |
| tax | *number* | The tax associated with the order line | `42.0` |
| id | *string* | Database id of the product | `"example"` |

*****

## classifications

#### Type: object

*_*

| Name    | Type    | Description | Example |
| ------- | ------- | ----------- | ------- |
| key | *string* | The key of the classification | `"example"` |
| value | *string* | The value of the classification | `"example"` |

*****

## extraProperties

#### Type: object

*Extra pieces of information you can tie to events you track*


*****
