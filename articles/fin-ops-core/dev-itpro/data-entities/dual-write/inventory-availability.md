---
title: Varaston käytettävyys kaksoiskirjoituksessa
description: Tässä ohjeaiheessa on tietoja varaston käytettävyyden tarkistamisesta kaksoiskirjoituksella.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: f967f832fc716938c544aad266d2c14a9ea19dd0ca8ee11fe228ce47145f3e78
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762423"
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

Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset     | kuvaus
---|---|---
[CDS:n käytettävissä olevan varaston merkinnät](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[CDS:n käytettävissä olevan varaston pyynnöt](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
