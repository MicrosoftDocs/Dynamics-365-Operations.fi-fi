---
title: Tuotekokoelmamoduulit
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotekokoelmamoduulien yleiskatsaus.
author: v-chgri
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4bae9ca722c2b6e776abb0e1da9694edc8afadf8
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097100"
---
# <a name="product-collection-modules"></a>Tuotekokoelmamoduulit

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotekokoelmamoduulien yleiskatsaus.

Tuotteiden etsintätyökalu on ensisijainen työkalu, jonka avulla jälleenmyyjät voivat seurata asiakkaita sähköisen kaupankäynnin sivustossa. Tuotekokoelmamoduulien avulla jälleenmyyjät voivat luoda houkuttelevia ostoskokemuksia tarjoamalla intuitiivisen visuaalisen käyttöliittymän, jonka avulla voi nopeasti luoda tuotekokoelmia.

Tuotekokoelmamoduulit edustavat verkkosivuston fyysisiä tuotteita ja palveluita. Tuotekokoelmamoduuli on yleensä linkitetty tietosivuun, jossa asiakkaat voivat ostaa tuotteen tai palvelun sekä saada siitä lisätietoja. 

Tuotekokoelmien lähteet voivat olla seuraavien neljän tyyppisiä luetteloita:

- Toimitukselliset luettelot tuotteista, jotka on määritetty Dynamics 365 Commerceissa manuaalisesti tuotteen tai tuoteluetteloiden liittyviksi tuotteiksi.
- Algoritmiset luettelot, kuten uusien, myydyimpien tai suosittujen tuotteiden luettelot
- Suositusluettelot, jotka perustuvat koneoppimiseen
- Mukautusluettelot, jotka tukevat asiakkaan yksilöllisiä tuloksia. Asiakkaiden on kirjauduttava sähköiseen Commerce-sivustoon nähdäkseen henkilökohtaiset tulokset. Vieraskäyttäjät eivät näe yksilöllisiä tuloksia. Asiakkaat voivat poistaa personoinnin käytöstä [tilinhallinta-sivulla](account-management.md).

Seuraavassa kuvassa näkyvät erityyppiset tuotekokoelmat, joita käytetään sähköisen kaupankäynnin sivustossa.

![Esimerkki erityyppisistä tuotekokoelmista sähköisen kaupankäynnin sivustossa](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Käytä aina tuotekokoelmamoduuleita samankaltaisten tuoteryhmien kanssa.

## <a name="product-collection-modules-and-types"></a>Tuotekokoelmamoduulit ja -tyypit

Seuraavassa taulukossa on tuotekokoelmamoduulien eri tyypit Dynamics 365 Commerce -sovelluksessa.

| Tuotekokoelmamoduuli  | Laji | Kuvaus |
|----------------------------|------|-------------|
| Luokka                   | Luokka | Tässä moduulissa on luettelo luokan tuotteista, jotka on määritetty kanavan vähittäismyyjän luoman siirtymisluokkahierarkian mukaan. |
| Liittyvät tuotteet           | Toimituksellinen | Tämä moduuli näyttää luettelon tuotteista, jotka myynninedistämispäällikkö on määrittänyt Commerce-sovelluksessa liittyviksi tuotteiksi tekijän valitsemaa suhdetyyppiä varten. |
| Hakutulokset             | Hakukysely | Tämäntyyppinen tuotekokoelmamoduuli näyttää luettelon tuotteista, jotka parhaiten vastaavat asiakkaan syöttämiä hakukyselyitä. |
| Kuratoidut tuoteluettelot      | Toimituksellinen | Tämä moduuli näyttää mukautetut luettelot, jonka myyjät ja muokkaajat ovat luoneet Commerce-sovelluksessa. |
| Uusi                        | Algoritmi | Tämä moduuli näyttää luettelon uusimmista tuotteista, jotka on lajiteltu kanaviin ja luetteloihin. Tämä luettelo voi näyttää mukautettuja tuloksia kirjautuneesta käyttäjästä, jos sivuston tekijä valitsee kyseisen vaihtoehdon. |
| Myydyin               | Algoritmi | Tämä moduuli näyttää luettelon tuotteista, jotka on järjestetty suurimman myyntimäärän mukaan. Tämä luettelo voi näyttää mukautettuja tuloksia kirjautuneesta käyttäjästä, jos sivuston tekijä valitsee kyseisen vaihtoehdon. |
| Suosittu                   | Algoritmi | Tämä moduuli näyttää luettelon parhaiten menestyvistä tuotteista annettuna ajanjaksona. Tämä luettelo voi näyttää mukautettuja tuloksia kirjautuneesta käyttäjästä, jos sivuston tekijä valitsee kyseisen vaihtoehdon. |
| Ostetaan usein yhdessä | Tekoäly/koneoppiminen | Tämä moduuli käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan liittyviä nimikkeitä, jotka ostetaan usein yhdessä tietyn tuotteen kanssa. Tämä luettelo voi näyttää mukautettuja tuloksia kirjautuneesta käyttäjästä, jos sivuston tekijä valitsee kyseisen vaihtoehdon. |
| Ihmiset pitävät myös seuraavista           | Tekoäly/koneoppiminen | Tämä moduuli käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan nimikkeitä, jotka liittyvät tiettyyn tuotteeseen. Tämä luettelo voi näyttää mukautettuja tuloksia kirjautuneesta käyttäjästä, jos sivuston tekijä valitsee kyseisen vaihtoehdon. |
| Valinnat sinulle              | Tekoäly/koneoppiminen | Tämä moduuli käyttää koneoppimista kirjautuneen käyttäjän ostomallien analysoimiseen ja antaa mukautettuja suosituksia, jotka perustuvat näihin ostotottumuksiin. Vieraskäyttäjän luettelo on kutistettu. |

## <a name="supported-modules"></a>Tuetut moduulit 

Tuotekokoelmamoduuli tukee [pikanäkymämoduulia](quick-view-module.md), jonka avulla käyttäjät voivat tarkastella tuotetietoja ja lisätä nimikkeitä ostoskoriin tuotekokoelmasivulta.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Tuotekokoelmamoduulin lisääminen luokkasivulle

Lisää tuotekokoelmamoduuli luokkasivulle seuraavasti.

1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa sama malli, jota käytettiin oletusluokkasivulla. Kirjoita **Sivun nimi** -kohtaan sopiva nimi ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Alialatunniste**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Tuotekokoelma**-moduuli ja valitse sitten **OK**.  
1. Valitse tuotekokoelmamoduulin ominaisuusruudussa **Lisää tuoteluetteloon**.
1. Valitse **Valitse tuoteluettelon määritys** -valintaikkunassa luettelon tyyppi, luettelolähde ja anna nimikkeiden määrä. Määritä muut vaihtoehdot, joita voi käyttää luettelotyypissä. Lisätietoja tämän tyyppisistä luettelotyypeistä on seuraavassa taulukossa. 
1. Valitse **OK**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

Seuraavassa taulukossa on luettelotyypit, jotka ovat valittavissa **Valitse tuoteluettelon määritys** -valintaikkunassa.

| Laji                       | Kuvaus | Käyttö | Sivun konteksti | Tietty konteksti | Mukauttaminen |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Tuotteet luokittain       | Luettelo tuotteista, jotka kuuluvat tiettyyn luokkaan. Tämän luokan määrittää joko sivukonteksti tai tekijän määrittämä konteksti. | Tämäntyyppistä luetteloa voidaan käyttää millä tahansa sivulla (esimerkiksi kotisivu, luokkasivu, markkinointisivu tai tuotetiedot-sivu \[PDP\]) tietyn tuoteluokan edistämiseksi. | Luokka sivuympäristöstä, jos sellainen on käytettävissä (esimerkiksi luokkasivu) | Tekijä voi tarjota tietyn luokan luettelon kontekstissa. | Ei käytettävissä |
| Liittyvät tuotteet           | Luettelo tuotteista, jotka myyntipäällikkö on määrittänyt liittyviksi tuotteiksi suhdetyyppiä varten Commerce-sovelluksessa. | Tämäntyyppistä luetteloa käytetään ensisijaisesti PDP:issä, mutta sitä voidaan käyttää millä tahansa sivulla, jos päätuote on annettu. | Tuote sivulta, suhdetyyppi (pakollinen) | Tuote voidaan valita valitsimessa, ja suhdetyyppiä käytetään. | Ei käytettävissä |
| Kuraattori                    | Mukautettu luettelo, jonka myyjät ja muokkaajat ovat luoneet Commerce-sovelluksessa. | Täydennetty luokkasivu, aloitussivu, kassa- ja ostoskorisivut sekä tuotesivut | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä |
| Algoritmi                | <ul><li>**Uusi** – Luettelo uusimmista tuotteista, jotka on lajiteltu kanaviin ja luetteloihin.</li><li>**Myydyin** – Luettelo tuotteista suurimman myyntimäärän mukaan.</li><li>**Trendit** – Luettelo parhaiten menestyvistä tuotteista annettuna ajanjaksona.</li></ul> | Aloitussivu, täydennetty luokkasivu ja kassa- ja ostoskorisivut | Luokka sivuympäristöstä (esimerkiksi luokkasivu) | Sivuston tekijän määrittämä luokka | Tuettu |
| Ostetaan usein yhdessä | Luettelo, joka käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan liittyviä nimikkeitä, jotka ostetaan usein yhdessä tietyn tuotteen kanssa. | Tämäntyyppinen luettelo koskee vain ostoskori-sivua. | Ostoskori | Ei käytettävissä | Tuettu |
| Ihmiset pitävät myös seuraavista           | Luettelo, joka käyttää koneoppimista analysoidessaan kuluttajien ostomalleja ja suositellessaan nimikkeitä, jotka liittyvät tiettyyn tuotteeseen. | Tämän tyyppistä luetteloa käytetään PDP:issä näyttämään tuotteita, joita muut asiakkaat ovat ostaneet. | Tuotteen konteksti sivulta | Sivuston tekijän tarjoama tuote | Tuettu |
| Valinnat sinulle              | Luettelo, joka määrittää asiakkaiden mieltymykset koneoppimisen avulla. | Tämäntyyppistä luetteloa voi käyttää millä tahansa sivulla. | Ei käytettävissä| Ei käytettävissä | Tuettu | 

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Karusellimoduuli](add-carousel.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Pikanäkymämoduuli](quick-view-module.md)
