---
title: "Jäännöspoisto 175 prosenttia"
description: "Tässä artikkelissa on yleiskuvaus 175 prosentin jäännösarvon poistomenetelmästä."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 812fbb3cc3159783e9908e537c366ffc7f934092
ms.lasthandoff: 03/31/2017


---

# <a name="175-percent-reducing-balance-depreciation"></a>Jäännöspoisto 175 prosenttia

Tässä artikkelissa on yleiskuvaus 175 prosentin jäännösarvon poistomenetelmästä.

Kun käyttöomaisuuden poistoprofiili määritetään ja **Poistoprofiilit**-sivun **Menetelmä** -kentästä valitaan **Jäännösarvo 175 %**, tähän poistoprofiiliin liitetyn käyttöomaisuuden poistoprosentti on sama kullakin poistojaksolla. 

Jos haluat määrittää jäännösarvoksi 175 %, valitse **Poistoprofiilit**-sivulla myös **Poistovuosi**- ja **Kausiväli**-kentän asetukset. **Kausiväli**-kentän käytettävissä olevat vaihtoehdot vaihtelevat **Poistovuosi**-kentässä valitun arvon mukaan.

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

Jos valitset **Poistovuosi**-kentässä **Tilivuosi**-vaihtoehdon, 175 prosentin jäännösarvo lasketaan kirjalle määritetyn kirjanpidon vuosikalenterin tilivuoden perusteella tai **Kirjanpito**-sivulla valitun kirjanpidon vuosikalenterin perusteella. Kirjanpidon vuosikalenterit määritetään **Kirjanpidon kalenterit** -sivulla. Lisätietoja on ohjeaiheessa [kirjanpidon vuosikalenterit, tilivuodet ja pisteitä.](\financials\budgeting\fiscal-calendars-fiscal-years-periods.md).

Esimerkiksi heinäkuun 1. – 30. kesäkuuta tilikauden poiston laskeminen alkaa heinäkuun 1. Tilivuosi voi olla pidempi tai lyhyempi kuin 12 kuukautta. Poisto säätyy automaattisesti kutakin tilijaksoa varten ja seuraavan tilivuoden pituus määräytyy **Kirjanpidon kalenterit**-lomakkeessa määritetyistä tilijaksojen asetuksista. 

Jos valitset poistovuodeksi **Tilivuosi**, seuraavat vaihtoehdot ovat valittavissa**Kausiväli**-kentässä:

-   **Vuosittain** kirjaa tilivuodelle lasketun poiston kokonaismäärän tilivuoden viimeisenä päivänä.
-   **Tilikausi** laskee tilikaudelle lasketun poiston kokonaismäärän. Summa on jaksotettu tilikausille, jotka määritetään **Kirjanpidon kalenterit** -sivulla.

## <a name="example-of-175-reducing-balance-depreciation"></a>Esimerkki 175 prosentin jäännöspoistosta
|                                |        |
|--------------------------------|--------|
| Hankintakustannukset               | 11 000 |
| Jäännösarvo                  | 1 000  |
| Poistokanta              | 10 000 |
| Käyttöikä vuosina             | 5      |
| Vuosittainen poistoprosentti: | 35 %    |

175 %:n jäännösarvon poistomenetelmä jakaa arvon 175 % käyttövuosilla. Kyseinen prosentti kerrotaan käyttöomaisuuserän nettokirjanpitoarvolla, jolloin saadaan tulokseksi vuoden poistosumma.

| Kausi | Vuotuisen poistomäärän laskeminen | Kirjanpitoarvo                  | Nettokirjanpitoarvo vuoden lopussa: |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| Vuosi 1 | (11 000 – 1 000) × 35 % = 3 500                | 11 000 – 3 500 = 7 500      | 11 000 – 1 000 – 3 500 = 6 500        |
| Vuosi 2 | 6 500 × 35 % = 2 275                           | 7 500 – 2 275 = 5 225       | 6 500 – 2 275 = 4 225                 |
| Vuosi 3 | 4 225 × 35 % = 1 478,75                        | 5 225 – 1 478,75 = 3 746,25 | 4 225 – 1 478,75 = 2 746,25           |

> [!NOTE] 
> Kun summa, joka lasketaan käyttämällä 175 prosentin jäännöspoiston degressiivistä poistomenetelmää, yleensä on pienempi kuin se summa, joka lasketaan käyttämällä tasapoiston menetelmää on jäljellä olevana tasapoistomenetelmän poistoprosentin muuntaminen.


