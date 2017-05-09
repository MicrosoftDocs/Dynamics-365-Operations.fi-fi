---
title: Projektiin laskutus
description: "Tämä artikkeli sisältää aika- ja materiaaliprojektien sekä kiinteähintaisten projektien projektilaskutuksen yleiskatsauksen. Artikkelissa on tietoja myös laskuehdotuksista (alustavista laskuista), laskutuksen hallinnasta, ennakkolaskutuksesta, toimittajan laskutuksesta ja hyvityslaskuista."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76abfa35e53673f9780d1a6f8816bd24f9f8e48
ms.openlocfilehash: f09aef9cf1e516b80f908c34b2b3c3397dde8a0f
ms.lasthandoff: 03/31/2017


---

# <a name="project-invoicing"></a>Projektiin laskutus

[!include[banner](../includes/banner.md)]


Tämä artikkeli sisältää aika- ja materiaaliprojektien sekä kiinteähintaisten projektien projektilaskutuksen yleiskatsauksen. Artikkelissa on tietoja myös laskuehdotuksista (alustavista laskuista), laskutuksen hallinnasta, ennakkolaskutuksesta, toimittajan laskutuksesta ja hyvityslaskuista.

Projektityyppi määrittää, mitä laskutusmenettelyä käytetään. Vain kahta ulkoista projektityyppiä, aika- ja materiaaliprojektit sekä kiinteähintaiset projektit, voidaan laskuttaa. Aika- ja materiaaliprojektit sekä kiinteähintaiset projektit liittyvät aina projektisopimukseen.

-   **Kiinteähintaiset projektit** – Myyntilaskun summa perustuu laskun laskutusaikatauluun. Laskutus tapahtuu ennakkolaskuasetusten, joita kutsutaan myös laskutusaikatauluksi. Kiinteähintaiset projektit voidaan laskuttaa projekti- tai projektisopimuskohtaisesti.
-   **Aika- ja materiaaliprojektit** – Myyntilaskun summa perustuu projekteille annettuihin tapahtumariveihin. Tapahtumat voidaan laskuttaa projekti- tai projektisopimuskohtaisesti.

Aika- ja materiaaliprojektit ja kiinteähintaiset projektit voidaan liittää laskutusprojekteihin kolmella tavalla:

-   **Ennakkolaskutus** – Aika- ja materiaaliprojektit ja kiinteähintaiset projektit voidaan laskuttaa ennakkoon. Kummallekin projektityypille on määritettävä omat ennakkolaskutusasetukset.
-   **Laskutus kausittain** – Kausitoimintojen avulla voidaan laskuttaa eri projektien tapahtumia. Kausitoimintojen avulla voi laatia laskutettavien tapahtumien yleiskatsauksen.
-   **Hyvityslaskujen käyttö laskutuksessa**– hyvityslasku voidaan luoda sekä aika- ja materiaaliprojekteille että kiinteähintaisille projekteille.

## <a name="invoice-proposals"></a>Laskuehdotukset
Ennen kuin luot projektin myyntilaskun, voit luoda alustavan laskun tai laskuehdotuksen. Voit valita laskuehdotuksessa projektilaskuun sisällytettävät projektitapahtumat. Voit sitten tarkistaa laskun tiedot ennen projektilaskun kirjaamista ja lähettämistä asiakkaalle tai toiselle rahoituslähteelle.

### <a name="creating-invoice-proposals"></a>Laskuehdotusten luominen

Voit luoda laskuehdotuksia manuaalisesti valitsemalla määritetyn projektin tapahtumien luettelosta. Voit määrittää laskutuksen säännöt, jotka määrittävät milloin laskuehdotus luodaan automaattisesti. Voit esimerkiksi luoda laskutussäännön laskuehdotuksen luomiseksi, kun projektin työstä on suoritettu 25 %, 50 %, 75 % ja 100 %. 

Voit luoda laskuehdotukset seuraaville tapahtumille:

-   Tunnit, kulut ja muut projektitapahtumat
-   Summat, jotka asiakkaat ovat pidättäneet ennen projektilaskuja
-   Hyvityslaskut
-   Summat, jotka asiakas on maksanut ennen projektin alkamista

Voit luoda laskuehdotuksen maksutapahtumat. Voit myös muokata myyntihintaa tunti-, nimike- ja maksutapahtumissa. Jos kirjaat laskuehdotuksen, päivitetyt hinnat ja tapahtumat lisätään projektiraportteihin ja tapahtumien historiatietoihin. 

Voit halutessasi luoda useita asiakaslaskuja projektille luomalla kullekin laskulle laskuehdotuksen. Voit esimerkiksi luoda laskuja tapahtumatyypin perusteella. Voit määrittää tunnit yhteen myyntilaskuun ja nimikkeet toiseen laskuun luomalla tuntitapahtumille ja maksutapahtumille laskuehdotukset. 

Jos projektilla on enemmän kuin yksi rahoituslähde, voit luoda kullekin rahoituslähteelle erillisen laskuehdotuksen. Voit määrittää **Rahoitussäännön kohdistukset** -sivulla tapahtumasumman prosenttiosuuden, joka kohdistetaan kullekin rahoituslähteelle, ja lähteen, johon pyöristyserot kirjataan.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Myyntilaskujen luominen laskuehdotuksista

Kun olet luonut ja kirjannut laskuehdotuksen, laskuehdotukseen sisältyville tapahtumille luodaan automaattisesti myyntilasku. 

Voit lisätä tapahtumia laskuehdotukseen tai poistaa niitä laskuehdotuksesta ennen laskuehdotuksen kirjaamista. Voit esimerkiksi poistaa kulutapahtumat, jotka kirjattiin projektiin mutta joita ei voi laskuttaa asiakkaalta. 

Jos organisaatio edellyttää laskuehdotuksien tarkistamista ennen niiden kirjaamista, laskuehdotus saattaa edellyttää hyväksymistä projektin laskuehdotuksen tarkistuksen työnkulun kautta, ennen kuin se kirjataan.

## <a name="on-account-invoicing"></a>Ennakkolaskutus
Summa, jonka kirjaat projektin ennakkolaskulle, perustuu ajoitukseen, valmistumisprosenttiin ja muihin laskutusehtoihin, jotka on määritetty liittyvässä projektisopimuksessa. Summaa ei lasketa projektiin kirjattujen tuntien, nimikkeiden, kulujen tai maksujen perusteella. 

Sinun on luotava ennakkomaksutapahtuma kiinteähintaiselle projektille tai aika ja materiaali -projektille ennen kyseisen ennakkomaksutapahtuman lisäämistä projektilaskuun. Kirjoita ennakkolaskutustapahtumaan asiakkaalta laskutettava summa. Jos haluat luoda projektilaskun, luo alustava lasku (laskuehdotus). Valitse ennakkotapahtuma laskuehdotuksessa. Voit tarkastaa ennakkolaskun tiedot laskuehdotuksesta, ennen kuin luot projektilaskun siitä.

### <a name="fixed-price-projects"></a>Kiinteähintaiset projektit

Kiinteähintaisissa projekteissa ennakkolaskutapahtumat perustuvat sovittuun välitavoitteeseen, toimitusyksikköön tai projektin sopimuksessa määritettyyn edistymiseen perustuvaan laskutusjärjestelyyn. Ohjelma luo rivin jokaiselle maksulle, joka tullaan vastaanottamaan projektiasiakkaalta. Vähennyksiä ei edellytetä.

### <a name="time-and-material-projects"></a>Aika- ja materiaaliprojektit

Aika-ja materiaaliprojekteissa voit laskuttaa asiakasta tai toista rahoituslähdettä ennakkomaksun määrän käyttämällä ennakkolaskulaskuehdotusta. Kirjoita ennakkolaskutapahtumat yhdellä rivillä Voit halutessasi lisätä lisärivejä vähennyksinä vastakirjataksesi kaikki ennakkomaksut, jotka asiakas on tehnyt. Voit luoda vähennysrivit lisäämällä niiden eteen miinusmerkin.

## <a name="invoice-control"></a>Laskutuksen hallinta
Voit seurata laskun hallinnalla sekä laskutettuja että laskuttamattomia tapahtumia ja analysoida kyseisiä tapahtumia vertaamalla niitä tarjouksiin. Saat tällä tavoin kattavan näkemyksen projekteista tarjousvaiheesta valmistumiseen. Näet, mitkä tapahtumat on veloitettu tietylle projektille ja mitkä rivit on laskutettu. Voit tarkastella myös yksittäisiä tapahtumia, joten voit oikaista niitä kirjaamisen jälkeen.

## <a name="invoicing-fixed-price-projects"></a>Kiinteähintaisten projektien laskuttaminen
Kiinteähintaisen projektin laskuttaminen edellyttää laskutusaikataulun määrittämistä ja laskutusmenettelyn suorittamista.

### <a name="billing-schedule"></a>Laskutusaikataulu

Voit laskuttaa kiinteähintaiset projektit laskutusaikataulun mukaisesti. Laskutusaikataulu määritetään projektin välitavoitteiden mukaan, joita voi olla yksi tai useita. Jokaiselle välitavoitteelle määritetään tietty päivämäärä, myyntivaluutta, myyntihinta ja tehtävä. 

Voit esimerkiksi määrittää seuraavan laskutusaikataulun:

-   20 prosenttia, kun projektisopimus allekirjoitetaan
-   30 prosenttia ensimmäisen toimituksen yhteydessä
-   15 prosentti toisen toimituksen yhteydessä
-   35 prosenttia viimeisen toimituksen yhteydessä

### <a name="invoicing-procedure"></a>Laskutusmenettely

Kun välitavoitemaksut ovat valmiita laskutettaviksi, käytetään ennakkosummien laskutustapaa.

## <a name="vendor-invoicing"></a>Toimittajan laskutus
Kun tilaat nimikkeen toimittajalta ja määrität nimikkeen projektiin, kyseisen nimikkeen ostotilausriville valittu riviominaisuus määrittää, laskutetaanko ostettu nimike asiakkaalle. Jos määrität oletusriviominaisuudet, ne näytetään nimikkeelle ostotilausrivillä (Rivin erittely &gt; Projekti &gt; Rivin ominaisuus). Riviominaisuutta voi muokata kahdella tavalla:

-   Projektin asiakasta laskutetaan nimikkeestä: määritä nimikkeen riviominaisuus veloitettavalle arvolle ostotilauksessa ja laskuta sitten asiakasta oikealla projektilaskutustavalla.
-   Projektin asiakasta ei laskuteta nimikkeestä: Älä valitse nimikkeen ostotilausrivin **Veloitettava**-riviominaisuutta. Voit sitten laskuttaa ostotilauksen eikä muita toimintoja tarvita.

## <a name="credit-notes"></a>Hyvityslaskut
Kun myyntilaskun summana on negatiivinen arvo, lasku luokitellaan hyvityslaskuksi. Kun asiakirja tulostetaan, sen otsikkona on Hyvityslasku. 

Kun luot hyvityslaskun aiemmin laskutetun summan hyvittämistä varten, laskutettu summa on ensin valittava hyvittämistä varten. Voit sitten luoda hyvityslaskun samalla tavalla kuin loisit tavallinen myyntilaskun. Valitset siis tapahtumat, jotka kirjattiin aiemmin myyntilaskulle, ja luot ja kirjaat sitten hyvityslaskuehdotuksen. 

Sama asiakirja voi sisältää tapahtumat, jotka on valittu hyvitettäviksi, hyvitystapahtumia ja tapahtumia, jotka on kirjattu. Asiakirja luokitellaan joko laskuksi tai hyvityslaskuksi sen mukaan, onko kokonaissumma positiivinen vai negatiivinen luku. 

Jos haluat hyvittää laskutetun summan, laskutettu summa on ensin valittava hyvittämistä varten, jonka jälkeen luodaan uusi hyvityslasku. Voit luoda hyvityslaskun samalla tavoin kuin loisit myyntilaskun. 

Voit luoda laskun, jossa on negatiivinen summa ja josta tulee hyvityslaskuksi luokiteltava lasku. Jos haluat luoda ja tulostaa hyvityslaskun, sinun on valittava tapahtumat, jotka kirjattiin aiemmin myyntilaskulle ja muokattava sitten tapahtumia. Laskun otsikko on Korjaava lasku, ellei yrityksen ensisijainen osoite ole Saksassa.




