---
title: Varaston käytettävyys kaksoiskirjoituksessa
description: Tässä ohjeaiheessa on tietoja varaston käytettävyyden tarkistamisesta kaksoiskirjoituksella.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839546"
---
# <a name="inventory-availability-in-dual-write"></a>Varaston käytettävyys kaksoiskirjoituksessa

[!include [banner](../../includes/banner.md)]

Varaston käytettävyyttä käyttämällä voi tarkistaa varaston, ennen kuin tuote lisätään Microsoft Dynamics 365 Salesin **Tarjoukset**-, **Tilaukset**- tai **Laskut**-sivulla. Esimerkiksi varaston tarkistaminen ja täyttämispäivän määrittäminen ovat yksi [prospektista käteiseksi](dual-write-prospect-to-cash.md) -prosessin avaintehtävistä.

Jos varastoa ei ole riittävästi, voit arvioida toimituspäivämäärän arvioitujen varastovastaanottojen ja varastostaottojen perusteella. Voit myös tarkistaa tuotteen luvattavissa oleva määrä (ATP) -tiedot, joiden ATP-määrä löytyy ennalta määritetystä aikaraja-arvotyypistä.

## <a name="on-hand-inventory"></a>Käytettävissä oleva varasto

Dynamics 365 Salesin **Tarjous**-, **Tilaus**- ja **Lasku** -sivujen otsikkoon on lisätty uusi **Käytettävissä oleva varasto** -painike. Kun valitset tämän painikkeen, näyttöön avautuu valintaikkuna, jossa voit määrittää yrityksen ja tuotteen, jonka käytettävissä olevan varaston haluat tarkistaa. Tässä valintaikkunassa on samat tiedot kuin [käytettävissä olevassa varastossa](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Valintaikkuna palauttaa varastotiedot Dynamics 365 Supply Chain Managementista. Nämä tiedot sisältävät seuraavat määrät:

- Varastosaldo
- Varattu varastosaldo
- Käytettävissä oleva varastosaldo
- Tilattu määrä
- Tilauksessa oleva määrä
- Varattu tilattu määrä
- Käytettävissä oleva kokonaismäärä

## <a name="atp-information"></a>ATP-tiedot

Salesissa on lisätty uusi **ATP-tiedot**-painike **Tarjoukset**-, **Tilaukset**- ja **Laskut**-sivujen rivinimikkeisiin. Kun tämä painike valitaan, avautuvassa valintaikkunassa voi määrittää yrityksen, tuotteen, varastopaikan, varastointivaraston ja tilausmäärän. Tässä valintaikkunassa on samat asetukset, jotka kuvattiin kohdassa [Luvatut tilaukset](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Valintaikkuna palauttaa ATP-tiedot Supply Chain Managementissa. Nämä tiedot sisältävät seuraavat määrät:

- ATP-määrä
- Vastaanoton määrä
- Varasto-oton määrä
- Varastosaldo

## <a name="how-it-works"></a>Näin se toimii

Kun **Käytettävissä oleva varasto** -painike valitaan **Tarjoukset**-, **Tilaukset**- tai **Laskut**-sivulla, reaaliaikainen kaksoiskirjoituskutsu tehdään **Käytettävissä oleva varasto** -ohjelmistorajapinnassa. Ohjelmointirajapinta laskee annetun tuotteen käytettävissä olevan varaston. Tulos tallennetaan **InventCDSInventoryOnHandRequestEntity**- ja **InventCDSInventoryOnHandEntryEntity**-taulukoihin ja kirjoitettaan sitten kaksoiskirjoituksella Dataverseen. Tämän toiminnon käyttämistä varten on suoritettava seuraavat kaksoiskirjoituksen määritykset. Ohita ensimmäinen synkronointi määrityksiä suoritettaessa.

- CDS:n käytettävissä olevan varaston viennit (msdyn_inventoryonhandentries)
- CDS:n käytettävissä olevan varaston pyynnöt (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Mallit
Seuraavat mallit ovat käytettävissä käytettävissä olevan varaston tietojen tuominen nähtäville

Finance and Operations -sovellukset | Asiakkaiden aktivointisovellus | kuvaus 
---|---|---
[CDS:n käytettävissä olevan varaston merkinnät](#145) | msdyn_inventoryonhandentries |
[CDS:n käytettävissä olevan varaston pyynnöt](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>CDS:n käytettävissä olevan varaston viennit (msdyn_inventoryonhandentries)

Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Dataversen välillä.

Finance and Operations -kenttä | Määritystyyppi | Asiakkaiden aktivointi -kenttä | Oletusarvo
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>CDS:n käytettävissä olevan varaston pyynnöt (msdyn_inventoryonhandrequests)

Tämä malli synkronoi tiedot Finance and Operations -sovellusten ja Dataversen välillä.

Finance and Operations -kenttä | Määritystyyppi | Asiakkaiden aktivointi -kenttä | Oletusarvo
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]