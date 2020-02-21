## <a name="currencies-to-transactioncurrencies"></a>Valūtas uz transactioncurrencies

Šī veidne sinhronizē datus starp Finance and Operations programmām un Common Data Service.

Avota filtrs: ((CURRENCYCODE != "999"))

Finance and Operations lauks | Kartes veids | Cits Dynamics 365 lauks | Noklusējuma vērtība
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NOSAUKUMS | = | currencyname | 
SIMBOLS | = | currencysymbol | 
nav | >> | exchangerate | 1
