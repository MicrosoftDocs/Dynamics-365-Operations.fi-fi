---
title: Resurssin ominaisuudet
description: "Tässä artikkelissa on tietoja resurssin ominaisuuksista. Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Artikkelissa kerrotaan miten ominaisuuksia ja siihen liittyviä käsitteitä, kuten pätevyystasoa ja prioriteettia, käytetään valittaessa sopivia resursseja tehtävään."
author: sorenva
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 533faf78e4cc9a091d64f7c6a0f82d14158710c8
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="resource-capabilities"></a>Resurssin ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja resurssin ominaisuuksista. Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Artikkelissa kerrotaan miten ominaisuuksia ja siihen liittyviä käsitteitä, kuten pätevyystasoa ja prioriteettia, käytetään valittaessa sopivia resursseja tehtävään.

Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Operatiivisella resurssilla voi olla useampi kuin yksi siihen liitetty ominaisuus, ja ominaisuus voidaan määrittää useammalle kuin yhdelle resurssille. Voit määrittää ominaisuuksia resursseille tilapäisesti asettamalla ominaisuusmääritykselle alkamis- ja vanhentumispäivät. Kun resurssin ominaisuuden voimassaolo on päättynyt, kyseistä resurssia ei voida kohdistaa projektille tai tuotannolle, joka vaatii kyseisen ominaisuuden. Ominaisuus, jonka voimassaolo on päättynyt, voidaan uusia. Voit poistaa ominaisuuksia sillä edellytyksellä, että ne eivät ole reitityssuhteella tai osana aktiivisen tuotantotilauksen tuotantoreititystä. Yleisesti ottaen, ole varovainen poistaessasi ominaisuuksia. Harkitse sen sijaan kyseisen ominaisuuden sisältävien resurssien voimassaolon päättymispäivän muuttamista. Ominaisuuksia voidaan määrittää kaiken tyyppisille resursseille: työkalu, toimittaja, kone, toimipaikka, tai henkilöresurssi.

## <a name="level"></a>Tasaa
Useilla resursseilla on usein sama toiminnallinen ominaisuus mutta eri pätevyystasoilla (esimerkiksi vahvuus, käsittelynopeus tai tarkkuus). Näin ollen, määrittäessäsi resurssille ominaisuuden, voit määrittä **Taso**-arvon. Tasoarvo on yksinkertainen numeerinen arvo. Jos määrität, että ominaisuus on tuotantoreitityksen resurssivaatimus, voit määrittää myös **Vaadittu vähimmäistaso** -arvon kyseiselle ominaisuudelle. Ajoitusmoduuli valitsee sitten vain ne resurssit, joilla on tarvittavat ominaisuudet tasolla, joka vastaa resurssivaatimuksessa määriteltyä vähimmäistasoa tai on sitä suurempi.

## <a name="priority"></a>Prioriteetti
Operatiivisille resursseille, joilla on samat ominaisuudet, voidaan määrittää prioriteetti. Tällöin, jos useilla resursseilla on ominaisuuksia, jotka täyttävät ajoitusvaatimukset vaaditulla tasolla ja niillä on vapaata kapasiteettia, ajoitusmoduuli voi tehdä valinnan näiden resurssien välillä. Jos **Prioriteetti** on valittu **Ensisijaisen resurssin valinta** -kentässä **Ajoitusparametrit** -sivulla, resurssi, jolla on korkein prioriteetti (alhaisin numeerinen arvo **Prioriteetti**-kentässä) valitaan ajoitukseen ensin.

## <a name="resource-requirements"></a>Resurssivaatimukset
Määrittäessäsi resurssivaatimukset tuotantoreititykselle, voit määrittää yhden tai useampia ominaisuuksia vaatimuksiksi. Tuotantosuunnitelmassa ominaisuudet, jotka on määritetty reitityksen työvaiheen resurssivaatimuksissa, kohdistetaan resursseille määritettyihin ominaisuuksiin. Resurssit, joiden ominaisuudet vastaavat resurssivaatimukset, valitaan. Jos useilla resursseilla on usein sama toiminnallinen ominaisuus mutta eri pätevyydet (kuten vahvuus, käsittelynopeus tai tarkkuus), voit joko määrittää useita ominaisuuksia tai käyttää ominaisuuden tasoa resurssin ominaisuuden määrittämiseksi. Tässä on esimerkki:

-   Reitityksessä porausprosessin aika on asetettu 10 yksikköön tunnissa, mutta itse vaatimus on määritetty arvolla Poraus.
-   Sinulla on kaksi porauskonetta, M1 ja M2.
-   Poraus-ominaisuus on määritetty molemmille resursseille, M1-koneelle ja M2-koneelle.
-   M1-kone pystyy poraamaan kaksi yksikköä tunnissa ja M2-kone pystyy poraamaan 11 yksikköä tunnissa.

Tässä esimerkissä ajoitusmoduuli voi valita molemmat koneet, koska molemmat täyttävät perusominaisuusvaatimuksen (Poraus). M1-kone pystyy kuitenkin poraamaan vain kaksi yksikköä tunnissa. Koska tämä määrä on paljon vähemmän kuin reitille määritetty 10 yksikköä tunnissa, M1-kone aiheuttaa tuotanto-ongelmia, jos se valitaan. On kaksi tapaa ratkaista tämä ongelma ja varmistaa, että M2-kone valitaan M1-koneen sijaan:

-   Luo kaksi erillistä ominaisuutta: Hidas poraus ja Nopea poraus. Määritä Hidas poraus poraukseksi, jonka prosessiaika on yhdestä yhdeksään yksikköä tunnissa. Määritä Nopea poraus poraukseksi, jonka porausprosessiaika on 10 - 19 yksikköä tunnissa. Määritä sitten M1-koneelle Hidas poraus -ominaisuus ja M2-koneelle Nopea poraus -ominaisuus. Muuta lopuksi resurssin ominaisuusvaatimus reitillä arvoksi Nopea poraus. Ajoitusmoduuli valitsee sitten oikean koneen (M2).
-   Käytä ominaisuuden tasoa määrittämään Poraus-ominaisuus, joka määritetään porauskoneille. Määritä, että M1-koneella on Poraus-ominaisuus tasolla 2.0 ja että M2-koneella on Poraus-ominaisuus tasolla 11.0. Määritä sitten, että 10.0 on Poraus-ominaisuuden vähimmäisvaatimus reitillä. Ajoitusmoduuli päättelee sitten, että vain M2-kone vastaa resurssivaatimuksia.

## <a name="competencies-for-human-resources"></a>Henkilöresurssien ominaisuudet
Kun sinulla on **Henkilöresurssi**-tyyppisiä operatiivisia resursseja, jotka on linkitetty työntekijöihin Henkilöstöhallinnossa, voit myös hyödyntää työntekijöiden ominaisuuksia määrittäessäsi tuotantoreitin resurssivaatimuksia. Voit toisin sanoen määrittää tiettyjä osaamisalueita, kursseja, todistuksia tai ammattinimikkeitä koskevia vaatimuksia. Ajoitusmoduuli voi sitten valita työntekijöihin linkitetyt resurssit, ja valinta tapahtuu näiden työntekijöiden ominaisuuksien perusteella. Ominaisuudet määritetään Henkilöstöhallinto-sivulla eikä **Resurssin ominaisuudet** -sivulla. Kun määrität osaamisalueita, kursseja, todistuksia tai ammattinimikkeitä resurssivaatimuksiksi sinun on käytettävä Henkilöstöhallinto-toimintoa ja linkitettävä kukin **Henkilöresurssin** tyyppi vastaavalle työntekijälle. Jos et käytä Henkilöstöhallinto-toimintoa, voit määrittää ominaisuudet **Resurssin ominaisuudet** -sivulla, joka muistuttaa Henkilöstöhallinto-kohdan ominaisuuksia tai kopioi ne. **Resurssin ominaisuudet** -sivu ei kuitenkaan sisällä toimintoa, joka tarvitaan ylläpitämään osaamisalueita, kursseja, todistuksia tai ammattinimikkeitä.




