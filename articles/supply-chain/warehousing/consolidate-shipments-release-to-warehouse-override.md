---
title: Lähetysten konsolidointi, kun lähetyksen konsolidointikäytäntö ohitetaan
description: Tässä artikkelissa käsitellään skenaariota, jossa vähintään yksi myyntirivi on vapautettava varastoon manuaalisesti Vapauta varastoon -sivulla ja järjestelmän määrittämä lähetyksen konsolidointikäytäntö on korvattava ennen vapautusta.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 680941adeba1fc1cd54a02fb366d3d5903938d77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878697"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Lähetysten konsolidointi, kun lähetyksen konsolidointikäytäntö ohitetaan

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään skenaariota, jossa vähintään yksi myyntirivi on vapautettava varastoon manuaalisesti **Vapauta varastoon** -sivulla ja järjestelmän määrittämä lähetyksen konsolidointikäytäntö on korvattava ennen vapautusta. Lähetyksen konsolidointikäytäntö on ehkä korvattava, jos esimerkiksi tilaus, jota ei yleensä konsolidoida avoimien lähetysten kanssa, on konsolidoitava avoimien lähetysten kanssa.

Tämän skenaarion aikana luodaan myyntitilausjoukko ja korvataan sitten lähetyksen oletuskonsolidointikäytäntö ennen tilausten vapauttamista varastoon.

## <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Artikkelin skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen

Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu. Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.

## <a name="create-the-sales-orders-for-this-scenario"></a>Myyntitilausten luonti skenaarioon

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo siten kolme samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-002*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Myyntitilausten vapauttaminen Vapauta varastoon -sivulta

Korvaa lähetyksen konsolidointikäytäntö varastoon vapautuksen aikana seuraavasti:

1. Valitse **Varastonhallinta \> Vapauta varastoon \> Vapauta varastoon**.
1. Valitse yläruudussa ensimmäinen tähän skenaarioon luotu myyntitilaus.
1. Lisää rivi varastoon vapautukseen valitsemalla **Lisää**. Huomaa, että *oletusarvoinen* lähetyksen konsolidointikäytäntöä käytetään alaruudussa.
1. Valitse alaruudussa **Valitse uusi lähetyksen konsolidointikäytäntö**.
1. Valitse käytäntö, joka sallii konsolidoinnin muiden samaa käytäntöä käyttävien avoimien lähetysten konsolidoinnin. Valitse esimerkiksi *CustomerOrderNo*-käytäntö.
1. Valitse **Vapauta varastoon**.
1. Valitse toinen ja kolmas tähän skenaarioon luotu myyntitilaus.
1. Lisää rivit varastoon vapautukseen valitsemalla **Lisää**. Huomaa, että *oletusarvoista* käytäntöä käytetään alaruudussa.
1. Valitse ensin toinen rivi ja valitse sitten **Valitse uusi lähetyksen konsolidointikäytäntö** -kentässä *CustomerOrderNo*-käytäntö.
1. Valitse kummallakin rivillä **Vapauta varastoon**.

## <a name="verify-the-shipments"></a>Lähetysten tarkistaminen

Luotuja lähetyksiä on oltava kaksi:

- Ensimmäisessä lähetyksessä on kaksi riviä, ja se luotiin käyttämällä lähetysten *CustomerOrderNo*-konsolidointikäytäntöä.
- Toisessa lähetyksessä on yksi rivi, ja se luotiin käyttämällä *oletusarvoista* lähetysten konsolidointikäytäntöä.

Tarkista luodut lähetykset seuraavien ohjeiden avulla:

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Etsi ja valitse tarvittava lähetys.
1. Tarkista **Lähetyksen konsolidointikäytäntö** -kentässä konsolidointikäytäntö, jota käytettiin lähetystä luotaessa.

## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidoinnin käytännöt](about-shipment-consolidation-policies.md)
- [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]