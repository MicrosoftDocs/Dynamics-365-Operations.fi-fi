---
title: Toimittajan ostohyvitykset
description: "Tämä ohjeaihe sisältää yhteenvedon yleisimmistä tehtävistä, joita suoritetaan toimittajan ostohyvitysten yhteydessä. Toimittajan ostohyvitysten avulla yritykset voivat hallita toimittajan ostohyvitysohjelmiaan paremmin automatisoimalla tehtäviä, joilla hallitaan, seurataan ja haetaan ansaittuja ostohyvityksiä."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ae5ee60238b951779c7790870e6c6adfba55d7d
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-rebates"></a>Toimittajan ostohyvitykset
[!include [banner](../includes/banner.md)]

Toimittajan ostohyvitysten avulla yritykset voivat hallita toimittajan ostohyvitysohjelmiaan paremmin automatisoimalla tehtäviä, joilla hallitaan, seurataan ja haetaan ansaittuja ostohyvityksiä.

Tämä ohjeaihe sisältää yhteenvedon yleisimmistä tehtävistä, joita suoritetaan toimittajan ostohyvitysten yhteydessä. Yhteenveto kattaa seuraavat tehtävät:

- Ostohyvityssopimuksen tietojen tarkastelu
- Tunnista tilaukset, jotka ovat oikeutettuja ostohyvitykseen ja luo ostohyvitysvaatimuksia.
- Tarkista ja hyväksy vaatimuksia.

## <a name="audience-and-purpose"></a>Käyttäjäryhmät ja tarkoitus

Tämän ohjeaiheen tiedot on tarkoitettu konserniyritysten päätöksentekijöille, kuten ostopäälliköille, talousjohtajille (CFO) ja kirjanpidon päälliköille, joilla on seuraavat vastuut:

- Toimittajahintojen, alennusten ja ostohyvityssopimusten neuvottelu.
- Ostohyvitysvaatimuksia käsittelevien ja maksuja keräävien työntekijöiden johtaminen.
- Varaston hankinta parhaalla mahdollisella hinnalla.

Näitä tehtäviä toteuttavat henkilöt haluavat saavuttaa useita tavoitteita. Seuraavassa on muutamia esimerkkejä:

- Käyttää useita erilaisia toimittajia koskevia kampanjaohjelmia ja ostohyvitysehtoja.
- Vähentää johdon painetta sekä virheitä, jotka liittyvät kampanjoiden suorituskyvyn valvontaan ja vaatimusten käsittelyyn.
- Parantaa kassavirtaennusteita jaksottamalla tulevia myyntejä.
- Käyttää arvotettua perustetta nykyisille ja tuleville toimittajaneuvotteluille ostohyvityksiin liittyen.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Toimittajan ostohyvityssopimuksen tietojen tarkastelu
Toimittajan ostohyvityssopimus on sopimustietue, joka määrittää toimittajan kanssa sovitut ehdot, joiden perusteella yritys on oikeutettu rahapalkkioon saavuttaessaan määrättyjä ostotavoitteita. Toimittajan ostohyvityssopimukset kirjataan **Ostohyvityssopimukset**-sivulla.

Avaa **Toimittajan ostohyvityssopimukset** -sivu ja valitse **Hankinta** &gt; **Toimittajan ostohyvitykset** &gt; **Ostohyvityssopimukset**.

![Ostosopimus](media/purchase-agreement.PNG)

**Toimittajan ostohyvityssopimukset** -sivulla voit tarkastella tietoja toimittajasopimuksessa sovituista ehdoista.

Sopimuksen otsikossa määritetään yleiset ehdot, jotka oikeuttavat yrityksen ostohyvitykseen. Käytännössä otsikkotiedot määrittävät, että toimittaja antaa ostohyvityksen, kun tiettyä tuotetta ostetaan tietty määrä. Otsikossa määritetään myös ostohyvityksen mittayksikkö ja päivämäärän laskentatyyppi.

- Voit määrittää **Yleiset**-välilehden **Ostohyvitysvaihtoehdon mittayksikkö** -kenttään, voiko ostotilausrivillä käyttää hyvitysehtona mittayksikköä. 

    - **Muunna** – ostotilausrivi on oikeutettu toimittajan ostohyvitykseen sopimuksen mukaisesti. Ostohyvitys myönnetään rivillä käytetystä mittayksiköstä huolimatta.
    - **Täsmälleen** – ostohyvityksellä on oltava sopimuksessa määritetty mittayksikkö, jotta ostohyvitys voidaan myöntää.

- Valitse **Yleiset** -välilehden **Laskentapäivätyyppi** -kentässä päivämäärä, jonka perusteella määritetään, onko osto tapahtunut ostohyvityssopimuksen voimassaoloaikana.

    - **Luotu** – käytetään ostotilauksen luontipäivämäärää.
    - **Pyydetty toimitus** – käytetään pyydettyä toimituspäivämäärää.

Voit määrittää sopimusriveillä toimittajan ostohyvityssopimukselle tarkempia ehtoja.

- **Ostojen kumulointiperuste** -kentässä voit valita ostohyvitysvaatimuksen laskentatavan. Summa voidaan määrittää riippuvaiseksi aikajaksosta (viikko, kuukausi, vuosi, käyttöikä tai mukautettu kausi). **Lasku**-arvo tarkoittaa, että ostohyvitysvaatimus määritetään aina, kun ostotilausrivi laskutetaan.
- **Oton lähde** -kentässä voit määrittää ostohyvityksen laskentatavan perusteen.

    - **Brutto** – Ostohyvitys lasketaan nimikkeen bruttohinnan perusteella.
    - **Netto** – Ostohyvitys lasketaan nimikkeen nettohinnasta (eli hinta alennusten jälkeen).

- **Ostohyvitysohjelman jaksotus** ja **Ostohyvitysohjelman kulutili** -kenttiin numerot tileille, jotka vastaanottavat ostohyvityksen jaksotetut summat hyväksynnän ja käsittelyn välisenä aikana.
- Kun **Vaatii hyväksynnän** -asetukseksi on määritetty **Kyllä**, ostohyvitysvaatimus on hyväksyttävä ennen sen kerryttämistä tai maksamista.
- Ostohyvitysten peruste näkyy **Ostohyvitysrivin vaihtotyyppi** -kentässä.

    - **Määrä** – ostohyvitykset ovat tilavuusperusteisia.
    - **Summa** – ostohyvitykset ovat summaperusteisia.

- **Rivit** -pikavälilehdellä näet, miten voit määrittää useita määrätasoja myöntämään eritasoisia ostohyvityksiä. Edellisen kuvan esimerkin mukaisesti **Arvosta** ja **Arvoon** -kentät ilmaisevat, että kun tuotteen määrä on välillä 10–19, ostohyvityksen määrä on 15 USD yksikköä kohden.

    > [!NOTE]
    > **Arvosta**-arvo on sisällyttävä ja **Arvoon** on poissulkeva. Esimerkiksi **Ostohyvitysrivin vaihtotyyppi** -kentän arvoksi on asetettu **Määrä**, ja annat **Arvosta**-kentän arvoksi **1** ja **Arvoon**-kentän arvoksi **3**. Tässä tapauksessa ostohyvitys myönnetään, kun ostat yhden tai kaksi nimikettä, mutta ei kolmea nimikettä ostettaessa.

- **Työnkulun hyväksyntätila** -kentän **Hyväksytty**-arvo ilmaisee, että sopimusta voidaan käyttää ostotilauksilla, jotka täyttävät sopimuksen ehdot.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Tunnista tilaukset, jotka ovat oikeutettuja ostohyvitykseen ja luo ostohyvitysvaatimuksia

Kun ostotilaukset sijoitetaan toimittajalle, jolla on ostohyvityssopimus yrityksen kanssa, ohjelma tunnistaa kaikki tulevat toimittajan hyvitysmaksut. Jos ostotilauksille voidaan myöntää hyvitys, kullekin tilausriville luodaan hyvitysvaatimus heti, kun ostolasku kirjataan. Prosessi on automaattinen. Voit myöhemmin tarkastella odotettuja ostohyvityksiä ja nähdä hyvitysten vaikutuksen tuotteen kustannuksiin ja katetuottoon.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Tarkastele tietoja hyvityksistä, joita on käytetty ostotilausriville toimittajan ostohyvityssopimuksen mukaisesti
1. Valitse **Ostotilaukset**-sivulla tilausrivi ja sitten **Ostotilausrivi** &gt; **Näytä** &gt; **Hintatiedot**.
2. Valitse **Hintatiedot**-sivulta **Ostohyvitykset**-pikavälilehti.

Ostohyvityksen tiedot näkyvät myös **Toimittajan ostohyvitys** -kentässä **Hintatiedot**-sivun **Marginaaliarvio**-osassa.

> [!NOTE]
> Varmista **Hankintaparametrit**-sivun **Hinnat**-välilehdellä, että **Ota käyttöön hintatiedot** -asetukseksi on määritetty **Kyllä**. Jos tämä asetus on **Ei**, et voi tarkastella ostohyvityksiä.

## <a name="review-and-approve-claims"></a>Tarkista ja hyväksy vaatimuksia
Luodut ostohyvitysvaatimukset vastaavat toimittajalta odotettavia, tulevia maksuja. Ennen hyvityslaskun lähettämistä toimittajalle, sopimuksen omistaja haluaa yleensä tarkistaa vaatimukset ja hyväksiä ne. Huomaa kuitenkin, että vaatimuksen tila määrittää, onko vaatimus valmis hyväksyttäväksi.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Vaatimusten tilat ja niiden vaikutus hyväksyntäprosessiin
Kun vaatimus on luotu, sen tilaksi tulee **Lasketaan**, jos ostohyvitys myönnetään kumulatiivisena tai **Laskettu**, jos hyvitys myönnetään laskukohtaisesti. Jos vaatimuksen tila on **Lasketaan**, sen on käytävä läpi laskentaprosessi, josta vastaa Kumuloi-toiminto. Vain vaatimukset, joiden tila on **Laskettu** voidaan sisällyttää hyväksyntäprosessin.

> [!NOTE]
> Jos **Vaatii hyväksynnän** -asetus toimittajan ostohyvityssopimuksella on **Ei**, kaikkien luotujen vaatimusten tila on **Hyväksytty**. Hyväksyntä on pakollinen vaatimuksille, jotka myönnetään kumulatiivisesti.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Hyväksy vaatimuksia sekä tarkastele kirjauksia ja laskutietoja
Kun saatavat on hyväksytty, ne voidaan käsitellä ostoreskontrassa (A/P). Hyvityslasku (toimittajalasku) luodaan automaattisesti hyvityksen vaatimussummalle. Hyvityksen voi sitten lisätä toimittajan saldoon, ja ostoreskontraryhmä voi sisällyttää sen säännölliseen selvitysprosessiin.

1. Valitse **Hankinta** &gt; **Toimittajan ostohyvitykset** &gt; **Hyvitysvaatimukset** avataksesi hyvitysvaatimuksen.
2. Ostohyvitysvaatimuksen sulkeminen.
3. Valitse vaatimus ja sitten toimintoruudusta **Hyväksy**.
4. Valitse pyyntösivun **Toimittaja**-kentässä toimittaja, jolta olet oikeutettu vastaanottamaan ostohyvityksiä ja valitse sitten **OK**.

    Vaatimuksen summalle kirjataan Ostohyvityksen jaksotuskirjauskansio. Kirjaus veloittaa kertyneiden toimittajan ostohyvitysten saatavatililtä odotetun toimittajan maksun ja siirtää kertyneiden toimittajan ostohyvityssaatavien välitilille odotetun voiton.

    ![Viesti](media/message.png)

5. Valitse ostohyvitysluettelossa rivi ja valitse sitten toimintoruudussa **Ostohyvitystapahtumat**, jos haluat tarkastella ja siirtyä tämän ostohyvityksen kertymäkirjauksen kirjauskansion eränumeroon.

    Vaatimusten siirtämiseksi tavalliseen ostoreskontraprosessiin reskontrakäsittelijän on nyt tehtävä hyvitysvaatimus valmiiksi suorittamalla Käsittele-toiminto.

6. Valitse toimintoruudussa **Käsittele**, ja valitse sitten **Suodata**. Valitse **Ehdot**-kenttään **Toimittajatili**-kentässä toimittaja, jonka ostohyvitysvaatimuksia haluat käsitellä, aseta muut tarvittavat suodattimet ja valitse **OK**.

    Sanomapalkit ja se, että tilaksi tulee **Valmis** ilmaisee, että seuraavat tapahtumat ovat tapahtuneet:

    - Ostohyvityksen jaksotuksen kirjaus on palauttanut aiemmat välisummat kertymien saatava- ja kulutileiltä.
    - Toimittajalasku (hyvityslasku) on luotu ostohyvityksen summalle.

        > [!NOTE]
        > **Manuaalinen laskun kirjaus** -asetuksen arvo **Hankintaparametrit**-sivun **Ostohyvitysohjelma** -välilehdellä määrittää, kirjataanko toimittajalasku manuaalisesti tai automaattisesti osana vaatimusten käsittelyä.

    - Kun toimittajalasku kirjataan joko automaattisesti tai manuaalisesti, toimittajan maksutiliä on veloitettu, ja Saadut alennukset ja palkkiot -tiliä on hyvitetty.

        > [!NOTE] 
        > Saadut alennukset ja palkkiot -tilin numero määritetään hankintaluokassa, jota käytetään ostohyvityksen ostolaskun rivillä. Hankintaluokka puolestaan on määritetty **Hankintaparametrit**-sivun **Ostohyvitysohjelma**-välilehdellä.

7. Valitse ostohyvitysluettelossa rivi ja valitse sitten toimintoruudussa **Ostohyvitystapahtumat**, jos haluat tarkastella ja siirtyä tämän ostohyvityksen kertymäkirjauksen kirjauskansion eränumeroon sekä toimittajan laskun numeroon.
8. Valitse toimittajan laskutapahtuman rivi ja valitse sitten toimintoruudussa **Toimittajan lasku**. Jos toimittajalasku on kirjattu, näet laskukirjauskansion. Muussa tapauksessa näyttöön tulee toimittajan lasku odottavana toimittajan laskuna, joka edellyttää manuaalista kirjausta.

    Laskurivi määrittää toimittajalaskun tiedot **Provisiot ja ostohyvitykset** -hankintaluokkaan.

9. Valitse **Kaikki toimittajat** -sivulla toimittaja, jolta ostohyvitys vastaanotetaan, ja valitse sitten toimintoruudusta **Tapahtumat**. Etsi laskun rivi. Ostohyvityksen summa on lisätty toimittajan saldoon.

## <a name="summary"></a>Yhteenveto
Toimittajan ostohyvitysten käsittelyyn käytettävä prosessi sisältää useita, manuaalisia seurantatehtäviä, jotka ovat usein pitkäveteisiä. Näiden tehtävien automatisointi toimittajan ostohyvitysten hallintatoiminnon avulla voi helpottaa seuraavien prosessien käsittelyä:

- Tarkkojen ostohyvitysvaatimusten muodostaminen
- Odotettujen saatavien kerryttäminen ja väliaikainen kirjaaminen kirjanpitoon
- Toimittajasaldon ja tuloslaskelman päivittäminen erääntyvällä korvauksella

