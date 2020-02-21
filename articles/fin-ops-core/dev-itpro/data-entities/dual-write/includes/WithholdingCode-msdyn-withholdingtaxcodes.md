## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>Ieturēto nodokļu kodi uz msdyn_withholdingtaxcodes

Šī veidne sinhronizē datus starp Finance and Operations programmām un Common Data Service.

Finance and Operations lauks | Kartes veids | Cits Dynamics 365 lauks | Noklusējuma vērtība
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
