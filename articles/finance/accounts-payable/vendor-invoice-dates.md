---
title: Toimittajan laskujen päivämäärät
description: Tässä artikkelissa kuvataan toimittajan laskuissa näkyvät päivämäärät. Artikkelissa kerrotaan myös, miten kirjauspäivämäärää oikaistaan automaattisesti.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775265"
---
# <a name="vendor-invoice-dates"></a>Toimittajan laskujen päivämäärät

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan toimittajan laskuissa näkyvät päivämäärät. Artikkelissa kerrotaan myös, miten kirjauspäivämäärää oikaistaan automaattisesti.

**Odotetaan toimittajan laskutietoja** -sivulla laskun otsikossa näkyy neljä päivämäärää: **laskun vastaanottopäivä**, **laskutuspäivä**, **kirjauspäivä** ja **eräpäivä**. Kun toimittajan lasku luodaan, seuraavat päivämäärät täytetään oletusarvoisesti:

- **Laskun vastaanottopäivä** – Tämän kentän arvoksi tulee järjestelmän kulloinenkin päivämäärä.
- **Kirjauspäivä** – Tämän kentän arvoksi tulee järjestelmän kulloinenkin päivämäärä. 
- **Eräpäivä** – Tämän kentän päivämäärä lasketaan kirjauspäivän ja maksuehtojen perusteella.
- **Laskutuspäivä** – Oletusarvoisesti tämä kenttä on tyhjä. Voit kuitenkin syöttää arvon tarpeen mukaan. Tällöin **Eräpäivä**-kentän päivämäärä lasketaan uudelleen laskutuspäivän ja maksuehtojen perusteella.

Joskus toimittajan lasku voi olla odottavassa tilassa kauan jakson sulkemisen jälkeen. Kun se on valmis kirjattavaksi, käytetään edelleen edellisen kirjausjakson vanhaa kirjauspäivää. Tämä jakso on kuitenkin nyt suljettu. Siksi ostoreskontran käsittelijän on muutettava kaikki kirjauspäivät manuaalisesti uudelle kirjausjaksolle kaikkien odottavien laskujen osalta, jotka on luotu aiemmin.

Tässä artikkelissa kuvatun ominaisuuden avulla voit automaattisesti oikaista kirjauspäivää liiketoimintavaatimusten mukaisesti.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Toimittajan laskun kirjauspäivän automaattisen oikaisemisen parametri

Näiden vaiheiden avulla toimittajien laskujen kirjauspäivä voidaan oikaista automaattisesti.

1.  Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.
2.  Valitse **Kirjanpito- ja arvonlisävero** -välilehden kentässä **Oikaise kirjauspäivä automaattisesti** jokin seuraavista arvoista:

    - **Ei muutosta** – Järjestelmä ei muuta kirjauspäivää automaattisesti kirjauksen aikana. Tämä arvo on valittuna oletusarvoisesti.
    - **Vaihda kirjauspäivä aina järjestelmän päivämääräksi** – Kirjauspäivä muutetaan automaattisesti järjestelmän päivämääräksi kirjauksen yhteydessä.
    - **Muuta kirjauspäivä järjestelmän päivämääräksi, kun kirjauspäiväjakso suljetaan tai asetetaan pitoon** – Kirjauspäivän muutetaan automaattisesti järjestelmän kirjauspäiväksi kirjauksen yhteydessä, mutta vain, jos kirjauspäivän vastaavan jakson tila on **Suljettu** tai **Pidossa**.
    - **Muuta kirjauspäivä uuden jakson ensimmäiseksi päivämääräksi, kun kirjauspäiväjakso suljetaan tai asetetaan pitoon** – Kirjauspäivä muutetaan uuden avoimen jakson ensimmäiseksi päiväksi kirjauksen yhteydessä, mutta vain, jos kirjauspäivän vastaavan jakson tila on **Suljettu** tai **Pidossa**.

> [!NOTE]
> Jos automaattisesti oikaistu kirjauspäivämäärä kuuluu uuteen tilikauteen, laskun kirjauspäivämäärää ei päivitetä. Käyttäjä saa virhesanoman "Tilikausi on vaihtunut. Tarkista kirjauspäivämäärä ja lisää se uudelleen." Laskun kirjauspäivämäärä on päivitettävä uuteen tilikauden päivämäärään kirjausta varten.

## <a name="impact-of-posting-date-changes"></a>Kirjauspäivän muutosten vaikutukset

Kun odottavan toimittajan laskun kirjauspäivää muutetaan, muutos vaikuttaa seuraavasti:

- **Määräpäivä**

    - Jos **Laskutuspäivä**-kenttä on tyhjä, eräpäivä lasketaan uudelleen uuden kirjauspäivän ja maksuehtojen perusteella.
    - Jos **Laskutuspäivä**-kenttä on määritetty aiemmin, kirjauspäivä ei vaikuta eräpäivään.

- **Käteisalennuksen päivämäärä**

    - Jos **Laskutuspäivä**-kenttä on tyhjä, uutta kirjauspäivää käytetään käteisalennuksen laskemiseen.
    - Jos **Laskutuspäivämäärä**-kenttä on määritetty aiemmin, käteisalennus ei muutu.

- **Vaihtokurssi** – Vaihtokurssin päivämäärä määräytyy **Ostoreskontran** parametrit -sivun **Lasku**-välilehden **Päivitä toimittajan kirjanpito käyttäen laskutuspäivää** -asetuksen arvon mukaan (**Ostoreskontra \> Määritys \> Ostoreskontran parametrit**).

    - Jos asetuksen arvona on **Kyllä**, käytetään **laskutuspäivää**, jolloin **kirjauspäivä** ei vaikuta vaihtokurssiin.
    - Jos asetuksen arvona on **Ei**, kirjauspäivää käytetään vaihtokurssin laskemiseen. Kun kirjauspäivä päivitetään, kirjanpito- ja raportointisummat lasketaan uudelleen. Siksi täsmäytyksen vahvistus on suoritettava uudelleen.

## <a name="validation"></a>Oikeellisuustarkistus

Kaksi muuta **Ostoreskontran parametrit** -sivun **Lasku**-välilehden kenttää (**Ostoreskontra \> Määritys \>Ostoreskontran parametrit**) vaikuttaa laskun käsittelyyn:

- Jos **Tarkista käytetty laskunumero** -kentän arvoksi on määritetty **Hylkää kaksoiskappaleet tilikauden sisällä**, käytetään kirjauspäivää laskujen kaksoiskappaleiden etsimiseen laskun kirjauksen yhteydessä.
- Jos **Vaadi asiakirjan päiväys toimittajan laskussa** -kentän arvoksi on määritetty **Virhevaihtoehto**, **Laskutuspäivä odottavan laskun otsikossa** -kenttää edellytetään. Jos laskutuspäivä on kirjauspäivää myöhemmin, näytetään virhesanoma.
