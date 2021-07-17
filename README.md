# ghasedak-kavenegar-node

## Installation

<p> For installing Ghasedak-Kavenegar  use this command via npm </p>

```node
npm install ghasedakkavenegar
```


If you don't have npm you can easily install it from  [npm website](https://www.npmjs.com/)


## Usage

Well, There is two  example to Send SMS by node below.

```node
var Kavenegar = require('ghasedakkavenegar');
var api = Kavenegar.KavenegarApi({
    apikey: 'your apikey here'
});
api.Send({
        message: "وبسرویس قاصدک برای کاربران کاوه‌نگار",
        sender: "10004346",
        receptor: "09123456789,09367891011"
    },
    function(response, status) {
        console.log(response);
        console.log(status);
    });
/*
sample output
{
    "return":
    {
        "status":200,
        "message":"تایید شد"
    },
    "entries": 
    [
        {
            "messageid":8792343,
            "message":"وبسرویس قاصدک برای کاربران کاوه‌نگار",
            "status":1,
            "statustext":"در صف ارسال",
            "sender":"10004346",
            "receptor":"09123456789",
            "date":1356619709,
            "cost":120
        },
        {
            "messageid":8792344,
            "message":"وبسرویس قاصدک برای کاربران کاوه‌نگار",
            "status":1,
            "statustext":"در صف ارسال",
            "sender":"10004346",
            "receptor":"09367891011",
            "date":1356619709,
            "cost":120
        }
    ]
}
*/
```
```node
var Kavenegar = require('kavenegar');
var api = Kavenegar.KavenegarApi({
    apikey: 'your apikey here'
});
api.VerifyLookup({
    receptor: "09361234567",
    token: "852596",
    template: "registerverify"
}, function(response, status) {
    console.log(response);
    console.log(status);
});
/*
sample output
{
    "return":
    {
        "status":200,
        "message":"تایید شد"
    },
    "entries": {
            "messageid":8792343,
			"message": "ممنون از ثبت نام شما کد تایید عضویت  : 852596",
            "status":5,
            "statustext":"ارسال به مخابرات",
            "sender":"10004346",
            "receptor":"09361234567",
            "date":1356619709,
            "cost":120
   }    
    
}
*/
```
## Contribution

Bug fixes, docs, and enhancements welcome! Please let us know <a href="mailto:support@ghasedak.me?Subject=SDK" target="_top">support@ghasedak.me</a>



