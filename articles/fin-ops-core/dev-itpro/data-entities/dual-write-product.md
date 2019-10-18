---
title: Yhtenäinen tuotekokemus
description: Tässä aiheessa käsitellään tuotetietojen integraatiota Finance and Operations -sovellusten ja Common Data Servicen välillä.
author: t-benebo
manager: AnnBe
ms.date: 09/3/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9dc26e0e50c0b77555d09e4a50b846c80b1d5760
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249325"
---
# <a name="unified-product-experience"></a>Yhtenäinen tuotekokemus

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Jos liiketoiminnan ekosysteemi muodostuu Dynamics 365 -sovelluksista, kuten Financesta, Supply Chain Managementista ja Salesista, asiakkaiden on luontevaa käyttää näitä sovelluksia tuotetietojen lähteenä. Tämä johtuu siitä, nämä sovellukset muodostavat toimivan tuoteinfrastruktuurin, jota kehittyneet hinnoittelukäsitteet ja tarkat käytettävissä olevan varaston tiedot täydentävät. Jos asiakkaat käyttävät ulkoista tuotteen elinkaaren hallinta- eli PLM-järjestelmää tuotetietojen lähteenä, he voivat kanavoida tuotteita Finance and Operations -sovelluksista muihin Dynamics 365 -sovelluksiin. Integroitu tuotetietomalli voidaan tuoda yhtenäisen tuotekokemuksen avulla Common Data Serviceen, jolloin kaikki sovelluksen käyttäjät, myös Power Platform -käyttäjät, voivat hyödyntää Finance and Operations -sovelluksista saatavia monipuolisia tuotetietoja.

Salesin tuotetietomalli.

![Salesin tuotetietomalli](media/dual-write-product-4.jpg)

Finance and Operations -sovellusten tuotetietomalli.

![Finance and Operationsin tuotetietomalli](media/dual-write-products-5.jpg)

Nämä kaksi tuotetietomallia on integroitu Common Data Servicessä seuraavan kuvan osoittamalla tavalla.

![Dynamics 365 -sovellusten tuotetietomalli](media/dual-write-products-6.jpg)

Tuotteiden kaksoiskirjoituksen yksikkökartat on suunniteltu vain yksisuuntaista tiedonkulkua varten, ja tieto kulkee Finance and Operations -sovelluksista Common Data Serviceen lähes reaaliaikaisesti. Tuoteinfrastruktuuri on kuitenkin avoin, joten se voidaan tarvittaessa muuttaa kaksisuuntaiseksi. Asiakkaat voivat mukauttaa sitä omalla vastuullaan, sillä Microsoft ei suosittele tätä lähestymistapaa.

## <a name="templates"></a>Mallit

Tuotetiedot sisältävät kaiken tuotteeseen liittyvät tiedot ja tuotteen määrityksen, kuten tuotedimensiot tai seuranta- ja varastodimensiot. Seuraava taulukko osoittaa, miten yksikkökarttakokoelma luodaan synkronoimaan tuotteita ja liittyviä tietoja.

Finance and Operations | Muut Dynamics 365 -sovellukset
-----------------------|--------------------------------
Vapautetut tuotteet V2 | msdyn\_sharedproductdetails
CDS-vapautetut erilliset tuotteet | Tuote
Tuotenumeron viivakoodi | msdyn\_productbarcodes
Tilauksen oletusasetukset | msdyn\_productdefaultordersettings
Tuotekohtaiset oletustilausasetukset | msdyn_productspecificdefaultordersettings
Tuotedimension ryhmät | msdyn\_productdimensiongroups
Varastodimensioryhmät | msdyn\_productstoragedimensiongroups
Seurantadimensioryhmät | msdyn\_producttrackingdimensiongroups
Värit | msdyn\_productcolors
Koot | msdyn\_productsizes
Tyylit | msdyn\_productsytles
Konfiguroinnit | msdyn\_productconfigurations
Päätuotteen värit | msdyn_sharedproductcolors
Päätuotteen koot | msdyn_sharedproductsizes
Päätuotteen tyylit | msdyn_sharedproductstyles
Päätuotteen konfiguraatiot | msdyn_sharedproductconfigurations
Kaikki tuotteet | msdyn_globalproducts
Yksikkö | uoms
Yksikkömuunnokset | msdyn_ unitofmeasureconversions
Tuotekohtainen mittayksikön muunnos | msdyn_productspecificunitofmeasureconversion
Sivustot | msdyn\_operationalsites
Varastot | msdyn\_inventwarehouses

[!include [symbols](../includes/dual-write-symbols.md)]

## <a name="integration-of-products"></a>Tuotteiden integrointi

Tässä mallissa tuotetta vastaa kahden Common Data Servicen yksikön yhdistelmä: **tuote** ja **msdyn\_sharedproductdetails**. Siinä missä ensimmäinen yksikkö sisältää tuotteen määritelmän (tuotteen yksilöivän tunnisteen, tuotteen nimien ja kuvauksen), toinen yksikkö sisältää tuotetasolla tallennetut kentät. Tuote määritetään näiden kahden yksikön yhdistelmällä varastointiyksikkö (SKU) -käsitteen mukaisesti. Kunkin julkaistun tuotteen tiedot ovat näissä yksiköissä (tuote ja jaetut tuotetiedot) Kaikkia tuotteita (julkaistuja ja julkaisemattomia) voidaan seurata **Tuotteet yleisesti** -yksikön avulla. 

Koska tuote ilmaista varastointiyksikkönä, käsitteet erilliset tuotteet, päätuotteet ja tuotevariantit voidaan tallentaa Common Data Serviceen seuraavasti:

- **Tuotteet, joissa on alatyypin tuote** ovat itsensä määrittäviä tuotteita. Niille ei tarvitse määrittää dimensioita. Tällainen tuote on esimerkiksi tietty kirja. Näille tuotteille luodaan yksi tietue **Tuote**-yksikössä ja yksi tietue **msdyn\_sharedproductdetails**-yksikössä. Tuoteperhetietuetta ei luoda.
- **Päätuotteita** käytetään yleisinä tuotteina, joissa olevat säännöt ja määritelmä määrittävät liiketoimintaprosessien toiminnan. Näiden määritelmien perusteella voidaan luoda tuotevarianteiksi kutsuttuja erillisiä tuotteita. Esimerkiksi t-paita on päätuote, jonka dimensioita väri ja koko voivat olla. Julkaistavissa varianteissa voi olla erilaisia dimensioyhdistelmiä, kuten s-kokoinen sininen t-paita tai m-kokoinen vihreä t-paita. Integroinnissa tuotetauluun luodaan kullekin variantille yksi tietue. Tämä tietue sisältää varianttikohtaiset tiedot, kuten eri dimensiot. Tuotteen yleiset tiedot tallennetaan **msdyn\_sharedproductdetails**-yksikköön. (Näitä yleisiä tietoja säilytetään päätuotteessa.) Lisäksi kullekin päätuotteelle luodaan lisäksi yksi tuoteperhetietue. Päätuotteen tiedot synkronoidaan Common Data Serviceen heti, kun vapautettu päätuote luodaan (mutta ennen varianttien vapauttamista).
- **Erillisillä tuotteilla** tarkoitetaan kaikkia tuotteiden alatyypin tuotteita ja kaikkia tuotevariantteja. 

![Tuotteiden tietomalli](media/dual-write-product.png)

Kun kaksoiskirjoitustoiminto on käytössä, Finance and Operationsin sovellukset synkronoidaan muissa Dynamics 365 -sovelluksissa **Luonnos**-tilassa. Ne lisätään ensimmäiseen hinnastoon, jossa on sama valuutta. Ne siis toisin sanoen lisätään ensimmäiseen Dynamics 365 -sovelluksen hinnastoon, joka vastaa sen yrityksen valuuttaa, jossa tuote vapautetaan Finance and Operations -sovelluksessa. 

Jos haluat synkronoida **Aktiivinen**-tilassa olevan tuotteen, jotta sitä voi käyttää esimerkiksi suoraan myyntitilauksen tarjouksissa, seuraavat asetukset on valittava: valitse ensin **Järjestelmä> Hallinto > Järjestelmän hallinta > Järjestelmäasetukset > Sales** ja sitten **Luo tuotteet aktiivisessa tilassa = kyllä**. 

### <a name="cds-released-distinct-products-to-product"></a>CDS on vapauttanut erilliset tuotteet tuotteeseen

**Tuote**-yksikön kentät määrittävät tuotteen. Se sisältää yksittäisiä tuotteita (tuotteita, joissa on alatyypin tuote) ja tuotevariantteja. Yhdistämismääritykset ovat seuraavassa taulukossa.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PRODUCTNUMBER | >> | productnumber
PRODUCTNAME | >> | name
PRODUCTDESCRIPTION | >> | kuvaus
ITEMNUMBER | >> | msdyn_itemnumber
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol
SALESPRICE | >> | hinta
UNITCOST | >> | currentcost
PRODUCTTYPE | >> | producttypecode
SALESUNITDECIMALPRECISION | >> | quantitydecimal
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle

### <a name="released-products-v2-to-msdyn_sharedproductdetails"></a>msdyn\_sharedproductdetails-yksikköön vapautetut tuotteet V2

**msdyn\_sharedproductdetails**-yksikkö sisältää ne Finance and Operations -sovellusten kentät, jotka määrittävät tuotteen ja jotka sisältävät tuotteen taloudelliset ja hallinnolliset tiedot. Yhdistämismääritykset ovat seuraavassa taulukossa.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PRODUCTNUMBER | > | msdyn_globalproduct.msdyn_productnumber
INTRASTATCHARGEPERCENTAGE | > | msdyn_intrastatchargepercentage
ITEMNUMBER | >> | msdyn_itemnumber
APPROXIMATESALESTAXPERCENTAGE | > | msdyn_approximatesalestaxpercentage
BESTBEFOREPERIODDAYS | > | msdyn_bestbeforeperioddays
CARRYINGCOSTABCCODE | >> | msdyn_carryingcostabccode
CONSTANTSCRAPQUANTITY | > | msdyn_constantscrapquantity
COSTCHARGESQUANTITY | > | msdyn_costchargesquantity
DEFAULTRECEIVINGQUANTITY | > | msdyn_defaultreceivingquantity
FIXEDPURCHASEPRICECHARGES | > | msdyn_fixedpurchasepricecharges
FIXEDSALESPRICECHARGES | > | msdyn_fixedsalespricecharges
GROSSDEPTH | > | msdyn_grossdepth
GROSSPRODUCTHEIGHT | > | msdyn_grossproductheight
GROSSPRODUCTWIDTH | > | msdyn_grossproductwidth
INVENTORYUNITSYMBOL | > | msdyn_inventoryunitsymbol.msdyn_symbol
ISDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_isdiscountposregistrationprohibited
ISEXEMPTFROMAUTOMATICNOTIFICATIONANDCANCELLATION | >> | msdyn_exemptautomaticnotificationcancel
ISINSTALLMENTELIGIBLE | >> | msdyn_isinstallmenteligible
ISINTERCOMPANYPURCHASEUSAGEBLOCKED | >> | msdyn_isintercompanypurchaseusageblocked
ISINTERCOMPANYSALESUSAGEBLOCKED | >> | msdyn_isintercompanysalesusageblocked
ISMANUALDISCOUNTPOSREGISTRATIONPROHIBITED | >> | msdyn_ismanualdiscposregistrationprohibited
ISPHANTOM | >> | msdyn_isphantom
ISPOSREGISTRATIONBLOCKED | >> | msdyn_isposregistrationblocked
ISPOSREGISTRATIONQUANTITYNEGATIVE | >> | msdyn_isposregistrationquantitynegative
ISPURCHASEPRICEAUTOMATICALLYUPDATED | >> | msdyn_ispurchasepriceautomaticallyupdated
ISPURCHASEPRICEINCLUDINGCHARGES | >> | msdyn_ispurchasepriceincludingcharges
ISSALESWITHHOLDINGTAXCALCULATED | >> | msdyn_issaleswithholdingtaxcalculated
ISRESTRICTEDFORCOUPONS | >> | msdyn_isrestrictedforcoupons
ISSALESPRICEADJUSTMENTALLOWED | >> | msdyn_issalespriceadjustmentallowed
ISSALESPRICEINCLUDINGCHARGES | >> | msdyn_issalespriceincludingcharges
ISSCALEPRODUCT | >> | msdyn_isscaleproduct
ISSHIPALONEENABLED | >> | msdyn_isshipaloneenabled
ISUNITCOSTPRODUCTVARIANTSPECIFIC | >> | msdyn_isunitcostproductvariantspecific
ISVARIANTSHELFLABELSPRINTINGENABLED | >> | msdyn_isvariantshelflabelsprintingenabled
ISZEROPRICEPOSREGISTRATIONALLOWED | >> | msdyn_iszeropriceposregistrationallowed
KEYINPRICEREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinpricerequirementsatposregister
KEYINQUANTITYREQUIREMENTSATPOSREGISTER | >> | msdyn_keyinquantityrequirementsatposregister
MARGINABCCODE | >> | msdyn_marginabccode
MAXIMUMPICKQUANTITY | > | msdyn_maximumpickquantity
MUSTKEYINCOMMENTATPOSREGISTER | >> | msdyn_mustkeyincommentatposregister
NECESSARYPRODUCTIONWORKINGTIMESCHEDULINGPROPERTYID | > | msdyn_necessaryproductionworkingtimeschedulingp
NETPRODUCTWEIGHT | > | msdyn_netproductweight
PACKINGDUTYQUANTITY | > | msdyn_packingdutyquantity
POSREGISTRATIONACTIVATIONDATE | > | msdyn_posregistrationactivationdate
POSREGISTRATIONBLOCKEDDATE | > | msdyn_posregistrationblockeddate
POSREGISTRATIONPLANNEDBLOCKEDDATE | > | msdyn_posregistrationplannedblockeddate
POTENCYBASEATTIBUTETARGETVALUE | > | msdyn_potencybaseattibutetargetvalue
POTENCYBASEATTRIBUTEVALUEENTRYEVENT | >> | msdyn_potencybaseattributevalueentryevent
PRODUCTTYPE | >> | msdyn_producttype
PRODUCTIONCONSUMPTIONDENSITYCONVERSIONFACTOR | > | msdyn_productionconsumptiondensityconversion
PRODUCTIONCONSUMPTIONDEPTHCONVERSIONFACTOR | > | msdyn_productionconsumptiondepthconversion
PRODUCTIONCONSUMPTIONHEIGHTCONVERSIONFACTOR | > | msdyn_productionconsumptionheightconversion
PRODUCTIONCONSUMPTIONWIDTHCONVERSIONFACTOR | > | msdyn_productionconsumptionwidthconversion
PRODUCTVOLUME | > | msdyn_productvolume
PURCHASECHARGESQUANTITY | > | msdyn_purchasechargesquantity
PURCHASEOVERDELIVERYPERCENTAGE | > | msdyn_purchaseoverdeliverypercentage
PURCHASEPRICE | > | msdyn_purchaseprice
PURCHASEPRICEDATE | > | msdyn_purchasepricedate
PURCHASEPRICINGPRECISION | > | msdyn_purchasepricingprecision
PURCHASEUNDERDELIVERYPERCENTAGE | > | msdyn_purchaseunderdeliverypercentage
RAWMATERIALPICKINGPRINCIPLE | >> | msdyn_rawmaterialpickingprinciple
SALESCHARGESQUANTITY | > | msdyn_saleschargesquantity
SALESOVERDELIVERYPERCENTAGE | > | msdyn_salesoverdeliverypercentage
SALESPRICE | > | msdyn_salesprice
SALESPRICECALCULATIONCHARGESPERCENTAGE | > | msdyn_salespricecalculationchargespercentage
SALESPRICECALCULATIONCONTRIBUTIONRATIO | > | msdyn_salespricecalculationcontributionratio
SALESPRICECALCULATIONMODEL | >> | msdyn_salespricecalculationmodel
SALESPRICEDATE | > | msdyn_salespricedate
SALESPRICINGPRECISION | > | msdyn_salespricingprecision
SALESUNDERDELIVERYPERCENTAGE | > | msdyn_salesunderdeliverypercentage
SALESUNITSYMBOL | > | msdyn_salesunitsymbol.msdyn_symbol
SCALEINDICATOR | >> | msdyn_scaleindicator
SELLSTARTDATE | > | msdyn_sellstartdate
SHELFADVICEPERIODDAYS | > | msdyn_shelfadviceperioddays
SHELFLIFEPERIODDAYS | > | msdyn_shelflifeperioddays
SHIPSTARTDATE | > | msdyn_shipstartdate
TAREPRODUCTWEIGHT | > | msdyn_tareproductweight
TRANSFERORDEROVERDELIVERYPERCENTAGE | > | msdyn_transferorderoverdeliverypercentage
TRANSFERORDERUNDERDELIVERYPERCENTAGE | > | msdyn_transferorderunderdeliverypercentage
UNITCOST | > | msdyn_unitcost
UNITCOSTDATE | > | msdyn_unitcostdate
UNITCOSTQUANTITY | > | msdyn_unitcostquantity
VARIABLESCRAPPERCENTAGE | > | msdyn_variablescrappercentage
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE1 | > | msdyn_warehousemobiledevicedescriptionline1
WAREHOUSEMOBILEDEVICEDESCRIPTIONLINE2 | > | msdyn_warehousemobiledevicedescriptionline2
WILLINVENTORYISSUEAUTOMATICALLYREPORTASFINISHED | >> | msdyn_willinventoryissueautoreportasfinished
WILLINVENTORYRECEIPTIGNOREFLUSHINGPRINCIPLE | >> | msdyn_willinventoryreceiptignoreflushing
WILLPICKINGWORKBENCHAPPLYBOXINGLOGIC | >> | msdyn_willpickingworkbenchapplyboxinglogic
WILLTOTALPURCHASEDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalpurchdiscountcalcincludeproduct
WILLTOTALSALESDISCOUNTCALCULATIONINCLUDEPRODUCT | >> | msdyn_willtotalsalesdiscountcalcincludeproduct
WILLWORKCENTERPICKINGALLOWNEGATIVEINVENTORY | >> | msdyn_willworkcenterpickingallownegativeinvent
YIELDPERCENTAGE | > | msdyn_yieldpercentage
ISUNITCOSTAUTOMATICALLYUPDATED | >> | msdyn_isunitcostautomaticallyupdated
PURCHASEUNITSYMBOL | > | msdyn_purchaseunitsymbol.msdyn_symbol
PURCHASEPRICEQUANTITY | > | msdyn_purchasepricequantity
ISUNITCOSTINCLUDINGCHARGES | >> | msdyn_isunitcostincludingcharges
FIXEDCOSTCHARGES | >> | msdyn_fixedcostcharges
MINIMUMCATCHWEIGHTQUANTITY | >> | msdyn_minimumcatchweightquantity
MAXIMUMCATCHWEIGHTQUANTITY | >> | msdyn_maximumcatchweightquantity
ALTERNATIVEITEMNUMBER | >> | msdyn_alternativeitemnumber.msdyn_itemnumber
BOMUNITSYMBOL | >> | msdyn_bomunitsymbol.msdyn_symbol
CATCHWEIGHTUNITSYMBOL | >> | msdyn_catchweightunitsymbol.msdyn_symbol
COMPARISONPRICEBASEUNITSYMBOL | >> | msdyn_comparisonpricebaseunitsymbol.msdyn_symbol
PRIMARYVENDORACCOUNTNUMBER | >> | msdyn_vendorid.msdyn_vendoraccountnumber
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight
PRODUCTDIMENSIONGROUPNAME | >> | msdyn_productdimensiongroupid.msdyn_groupname

## <a name="all-product-to-msdyn_global-products"></a>Kaikki tuotteet msdyn_global-tuotteisiin

Kaikkien tuotteiden yksikkö sisältää kaikki tuotteet, jotka ovat käytettävissä Finance and Operations -sovelluksessa – siis sekä vapautetut tuotteet että tuotteet, joita ei ole vapautettu. Näitä tuotteita voi käyttää Common Data Servicessä seuraavilla yhdistämismäärityksillä:

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PRODUCTNAME | >> | msdyn_productname
PRODUCTNUMBER | >> | msdyn_productnumber

## <a name="product-dimensions"></a>Tuotedimensiot 

Tuotedimensiot ovat ominaisuuksia, joilla voidaan tuotevariantti tunnistetaan. Neljä tuotedimensiota (väri, koko, tyyli ja konfiguraatio) yhdistetään myös Common Data Serviceen määrittämää tuotevariantteja. Seuraavassa kuvassa on Väri-tuotedimension tietomalli. Samaa mallia käytetään myös kokojen, tyylien ja konfiguraatioiden osalta. 

![Tuotteiden tietomalli](media/dual-write-product-2.PNG)

### <a name="colors"></a>Värit

Mahdolliset värit ovat käytettävissä Common Data Servicessä seuraavien yhdistämismääritysten kautta.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
COLORID | \>\> | msdyn\_productcolorname

### <a name="sizes"></a>Koot

Mahdolliset koot ovat käytettävissä Common Data Servicessä seuraavien yhdistämismääritysten kautta.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
SIZEID | \>\> | msdyn\_productsize

### <a name="styles"></a>Tyylit

Mahdolliset tyylit ovat käytettävissä Common Data Servicessä seuraavien yhdistämismääritysten kautta.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
STYLEID | \>\> | msdyn\_productstyle

### <a name="configurations"></a>Konfiguroinnit

Mahdolliset konfiguraatiot ovat käytettävissä Common Data Servicessä seuraavien yhdistämismääritysten kautta.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
CONFIGURATIONID | \>\> | msdyn\_name

Kun tuotteella on erilaisia tuotedimensioita (esimerkiksi koko ja väri ovat päätuotteen tuotedimensioita), kukin erillinen tuote (toisin sanoen kukin tuotevariantti) määritetään kyseisten tuotedimensioiden yhdistelmänä. Esimerkiksi tuotenumero B0001 on XS-kokoinen musta t-paita, ja tuotenumero B0002 on S-kokoinen musta t-paita. Tässä tapauksessa määritetään aiemmin luodut tuotedimensioyhdistelmät. Esimerkiksi edellisen esimerkin t-paita voi olla XS-kokoinen ja musta, S-kokoinen ja musta, M-kokoinen ja musta tai L-kokoinen ja musta mutta se ei voi olla XL-kokoinen ja musta. Päätuotteessa käytettävät tuotedimensiot on siis määritetty, ja variantit voidaan vapauttaa näiden arvojen perusteella.

Päätuotteen käytössä olevien tuotedimensioiden seuraamista varten on luotu seuraavat yksiköt, jotka on yhdistetty kunkin tuotedimension osalta Common Data Serviceen. Lisätietoja on kohdassa [Tuotetietojen yleiskatsaus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

### <a name="shared-product-color"></a>Jaettu tuoteväri

**Jaettu tuoteväri** -yksikkö ilmaisee värit, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Common Data Serviceen, jotta tiedot pysyvät yhdenmukaisina. Yhdistämismääritykset ovat seuraavassa taulukossa.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PRODUCTCOLORID | \>\> | msdyn\_productcolorid.msdyn\_productcolorname
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_retaildisplayorder

### <a name="shared-product-size"></a>Jaettu tuotekoko

**Jaettu tuotekoko** -yksikkö ilmaisee koot, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Common Data Serviceen, jotta tiedot pysyvät yhdenmukaisina. Yhdistämismääritykset ovat seuraavassa taulukossa.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
PRODUCTSIZEID | \>\> | msdyn\_productsizeid.msdyn\_productsize
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-style"></a>Jaettu tuotetyyli

**Jaettu tuotetyyli** -yksikkö ilmaisee tyylit, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Common Data Serviceen, jotta tiedot pysyvät yhdenmukaisina. Yhdistämismääritykset ovat seuraavassa taulukossa.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailsid.msdyn\_itemnumber
PRODUCTSTYLEID | \>\> | msdyn\_productstyleintegration
PRODUCTSTYLEID | \>\> | msdyn\_productstyleid.msdyn\_productstyle
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

### <a name="shared-product-configuration"></a>Jaettu tuotekonfiguraatio

**Jaettu tuotekonfiguraatio** -yksikkö ilmaisee konfiguraatiot, joita tietyllä päätuotteella voi olla. Tämä käsite siirretään Common Data Serviceen, jotta tiedot pysyvät yhdenmukaisina. Yhdistämismääritykset ovat seuraavassa taulukossa.

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
CONTAINERUNITSYMBOL | \>\> | msdyn\_containerunitsymbol
PRODUCTCONFIGURATIONID | \>\> | msdyn\_productconfigurationid.msdyn\_productconfiguration
PRODUCTMASTERNUMBER | \>\> | msdyn\_sharedproductdetailid.msdyn\_itemnumber
REPLENISHMENTWEIGHT | \>\> | msdyn\_replenishmentweight
DISPLAYSEQUENCENUMBER | \>\> | msdyn\_displaysequencenumber

## <a name="product-number-identifier-bar-codes"></a>Tuotenumeron viivakoodit

Tuotteen viivakoodeja käytetään tuotteiden yksilöimiseen. Nämä tuotteen viivakoodit otetaan käyttöön Common Data Servicessä seuraavilla yhdistämismäärityksillä:

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
PRODUCTNUMBER | \> | msdyn\_productnumberid.productnumber
BARCODE | \> | msdyn\_name
BARCODE | \> | msdyn\_barcode
PRODUCTQUANTITY | \> | msdyn\_productquantity
PRODUCTDESCRIPTION | \> | msdyn\_productdescription
BARCODESETUPID | \> | msdyn\_barcodesetupid
PRODUCTQUANTITYUNITSYMBOL | \> | msdyn\_unitofmeasureid.name
ISDEFAULTSCANNEDBARCODE | \>\> | msdyn\_isdefaultscannedbarcode
ISDEFAULTPRINTEDBARCODE | \>\> | msdyn\_isdefaultprintedbarcode
ISDEFAULTDISPLAYEDBARCODE | \>\> | msdyn\_isdefaultdisplayedbarcode

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Tilauksen oletusasetukset ja tuotekohtaiset tilauksen oletusasetukset

Tilauksen oletusasetukset määrittävät toimipaikan ja varaston, josta nimikkeet ovat lähtöisin tai säilytetään, minimi-, maksimi-, monikerta- ja vakiomäärät, joita käytetään kaupankäynnissä tai varastonhallinnassa, sekä läpimenoaikojen, lopetusmerkin ja luvattujen tilausten menetelmässä. Näitä tietoja voidaan käyttää CDS:ssä käyttämällä tilauksen oletusasetusten ja tuotekohtaisen tilauksen oletusasetusten yksikön avulla. Lisätietoja toiminnosta on kohdassa [Tilauksen oletusasetukset -sivu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

### <a name="default-order-settings"></a>Tilauksen oletusasetukset

Tilauksen oletusasetukset otetaan käyttöön Common Data Servicessä seuraavilla yhdistämismäärityksillä:

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
INVENTWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESORDERPROMISINGDEFAULTSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory

### <a name="product-specific-default-order-settings"></a>Tuotekohtaiset oletustilausasetukset

Tuotekohtaiset ilauksen oletusasetukset otetaan käyttöön Common Data Servicessä seuraavilla yhdistämismäärityksillä:

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
INVENTORYWAREHOUSEID | = | msdyn_inventorywarehouse.msdyn_warehouseidentifier
INVENTORYSITEID | = | msdyn_inventorysite.msdyn_siteid
INVENTORYATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_inventoryatpdelayeddemandoffsetdays
INVENTORYATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_inventoryatpdelayedsupplyoffsetdays
ITEMNUMBER | = | msdyn_itemnumber.msdyn_itemnumber
INVENTORYATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_inventoryatpbackwarddemandtimefencedays
INVENTORYATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_inventoryatpbackwardsupplytimefencedays
INVENTORYATPTIMEFENCEDAYS | = | msdyn_inventoryatptimefencedays
MAXIMUMINVENTORYORDERQUANTITY | = | msdyn_maximuminventoryorderquantity
MAXIMUMPROCUREMENTORDERQUANTITY | = | msdyn_maximumprocurementorderquantity
MAXIMUMSALESORDERQUANTITY | = | msdyn_maximumsalesorderquantity
MINIMUMINVENTORYORDERQUANTITY | = | msdyn_minimuminventoryorderquantity
MINIMUMPROCUREMENTORDERQUANTITY | = | msdyn_minimumprocurementorderquantity
MINIMUMSALESORDERQUANTITY | = | msdyn_minimumsalesorderquantity
STANDARDINVENTORYORDERQUANTITY | = | msdyn_standardinventoryorderquantity
STANDARDPROCUREMENTORDERQUANTITY | = | msdyn_standardprocurementorderquantity
STANDARDSALESORDERQUANTITY | = | msdyn_standardsalesorderquantity
INVENTORYLEADTIMEDAYS | = | msdyn_inventoryleadtimedays
INVENTORYQUANTITYMULTIPLES | = | msdyn_inventoryquantitymultiples
PROCUREMENTQUANTITYMULTIPLES | = | msdyn_procurementquantitymultiples
SALESQUANTITYMULTIPLES | = | msdyn_salesquantitymultiples
PROCUREMENTSITEID | = | msdyn_procurementsite.msdyn_siteid
PROCUREMENTLEADTIMEDAYS | = | msdyn_procurementleadtimedays
SALESSITEID | = | msdyn_salessite.msdyn_siteid
SALESATPDELAYEDDEMANDOFFSETDAYS | = | msdyn_salesatpdelayeddemandoffsetdays
SALESATPDELAYEDSUPPLYOFFSETDAYS | = | msdyn_salesatpdelayedsupplyoffsetdays
SALESATPBACKWARDDEMANDTIMEFENCEDAYS | = | msdyn_salesatpbackwarddemandtimefencedays
SALESATPBACKWARDSUPPLYTIMEFENCEDAYS | = | msdyn_salesatpbackwardsupplytimefencedays
SALESATPTIMEFENCEDAYS | = | msdyn_salesatptimefencedays
SALESLEADTIMEDAYS | = | msdyn_salesleadtimedays
PROCUREMENTWAREHOUSEID | = | msdyn_procurementwarehouse.msdyn_warehouseidentifier
SALESWAREHOUSEID | = | msdyn_saleswarehouse.msdyn_warehouseidentifier
AREINVENTORYDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_areinventoryorderdefaultsoverridden
INVENTORYORDERPROMISINGMETHOD | >< | msdyn_inventoryorderpromisingmethod
ISINVENTORYATPINCLUDINGPLANNEDORDERS | >< | msdyn_isinventoryatpincludingplannedorders
ISINVENTORYUSINGWORKINGDAYS | >< | msdyn_isinventoryusingworkingdays
ISINVENTORYSITEMANDATORY | >< | msdyn_isinventorysitemandatory
ISINVENTORYPROCESSINGSTOPPED | >< | msdyn_isinventoryprocessingstopped
ISPROCUREMENTUSINGWORKINGDAYS | >< | msdyn_isprocurementusingworkingdays
ISPROCUREMENTSITEMANDATORY | >< | msdyn_isprocurementsitemandatory
ISPROCUREMENTPROCESSINGSTOPPED | >< | msdyn_isprocurementprocessingstopped
ARESALESDEFAULTORDERSETTINGSOVERRIDDEN | >< | msdyn_aresalesorderdefaultsoverridden
SALESORDERPROMISINGMETHOD | >< | msdyn_salesorderpromisingmethod
ISSALESATPINCLUDINGPLANNEDORDERS | >< | msdyn_issalesatpincludingplannedorders
ISSALESSITEMANDATORY | >< | msdyn_issalessitemandatory
ISSALESLEADTIMEOVERRIDDEN | >< | msdyn_issalesleadtimeoverridden
ISSALESPROCESSINGSTOPPED | >< | msdyn_issalesprocessingstopped
ISINVENTORYWAREHOUSEMANDATORY | >< | msdyn_isinventorywarehousemandatory
ISPROCUREMENTWAREHOUSEMANDATORY | >< | msdyn_isprocurementwarehousemandatory
ISSALESWAREHOUSEMANDATORY | >< | msdyn_issaleswarehousemandatory
OPERATIONALSITEID | = | msdyn_operationalsite.msdyn_siteid
PRODUCTCOLORID | = | msdyn_productcolor.msdyn_productcolorname
PRODUCTCONFIGURATIONID | = | msdyn_productconfiguration.msdyn_productconfiguration
PRODUCTSIZEID | = | msdyn_productsize.msdyn_productsize
PRODUCTSTYLEID | = | msdyn_productstyle.msdyn_productstyle

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Mittayksikkö ja mittayksikön muunnokset

Mittayksikkö ja sen muunnokset saadaan käytettäväksi Common Data Servicessä seuraavassa kuvassa olevan tietomallin mukaisesti.

![Tuotteiden tietomalli](media/dual-write-product-3.PNG)

Mittayksikkökäsite on integroitu Finance and Operations- ja muiden Dynamics 365 -sovellusten välillä. Kullekin Finance and Operations -sovelluksen yksikköluokalle luodaan Dynamics 365 -sovelluksessa yksikköryhmä, joka sisältää yksikköluokkaan kuuluvat yksiköt. Jokaiselle yksikköryhmälle luodaan myös oletusarvoinen perusyksikkö. 

### <a name="unit-of-measure"></a>Mittayksikkö

Finance and Operations -sovellusten mittayksiköt saadaan käyttöön Common Data Servicessä seuraavien yhdistämismääritysten avulla:

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
UNITSYMBOL | >> | msdyn_symbol
UNITCLASS | >> | msdyn_externalunitclassname
DECIMALPRECISION | >> | msdyn_decimalprecision
ISBASEUNIT | >> | msdyn_isbaseunit
ISSYSTEMUNIT | >> | msdyn_issystemunit
SYSTEMOFUNITS | >> | msdyn_systemofunits
UNITSYMBOL | >> | name
UNITDESCRIPTION | >> | msdyn_description

### <a name="unit-of-measure-conversions"></a>Mittayksiköiden muunnokset

Finance and Operations -sovellusten mittayksiköiden muunnokset saadaan käyttöön Common Data Servicessä seuraavien yhdistämismääritysten avulla:

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol

### <a name="product-specific-unit-of-measure-conversions"></a>Tuotekohtaiset mittayksikön muunnokset

Finance and Operations -sovellusten tuotekohtaiset mittayksikön muunnokset saadaan käyttöön Common Data Servicessä seuraavien yhdistämismääritysten avulla:

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
DENOMINATOR | = | msdyn_denominator
NUMERATOR | = | msdyn_numerator
FACTOR | = | msdyn_factor
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber
INNEROFFSET | = | msdyn_inneroffset
OUTEROFFSET | = | msdyn_outeroffset
ROUNDING | >< | msdyn_rounding

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Tuotekäytännöt: dimensio-, seuranta- ja varastoryhmät

Tuotekäytännöt ovat käytäntöjoukkoja, jolla määritetään varaston tuotteet ja niiden ominaisuudet. Tuotedimensioryhmää, tuotteen seurantadimensioryhmää ja varastodimensioryhmää voi etsiä tuotekäytäntöinä. 

### <a name="product-dimension-group"></a>Tuotedimensioryhmä

Tuotedimensioryhmä määrittää, mitkä tuotedimensiot määrittävät tuotteet. Mahdollisia tuotedimensioryhmiä on neljä: koko, väri, tyyli ja konfigurointi. Tuotedimensioryhmät saadaan käyttöön Common Data Servicessä seuraavilla yhdistämismäärityksillä: 

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
WILLSALESPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willsalespricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willpurchasepricesearchuseproductsize
WILLSALESPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willsalespricesearchuseprodconfig
WILLSALESPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willsalespricesearchuseproductcolor
WILLPURCHASEPRICESEARCHUSEPRODUCTSTYLE | >< | msdyn_willpurchasepricesearchuseproductstyle
WILLPURCHASEPRICESEARCHUSEPRODUCTCONFIGURATION | >< | msdyn_willpurchpricesearchuseprodconfig
WILLPURCHASEPRICESEARCHUSEPRODUCTCOLOR | >< | msdyn_willpurchpricesearchuseproductcolor
ISPRODUCTSTYLEACTIVE | >< | msdyn_isproductstyleactive
ISPRODUCTSIZEACTIVE | >< | msdyn_isproductsizeactive
ISPRODUCTCONFIGURATIONACTIVE | >< | msdyn_isproductconfigurationactive
ISPRODUCTCOLORACTIVE | >< | msdyn_isproductcoloractive
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
PRODUCTVARIANTNOMENCLATURENAME | = | msdyn_productvariantnomenclaturename
WILLSALESPRICESEARCHUSEPRODUCTSIZE | >< | msdyn_willsalespricesearchuseproductsize

### <a name="product-tracking-dimension-group"></a>Tuotteen seurantadimensioryhmä

Tuotteen seurantadimensioryhmä ilmaisee menetelmän, jolla varastossa olevia tuotteita seurataan. Niitä voi käyttää Common Data Servicessä seuraavilla yhdistämismäärityksillä: 

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
SERIALNUMBERCAPTURINGOPERATION | >< | msdyn_serialnumbercapturingoperation
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISSERIALNUMBERENABLEDFORPRODUCTIONCONSUMPTIONPROCESS | >< | msdyn_issnenabledforpcprocess
ISSERIALNUMBERCONTROLENABLED | >< | msdyn_isserialnumbercontrolenabled
ISSERIALNUMBERENABLEDFORSALESPROCESS | >< | msdyn_isserialnumberenabledforsalesprocess
ISSERIALNUMBERACTIVE | >< | msdyn_isserialnumberactive
ISSALESPRICEBYSERIALNUMBER | >< | msdyn_issalespricebyserialnumber
ISSALESPRICEBYBATCHNUMBER | >< | msdyn_issalespricebybatchnumber
ISPURCHASEPRICEBYSERIALNUMBER | >< | msdyn_ispurchasepricebyserialnumber
ISPURCHASEPRICEBYBATCHNUMBER | >< | msdyn_ispurchasepricebybatchnumber
ISPRIMARYSTOCKINGENABLEDFORSERIALNUMBER | >< | msdyn_isprimarystockingenabledforsn
ISPRIMARYSTOCKINGENABLEDFORBATCHNUMBER | >< | msdyn_isprimarystockingenabledforbn
ISPHYSICALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isphysicalinventoryenabledforsn
ISPHYSICALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isphysicalinventoryenabledforbn
ISFINANCIALINVENTORYENABLEDFORSERIALNUMBER | >< | msdyn_isfinancialinventoryenabledforsn
ISFINANCIALINVENTORYENABLEDFORBATCHNUMBER | >< | msdyn_isfinancialinventoryenabledforbn
ISCOVERAGEPLANENABLEDFORSERIALNUMBER | >< | msdyn_iscoverageplanenabledforserialnumber
ISCOVERAGEPLANENABLEDFORBATCHNUMBER | >< | msdyn_iscoverageplanenabledforbatchnumber
ISBLANKRECEIPTALLOWEDFORSERIALNUMBER | >< | msdyn_isblankreceiptallowedforserialnumber
ISBLANKRECEIPTALLOWEDFORBATCHNUMBER | >< | msdyn_isblankreceiptallowedforbatchnumber
ISBLANKISSUEALLOWEDFORSERIALNUMBER | >< | msdyn_isblankissueallowedforserialnumber
ISBLANKISSUEALLOWEDFORBATCHNUMBER | >< | msdyn_isblankissueallowedforbatchnumber
ISBATCHNUMBERACTIVE | >< | msdyn_isbatchnumberactive
ISINVENTORYOWNERACTIVE | >< | msdyn_isinventoryowneractive

### <a name="product-storage-dimension-group"></a>Tuotteen varastodimensioryhmä

Tuotteen varastodimensioryhmä ilmaisee menetelmän, jolla tuotteiden sijoittaminen varastoon määritetään. Niitä voi käyttää Common Data Servicessä seuraavilla yhdistämismäärityksillä: 

Lähdetaulu | Määritystyyppi | Kohdekenttä
---|---|---
WILLSALESPRICESEARCHUSEWAREHOUSE | >< | msdyn_willsalespricesearchusewarehouse
WILLSALESPRICESEARCHUSESITE | >< | msdyn_willsalespricesearchusesite
WILLSALESPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willsalespricesearchuseinventorystatus
WILLPURCHASEPRICESEARCHUSEWAREHOUSE | >< | msdyn_willpurchasepricesearchusewarehouse
WILLPURCHASEPRICESEARCHUSESITE | >< | msdyn_willpurchasepricesearchusesite
WILLPURCHASEPRICESEARCHUSEINVENTORYSTATUS | >< | msdyn_willpurchpricesearchuseinventstatus
WILLCOVERAGEPLANNINGUSEWAREHOUSE | >< | msdyn_willcoverageplanusewarehouse
WILLCOVERAGEPLANNINGUSELOCATION | >< | msdyn_iscoverageplanenabledforlocation
WILLCOVERAGEPLANNINGUSEINVENTORYSTATUS | >< | msdyn_willcoverageplanuseinventorystatus
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >< | msdyn_areadvancedwmprocessesenabled
ISWAREHOUSEPRIMARYSTORAGEDIMENSION | >< | msdyn_iswarehouseprimarystoragedimension
ISWAREHOUSEMANDATORY | >< | msdyn_iswarehousemandatory
ISPHYSICALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isphysicalinventoryenabledforwarehouse
ISPHYSICALINVENTORYENABLEDFORLOCATION | >< | msdyn_isphysicalinventoryenabledforlocation
ISLOCATIONACTIVE | >< | msdyn_islocationactive
ISFINANCIALINVENTORYENABLEDFORWAREHOUSE | >< | msdyn_isfinancialinventoryenabledforwarehouse
GROUPNAME | = | msdyn_groupname
GROUPDESCRIPTION | = | msdyn_groupdescription
ISBLANKRECEIPTALLOWEDFORLOCATION | >< | msdyn_isblankreceiptallowedforlocation
ISBLANKISSUEALLOWEDFORLOCATION | >< | msdyn_isblankissueallowedforlocation

