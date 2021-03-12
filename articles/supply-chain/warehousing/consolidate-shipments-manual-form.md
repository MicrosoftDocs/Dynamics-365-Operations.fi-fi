---
title: Lähetysten konsolidointi manuaalisesti käyttämällä Konsolidoi lähetykset -sivua
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka myöhemmin konsolidoidaan Konsolidoi lähetykset -sivulla.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983012"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Lähetysten konsolidointi manuaalisesti käyttämällä Konsolidoi lähetykset -sivua

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka myöhemmin konsolidoidaan **Konsolidoi lähetykset** -sivulla.

## <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen

Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu. Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.

## <a name="create-the-sales-orders-for-this-scenario"></a>Myyntitilausten luonti skenaarioon

Aloita luomalla myyntitilauskokoelma, jota voit käyttää. Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön. Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.

Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.

### <a name="create-sales-orders-1-and-2"></a>Myyntitilausten 1 ja 2 luominen

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-007*
    - **Pooli:** *ShipCons*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

### <a name="create-sales-orders-3-and-4"></a>Myyntitilausten 3 ja 4 luominen

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-007*
    - **Pooli:** jätä tämä kenttä tyhjäksi.

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

## <a name="release-the-orders-to-the-warehouse"></a>Tilausten vapauttaminen varastoon

Vapauta jokainen tähän skenaarioon luotu myyntitilaus varastoon seuraavien ohjeiden avulla:

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset**.
1. Etsi ja valitse vapautettava myyntitilaus.
1. Vapauta valittu myyntitilaus valitsemalla toimintoruudun **Varasto**-välilehdessä **Toiminnot \> Vapauta varastoon**.
1. Toista tämä menettely jokaisen tähän skenaarioon luodun myyntitilauksen osalta.

## <a name="consolidate-shipments"></a>Konsolidoi lähetykset

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Etsi ja valitse lähetys, joka luotiin, kun myyntitilaus 1 vapautettiin varastoon. (Sen **Lähetyksen konsolidointikäytäntö** -kentän asetuksena on oltava *Tilauspooli*.)
1. Valitse toimintoruudun **Lähetykset**-välilehdessä **Lähetykset \> Konsolidoi lähetykset**.
1. Tarkista konsolidointiin ehdotetut lähetykset. Konsolidointiin pitäisi ehdottaa vain lähetystä, jossa on sama käytäntö.
1. Sulje **Lähetyksen konsolidointi** -sivu.
1. Etsi ja valitse lähetys, joka luotiin, kun myyntitilaus 3 vapautettiin varastoon. (Sen **Lähetyksen konsolidointikäytäntö** -kentän asetuksena on oltava *Oletus*.)
1. Valitse toimintoruudun **Lähetykset**-välilehdessä **Lähetykset \> Konsolidoi lähetykset**.
1. Tarkista, ettei konsolidointiin ole ehdotettu yhtään lähetystä.
1. Valitse **Näytä suodattimet**.
1. Poista **Tilausnumero**-suodatin **Suodattimet**-ruudussa ja valitse sitten **Käytä**.
1. Tarkista konsolidointiin ehdotetut lähetykset. Konsolidointiin pitäisi ehdottaa vain lähetystä, jossa on sama käytäntö.

## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidoinnin käytännöt](about-shipment-consolidation-policies.md)
- [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md)