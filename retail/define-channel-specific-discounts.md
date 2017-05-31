---
title: "Kanavakohtaisten alennusten määrittäminen"
description: "Vähittäismyyjät määrittävät usein erilaisia alennuksia eri kanaville. Tässä aiheessa tarkastellaan käsitteitä, joita tarvitaan tietyn kanavan alennuksen luomisessa."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 750f61198550a248d70fd531c3cb2ff86ca37f50
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="define-channel-specific-discounts"></a>Kanavakohtaisten alennusten määrittäminen

[!include[banner](includes/banner.md)]


Vähittäismyyjät määrittävät usein erilaisia alennuksia eri kanaville. Tässä aiheessa tarkastellaan käsitteitä, joita tarvitaan tietyn kanavan alennuksen luomisessa. 

<a name="channel-specific-discounts"></a>Kanavakohtaiset alennukset
--------------------------

Vähittäismyyjät tarjoavat usein erilaisia alennuksia eri kanaville. Syynä voi olla paikallisten markkinaolosuhteiden huomioon ottaminen tai kilpailu muiden vähittäismyyjien kanssa.

Microsoft Dynamics 365 for Operationsin Vähittäismyynti ja kauppa määrittää kanavakohtaiset alennukset hintaryhmien avulla. Hintaryhmät voivat määrittää yhteen seuraavista yksiköistä tai useisiin yksikköihin: kanavat. luettelot, liitokset ja kanta-asiakasohjelmat. Tässä artikkelissa käsitellään kanavia, mutta samat käsitteet koskevat myös luettelo-, liitos- ja kanta-asiakasalennuksia.

## <a name="price-groups"></a>Hintaryhmät

[![Hintaryhmät](./media/price-groups-1024x608.png)](./media/price-groups.png)

Edellä olevassa kaaviossa on kuva tapahtumassa mahdollisesti olevien yksikköjen suhteesta (kanava, luettelo, liitos, asiakas, kanta-asiakaskortti) ja erilaisista määritettävistä alennustyypeistä. Kaikki tapahtumat tapahtuvat kanavassa, joten kanava on varmasti mukana tapahtumassa. Muut yksiköt ovat valinnaisia. Jokaisella päätietosivulla on linkki liittyvään hintaryhmäsivuun, jossa voit tarkastella hintaryhmiä ja lisätä niitä tarvittaessa. Hintaryhmän avulla neljä eri tyyppistä yksikköä liitetään alennuksiin, hinnanoikaisuihin ja kauppasopimuksiin. On suositeltavaa, että suunnittelet hintaryhmille nimeämisstrategian, jotta ne pysyvät järjestyksessä. Tyypit voi erottaa toisistaan käyttämällä etu- tai jälkiliitteenä kirjainta tai numeroa. Esimerkiksi 1-xxxxx voi viitata kanavan hintaryhmään ja 2-xxxxx luettelon hintaryhmään. Kullakin vähittäismyyntiyksiköllä, joihin voidaan liittää alennuksia, on neljä kyselysivua.

-   **Vähittäismyyntikanavan hintaryhmät** – tällä sivulla on luettelo kanavista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.
-   **Luettelon hintaryhmät** – tällä sivulla on luettelo luetteloista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.
-   **Kanta-asiakasohjelman hintaryhmät** – tällä sivulla on luettelo kanta-asiakasohjelmista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.
-   **Liitoksen hintaryhmät** – tällä sivulla on luettelo liitoksista ja alennuksista, jotka on liitetty yhteen kullekin hintaryhmälle.

## <a name="example-channel-discount-set-up"></a>Kanavan alennusasetusten esimerkki
Seuraavassa esimerkissä käsitellään tehtäviä, jotka liittyvät kanava-alennuksen määrittämiseen.

1.  Tässä esimerkissä on **Houston**-niminen kanava ja luot uuden alennuksen, jonka nimi on **Takaisin kouluun**.
2.  Koska hinnoittelu- ja alennusstrategia mahdollistaa kanava-alennukset, kanavaa luotaessa luodaan aina myös kanavakohtainen hintaryhmä.
3.  Sinulla hintaryhmä **Houston-PG**, joka on määritetty **Houston**-kanavaan.
4.  Kun olet luonut uuden **Takaisin kouluun** -alennukset, valitse **Hintaryhmät** **Alennus**-sivun yläosassa. **Alennushintaryhmät**-sivu avautuu. Valitse seuraavaksi ensin **Uusi** ja sitten **Houston-PG**-hintaryhmä.
5.  Voit nyt ottaa alennuksen käyttöön ja siirtää sen kanavaan.

 

<a name="see-also"></a>Lisätietoja
--------

[Hinnanoikaisut ja alennukset](price-adjustments-discounts.md)




