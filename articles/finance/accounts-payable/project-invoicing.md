---
title: Projektin laskutus
description: Tämä ohjeaihe sisältää aika- ja materiaaliprojektien sekä kiinteähintaisten projektien projektilaskutuksen yleiskatsauksen. Artikkelissa on tietoja myös laskuehdotuksista (alustavista laskuista), laskutuksen hallinnasta, ennakkolaskutuksesta, toimittajan laskutuksesta ja hyvityslaskuista.
author: TaylorVH
ms.date: 07/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: zezhangzhao
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: bdb5c9162ab85632c8780a737df0998e4cd34f0c
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733845"
---
# <a name="project-invoicing"></a>Projektin laskutus

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää aika- ja materiaaliprojektien sekä kiinteähintaisten projektien projektilaskutuksen yleiskatsauksen. Artikkelissa on tietoja myös laskuehdotuksista (alustavista laskuista), laskutuksen hallinnasta, ennakkolaskutuksesta, toimittajan laskutuksesta ja hyvityslaskuista.

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

Voit luoda laskuehdotuksia manuaalisesti valitsemalla tapahtuma määritetyn projektin käytettävissä olevien tapahtumien luettelosta. Voit määrittää laskutuksen säännöt, jotka määrittävät milloin laskuehdotus luodaan automaattisesti. Voit esimerkiksi luoda laskutussäännön laskuehdotuksen luomiseksi, kun projektin työstä on suoritettu 25, 50, 75 ja 100 prosenttia. 

Voit luoda laskuehdotukset seuraaville tapahtumille:

-   Tunnit, kulut ja muut projektitapahtumat
-   Summat, jotka asiakkaat ovat pidättäneet ennen projektilaskuja
-   Hyvityslaskut
-   Summat, jotka asiakas on maksanut ennen projektin alkamista

> [!NOTE]
> **Ota resurssin mukainen lajittelu käyttöön projektilaskuehdotuksen luomisessa** -toiminnon avulla projektin kirjapitäjä voi lajitella laskutettavissa olevat projektitapahtumat resurssin mukaan luodessaan uuden projektilaskuehdotuksen. Käytettävissä olevat projektitapahtumat näyttävässä ruudukossa on erilliset kentät **resurssitunnukselle** ja **resurssille**. Näiden kenttien avulla voit suodattaa ja lajitella resurssin nimen. Oletusarvon mukaan tämä asetus on pois käytöstä. Se voidaan ottaa käyttöön **Ominaisuuksien hallinta** -sivun avulla (**Työtilat > Ominaisuuksien hallinta**). Ota yhteyttä järjestelmänvalvojaan, jos tarvitset apua tämän ominaisuuden käyttöönotossa.

Voit luoda laskuehdotuksen maksutapahtumat. Voit myös muokata myyntihintaa tunti-, nimike- ja maksutapahtumissa. Jos kirjaat laskuehdotuksen, päivitetyt hinnat ja tapahtumat lisätään projektiraportteihin ja tapahtumien historiatietoihin. 

Voit halutessasi luoda useita asiakaslaskuja projektille luomalla kullekin laskulle laskuehdotuksen. Voit esimerkiksi luoda laskuja tapahtumatyypin perusteella. Voit määrittää tunnit yhteen myyntilaskuun ja nimikkeet toiseen laskuun luomalla tuntitapahtumille ja maksutapahtumille laskuehdotukset. 

Jos projektilla on enemmän kuin yksi rahoituslähde, voit luoda kullekin rahoituslähteelle erillisen laskuehdotuksen. Voit määrittää **Rahoitussäännön kohdistukset** -sivulla tapahtumasumman prosenttiosuuden, joka kohdistetaan kullekin rahoituslähteelle, ja lähteen, johon pyöristyserot kirjataan.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Myyntilaskujen luominen laskuehdotuksista

Kun olet luonut ja kirjannut laskuehdotuksen, laskuehdotukseen sisältyville tapahtumille luodaan automaattisesti myyntilasku. 

Voit lisätä tapahtumia laskuehdotukseen tai poistaa niitä laskuehdotuksesta ennen laskuehdotuksen kirjaamista. Voit esimerkiksi poistaa kulutapahtumat, jotka kirjattiin projektiin, mutta joita ei voi laskuttaa asiakkaalta. 

Jos organisaatio edellyttää laskuehdotuksien tarkistamista ennen niiden kirjaamista, laskuehdotus saattaa edellyttää hyväksymistä projektin laskuehdotuksen tarkistuksen työnkulun kautta, ennen kuin se kirjataan.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>Määrärahatietojen tarkasteleminen projektilaskuluettelosivuilla

Julkisen sektorin käyttäjät voivat lisätä **määrärahan tunnuksen** ja **määrärahan nimen** **Projektilaskuehdotukset**- ja **Projektilaskut**-luettelosivuille. Nämä sarakkeet otetaan käyttöön **Lisää määrärahan tiedot projektilaskuluettelosivuille** -ominaisuuden avulla. Tämä ominaisuus on oletusarvoisesti pois käytöstä. Se voidaan ottaa käyttöön kohdassa **Työtilat > Ominaisuuksien hallinta**. Ota yhteyttä järjestelmänvalvojaan, jos tarvitset apua tämän ominaisuuden käyttöönotossa.

## <a name="on-account-invoicing"></a>Ennakkolaskutus
Summa, jonka kirjaat projektin ennakkolaskulle, perustuu ajoitukseen, valmistumisprosenttiin ja muihin laskutusehtoihin, jotka on määritetty liittyvässä projektisopimuksessa. Summaa ei lasketa projektiin kirjattujen tuntien, nimikkeiden, kulujen tai maksujen perusteella. 

Sinun on luotava ennakkomaksutapahtuma kiinteähintaiselle projektille tai aika ja materiaali -projektille ennen kyseisen ennakkomaksutapahtuman lisäämistä projektilaskuun. Kirjoita ennakkolaskutustapahtumaan asiakkaalta laskutettava summa. Jos haluat luoda projektilaskun, luo alustava lasku (laskuehdotus). Valitse ennakkotapahtuma laskuehdotuksessa. Voit tarkastaa ennakkolaskun tiedot laskuehdotuksesta, ennen kuin luot projektilaskun siitä. 

### <a name="fixed-price-projects"></a>Kiinteähintaiset projektit
Kiinteähintaisissa projekteissa ennakkolaskutapahtumat perustuvat sovittuun välitavoitteeseen, toimitusyksikköön tai projektin sopimuksessa määritettyyn edistymiseen perustuvaan laskutusjärjestelyyn. Ohjelma luo rivin jokaiselle maksulle, joka tullaan vastaanottamaan projektiasiakkaalta. Vähennyksiä ei edellytetä.

### <a name="time-and-material-projects"></a>Aika- ja materiaaliprojektit

Aika-ja materiaaliprojekteissa voit laskuttaa asiakasta tai toista rahoituslähdettä ennakkomaksun määrän käyttämällä ennakkolaskulaskuehdotusta. Kirjoita ennakkolaskutapahtumat yhdellä rivillä Voit halutessasi lisätä lisärivejä vähennyksinä vastakirjataksesi kaikki ennakkomaksut, jotka asiakas on tehnyt. Voit luoda vähennysrivit lisäämällä miinusmerkin summan eteen.

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
Kun tilaat nimikkeen toimittajalta ja määrität nimikkeen projektiin, kyseisen nimikkeen ostotilausriville valittu riviominaisuus määrittää, laskutetaanko ostettu nimike asiakkaalle. Jos määrität oletusriviominaisuudet, ne näytetään nimikkeelle ostotilausrivillä (**Rivin tiedot > Projekti > Rivin ominaisuuden summat**). Riviominaisuutta voi muokata kahdella tavalla:

-   Laskuta nimike projektin asiakkaalta. Voit tehdä tämän määrittämällä nimikkeen riviominaisuuden veloitettavalle arvolle ostotilauksessa ja laskuta sitten asiakasta oikealla projektilaskutustavalla.
-   Älä laskuta nimikettä projektin asiakkaalta. Voit tehdä tämän, jos et valitse **Laskutettavissa**-riviominaisuutta nimikkeen ostotilausrivillä. Voit sitten laskuttaa ostotilauksen eikä muita toimintoja tarvita.

> [!NOTE] 
> Vapautuksen säilytysrivit eivät oletusarvoisesti ole veloitettavissa. Tämä tarkoittaa, että vapautetun säilytyksen laskuehdotuksen luontimahdollisuus ei ole käytössä.

## <a name="credit-notes"></a>Hyvityslaskut
Kun myyntilaskun summana on negatiivinen arvo, lasku luokitellaan hyvityslaskuksi. Kun asiakirja tulostetaan, sen otsikkona on Hyvityslasku. 

Kun luot hyvityslaskun aiemmin laskutetun summan hyvittämistä varten, laskutettu summa on ensin valittava hyvittämistä varten. Voit sitten luoda hyvityslaskun samalla tavalla kuin tavallisen myyntilaskun luomisessa. Valitse tapahtumat, jotka kirjattiin aiemmin myyntilaskulle. Luo ja kirjaa sitten hyvityslaskuehdotus. 

Sama asiakirja voi sisältää tapahtumat, jotka on valittu hyvitettäviksi, hyvitystapahtumia ja tapahtumia, jotka on kirjattu. Asiakirja luokitellaan joko laskuksi tai hyvityslaskuksi sen mukaan, onko kokonaissumma positiivinen vai negatiivinen luku. 

Jos haluat hyvittää laskutetun summan, laskutettu summa on ensin valittava hyvittämistä varten, jonka jälkeen luodaan uusi hyvityslasku. Voit luoda hyvityslaskun samalla tavoin kuin loisit myyntilaskun. 

Voit luoda laskun, jossa on negatiivinen summa ja josta tulee hyvityslaskuksi luokiteltava lasku. Jos haluat luoda ja tulostaa hyvityslaskun, sinun on valittava tapahtumat, jotka kirjattiin aiemmin myyntilaskulle ja muokattava sitten tapahtumia. Laskun otsikko on Korjaava lasku, ellei yrityksen ensisijainen osoite ole Saksassa.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
