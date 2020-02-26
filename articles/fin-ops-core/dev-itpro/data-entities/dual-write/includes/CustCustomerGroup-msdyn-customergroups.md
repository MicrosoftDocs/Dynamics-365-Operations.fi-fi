## <a name="customer-groups-to-msdyn_customergroups"></a>Asiakasryhmät kohteeseen msdyn_customergroups

Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Common Data Servicen välillä.

Finance and Operations -kenttä | Määritystyyppi | Muu Dynamics 365 -kenttä | Oletusarvo
---|---|---|---
CUSTOMERGROUPID | = | msdyn_groupid | 
DESCRIPTION | = | msdyn_description | 
ISSALESTAXINCLUDEDINPRICE | >< | msdyn_issalestaxincludedinprice | 
PAYMENTTERMID | = | msdyn_paymenttermid.msdyn_name | 
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn_clearingperiodpaymenttermname.msdyn_name | 
