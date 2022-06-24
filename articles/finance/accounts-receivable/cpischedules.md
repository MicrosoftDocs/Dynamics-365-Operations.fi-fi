---
title: Kuluttajahintaindeksin aikataulu
description: Tässä artikkelissa kerrotaan, kuinka voit luoda luettelon kuluttajahintaindeksin (CPI) aikatauluista, jotka hankit Internetistä tilauslaskutuksen eskalaatiomaksun määrittämiseksi.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f08b79ee00baab3713d9ccc24a7595b1de7a7768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904870"
---
# <a name="consumer-price-index-schedule"></a>Kuluttajahintaindeksin aikataulu

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten luodaan, poistetaan, tarkistetaan ja käsitellään hintaindeksin (CPI) aikatauluja. CPI-aikataulun avulla voidaan määrittää niiden kulutustavaroiden ja -palvelujen hinnat, jotka lisätään laskutusaikataulun riveille. CPI-ajoitusta voi sitten käyttää laskutusaikataulun eskaloinnin ja alennuksen hinnoittelussa, tai se voidaan käsitellä manuaalisesti laskutusaikataulujen laskutussummien päivittämiseksi. Voit määrittää CPI-ajoituksen manuaalisesti tai voit tuoda ne käyttämällä CPI-ajoituksen yhdistelmäyksikköä.

CPI-ajoitus lisätään seuraavasti:

1. Valitse **Kuluttajahintaindeksin aikataulu** -sivulla **Uusi**.
2. Kirjoita **Kuluttajahintaindeksin aikataulu** -kenttään yksilöivä nimi.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Kuluttajahintaindeksin aikataulu** -välilehdellä **Lisää**.
5. Määritä **Hintaindeksin päivämäärä** -kentässä päivämäärä, jolloin uusi CPI-ajoitus otetaan käyttöön.
6. Kirjoita **Kuluttajahintaindeksin ajoitus** -kenttään nimi, jonka olet kirjoittanut vaiheessa 2.
7. Valitse **Tallenna**.

Voit poistaa CPI-aikataulun päivän seuraavien ohjeiden avulla.

1. Valitse **Kuluttajahintaindeksin ajoitus** -sivulla yksi tai useita rivejä, jotka haluat poistaa, ja valitse sitten **Poista**.
2. Jos haluat poistaa koko CPI-aikataulun, valitse toimintoruudusta **Poista**. Et voi poistaa valittua CPI-ajoitusta, jos se on liitetty laskutusaikatauluun.
3. Päivitä valittua CPI-ajoitusta käyttävät laskutusaikataulut valitsemalla toimintoruudusta **Prosessi**. Uusimpia CPI-päivämääriä ja aikataulusummia käytetään laskutusaikataulun hintojen päivityksessä.
4. Tarkista **Kuluttajahintaindeksiprosessi**-pikavälilehdessä päivitetyt **laskutusaikataulun numeron**, **nimiketunnuksen**, **laskutusten alkamispäivämäärän**, **laskutuspäivämäärän**, **eskalointipäivämäärän** ja **eskalointivälin** kentät.

Kun CPI-aikataulut on määritetty, niitä voidaan käyttää laskutusaikataulujen eskalointiin ja alennushintamuutoksia varten.

## <a name="cpi-calculation"></a>CPI-laskelma

Näissä esimerkeissä kausi on 1.1.2020 - 31.12.2022. Perus-CPI-hinta (CPI-arvo sopimuksen käynnistyessä) on 105,65. Nykyinen CPI on 1.1.2021 110,5. Nykyinen CPI on 1.1.2022 114,25. Alkuperäinen summa on 1 000 dollaria.

**Esimerkki 1**

Määritä **Toistuvat sopimuksen laskutusparametrit** -sivulla **Kulutushintaindeksinlaskenta** -kentän arvoksi **Perushintaindeksi**.

Kauden 1.1.2021 ensimmäinen eskalointisumma lasketaan seuraavasti alkuperäisen summan perusteella:

1 000 + (110,5 – 105,65) &divide; 105.65 &times; 1 000 = 1 045,91

Kauden 1.1.2022 ensimmäinen eskalointisumma lasketaan seuraavasti:

1 000 + (114,25 – 105,65) &divide; 105,65 &times; 1 000 = 1 081,40

**Esimerkki 2**

Määritä **Toistuvat sopimuksen laskutusparametrit** -sivulla **Kulutushintaindeksinlaskenta** -kentän arvoksi **Aiempi kulutushintaindeksi**.

Kauden 1.1.2021 ensimmäinen eskalointisumma lasketaan seuraavasti alkuperäisen summan perusteella:

1 000 + (110,5 – 105,65) &divide; 105.65 &times; 1 000 = 1 045,91

Kauden 1.1.2022 eskalointisumma lasketaan seuraavasti ensimmäisen eskalointisumman perusteella:

1 045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1 045,91 = 1 081,40

> [!NOTE]
> Eskalointiprosessissa käytetään aina viimeisintä CPI-arvoa indeksipäivästä riippumatta. Jos eskalointi on esimerkiksi syyskuussa ja viimeisimpänä CPI-arvona on heinäkuu, käytetään heinäkuun indeksiä. Syyskuun indeksin lisäämisen jälkeen ei tehdä muutoksia.

## <a name="prorated-escalation"></a>Ennustettu eskalointi

Jos eskalointi tapahtuu laskutuskauden aikana, summat on luokiteltu. Laskutuskausi voi olla esimerkiksi 1.8.2020 - 31.7.2021. CPI-päivämäärä on 1.9.2019, CPI-arvo on 244. CPI-päivämäärä on 1.9.2020, CPI-arvo on 250. Jos edellinen hinta on 1 000, kauden laskutussumma lasketaan seuraavien kaavojen avulla:

* *CPI:n muutokset* = (250 – 244) &divide; 244 = 2,459 %
* *Kuluva päivämäärä* = 1 000 &times; 2,459 % = 1 024,59
* *Nykyisen kurssin päivien määrä* = 31.7.2021 – 1. syyskuuta 2020 = 334
* *Edellinen summa* = 1 000
* *Edellisen kurssin päivien määrä* = 31.8.2020 – 1.8.2020 = 31
* *Laskutuskauden päivien kokonaismäärä* = 31.7.2021 – 1.8.2020 + 1 = 365
* *Tämän kauden laskutussumma* = (1 000 &times; 31 &divide; 365) + (1 024,59 &times; 334 &divide; 365) = 1 022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Eskalointi, joka käyttää CPI:tä ja prosenttiarvoa

Eskalointi voidaan tehdä käyttämällä CPI:tä. CPI sekä 3 prosentin eskalointi alkaa 1.1.2020, ja sillä on vuosittainen tiheys.

- Summa, joka laskutetaan 1.1.2019 - 31.12.2020, on 4 000.
- Laskutuskausi, joka eskaloituu, on 1.1.2020 - 31.12.2020.
- CPI-päivämäärä on 1.12.2018, CPI-arvo on 205,3. CPI-päivämäärä on 1.12.2018, CPI-arvo on 219,6.

Jos edellinen hinta on 4 000, tämän kauden laskutussumma lasketaan seuraavasti:

- *CPI:n muutokset* = (219.6 – 205.3) &divide; 205.3 = 6,965 %
- *Kuluva päivämäärä* = (4 000 &times; 6,965 %) – 4 000 = 278,60
- *Prosenttiluvun muutokset* = (4 000 &times; 1,03) – 4 000 = 120
- *Laskutussumma* = 4 000 + 278,6 + 120 = 4 398,6
