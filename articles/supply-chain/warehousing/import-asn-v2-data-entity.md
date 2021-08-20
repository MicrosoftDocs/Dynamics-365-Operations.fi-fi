---
title: Tuo saapuvat ASN:t V2-tietoyksikön kautta
description: Tässä aiheessa kerrotaan, miten saapuvien lisätoimitusilmoitusten (ASN-koodien) tuontia hallitaan saapuvan ASN V2 -tietoyksikön kautta.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8f3c42e28b01afd3b7ca8b1af8381dd5377e17eb31da655a397bd7805779f879
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751694"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a>Tuo saapuvat ASN:t V2-tietoyksikön kautta

[!include [banner](../../includes/banner.md)]

Advanced shipping notices (ASNs) ilmoittaa toimittajien toimituksista. Niiden avulla lähettäjä voi kuvata lähetyksen sisällön sekä siihen liittyvät lisätiedot, kuten nimikkeet ja pakkaustiedot.

ASN-määritykset voivat auttaa varastotyöntekijöitä tietämään, mitä saapuu milloin. Siksi he voivat valmistautua. Varastotyöntekijät voivat myös täsmätä ASN-numeroiden avulla lähetyksen tiedot aiemmin luotuun ostotilaukseen.

Tämä ohjeaihe sisältää skenaariokokoelman, jotka näyttävät esimerkkien avulla, miten ASN-tiedostoja käytetään.

> [!IMPORTANT]
> *Saapuva ASN* -tuonti koskee vain nimikkeitä, jotka on otettu käyttöön varaston lisähallinnassa (WMS). Ennen ASN-ilmoituksen vastaanottamista järjestelmään on rekisteröitävä ostotilaus ASN:in lähettävää toimittajaa vastaan.

## <a name="inbound-asn-v2-entity"></a>Saapuva ASN V2 -yksikkö

Saapuvat ASN-tiedot tuodaan käyttämällä *Saapuva ASN V2* -yhdistelmätietoyksikköä. *Saapuva ASN V2* käyttää etuna seuraavia yksiköitä:

- Saapuvan kuorman otsikko
- Saapuvan lähetyksen otsikko
- Saapuvan kuorman pakkausrakenteet
- Saapuvien kuormien pakkausrakenteen laatikot
- Saapuvien kuormien pakkausrakenteen laatikoiden rivit
- Saapuvien kuormien pakkausrakenteen rivit

*Saapuva ASN V2* -yhdistelmätietoyksikkö on tarkoitettu asynkroniseen integrointiin, jossa käytetään XML-tiedostoihin perustuvia tuontitietoja.

## <a name="xml-format-for-importing-asns"></a>XML-muoto ASN-tietojen tuomista varten

Microsoft Dynamics 365 Supply Chain Management tukee seuraavaa XML-muotoa ASN-tunnisteiden tuomista varten. Kukin XML-tiedoston solmu edustaa yksittäisen yksikön määritettä.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Esimerkkejä

Seuraavissa alisivustoissa on esimerkkejä toimittajien lähetysten ASN XML -tuontitiedostoista.

### <a name="example-1"></a>Esimerkki 1

Seuraavassa esimerkissä esitetään XML-tiedosto, joka sisältää yhden ostotilauksen toimittajalähetykset tuomista varten, kun tapaustietoja ei sisällytetä.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Esimerkki 2

Seuraavassa esimerkissä esitetään XML-tiedosto, joka sisältää yhden ostotilauksen toimittajalähetykset tuomista varten, kun tapaustiedot sisällytetään.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Esimerkki 3

Seuraavassa esimerkissä esitetään XML-tiedosto, joka sisältää useita ostotilauksia toimittajalähetykset tuomista varten, kun tapaustiedot sisällytetään.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>ASN-tiedoston tuonnin tulosten tarkastaminen

Noudattamalla näitä ohjeita voit tarkistaa ASN-tiedoston tuonnin tulokset.

1. Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.
1. Etsi ja avaa ASN-tuonnin yhteydessä luotu kuorma.
1. **Lataa**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat arvot.
1. **Kuormarivit**-pikavälilehdessä on XML-tiedostoon perustuvat ostotilausnumerot ja nimiketiedot.
1. Tarkista kuormituksen pakkausrakenne valitsemalla toimintoruudun **Lähetys ja vastaanotto** -välilehden **Vastaanotto**-ryhmästä **pakkausrakenne**.
1. **Lava**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat rekisterikilvet.
1. **Palvelupyynnöt**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat palvelupyynnöt.
1. **Nimikkeet**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat nimikkeet ja määrät.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
