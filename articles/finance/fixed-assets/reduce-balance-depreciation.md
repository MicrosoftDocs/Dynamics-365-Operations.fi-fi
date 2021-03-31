---
title: Jäännöspoiston vähentäminen
description: Tässä artikkelissa on yleiskuvaus poiston jäännösarvopoistomenetelmästä.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69228aec217826780ceb91771028a6a5a180d037
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220982"
---
# <a name="reduce-balance-depreciation"></a>Jäännöspoiston vähentäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus poiston jäännösarvopoistomenetelmästä.

Kun käyttöomaisuuden poistoprofiili määritetään ja Poistoprofiilit-sivun Menetelmä-kentästä valitaan Jäännösarvo, tähän poistoprofiiliin liitettyjen käyttöomaisuuserien poistoprosentti on sama kullakin poistojaksolla.

Voit määrittää jäännösarvopoiston tekemällä valinnat myös Poistoprofiilit-lomakkeen Yleinen-pikavälilehden kenttissä. Valitse ensin vuosi Poistovuosi-kentässä. Tekemäsi valinnan mukaan Kausiväli-kentässä näkyy erilaisia vaihtoehtoja, kuten seuraavissa osissa kerrotaan. 

Määritä arvo myös poistoprofiilin Prosentti-kenttään. Jos valitset Täyspoisto-vaihtoehdon, jäljellä oleva poistokantana käytetään viimeisen poistokauden summaa, joka voi olla suuri. Joissakin maissa tai joillakin alueilla ei käytetä siirtymistä tasapoistomenetelmään. Vaihdos tapahtuu, kun vaihtoehtoisen poistomenetelmän summa on suurempi tai yhtä suuri kuin ensisijaisen poistoprofiilin summa ja poistosummaksi valitaan vaihtoehtoisen menetelmän summa. 

Koska käyttöomaisuus ei prosenttilaskennan avulla tule koskaan kokonaan poistetuksi, Täyspoisto-vaihtoehto on valittava, jos käyttöomaisuuserä halutaan poistaa kokonaan.

## <a name="select-a-depreciation-year"></a>Poistovuoden valitseminen
Voit valita Poistoprofiilit-sivulla Poistovuosi-kenttään joko Kalenteri tai Tilikausi. Valinta määrittää, mitä valintoja Kausiväli-kentässä on käytettävissä. Oletusarvo on Kalenteri.

### <a name="calendar"></a>Kalenteri

Kalenteri-vaihtoehto päivittää poistokannan, joka on tavallisesti nettokirjanpitoarvo vähennettynä jäännösarvolla, kunkin vuoden tammikuun 1. päivänä. Myöhemmin tässä ohjeaiheessa olevassa jäännöspoistoesimerkeissä poistokanta on laskelmien sarakkeen ensimmäisen lausekkeen osoittaja. 

Jos valitset Kalenteri-vaihtoehdon, Kausiväli-kentässä ovat käytettävissä seuraavat vaihtoehdot, jotka määrittävät poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana:

-   Vuosittain tekee kirjauksen 31. joulukuuta
-   Kuukausittain kirjaa kuukausikohtaisen poiston kunkin kuun lopussa
-   Neljännesvuosittain kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)
-   Puolivuosittain kirjaa puolen vuoden summan kunkin kalenterivuosipuolikkaan lopussa (30.6. ja 31.12.)
-   Päivittäin kirjaa päivittäisen poistomenetelmän poistosumman yhdellä tapahtumalla päivää kohden.

Jos valitset esimerkiksi Vuosittain, vuoden poisto kirjataan vain kerran eli kunkin vuoden joulukuun 31. päivä. Jos valitset Kuukausittain, kuukauden poisto kirjataan joka kuukausi käyttämällä 1/12 koko vuoden poistosummasta.

### <a name="fiscal"></a>Tilivuosi

Jos valitset Poistovuosi-kentästä Tilivuosi-vaihtoehdon, käytetään tasapoistomenetelmää. Se lasketaan Kirjanpito-sivulla valitulle tilikalenterille Kirjanpidon kalenterit -sivulla määritetyn tilivuoden perustella. Esimerkiksi tilikauden 1.7–30.6. poistojen laskeminen alkaa 1.7. Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta. Poisto oikaistaan jokaisella tilikaudella. Seuraavan tilivuoden pituus perustuu Kirjanpidon kalenterit -sivulla uuden tilivuoden luomisen yhteydessä määritettyihin tilikausiin.


Jos valitset tilivuoden, seuraavat vaihtoehdot ovat käytettävissä Kausiväli-kentässä:

-   Kirjaa vuosittain tilivuodelle lasketun poiston kokonaismäärän yhtenä summana tilivuoden viimeisenä päivänä.
-   Tilikausi kirjaa tilikaudelle lasketun poiston kokonaismäärän, joka jaksotetaan tilikausille, jotka on määritetty Kirjanpito-sivulla valitun kirjanpidon kalenterissa tai käyttöomaisuuden kirjalle valitussa kirjanpidon kalenterissa.

## <a name="example-of-reducing-balance-depreciation"></a>Esimerkki jäännöspoistosta

Oletetaan, että käyttöomaisuuserän hankintahinta on 11 000, romutusarvo on 1 000 ja poistoprosentti on 30. 

Jäännösarvopoisto-menetelmää käytettäessä lasketaan 30 prosenttia edellisen poistokauden lopun poistokannasta (nettokirjanpitoarvo vähennettynä romutusarvolla). Seuraavassa taulukossa on esitetty ensimmäisten kolmen vuoden poistot.

| Kausi | Vuotuisen poistomäärän laskeminen: | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-------------------------------------------|---------------------------------------|
| Vuosi 1 | (11 000 - 1 000) \* 30 % = 3 000           | (11 000 - 1 000) - 3 000 = 7 000      |
| Vuosi 2 | (7 000 - 1 000) \* 30 % = 1 800            | (7 000 -1 800) = 5 200                |
| Vuosi 3 | (5 200 - 1 000) \* 30 % = 1 260            | (5 200 - 1 260) = 3 940               |


-







[!INCLUDE[footer-include](../../includes/footer-banner.md)]