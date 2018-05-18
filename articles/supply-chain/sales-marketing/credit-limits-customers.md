---
title: Asiakkaiden luottorajat
description: "Tässä artikkelissa on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin luottorajojen yleiskatsaus."
author: omulvad
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e00828ea24434da6dfd7443153b007ea728375f3
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="credit-limits-for-customers"></a>Asiakkaiden luottorajat

[!include [banner](../includes/banner.md)]

Voit määrittää asiakkaillesi myönnettävän luoton asettamalla luottorajoja. Jos olet määrittänyt luottorajan, se tarkistetaan automaattisesti, kun käyttäjä yrittää päivittää asiakirjan. Jos luottoraja ylittyy, käyttäjälle näytetään sanoma. Tämä artikkeli on yleiskatsaus luottorajojen toimintaan, ja se vastaa seuraaviin kysymyksiin:

-   Mitä tiedostoja ja prosesseja voin käyttää luottorajojen tarkistamiseen?

-   Missä määritetään asiakkaan jäljellä olevan luoton laskentatapa?

-   Missä asiakkaan jäljellä olevan luoton tietoja käytetään?

-   Missä määritän, tarvitaanko luoton antamiseen asiakkaalle asiakkaan tunnistusta, ja mikä on luottorajan määrä, jolla tunnistus tarvitaan?

-   Missä määritän, näytetäänkö varoitus tai virhe, jos luottoraja on ylitetty?

-   Miten määritän luottorajan tietylle asiakkaalle?

-   Miten tarkistan luottorajan manuaalisesti myyntitilauksissa?

**Mitä tiedostoja ja prosesseja voin käyttää luottorajojen tarkistamiseen?**

Voit määrittää asiakirjat, joille luottoraja tarkistetaan **Myyntireskontran parametrit** -lomakkeessa. Sinulla on oltava järjestelmänvalvojan (-SYSADMIN-) käyttöoikeusrooli, jotta voit tehdä muutoksia tähän lomakkeeseen. Voit tarkistaa luottorajan seuraaville tiedostoille ja prosesseille:

-   Myyntitilausten laskut, kun laskut kirjataan.

-   Myyntitilausten pakkausluettelot, kun pakkausluettelot päivitetään.

-   Myyntitilaukset, kun niihin lisätään rivejä **Myyntitilaus**-lomakkeella

-   Myyntitilaukset, kun ne luodaan palvelun kautta

-   Vapaatekstilaskut, kun laskut kirjataan

Luottorajat tarkistetaan automaattisesti, jos jompikumpi seuraavista vaihtoehdoista on käytössä:

-   Jos **Myyntireskontran parametrit** -lomakkeen **Luottorajan tyyppi** -kenttä on asetettu arvoon, joka ei ole **Ei mitään**. Luottorajat tarkistetaan kaikilta asiakkailta.

-   **Myyntireskontran parametrit** -lomakkeen **Luottorajan tyyppi** -kentän arvo on **Ei mitään**, mutta **Pakollinen luottoraja** on valittuna **Asiakkaat**-lomakkeessa olevalle asiakkaalle. Luottorajat tarkistetaan vain tietyiltä asiakkailta.

Jos haluat tarkistaa luottorajan seuraavien tiedostojen yhteydessä, sinun on määritettävä lisäasetuksia.

|    Asiakirja                                    |    Lisäasetus                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Vapaatekstilasku                         |    Valitse Myyntireskontran parametrit -lomakkeen Luottokelpoisuusluokitus-alueella Tarkista vapaatekstilaskun luottoraja.     |
|    Myyntitilaus (manuaalisesti)            |    Valitse Myyntireskontran parametrit -lomakkeen Luottokelpoisuusluokitus-alueella Tarkista myyntitilauksen luottoraja.           |
|    Myyntitilaus (sähköisessä muodossa vastaanotetut)     |    Valitse Myyntireskontran parametrit -lomakkeen AIF-alueella Tarkista myyntitilauksen luottoraja.                     |

**Missä määritetään asiakkaan jäljellä olevan luoton laskentatapa?**

Voit määrittää Dynamics 365:n laskemaan asiakkaan jäljellä olevan luoton seuraavilla tavoilla:

-   Luottorajaa verrataan asiakkaan saldoon.

-   Luottorajaa verrataan asiakkaan saldoon ja pakkausluettelon summiin.

-   Luottorajaa verrataan asiakkaan saldoon ja kaikkiin avoimiin tapahtumatehtäviin. Tämä sisältää pakkausluetteloiden ja myyntitilausten summat.

Määritä verrattavat tiedot **Myyntireskontran parametrit** -lomakkeessa. Sinulla on oltava järjestelmänvalvojan (-SYSADMIN-) käyttöoikeusrooli, jotta voit tehdä muutoksia tähän lomakkeeseen. Valitse **Luottorajan tyyppi** -kentässä suoritetaanko luottorajan tarkistukset, ja mitä tapahtumatietoja luottorajan tarkistukseen sisältyy. Valitse seuraavista vaihtoehdoista:

-   **Ei mitään** – luottorajoja ei tarkisteta. Voit korvata vaihtoehdon yksittäisille asiakkaille valitsemalla **Pakollinen luottoraja** -valintaruudun **Asiakkaat**-lomakkeessa. Kun teet näin, luottorajaa verrataan asiakkaan saldoon.

-   **Saldo** – Luottorajaa verrataan asiakkaan saldoon.

-   **Saldo + pakkausluettelo tai tuotteen vastaanotto** – luottorajaa verrataan asiakkaan saldoon ja toimituksiin.

-   **Saldo+Kaikki** – Luottorajaa verrataan asiakkaan saldoon, toimituksiin ja avoimiin tilauksiin.

**Missä asiakkaan jäljellä olevan luoton tietoja käytetään?**

Tiedot asiakkaan saldosta ja jäljellä olevasta luoton määrästä lasketaan ja tallennetaan, kun luot erääntymistilannevedoksen, ja ne näytetään **Perintä**-lomakkeella. Summat, jotka näytetään **Perintä**-lomakkeella eivät välttämättä sisällä kaikkia tapahtumatehtäviä ennen uuden erääntymistilannevedoksen luontia. Lisätietoja on kohdassa [Luotto ja perintä myyntireskontrassa](https://technet.microsoft.com/en-us/library/hh209221.aspx).

Tiedot asiakkaan saldosta ja luoton määrästä lasketaan valittujen asiakirjojen mukaan, kun myyntitilauksia, pakkausluetteloita ja asiakkaan laskuja päivitetään. Jos käsiteltävän asiakirjan summa aiheuttaa luottorajan ylittymisen, järjestelmä näyttää varoitusviestin.

**Missä määritän, tarvitaanko luoton antamiseen asiakkaalle asiakkaan tunnistusta, ja mikä on luottorajan määrä, jolla tunnistus tarvitaan?**

Voit määrittää tunnistusvaatimuksen ja siihen tarvittavan luottorajan määrän **Myyntireskontran parametrit** -lomakkeella.
Sinulla on oltava järjestelmänvalvojan (-SYSADMIN-) käyttöoikeusrooli, jotta voit tehdä muutoksia tähän lomakkeeseen.

|    Kenttä                                    |    kuvaus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Edellytä tunnistus luoton yhteydessä     |    Valitse niille asiakkaille määritettävän tunnistuksen tyyppi, joille yritys myöntää luottoa. Tässä kentässä valittu vaihtoehto määrittää, milloin ja mitä tietoja on määritettävä Asiakkaat-lomakkeen Valtion antama tunnus -kenttiin:	Ei – Viranomaisten myöntämää tunnusta ei edellytetä asiakkaan luottorajasta riippumatta.     Kyllä – Viranomaisten myöntämä tunnus edellytetään, jos asiakkaan luottoraja on suurempi tai yhtä suuri kuin nolla.     Vähimmäisraja – Viranomaisten myöntämä tunnus edellytetään, jos asiakkaan luottoraja on suurempi tai yhtä suuri kuin tämän lomakkeen Raja-kenttään määritetty arvo.        |
|    Raja                                    |    Kirjoita luottoraja, jonka ylityttyä asiakkailta edellytetään viranomaisten myöntämää tunnusta.    Kirjoita esimerkiksi 2 000, jos haluat, että asiakkailta, joiden luottoraja on suurempi kuin 2 000, edellytetään tunnusta.    Tämä kenttä on käytettävissä, jos olet valinnut Vähimmäisraja-vaihtoehdon Edellytä tunnus luoton yhteydessä -kentässä.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Missä määritän, näytetäänkö varoitus tai virhe, jos luottoraja on ylitetty?**

Määritä **Myyntireskontran parametrit** -lomakkeessa, näytetäänkö varoitus vai virhe, kun luottoraja ylittyy. Varoitus- tai virhesanoma tulee näkyviin, kun käyttäjä syöttää tai kirjaa tietoa, tai tieto sisältyy lokiin, jos tiedostot käsitellään sähköisessä palvelussa. Sinulla on oltava järjestelmänvalvojan (-SYSADMIN-) käyttöoikeusrooli, jotta voit tehdä muutoksia tähän lomakkeeseen.

|    Kenttä                                                               |    kuvaus                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Sanoma luottorajan ylittyessä (Luottokelpoisuusluokitus-alueella)     |    Valitse, miten viestit luottorajojen ylittymisestä näytetään käyttäjille. Valitse jokin seuraavista vaihtoehdoista:	Virhe – järjestelmä näyttää virhesanoman. Tämä yleensä pysäyttää nykyisen toiminnon ja ongelma on ratkaistava, ennen kuin toimintoja voi jatkaa.     Varoitus – Näytetään varoitussanoma, mutta prosessi voi jatkua.                     |
|    Sanoma luottorajan ylittyessä (AIF-alueella)               |    Valitse, kuinka luottorajan ylitystä koskevat sanomat toimitetaan lokiin: Valitse jokin seuraavista vaihtoehdoista:	Virhe – Poikkeukset-lomakkeessa näytetään virhesanoma, ja asiakirjan käsittely keskeytyy, kunnes virhe on ratkaistu.     Varoitus – Poikkeukset-lomakkeessa näytetään varoitussanoma, mutta prosessi voi jatkua.        |

**Miten määritän luottorajan määrän tietylle asiakkaalle?**

Voit määrittää luottorajan määrän tietylle asiakkaalle **Asiakkaat**-lomakkeessa. Sinulla on oltava käyttöoikeusrooli, jolla on Ylläpidä asiakkaiden päätietoja (CustCustomersMaintain) -velvollisuus, jotta voit tehdä muutoksia lomakkeeseen.

1.  Valitse **Myyntireskontra** \> **Yleinen** \> **Asiakkaat** \> **Kaikki asiakkaat**. Kaksoisnapsauta asiakastiliä.

2.  Valitse **Asiakkaat**-lomakkeen toimintoruudusta **Muokkaa**.

3.  Anna **Luottoraja** -kenttään summa. Tämän arvon on oltava suurempi kuin nolla (0); sitä käytetään luottorajan määränä.

4.  Jos sitä edellytetään, anna viranomaisten myöntämä tunnus **Valtion antama tunnus** -kenttään.

> [!NOTE]
> **Luottorajatyyppi myyntireskontran parametrit** -lomakkeessa valitaan yleensä luottorajan tyyppi. Jos luottorajan tyypiksi on kuitenkin valittu **Ei rajaa**, **Pakollinen luottoraja** -valintaruutu **Asiakkaat**-lomakkeessa on valittava, jotta asiakkaan luottorajaa voi verrata asiakkaan saldoon. Lisätietoja luottorajan tyypeistä on ”Mitä tiedostoja ja prosesseja voin käyttää luottorajojen tarkistamiseen?" tässä ohjeaiheessa. 

**Miten tarkistan luottorajan manuaalisesti myyntitilauksissa?**

Voit joutua tarkistamaan asiakkaan luottorajan manuaalisesti. Voit esimerkiksi tarkistaa asiakkaan luottorajan manuaalisesti ennen myyntitilauksen täyttämistä. Luottorajan voi tarkistaa manuaalisesti **Myyntitilaus** -lomakkeessa. Sinulla on oltava käyttöoikeusrooli, jolla on Ylläpidä myyntitilauksia (SalesOrderMaintain) -velvollisuus, jotta voit tehdä muutoksia lomakkeeseen.

1.  Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**. Kaksoisnapsauta myyntitilausta.

2.  Valitse **Myyntitilaus**-lomakkeen toimintoruudun **Hallinta**-välilehdessä **Luottorajan tarkistus**.

