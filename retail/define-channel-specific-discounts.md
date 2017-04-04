---
title: "Kanavakohtaisten alennusten määrittäminen"
description: "Vähittäismyyjät määrittävät usein erilaisia alennuksia eri kanaville. Tässä aiheessa tarkastellaan käsitteitä, joita tarvitaan tietyn kanavan alennuksen luomisessa."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Kanavakohtaisten alennusten määrittäminen

Vähittäismyyjät määrittävät usein erilaisia alennuksia eri kanaville. Tässä aiheessa tarkastellaan käsitteitä, joita tarvitaan tietyn kanavan alennuksen luomisessa. 

<a name="channel-specific-discounts"></a>Kanavakohtaiset alennukset
--------------------------

Jälleenmyyjät tarjoavat usein alennuksia eri kanaviin. Tämä ei ehkä tehdä osoite paikallisten markkinoiden olosuhteisiin tai käsitellä kilpailevien vähittäismyyjien.

Jälleenmyynti- ja Microsoft Dynamics-365 työvaiheiden kaupankäynnin määrittää hintaryhmät avulla kanavaan liittyviä alennuksia. Hintaryhmät voivat määrittää yhteen seuraavista yksiköistä tai useisiin yksikköihin: kanavat. luettelot, liitokset ja kanta-asiakasohjelmat. Tässä artikkelissa käsitellään kanavia, mutta samat käsitteet koskevat myös luettelo-, liitos- ja kanta-asiakasalennuksia.

## <a name="price-groups"></a>Hintaryhmät
\[selosteen tunnus = "liitteen\_256084" Tasaa = "alignnone" width = "640"\][![hinta ryhmät](./media/price-groups-1024x608.png)](./media/price-groups.png) for Retail hinta linkkien ryhmittely\[/tekstitys\]

Edellä kaavio havainnollistaa ja kohteista, joita tapahtuman (kanava, Kuvasto, työsuhde, asiakas, kanta-asiakaskortti), joka voidaan määrittää eri alennustyypeille välistä suhdetta. Kaikki tapahtumat tapahtuvat kanava, joten kanava on varmasti olla läsnä tapahtumassa. Muut yksiköt ovat valinnaisia. Jokaisella päätietosivulla on linkki liittyvään hintaryhmäsivuun, jossa voit tarkastella hintaryhmiä ja lisätä niitä tarvittaessa. Hintaryhmän käytetään liittämään neljänlaisia kohteiden alennukset ja hintojen muutoksia kauppasopimuksia. Suosittelemme, että aiot strategiaa, kuinka nimeät hintaryhmät pitämään ne järjestyksessä. Yksi vaihtoehto olisi erottaa eri käytetään kirjain tai numero etuliite tai jälkiliite. Esimerkiksi 1-xxxxx kanavan hintaryhmät ja luettelon hintaryhmissä 2-xxxxx. Kullakin vähittäismyyntiyksiköllä, joihin voidaan liittää alennuksia, on neljä kyselysivua.

-   **Vähittäismyyntikanavan hintaryhmät ** – tällä sivulla on luettelo kanavista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.
-   **Luettelon hintaryhmät ** – tällä sivulla on luettelo luetteloista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.
-   **Kanta-asiakasohjelman hintaryhmät ** – tällä sivulla on luettelo kanta-asiakasohjelmista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.
-   **Liitoksen hintaryhmät ** – tällä sivulla on luettelo liitoksista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.

## <a name="example-channel-discount-set-up"></a>Kanavan alennusasetusten esimerkki
Seuraavassa esimerkissä käsitellään tehtäviä, jotka liittyvät kanava-alennuksen määrittämiseen.

1.  Tässä esimerkissä on **Houston**-niminen kanava ja luot uuden alennuksen, jonka nimi on **Takaisin kouluun**.
2.  Koska hinnoittelu- ja alennusstrategia mahdollistaa kanava-alennukset, kanavaa luotaessa luodaan aina myös kanavakohtainen hintaryhmä.
3.  Sinulla hintaryhmä **Houston-PG**, joka on määritetty **Houston**-kanavaan.
4.  Kun olet luonut uuden **Takaisin kouluun** -alennukset, valitse **Hintaryhmät** **Alennus**-sivun yläosassa. **Alennushintaryhmät**-sivu avautuu. Valitse seuraavaksi ensin **Uusi** ja sitten **Houston-PG**-hintaryhmä.
5.  Voit nyt ottaa alennuksen käyttöön ja siirtää sen kanavaan.

 

<a name="see-also"></a>Lisätietoja
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


