---
title: "Käyttöikään perustuva tasapoisto"
description: "Tässä artikkelissa on yleiskuvaus käyttöikään perustuvasta tasapoistomenetelmästä."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bb5715855c7e240cddf4fd264a4b26ca09a2f6c4
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="straight-line-service-life-depreciation"></a>Käyttöikään perustuva tasapoisto

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus käyttöikään perustuvasta tasapoistomenetelmästä.

Jos määrität käyttöomaisuudelle poistoprofiilin ja valitset Tasapoisto - käyttöaika -asetuksen Poistoprofiilit-sivun Menetelmä-kentästä, niiden käyttöomaisuuserien poisto, joille on määritetty tämä poistoprofiili, perustuu käyttöomaisuuden jäljellä olevaan käyttöikään. Tavallisesti poiston määrä on tällöin sama kullakin poistojaksolla. 

Ero tasapoiston jäljellä olevan käyttöajan ja tasapoiston käyttöajan mukaan lasketun poiston määrässä on silloin, kun käyttöomaisuuteen kirjataan arvon muutos. 

Jos haluat määrittää käyttöaikaan perustuvan tasapoiston, valitse Poistoprofiilit-sivulla myös Poistovuosi- ja Kausiväli-kenttien asetukset.

## <a name="select-a-depreciation-year"></a>Poistovuoden valitseminen
Voit valita Poistoprofiilit-sivulla Poistovuosi-kenttään joko Kalenteri tai Tilikausi. Valinta määrittää, mitä valintoja Kausiväli-kentässä on käytettävissä. Oletusarvo on Kalenteri.

### <a name="calendar"></a>Kalenteri

Jos valitset Poistovuosi-kentän arvoksi Kalenterivuosi, järjestelmä olettaa kauden olevan 1. tammikuuta–31. joulukuuta, vaikka kirjanpidon vuosikalenteri olisikin määritetty toisin. 

Kalenteri-vaihtoehto päivittää poistokannan, joka on tavallisesti nettokirjanpitoarvo vähennettynä jäännösarvolla, kunkin vuoden tammikuun 1. päivänä. Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja. 

Jos valitset Kalenteri-vaihtoehdon, Kausiväli-kentässä ovat käytettävissä seuraavat vaihtoehdot, jotka määrittävät poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana:
-   Vuosittain – summa kirjataan 31. joulukuuta.
-   Kuukausittain kirjaa kuukausikohtaisen poiston kunkin kuun lopussa
-   Neljännesvuosittain kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)
-   Puolivuosittain – puolen vuoden summa kirjataan kunkin kalenterivuosipuolikkaan lopussa (30.6. ja 31.12.)
-   Päivittäin kirjaa päivittäisen poistomenetelmän poistosumman yhdellä tapahtumalla päivää kohden.

Jos valitset esimerkiksi Vuosittain, vuoden poisto kirjataan vain kerran eli kunkin vuoden joulukuun 31. päivä. Jos valitset Kuukausittain, kuukauden poisto kirjataan joka kuukausi käyttämällä 1/12 koko vuoden poistosummasta.

### <a name="fiscal"></a>Tilivuosi

Jos valitset Poistovuosi-kentästä Tilivuosi-vaihtoehdon, käytetään käyttöaikaan perustuvaa tasapoistomenetelmää. Se lasketaan tilivuodesta, jonka määrittää kirjalle määritetty kirjanpidon vuosikalenteri tai Kirjanpito-sivulla valittu kirjanpidon vuosikalenteri. Kirjanpidon vuosikalenterit määritetään Kirjanpidon kalenterit -sivulla.

Esimerkiksi tilikauden 1.7–30.6. poistojen laskeminen alkaa 1.7. Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta. Poisto oikaistaan automaattisesti jokaisella tilikaudella. Seuraavan tilikauden pituus perustuu Kirjanpidon kalenterit -lomakkeessa uuden tilikauden luomisen yhteydessä määritettyihin tilikausiin. 

Jos valitset tilivuoden, seuraavat vaihtoehdot ovat käytettävissä Kausiväli-kentässä:
-   Vuosittain-vaihtoehto kirjaa tilikaudelle lasketun poiston kokonaismäärän yhtenä summana tilikauden viimeisenä päivänä.
-   Tilikausi laskee tilivuodelle poiston kokonaismäärän. Se jaetaan kausiksi, jotka on määritetty kirjanpidon vuosikalenterille Kirjanpidon kalenterit -lomakkeessa.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Esimerkki: Muuttumattoman käyttöomaisuuden tasapoisto
Oletetaan, että käyttöomaisuudella on seuraavat ominaisuudet.

|                     |        |
|---------------------|--------|
| Hankintakustannukset    | 11 000 |
| Jäännösarvo       | 1 000  |
| Poistokanta   | 10 000 |
| Käyttöikä vuosina  | 5      |
| Vuotuinen poisto | 2 000  |

Poiston määrä kunakin vuonna on sama. (hankintahinta - jäännösarvo) / käyttöaika vuosina

| Jakso: | Vuotuisen poistomäärän laskeminen: | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-------------------------------------------|---------------------------------------|
| Vuosi 1 | (11 000 - 1 000) / 5 = 2 000              | 9 000                                 |
| Vuosi 2 | (11 000 - 1 000) / 5 = 2 000              | 7 000                                 |
| Vuosi 3 | (11 000 - 1 000) / 5 = 2 000              | 5 000                                 |
| Vuosi 4 | (11 000 - 1 000) / 5 = 2 000              | 3 000                                 |
| Vuosi 5 | (11 000 - 1 000) / 5 = 2 000              | 1 000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a> Esimerkki: Muutetun käyttöomaisuuden tasapoisto

Oletetaan, että samaan käyttöomaisuuserään lisätään vuonna 2 hankintaoikaisu, jonka arvo on 4 000. 

Hankintaoikaisun käyttöaika on sama kuin käyttöomaisuuserän käyttöaika ja se alkaa hankintahetkellä. Vuoden 5 lopussa on jäljellä nettokirjanpitoarvo, joka vastaa hankintaoikaisun nettokirjanpitoarvoa. Kunkin jakson poisto lasketaan seuraavassa taulukossa esitetyllä tavalla.

| Jakso: | Vuotuisen poistomäärän laskeminen: | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-------------------------------------------|---------------------------------------|
| Vuosi 1 | 10 000 / 5 = 2 000                        | 11 000 - 2 000 = 9 000                |
| Vuosi 2 | 4 000 (hankintaoikaisu)            | 9 000 + 4 000 =13 000                 |
| Vuosi 2 | 14 000 / 5 = 2 800                        | 13 000 - 2 800 = 10 200               |
| Vuosi 3 | 14 000 / 5 = 2 800                        | 10 200 - 2 800 = 7 400                |
| Vuosi 4 | 14 000 / 5 = 2 800                        | 7 400 - 2 800 = 4 600                 |
| Vuosi 5 | 14 000 / 5 = 2 800                        | 4 600 - 2 800 = 1 800                 |
| Vuosi 6 | Jäljellä oleva arvo 800\*                           | 1 800 – 800 = 1 000                   |

\*Koska jäännösarvo on pienempi kuin poistosumma, kirjataan vain jäännösarvolla vähennetty jäljellä oleva summa.






