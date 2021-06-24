---
title: Hankintaluettelojen yleiskatsaus
description: Tässä artikkelissa kuvataan, kuinka ostajat voivat määrittää ja ylläpitää tuotteiden hankintaluetteloita. Hankintaluettelot määrittävät nimikkeet ja palvelut, joita yrityksen työntekijät voivat tilata sisäiseen käyttöön.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, CatDisplayProductRelationAdd
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ac31634844ea5d82f795b2262d17a6be3a926c2
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190133"
---
# <a name="procurement-catalogs-overview"></a>Hankintaluettelojen yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka ostajat voivat määrittää ja ylläpitää tuotteiden hankintaluetteloita. Hankintaluettelot määrittävät nimikkeet ja palvelut, joita yrityksen työntekijät voivat tilata sisäiseen käyttöön.

Hankintahenkilöstö voi luoda ja ylläpitää luetteloita nimikkeistä ja palveluista, joita voi ostaa organisaation sisäiseen käyttöön. Kun luettelot on määritetty, yrityksen työntekijät voivat luoda ostoehdotuksia luetteloissa olevien kohteiden tilaamiseksi. Luetteloilla voidaan ottaa käyttöön ostokäytäntöjä niin, että työntekijät voivat tilata vain ostavalle yritykselle sallittuja nimikkeitä ja palveluja. Kun luot tuotteiden hankintaluettelon, ota huomioon seuraavat tehtävät:

-   Hankintaluokkahierarkia täytyy määrittää, ennen kuin voit luoda luettelon.
-   Määritä mitä tuotteita työntekijät voivat tilata. Voit näyttää tai piilottaa tietyt tuotteet luettelosolmussa tai näyttää tai piilottaa kaikki solmun tuotteet.
-   Määritä vaadittavien tuotteiden hankintaluetteloidenmäärä. Tuotteiden hankintaluettelon käyttöoikeus määritellään luettelon käytäntösäännössä, jonka konfiguroit yritykselle ja toimintayksikölle, johon työntekijä on liitetty.

Monet tekijät määrittävät, mitä tuotteita työntekijät voivat tilata ja mitä hankintaluokkia he voivat käyttää ostoehdotuksia tehdessään:

-   Ostokäytäntöön sisältyvä luokan käyttöoikeuskäytäntösääntö määrittää, mitä hankintaluokkia ostoehdotuksessa voi käyttää. Jos mitään sääntöä ei määritetä, kaikki hankintaluokat ovat käytettävissä.
-   Työntekijät voivat tilata tuotteen vain, jos se on organisaation aktiivisessa tuotteiden hankintaluettelossa, käyttöön otetussa solmussa ja näkyvissä. Tuotteen on oltava myös luokassa, jonka käyttöoikeus työntekijällä on luokan käyttöoikeutta koskevan käytäntösäännön mukaisesti.
-   Luettelon käytäntösääntö määrittää käytettävän luettelon. Jos luettelon käytäntösääntöä ei ole määritetty, ainoastaan luokan käyttöoikeussääntö määrittää tuotteet, joita työntekijä voi ehdotuksessaan tilata.

## <a name="prerequisites"></a>Edellytykset
Seuraavassa taulukossa kuvataan tehtävät, jotka on suoritettava ennen kuin ostaja voi luoda tuotteiden hankintaluettelon.

| Tehtävä                                                | Rooli               | Kuvaus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä hankintaluokkahierarkia.            | Ostopäällikkö | Hankintaluokkahierarkioilla luokitellaan nimikkeitä tai tapahtumia raportointia ja analysointia varten. Käyttämällä hankintaluokkahierarkiaa yritykset voivat strategisesti hallita luokat, tuotteet, toimittajat ja hankintojen tekijät keskitetysti. Koko organisaatiolle on määritetty yksi hankintaluokkahierarkia. Luettelo perustuu hankintaluokkahierarkiaan: hierarkian luokista tulee luettelon solmuja. Toimittajat ja tuotteet sisältyvät luetteloon. |
| Lisää toimittajat ja tuotteet hankintaluokkiin. | Ostopäällikkö | Kun hankintaluokkahierarkia luodaan organisaatioon, kukin hankintaluokka voidaan liittää tiettyihin toimittajiin ja tuotteisiin jne. Nämä liitokset kopioidaan luetteloon automaattisesti.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Luettelon määrittäminen
Kun edellytykset täyttyvät, voit määrittää luettelot. Voit luoda joko yhden luettelon koko organisaation käyttöön tai useita luetteloita organisaation eri osastojen käyttöön. Jos luot yhden luettelon koko organisaation käyttöön, luettelon käyttöoikeudet määräytyvät hankintojen käytäntösäännön mukaan.  

Luettelo määrittää, mitä tuotteita on käytettävissä ostoehdotusten luonnin yhteydessä, mutta lisärajoituksia voi ottaa käyttöön luokan käyttöoikeuksia koskevien käytäntösääntöjen avulla. Koska luettelon solmut ovat hankintaluokkia, ne voidaan estää luokan käyttöoikeuksia koskevalla käytäntösäännöllä. Tässä tapauksessa luokan tuotteet eivät ole työntekijöiden käytettävissä ostoehdotuksissa. Voit määrittää luokkien käyttöoikeuksien käytäntösääntöjä **Ostokäytännöt**-sivulla. Seuraavassa taulukossa kuvataan tehtävät, jotka on suoritettava luettelon määrittämiseksi.

| Tehtävä                                                   | Rooli             | Kuvaus                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Luo uusi luettelo.                                  | Hankintaostaja | Luettelo luodessasi voit määrittää nimi ja kuvaus luettelolle. Määritä myös, päivitetäänkö luettelo manuaalisesti vai automaattisesti, ja määritä luettelon omistaja.                                                                                                                                      |
| Määritä, ovatko tuotteet käytettävissä luettelossa. | Hankintaostaja | Koska tuotteet periytyvät hankintaluokista, ne näkyvät kaikki asianmukaisissa luettelosolmuissa. Voit määrittää, piilotetaanko vai näytetäänkö kaikki solmun tuotteet, kun luetteloa käytetään ostoehdotuksessa. Voit myös määrittää, piilotetaanko vai näytetäänkö yksittäisiä solmuun sisältyviä tuotteita. |
| Julkaise luettelo.                                   | Hankintaostaja | Ennen kuin työntekijät voivat käyttää luetteloa ostoehdotuksessa, sinun täytyy määrittää luettelolle käytäntösääntö, asettaa luettelon tilaksi **Aktiivinen** ja julkaista luettelo. Voit myös poistaa käytöstä luetteloita, joiden et halua enää olevan käytettävissä.                                              |

Päivitykset julkaistaan automaattisesti tai manuaalisesti riippuen asetuksesta, jonka valitset luettelolle **Luettelot**-sivun **Oletuspäivitystyyppi**-kentästä. Luetteloille on valittavana seuraavat oletuspäivitystyypit:

-   **Dynaaminen** – luettelo päivittyy automaattisesti aina, kun tiedot muuttuvat.
-   **Staattinen** – luettelot on päivitettävä manuaalisesti.
-   **Molemmat** – jos luettelo sisältää tuoteluokkia, joiden oletuspäivitystyyppi on **staattinen**, se on päivitettävä manuaalisesti luokkien päivityksen yhteydessä. Jos luettelo sisältää tuoteluokkia, joiden oletuspäivitystyyppi on **Dynaaminen**, se päivitetään automaattisesti, kun tiedot muuttuvat.


## <a name="additional-resources"></a>Lisäresurssit

[Määritä hankintaluokkahierarkia](tasks/set-up-procurement-category-hierarchy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]