---
title: Jäännöspoisto 200 prosenttia
description: Tässä artikkelissa on yleiskuvaus 200 prosentin jäännösarvon poistomenetelmästä.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0474a8cecccaf1e23874458c27e0bea991140b6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187426"
---
# <a name="200-percent-reducing-balance-depreciation"></a>Jäännöspoisto 200 prosenttia

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus 200 prosentin jäännösarvon poistomenetelmästä.

Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Menetelmä** -kentästä valitaan **Jäännösarvo 200 %**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla. Prosentti lasketaan omaisuuserän käyttöajan mukaan. Jos omaisuuserän käyttöaika on esimerkiksi viisi vuotta, poistoprosentti on 40 (200 % ÷ 5). 

Tästä menetelmästä käytetään myös nimeä DDB-menetelmä.

Jos haluat määrittää jäännösarvoksi 200 %, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kentän asetukset. **Kausiväli**-kentässä valittavissa olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.

## <a name="select-a-depreciation-year"></a>Poistovuoden valitseminen
Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**. Oletusarvo on **Kalenteri**. 

Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä. Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.

### <a name="calendar"></a>Kalenteri

Voit säilyttää **Poistovuosi** -kentässä oletusarvon **Kalenteri**. 

**Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta. Yleensä poisto on nettokirjanpitoarvo vähennettynä jäännösarvolla. Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja. 

Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:

-   **Vuosittain** kirjaa summan 31. joulukuuta.
-   **Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.
-   **Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)
-   **Puolivuosittain** kirjaa puolen vuoden summan kalenteripuolivuosittain (30.6. ja 31.12.).
-   **Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.

### <a name="fiscal"></a>Veroasiakirja

Jos valitset **Poisto** vuosi-kentässä **Tilivuosi**-vaihtoehdon, 200 prosentin jäännösarvo lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella. Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla. 

Esimerkiksi tilikauden 1.7 – 30.6. poistojen laskeminen alkaa 1.7. Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta. Poisto oikaistaan jokaisella kaudella. **Kirjanpidon kalenterit** -sivun kausien asetuksissa määritetään seuraavan tilikauden pituus. 

Jos poistovuodeksi valitaan **Tilivuosi**, **Kausiväli**-kentässä ovat valittavana seuraavat vaihtoehdot:

-   **Vuosittain**-vaihtoehto kirjaa tilikaudelle lasketun poiston kokonaismäärän yhtenä summana tilikauden viimeisenä päivänä.
-   **Tilikausi** kirjaa tilivuodelle lasketun poiston kokonaismäärän. Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.

## <a name="example-of-200-reducing-balance-depreciation"></a>Esimerkki 200 prosentin jäännöspoistosta

|                                |        |
|--------------------------------|--------|
| Hankintakustannukset               | 11 000 |
| Jäännösarvo                  | 1 000 |
| Poistokanta              | 10 000 |
| Käyttöikä vuosina             | 5      |
| Vuosittainen poistoprosentti: | 40 %    |

200 %:n jäännösarvomenetelmä jakaa arvon 200 % käyttövuosilla. Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.

| Kausi | Vuotuisen poistomäärän laskeminen | Kirjanpitoarvo             | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| Vuosi 1 | (11 000 – 1 000) × 40 % = 4 000                | 11 000 – 4 000 = 7 000 | 11 000 – 1 000 – 4 000 = 6 000        |
| Vuosi 2 | 6 000 × 40 % = 2 400                           | 7 000 – 2 400 = 4 600  | 6 000 – 2 400 = 3 600                 |
| Vuosi 3 | 3 600 × 40 % = 1 440                           | 4 600 – 1 440 = 3 160  | 3 600 – 1 440 = 2 160                 |

> [!NOTE] 
> Jos 200 %:n jäännösarvon poistomenetelmän avulla laskettu määrä on pienempi kuin tasapoistomenetelmän avulla laskettu määrä, jäljellä olevalle käyttöiälle on yleensä olemassa tasapoistomenetelmä.



