---
title: Tuotekokoelmamoduulit
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotekokoelmamoduulien yleiskatsaus.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785464"
---
# <a name="product-collection-modules"></a>Tuotekokoelmamoduulit  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotekokoelmamoduulien yleiskatsaus.

## <a name="overview"></a>Yleiskatsaus

Tuotteiden etsintätyökalu on ensisijainen työkalu, jonka avulla jälleenmyyjät voivat seurata asiakkaita sähköisen kaupankäynnin sivustossa. Tuotekokoelmamoduulien avulla jälleenmyyjät voivat luoda houkuttelevia ostoskokemuksia tarjoamalla intuitiivisen visuaalisen käyttöliittymän, jonka avulla voi nopeasti luoda tuotekokoelmia.

Tuotekokoelmamoduulit edustavat verkkosivuston fyysisiä tuotteita ja palveluita. Tuotekokoelmamoduuli on yleensä linkitetty tietosivuun, jossa asiakkaat voivat ostaa tuotteen tai palvelun sekä saada siitä lisätietoja. 

Tuotekokoelmien lähteet voivat olla kolmen tyyppisiä luetteloita:

- Toimitukselliset luettelot tuotteista, jotka on määritetty Dynamics 365 Retailissa manuaalisesti tuotteen tai tuoteluetteloiden liittyviksi tuotteiksi.
- Algoritmiset luettelot, kuten uusien, myydyimpien tai suosittujen tuotteiden luettelot
- Suositusluettelot, jotka perustuvat koneoppimiseen

Seuraavassa kuvassa näkyvät erityyppiset tuotekokoelmat, joita käytetään sähköisen kaupankäynnin sivustossa.

![Esimerkki erityyppisistä tuotekokoelmista sähköisen kaupankäynnin sivustossa](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Käytä aina tuotekokoelmamoduuleita samankaltaisten tai saman teeman omaavien tuoteryhmien kanssa.

## <a name="product-collection-modules-and-types"></a>Tuotekokoelmamoduulit ja -tyypit

Seuraavassa taulukossa on tuotekokoelmamoduulien eri tyypit Dynamics 365 Commerce -sovelluksessa.

| Tuotekokoelmamoduuli  | Laji | Kuvaus |
|----------------------------|------|-------------|
| Luokan selaaminen            | Toimituksellinen | Tämäntyyppinen tuotekokoelmamoduuli käyttää siirtymisluokkahierarkiaa, jonka jälleenmyyjä on luonut vähittäismyyntikanavaa varten. Sen avulla näytetään selaustyönkulku tuotteille, joita tarjotaan tietyssä sivustoluokassa. |
| Hakutulokset             | Hakukysely | Tämäntyyppinen tuotekokoelmamoduuli näyttää luettelon tuotteista, jotka parhaiten vastaavat asiakkaan syöttämiä hakukyselyitä. |
| Liittyvät tuotteet           | Toimituksellinen | Tämäntyyppinen tuotekokoelmamoduuli näyttää luettelon tuotteista, jotka myynninedistämispäällikkö on määrittänyt Retail-sovelluksessa liittyviksi tuotteiksi tekijän valitsemaa suhdetyyppiä varten. |
| Kuratoidut tuoteluettelot      | Toimituksellinen | Tämäntyyppisessä tuotekokoelmamoduulissa näkyvät mukautetut luettelot, jotka kauppiaat ja muokkaajat ovat luoneet Retail-sovelluksessa. |
| Uusi                        | Algoritmi | Tämäntyyppinen tuotekokoelmamoduuli näyttää luettelon uusimmista tuotteista, jotka on lajiteltu kanaviin ja luetteloihin. |
| Myydyin               | Algoritmi | Tämäntyyppinen tuotekokoelmamoduuli näyttää luettelon tuotteista, jotka on listattu parhaiten myyvien tuotteiden mukaan. |
| Suosittu                   | Algoritmi | Tämäntyyppinen tuotekokoelmamoduuli näyttää luettelon annetun ajanjakson parhaiten menestyvistä tuotteista. |
| Ostetaan usein yhdessä | Tekoäly/koneoppiminen | Tämäntyyppinen tuotekokoelmamoduuli käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan liittyviä nimikkeitä, jotka ostetaan usein yhdessä tietyn tuotteen kanssa. |
| Ihmiset pitävät myös seuraavista           | Tekoäly/koneoppiminen | Tämäntyyppinen tuotekokoelmamoduuli käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan nimikkeitä, jotka liittyvät annettuun tuotteeseen. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Tuotekokoelmamoduulin lisääminen luokkasivulle

Lisää tuotekokoelmamoduuli luokkasivulle seuraavasti.

1. Siirry Dynamics 365 Commercessa sivustoon ja luo sivu, joka käyttää samaa mallia kuin oletusluokkasivu.
1. Valitse sivun jäsennyksessä **Alialatunniste**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti** ja valitse sitten **OK**.
1. Valitse säilömoduulissa kolmen pisteen painike ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tuotekokoelma** ja valitse sitten **OK**.
1. Määritä asetukset valitsemalla soveltuva tietolähde ja syötteet tuotekokoelmalle.
1. Valitse tuotekokoelmamoduulin ominaisuusruudussa **Lisää tuoteluetteloon**.
1. Valitse **Valitse tuoteluettelon määritys** -valintaikkunassa luettelon tyyppi. Syötä nimikkeiden määrä ja valitse muut vaihtoehdot, jotka luettelotyypille ovat käytettävissä. Lisätietoja tämän tyyppisistä luettelotyypeistä on seuraavassa taulukossa. 
1. Valitse **OK**.
1. Tallenna sivu ja kirjaa se sisään.

Seuraavassa taulukossa on luettelotyypit, jotka ovat valittavissa **Valitse tuoteluettelon määritys** -valintaikkunassa.
   
| Laji                       | Kuvaus | Yleinen käytäntö | Konteksti, joka voidaan johtaa sivukontekstista | Konteksti, jonka avulla tekijä voi ohittaa sivukontekstin |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Tuotteet luokittain       | Luettelo tuotteista, jotka kuuluvat tiettyyn luokkaan. Tämän luokan määrittää joko sivukonteksti tai tekijän määrittämä konteksti. | Täydennetty luokkasivu, aloitussivu, kassa- ja ostoskorisivut sekä tuotesivut | Luokka | Tekijän määrittämä luokka |
| Liittyvät tuotteet           | Luettelo tuotteista, jotka myyntipäällikkö on määrittänyt liittyviksi tuotteiksi Retail-sovelluksessa suhdetyyppiä varten. | Tuotesivut, kassa- ja ostoskorisivut, toivomuslistasivu ja asiakkaan tilin sivu | Tuote, suhdetyyppi (pakollinen)  | Tuote, suhdetyyppi |
| Kuraattori                    | Mukautettu luettelo, jonka myyjät ja muokkaajat ovat luoneet Retail-sovelluksessa. | Täydennetty luokkasivu, aloitussivu, kassa- ja ostoskorisivut sekä tuotesivut | Ei käytettävissä | Luettelon valitsin |
| Algoritmi                | <ul><li>**Uusi** – Luettelo uusimmista tuotteista, jotka on lajiteltu kanaviin ja luetteloihin.</li><li>**Myydyin** – Luettelo tuotteista suurimman myyntimäärän mukaan.</li><li>**Trendit** – Luettelo parhaiten menestyvistä tuotteista annettuna ajanjaksona.</li></ul> | Aloitussivu, täydennetty luokkasivu ja kassa- ja ostoskorisivut | Luokka | Tekijän määrittämä luokka |
| Ostetaan usein yhdessä | Luettelo, joka käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan liittyviä nimikkeitä, jotka ostetaan usein yhdessä tietyn tuotteen kanssa. | Tuotesivut ja kassa- ja ostoskorisivut | Tuote, ostoskori | Sisällytä ostoskori |
| Ihmiset pitävät myös seuraavista           | Luettelo, joka käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan nimikkeitä, jotka liittyvät tiettyyn tuotteeseen. | Tuotesivut ja kassa- ja ostoskorisivut | Tuote, ostoskori | Ei käytettävissä |

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Karusellimoduuli](add-carousel.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Sisällönsijoittelumoduuli](add-content-placement-modules.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

