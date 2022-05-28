---
title: Vuokrasopimuskirjojen määrittäminen
description: Tässä ohjeaiheessa käsitellään tietoja, joita ylläpidetään vuokrasopimuskirjoissa. Vuokrasopimuskirjat sisältävät kirjanpitokäytännöt, joiden mukaan vuokrasopimus otetaan huomioon järjestelmässä.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ba442b3085593221e2182b848e6879a96bbca127
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727086"
---
# <a name="set-up-lease-books"></a>Vuokrasopimuskirjojen määrittäminen

[!include [banner](../includes/banner.md)]

Vuokrasopimuskirjat sisältävät kirjanpitokäytännöt, joiden mukaan vuokrasopimus otetaan huomioon järjestelmässä. Kassaperusteisen kirjanpidon lisäksi resurssin vuokraus tukee seuraavia standardeja:

- Yhdysvaltojen yleisti hyväksytty kirjanpitostardardi US GAAP (Generally Accepted Accounting Principles)
- Kirjanpidon standardi ASC 842 (Accounting Standards Codification Topic 842)
- ASC 840
- Kansainvälinen tilinpäätösstandardi IFRS 16 (International Financial Reporting Standard 16)
- Kansainvälinen kirjanpitostandardi IAS 17 (International Accounting Standard 17)

Luo vuokrasopimuskirja noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokrasopimuskirjat**.
2. Lisää kirja valitsemalla **Uusi**.
3. Määritä seuraavat kentät.

    | Nimi                                     | kuvaus |
    |------------------------------------------|-------------|
    | Kirjanpitotaso                            | Valitse käytettävä kirjaustaso. Jokainen vuokrasopimukseen liitetty kirja määritetään tietylle kirjaustasolle. Kullakin kirjaustasolla on eri kirjaustarkoitukset. |
    | Vuokran tyyppi                               | Määritä, tuleeko vuokrasopimus luokitella automaattisesti vai määritetäänkö se ennalta rahoitus- tai käyttöleasingsopimukseksi. |
    | Kirjanpitokehys                     | Valitse kirjaan liittyvä kehys. |
    | Vuokra-/käyttöajan määrittäminen          | Järjestelmä luokittelee vuokrasopimuksen rahoitusleasingsopimukseksi, jos vuokrasopimustyyppi on määritetty **automaattiseksi** ja jos resurssin käyttöikää koskeva vuokra-aika on suurempi tai yhtä suuri kuin tässä kentässä määritetty prosenttisosuus.  |
    | Nykyinen arvo / resurssin käyvän arvon määrittäminen   | Anna kokonaisluku, joka määrittää vuokrasopimustyypin määrittävän raja-arvon. Jos tulevien vähimmäisvuokrien nykyinen arvo on enemmän kuin käyttäjän määritämä arvo kirjan asetuksista ja jos kirjan vuokrasopimuksen luokitus on määritetty automaattiseksi, järjestelmä luokittelee vuokrasopimuksen rahoitusleasingsopimukseksi. |
    | Lyhytaikainen kynnysarvo                     | Määritä lyhytaikaisten vuokraasopimusten kynnysarvona käytettävä kuukausien määrä. Jos vuokra-aika on pienempi tai yhtä suuri kuin tähän syöttämäsi kuukausien määrä, järjestelmä luokittelee vuokrasopimuksen lyhytaikaiseksi vuokrasopimukseksi ja käyttää toteutumattoman vuokran käsittelyä. |
    | Arvoltaan vähäinen kynnysarvo                      | Anna summa, jota käytetään arvoltaan vähäisen vuokrasopimuksen kynnysarvona. Jos resurssin käypä arvo on pienempi tai yhtä suuri kuin tähän syöttämäsi arvo, järjestelmä luokittelee vuokrasopimuksen arvoltaan vähäiseksi vuokrasopimukseksi ja käyttää toteutumattoman vuokran käsittelyä. |
    | Maksu toimittajalle                            | Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sallia maksujen kirjaamisen laskuna jokaiselle vuokrasopimukselle määritetylle toimittajan tilille. Kun maksu kirjataan, toimittajan tiliä hyvitetään. Jos tämän asetuksen arvoksi on määritetty **Ei**, hyvitetään sen sijaan **Vuokra**-kirjaustyypille **Vuokrasopimuksen kirjausparametrit** -sivulla määritettyä tiliä. |
    | Leasing-käytäntö                       | Valitse vuokran aloituspäivämäärän käytäntö:<ul><li><b>Ei mitään</b> – Käytä vuokran alkamispäivämäärää aloituspäivänä.</li><li><b>Täysi kuukausi</b> – Käytä aloituspäivänä sen kuukauden ensimmäistä päivää, johon vuokran alkaminen sijoittuu.</li></ul><p>Jos valitset <b>Ei mitään</b> -vaihtoehdon, riskinä on, että velan kuoletuksen ja käyttöomaisuuden poiston suunnitelmat kerryttävät ja kirjaavat kuluja keskellä kuukautta kuukauden lopun sijaan. Kun valitset <b>Täysi kuukausi</b>, varmistat, että järjestelmä ottaa vuokran huomioon kuukauden ensimmäisenä päivänä ja että koko kuukauden kulut jaksotetaan ja kirjataan kuukauden viimeisenä päivänä.</p><p><strong>Huomautus:</strong> Vuokramenetelmien ominaisuus voidaan ottaa käyttöön ominaisuuksien hallinnan avulla. Etsi ja valitse <b>Ominaisuuksien hallinta</b> -työtilassa toiminto, jonka nimi on <b>Käyttöomaisuuden vuokrauksen vuokramenetelmät</b> ja valitse sitten <b>Ota käyttöön nyt</b>.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
