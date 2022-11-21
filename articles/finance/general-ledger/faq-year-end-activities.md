---
title: Tilinpäätöstehtävien usein kysytyt kysymykset
description: Tässä artikkelissa on lueteltu kysymyksiä, joita tilinpäätöksen yhteydessä voi ilmetä, sekä niiden vastaukset, joista voi olla apua tilinpäätöstehtävissä.
author: moaamer
ms.date: 11/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a25f20c320b905a2cdd3091e76e3c5e73f1a845a
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752745"
---
# <a name="year-end-activities-faq"></a>Tilinpäätöstehtävien usein kysytyt kysymykset 

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on lueteltu kysymyksiä, joita tilinpäätöksen yhteydessä voi ilmetä, sekä niiden vastaukset, joista voi olla apua tilinpäätöstehtävissä. Tämän artikkelin tiedot koskevat ensisijaisesti kirjanpidon ja ostoreskontran tilinpäätöstehtäviä.

## <a name="general-ledger-year-end-enhancements"></a>Kirjanpidon tilinpäätöksen parannukset 
Version 10.0.20 myötä lisättiin tilinpäätöksen parannus, joka on käytössä oletusarvoisesti versiosta 10.0.25 alkaen. Jos organisaatiossa on käytössä aikaisempi versio kuin 10.0.25, suosittelemme ottamaan tämän ominaisuuden käyttöön ennen tilinpäätösprosessin aloittamista. Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat ominaisuuksien hallinnan työtilassa tarkistaa ominaisuuden tilan sekä ottaa sen käyttöön tarvittaessa. Työtilassa ominaisuus näkyy seuraavalla tavalla:

 - Moduuli: Kirjanpito
 - Ominaisuuden nimi: Kirjanpidon tilinpäätöksen parannukset

Tilinpäätösmallien asetukset on siirretty uudelle asetussivulle: **Tilinpäätösmallin asetukset**. Aiempi tilinpäätössivu muuttuu samantapaiseksi kuin kirjanpidon ulkomaanvaluutan uudelleenarvostuksen sivu, eli siinä näytetään luettelo aina, kun tilinpäätös suoritetaan tai peruutetaan. Kirjanpitäjä voi aloittaa tilinpäätöksen uudelta sivulta. 

Voit peruuttaa tilinpäätöksen valitsemalla kyseisen yrityksen viimeisimmän tilikauden ja valitsemalla **Peruuta tilinpäätös** ‑painikkeen. Peruutus poistaa edellisen tilinpäätöksen kirjanpitomerkinnät, eikä tilinpäätöstä suoriteta uudelleen automaattisesti. 

Voit suorittaa tilinpäätöksen uudelleen aloittamalla prosessin tilikaudelle ja yritykselle uudelleen. Prosessi käyttää edelleen kirjanpidon parametriasetusta sen määrittämiseen, otetaanko tilinpäätöksen uudelleen suorittamisessa huomioon vain uudet ja muuttuneet tapahtumat vai peruutetaanko edellinen tilipäätös kokonaan, minkä jälkeen prosessi suoritetaan uudelleen kaikille tapahtumille.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Kirjanpito: mistä tietää, että on suorittamassa tilinpäätöstä eikä kumoamassa sitä?
Organisaatiot ovat saattaneet yrittää suorittaa tilinpäätöstä, mutta ovatkin olleet kumoamassa tilinpäätöstä. Jos tilinpäätöksen suorittaminen vaikuttaa tapahtuvan todella nopeasti tai se ei tuota alkusaldoja, tarkista **Kumoa edellinen sulkeminen** ‑asetus kohdassa **Tilikauden lopetus** (**Kirjanpito > Kauden sulkeminen > Tilikauden lopetus > Suorita tilikauden lopetus**). 

[![Tilinpäätöksen suorittaminen verrattuna sen peruuttamiseen.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Jos **Kumoa edellinen sulkeminen** ‑asetukseksi on valittu **Kyllä**, edellinen tilinpäätös peruutetaan. Kun kumoaminen suoritetaan, kaikki loppusaldo- ja alkusaldomerkinnät poistetaan, ikään kuin tilinpäätöstä ei olisi missään vaiheessa suoritettukaan. Tositteet poistetaan. Tilinpäätöstä ei suoriteta uudelleen automaattisesti. Prosessi on aloitettava uudelleen siten, että **Kumoa edellinen sulkeminen** ‑asetuksen arvoksi muutetaan **Ei**. 

> [!NOTE]
> Loppusaldomerkinnän luominen suljettavalle vuodelle on valinnaista. Se luodaan vain, jos kirjanpitoparametrin **Luo päätöstapahtumat siirron yhteydessä** arvoksi on määritetty **Kyllä**. Alkusaldomerkintä luodaan aina, koska se on seuraavan vuoden alkusaldo.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Kirjanpito: mitä eroa on tilinpäätöksen kumoamis- ja sulkemisparametreilla?
Joillekin voi aiheuttaa hämmennystä, mitä eroa on parametreilla **Kumoa edellinen sulkeminen**, joka sijaitsee **Tilikauden lopetus** ‑valintaikkunassa, ja **Poista päätöstapahtumat siirron yhteydessä**, joka on kirjanpidossa (**Kirjanpito > Kauden sulkeminen > Tilikauden lopetus > Suorita tilikauden lopetus**).  

[![Tilinpäätöksen kumoamis- ja sulkemisparametrien välinen ero.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Valitsemalla tilinpäätöksen suorittamisen yhteydessä avattavasta valikosta **Kumoa edellinen sulkeminen** voit poistaa kaikki loppusaldo- ja alkusaldomerkinnät, ikään kuin tilinpäätöstä ei olisi missään vaiheessa suoritettu. Tositteet poistetaan. Tilinpäätöstä ei suoriteta uudelleen automaattisesti. Tilinpäätöksen suorittamiseksi tämä prosessi on aloitettava uudelleen siten, että **Kumoa edellinen sulkeminen** ‑asetuksen arvoksi muutetaan **Ei** (**Kirjanpito > Kirjanpidon asetukset > Kirjanpitoparametrit**). 

[![Kirjanpidon parametrin määrittäminen.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Kirjanpidon **Poista päätöstapahtumat siirron yhteydessä** ‑parametria käytetään vain suoritettaessa (ei kumottaessa) tilinpäätöstä (**Kumoa edellinen sulkeminen** ‑asetukseksi on määritetty **Ei**). Jos parametrin arvoksi määritetään **Kyllä**, kaikki loppusaldo- ja alkusaldomerkinnät poistetaan ja tilinpäätös suoritetaan uudelleen. Tätä prosessia käytetään, kun organisaatio haluaa kirjata kaikki tapahtumat, mukaan lukien edellisen tilinpäätöksen jälkeiset oikaisut, yhteen kirjanpitomerkintään loppusaldo- ja alkusaldomerkinnöissä. 

Jos tämän asetuksen arvoksi määritetään **Ei**, kaikki loppusaldo- ja alkusaldomerkinnät säilyvät. Niitä ei poisteta. Sen sijaan luodaan uusi loppusaldo- ja alkusaldomerkintä pelkästään erotukselle eli kyseisen tilikauden uusille, edellisen tilinpäätöksen jälkeen kirjatuille tapahtumille.  

> [!NOTE]
> Loppusaldomerkintä luodaan suljettavalle vuodelle. Näin tapahtuu vain, jos kirjanpidon parametrin **Luo päätöstapahtumat siirron yhteydessä** arvoksi on määritetty **Kyllä**. Alkusaldomerkintä luodaan aina, koska se on seuraavan vuoden alkusaldo. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Kirjanpito: mitä muutoksia voi tehdä tilinpäätöksen käsittelyn suorituskyvyn parantamiseksi? 
Voit tehdä useita muutoksia, jotka parantavat tilinpäätöksen käsittelyn suorituskykyä. Suosittelemme, että arvioit näiden ehdotettujen muutosten sopivuuden organisaatiollesi.  

### <a name="dimension-sets"></a>Dimensioyhdistelmät
Tilinpäätöksen suorittamisen yhteydessä kunkin dimensioyhdistelmän saldo muodostetaan uudelleen, mikä vaikuttaa suoraan suorituskykyyn. Jotkin organisaatiot luovat tarpeettomasti dimensioyhdistelmiä vain, koska niitä on jossain vaiheessa käytetty tai niitä saatettaisiin jossain vaiheessa käyttää.  Nämä tarpeettomat dimensioyhdistelmät muodostetaan edelleen uudelleen tilinpäätöksen yhteydessä, mikä pidentää käsittelyaikaa. Käy dimensioyhdistelmäsi läpi, arvioi ne ja poista mahdolliset turhat dimensioyhdistelmät.

Tarpeettomat dimensioyhdistelmät vaikuttavat myös **BudgetDimensionFocusInitializeBalance**-erätyöhön (**Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensioyhdistelmät**).

[![Taloushallinnon dimensioyhdistelmät.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Tilinpäätösmallin määritykset
Tilinpäätösmallin avulla organisaatio voi valita ylläpidettävän taloushallinnon dimension tason siirtäessään tulossaldoja jakamattomiin voittoihin. Asetusten avulla organisaatio voi ylläpitää yksityiskohtaisia taloushallinnon dimensioita (**Sulje kaikki**) siirtäessään saldoja jakamattomiin voittoihin tai tehdä summista yhteenvedon yksittäiseen dimensioarvoon (**Sulje yksittäinen**). Tämän voi määrittää kullekin taloushallinnon dimensiolle. Lisätietoja näistä asetuksista on artikkelissa [Tilinpäätös](year-end-close.md).

Suosittelemme arvioimaan organisaation tarpeet ja sulkemaan mahdollisimman monta dimensiota käyttämällä tilinpäätöksen **Sulje yksittäinen** ‑vaihtoehtoa suorituskyvyn parantamiseksi. Kun sulkeminen tapahtuu yksittäiseen dimensioarvoon (joka voi olla myös tyhjä arvo), järjestelmä laskee vähemmän yksityiskohtaisia tietoja määrittäessään jakamattomien voittojen tilivientien saldoja.

## <a name="degenerate-dimensions"></a>Johdetut dimensiot

Johdetulla dimensiolla ei ole juurikaan uudelleenkäyttöarvoa itsenäisesti eikä yhdessä muiden dimensioiden kanssa. Johdettuja dimensioita on kahta eri tyyppiä. Ensimmäinen tyyppi on yksittäin johdettu dimensio. Tavallisesti tämäntyyppinen degeneroitu dimensio näkyy vain yksittäisessä tapahtumassa tai pienissä tapahtumajoukoissa. Toinen tyyppi on dimensio, joka muuttuu johdetuksi yhdessä yhden tai useamman sellaisen muun dimension kanssa, joka ilmentää samoja mahdollisuuksia mahdollisten luotavien permutaatioiden perusteella. Johdetulla dimensiolla voi olla merkittävä vaikutus tilinpäätösprosessin suorituskykyyn. Voit minimoida suorituskykyongelmat määrittämällä tilinpäätöksen asetuksissa kaikille johdetuille dimensioille **Sulje yksittäinen** ‑asetuksen edellisessä osassa kuvatulla tavalla.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Kirjanpito: mitä Kauden sulkeminen – Tilikauden lopetus ‑ominaisuus tekee?
 
[![Kauden sulkeminen, tilikauden lopetus.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Taloushallinnon dimensiojoukkojen uudelleenmuodostuksen suorituskykyparannukset
Versioon 10.0.16 lisätty uusi ominaisuus parantaa tilinpäätös- ja konsolidointiprosessien suorituskykyä. Ominaisuuden nimi on ”Taloushallinnon dimensioyhdistelmien uudelleenmuodostuksen suorituskykyparannukset”. Tämä ominaisuus muuttaa dimensioyhdistelmien uudelleenmuodostustapaa niin, että ne muodostetaan uudelleen vain olennaisen aikavälin ajaksi. Edellisissä versioissa dimensioyhdistelmät muodostettiin uudelleen kaikille päivämäärille. Jos olet esimerkiksi sulkemassa vuotta 2020, järjestelmä muodostaa uudelleen vain tilikauden 2020 tapahtumien saldot. Jos olet suorittamassa konsolidointia päivämäärävälille 1.11.2020–30.11.2020, järjestelmä muodostaa uudelleen vain kyseisen päivämäärävälin saldot.

Ennen kuin voit käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat ominaisuuksien hallinnan työtilassa tarkistaa ominaisuuden tilan sekä ottaa sen käyttöön tarvittaessa. Työtilassa ominaisuus näkyy seuraavalla tavalla:
 
- Moduuli: Kirjanpito
- Ominaisuuden nimi: taloushallinnon dimensioyhdistelmien uudelleenmuodostuksen suorituskykyparannukset

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Ostoreskontra: mitä muutoksia vuodelle 2022 on tehty vuoden lopun 1099-raportoinnin tueksi?

#### <a name="update-to-all-1099-forms"></a>Päivitys kaikkiin 1099-lomakkeisiin
Vuoden 2022 verovuoden kaikkiin 1099-lomakkeisiin on tehty seuraavat muutokset:

  - Vuonna 2021 vuosi oli kiinteänä 1099-lomakkeissa. Vuodesta 2022 alkaen raportti täyttää vuositiedon. 

#### <a name="1099-misc"></a>1099-MISC
Verovuoden 2022 lomakkeeseen 1099-MISC on tehty seuraavat päivitykset:

 - Ruutu 13: näyttää nyt FATCA (Foreign Account Tax Compliance Act) ‑ilmoitusvaatimuksen. 
 - Rasia 14: käytetään nyt ylimääräisten "kultaisten laskuvarjomaksujen" raportointiin. 
 - Ruutu 15: käytetään nyt ylimääräistä kompensaation lykkäystä koskevien NQDC (nonqualified deferred compensation) ‑suunnitelmien alaisten maksujen raportointiin. 
 - Ruutu 16: käytetään nyt osavaltion ennakonpidätysten raportointiin.
 - Ruutu 17: käytetään nyt maksajan osavaltionumeron raportointiin.
 - Ruutu 18: käytetään nyt osavaltion tuloveron tulojen raportointiin. 

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Ostoreskontra: mitä muutoksia vuodelle 2021 on tehty vuoden lopun 1099-raportoinnin tueksi?

Vuonna 2021 DIV-, NEC- ja MISC-lomakkeita on hieman muutettu, ja joitakin ruutuja on lisätty.

#### <a name="div-new-box2e-2f"></a>DIV: uusi ruutu 2e, 2f
 
- Ruutu 2e. Näyttää ruudussa 1a olevan summan osuuden, joka on osan 897 mukaista USRPI:n (kiinteän omaisuuden omistukset Yhdysvalloissa) luovutuksesta saatua voittoa.  
- Ruutu 2f. Näyttää ruudussa 2a olevan summan osuuden, joka on osan 897 mukaista USRPI:n luovutuksesta saatua voittoa. Huomaa, että ruudut 2e ja 2f koskevat vain ulkomaisia henkilöitä ja tahoja, joiden tulojen luonne säilyy, kun ne välitetään tai jaellaan niiden suorille tai epäsuorille ulkomaisille omistajille tai edunsaajille. Tätä käsitellään tosiasiallisena kytköksenä kauppaan tai liiketoimintaan Yhdysvalloissa. Katso lisätietoja veronpalautusta koskevista ohjeista. 
 
#### <a name="nec-new-box-2"></a>NEC: uusi ruutu 2 
 
Jos ruutu 2 on valittuna, ilmoita kulutustuotteet, joiden yhteissumma on 5 000 $ tai enemmän, jotka on myyty sinulle jälleenmyyntiä varten, osto-myyntisopimuksella, etumaksutoimeksiantona tai muulla perusteella. Yleisesti ottaen ilmoita kaikki näiden tuotteiden myynnistäsi saadut tulot aikataulussa C (lomake 1040). 
 
NEC:n lomakkeen kokoa on myös muutettu. Tulostuksessa sivulle tulostetaan kolme lomaketta. 
 
#### <a name="misc-new-box-11"></a>MISC: uusi ruutu 11 
 
Ruudussa 11 näkyy maksettu summa kalan ostosta jälleenmyyntiin keneltä tahansa kalastusta harjoittavalta henkilöltä. Katso tämän tulon ilmoittamista koskevat veronpalautuksen ohjeet. 
 
#### <a name="electronic-filing"></a>Sähköiset ilmoitukset 
Lisätietoja sähköisistä ilmoituksista on [julkaisussa sähköisten ilmoitusten vaatimuksista](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Muotoilumääritysten ja tietueasetteluiden päivitys vuoden 2021 sähköiseen raporttiin 
- Osio 2 Myöntäjän A-tietue. 
- Summakoodit – kasvatettu kentän sijaintia 28-45, pituudeksi 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Osio 2 Myöntäjän A-tietue, 1099-DIV-lomakkeen maksujen raportointia varten: 
- Summan tyyppi – Lisätty osio 897 Tavalliset osingot ja lisätty summakoodi H. 
- Summan tyyppi – Lisätty osio 897 Pääomavoitot ja lisätty summakoodi J. 
 
#### <a name="sec-3-payee-b-record"></a>Osio 3 Maksunsaajan B-tietue 
- Yleistietojen tietueet – päivitetty kolmas kohta 16:sta 18:aan maksun summakenttään. 
- Kentän otsikko Maksu H – päivitetty kentän sijainti 247-258, kentän otsikko, pituus ja yleinen kentän kuvaus. 
- Kentän otsikko Maksu J – päivitetty kentän sijainti 259-270, kentän otsikko, pituus ja yleinen kentän kuvaus. 
- Päivitetty tyhjä kenttä kentän sijaintiin 271-286. 
- Päivitetty ulkomaan ilmaisin kentän sijaintiin 287. 
- Päivitä ensimmäisen maksunsaajan nimirivin kenttä kentän sijaintiin 288-327. 
- Päivitä toisen maksunsaajan nimirivin kenttä kentän sijaintiin 328-367. 
- Tietueasettelun sijainnit, lomake 1099-MISC – Poistettu kentän sijainti 548 ja kentän otsikko FATCA-ilmoitusten vaatimusten ilmaisin. 
- Tietueasettelun sijainnit, lomake 1099-NEC – päivitetty 545-546 tyhjäksi, päivitetty 547-kenttään suoramyynnin ilmaisin, pituus ja kuvaus ja huomautukset, päivitetty 548-722 -kenttä tyhjäksi. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Osio 4 Myöntäjän C-tietueen loppu 
- Kentän otsikko Maksu H – päivitetty kentän sijainti 304-321, kentän otsikko, pituus ja yleinen kentän kuvaus. 
- Kentän otsikko Maksu J – päivitetty kentän sijainti 322-339, kentän otsikko, pituus ja yleinen kentän kuvaus. 
- Kentän otsikko 340-499 – päivitetty pituudeksi 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>Osio 5 Osavaltion kokonaissummien K-tietue 
- Kentän otsikko Maksu H – päivitetty kentän sijainti 304-321, kentän otsikko, pituus ja yleinen kentän kuvaus. 
- Kentän otsikko Maksu J – päivitetty kentän sijainti 322-339, kentän otsikko, pituus ja yleinen kentän kuvaus. 
- Kentän otsikko 340-499 – päivitetty pituudeksi 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Ostoreskontra: 1099 – kuinka muutan sellaisen toimittajan 1099-ruutua ja -arvoja, joka ei ole seurannut 1099-tietoja koko vuoden ajan?
Käytä Päivitä valmistevero ‑toimintoa (**Ostoreskontra > Toimittajat > Kaikki toimittajat > Valitse toimittaja > Toimittaja-välilehti valintanauhassa > Päivitä valmistevero**), jos haluat käydä aiemmin maksetut laskutapahtumat läpi ja määrittää 1099-tiedot uudelleen **Toimittaja**-sivun **Valmistevero (1099)** ‑välilehden asetusten mukaisesti.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Voinko suorittaa Päivitä valmistevero (1099) ‑toiminnon kaikille toimittajille yhdellä kertaa?
Et voi. Päivitä valmistevero (1099) ‑toiminto suoritetaan yhdelle toimittajalle kerrallaan. Jos organisaatiollasi on tällainen tarve, äänestä ideaa [Toimittajan 1099-tietojen päivittämisen eräkäsittely](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Ostoreskontra: 1099 – Päivitä valmistevero ‑työkalun vaihtoehdot ”Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen” ja ”Päivitä kaikki”
**Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** -valintaruutu palauttaa 1099-summan maksettujen arvojen kokonaissummaksi, kun sitä käytetään yhdessä **Päivitä kaikki** ‑valintaruudun kanssa. 

[![Valmisteverotapahtumat (1099): ennen päivitysrutiinin suorittamista.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

**Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** ‑valintaruutu tulee käyttöön vain, kun laskussa on osa osittaisia 1099-arvoja tai jos sitä on muutettu Valmistevero (1099) ‑lomakkeessa. Oletetaan esimerkiksi, että sinulla on lasku, jonka arvo on 1 000,00 $, mutta käyttäjä kirjoittaa laskulle manuaalisesti 1099-summan 500,00 $.

[![Valmisteverotapahtumat: sekä Päivitä kaikki- että Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen ‑valintaruutujen valitseminen.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Kun tämä maksetaan, maksettava 1099-summa on 500,00 $. Jos suoritat uudelleenlaskentarutiinin, järjestelmä muuttaa 1099-summaksi 1 000,00 $, joka on maksettu kokonaissumma.

[![Valmisteverotapahtumat: 1099-rutiinin suorittamisen jälkeen.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Ostoreskontra: 1099 – 1099-tapahtumien luominen manuaalisesti
Organisaation voi olla tarpeen luoda manuaalisesti 1099-tapahtumia, joita ei ole liitetty laskuun. Voit lisätä 1099-tapahtumia manuaalisesti valitsemalla **Ostoreskontra > Kausittaiset tehtävät > Valmistevero (1099) > Toimittajien tilitykset valmisteveroja (1099) varten**. Valitse **Manuaaliset 1099-tapahtumat** -painike. 

Manuaalisesti luotuja 1099-tapahtumia ei päivitetä **Päivitä kaikki** -prosessilla tai **Laske aiemmin määritetyt valmisteverosummat (1099) uudelleen** ‑prosessilla **Päivitä valmistevero** ‑työkalussa.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Ostoreskontra: 1099 – tukeeko Dynamics 365 Finance 1096-lomaketta? 

Dynamics 365 Finance ei tulosta 1096 Annual Summary and Transmittal of US Information Returns -lomaketta.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Ostoreskontra: 1099 – onko uusia ominaisuuksia, jotka tukevat julkisen sektorin 1099-raportointia? 
Ratkaisuun on lisätty uusi julkisen sektorin ominaisuus **Päivitä 1099-tiedot päätilin mukaan**, jonka voit ottaa käyttöön **Ominaisuuksien hallinta** ‑työtilassa. Tämän ominaisuuden avulla voit liittää toimittajan 1099-arvot kirjanpidollisen jaon päätilin mukaan toimittajatietueen oletustilin sijaan.

Lisätietoja on ohjeaiheessa [1099-raportoinnin toimittajien asetukset](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
