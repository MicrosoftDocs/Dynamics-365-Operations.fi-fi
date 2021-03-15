---
title: Myyntipisteen asiakastilaukset
description: Tässä ohjeaiheessa on tietoja myyntipisteen asiakkaan työnkulusta. Asiakastilauksia kutsutaan myös erikoistilauksiksi. Aihe sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista.
author: josaw1
manager: AnnBe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6fec80dd2836a5400a7178e732fe1d5da41aca4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995792"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Myyntipisteen asiakastilaukset

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja myyntipisteen asiakkaan työnkulun luomisesta ja hallinnoimisesta. Asiakastilauksia voi käyttää myynnin tallentamisessa silloin, kun ostajat haluavat noutaa tuotteet myöhemmin, noutaa ne eri sijainnista tai valita nimikkeiden toimituksen. 

Monikanavaisessa kaupan maailmassa monet vähittäiskauppiaat tarjoavat asiakastilausten eli erikoistilausten mahdollisuuden täyttääkseen erilaisia eri tuote- ja palveluvaatimuksia. Seuraavassa on joitakin tyypillisiä skenaarioita:

- Asiakas haluaa, että tuotteet toimitetaan tiettynä päivänä tiettyyn osoitteeseen.
- Asiakas haluaa noutaa tuotteet myymälästä tai sijainnista, joka on eri kuin myymälä tai sijainti, josta asiakas osti nämä tuotteet.
- Myymälässä oleva asiakas haluaa tilata tuotteet tänään ja noutaa ne samasta myymälästä myöhemmin.

Vähittäiskauppiaat voivat käyttää asiakastilauksia myös pienentääkseen menetettyä myyntiä, jota varaston tyhjeneminen voi muuten aiheuttaa, koska kauppatavara voidaan toimittaa tai kerätä eri aikaan tai eri paikasta.

## <a name="set-up-customer-orders"></a>Määritä asiakastilaukset
Ennen kuin yrität käyttää asiakastilaustoimintoja myyntipisteessä, varmista, että kaikki pakolliset määritykset on tehty Commerce Headquarters -sovelluksessa.

### <a name="configure-modes-of-delivery"></a>Toimitustapojen määrittäminen

Jos haluat käyttää asiakastilauksia, sinun on määritettävä toimitustavat myymäläkanavan käyttöä varten. Sinun on määritettävä vähintään yksi toimitustapa, jota käytetään toimitettaessa tilausrivit myymälästä asiakkaalle. Sinun on määritettävä myös vähintään yksi noudon toimitustapa, jota käytetään, kun tilausrivit ovat noudettavissa myymälästä. Toimitustavat määritetään Commerce Headquarters -sovelluksen **Toimitustavat**-sivulla. Lisätietoja toimitustilan määrittämisestä Commerce-kanaville on kohdassa [Toimitustapojen määrittäminen](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Toimitustavat-sivu](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Täytäntöönpanoryhmien määrittäminen

Jotkin myymälät tai varastosijainnit eivät ehkä pysty täyttämään asiakastilauksia. Määrittämällä täytäntöönpanoryhmät organisaatio voi määrittää myyntipisteessa asiakastilauksia luoville käyttäjille vaihtoehtoina näytettävät myymälät ja varastosijainnit. Täytäntöönpanoryhmät määritetään **Täytäntöönpanoryhmät**-sivulla. Organisaatiot voivat luoda tarvittavan määrän täytäntöönpanoryhmiä. Kun täytäntöönpanoryhmä on määritetty, linkitä se myymälään valitsemalla toimintoruudun **Myymälät**-sivun **Määritys**-välilehdessä **Täytäntöönpanoryhmän määritys**.

Commercen versiossa 10.0.12 ja uudemmissa versioissa organisaatiot voivat määrittää, käytetäänkö täytäntöönpanoryhmissä määritettyä varastoa tai varaston ja myymälän yhdistelmää toimituksessa, noudossa tai sekä toimituksessa että noudossa. Tämä mahdollistaa joustavan määrityksen, jonka avulla yritys voi määrittää, mitä varastoja voidaan valita, kun nimikkeiden toimitusta varten luodaan asiakastilaus sekä mitkä myymälät voidaan valita luotaessa asiakastilaus nimikkeiden noutoa varten. Jos haluat käyttää näitä määritysvaihtoehtoja, ota käyttöön **Mahdollisuus määrittää sijainniksi Toimitus tai Nouto on otettu käyttöön täytäntöönpanoryhmissä** -ominaisuus. Jos myymälässä ei ole täytäntöönpanoryhmään linkitettyä varastoa, se voidaan määrittää vain toimitussijainniksi. Sitä ei voi käyttää, kun noudon tilaukset on määritetty myyntipisteessä.

![Täytäntöönpanoryhmät-sivu](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanavan asetusten määrittäminen

Jotkin myyntikanavan asetukset on tarkistettava, kun asiakastilauksia käsitellään myyntipisteessä. Nämä asetukset ovat Commerce Headquarters -sovelluksen **Myymälät**-sivulla.

- **Varasto** – Tämä kenttä osoittaa varaston, jota käytetään myymälässä määritettyjen toimitusten täyttämisessä.
- **Täytäntöönpanoryhmän määritys** – Valitse tämä painike (toimintoruudun **Määritys**-välilehdessä), jos haluat linkittää noutosijaintien tai toimitusten alkuperäisten sijaintien näyttövaihtoehtoihin viittaavat täytäntöönpanoryhmät, kun asiakastilaukset luodaan myyntipisteessä.
- **Käytä kohteeseen perustuvaa veroa** – Tämä vaihtoehto osoittaa, käytetäänkö toimitusosoitetta sen veroryhmän määrittämisessä, joka kohdistetaan asiakkaan osoitteeseen toimitettaviin tilausriveihin.
- **Käytä asiakkaaseen perustuvaa veroa** – Tämä vaihtoehto osoittaa, käytetäänkö asiakkaan toimitusosoitteelle määritettyä veroryhmää myyntipisteessä luoduissa asiakkaan kotiin toimitettavien asiakastilausten verotuksessa.

![Myymälän kanavan asetukset Myymälät-sivulla](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Asiakastilausten parametrien määrittäminen

Ennen kuin yrität luoda asiakastilauksia myyntipisteessä, määritä soveltuvat parametrit Commerce Headquarters -sovelluksessa. Nämä parametrit ovat **Asiakastilaukset**-välilehdessä **Kaupan parametrit** -sivulla.

- **Oletustilaustyyppi** – Voit määrittää tilaustyypin, joka määritetään oletusarvoisesti myyntipisteessä luotuihin asiakastilauksiin. Nämä asiakastilaukset voivat olla myynti- tai tarjoustilauksia. Oletustilaustyypistä riippumatta käyttäjät voivat yhä luoda sekä myynti- että asiakastilauksia myyntipisteessä.
- **Oletuskäsirahaprosentti** – Määritä se tilauksen kokonaissumman prosenttiosuus, joka asiakkaan on maksettava talletuksena ennen tilauksen vahvistamista. Myymälän myyjät voivat käyttöoikeuksista riippuen ohittaa summan käyttämällä myyntipisteen **Talletuksen ohitus** -toimintoa, jos tämä toiminto on määritetty tapahtumanäytön asetuksissa.
- **Nouto-toimitustapa** – Määritä toimitustapa, jota käytetään myyntipisteessä noudettaviksi määritetyissä myyntitilausriveissä.
- **Nouto liikkeestä -toimitustapa** – Määritä toimitustapa, jota käytetään nouto liikkeestä -tilausriveiksi määritetyissä myyntitilausriveissä, kun on luotu yhdistetty ostoskori ja ostoskorin riveistä osa noudetaan tai toimitetaan ja asiakas noutaa osan heti liikkeestä.
- **Peruutusmaksuprosentti** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, määritä kyseisen maksun määrä.
- **Peruutusmaksun koodi** – Määritä myyntireskontran kulukoodi, jota käytetään kohdistettaessa peruutusmaksu peruutettuihin asiakastilauksiin myyntipisteen kautta. Kulukoodi määrittää peruutusmaksun taloushallinnon kirjauslogiikan.
- **Toimitusmaksun koodi** – Jos **Käytä automaattisia lisäveloituksia** -asetukseksi on määritetty **Kyllä**, tämän parametrin asetuksella ei ole vaikutusta. Jos tämän asetuksen arvoksi on määritetty **Ei**, käyttäjiä pyydetään syöttämään toimituskulu manuaalisesti, kun he luovat asiakastilauksia myyntipisteessä. Tämän parametrin avulla voit määrittää tilausten myyntireskontran kulukoodin. Sitä käytetään, kun käyttäjä syöttää toimitusmaksun. Kulukoodi määrittää toimitusmaksun taloushallinnon kirjauslogiikan.
- **Käytä automaattisia lisäveloituksia** – Määritä asetukseksi **Kyllä**, jos haluat käyttää järjestelmän laskemiasi automaattisia veloituksia, kun asiakastilaukset luodaan myyntipisteessä. Näitä automaattisia veloituksia voidaan käyttää toimituskulujen tai muiden tilaukseen tai nimikkeeseen liittyvien kulujen maksamisessa. Lisätietoja automaattisten lisäveloitusten määrittämisestä ja käyttämisestä on kohdassa [Monikanavaiset edistyneet automaattiset veloitukset](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Asiakastilaukset-välilehti kaupan parametrien sivulla](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Tapahtumanäytön asetteluiden päivittäminen myyntipisteessä

Varmista, että myyntipiste [näyttöasettelu](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) on määritetty tukemaan asiakastilausten luomista ja hallintaa ja että kaikki vaaditut myyntipisteen toiminnot on määritetty. Seuraavaksi esitellään joitakin myyntipisteen toimintoja, joiden tulee tukea asiakastilausten luomista ja hallintaa oikealla tavalla:
- **Lähetä kaikki tuotteet** – Tätä toimintoa käytetään määritettäessä, että kaikki tapahtuman ostoskorin rivit lähetetään kohteeseen.
- **Lähetä valitut tuotteet** – Tätä toimintoa käytetään määritettäessä, että valitut tapahtuman ostoskorin rivit lähetetään kohteeseen.
- **Nouda kaikki tuotteet** – Tätä toimintoa käytetään määritettäessä, että kaikki tapahtuman ostoskorin rivit noudetaan valitusta myymäläsijainnista.
- **Nouda valitut tuotteet** – Tätä toimintoa käytetään määritettäessä, että valitut tapahtuman ostoskorin rivit noudetaan valitusta myymäläsijainnista.
- **Asiakas kuljettaa kaikki tuotteet** – Tätä toimintoa käytetään määritettäessä, että asiakas kuljettaa kaikki tapahtuman ostoskorin rivit. Jos tätä toimintoa käytetään myyntipisteessä, asiakastilaus muunnetaan itsepalvelutukkutapahtumaksi.
- **Asiakas kuljettaa valitut tuotteet** – Tätä toimintoa käytetään määritettäessä, että asiakas kuljettaa valitut tapahtuman ostoskorin rivit ostotapahtuman yhteydessä. Tämä toiminto on hyödyllinen vain [hybriditilausten](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders) skenaariossa.
- **Jatka tilausta** – Tätä toimintoa käytetään haettaessa ja noudettaessa asiakastilauksia niin, että myyntipisteen käyttäjät voivat muokata, peruuttaa ja suorittaa täytäntöön liittyviä toimintoja tarvittaessa.
- **Muuta toimitustapaa** – Tämän toiminnon avulla voi muuttaa toimitusta varten määritettyjen rivien toimitustavan nopeasti. Käyttäjän ei tarvitse palata Lähetä kaikki tuotteet- tai Lähetä valitut tuotteet -toimintoon.
- **Talletuksen ohitus** – Tämän toiminnon avulla voi muuttaa asiakkaan valitusta asiakastilauksesta maksaman talletussumman.

![Myyntipisteen tapahtumanäytön toiminnot](media/customer-order-screen-layout.png)

## <a name="work-with-customer-orders-in-pos"></a>Asiakastilausten käsitteleminen myyntipisteessä

> [!NOTE]
> Tuoton tuloutustoiminnon käyttöä ei tällä hetkellä tueta Commerce-kanavissa (sähköinen kauppa, myyntipiste, puhelinkeskus). Nimikkeitä, joilla on määritetty tuottojen tuloutus, ei lisätä Commerce-kanavissa luotuihin tilauksiin. 

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Asiakastilauksen luominen tuotteille, jotka lähetetään asiakkaalle

1. Lisää myyntipisteen tapahtumanäytössä tapahtumalle asiakas.
2. Lisää tuotteet ostoskoriin.
3. Valitse **Lähetä valitut** tai **Lähetä kaikki**, jos haluat lähettää tuotteet asiakastilin osoitteeseen.
4. Valitse vaihtoehto asiakastilauksen luomista varten.
5. Vahvista tai muuta lähetyssijainti, vahvista tai muuta lähetysosoite ja valitse lähetystapa.
6. Anna asiakkaan toivoma tilauksen lähetyspäivä.
7. Käytä erääntyneiden laskettujen summien maksamisessa maksutoimintoja tai muuta erääntyviä summia **Talletuksen ohitus** -toiminnon avulla ja kohdista maksu.
8. Jos tilauksen kokonaissummaa ei ole maksettu, anna erääntyvää saldoa varten luottokortin tiedot. Niitä käytetään tilauksen laskuttamisen yhteydessä.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Asiakastilauksen luominen tuotteille, jotka asiakas noutaa

1. Lisää myyntipisteen tapahtumanäytössä tapahtumalle asiakas.
2. Lisää tuotteet ostoskoriin.
3. Valitse **Nouda valitut** tai **Nouda kaikki**, jos haluat käynnistää tilauksen noudon määrityksen.
4. Valitse myymäläsijainti, josta asiakas noutaa valitut tuotteet.
5. Valitse päivämäärä, jolloin nimike noudetaan.
6. Käytä erääntyneiden laskettujen summien maksamisessa maksutoimintoja tai muuta erääntyviä summia **Talletuksen ohitus** -toiminnon avulla ja kohdista maksu.
7. Jos tilauksen kokonaissummaa ei ole maksettu, määritä, maksaako asiakas myöhemmin (noudettaessa) vai tallennetaanko luottokortin tiedot nyt myöhempää noudon yhteydessä tapahtuvaa käyttöä varten.

### <a name="edit-an-existing-customer-order"></a>Olemassa olevan asiakkaan tilauksen muokkaaminen

Vähittäismyyntitilaukset, jotka luodaan online- tai myymäläkanavassa, voidaan peruuttaa myyntipisteessä tarvittaessa. Tämän jälkeen niitä voi muokata.

> [!IMPORTANT]
> Kaikkia vähittäismyyntitilauksia ei voi muokata myyntipistesovelluksessa. Puhelinkeskuskanavassa luotuja tilauksia ei voi muokata myyntipisteessä, jos [Ota käyttöön tilausten viimeistely](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) -asetus on otettu käyttöön puhelinkeskuskanavassa. Voit varmistaa oikean maksuprosessin puhelinkeskuskanavan tilauksille, joissa on käytössä Ota käyttöön tilausten viimeistely -toiminto, muokkaamalla niitä puhelinkeskussovelluksessa Commerce Headquarters -sovelluksessa.

Versiossa 10.0.17 ja sitä myöhemmissä versioissa käyttäjät voivat muokata hyväksyttäviä tilauksia myyntipistesovelluksen kautta, vaikka tilaus olisi osittain täytetty. Kokonaan laskutettuja tilauksia ei kuitenkaan vielä voi muokata myyntipisteessä. Jos haluat ottaa käyttöön tämän ominaisuuden, ota **Ota käyttöön osittain täytettyjen tilausten muokkaaminen myyntipisteessä** -toiminto käyttöön **Ominaisuuksien hallinta** -työtilassa. Jos tämä toiminto ei ole käytössä tai käytössä on versio 10.0.16 tai aiempi versio, käyttäjät voivat muokata asiakastilauksia myyntipisteessä vain, jos tilaus on kokonaan avoin. Lisäksi, jos ominaisuus on käytössä, voit rajoittaa, mitkä myymälät voivat muokata osittain täytettyjä tilauksia. Tämän toiminnon poistaminen käytöstä tietyissä myymälöissä voidaan konfiguroida **toimintoprofiilin** avulla **Yleiset**-pikavälilehdessä.


1. Valitse **Peruuta tilaus**.
2. Syötä suodattimet ja etsi tilaus **Hae**-kohdan avulla. Valitse sitten **Käytä**.
3. Valitse tilaus tulosluettelosta ja valitse sitten **Muokkaa**. Jos **Muokkaa**-painike ei ole käytettävissä, tilaus on tilassa, jossa sitä ei voi muokata.
4. Tee asiakastilaukseen tarvittavat muutokset tapahtuman ostoskorissa. Jotkin muutokset voivat olla kiellettyjä muokkauksen aikana.
5. Viimeistele muokkausprosessi valitsemalla maksutapahtuma.
6. Jos haluat poistua muokkausprosessista tallentamatta muutoksia, voit käyttää **Mitätöi tapahtuma** -toimintoa.



### <a name="cancel-a-customer-order"></a>Asiakastilauksen peruuttaminen

1. Valitse **Peruuta tilaus**.
2. Syötä suodattimet ja etsi tilaus **Hae**-kohdan avulla. Valitse sitten **Käytä**.
3. Valitse tilaus tulosluettelosta ja valitse sitten **Peruuta**. Jos **Peruuta**-painike ei ole käytettävissä, tilaus on tilassa, jossa sitä ei voi enää peruuttaa.
4. Jos peruutusmaksut on määritetty, vahvista ne. Voit oikaista peruutusmaksuja ennen niiden vahvistamista tarpeen mukaan. 
5. Viimeistele peruutusprosessi tapahtuman ostoskorissa valitsemalla maksutoiminto. Jos maksetut talletukset ylittävät peruutusmaksun, saatetaan joutua maksamaan hyvitysmaksuja.
6. Jos haluat poistua peruutusprosessista tallentamatta muutoksia, voit käyttää **Mitätöi tapahtuma** -toimintoa.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Asiakastilauksen lähetyksen tai noudon viimeisteleminen myyntipisteessä

Kun tilaus on luotu, asiakas noutaa nimikkeet myymäläsijainnista tai ne lähetetään tilauksen määrityksestä riippuen. Lisätietoja prosessista on [myymälän tilauksen täyttämisen](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview) dokumentaatiossa.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asiakastilausten tapahtumien asynkroninen työnkulku

Asiakastilauksia voi luoda myyntipisteessä joko synkronoidussa tai asynkronisessa tilassa. Jos asiakastilausten luomisen yhteydessä myyntipisteessä on suorituskykyonhgelmia tai käyttäjän viivettä, voit ottaa käyttöön asynkronisen tilauksen luomisen.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Ota käyttöön asiakastilausten luonti asynkronisessa tilassa

1. Valitse Commerce Headquarters -sovelluksen **Toimintoprofiilit**-sivulla määritettävää myymälää vastaava toimintoprofiili.
2. **Yleiset**-pikavälilehdessä määritä **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvoksi **Kyllä**.

Kun **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvo on **Kyllä**, asiakastilaukset luodaan aina asynkronisessa tilassa, vaikka Retail Transaction Service (RTS) -palvelu on käytettävissä. Jos määrität tämän asetuksen arvoksi **Ei**, asiakkaan tilaukset luodaan aina synkronoidussa tilassa RTS:n avulla. Kun asiakastilaukset luodaan asynkronisessa tilassa, ne noudetaan ja luodaan vähittäismyyntitapahtumina Commerce Headquarters -sovelluksessa kaupan noutotöinä. Vähittäismyyntitapahtumille luodaan vastaavat myyntitilaukset, kun **Synkronoi tilaukset** suoritetaan joko manuaalisesti tai eräprosessina.

## <a name="additional-resources"></a>Lisäresurssit

[Asiakkaiden yhdistelmätilaukset](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]