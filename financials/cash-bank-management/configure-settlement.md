---
title: Tilin konfiguroiminen
description: "Tapahtumien tilityksen ajankohdan ja tavan määrittäminen voi olla monimutkaista, joten on tärkeää, että parametrit ymmärretään ja määritetään oikein. Näin ne vastaavat liiketoimintatarpeita. Tässä artikkelissa esitellään parametrit, joita käytetään ostoreskontran ja myyntireskontran tilityksessä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 059513de66827aa3a839b9eb06973ec4c1549f73
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Tilin konfiguroiminen
<a id="configure-settlement" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tapahtumien tilityksen ajankohdan ja tavan määrittäminen voi olla monimutkaista, joten on tärkeää, että parametrit ymmärretään ja määritetään oikein. Näin ne vastaavat liiketoimintatarpeita. Tässä artikkelissa esitellään parametrit, joita käytetään ostoreskontran ja myyntireskontran tilityksessä. 

Seuraavat parametrit vaikuttavat siihen, kuinka tilityksiä käsitellään Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa. Tilitys on prosessi, jossa selvitetään lasku maksua tai hyvityslaskua vastaan. Nämä parametrit sijaitsevat **Tilityksen** alueella **Myyntireskontran parametrit** ja **Ostoreskontran parametrit** -sivuilla.

-   **Automaattinen tilitys** – Aseta asentoon **Kyllä** jos tapahtuma tulisi selvittää automaattisesti muita avoimia tapahtumia vastaan kirjauksen yhteydessä. Jos asetukseksi on määritetty asentoon **Ei**, käyttäjät voivat selvittää tapahtumat manuaalisesti maksujen syöttämisen yhteydessä tai myöhemmin käyttäen **Tapahtumat selvitetään**-sivulla.
-   **Käteisalennuksen hallinta** – Määritä kuinka [käteisalennusta käsitellään, kun laskua on maksettu liikaa](cash-discount-handling-overpayments.md). Ylimaksulle käteisalennus voidaan vähentää, sitä voidaan käsitellä erotuksena tai se voi jäädä asiakkaan tai toimittajan tilille.
    -   **Yksilöimättömät** – Käteisalennussummasta vähennetään yli maksettu summa. Järjestelmä toimii näin aina, riippumatta siitä, onko liikamaksun summa suurempi vai pienempi kuin summa, joka on syötetty **Liian vähän / liian paljon maksetun summan enimmäismäärä** -kenttään.
    -   **Erityinen** – Liikamaksun summa kirjataan joko käteisalennuksen eron kirjanpitotilille tai säilytetään saldona asiakkaan tilillä. Erityinen toiminta riippuu siitä, onko liikamaksun summa 0,00:n ja syötetyn summan välillä **Liikaa / liian vähän maksetun summan enimmäismäärä** -kentässä, vai onko liikamaksun summa suurempi kuin **Liikaa / liian vähän maksetun summan enimmäismäärä** -summa.
-   **Suurin mahdollinen pyöristysero** – Syötä suurin sallittu maksettujen tapahtumien suoritusten pyöristysero. Jos pyöristysero on sama tai pienempi kuin tässä kentässä määritetty pyöristysero, se kirjataan kirjanpidon pyöristyserotilille, joka on määritetty **Automaattisten tapahtumien tilit**-sivulla.
-   **Liikaa tai liian vähän maksetun summan enimmäismäärä** – Syötä summa, joka hyväksytään liikaa tai liian vähän maksetuksi summaksi. Voit laskea liikaa tai liian vähän maksetun summan veron valitsemalla **Kirjanpitoparametrit**-sivun, klikkaamalla **Arvonlisävero** ja sitten valitsemalla **Liikaa / liian vähän maksettujen summien arvonlisävero** -vaihtoehdon.
    -   Jos liikaa tai liian vähän maksetun summan pyöristysero on pienempi kuin pyöristysero, joka on määritetty **Suurin pyöristysero** -kentässä, pyöristyserosumma kirjataan pyöristyserotilille.
    -   Jos liikaa tai liian vähän maksetun summan pyöristysero on suurempi kuin pyöristysero, joka on määritetty **Suurin pyöristysero** -kentässä pyöristyserosumma kirjataan pyöristyserotilille, joka valitaan **Asiakkaan käteisalennus** tai **Toimittajan käteisalennus** kirjaustyyppiin **Automaattisten tapahtumien tilit** -sivulle.
-   **Laske käteisalennukset osamaksuille** – Aseta tämä vaihtoehto asentoon **Kyllä** salliaksesi käteisalennuksien automaattinen laskemisen osittaisille maksuille.
    -   Tämän vaihtoehdon vaikutus riippuu **Käytä käteisalennusta** -kentän arvosta **Tapahtumien maksu** -sivulla. Jos asetukseksi on määritetty asentoon **Kyllä**, alennus otetaan, kun **Käytä käteisalennusta** -kenttä on laitettu **Normaali**-asentoon. Kun **Käytä käteisalennusta** -kentän arvoksi tulee **Aina**, käteisalennus otetaan aina, tämän kentän asetuksista riippumatta. Kun **Käytä käteisalennusta** -kentän arvoksi tulee **Ei koskaan**, käteisalennusta ei oteta koskaan, tämän kentän asetuksista riippumatta.
    -   Jos tämä vaihtoehto on asetettu kohtaan **Kyllä** ja käyttäjä muuttaa arvon **Tilitettävä summa** -kentässä **Tilitä tapahtumat**-sivulla, alennus lasketaan automaattisesti ja näytetään oletusarvona **Käytettävä käteisalennussumma** -kentässä.
    -   Jos tämä vaihtoehto on asetettu **Ei**-asentoon ja käyttäjä muuttaa arvon **Tilitettävä summa** -kentässä **Tilitä tapahtumat** -sivulla, oletusarvo **Käytettävä käteisalennussumma** -kentässä on **0** (nolla).
-   **Laske käteisalennukset hyvityslaskuille** – Aseta tämä vaihtoehto **Kyllä**-asentoon, jotta käteisalennus hyvityslaskuille lasketaan automaattisesti. Myyntireskontrassa hyvityslaskutapahtuma on negatiivinen tapahtuma, jolla on arvo **Lasku**-kentässä **Vapaatekstilasku**-sivulla tai palautus **Myyntitilaus** -sivulla.
    -   Tämän vaihtoehdon vaikutus riippuu **Käytä käteisalennusta** -kentän arvosta **Tapahtumien maksu** -sivulla. Jos asetukseksi on määritetty asentoon **Kyllä**, alennus otetaan, kun ****Käytä käteisalennusta**** -kenttä on laitettu **Normaali**-asentoon. Kun ****Käytä käteisalennusta**** -kentän arvoksi tulee **Aina**, käteisalennus otetaan aina, tämän kentän asetuksista riippumatta. Kun ****Käytä käteisalennusta**** -kentän arvoksi tulee **Ei koskaan**, käteisalennusta ei oteta koskaan, tämän kentän asetuksista riippumatta.
    -   Jos tämä vaihtoehto on asetettuna **Kyllä**-asentoon ja hyvityssumma on merkitty **Tilitä tapahtumat** -sivulla, alennus lasketaan automaattisesti ja näytetään oletusarvona **Käytettävä käteisalennussumma** -kentässä.
    -   Jos tämä vaihtoehto on asetettu **Ei**-asentoon ja hyvityslasku on merkitty **Tilitä avoimet tapahtumat**-sivulla, oletusarvo **Käytettävä käteisalennussumma** kenttä on **0** (nolla).
-   **Alennus vastatilit (vain ostoreskontran)** – Määritä oletusarvoinen käteisalennuksen kirjanpitotili, jota tulee käyttää kirjanpidon käteisalennusten kohteille.
    -   **Päätilin käytetään toimittaja-alennuksille** – Käteisalennus kirjataan päätiliin, joka on määritetty **Käteisalennuksen asetukset** -sivulla.
    -   **Laskurivien tilit** – Käteisalennus kirjataan kirjanpitotileille alkuperäiseen laskuun.
-   **Merkitse rivit vapaatekstilaskuihin ja korkolaskuille (vain AR)** – Asetukseksi **Kyllä** käyttääksesi **Merkitse laskurivit** -painike **Asiakasmaksujen syöttäminen** -sivulla, **Kirjauskansion tosite-**, ja **Tilitä tapahtumat** -sivuilla. Tämän painikkeen avulla käyttäjät voivat merkitä yksittäisiä rivejä tilitystä varten.
-   **Priorisoi tilitystä (vain AR)** – Asetukseksi **Kyllä** käyttääksesi **Merkitse prioriteetin mukaan** -painiketta **Syötä asiakasmaksut** ja **Tilitä tapahtumat** -sivuilla. Tämän painikkeen avulla käyttäjät voivat liittää esimääritetyn selvitysjärjestyksen tapahtumiin.  Kun tilitysjärjestys on otettu käyttöön tapahtumassa, järjestystä ja maksun kohdistusta voidaan muokata ennen kirjausta.
-   **Käytä automaattisten selvitysten priorisointia** – Määritä tämän asetuksen arvoksi **Kyllä**, käyttääksesi määritettyä priorisointijärjestystä, kun tapahtumia selvitetään automaattisesti. Tämä kenttä on käytettävissä vain, jos **Priorisoi selvitys**- ja **Automaattinen tilitys** -asetukset on määritetty arvoon **Kyllä**.





