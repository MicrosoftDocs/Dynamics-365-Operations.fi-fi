## <a name="exchange-rate-currency-pair-to-msdyn_currencyexchangeratepairs"></a>Vaihtokurssin valuuttapari kohteeseen msdyn_currencyexchangeratepairs

Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Common Data Servicen välillä.

Finance and Operations -kenttä | Määritystyyppi | Muu Dynamics 365 -kenttä | Oletusarvo
---|---|---|---
EXCHANGERATEDISPLAYFACTOR | >< | msdyn_displayfactor | 
EXCHANGERATETYPENAME | = | msdyn_currencyexchangeratetypeid.msdyn_name | 
FROMCURRENCYCODE | = | msdyn_fromtransactioncurrencyid.isocurrencycode | 
TOCURRENCYCODE | = | msdyn_totransactioncurrencyid.isocurrencycode | 
