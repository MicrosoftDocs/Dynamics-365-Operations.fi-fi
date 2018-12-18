---
title: "Käyttäjäkokemuksen mukauttaminen"
description: "Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Finance and Operationsin mukauttamista."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7344f460fcb443a78b254e2387fbf5c9134bf674
ms.openlocfilehash: 1860b603f789aabca1ca58848a88e11a6e08e31f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---

# <a name="personalize-the-user-experience"></a>Käyttäjäkokemuksen mukauttaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Finance and Operationsin mukauttamista.

Finance and Operationsissa on kolme mukauttamisen perusluokkaa.

- Asetussivulla tehtävät mukautukset. Väriteema ja aikavyöhyke ovat niistä esimerkkejä.
- Sivun käyttöön liittyvät mukautukset, joita kutsutaan *implisiittisiksi* mukautuksiksi. Finance and Operations esimerkiksi seuraa ruudukoiden sarakeleveyksiä, jos muutat niitä, sekä pikavälilehtien laajennus- tai tiivistystiloja.
- Kun käyttäjän mukautukset muokkaavat sivun ulkoasua muuttamalla tapaa, jolla elementti näkyy tai toimii kyseisellä sivulla, käytössä on usein ollut vuorovaikutteinen mukautustila. Näitä mukautuksia kutsutaan *eksplisiittisiksi* mukautuksiksi. Käyttäjä voi esimerkiksi lisätä sivulle elementtejä, piilottaa ne tai muuttaa niiden järjestystä.

Kaikki käyttäjän Finance and Operationsissa tekemät mukautukset koskevat vain kyseistä käyttäjää riippumatta mukautuksen tyypistä tai yrityksestä, jonka kanssa käyttäjä on vuorovaikutuksessa. Yhden käyttäjän sivulle tekemät muutokset eivät vaikuta järjestelmän muihin käyttäjiin.

## <a name="system-wide-options-for-the-current-user"></a>Nykyisen käyttäjän järjestelmänlaajuiset vaihtoehdot

**Käyttäjän asetukset** -sivulla on useita nykyisen käyttäjän koko järjestelmää koskevia asetuksia. Avaa **Käyttäjän asetukset** -sivu valitsemalla **Asetukset**-valikko (rataskuvake) siirtymispalkissa. Valitse sitten **Käyttäjän asetukset**. **Käyttäjän asetukset** -sivulla on neljä välilehteä, joissa erilaisia käyttäjäasetuksia:

- **Visuaalinen** – valitse sivun elementtien väriteema ja oletuskoko.
- **Valitse** – Valitse oletusarvot, joita käytetään aina, kun avaat Finance and Operationsissa. Näitä arvoja ovat esimerkiksi yritys, ensimmäinen sivu sekä näkymän tai muokkauksen oletustila. (Näkymä- tai muokkaustila määrittää, lukitaanko sivu näyttämistä varten vai avataanko se muokattavaksi aina, kun avaat sen.) Tässä välilehdessä on kieli- ja aikavyöhykeasetukset sekä päivämäärä-, kellonaika- ja numeromuotoilun asetukset. Tässä välilehdessä on lisäksi sekalaisia asetuksia,, jotka vaihtelevat julkaisuversiosta toiseen.
- **Tili** – käyttäjänimen ja muiden tiliin liittyvien asetusten säätäminen.
- **Työnkulku** – työnkulkuun liittyvien asetusten valitseminen.

## <a name="implicit-personalizations"></a>Implisiittiset mukautukset

Implisiittiset mukautukset ovat mukautuksia, joita tehdään olemalla vuorovaikutuksessa ohjausobjektien kanssa, jotka muistavat nykyisen näkyvän tilan.

- **Ruudukon sarakkeet** – Ruudukon sarakkeen leveyttä voidaan säätää valitsemalla koon muuttamiseen tarkoitettu palkki sarakkeen otsikon vasemmalla tai oikealla puolella ja vetämällä sitä vasemmalle tai oikealle, kunnes sarake on halutun levyinen. Finance and Operations tallentaa sarakkeelle määritetyn leveyden. Sarakkeen leveys muutetaan jatkossa tähän leveyteen aina, kun avaat ruudukon sisältävän sivun.
- **Pikavälilehdet** – Joillain sivuilla on laajennettavia *pikavälilehtinä* tunnettuja osia. Finance and Operations tallentaa tietoja laajennetuista ja tiivistetyistä pikavälilehdistä. Kun tämän jälkeen palaat sivulle, pikavälilehdet näkyvät joko laajennettuina tai tiivistettyinä sen mukaan, mitä olet valinnut sivulla edellisellä kerralla. Joissain tapauksissa voit parantaa järjestelmän suorituskykyä tiivistämällä pikavälilehden, koska Finance and Operationsin ei tarvitse noutaa tietoja kyseistä pikavälilehteä varten ennen kuin se laajennetaan. Toisaalla tässä ohjeaiheessa kertaan, miten voit myös muuttaa sivulla olevien pikavälilehtien järjestystä.
- **Tietoruudut** – Joillain sivuilla on *tietoruuduiksi* kutsuttuja osia. Tässä ruudussa on vain valitun sivun aihepiiriin liittyvää vain luku -muotoista tietoa. Kutakin Tietoruutu-ruudun osaa kutsutaan *tietoruuduksi*. Voit piilottaa tai näyttää koko Tietoruutu-ruudun. Voit myös laajentaa tai tiivistää yksittäisiä tietoruutuja. Finance and Operations tallentaa valintasi. Kun palaat tämän jälkeen sivulle, Tietoruutu-ruudun ja yksittäisten tietoruutujen tila palautetaan sen mukaan, mitä olet valinnut sivulla edellisellä kerralla. Joissain tapauksissa voit parantaa järjestelmän suorituskykyä tiivistämällä tietoruudun, koska Finance and Operationsin ei tarvitse noutaa tietoja kyseistä tietoruutua varten ennen kuin se laajennetaan.
- **Toimintoruudut** – *Toimintoruutu* näkyy useimmilla sivuilla yläreunan lähellä. Toimintoruudussa on painikkeita, joilla voi tehdä monia valitulla sivulla tehtäviä toimintoja. Nämä painikkeet on usein järjestetty välilehtiin. Voit kiinnittää koko toimintoruudun avoimeksi. Vaihtoehtoisesti voit sen oletusasetukseksi tiivistämisen. Kun seuraavan kerran avaat sivun, Finance and Operations palauttaa toimintoruudun kiinnitetyn tilan. Jos toimintoruutu on kiinnitetty avoimeksi, Finance and Operations näyttää myös viimeksi käytettyjen toimintojen välilehden.
- **Pikasuodattimet** – *Pikasuodatin* näkyy monien ruudukoiden yläpuolella. Pikasuodattimia voi käyttää ruudukon suodattamiseen valitun sarakkeen perusteella. Finance and Operations tallentaa sarakkeen, johon suodatus perustuu. Kun avaat seuraavan kerran sivun, jolla kyseinen ruudukko on, ruudukko suodatetaan saman sarakkeen perusteella. Voit kuitenkin suodattaa ruudukon tämän jälkeen toisen sarakkeen perusteella.
- **Sarakeotsikon suodattimet** – Kun ruudukkoa suodatetaan *sarakeotsikon suodattimilla*, suodatinoperaattori voidaan tarvittaessa vaihtaa etsittävien tietojen mukaan. Voit esimerkiksi vaihtaa operaattorin **alkaa** operaattoriksi **on täsmälleen**. Aina kun käytät sarakeotsikon suodatinta ja muokkaa suodatinoperaattoria, Finance and Operations tallentaa muutoksen. Tämän jälkeen suodatinoperaattori palautetaan, kun suodatat kyseistä saraketta seuraavan kerran.
- **Siirtymisruutu** – Voit avata *navigointiruudun* valitsemalla **Valikko**-painikkeen minkä tahansa sivun vasemmassa ruudussa. (**Valikko**-painikkeessa on *allekkain* *useita* *viivoja*.) Voit kiinnittää siirtymisruudun avoimeksi tai pitää sen oletusarvoisesti tiivistettynä. Kun olet kiinnittänyt siirtymisruudun avoimeksi, Finance and Operations pitää sen avoimena siihen asti, että tiivistät sen.

## <a name="explicit-personalizations"></a>Eksplisiittiset mukautukset

Tietojen tärkeys vaihtelee käyttäjä- ja yrityskohtaisesti. Toisin sanoen tiedot, jotka ovat välttämättömiä jollekin ovat liiketoiminnan kannalta merkityksettömiä jollekin toiselle. Finance and Operationsin on mahdollista muokata tapaa, jolla tiedostot järjestetään ja miten niitä käytetään. Voit myös määrittää tietyt tiedot piilotettaviksi. Nämä ominaisuudet ovat esimerkkejä eksplisiittisistä mukautuksista, ja ne ovat ratkaisevan tärkeitä henkilökohtaisen ja tuottavan kokemuksen kannalta. Eksplisiittinen mukauttaminen on mukauttamista, jonka nimenomaisena tarkoituksena on muuttaa elementin tai sivun ulkoasua tai toimintaa.

### <a name="shortcut-menu-options"></a>Pikavalikkovaihtoehdot

Pikavalikkojen avulla sivua voi eksplisiittisesti muuttaa muutamalla tavalla siten, että se vastaa paremmin omia tai yrityksen vaatimuksia. (Pikavalikkoa kutsutaan myös *hiiren kakkospainikkeella avattavaksi valikoksi* ja *tilannevalikoksi*.)

Tietyt tavallisimmat ja tärkeimmät sivulle tehtävät muutokset ovat käytettävissä suoraan pikavalikon vaihtoehtoina. Ruudukon sarakkeita voi esimerkiksi lisätä tai piilottaa kätevästi ympäristöpäivityksestä 17 alkaen napsauttamalla sarakeotsikkoa hiiren kakkospainikkeella ja valitsemalla sitten **Lisää sarakkeita** tai **Piilota tämä sarake**.

Lisäksi eksplisiittisen mukauttamisen yleisimmät tyypit saa käyttöön napsauttamalla elementtiä hiiren kakkospainikkeella ja valitsemalla **Mukauta**. (Huomaa, että kaikkia sivun elementtejä ei voida mukauttaa.). Kun valitset tämän mukauttamistavan, elementin ominaisuusikkuna tulee näkyviin.

[![Elementin ominaisuuksien mukauttaminen](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

Voit mukauttaa elementtiä ominaisuusikkunassa seuraavilla tavoilla:

- Elementin otsikon muuttaminen.
- Elementin piilottaminen niin, ettei se näy sivulla. Kentän tietoja ei poisteta eikä muokata. Tiedot eivät vain enää näy sivulla.
- Pikavälilehden yhteenveto-osan tietojen sisällyttäminen (jos elementti on pikavälilehdessä).
- Sivun kentissä liikkuminen ohittamalla kenttä sarkainpainetta painamalla.
- (Minkä tahansa) kentän tietojen muokkauksen estäminen.

Ominaisuusikkunassa voi olla elementin mukaan myös muita mukauttamisominaisuuksia. Ruudun ominaisuusikkunassa voi esimerkiksi olla mahdollista viedä kyseisen ruutu ylös koontinäyttöön, kun taas koontinäytön ominaisuusikkuna voi mahdollistaa uuden työtilan luonnin kyseissä koontinäytössä.

### <a name="the-personalization-toolbar"></a>Mukauttamisen työkalurivi

Jos haluat tehdä useita muutoksia sivulle tai tehdä muutoksia, jotka eivät ole käytettävissä muiden mekanismien kautta (kuten elementtien uudelleenjärjestely), voit käyttää **Mukauttaminen**-työkaluriviä. Avaa **mukauttamisen** työkalurivi valitsemalla **Mukauta tämä lomake** elementin ominaisuusikkunassa. Voit valita **Mukauta tämä lomake** -vaihtoehdon myös kunkin sivun **Asetukset**-välilehden **Mukauta**-ryhmässä.

[![Mukauttamisen työkalurivi](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

#### <a name="navigating-the-page"></a>Siirtyminen sivulla

Mahdollisuus siirtyä sivulla, kun **Mukauttaminen-työkalurivi** on avoinna, riippuu käyttämästäsi ympäristöversiosta.

- Ennen ympäristöpäivitystä 19, kun **Mukauttaminen**-työkalurivi oli auki, sivu oli Vain luku -tilassa (siihen ei voi syöttää mitään) eikä se ollut vuorovaikutteinen (muutoksia pystyi tekemään vain sivun näkyviin elementteihin). Jos halusit tehdä muutoksia tiivistetyn osion tai eri välilehden sisäisiin elementteihin, sinun oli suljettava **Mukauttaminen**-työkalurivi, laajennettava osiota tai vaihdettava haluttuun välilehteen ja sitten avattava **Mukauttaminen**-työkalurivi uudelleen.

- Ympäristöpäivityksestä 19 alkaen, jos **Mukauttaminen**-työkalurivi on avoinna, sivu on yhä Vain luku -tilassa, mutta paljon vuorovaikutteisempi. Voit etenkin laajentaa tai supistaa Tietoruutua, vaihtaa välilehtiä ja laajentaa tai tiivistää osioita, kun **Mukauttaminen**-työkalurivi avataan, samalla tavoin kuin yleensäkin tekisit sivulla. Voit soveltaa mukauttamisen muutosta tiivistettyyn osioon tai välilehteen (kuten piilottaa Tietoruudun) käyttämällä painiketta, joka ilmestyy tiivistetyn osion tai välilehden viereen, kun kohdistat siihen näppäimistöllä tai liikutat hiirtä sen yläpuolella.

#### <a name="personalization-tools"></a>Mukauttamisen työkalut

**Mukauttamisen** työkalurivillä on seuraavat työkalut:

- Valitse elementin ominaisuuksia ja muuta niitä **Valitse**-työkalulla. Valitse ensin **Valitse**-työkalu ja sitten elementti, jonka ominaisuuksia muokataan. Kun valitset elementin, sen ominaisuusikkuna avautuu ja voit muokata elementin kaikkia ominaisuuksia. Voit toistaa prosessin muille kyseisen sivun mukautettaville elementeille. Tiettyjen elementtien käyttötavan vuoksi Finance and Operations ei kuitenkaan salli niiden tiettyjen ominaisuuksien muuttamista. Näin ollen on mahdollista, että kaikkia valitun elementin ominaisuuksia ei voi muokata. Et voi esimerkiksi piilottaa pakollista kenttää.
- Voit siirtää elementin **Siirrä**-työkalulla toiseen sijaintiin nykyisen elementtiryhmän sisällä. (Et voi siirtää elementtiä sen pääryhmän ulkopuolelle.) Valitse ensin **Siirrä**-työkalua ja sitten siirrettävä elementti. Kun valitset elementin, Finance and Operations tarkistaa sivun ja määrittää, mihin elementti voidaan siirtää. Tämän jälkeen se luo pudotusalueita. Kun vedät elementtiä valitussa ryhmä, värillinen lihavoitu viiva osoittaa pudotusalueen, johon elementti voidaan pudottaa.
- Voit piilottaa elementin sivulla **Piilota**-työkalulla. Valitse ensin **Piilota**-työkalua ja sitten piilotettava elementti. Kun valitset **Piilota**-työkalun, kaikki tällä hetkellä piilotettuna olevat elementit tulevat näkyviin varjostetussa säilössä. Voit sitten tuoda ne esiin. Valitsemalla **Valitse**-työkalun näet, miltä sivu näyttää, kun valitut elementit piilotetaan.

    - Ympäristöpäivityksestä 18 alkaen voit piilottaa vaaditut kentät ja osiot, jotka sisältävät vaaditut kentät. Voit näin luoda yksinkertaistetun kokemuksen, jossa liiketoimintalogiikan oletusarvojen mukaan määritettyjä vaadittuja kenttiä ei näytetä. Vaaditut piilotetut kentät näkyvät myös tilapäisesti, jos ne ovat tyhjiä, kun yritetään tallennusta.

- Jos haluat elementit näkyvän pikavälilehden yhteenveto-osassa, käytä **Yhteenveto**-työkalua. Yhteenvetotyökalu koskee vain pikavälilehtiosiossa olevia kenttiä. Kun valitset **Yhteenveto**-työkalun, kaikki yhteenvetokentiksi valitut kentät näkyvät varjostetussa säilössä. Voit lisätä kenttiä vuorovaikutteisesti pikavälilehden yhteenvetoon ja poistaa kenttiä niistä valitsemalla kenttiä.
- Voit poistaa elementin nykyisen sivun näppäimistön sarkaimella tehtävistä valinnoista **Ohita**-työkalulla. Kun valitset **Ohita**-työkalun, kaikki tällä hetkellä ohitettavat elementit näkyvät varjostetussa säilössä. Voit sitten lisätä ne takaisin sarkaimella tehtäviin valintoihin.
- Voit merkitä **Muokkaa**-työkalulla. onko elementti muokattavissa vai ei. Kun valitset **Muokkaa**-työkalun, kaikki tällä hetkellä ei-muokattavat elementit näkyvät varjostetussa säilössä. Voit sitten määrittää ne takaisin muokattaviksi. Huomaa, että osa kentistä on pakollisia, jolloin niiden muokkaamista ei voi estää. Näiden kenttien vieressä on lukkokuvake.
- Saat **Lisää**-painikkeella näkyviin luettelon sivulle lisättävistä elementeistä.

    - Lisää kenttä sivulle valitsemalla **Kenttä**-työkalu **Lisää**-kohdassa. Voit lisätä **Kenttä**-työkalulla vain kenttiä, jotka sisältyvät sivumääritykseen mutta joita ei tällä hetkellä näytetä sivulla. Lisätietoja nykyisen sivumääritelmän ulkopuolisten uusien kenttien luomisesta on kohdassa [Mukautetut kentät](user-defined-fields.md). Sinun on valittava **Kenttä**-työkalun valinnan jälkeen ensin ryhmä tai alue, johon haluat lisätä kentän. Valintaikkunassa on luettelo valittuun ryhmään tai alueeseen liittyvistä kentistä. Valitse valintaluettelossa ensin vähintään yksi lisättävä kenttä ja sitten **Lisää**. Voit poistaa aiemmin lisätyn kentän toistamalla edellä mainitut vaiheet mutta poistamalla valintaikkunassa kentän valinnan.
    - Valitse **PowerApp**-työkalu **Lisää**-kohdassa, jos haluat upottaa sivulla Microsoft PowerAppsilla luodun sovelluksen. Lisätietoja PowerApps-sovelluksen upottamisesta sivulle on kohdassa [PowerApps-sovellusten upottaminen](embed-power-apps.md).

- Valitsemalla **Hallinta**-painikkeen näet luettelon hallintavaihtoehdoista, jotka liittyvät kaikkiin nykyisen sivun mukautuksiin.

    - Palauta sivu oletusasennustilaan valitsemalla **Tyhjennä**. Kaikki nykyisen sivun mukautukset tyhjennetään. Tätä toimintoa ei voi kumota. Käytä tätä vaihtoehtoa tämän vuoksi vain silloin, kun olet varma, että haluat palauttaa sivun alkuperäiset asetukset.
    - Voit ladata mukautuksen sivulle aiemmin luodusta tiedostosta valitsemalla **Tuo**. Kaikki sivulla olevat mukautukset korvataan valitun tiedoston mukautuksilla.
    - Voit tallentaa sivun mukautukset tiedostoon valitsemalla **Vie**. Voit jakaa mukautuksesi muiden käyttäjien kanssa. Kyseisten käyttäjien tarvitsee vain tuoda sivun mukautukset sisältävä tiedosto.

- Sulje **mukauttamisen** työkalurivi valitsemalla **Sulje**-painike. Sivu palautuu nyt alkuperäiseen vuorovaikutteiseen tilaan.

**Mukauttamisen** työkaluriviä käytettäessä tallennustoiminnot ovat implisiittisiä. Mukautukset otetaan käyttöön heti, kun ne on tehty, eikä sinun tarvitse valita **Tallenna**-painiketta. Joissain tapauksissa työkalua valittaessa elementin vieressä näkyy lukkokuvake. Tämä kuvake ilmaisee, että valittuun työkaluun liittyviä elementin ominaisuuksia ei voi muokata, koska kyseisten ominaisuuksien muutokset estävät sivun odotetun toiminnan.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Ruudun, luettelon tai linkin lisääminen työtilaan

Joillakin luetteloja sisältävillä sivuilla on käytössä lisämukautusominaisuus. Toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmän **Lisää työtilaan** -painikkeella voi näyttää nykyisen luettelon tiedot tietyssä työtilassa. Voit näyttää tietojen suodatetun tai lajitellun näkymän työtilassa. Vaihtoehtoisesti voit näyttää oletusnäkymän. Voit myös määrittää, näkyvätkö tiedot työtilassa luettelona, luettelon nimikkeiden määrän näyttävänä yhteenvetoruutuna vai linkkinä.

[![Lisää työtilaan](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Voit lisätä luettelon työtilaan lajittelemalla tai suodattamalla luettelon ensin sivulla niin, että tiedot näkyvät siinä muodossa kuin haluat niiden näkyvän työtilassa. Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Luettelo**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit valita työtilan luettelossa näytettävät sarakkeet. Voit myös määrittää työtilan luettelossa käytettävän otsikon.
- Voit lisätä ruudun työtilaan suodattamalla ensin sivun luettelon niin, että se näyttää vain tiedot, joista haluat yhteenvedon tai joita haluat käyttää nopeasti. Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Ruutu**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit määrittää ruudun työtilassa käytettävän otsikon. Voit myös määrittää, näytetäänkö määrä ruudussa. Kun ruutu on lisätty työtilaan, voit ruudun valitsemalla avata nykyisen sivun työtilasta ja näyttää ruutuun liitetyn suodatetun luettelon.
- Voit lisätä linkin työtilaan suodattamalla ensin sivun luettelon näyttämään vain ne tiedot, joista olet kiinnostunut. Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Linkki**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit määrittää linkin otsikon. Voit myös määrittää otsikon uudelle, tämän linkin sisältävälle osalle otsikon (valinnainen).

Kun luettelo, ruutu tai linkki on lisätty työtilaan, voit avata kyseisen työtilan ja muuttaa sen elementtien järjestystä tarpeen mukaan.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Yhteenvedon lisääminen työtilasta koontinäyttöön

Joissakin työtiloissa on lukumääräruutuja (ruutuja, joissa on numeroita). On mahdollista, että haluat nähdä kyseiset ruudut myös koontinäytössä. Napsauta työtilassa lukumääräruutua hiiren kakkospainikkeella ja valitse sitten **Mukauta**. Valitse sitten ruudun ominaisuusikkunassa **Kiinnitä koontinäyttöön**. Kun seuraavan kerran avaat (ja päivität) valitun koontinäytön, lukumäärä näkyy kyseisen työtilan siirtymisruudun alapuolella. Voit valita, että tämä lukumäärä, siirtyy suoraan tietoihin, joihin se viittaa.

### <a name="personalizing-your-dashboard"></a>Koontinäytön mukauttaminen

Koontinäyttö on usein ensimmäinen sivu, jonka näet, kun avaat Finance and Operationsin. Voit mukauttaa koontinäytön näyttämään vain ne työtilaruudut, jotka haluat nähdä. Voit myös järjestää ruudut itsellesi sopivaan järjestykseen, nimetä työtilan siirtymisruudut uudelleen tai lisätä täysin uuden työtilan ruudun.

Voit mukauttaa koontinäyttöä napsauttamalla jotakin ruutua hiiren kakkospainikkeella ja avata sitten ruudun ominaisuusikkunan valitsemalla **Mukauta**-vaihtoehdon.

- Jos haluat piilottaa valitun ruudun tai nimetä sen uudelleen, muutos on tehtävä suoraan ominaisuusikkunassa.
- Voit muuttaa työtilan ruutujen järjestystä valitsemalla ominaisuusikkunassa **Mukauta tämä lomake**, jolloin **mukauttamisen** työkalurivi avautuu. Voit sitten järjestää ruudut haluallasi tavalla **Siirrä**-työkalulla.
- Voit luoda uuden työtilan ruudun valitsemalla ominaisuusikkunassa **Lisää työtilaan**. Uusi työtilan ruutu luodaan koontinäytön alareunaan. Voit nimetä tämän uuden työtilan ruudun haluamallasi tavalla. Voit myös lisätä luetteloita, ruutuja ja linkkejä työtilaa aiemmin tämän ohjeaiheen kohdassa [Luetteloiden, ruutujen tai linkkien lisääminen työtilaan](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace) kuvatulla tavalla.

## <a name="administration-of-personalization"></a>Mukauttamisen hallinta

Kun olet mukauttanut sivun, voit jakaa mukautukset muiden käyttäjien kanssa viemällä mukautetun sivun. Voit sitten pyytää käyttäjiä avaamaan mukautetun sivun ja tuomaan luodun mukautustiedoston. Vaihtoehtoisesti voit antaa mukautuksen käyttäjälle, jolla on järjestelmänvalvojan oikeudet. Tämä käyttäjä voi sitten ottaa mukautustiedoston käyttöön useille käyttäjille samanaikaisesti.

Jos käyttäjällä on järjestelmänvalvojan oikeudet, hän voi myös hallita muiden käyttäjien mukautuksia **Mukautukset**-sivulla. Sivulla on neljä välilehteä:

- **Käytä** – Voit tuoda tai valita yhden tai usean käyttäjän mukautuksen. Jos mukautus otetaan käyttöön yhdelle tai usealle käyttäjälle, ensiksi valitaan rooli ja käyttäjät, joilla tämä rooli on. Valitse sitten joko aiemmin luotu mukautus, jota haluat käyttää valituille käyttäjille, tai tuo mukautustiedosto. Mukautuksen oikeellisuus tarkistetaan ja sitä käytetään kaikille käyttäjille, kun he seuraavan kerran avaavat valitun sivun.
- **Tyhjennä** – Voit tyhjentää yhden tai usean käyttäjän sivun tai työtilan kaikki mukautukset. Valitse ensin sivu tai työtila. Näet nyt luettelon käyttäjistä, jotka ovat mukauttaneet sitä. Valitse sitten käyttäjät, joiden sivun tai mukautukset on tyhjennettävä. Valitse lopuksi **Tyhjennä**. Kaikki mukautukset, joita valitut käyttäjät ovat käyttäneet valitulla sivulla tai valitussa työtilassa, poistetaan. Tätä toimintoa ei voi kumota. Jos sivulla tai työtilassa on kuitenkin tallennettuja mukautuksia, nämä mukautukset voidaan tuoda uudelleen.
- **Käyttäjäkohtainen esimies** – Valitse käyttäjä, kun haluat tarkastella käyttäjän mukauttamien sivujen luetteloa. Voit sitten antaa käyttäjälle tietyn sivun tai koko järjestelmän mukautusten käyttöoikeuden tai poistaa mukautusten käyttöoikeuden käytöstä. Voit myös tuoda, viedä tai tyhjentää valitun käyttäjän mukautuksen.
- **Järjestelmä** – Voit poistaa tässä välilehdessä kaikkien järjestelmän käyttäjien mukautukset tilapäisesti. Siinä tapauksessa mukautuksia ei kuitenkaan poisteta. Kaikkien käyttäjien kaikki sivut vain palautetaan alkuperäisiin asetuksiin. Jos otat mukautukset myöhemmin uudelleen käyttöön, kaikkia mukautuksia käytetään uudelleen. Voit poistaa tässä välilehdessä kaikkien järjestelmän käyttäjien mukautukset myös pysyvästi. Poistettuja mukautuksia ei voida palauttaa. Varmista tämän vuoksi ennen tämän tehtävän suorittamista, että olet vienyt kaikki ne mukautukset, jotka ehkä tarvitset myöhemmin.

## <a name="personalization-of-inventory-dimensions"></a>Varastodimensioiden mukauttaminen

Kun mukautat varastodimension asetuksia sivulla, pidä mielessä **Näytä dimensio** -asetuksen avulla luodut asetukset. Voit esimerkiksi piilottaa eränumeron varastodimension sarakkeen mukautuksen avulla. Sarake kuitenkin näkyy, kun sivu avataan seuraavan kerran. Tämä on mahdollista, koska **dimension näyttöasetukset** määrittävät varastodimension näytettävät sarakkeet.

**Dimension näyttöasetuksia**käytetään kaikilla sivulla, ja ne korvaavat kaikki yksittäisten sivujen mukautetut varastodimension kenttien asetukset.

Jos et siis halua edellisessä esimerkissä, että varastodimension eränumero näkyy, kyseisen dimension valinta on poistettava taulukon **Näytä dimensiot** -vaihtoehdon osana. Tämän jälkeen tätä muutosta käytetään tietyn sivun lisäksi kaikilla sivuilla.

