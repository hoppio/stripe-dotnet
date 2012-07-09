# About the Library

Stripe is a simple, developer-friendly way to accept payments online. We believe that enabling transactions on the web is a problem rooted in code, not finance, and we want to help put more websites in business.

Currently, the library is feature complete for the Stripe API which can be found here: https://stripe.com/docs/api

# How can I install it using NuGet?

To install Stripe, run the following command in the Package Manager Console

```
PM> Install-Package Stripe
```

# How can I start using this library?

```csharp
var apiKey = "Your API Key";
var api = new StripeClient(apiKey);

var card = new CreditCard {
	Number = "4111111111111111",
	ExpMonth = 3,
	ExpYear = 2015
};

dynamic response = api.CreateCharge(
	amount: 100, // $100
	currency: "usd",
	card: card);

if (response.Paid)
	Console.WriteLine("Whoo Hoo...  We made our first sale!");
```

# Authors

*	Nick Berardi (https://github.com/nberardi)

Copyright 2012 Stripe, Inc.