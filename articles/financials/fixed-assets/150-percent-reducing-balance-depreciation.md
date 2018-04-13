---
title: "Jäännöspoisto 150 prosenttia"
description: "Tässä artikkelissa on yleiskuvaus 150 prosentin jäännösarvon poistomenetelmästä."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b35b8ea652ccb06c45b8091cc7f57e849e1a5915
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="150-percent-reducing-balance-depreciation"></a>Jäännöspoisto 150 prosenttia

[!INCLUDE [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus 150 prosentin jäännösarvon poistomenetelmästä.

Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Jäännösarvo 150 %** -kentästä valitaan **Menetelmä**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla. Tämä prosentti lasketaan omaisuuserän käyttöajan mukaan. Jos omaisuuserän käyttöaika on esimerkiksi viisi vuotta, poistoprosentti on 30 (150 % ÷ 5). 

Kun haluat määrittää jäännösarvoksi 150 %, valitse myös **Poistoprofiilit**-sivun **Poistovuosi**- ja **Kausiväli**-kenttä. **Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.

## <a name="selection-of-depreciation-year"></a>Poistovuoden valitseminen
Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**. 

Oletusarvo on **Kalenteri**. Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä. Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.

### <a name="calendar"></a>Kalenteri

Voit säilyttää **Poistovuosi** -kentässä oletusarvon **Kalenteri**. 

**Kalenteri**-vaihtoehto päivittää joka vuosi poistokannan 1. tammikuuta. Yleensä poistokanta on nettokirjanpitoarvo vähennettynä jäännösarvolla. Alla olevissa esimerkeissä poistokanta on laskentasarakkeen ensimmäisen lausekkeen osoittaja. 

Jos poistovuodeksi valitaan **Kalenteri**, **Kausiväli**-kentässä ovat käytettävissä seuraavat vaihtoehdot:

-   **Vuosittain** kirjaa summan 31. joulukuuta.
-   **Kuukausittain** kirjaa kuukausikohtaisen poiston kunkin kuun lopussa.
-   **Neljännesvuosittain** kirjaa neljännesvuoden poiston kalenterivuoden kunkin neljänneksen lopussa (31.3, 30.6. 30.9. ja 31.12.)
-   **Puolivuosittain** kirjaa puolen vuoden summan kalenteripuolivuosittain (30.6. ja 31.12.).
-   **Päivittäin** kirjaa päivittäisen poistomenetelmän poistosumman käyttämällä yhtä tapahtumaa päivää kohden.

### <a name="fiscal"></a>Veroasiakirja

Jos valitset **Poistovuosi**-kentässä **Tilivuosi**-vaihtoehdon, 150 prosentin jäännösarvo lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella. Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla. 

Esimerkiksi tilikauden 1.7 – 30.6. poistojen laskeminen alkaa 1.7. Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta. Poisto oikaistaan jokaisella kaudella. **Kirjanpidon kalenterit** -sivun kausien asetuksissa määritetään seuraavan tilikauden pituus. 

Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa **Kausiväli**-kentässä:

-   **Vuosittain** kirjaa tilivuodelle lasketun poiston kokonaismäärän tilivuoden viimeisenä päivänä.
-   **Tilikausi** kirjaa tilivuodelle lasketun poiston kokonaismäärän. Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.

## <a name="example-of-150-reducing-balance-depreciation"></a>Esimerkki 150 %:n jäännöspoistosta

|                                |        |
|--------------------------------|--------|
| Hankintakustannukset               | 11 000 |
| Jäännösarvo                  | 1 000  |
| Poistokanta              | 10 000 |
| Käyttöikä vuosina             | 5      |
| Vuosittainen poistoprosentti: | 30 %    |

150 %:n jäännösarvomenetelmä jakaa arvon 150 % käyttövuosilla. Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.

| Kausi | Vuotuisen poistomäärän laskeminen | Kirjanpitoarvo             | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| Vuosi 1 | (11 000 - 1 000) × 30 % = 3 000                | 11 000 - 3 000 = 8 000 | 11 000 - 1 000 – 3 000 = 7 000        |
| Vuosi 2 | 7 000 × 30 % = 2 100                           | 8 000 - 2 100 = 5 900  | 7 000 - 2 100 = 4 900                 |
| Vuosi 3 | 4 900 × 30 % = 1 470                           | 5 900 - 1 470 = 4 430  | 4 900 - 1 470 = 3 430                 |

> [!NOTE]
> Jos 150 %:n jäännösarvon poistomenetelmän avulla laskettu määrä on pienempi kuin tasapoistomenetelmän avulla laskettu määrä, jäljellä olevalle käyttöiälle on yleensä olemassa tasapoistomenetelmä.




