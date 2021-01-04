---
title: Tilin konfiguroiminen
description: Tapahtumien tilityksen ajankohdan ja tavan määrittäminen voi olla monimutkaista, joten on tärkeää, että parametrit ymmärretään ja määritetään oikein. Näin ne vastaavat liiketoimintatarpeita. Tässä aiheessa esitellään parametrit, joita käytetään ostoreskontran ja myyntireskontran tilityksessä.
author: kweekley
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 094b8876b3b10b6dcbc0ce399a1a9915271459ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442908"
---
# <a name="configure-settlement"></a>Tilin konfiguroiminen

[!include [banner](../includes/banner.md)]

Tapahtumien tilityksen ajankohdan ja tavan määrittäminen voi olla monimutkaista, joten on tärkeää, että parametrit ymmärretään ja määritetään oikein. Näin ne vastaavat liiketoimintatarpeita. Tässä aiheessa esitellään parametrit, joita käytetään ostoreskontran ja myyntireskontran tilityksessä. 

Seuraavat parametrit vaikuttavat siihen, kuinka tilityksiä käsitellään Microsoft Dynamics 365 Financessa. Tilitys on prosessi, jossa selvitetään lasku maksua tai hyvityslaskua vastaan. Nämä parametrit sijaitsevat **Tilityksen** alueella **Myyntireskontran parametrit** ja **Ostoreskontran parametrit** -sivuilla.

- **Automaattinen tilitys** – Aseta asentoon **Kyllä** jos tapahtuma tulisi selvittää automaattisesti muita avoimia tapahtumia vastaan kirjauksen yhteydessä. Jos asetukseksi on määritetty asentoon **Ei**, käyttäjät voivat selvittää tapahtumat manuaalisesti maksujen syöttämisen yhteydessä tai myöhemmin käyttäen **Tapahtumat selvitetään**-sivulla.
- **Käteisalennuksen hallinta** – Määritä kuinka [käteisalennusta käsitellään, kun laskua on maksettu liikaa](cash-discount-handling-overpayments.md). Ylimaksulle käteisalennus voidaan vähentää, sitä voidaan käsitellä erotuksena tai se voi jäädä asiakkaan tai toimittajan tilille.
  -   **Yksilöimättömät** – Käteisalennussummasta vähennetään yli maksettu summa. Järjestelmä toimii näin aina, riippumatta siitä, onko liikamaksun summa suurempi vai pienempi kuin summa, joka on syötetty **Liian vähän / liian paljon maksetun summan enimmäismäärä** -kenttään.
  -   **Erityinen** – Liikamaksun summa kirjataan joko käteisalennuksen eron kirjanpitotilille tai säilytetään saldona asiakkaan tilillä. Erityinen toiminta riippuu siitä, onko liikamaksun summa 0,00:n ja syötetyn summan välillä **Liikaa / liian vähän maksetun summan enimmäismäärä** -kentässä, vai onko liikamaksun summa suurempi kuin **Liikaa / liian vähän maksetun summan enimmäismäärä** -summa.
- **Suurin mahdollinen pyöristysero** – Syötä suurin sallittu maksettujen tapahtumien suoritusten pyöristysero. Jos pyöristysero on sama tai pienempi kuin tässä kentässä määritetty pyöristysero, se kirjataan kirjanpidon pyöristyserotilille, joka on määritetty **Automaattisten tapahtumien tilit**-sivulla.
- **Liikaa tai liian vähän maksetun summan enimmäismäärä** – Syötä summa, joka hyväksytään liikaa tai liian vähän maksetuksi summaksi. Voit laskea liikaa tai liian vähän maksetun summan veron valitsemalla **Kirjanpitoparametrit**-sivun, klikkaamalla **Arvonlisävero** ja sitten valitsemalla **Liikaa / liian vähän maksettujen summien arvonlisävero** -vaihtoehdon.
  -   Jos liikaa tai liian vähän maksetun summan pyöristysero on pienempi kuin pyöristysero, joka on määritetty **Suurin pyöristysero** -kentässä, pyöristyserosumma kirjataan pyöristyserotilille.
  -   Jos liikaa tai liian vähän maksetun summan pyöristysero on suurempi kuin pyöristysero, joka on määritetty **Suurin pyöristysero** -kentässä pyöristyserosumma kirjataan pyöristyserotilille, joka valitaan **Asiakkaan käteisalennus** tai **Toimittajan käteisalennus** kirjaustyyppiin **Automaattisten tapahtumien tilit** -sivulle.
- **Laske käteisalennukset osamaksuille** – Aseta tämä vaihtoehto asentoon **Kyllä** salliaksesi käteisalennuksien automaattinen laskemisen osittaisille maksuille.
  -   Tämän vaihtoehdon vaikutus riippuu **Käytä käteisalennusta** -kentän arvosta **Tapahtumien maksu** -sivulla. Jos asetukseksi on määritetty asentoon **Kyllä**, alennus otetaan, kun **Käytä käteisalennusta** -kenttä on laitettu **Normaali**-asentoon. Kun **Käytä käteisalennusta** -kentän arvoksi tulee **Aina**, käteisalennus otetaan aina, tämän kentän asetuksista riippumatta. Kun **Käytä käteisalennusta** -kentän arvoksi tulee **Ei koskaan**, käteisalennusta ei oteta koskaan, tämän kentän asetuksista riippumatta.
  -   Jos tämä vaihtoehto on asetettu kohtaan **Kyllä** ja käyttäjä muuttaa arvon **Tilitettävä summa** -kentässä **Tilitä tapahtumat**-sivulla, alennus lasketaan automaattisesti ja näytetään oletusarvona **Käytettävä käteisalennussumma** -kentässä.
  -   Jos tämä vaihtoehto on asetettu **Ei**-asentoon ja käyttäjä muuttaa arvon **Tilitettävä summa** -kentässä **Tilitä tapahtumat** -sivulla, oletusarvo **Käytettävä käteisalennussumma** -kentässä on **0** (nolla).
- **Laske käteisalennukset hyvityslaskuille** – Aseta tämä vaihtoehto **Kyllä**-asentoon, jotta käteisalennus hyvityslaskuille lasketaan automaattisesti. Myyntireskontrassa hyvityslaskutapahtuma on negatiivinen tapahtuma, jolla on arvo **Lasku**-kentässä **Vapaatekstilasku**-sivulla tai palautus **Myyntitilaus** -sivulla.
  - Tämän vaihtoehdon vaikutus riippuu <strong>Käytä käteisalennusta</strong> -kentän arvosta <strong>Tapahtumien maksu</strong> -sivulla. Jos asetukseksi on määritetty <strong>Kyllä</strong>, alennus otetaan, kun *<strong><em>Käytä käteisalennusta</em></strong>* -kentässä on valittu <strong>Normaali</strong>. Kun *<strong><em>Käytä käteisalennusta</em></strong>* -kentässä valitaan <strong>Aina</strong>, käteisalennus otetaan aina tämän kentän asetuksista riippumatta. Kun *<strong><em>Käytä käteisalennusta</em></strong>* -kentässä valitaan <strong>Ei koskaan</strong>, käteisalennusta ei oteta koskaan tämän kentän asetuksista riippumatta.
  - Jos tämä vaihtoehto on asetettuna **Kyllä**-asentoon ja hyvityssumma on merkitty **Tilitä tapahtumat** -sivulla, alennus lasketaan automaattisesti ja näytetään oletusarvona **Käytettävä käteisalennussumma** -kentässä.
  - Jos tämä vaihtoehto on asetettu **Ei**-asentoon ja hyvityslasku on merkitty **Tilitä avoimet tapahtumat**-sivulla, oletusarvo **Käytettävä käteisalennussumma** kenttä on **0** (nolla).

- **Alennus vastatilit (vain ostoreskontran)** – Määritä oletusarvoinen käteisalennuksen kirjanpitotili, jota tulee käyttää kirjanpidon käteisalennusten kohteille.
  -   **Päätilin käytetään toimittaja-alennuksille** – Käteisalennus kirjataan päätiliin, joka on määritetty **Käteisalennuksen asetukset** -sivulla.
  -   **Laskurivien tilit** – Käteisalennus kirjataan kirjanpitotileille alkuperäiseen laskuun.
- **Merkitse rivit vapaatekstilaskuihin ja korkolaskuille (vain AR)** – Asetukseksi **Kyllä** käyttääksesi **Merkitse laskurivit** -painike **Asiakasmaksujen syöttäminen** -sivulla, **Kirjauskansion tosite-**, ja **Tilitä tapahtumat** -sivuilla. Tämän painikkeen avulla käyttäjät voivat merkitä yksittäisiä rivejä tilitystä varten.
- **Priorisoi tilitystä (vain AR)** – Asetukseksi **Kyllä** käyttääksesi **Merkitse prioriteetin mukaan** -painiketta **Syötä asiakasmaksut** ja **Tilitä tapahtumat** -sivuilla. Tämän painikkeen avulla käyttäjät voivat liittää esimääritetyn selvitysjärjestyksen tapahtumiin.  Kun tilitysjärjestys on otettu käyttöön tapahtumassa, järjestystä ja maksun kohdistusta voidaan muokata ennen kirjausta.
- **Käytä automaattisten selvitysten priorisointia** – Määritä tämän asetuksen arvoksi **Kyllä**, käyttääksesi määritettyä priorisointijärjestystä, kun tapahtumia selvitetään automaattisesti. Tämä kenttä on käytettävissä vain, jos **Priorisoi selvitys**- ja **Automaattinen tilitys** -asetukset on määritetty arvoon **Kyllä**.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Myyntireskontran/ostoreskontran päätilien kiinteät dimensiot

Kun myyntireskontran/ostoreskontran päätilissä kiinteitä dimensioita käytetään, lisäkirjanpitomerkinnät ja kaksi lisätoimittajatapahtumaa kirjataan selvitysprosessissa. Tilitys vertaa myyntireskontran/ostoreskontran kirjanpitotiliä laskusta ja maksusta.  Kun maksaminen ja tilittäminen suoritetaan yhdessä (mikä on tavanomainen tilanne), maksun kirjanpitotapahtumaa ei kirjata yleiseen kirjanpitoon ennen kuin selvitysprosessi myös on valmis. Käsittelytapahtumien järjestyksen vuoksi tilitys ei voi määrittää todellista myyntireskontran/ostoreskontran kirjanpitotiliä maksun kirjanpitotapahtumasta. Tilitys määrittää, mitä kirjanpitotili on maksulle. Tästä tulee ongelma, kun myyntireskontran/ostoreskontran päätilille käytetään kiinteää dimensiota.

Kirjanpitotilin määrittämiseksi myyntireskontran/ostoreskontran päätili haetaan kirjausprofiilista ja taloushallinnon dimensiot haetaan maksun toimittajatapahtumatietueesta, kuten on määritetty maksukirjauskansiossa. Kiinteitä dimensioita ei oletusarvoisesti määritetä maksukirjauskansioihin, mutta sen sijaan niitä käytetään päätilille kirjausprosessin viimeisenä vaiheena. Tuloksena kiinteän dimension arvo ei todennäköisesti sijaitse toimittajatapahtumassa, jollei sitä oletusarvoisesti noudeta muusta lähteestä, esimerkiksi toimittajasta. Kiinteä dimensio ei sisälly rekonstruoituun tiliin. Tilityksen käsittely määrittää, että oikaiseva merkintä on luotava, sillä lasku, joka kirjattiin käyttäen kiinteän dimension arvoa ja rekonstruoitua maksutiliä, ei luonut merkintää.  Kun tilitys jatkuu oikaisevan tapahtuman kirjaamisella, kirjauksen viimeinen vaihe on käytettävälle kiinteälle dimensiolle. Lisäämällä kiinteän dimension oikaisevaan tapahtumaan se kirjataan debetin ja kreditin kanssa samalle kirjanpitotilille. Selvitys ei voi palautua takaisin kirjanpidon kirjaukseen.

Kirjanpidon lisätapahtumien välttämiseksi kirjattaessa debet ja kredit samalle kirjanpitotilille, suositellaan harkittavan seuraavia ratkaisuja liiketoiminnan tarpeiden mukaan. 

-   Organisaatiot käyttävät usein kiinteitä dimensioita, jotta voidaan täyttää nollilla taloushallinnon dimensio, joka ei ole pakollinen. Tämä on yleistä tasetileissä, kuten myyntireskontrassa/ostoreskontrassa. Tilirakenteita voidaan käyttää seuranna poistamiseen taloushallinnon dimensioista, jotka on yleensä täytetty nollilla.  Voit poistaa kirjanpitodimension tasetileiltä, jotta ei tarvitse käyttää kiinteitä dimensioita.
-   Jos organisaatiosi vaatii kiinteitä dimensioita myyntireskontran/ostoreskontran päätilille, etsi tapa liittää kiinteä dimensio oletusarvoisesti maksuun, jotta kiinteä dimensioarvo tallennetaan maksun toimittajatapahtumaan. Tällöin järjestelmä luo myyntireskontran/ostoreskontran päätilin sisältämään kiinteät dimensioarvot. Kiinteä dimensioarvo voidaan määrittää oletusarvona joko toimittajille tai maksukirjauskansion kirjauskansionimelle.
