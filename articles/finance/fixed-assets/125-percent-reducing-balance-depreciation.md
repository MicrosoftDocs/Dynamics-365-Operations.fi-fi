---
title: Jäännöspoisto 125 prosenttia
description: Tässä artikkelissa on yleiskuvaus 125 prosentin jäännösarvon poistomenetelmästä.
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9511917d72a1bb45daf2ce7e4b56d94c17825daf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969225"
---
# <a name="125-percent-reducing-balance-depreciation"></a>Jäännöspoisto 125 prosenttia

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleiskuvaus 125 prosentin jäännösarvon poistomenetelmästä.

Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Menetelmä** -kentästä valitaan **Jäännösarvo 125 %**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla. Tämä prosentti lasketaan omaisuuserän käyttöajan mukaan. Jos omaisuuserän käyttöaika on esimerkiksi viisi vuotta, poistoprosentti on 25 (125 % ÷ 5).

Jos haluat määrittää jäännösarvoksi 125 %, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kentän asetukset. **Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.

## <a name="select-a-depreciation-year"></a>Poistovuoden valitseminen
Voit valita **Poistoprofiilit**-sivulla **Poistovuosi**-kenttään joko **Kalenteri** tai **Tilikausi**. Oletusarvo on **Kalenteri**. 

Valinta määrittää, mitä valintoja **Kausiväli**-kentässä on käytettävissä. Tämä kenttäsi määrittää poiston jaksotuksen kirjauspäivät ja -määrät kalenterivuoden aikana.

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

Jos valitset **Poistovuosi**-kentässä **Tilivuosi**-vaihtoehdon, 125 prosentin poisto lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella. Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla. 

Esimerkiksi tilikauden 1.7 – 30.6. poistojen laskeminen alkaa 1.7. Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta. Poisto säätyy automaattisesti kutakin tilijaksoa varten ja seuraavan tilivuoden pituus määräytyy **Kirjanpidon kalenterit**-lomakkeessa määritetyistä tilijaksojen asetuksista. 

Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa **Kausiväli**-kentässä:

-   **Vuosittain**-vaihtoehto kirjaa tilikaudelle lasketun poiston kokonaismäärän yhtenä summana tilikauden viimeisenä päivänä.
-   **Tilikausi** kirjaa tilivuodelle lasketun poiston kokonaismäärän. Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.

## <a name="example-of-125-reducing-balance-depreciation"></a>Esimerkki 125 prosentin jäännöspoistosta

|                                |        |
|--------------------------------|--------|
| Hankintakustannukset               | 11 000 |
| Jäännösarvo                  | 1 000  |
| Poistokanta              | 10 000 |
| Käyttöikä vuosina             | 5      |
| Vuosittainen poistoprosentti: | 25 %    |

125 %:n jäännösarvomenetelmä jakaa arvon 125 % käyttövuosilla. Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.

| Kausi | Vuotuisen poistomäärän laskeminen | Kirjanpitoarvo                    | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| Vuosi 1 | (11 000 – 1 000) × 25% = 2 500                | (11 000 – 2 500) = 8 500      | (11 000 – 1 000 – 2 500) = 7 500      |
| Vuosi 2 | 7 500 × 25 % = 1 875                           | (8 500 – 1 875) = 6 625       | (7 500 – 1 875) = 5 625               |
| Vuosi 3 | 5 625 × 25 % = 1 406,25                        | (6 625 – 1 406,25) = 5 218,75 | (5 625 – 1 406,25) = 4 218,75         |

> [!NOTE] 
> Jos 125 %:n jäännösarvon poistomenetelmän avulla laskettu määrä on pienempi kuin tasapoistomenetelmän avulla laskettu määrä, jäljellä olevalle käyttöiälle on yleensä olemassa tasapoistomenetelmä.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]