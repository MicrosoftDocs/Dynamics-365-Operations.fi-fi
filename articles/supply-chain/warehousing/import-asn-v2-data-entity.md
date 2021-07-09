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
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249093"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="7df6f-103">Tuo saapuvat ASN:t V2-tietoyksikön kautta</span><span class="sxs-lookup"><span data-stu-id="7df6f-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7df6f-104">Advanced shipping notices (ASNs) ilmoittaa toimittajien toimituksista.</span><span class="sxs-lookup"><span data-stu-id="7df6f-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="7df6f-105">Niiden avulla lähettäjä voi kuvata lähetyksen sisällön sekä siihen liittyvät lisätiedot, kuten nimikkeet ja pakkaustiedot.</span><span class="sxs-lookup"><span data-stu-id="7df6f-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="7df6f-106">ASN-määritykset voivat auttaa varastotyöntekijöitä tietämään, mitä saapuu milloin.</span><span class="sxs-lookup"><span data-stu-id="7df6f-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="7df6f-107">Siksi he voivat valmistautua.</span><span class="sxs-lookup"><span data-stu-id="7df6f-107">Therefore, they can prepare.</span></span> <span data-ttu-id="7df6f-108">Varastotyöntekijät voivat myös täsmätä ASN-numeroiden avulla lähetyksen tiedot aiemmin luotuun ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="7df6f-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="7df6f-109">Tämä ohjeaihe sisältää skenaariokokoelman, jotka näyttävät esimerkkien avulla, miten ASN-tiedostoja käytetään.</span><span class="sxs-lookup"><span data-stu-id="7df6f-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7df6f-110">*Saapuva ASN* -tuonti koskee vain nimikkeitä, jotka on otettu käyttöön varaston lisähallinnassa (WMS).</span><span class="sxs-lookup"><span data-stu-id="7df6f-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="7df6f-111">Ennen ASN-ilmoituksen vastaanottamista järjestelmään on rekisteröitävä ostotilaus ASN:in lähettävää toimittajaa vastaan.</span><span class="sxs-lookup"><span data-stu-id="7df6f-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="7df6f-112">Saapuva ASN V2 -yksikkö</span><span class="sxs-lookup"><span data-stu-id="7df6f-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="7df6f-113">Saapuvat ASN-tiedot tuodaan käyttämällä *Saapuva ASN V2* -yhdistelmätietoyksikköä.</span><span class="sxs-lookup"><span data-stu-id="7df6f-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="7df6f-114">*Saapuva ASN V2* käyttää etuna seuraavia yksiköitä:</span><span class="sxs-lookup"><span data-stu-id="7df6f-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="7df6f-115">Saapuvan kuorman otsikko</span><span class="sxs-lookup"><span data-stu-id="7df6f-115">Inbound load header</span></span>
- <span data-ttu-id="7df6f-116">Saapuvan lähetyksen otsikko</span><span class="sxs-lookup"><span data-stu-id="7df6f-116">Inbound shipment header</span></span>
- <span data-ttu-id="7df6f-117">Saapuvan kuorman pakkausrakenteet</span><span class="sxs-lookup"><span data-stu-id="7df6f-117">Inbound load packing structures</span></span>
- <span data-ttu-id="7df6f-118">Saapuvien kuormien pakkausrakenteen laatikot</span><span class="sxs-lookup"><span data-stu-id="7df6f-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="7df6f-119">Saapuvien kuormien pakkausrakenteen laatikoiden rivit</span><span class="sxs-lookup"><span data-stu-id="7df6f-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="7df6f-120">Saapuvien kuormien pakkausrakenteen rivit</span><span class="sxs-lookup"><span data-stu-id="7df6f-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="7df6f-121">*Saapuva ASN V2* -yhdistelmätietoyksikkö on tarkoitettu asynkroniseen integrointiin, jossa käytetään XML-tiedostoihin perustuvia tuontitietoja.</span><span class="sxs-lookup"><span data-stu-id="7df6f-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="7df6f-122">XML-muoto ASN-tietojen tuomista varten</span><span class="sxs-lookup"><span data-stu-id="7df6f-122">XML format for importing ASNs</span></span>

<span data-ttu-id="7df6f-123">Microsoft Dynamics 365 Supply Chain Management tukee seuraavaa XML-muotoa ASN-tunnisteiden tuomista varten.</span><span class="sxs-lookup"><span data-stu-id="7df6f-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="7df6f-124">Kukin XML-tiedoston solmu edustaa yksittäisen yksikön määritettä.</span><span class="sxs-lookup"><span data-stu-id="7df6f-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

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

## <a name="examples"></a><span data-ttu-id="7df6f-125">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="7df6f-125">Examples</span></span>

<span data-ttu-id="7df6f-126">Seuraavissa alisivustoissa on esimerkkejä toimittajien lähetysten ASN XML -tuontitiedostoista.</span><span class="sxs-lookup"><span data-stu-id="7df6f-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="7df6f-127">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="7df6f-127">Example 1</span></span>

<span data-ttu-id="7df6f-128">Seuraavassa esimerkissä esitetään XML-tiedosto, joka sisältää yhden ostotilauksen toimittajalähetykset tuomista varten, kun tapaustietoja ei sisällytetä.</span><span class="sxs-lookup"><span data-stu-id="7df6f-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

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

### <a name="example-2"></a><span data-ttu-id="7df6f-129">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="7df6f-129">Example 2</span></span>

<span data-ttu-id="7df6f-130">Seuraavassa esimerkissä esitetään XML-tiedosto, joka sisältää yhden ostotilauksen toimittajalähetykset tuomista varten, kun tapaustiedot sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="7df6f-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

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

### <a name="example-3"></a><span data-ttu-id="7df6f-131">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="7df6f-131">Example 3</span></span>

<span data-ttu-id="7df6f-132">Seuraavassa esimerkissä esitetään XML-tiedosto, joka sisältää useita ostotilauksia toimittajalähetykset tuomista varten, kun tapaustiedot sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="7df6f-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

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

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="7df6f-133">ASN-tiedoston tuonnin tulosten tarkastaminen</span><span class="sxs-lookup"><span data-stu-id="7df6f-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="7df6f-134">Noudattamalla näitä ohjeita voit tarkistaa ASN-tiedoston tuonnin tulokset.</span><span class="sxs-lookup"><span data-stu-id="7df6f-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="7df6f-135">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="7df6f-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7df6f-136">Etsi ja avaa ASN-tuonnin yhteydessä luotu kuorma.</span><span class="sxs-lookup"><span data-stu-id="7df6f-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="7df6f-137">**Lataa**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat arvot.</span><span class="sxs-lookup"><span data-stu-id="7df6f-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="7df6f-138">**Kuormarivit**-pikavälilehdessä on XML-tiedostoon perustuvat ostotilausnumerot ja nimiketiedot.</span><span class="sxs-lookup"><span data-stu-id="7df6f-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="7df6f-139">Tarkista kuormituksen pakkausrakenne valitsemalla toimintoruudun **Lähetys ja vastaanotto** -välilehden **Vastaanotto**-ryhmästä **pakkausrakenne**.</span><span class="sxs-lookup"><span data-stu-id="7df6f-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="7df6f-140">**Lava**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat rekisterikilvet.</span><span class="sxs-lookup"><span data-stu-id="7df6f-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="7df6f-141">**Palvelupyynnöt**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat palvelupyynnöt.</span><span class="sxs-lookup"><span data-stu-id="7df6f-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="7df6f-142">**Nimikkeet**-pikavälilehdessä pitäisi nähdä XML-tiedostoon perustuvat nimikkeet ja määrät.</span><span class="sxs-lookup"><span data-stu-id="7df6f-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
