---
title: Tuotetietoyksiköt
description: Tässä ohjeaiheessa on tietoja eri entiteeteistä, joita voidaan käyttää tuotetietojen tuontiin ja vientiin.
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 20d067effc6139084c5d89b5d4698e1adf2bbf9f
ms.sourcegitcommit: e9776095b92d19f214cd6765bbe9bf111432a699
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4427544"
---
# <a name="product-data-entities"></a>Tuotetietoyksiköt

[!include [banner](../includes/banner.md)]

Tuotetietojen tuontiin ja vientiin on käytettävä tietoyksiköitä. Seuraavassa taulukossa on tietoja tuotteeseen liittyvistä tietoyksiköistä ja kunkin tarkoituksen kuvaus.

| Kokonaisuus | Sovellusobjektipuun (AOT) nimi (tyyppi) | Muistiinpanot |
|--------|-------------------------------------------|-------|
| Tuotteet V2 | `EcoResProductV2Entity` | Tätä entiteettiä käytetään jaettujen tuotteiden-erillisten tuotteiden ja päätuotteiden tuontiin ja vientiin. Se mahdollistaa päivitykset. Se ei tue joukkoon perustuvia SQL-toimintoja. Se on otettu käyttöön Open Data Protocolissa (OData). |
| Vapautetut tuotteet V2 | `EcoResReleasedProductV2Entity` | Tätä entiteettiä käytetään julkaistujen tuotteiden-erillisten tuotteiden ja päätuotteiden tuontiin ja vientiin. Se mahdollistaa päivitykset. Se edellyttää, että jaettu tuote on jo luotu. Kun uusi vapautettu tuote tuodaan, jaetun tuotteen julkaisu tapahtuu. On myös erillisiä entiteettejä, joiden avulla voidaan tuoda ja viedä vapautettuja päätuotteita ja julkaista erillisiä variantteja. Tämä entiteetti ei tue joukkoon perustuvia SQL-toimintoja tai poistotoimintoja. Se on otettu käyttöön ODatassa. |
| Vapautetun tuotteen luominen V2 | `EcoResReleasedProductCreationV2Entity` | Tätä entiteettiä käytetään, kun tuodaan jaettuja tuotteita ja vapautettuja tuotteita yhdessä vaiheessa. Vaikka se tukee vientiä, tätä käyttöä ei suositella, koska entiteetin tarkoitus on tuotteen luonti. Se ei tue päivityksiä. Se tukee rajoitettua joukkoa kenttiä (kenttiä, jotka ovat käytettävissä tuotteen luonti -valintaikkunassa). Se ei tue joukkoon perustuvia SQL-toimintoja. Se ei altistu ODatan kautta. |
| Tuotevariantit | `EcoResProductVariantEntity` | Tätä entiteettiä käytetään jaettujen tuotevarianttien tuontiin ja vientiin. Se mahdollistaa päivitykset. Se edellyttää, että dimensioarvot on jo luotu. Integrointiavain on päätuote ja tuotedimensiot. Tämä yksikkö ei tue joukkoon perustuvia SQL-toimintoja. Se on otettu käyttöön ODatassa. Se tukee poistotoimintoja. Sitä ei voi laajentaa lisäämällä uusia tuotedimensioita. |
| Tuotevariantit tuotenumeron tunnuksen mukaan | `EcoResProductNumberIdentifiedProductVariantEntity` | Tätä entiteettiä käytetään jaettujen tuotevarianttien tuontiin ja vientiin. Se mahdollistaa päivitykset. Se edellyttää, että dimensioarvot on jo luotu. Integrointiavain on tuotenumero (kun taas **tuotevariantit** -entiteetin integrointiavain on päätuote ja tuotedimensiot). |
| Vapautetut tuotevariantit | `EcoResReleasedProductVariantEntity` | Tätä entiteettiä käytetään julkaistujen tuotevarianttien tuontiin ja vientiin. Se mahdollistaa päivitykset. Se edellyttää, että jaettu tuotevariantti on jo luotu. Kun uusi vapautettu tuotevariantti tuodaan, jaetun tuotevariantin julkaisu tapahtuu. Tämä yksikkö ei tue joukkoon perustuvia SQL-toimintoja. Se on otettu käyttöön ODatassa. Vaikka se tukee poistotoimintoja, kyseinen käyttö aiheuttaa tällä hetkellä tietojen vioittumisen, koska nykyisessä ympäristössä on virhe. Tätä entiteettiä ei voi laajentaa lisäämällä uusia tuotedimensioita. |
| Vapautetut tuotevariantit tuotenumeron tunnuksen mukaan | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | Tämä entiteetti muistuttaa **Julkaistut tuotevariantit** -entiteettiä, mutta integrointiavain on tuotenumero eikä päätuote ja tuotedimensiot. Sitä voi laajentaa lisäämällä uusia tuotedimensioita. |
| Myytävät vapautetut tuotteet | `EcoResSellableReleasedProductEntity` | Tätä entiteettiä käytetään vain myytävissä olevan tuotteen vientiin. Myytävissä olevat tuotteet ovat tuotteita, joille on määritetty tiedot myyntitilauksessa käyttämistä varten. Samoja sääntöjä käytetään, kun tuote tarkistetaan **Vapautetut tuoteet** -sivun **Vahvista**-toiminnon avulla. |
| Vapautetut erilliset tuotteet V2 | `EcoResDistinctProductV2Entity` | Tätä entiteettiä käytetään vain erillisten tuotteiden vientiin. Nämä erilliset tuotteet voivat olla tuotteita, tuotteiden alatyypin tuotteita ja kaikkia tuotevariantteja. |
| Vapautetut päätuotteet V2 | `EcoResProductMasterV2Entity` | Tätä entiteettiä käytetään päätuotteiden tuontiin ja vientiin. Se ei ole käytössä tietojen hallinnassa. |
| Nimike – viivakoodi | `EcoResProductBarcodeEntityV3` | Tätä entiteettiä käytetään vain tuotteiden vientiin ja viivakoodeihin. Tämä entiteetti ei salli muutosten seurantaa, päivityksiä tai poistoja. Viivakoodien muutosten seuranta, päivitykset tai poistot ovat mahdollisia käyttämällä **Nimike–viivakoodiliitos**-entiteettiä. |
| Nimike–viivakoodiliitos | `EcoResProductBarcodeAssociationEntity` | Tätä entiteettiä käytetään vain tuotteiden vientiin ja viivakoodeihin. Sen avulla muutosten seuranta, päivitykset ja poistot ovat mahdollisia. Nimikkeen käyttö edellyttää, että *Nimike – viivakoodin parannukset* -omaisuus on oltava otettuna käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Sen yksikköavain `AssociationID` luo liitoksen viivakoodin ja tuotteen välille. Tämän avaimen tuki lisätään täyttämällä `InventitemBarcodeAssociation`-taulukkoon aiemmin luodun nimikkeen viivakoodin tiedot, kun ominaisuus otetaan käyttöön. Taulukon täyttöön käytetään erätyötä. Jos viivakooditaulukossa on runsaasti tietueita, erätyön suorittaminen voi kestää kauan. Tämän vuoksi ominaisuuden käyttöönotto (ja siten myös erätyön suorittaminen) kannattaa suunnittele liiketoiminnan kannalta sopivimpaan ajankohtaan. |
| Tuotteen elinkaaren tilat | `EcoResProductLifecycleSateEntity` | Tätä entiteettiä käytetään tuomaan ja viemään tuotteen elinkaaren eri tilat, jotka voidaan liittää tuotteeseen. |

> [!NOTE]
> Voit käyttää **Julkaistut tuotteet V2** -tietoyksikköä tuodaksesi tuotteita järjestelmään vain, jos jaettu tuote on jo luotu. Jos haluat tuoda tuotteita järjestelmään, sinun on käytettävä **tuotteen luonti** -tietoyksikköä.
