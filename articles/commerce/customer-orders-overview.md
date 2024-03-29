---
title: Myyntipisteen asiakastilaukset
description: Tässä artikkelissa on tietoja myyntipisteen asiakastilauksista. Asiakastilauksia kutsutaan myös erikoistilauksiksi. Artikkeli sisältää keskustelun liittyvistä parametreista ja tapahtumatyönkuluista.
author: josaw1
ms.date: 08/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom:
- "260594"
- intro-internal
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6051e0a18823b354dd9940aac70a086a0f317002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850379"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Myyntipisteen asiakastilaukset

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja asiakastilauksen luomisesta ja hallinnasta myyntipistesovelluksessa. Asiakastilauksia voi käyttää myynnin tallentamisessa silloin, kun ostajat haluavat noutaa tuotteet myöhemmin, noutaa ne eri sijainnista tai valita nimikkeiden toimituksen. 

Monikanavaisessa kaupan maailmassa monet vähittäiskauppiaat tarjoavat asiakastilausten eli erikoistilausten mahdollisuuden täyttääkseen erilaisia eri tuote- ja palveluvaatimuksia. Seuraavassa on joitakin tyypillisiä skenaarioita:

- Asiakas haluaa, että tuotteet toimitetaan tiettynä päivänä tiettyyn osoitteeseen.
- Asiakas haluaa noutaa tuotteet myymälästä tai sijainnista, joka on eri kuin myymälä tai sijainti, josta asiakas osti nämä tuotteet.
- Myymälässä oleva asiakas haluaa tilata tuotteet tänään ja noutaa ne samasta myymälästä myöhemmin.

Vähittäiskauppiaat voivat käyttää asiakastilauksia myös pienentääkseen menetettyä myyntiä, jota varaston tyhjeneminen voi muuten aiheuttaa, koska kauppatavara voidaan toimittaa tai kerätä eri aikaan tai eri paikasta.

## <a name="set-up-customer-orders"></a>Määritä asiakastilaukset
Ennen kuin yrität käyttää asiakastilaustoimintoja myyntipisteessä, varmista, että kaikki pakolliset määritykset on tehty Commerce Headquarters -sovelluksessa.

### <a name="configure-modes-of-delivery"></a>Toimitustapojen määrittäminen

Jos haluat käyttää asiakastilauksia, sinun on määritettävä toimitustavat myymäläkanavan käyttöä varten. Sinun on määritettävä vähintään yksi toimitustapa, jota käytetään toimitettaessa tilausrivit myymälästä asiakkaalle. Sinun on määritettävä myös vähintään yksi noudon toimitustapa, jota käytetään, kun tilausrivit ovat noudettavissa myymälästä. Toimitustavat määritetään Commerce Headquarters -sovelluksen **Toimitustavat**-sivulla. Lisätietoja toimitustilan määrittämisestä Commerce-kanaville on kohdassa [Toimitustapojen määrittäminen](./configure-call-center-delivery.md#define-delivery-modes).

![Toimitustavat-sivu.](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Täytäntöönpanoryhmien määrittäminen

Jotkin myymälät tai varastosijainnit eivät ehkä pysty täyttämään asiakastilauksia. Määrittämällä täytäntöönpanoryhmät organisaatio voi määrittää myyntipisteessa asiakastilauksia luoville käyttäjille vaihtoehtoina näytettävät myymälät ja varastosijainnit. Täytäntöönpanoryhmät määritetään **Täytäntöönpanoryhmät**-sivulla. Organisaatiot voivat luoda tarvittavan määrän täytäntöönpanoryhmiä. Kun täytäntöönpanoryhmä on määritetty, linkitä se myymälään valitsemalla toimintoruudun **Myymälät**-sivun **Määritys**-välilehdessä **Täytäntöönpanoryhmän määritys**.

Commercen versiossa 10.0.12 ja uudemmissa versioissa organisaatiot voivat määrittää, käytetäänkö täytäntöönpanoryhmissä määritettyä varastoa tai varaston ja myymälän yhdistelmää toimituksessa, noudossa tai sekä toimituksessa että noudossa. Tämä mahdollistaa joustavan määrityksen, jonka avulla yritys voi määrittää, mitä varastoja voidaan valita, kun nimikkeiden toimitusta varten luodaan asiakastilaus sekä mitkä myymälät voidaan valita luotaessa asiakastilaus nimikkeiden noutoa varten. Jos haluat käyttää näitä määritysvaihtoehtoja, ota käyttöön **Mahdollisuus määrittää sijainniksi Toimitus tai Nouto on otettu käyttöön täytäntöönpanoryhmissä** -ominaisuus. Jos myymälässä ei ole täytäntöönpanoryhmään linkitettyä varastoa, se voidaan määrittää vain toimitussijainniksi. Sitä ei voi käyttää, kun noudon tilaukset on määritetty myyntipisteessä.

![Täytäntöönpanoryhmät-sivu.](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Kanavan asetusten määrittäminen

Jotkin myyntikanavan asetukset on tarkistettava, kun asiakastilauksia käsitellään myyntipisteessä. Nämä asetukset ovat Commerce Headquarters -sovelluksen **Myymälät**-sivulla.

- **Varasto** – Tämä kenttä ilmaisee varaston, jota käytetään, kun varastoa vähennetään maksa ja nouda- ja asiakkaan nouto -tilauksille, jotka ovat sidottuja tähän myymälään. Parhaan käytännön mukaisesti on hyvä käyttää kullekin myymäläkanavalle yksilöllisiä varastoja, jotta voidaan estää myymälöiden väliset ristiriitaiset liiketoimintalogiikan ongelmat.
- **Lähetysvarasto** – Tämä kenttä ilmaisee varaston, jota käytetään, kun varastoa vähennetään maksa ja nouda- ja asiakkaan nouto -tilauksille, jotka toimitetaan valitusta myymälästä. Jos **Mahdollisuus määrittää sijainniksi Lähetys tai Nouto on otettu käyttöön täyttämisryhmässä** -toiminto on otettu käyttöön ympäristössäsi, myyntipisteen käyttäjät voivat valita myyntipisteessa tietyn varaston, josta lähetetään, sen sijaan, että valittaisiin myymälä, josta lähetetään. Kun tämä ominaisuus on käytössä, lähetysvarastoa ei enää käytetä, koska käyttäjä valitsee tietyn varaston, josta tilaus lähetetään tilauksen luomisen yhteydessä.
- **Täytäntöönpanoryhmän määritys** – Valitse tämä painike (toimintoruudun **Määritys**-välilehdessä), jos haluat linkittää noutosijaintien tai toimitusten alkuperäisten sijaintien näyttövaihtoehtoihin viittaavat täytäntöönpanoryhmät, kun asiakastilaukset luodaan myyntipisteessä.
- **Käytä kohteeseen perustuvaa veroa** – Tämä vaihtoehto osoittaa, käytetäänkö toimitusosoitetta sen veroryhmän määrittämisessä, joka kohdistetaan asiakkaan osoitteeseen toimitettaviin tilausriveihin.
- **Käytä asiakkaaseen perustuvaa veroa** – Tämä vaihtoehto osoittaa, käytetäänkö asiakkaan toimitusosoitteelle määritettyä veroryhmää myyntipisteessä luoduissa asiakkaan kotiin toimitettavien asiakastilausten verotuksessa.

![Myymälän kanavan asetukset Myymälät-sivulla.](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Asiakastilausten parametrien määrittäminen

Ennen kuin yrität luoda asiakastilauksia myyntipisteessä, määritä soveltuvat parametrit Commerce Headquarters -sovelluksessa. Nämä parametrit ovat **Asiakastilaukset**-välilehdessä **Kaupan parametrit** -sivulla.

- **Oletustilaustyyppi** – Voit määrittää tilaustyypin, joka määritetään oletusarvoisesti myyntipisteessä luotuihin asiakastilauksiin. Nämä asiakastilaukset voivat olla myynti- tai tarjoustilauksia. Oletustilaustyypistä riippumatta käyttäjät voivat yhä luoda sekä myynti- että asiakastilauksia myyntipisteessä.
- **Oletuskäsirahaprosentti** – Määritä se tilauksen kokonaissumman prosenttiosuus, joka asiakkaan on maksettava talletuksena ennen tilauksen vahvistamista. Myymälän myyjät voivat käyttöoikeuksista riippuen ohittaa summan käyttämällä myyntipisteen **Talletuksen ohitus** -toimintoa, jos tämä toiminto on määritetty tapahtumanäytön asetuksissa.
- **Nouto-toimitustapa** – Määritä toimitustapa, jota käytetään myyntipisteessä noudettaviksi määritetyissä myyntitilausriveissä.
- **Nouto liikkeestä -toimitustapa** – Määritä toimitustapa, jota käytetään nouto liikkeestä -tilausriveiksi määritetyissä myyntitilausriveissä, kun on luotu yhdistetty ostoskori ja ostoskorin riveistä osa noudetaan tai toimitetaan ja asiakas noutaa osan heti liikkeestä.
- **Peruutusmaksuprosentti** – Jos asiakkaan tilauksen peruuttamisesta perittään maksu, määritä kyseisen maksun määrä.
- **Peruutusmaksun koodi** – Määritä myyntireskontran kulukoodi, jota käytetään kohdistettaessa peruutusmaksu peruutettuihin asiakastilauksiin myyntipisteen kautta. Kulukoodi määrittää peruutusmaksun taloushallinnon kirjauslogiikan.
- **Toimitusmaksun koodi** – Jos **Käytä automaattisia lisäveloituksia** -asetukseksi on määritetty **Kyllä**, tämän parametrin asetuksella ei ole vaikutusta. Jos tämän asetuksen arvoksi on määritetty **Ei**, käyttäjiä pyydetään syöttämään toimituskulu manuaalisesti, kun he luovat asiakastilauksia myyntipisteessä. Tämän parametrin avulla voit määrittää tilausten myyntireskontran kulukoodin. Sitä käytetään, kun käyttäjä syöttää toimitusmaksun. Kulukoodi määrittää toimitusmaksun taloushallinnon kirjauslogiikan.
- **Käytä automaattisia lisäveloituksia** – Määritä asetukseksi **Kyllä**, jos haluat käyttää järjestelmän laskemiasi automaattisia veloituksia, kun asiakastilaukset luodaan myyntipisteessä. Näitä automaattisia veloituksia voidaan käyttää toimituskulujen tai muiden tilaukseen tai nimikkeeseen liittyvien kulujen maksamisessa. Lisätietoja automaattisten lisäveloitusten määrittämisestä ja käyttämisestä on kohdassa [Monikanavaiset edistyneet automaattiset veloitukset](./omni-auto-charges.md).

![Asiakastilaukset-välilehti Kaupan parametrit -sivulla.](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Tapahtumanäytön asetteluiden päivittäminen myyntipisteessä

Varmista, että myyntipiste [näyttöasettelu](./pos-screen-layouts.md) on määritetty tukemaan asiakastilausten luomista ja hallintaa ja että kaikki vaaditut myyntipisteen toiminnot on määritetty. Seuraavaksi esitellään joitakin myyntipisteen toimintoja, joiden tulee tukea asiakastilausten luomista ja hallintaa oikealla tavalla:
- **Lähetä kaikki tuotteet** – Tätä toimintoa käytetään määritettäessä, että kaikki tapahtuman ostoskorin rivit lähetetään kohteeseen.
- **Lähetä valitut tuotteet** – Tätä toimintoa käytetään määritettäessä, että valitut tapahtuman ostoskorin rivit lähetetään kohteeseen.
- **Nouda kaikki tuotteet** – Tätä toimintoa käytetään määritettäessä, että kaikki tapahtuman ostoskorin rivit noudetaan valitusta myymäläsijainnista.
- **Nouda valitut tuotteet** – Tätä toimintoa käytetään määritettäessä, että valitut tapahtuman ostoskorin rivit noudetaan valitusta myymäläsijainnista.
- **Asiakas kuljettaa kaikki tuotteet** – Tätä toimintoa käytetään määritettäessä, että asiakas kuljettaa kaikki tapahtuman ostoskorin rivit. Jos tätä toimintoa käytetään myyntipisteessä, asiakastilaus muunnetaan itsepalvelutukkutapahtumaksi.
- **Asiakas kuljettaa valitut tuotteet** – Tätä toimintoa käytetään määritettäessä, että asiakas kuljettaa valitut tapahtuman ostoskorin rivit ostotapahtuman yhteydessä. Tämä toiminto on hyödyllinen vain [hybriditilausten](./hybrid-customer-orders.md) skenaariossa.
- **Jatka tilausta** – Tätä toimintoa käytetään haettaessa ja noudettaessa asiakastilauksia niin, että myyntipisteen käyttäjät voivat muokata, peruuttaa ja suorittaa täytäntöön liittyviä toimintoja tarvittaessa.
- **Muuta toimitustapaa** – Tämän toiminnon avulla voi muuttaa toimitusta varten määritettyjen rivien toimitustavan nopeasti. Käyttäjän ei tarvitse palata Lähetä kaikki tuotteet- tai Lähetä valitut tuotteet -toimintoon.
- **Talletuksen ohitus** – Tämän toiminnon avulla voi muuttaa asiakkaan valitusta asiakastilauksesta maksaman talletussumman.

![Myyntipisteen tapahtumanäytön toiminnot.](media/customer-order-screen-layout.png)

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
> Kaikkia vähittäismyyntitilauksia ei voi muokata myyntipistesovelluksessa. Puhelinkeskuskanavassa luotuja tilauksia ei voi muokata myyntipisteessä, jos [Ota käyttöön tilausten viimeistely](./set-up-order-processing-options.md#enable-order-completion) -asetus on otettu käyttöön puhelinkeskuskanavassa. Voit varmistaa oikean maksuprosessin puhelinkeskuskanavan tilauksille, joissa on käytössä Ota käyttöön tilausten viimeistely -toiminto, muokkaamalla niitä puhelinkeskussovelluksessa Commerce Headquarters -sovelluksessa.

> [!NOTE]
> Myyntipisteessä ei kannata muokata tilauksia ja tarjouksia, jotka muu kuin puhelinkeskuskäyttäjä loi Commerce-pääkonttorisovelluksessa. Nämä tilaukset ja tarjoukset eivät käytä Commercen hinnoittelumoduulia, joten jos niitä muokataan myyntipisteessä, Commercen hinnoittelumoduuli hinnoittelee ne uudelleen.


Versiossa 10.0.17 ja sitä myöhemmissä versioissa käyttäjät voivat muokata hyväksyttäviä tilauksia myyntipistesovelluksen kautta, vaikka tilaus olisi osittain täytetty. Kokonaan laskutettuja tilauksia ei kuitenkaan vielä voi muokata myyntipisteessä. Jos haluat ottaa käyttöön tämän ominaisuuden, ota **Ota käyttöön osittain täytettyjen tilausten muokkaaminen myyntipisteessä** -toiminto käyttöön **Ominaisuuksien hallinta** -työtilassa. Jos tämä toiminto ei ole käytössä tai käytössä on versio 10.0.16 tai aiempi versio, käyttäjät voivat muokata asiakastilauksia myyntipisteessä vain, jos tilaus on kokonaan avoin. Lisäksi, jos ominaisuus on käytössä, voit rajoittaa, mitkä myymälät voivat muokata osittain täytettyjä tilauksia. Tämän toiminnon poistaminen käytöstä tietyissä myymälöissä voidaan konfiguroida **toimintoprofiilin** avulla **Yleiset**-pikavälilehdessä.


1. Valitse **Peruuta tilaus**.
2. Syötä suodattimet ja etsi tilaus **Hae**-kohdan avulla. Valitse sitten **Käytä**.
3. Valitse tilaus tulosluettelosta ja valitse sitten **Muokkaa**. Jos **Muokkaa**-painike ei ole käytettävissä, tilaus on tilassa, jossa sitä ei voi muokata.
4. Tee asiakastilaukseen tarvittavat muutokset tapahtuman ostoskorissa. Jotkin muutokset voivat olla kiellettyjä muokkauksen aikana.
5. Viimeistele muokkausprosessi valitsemalla maksutapahtuma.
6. Jos haluat poistua muokkausprosessista tallentamatta muutoksia, voit käyttää **Mitätöi tapahtuma** -toimintoa.

#### <a name="pricing-impact-when-orders-are-edited"></a>Hinnoittelun vaikutus tilauksia muokattaessa

Kun tilaukset tehdään myyntipisteessä tai Commercen sähköisessä kaupankäyntisivustossa, asiakkaat vahvistavat summan. Tämä summa sisältää hinnan, ja se voi sisältää myös alennuksen. Asiakkaalla, joka tekee tilauksen ja muuttaa sitten myöhemmin tilausta (esimerkiksi lisäämällä toisen nimikkeen) ottamalla yhteyttä puhelinkeskukseen, on tiettyjä odotuksia alennusten käytöstä. Vaikka aiemmin luotujen tilausrivien kampanjat olisivat päättyneet, asiakas odottaa, että kyseisillä riveillä alun perin käytetyt alennukset pysyvät voimassa. Jos alennus ei kuitenkaan ollut vielä voimassa, kun tilaus alun perin tehtiin, mutta on tullut voimaan sen jälkeen, asiakas odottaa, että uutta alennusta käytetään muuttuneeseen tilaukseen. Muussa tapauksessa asiakas saattaa peruuttaa aiemmin luodun tilauksen ja luoda sitten uuden tilauksen, jossa uutta alennusta käytetään. Tämä skenaario osoittaakin, että asiakkaan vahvistamat hinnat ja alennukset on säilytettävä. Myyntipisteen ja puhelinkeskuksen käyttäjien kuitenkin voitava myös joustavasti laskea tarvittaessa myyntitilausrivien hinnat ja alennukset uudelleen.

Kun tilauksia peruutetaan ja muokataan myyntipisteessä, aiemmin luotujen tilausrivien hintoja ja alennuksia pidetään lukittuina. Ne eivät toisin sanoen muutu, vaikka osa tilausriveistä peruttaisiin, niitä muutettaisiin tai uusia tilausrivejä lisättäisiin. Myyntipisteen käyttäjä voi muuttaa aiemmin luotujen myyntirivien hintoja ja alennuksia valitsemalla **Laske uudelleen**. Hintalukitus poistetaan silloin aiemmin luoduilta tilausriveiltä. Tämä ominaisuus ei kuitenkaan ollut käytettävissä puhelinkeskuksessa ennen Commercen versiota 10.0.21. Tilausriveille tehdyt muutokset aiheuttivat sen sijaan hintojen ja alennusten laskemisen uudelleen.

Commercen versiossa 10.0.21 on uusi **Ominaisuuksien hallinta** -työtilassa käytettävissä oleva ominaisuus, **Estä kaupankäynnin tilausten tahaton hinnan laskenta**. Tämä ominaisuus on otettu oletusarvoisesti käyttöön. Kun ominaisuus on otettu käyttöön, kaikissa sähköisen kaupankäynnin tilauksissa voi käyttää **Hinta lukittu** -ominaisuutta. Kun missä tahansa kanavassa tehdyn tilauksen sieppaus on valmis, tämä ominaisuus otetaan automaattisesti käyttöön (eli valintaruutu on valittuna) kaikilla tilausriveillä. Commercen hinnoittelumoduuli jättää tämän jälkeen kyseiset tilausrivit pois kaikista hinta- ja alennuslaskelmista. Niinpä tilausta muokattaessa tilausrivit jätetään oletusarvoisesti pois hinnoittelu- ja alennuslaskelmista. Puhelinkeskuksen käyttäjät voivat kuitenkin poistaa omaisuuden käytöstä (eli poistaa valintaruudun valinnan) millä tahansa tilausrivillä ja valita sitten **Laske uudelleen**, jolloin aiemmin luodut tilausrivit ovat mukana hintalaskelmissa.

Vaikka puhelinkeskuksen käyttäjät käyttäisivät manuaalista alennusta aiemmin luodulla tilausrivillä, myyntirivin **Hinta lukittu** -ominaisuus on silti poistettava käytöstä ennen manuaalisen alennuksen käyttöä.

Puhelinkeskuksen käyttäjät voivat käyttää myös tilausrivien **Hinta lukittu** -ominaisuuden joukkokäytöstäpoistoa valitsemalla **Poista hinnan lukitus** **Myyntitilaus**-sivun toimintoruudun **Myynti**-välilehden **Laske**-ryhmässä. Hinnan lukitus poistetaan tässä tapauksessa kaikilta muilta tilausriveiltä lukuun ottamatta rivejä, joita ei voi muokata (eli rivejä, joiden tila on **Osittain laskutettu** tai **Laskutettu**). Sen jälkeen kun tilaukseen tehtävät muutokset ovat valmiita ja ne on lähetty, hinnan lukitus otetaan uudelleen käyttöön kaikilla tilausriveillä.

> [!IMPORTANT]
> Kun **Estä kaupankäynnin tilausten tahaton hinnan laskenta** -ominaisuus on otettu käyttöön, kauppasopimuksen arviointimääritykset ohitetaan hinnoittelutyönkuluissa. Toisin sanoen kauppasopimuksen arviointi-ikkunassa ei näy **Hintaan liittyvä** -osaa. Tämä johtuu siitä, että sekä kauppasopimuksen arviointimäärityksellä että hinnan lukitusominaisuudella on sama tarkoitus: estää tahattomat hinnan muutokset. Kauppasopimuksen arvioinnin käyttökokemus ei kuitenkaan skaalaudu hyvin suurissa tilauksissa, joissa käyttäjän on valittava uudelleenhinnoittelua varten yksi tilausrivi tai useita rivejä.

> [!NOTE]
> **Hinta lukittu** -ominaisuus voidaan poistaa yhdeltä tai usealta riviltä vain **Puhelinkeskus**-moduulia käytettäessä. Myyntipisteen toiminta ei muutu. Myyntipisteen käyttäjät eivät voi avata valittujen tilausrivien hintojen lukitusta. He voivat kuitenkin poistaa hinnan lukituksen kaikista aiemmin luoduista tilausriveistä valitsemalla **Laske uudelleen**.

### <a name="cancel-a-customer-order"></a>Asiakastilauksen peruuttaminen

1. Valitse **Peruuta tilaus**.
2. Syötä suodattimet ja etsi tilaus **Hae**-kohdan avulla. Valitse sitten **Käytä**.
3. Valitse tilaus tulosluettelosta ja valitse sitten **Peruuta**. Jos **Peruuta**-painike ei ole käytettävissä, tilaus on tilassa, jossa sitä ei voi enää peruuttaa.
4. Jos peruutusmaksut on määritetty, vahvista ne. Voit oikaista peruutusmaksuja ennen niiden vahvistamista tarpeen mukaan. 
5. Viimeistele peruutusprosessi tapahtuman ostoskorissa valitsemalla maksutoiminto. Jos maksetut talletukset ylittävät peruutusmaksun, saatetaan joutua maksamaan hyvitysmaksuja.
6. Jos haluat poistua peruutusprosessista tallentamatta muutoksia, voit käyttää **Mitätöi tapahtuma** -toimintoa.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Asiakastilauksen lähetyksen tai noudon viimeisteleminen myyntipisteessä

Kun tilaus on luotu, asiakas noutaa nimikkeet myymäläsijainnista tai ne lähetetään tilauksen määrityksestä riippuen. Lisätietoja prosessista on [myymälän tilauksen täyttämisen](./order-fulfillment-overview.md) dokumentaatiossa.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asiakastilausten tapahtumien asynkroninen työnkulku

Asiakastilauksia voi luoda myyntipisteessä joko synkronoidussa tai asynkronisessa tilassa. Jos asiakastilausten luomisen yhteydessä myyntipisteessä on suorituskykyonhgelmia tai käyttäjän viivettä, voit ottaa käyttöön asynkronisen tilauksen luomisen.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Ota käyttöön asiakastilausten luonti asynkronisessa tilassa

1. Valitse Commerce Headquarters -sovelluksen **Toimintoprofiilit**-sivulla määritettävää myymälää vastaava toimintoprofiili.
2. **Yleiset**-pikavälilehdessä määritä **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvoksi **Kyllä**.

Kun **Luo asiakastilaus asynkronisessa tilassa** -asetuksen arvo on **Kyllä**, asiakastilaukset luodaan aina asynkronisessa tilassa, vaikka Retail Transaction Service (RTS) -palvelu on käytettävissä. Jos määrität tämän asetuksen arvoksi **Ei**, asiakkaan tilaukset luodaan aina synkronoidussa tilassa RTS:n avulla. Kun asiakastilaukset luodaan asynkronisessa tilassa, ne noudetaan ja luodaan vähittäismyyntitapahtumina Commerce Headquarters -sovelluksessa kaupan noutotöinä. Vähittäismyyntitapahtumille luodaan vastaavat myyntitilaukset, kun **Synkronoi tilaukset** suoritetaan joko manuaalisesti tai eräprosessina.

## <a name="additional-resources"></a>Lisäresurssit

[Asiakkaiden yhdistelmätilaukset](hybrid-customer-orders.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
