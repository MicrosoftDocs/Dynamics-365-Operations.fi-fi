---
title: "Jäljellä olevan käyttöajan tasapoisto"
description: "Tässä artikkelissa on yleiskuvaus jäljellä olevaan käyttöaikaan perustuvasta tasapoistomenetelmästä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: 9b690b80f148e7ccecba19850bd78c81216d8658
ms.lasthandoff: 03/31/2017


---

# <a name="straight-line-life-remaining-depreciation"></a>Jäljellä olevan käyttöajan tasapoisto

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on yleiskuvaus jäljellä olevaan käyttöaikaan perustuvasta tasapoistomenetelmästä.

Jos määrität käyttöomaisuudelle poistoprofiilin ja valitset **Tasapoisto - jäljellä oleva käyttöaika** -asetuksen **Poistoprofiilit**-sivun **Menetelmä** -kenttään, niiden käyttöomaisuuserien poisto, joille on määritetty tämä poistoprofiili, perustuu käyttöomaisuuden jäljelläoleviin käyttövuosiin. Tavallisesti poiston määrä on tällöin sama kullakin poistojaksolla. Jos haluat määrittää jäljellä olevaan käyttöaikaan perustuvan tasapoiston, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kenttien asetukset. **Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.

## <a name="select-a-depreciation-year"></a>Poistovuoden valitseminen
Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**. Oletusarvo on **Kalenteri**. Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä. Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.

### <a name="calendar"></a>Kalenteri

Valitessasi ***Poistovuosi***-kentän arvoksi **Kalenterivuosi**, järjestelmä olettaa kauden olevan 1. tammikuuta – 31. joulukuuta, vaikka kirjanpidon vuosikalenteri olisikin määritetty toisin. **Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta. Yleensä poistokanta on nettokirjanpitoarvo vähennettynä jäännösarvolla. Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja. Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:

-   **Vuosittain** kirjaa summan 31. joulukuuta.
-   **Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.
-   **Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)
-   **Puolivuosittain** kirjaa puolen vuoden summan kunkin kalenterivuosipuolikkaan lopussa (30.6. ja 31.12.)
-   **Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.

Jos valitset esimerkiksi **Vuosittain**, vuoden poisto kirjataan vain kerran eli kunkin vuoden joulukuun 31. päivä. Jos valitset **Kuukausittain**, kuukauden poisto kirjataan joka kuukausi käyttämällä kahdestoistaosaa koko vuoden poistosummasta.

### <a name="fiscal"></a>Veroasiakirja

Jos valitset **Poistovuosi**-kentästä **Tilivuosi**-vaihtoehdon, käytetään käyttöaikaan perustuvaa tasapoistomenetelmää. Poisto lasketaan jäljellä olevien tilikausien mukaan. Esimerkiksi tilikauden 1.7.2015 – 30.6.2016 poistojen laskeminen alkaa 1.7. Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta. Poisto oikaistaan jokaisella tilikaudella. **Kirjanpidon kalenterit** -sivun kausien asetuksissa määritetään seuraavan tilikauden pituus. Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa**Kausiväli**-kentässä:

-   **Vuosittain** kirjaa tilivuodelle lasketun poiston kokonaismäärän yhtenä summana tilivuoden viimeisenä päivänä.
-   **Tilikausi** laskee tilikaudelle lasketun poiston kokonaismäärän. Tämä määrä jaetaan kirjauskausille, jotka on määritetty kirjan **Kirjanpidon kalenterit** -sivulla valitussa kirjanpitokalenterissa.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Esimerkki muuttamattoman käyttöomaisuuden tasapoistosta
Käyttöomaisuudella on seuraavat ominaisuudet:

|                     |        |
|---------------------|--------|
| Hankintakustannukset    | 11 000 |
| Jäännösarvo       | 1 000  |
| Poistokanta   | 10 000 |
| Käyttöikä vuosina  | 5      |
| Vuotuinen poisto | 2 000  |

Poiston määrä on sama vuosittain: (hankintahinta-jäännösarvo) / käyttövuodet

| Kausi | Vuotuisen poistomäärän laskeminen | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-----------------------------------------------|---------------------------------------|
| Vuosi 1 | (11 000 – 1 000) ÷ 5 = 2 000                  | −9 000                                 |
| Vuosi 2 | (9 000 – 1 000) ÷ 4 = 2 000                   | 7 000                                 |
| Vuosi 3 | (7 000 – 1 000) ÷ 3 = 2 000                   | 5 000                                 |
| Vuosi 4 | (5 000 – 1 000) ÷ 2 = 2 000                   | 3 000                                 |
| Vuosi 5 | (3 000 – 1 000) ÷ 1 = 2 000                   | 1 000                                 |






