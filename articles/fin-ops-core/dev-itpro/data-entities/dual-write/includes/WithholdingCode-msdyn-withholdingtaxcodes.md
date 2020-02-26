## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>Ennakonpidätyskoodit kohteeseen msdyn_withholdingtaxcodes

Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Common Data Servicen välillä.

Finance and Operations -kenttä | Määritystyyppi | Muu Dynamics 365 -kenttä | Oletusarvo
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
