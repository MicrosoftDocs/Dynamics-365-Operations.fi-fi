---
title: Resurssin ominaisuudet
description: "Tässä artikkelissa on tietoja resurssin ominaisuuksista. Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Artikkelissa kerrotaan miten ominaisuuksia ja siihen liittyviä käsitteitä, kuten pätevyystasoa ja prioriteettia, käytetään valittaessa sopivia resursseja tehtävään."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4463ca8e11115eb83323716faa4ed6b38937a3e4
ms.lasthandoff: 03/31/2017


---

# <a name="resource-capabilities"></a>Resurssin ominaisuudet

Tässä artikkelissa on tietoja resurssin ominaisuuksista. Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Artikkelissa kerrotaan miten ominaisuuksia ja siihen liittyviä käsitteitä, kuten pätevyystasoa ja prioriteettia, käytetään valittaessa sopivia resursseja tehtävään.

Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Operatiivisella resurssilla voi olla useampi kuin yksi siihen liitetty ominaisuus, ja ominaisuus voidaan määrittää useammalle kuin yhdelle resurssille. Voit määrittää ominaisuuksia resursseille tilapäisesti asettamalla ominaisuusmääritykselle alkamis- ja vanhentumispäivät. Kun resurssin ominaisuuden voimassaolo on päättynyt, kyseistä resurssia ei voida kohdistaa projektille tai tuotannolle, joka vaatii kyseisen ominaisuuden. Ominaisuus, jonka voimassaolo on päättynyt, voidaan uusia. Voit poistaa ominaisuuksia sillä edellytyksellä, että ne eivät ole reitityssuhteella tai osana aktiivisen tuotantotilauksen tuotantoreititystä. Yleisesti ottaen, ole varovainen poistaessasi ominaisuuksia. Harkitse sen sijaan kyseisen ominaisuuden sisältävien resurssien voimassaolon päättymispäivän muuttamista. Ominaisuuksia voidaan määrittää kaiken tyyppisille resursseille: työkalu, toimittaja, kone, toimipaikka, tai henkilöresurssi.

## <a name="level"></a>Tasaa
Useilla resursseilla on usein sama toiminnallinen ominaisuus mutta eri pätevyystasoilla (esimerkiksi vahvuus, käsittelynopeus tai tarkkuus). Näin ollen, määrittäessäsi resurssille ominaisuuden, voit määrittä **Taso**-arvon. Tasoarvo on yksinkertainen numeerinen arvo. Jos määrität, että ominaisuus on tuotantoreitityksen resurssivaatimus, voit määrittää myös**Vaadittu vähimmäistaso** -arvon kyseiselle ominaisuudelle. Ajoitusmoduuli valitsee sitten vain ne resurssit, joilla on tarvittavat ominaisuudet tasolla, joka vastaa resurssivaatimuksessa määriteltyä vähimmäistasoa tai on sitä suurempi.

## <a name="priority"></a>Prioriteetti
Operatiivisille resursseille, joilla on samat ominaisuudet, voidaan määrittää prioriteetti. Sitten, jos useita resursseja on ominaisuuksia, jotka täyttävät ajoitusvaatimusten vaadittavalla tasolla, ja on vapaata kapasiteettia, aikataulutusmoduuli valita näiden resurssien kesken. Jos **prioriteetti** valitaan **ensisijaisen resurssin valinta** -kenttään **ajoitusparametrit** sivun resurssi, joka on korkein prioriteetti (alin numeerinen arvo **prioriteetti** kenttä) valitaan ensimmäinen ajoituksen aikana.

## <a name="resource-requirements"></a>Resurssivaatimukset
Määrittäessäsi resurssivaatimukset tuotantoreititykselle, voit määrittää yhden tai useampia ominaisuuksia vaatimuksiksi. Tuotantosuunnitelmassa ominaisuudet, jotka on määritetty reitityksen työvaiheen resurssivaatimuksissa, kohdistetaan resursseille määritettyihin ominaisuuksiin. Resurssit, joiden ominaisuudet vastaavat resurssivaatimukset, valitaan. Jos useilla resursseilla on usein sama toiminnallinen ominaisuus mutta eri pätevyydet (kuten vahvuus, käsittelynopeus tai tarkkuus), voit joko määrittää useita ominaisuuksia tai käyttää ominaisuuden tasoa resurssin ominaisuuden määrittämiseksi. Tässä on esimerkki:

-   Reitityksessä porausprosessin aika on asetettu 10 yksikköön tunnissa, mutta itse vaatimus on määritetty arvolla Poraus.
-   Sinulla on kaksi porauskonetta, M1 ja M2.
-   Poraus-ominaisuus on määritetty molemmille resursseille, M1-koneelle ja M2-koneelle.
-   M1-kone pystyy poraamaan kaksi yksikköä tunnissa ja M2-kone pystyy poraamaan 11 yksikköä tunnissa.

Tässä esimerkissä ajoitusmoduuli voi valita molemmat koneet, koska molemmat täyttävät perusominaisuusvaatimuksen (Poraus). M1-kone pystyy kuitenkin poraamaan vain kaksi yksikköä tunnissa. Koska tämä määrä on paljon vähemmän kuin reitille määritetty 10 yksikköä tunnissa, M1-kone aiheuttaa tuotanto-ongelmia, jos se valitaan. On kaksi tapaa ratkaista tämä ongelma ja varmistaa, että M2-kone valitaan M1-koneen sijaan:

-   Luo kaksi erillistä ominaisuutta: Hidas poraus ja Nopea poraus. Määritä Hidas poraus poraukseksi, jonka prosessiaika on yhdestä yhdeksään yksikköä tunnissa. Määritä Nopea poraus poraukseksi, jonka porausprosessiaika on 10 - 19 yksikköä tunnissa. Määritä koneen M1 ydinjätteen Low-speed-ominaisuus ja määritä M2 koneen nopean ydinjätteen ominaisuus. Lopuksi muuta mahdollisuutta resurssitarve reitillä nopea poraus. Ajoitusmoduuli valitsee sitten oikean koneen (M2).
-   Käytä ominaisuuden tasoa määrittämään Poraus-ominaisuus, joka määritetään porauskoneille. Määrittää, että M1-kone on 2.0 tasolla Drilling valmiudet ja M2-kone on valmius Drilling 11.0 tasolla. Sitten määrittää, että 10.0 vähimmäistason, jota tarvitaan Drilling ominaisuus vaatimus reitillä. Ajoitusmoduuli päättelee sitten, että vain M2-kone vastaa resurssivaatimuksia.

## <a name="competencies-for-human-resources"></a>Henkilöresurssien ominaisuudet
Kun sinulla on **Henkilöresurssi**-tyyppisiä operatiivisia resursseja, jotka on linkitetty työntekijöihin Henkilöstöhallinnossa, voit myös hyödyntää työntekijöiden ominaisuuksia määrittäessäsi tuotantoreitin resurssivaatimuksia. Voit toisin sanoen määrittää tiettyjä osaamisalueita, kursseja, todistuksia tai ammattinimikkeitä koskevia vaatimuksia. Ajoitusmoduuli voi sitten valita työntekijöihin linkitetyt resurssit, ja valinta tapahtuu näiden työntekijöiden ominaisuuksien perusteella. Ominaisuudet määritetään Henkilöstöhallinto-sivulla eikä **Resurssin ominaisuudet** -sivulla. Kun taidot, kurssit, todistukset tai otsikoita Määritä resurssivaatimukset, Human resources-toimintoa ja linkittää kunkin resurssin **henkilöstöhallinnon** tyyppiä vastaava työntekijä. Jos et käytä henkilöstöhallinnon toimintoja, voit määrittää ominaisuuksia **resurssin ominaisuudet**, jotka muistuttavat tai -inhimillisten voimavarojen osaamisalueet monista sivu. **Resurssin ominaisuudet** -sivu ei kuitenkaan sisällä toimintoa, joka tarvitaan ylläpitämään osaamisalueita, kursseja, todistuksia tai ammattinimikkeitä.


