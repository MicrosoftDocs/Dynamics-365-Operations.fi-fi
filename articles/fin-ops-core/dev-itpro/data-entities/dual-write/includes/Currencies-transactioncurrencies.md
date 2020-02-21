## <a name="currencies-to-transactioncurrencies"></a>Valuutat kohteeseen transactioncurrencies

Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Common Data Servicen välillä.

Lähdesuodatin: ((CURRENCYCODE != "999"))

Finance and Operations -kenttä | Määritystyyppi | Muu Dynamics 365 -kenttä | Oletusarvo
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
none | >> | exchangerate | 1
