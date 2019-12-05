---
title: Käyttäjäkokemuksen mukauttaminen
description: Tässä ohjeaiheessa kerrotaan, miten voit mukauttaa sovellusta.
author: jasongre
manager: AnnBe
ms.date: 10/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3cf2b82470887ee617704b72e47a53d299911e3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811528"
---
# <a name="personalize-the-user-experience"></a>Käyttäjäkokemuksen mukauttaminen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit mukauttaa sovellusta.

Räätälöintien perusluokkia on kolme.

- Asetussivulla tehtävät mukautukset. Väriteema ja aikavyöhyke ovat niistä esimerkkejä.
- Sivun käyttöön liittyvät mukautukset. Näitä mukautuksia kutsutaan *implisiittisiksi* mukautuksiksi. Järjestelmä esimerkiksi seuraa ruudukoiden sarakeleveyksiä, jos muutat niitä, sekä pikavälilehtien laajennus- tai tiivistystiloja.
- Kun käyttäjä mukauttaa sivun ulkoasua muuttamalla tapaa, jolla elementti näkyy tai toimii kyseisellä sivulla, käytössä on usein ollut vuorovaikutteinen mukautustila. Näitä mukautuksia kutsutaan *eksplisiittisiksi* mukautuksiksi. Käyttäjä voi esimerkiksi lisätä sivulle elementtejä, piilottaa niitä tai muuttaa niiden järjestystä.

Kaikki käyttäjän tekemät mukautukset koskevat vain kyseistä käyttäjää riippumatta mukautuksen tyypistä tai yrityksestä, jonka kanssa käyttäjä on vuorovaikutuksessa. Yhden käyttäjän sivulle tekemät muutokset eivät vaikuta järjestelmän muihin käyttäjiin.

## <a name="system-wide-options-for-the-current-user"></a>Nykyisen käyttäjän järjestelmänlaajuiset vaihtoehdot

**Käyttäjän asetukset** -sivulla on useita nykyisen käyttäjän koko järjestelmää koskevia asetuksia. Avaa **Käyttäjän asetukset** -sivu valitsemalla **Asetukset**-painike (rataskuvake) siirtymispalkissa. Valitse sitten **Käyttäjän asetukset**. **Käyttäjän asetukset** -sivulla on neljä välilehteä, joissa erilaisia käyttäjäasetuksia:

- **Visuaalinen** – valitse sivun elementtien väriteema ja oletuskoko.
- **Asetukset** – Valitse oletusarvot, joita käytetään aina, kun avaat järjestelmän. Näitä arvoja ovat esimerkiksi yritys, ensimmäinen sivu sekä näkymän tai muokkauksen oletustila. (Näkymä- tai muokkaustila määrittää, lukitaanko sivu näyttämistä varten vai avataanko se muokattavaksi aina, kun avaat sen.) Tässä välilehdessä on kieli- ja aikavyöhykeasetukset sekä päivämäärä-, kellonaika- ja numeromuotoilun asetukset. Tässä välilehdessä on lisäksi sekalaisia asetuksia,, jotka vaihtelevat julkaisuversiosta toiseen.
- **Tili** – käyttäjänimen ja muiden tiliin liittyvien asetusten säätäminen.
- **Työnkulku** – työnkulkuun liittyvien asetusten valitseminen.

Asetuksien muuttamisen lisäksi voit myös tarkastella ja poistaa käyttötiedot ja mukautukset käyttämällä **Käyttötiedot**-sivua. Valitse vain **Käyttötiedot** toimintoruudusta.

Kun käytät sovellusta, monet tehdyistä valinnoista tallennetaan helppokäyttöisyyden lisäämiseksi tulevaisuudessa. **Mukauttaminen**-välilehdessä voit tarkastella ja hallita henkilökohtaisia muutoksia, jotka olet tehnyt sivuihin järjestelmässä. Tässä välilehdessä voit myös nollata kuvatekstitoiminnot (eli ponnahdusikkunat, joissa esitellään järjestelmän uudet ominaisuudet). Tämän jälkeen sinulle ilmoitetaan jälleen aiemmin käytetyistä ominaisuuksista.

> [!NOTE]
> Jos [Tallennetut näkymät](saved-views.md) -toiminto on käytössä, voit tarkastella ja hallita omia mukautuksiasi valitsemalla **Mukauttaminen** toimintoruudun **Käyttäjän asetukset** -sivulla.

## <a name="implicit-personalizations"></a>Implisiittiset mukautukset

Implisiittiset mukautukset ovat mukautuksia, joita tehdään olemalla vuorovaikutuksessa ohjausobjektien kanssa, jotka tallentavat nykyisen näkyvän tilan.

- **Ruudukon sarakkeet** – Ruudukon sarakkeen leveyttä voidaan säätää valitsemalla koon muuttamiseen tarkoitettu palkki sarakkeen otsikon vasemmalla tai oikealla puolella ja vetämällä sitä vasemmalle tai oikealle, kunnes sarake on halutun levyinen. Sovellus tallentaa sarakkeelle määritetyn leveyden. Kun sitten seuraavan kerran avaat ruudukon sisältävän sivulla, sarakkeen koko muutetaan vastaamaan kyseistä leveyttä.
- **Pikavälilehdet** – Joillain sivuilla on laajennettavia *pikavälilehtinä* tunnettuja osia. Sovellus tallentaa tietoja laajennetuista ja tiivistetyistä pikavälilehdistä. Kun tämän jälkeen avaat sivut, pikavälilehdet näkyvät joko laajennettuina tai tiivistettyinä sen mukaan, mitä olet valinnut sivulla edellisellä kerralla. Joissain tapauksissa voit parantaa järjestelmän suorituskykyä tiivistämällä pikavälilehden, koska sovellus ei tarvitse noutaa tietoja pikavälilehtiä varten, ennen kuin ne laajennetaan. Jäljempänä tässä aiheessa selitetään, miten voit myös muuttaa sivulla olevien pikavälilehtien järjestystä.
- **Tietoruudut** – Osalla sivuista on **Aiheeseen liittyviä tietoja** -ruutu, jossa näkyy vain luku -tietoja, jotka liittyvät sivun kulloiseenkin aiheeseen. Kukin **Aiheeseen liittyviä tietoja** -ruudun osio on nimeltään *Tietoruutu*. Voit laajentaa tai kutistaa **Aiheeseen liittyviä tietoja**-ruudun. Voit myös laajentaa tai kutistaa yksittäisiä tietoruutuja. Sovellus tallentaa nämä asetukset. Kun seuraavan kerran avaat sivun **Aiheeseen liittyviä tietoja** -ruutu ja yksittäiset tietoruudut ovat joko laajennettuna tai kutistettuna sen mukaan, mitä olet valinnut edellisellä kerralla. Joissain tapauksissa voit parantaa järjestelmän suorituskykyä kutistamalla tietoruudun, koska sovelluksen ei tarvitse noutaa tietoja tietoruutuja varten, ennen kuin ne laajennetaan.
- **Toimintoruudut** – *Toimintoruutu* näkyy useimmilla sivuilla yläreunan lähellä. Toimintoruudussa on painikkeita, joilla voi tehdä monia valitulla sivulla tehtäviä toimintoja. Nämä painikkeet on usein järjestetty välilehtiin. Voit "kiinnittää" koko toimintoruudun avoimeksi. Vaihtoehtoisesti se voi olla oletusarvoisesti kutistettuna. Kun tämän jälkeen avaat sivun, toimintoruutu on joko auki tai kutistettuna sen mukaan, mitä olet valinnut edellisellä kerralla. Jos olet kiinnittänyt toimintoruudun avoimeksi, näkyvissä on viimeisin käyttämäsi välilehti.
- **Pikasuodattimet** – *Pikasuodatin* näkyy monien ruudukoiden yläpuolella. Pikasuodattimia voi käyttää ruudukon suodattamiseen valitun sarakkeen perusteella. Sovellus tallentaa sarakkeen, johon suodatus perustuu. Kun avaat seuraavan kerran sivun, jolla kyseinen ruudukko on, ruudukko suodatetaan saman sarakkeen perusteella. Voit kuitenkin suodattaa ruudukon tämän jälkeen toisen sarakkeen perusteella.
- **Sarakeotsikon suodattimet** – Kun ruudukkoa suodatetaan *sarakeotsikon suodattimilla*, suodatinoperaattori voidaan tarvittaessa vaihtaa etsittävien tietojen mukaan. Voit esimerkiksi vaihtaa operaattorin **alkaa** operaattoriksi **on täsmälleen**. Aina kun käytät sarakeotsikon suodatinta ja muutat suodatinoperaattoria, sovellus tallentaa muutoksen. Kun sitten seuraavan kerran suodatat kyseistä saraketta, suodatinoperaattori palautetaan.
- **Siirtymisruutu** – Voit avata *navigointiruudun* valitsemalla **Laajenna siirtymisruutu**-painikkeen minkä tahansa sivun vasemmassa yläkulmassa. (Tätä painiketta kutsutaan myös _**Valikko**-painikkeeksi_, *hampurilaiseksi*, *hampurilaismenuksi* tai *hampurilaispainikkeeksi*.) Voit kiinnittää siirtymisruudun avoimeksi tai pitää sen oletusarvoisesti kutistettuna. Kun olet kiinnittänyt siirtymisruudun avoimeksi, sovellus pitää sen avoimena siihen asti, että kutistat sen.

## <a name="explicit-personalizations"></a>Eksplisiittiset mukautukset

Tietojen tärkeys vaihtelee käyttäjä- ja yrityskohtaisesti. Toisin sanoen tiedot, jotka ovat välttämättömiä jollekin, ovat liiketoiminnan kannalta merkityksettömiä jollekin toiselle. On mahdollista muokata tapaa, jolla tiedostot järjestetään ja miten niitä käytetään. Voit myös määrittää tietyt tiedot piilotettaviksi. Nämä ominaisuudet ovat esimerkkejä eksplisiittisistä mukautuksista ja ovat ratkaisevan tärkeitä henkilökohtaisen ja tuottavan kokemuksen kannalta. Eksplisiittinen mukauttaminen on mukauttamista, jonka nimenomaisena tarkoituksena on muuttaa elementin tai sivun ulkoasua tai toimintaa.

### <a name="shortcut-menu-options"></a>Pikavalikkovaihtoehdot

Pikavalikkojen avulla sivua voi eksplisiittisesti muuttaa muutamalla tavalla siten, että se vastaa paremmin omia tai yrityksen vaatimuksia. (Pikavalikkoa kutsutaan myös *hiiren kakkospainikkeella avattavaksi valikoksi* ja *tilannevalikoksi*.)

Tietyt tavallisimmat ja tärkeimmät sivulle tehtävät muutokset ovat käytettävissä suoraan pikavalikon vaihtoehtoina. Ruudukon sarakkeita voi esimerkiksi lisätä tai piilottaa kätevästi ympäristöpäivityksestä 17 alkaen napsauttamalla sarakeotsikkoa hiiren kakkospainikkeella ja valitsemalla sitten **Lisää sarakkeita** tai **Piilota tämä sarake**.

Lisäksi eksplisiittisen mukauttamisen yleisimmät tyypit saa käyttöön napsauttamalla elementtiä hiiren kakkospainikkeella ja valitsemalla **Mukauta**. (Huomaa, että kaikkia sivun elementtejä ei voida mukauttaa.). Kun valitset tämän mukauttamistavan, elementin ominaisuusikkuna tulee näkyviin.

![Elementin ominaisuuksien mukauttaminen](./media/personalization-element-properties.png)

Voit mukauttaa elementtiä ominaisuusikkunassa seuraavilla tavoilla:

- Elementin otsikon muuttaminen.
- Elementin piilottaminen niin, ettei se näy sivulla. Kentän tietoja ei poisteta eikä muokata. Tiedot eivät vain enää näy sivulla.
- Pikavälilehden yhteenveto-osan tietojen sisällyttäminen (jos elementti on pikavälilehdessä).
- Ohita kenttä, jotta siihen ei koskaan kohdisteta, kun siirryt sivun läpi sarkaimella.
- Estä kentän tietojen muokkaaminen (mikä tahansa tietue).

Ominaisuusikkunassa voi olla elementin mukaan myös muita mukauttamisominaisuuksia. Ruudun ominaisuusikkunassa voi esimerkiksi olla mahdollista viedä kyseisen ruutu ylös koontinäyttöön, kun taas koontinäytön ominaisuusikkuna voi mahdollistaa uuden työtilan luonnin kyseissä koontinäytössä.

### <a name="the-personalization-toolbar"></a>Mukauttamisen työkalurivi

Jos haluat tehdä useita muutoksia sivulle tai muutoksia, jotka eivät ole käytettävissä muiden mekanismien kautta (jos esimerkiksi haluat muuttaa elementtien järjestystä), voit käyttää **Mukauttaminen**-työkaluriviä. Voit avata **Mukauttaminen**-työkalurivin seuraavilla tavoilla:

- Valitse **Mukauta tämä lomake** elementin ominaisuusikkunassa.
- Valitse **Mukauta tätä sivua** minkä tahansa sivun toimintoikkunan **Asetukset**-välilehden **Mukauttaminen**-ryhmässä.
- Valitse **Asetukset**-painike siirtymispalkissa ja valitse sitten **Mukauta**.

[![Mukauttamisen työkalurivi](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Siirtyminen sivulla

Kun **Mukautus**-työkalurivi on auki, taustalla oleva sivu on vain luku -muodossa (tietoja ei siis voi muuttaa) mutta on edelleen vuorovaikutteinen. Voit laajentaa tai kutistaa **Aiheeseen liittyviä tietoja** -ruudun, vaihtaa välilehtiä ja laajentaa tai kutistaa osia tavanomaiseen tapaan. Voit ottaa kutistettavaan osaan tai välilehteen kohdistuvan mukautuksen (esimerkiksi pikavälilehden piilottamisen) käyttöön valitsemalla painikkeen, joka tulee näkyviin kyseisen osan tai välilehden viereen, kun kohdistat siihen näppäimistöllä tai liikutat hiirtä sen yläpuolella.

#### <a name="personalization-tools"></a>Mukauttamisen työkalut

**Mukauttamisen** työkalurivillä on seuraavat työkalut:

- Valitse elementin ominaisuuksia ja muuta niitä **Valitse**-työkalulla. Voit käyttää tätä työkalua valitsemalla työkalurivin **Valitse**-painikkeen ja valitsemalla sitten haluamasi elementin. Elementin ominaisuusikkuna avautuu, ja voit muuttaa elementin kaikkia ominaisuuksia. Voit toistaa prosessin muille kyseisen sivun mukautettaville elementeille. Ota huomioon, että kaikki mukautusominaisuudet eivät välttämättä ole käytettävissä kaikissa tilanteissa. Et esimerkiksi voi lukita pakollista kenttää.
- Voit piilottaa elementin sivulla **Piilota**-työkalulla. Voit käyttää tätä työkalua valitsemalla työkalurivin **Piilota**-painikkeen ja valitsemalla piilotettavan elementin. Kun käytät **Piilota**-työkalua, kaikki tällä hetkellä piilotettuna olevat elementit tulevat näkyviin varjostetussa säilössä. Voit tehdä elementistä näkyvän valitsemalla sen. Valitsemalla toisen mukautustyökalun näet, miltä sivu näyttää, kun elementit piilotetaan.
- Voit lisätä sivullesi kentän **Lisää**-työkalun avulla. Tällä työkalulla voidaan lisätä vain kenttiä, jotka sisältyvät sivumääritykseen. Lisätietoja nykyisen sivumääritelmän ulkopuolisten uusien kenttien luomisesta on kohdassa [Mukautettujen kenttien luominen ja käyttäminen](user-defined-fields.md). Sinun on valittava työkalurivin **Lisää kenttä**-painikkeen valitsemisen jälkeen ensin ryhmä tai alue, johon haluat lisätä kentän. Valintaikkunassa näkyy luettelo valittuun ryhmään tai alueeseen liittyvistä kentistä. Valitse valintaluettelossa ensin vähintään yksi lisättävä kenttä ja sitten **Lisää**. Voit poistaa aiemmin lisätyn kentän toistamalla edellä mainitut vaiheet mutta poistamalla valintaikkunassa kentän valinnan.
- Voit siirtää elementin **Siirrä**-työkalulla toiseen sijaintiin nykyisen elementtiryhmän sisällä. Ota huomioon, ettet voi siirtää elementtiä sen pääryhmän ulkopuolelle. Voit käyttää tätä työkalua valitsemalla työkalurivin **Siirrä**-painikkeen ja valitsemalla siirrettävän elementin. Kun valitset elementin, sovellus määrittää sijainnit, joihin elementti voidaan siirtää. Näitä sijainteja kutsutaan *pudotusalueiksi*. Kun vedät elementtiä valitussa ryhmässa, värillinen lihavoitu viiva osoittaa pudotusalueen, johon elementti voidaan pudottaa.
- Voit poistaa elementin nykyisen sivun näppäimistön sarkaimella tehtävistä valinnoista **Ohita**-työkalulla. Kun valitset työkalurivin **Ohita**-painikkeen, kaikki tällä hetkellä ohitettavat elementit näkyvät varjostetussa säilössä. Voit lisätä kenttiä sarkainjärjestykseen ja poistaa niitä vuorovaikutteisesti.
- Voit lisätä kentän pikavälilehtien yhteenveto-osaan käyttämällä **Näytä otsikossa**-työkalua. Kun valitset työkalurivin **Näytä otsikossa**-painikkeen, kaikki yhteenvetokentiksi valitut kentät näkyvät varjostetussa säilössä. Voit lisätä kenttiä vuorovaikutteisesti pikavälilehden yhteenvetoon ja poistaa niitä siitä valitsemalla kenttiä.
- **Lukitse**-työkalulla voit merkitä, onko elementti muokattavaissa vai ei. Kun valitset työkalurivin **Lukitse**-painikkeen, kaikki elementit, jotka eivät tällä hetkellä ole muokattavissa, näkyvät varjostetussa säilössä. Voit sitten määrittää ne takaisin muokattaviksi. Huomaa, että jotkut kentät ovat pakollisia, eikä niiden muokkausta voi estää. Näiden kenttien vieressä on lukkokuvake.
- **Lisää PowerApp** -painikkeella voit upottaa sivulle sovelluksen, joka on luotu Microsoft PowerAppsilla. Lisätietoja PowerApps-sovelluksen upottamisesta sivulle on kohdassa [PowerApps-sovellusten upottaminen](embed-power-apps.md).
- Voit palauttaa sivun oletusasennustilaan **Tyhjennä**-työkalulla. Kaikki senhetkisen sivun mukautukset tyhjennetään. Tätä toimintoa ei voi kumota. Käytä tätä työkalua tämän vuoksi vain silloin, kun olet varma, että haluat palauttaa sivun alkuperäiset asetukset.
- Voit ladata mukautuksen aiemmin luodusta tiedostosta käyttämällä **Tuo**-työkalua. Kun tuot sivulle mukautuksia, voit valita, lisätäänkö ne sivun mukautuksiin vai korvataanko mukautukset niillä. Tätä toimintoa ei voi kumota. Siksi sinun on manuaalisesti tyhjennettävä tai kumottava ei-toivotut muutokset, kun olet tuonut mukautuksia.
- Voit tallentaa sivun mukautukset tiedostoon käyttämällä **Vie**-työkalua. Sitten voit jakaa mukautuksesi muiden käyttäjien kanssa. Kyseisten käyttäjien tarvitsee vain tuoda sivun mukautukset sisältävä tiedosto.
- Sulje **mukauttamisen** työkalurivi valitsemalla **Sulje**-painike. Sivu palautuu nyt alkuperäiseen vuorovaikutteiseen tilaan.

Yleensä **Mukautus**-työkaluriviä käytettäessä mukautukset tulevat voimaan heti, kun ne on tehty. Jos [Tallennetut näkymät](saved-views.md) -ominaisuus kuitenkin on käytössä, sinun on erikseen tallennettava mukautukset valitsemaasi näkymään.

Joissain tapauksissa työkalua valittaessa elementin vieressä näkyy lukkokuvake. Tämä kuvake ilmaisee, että valittuun työkaluun liittyviä elementin ominaisuuksia ei voi muokata, koska kyseisten ominaisuuksien muutokset estävät sivun odotetun toiminnan.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Ruudun, luettelon tai linkin lisääminen työtilaan

Joillakin luetteloja sisältävillä sivuilla on käytettävissä **Lisää työtilaan** -mukautusominaisuus toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä. Tällä ominaisuudella voit siirtää tarvittavia tietoja kulloisestakin luettelosta tiettyyn työtilaan. Työtilassa näkyviin tulevat tiedot voivat perustua joko koko luetteloon tai suodatettuun ja lajiteltuun luettelon versioon. Voit myös määrittää, näkyvätkö tiedot työtilassa luettelona, luettelon nimikkeiden määrän näyttävänä yhteenvetoruutuna vai linkkinä.

> [!NOTE]
> Jos [Tallennetut näkymät](saved-views.md) -toiminto on käytössä, työtilaan siirrettävä sisältö on linkitetty suoraan näkymään. Näkymän kyselyä käytetään tietojen hakemiseen työtilassa ja vastaavaa työtilan ruutu tai linkki avaa kyseisen näkymän sivun, jolloin näkymän kyselyä ja mukautuksia sovelletaan siihen.

[![Lisää työtilaan](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Voit lisätä luettelon työtilaan lajittelemalla tai suodattamalla luettelon ensin sivulla niin, että tiedot näkyvät siinä muodossa kuin haluat niiden näkyvän työtilassa. (Jos Tallennetut näkymät -toiminto on käytössä, et voi jatkaa, ennen kuin olet tallentanut näkymän näillä ehdoilla.) Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Luettelo**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit valita työtilan luettelossa näytettävät sarakkeet. Voit myös määrittää työtilan luettelossa käytettävän otsikon.
- Voit lisätä ruudun työtilaan suodattamalla ensin sivun luettelon niin, että se näyttää vain tiedot, joista tehdään yhteenveto tai joita haluat käyttää nopeasti. (Jos Tallennetut näkymät -toiminto on käytössä, et voi jatkaa, ennen kuin olet tallentanut näkymän näillä ehdoilla.) Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Ruutu**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit määrittää työtilan ruudussa käytettävän otsikon. Voit myös määrittää, näytetäänkö määrä ruudussa. Kun ruutu on lisätty työtilaan voit valita, että se avaa kulloisenkin sivun työtilasta. Sen jälkeen voit tarkastella ruutuun liittyvää suodatettua luetteloa.
- Voit lisätä linkin työtilaan suodattamalla ensin sivun luettelon näyttämään vain ne tiedot, joista olet kiinnostunut. (Jos Tallennetut näkymät -toiminto on käytössä, et voi jatkaa, ennen kuin olet tallentanut näkymän näillä ehdoilla.) Valitse sitten **Lisää työtilaan**. Valitse ensin työtila ja sitten **Esittely**-kentässä **Linkki**. **Konfiguroi**-asetuksen valinnan jälkeen avautuu valintaikkuna, jossa voit määrittää linkin yhteydessä käytettävän otsikon. Voit myös määrittää otsikon uudelle, tämän linkin sisältävälle osalle otsikon (valinnainen).

Kun olet lisännyt luettelon, ruudun tai linkin työtilaan, voit avata kyseisen työtilan ja muuttaa sen elementtien järjestystä tarpeen mukaan.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Yhteenvedon lisääminen työtilasta koontinäyttöön

Joissakin työtiloissa on lukumääräruutuja (ruutuja, joissa on numeroita). On mahdollista, että haluat nähdä kyseiset ruudut myös koontinäytössä. Napsauta työtilassa hiiren kakkospainikkeella **Mukauta** ja valitse ruudun ominaisuusikkunassa **Kiinnitä koontinäyttöön**. Kun sitten seuraavan kerran avaat (ja päivität) valitun koontinäytön, lukumäärä näkyy kyseisen työtilan siirtymisruudun alapuolella. Voit valita, että tämä lukumäärä, siirtyy suoraan tietoihin, joihin se viittaa.

### <a name="personalizing-your-dashboard"></a>Koontinäytön mukauttaminen

Koontinäyttö on usein ensimmäinen sivu, jonka näet, kun avaat sovelluksen. Voit mukauttaa koontinäytön näyttämään vain ne työtilaruudut, jotka haluat nähdä. Voit myös järjestää ruudut itsellesi sopivaan järjestykseen, nimetä työtilan siirtymisruudut uudelleen tai lisätä uuden työtilaruudun.

Voit mukauttaa koontinäyttöä napsauttamalla jotakin ruutua hiiren kakkospainikkeella ja avata sitten ruudun ominaisuusikkunan valitsemalla **Mukauta**-vaihtoehdon.

- Jos haluat piilottaa valitun ruudun tai nimetä sen uudelleen, muutos on tehtävä suoraan ominaisuusikkunassa.
- Voit muuttaa työtilan ruutujen järjestystä valitsemalla ominaisuusikkunassa **Mukauta tämä lomake**, jolloin **mukauttamisen** työkalurivi avautuu. Voit sitten järjestää ruudut uudelleen haluamallasi tavalla **Siirrä**-työkalun avulla.
- Voit llisätä uuden työtilaruudun valitsemalla ominaisuusikkunassa **Lisää työtilaan**. Uusi työtilan ruutu luodaan koontinäytön alareunaan. Voit nimetä tämän uuden työtilan ruudun haluamallasi tavalla. Voit myös lisätä luetteloita, ruutuja ja linkkejä työtilaa aiemmin tämän ohjeaiheen kohdassa [Luetteloiden, ruutujen tai linkkien lisääminen työtilaan](#adding-a-tile-list-or-link-to-a-workspace) kuvatulla tavalla.

## <a name="administration-of-personalizations"></a>Mukautusten hallinta

Kun olet mukauttanut sivun, voit jakaa mukautukset muiden käyttäjien kanssa viemällä mukautetun sivun. Voit sitten pyytää käyttäjiä avaamaan mukautetun sivun ja tuomaan luodun mukautustiedoston. Vaihtoehtoisesti voit antaa mukautuksesi käyttäjälle, jolla on järjestelmänvalvojan oikeudet. Tämä käyttäjä voi sitten ottaa mukautustiedoston käyttöön useille käyttäjille samanaikaisesti.

Jos käyttäjällä on järjestelmänvalvojan oikeudet, hän voi myös hallita muiden käyttäjien mukautuksia **Mukautukset**-sivulla.

Niillä asiakkaila, jotka eivät ole ottaneet käyttöön [Tallennetut näkymät](saved-views.md) -ominaisuutta, tällä sivulla on neljä välilehteä:

- **Käytä** – Voit tuoda tai valita yhden tai usean käyttäjän mukautuksen. Jos mukautus otetaan käyttöön yhdelle tai usealle käyttäjälle, ensiksi valitaan rooli ja käyttäjät, joilla tämä rooli on. Valitse sitten joko aiemmin luotu mukautus, jota haluat käyttää valituille käyttäjille, tai tuo mukautustiedosto. Mukautuksen oikeellisuus tarkistetaan ja sitä käytetään kaikille käyttäjille, kun he seuraavan kerran avaavat valitun sivun.
- **Tyhjennä** – Voit tyhjentää yhden tai usean käyttäjän sivun tai työtilan kaikki mukautukset. Valitse ensin sivu tai työtila. Näet nyt luettelon käyttäjistä, jotka ovat mukauttaneet sitä. Valitse sitten käyttäjät, joiden sivun tai mukautukset on tyhjennettävä. Valitse lopuksi **Tyhjennä**. Kaikki mukautukset, joita valitut käyttäjät ovat käyttäneet valitulla sivulla tai valitussa työtilassa, poistetaan. Tätä toimintoa ei voi kumota. Jos sivulla tai työtilassa on kuitenkin tallennettuja mukautuksia, nämä mukautukset voidaan tuoda uudelleen.
- **Käyttäjät** – Valitse käyttäjä, kun haluat tarkastella käyttäjän mukauttamien sivujen luetteloa. Voit sitten sallia käyttäjän käyttävän mukautuksia tietyillä sivuilla tai koko järjestelmässä tai estää sen. Voit myös tuoda, viedä tai tyhjentää käyttäjän mukautuksen. Lisäksi voit palauttaa käyttäjän kuvatekstitoiminnot. Jos käyttäjä tällöin on aiemmin hylännyt uusia ominaisuuksia esitteleviä ponnahdusikkunoita, ne tulevat näkyviin uudelleen, kun kyseinen käyttäjä kohtaa kyseiset ominaisuudet.
- **Järjestelmä** – Voit poistaa kaikkien järjestelmän käyttäjien mukautukset käytöstä väliaikaisesti. Tällöin kaikkien käyttäjien mukautukset poistetaan ja kaikki sivut palautetaan oletustiloihinsa. Jos otat mukautukset myöhemmin jälleen käyttöön, kaikkia mukautuksia sovelletaan uudelleen. Voit poistaa tässä välilehdessä kaikkien järjestelmän käyttäjien mukautukset myös pysyvästi. Poistettuja mukautuksia ei voi palauttaa. Varmista tämän vuoksi ennen tämän tehtävän suorittamista, että olet vienyt kaikki ne mukautukset, jotka ehkä tarvitset myöhemmin.

Niillä asiakkailla, jotka ovat ottaneet [Tallennetut näkymät](saved-views.md) -ominaisuuden käyttöön, **Mukauttaminen**-sivulla on viisi välilehteä:

- **Julkaistut näkymät** – Nämä näkymät on julkaistu organisaatiollesi. Voit muuttaa käyttäjiä, jotka ovat näiden näkymien kohteena, muuttamalla kuhunkin näkymään liittyviä käyttöoikeusrooleja tai yrityksiä. Voit myös viedä tai poistaa yhden tai useita julkaistuja näkymiä.
- **Julkaisemattomat näkymät** – Nämä näkymät ovat mallinäkymiä, jotka on tuotu järjestelmääsi muttei vieelä julkaistu. Voit julkaista, viedä ja poistaa näitä näkymiä.
- **Henkilökohtaiset näkymät** – Nämä näkymät ovat järjestelmän käyttäjien luomia. Voit julkaista henkilökohtaisen näkymän organisaatiolle tai kopioida yhden tai useamman näistä näkymistä muille käyttäjille. Voit myös viedä ja poistaa näitä näkymiä tarpeen mukaan.
- **Käyttäjät** – Valitse käyttäjä, kun haluat tarkastella käyttäjän mukauttamien sivujen luetteloa. Voit sitten sallia käyttäjän käyttävän mukautuksia tietyillä sivuilla tai koko järjestelmässä tai estää sen. Voit myös tuoda, viedä tai tyhjentää käyttäjän mukautuksen. Lisäksi voit palauttaa käyttäjän kuvatekstitoiminnot. Jos käyttäjä tällöin on aiemmin hylännyt uusia ominaisuuksia esitteleviä ponnahdusikkunoita, ne tulevat näkyviin uudelleen, kun kyseinen käyttäjä kohtaa kyseiset ominaisuudet.
- **Järjestelmä** – Voit poistaa kaikkien järjestelmän käyttäjien mukautukset käytöstä väliaikaisesti. Tällöin kaikkien käyttäjien mukautukset poistetaan ja kaikki sivut palautetaan oletustiloihinsa. Jos otat mukautukset myöhemmin jälleen käyttöön, kaikkia mukautuksia sovelletaan uudelleen. Voit poistaa tässä välilehdessä kaikkien järjestelmän käyttäjien mukautukset myös pysyvästi. Poistettuja mukautuksia ei voi palauttaa. Varmista tämän vuoksi ennen tämän tehtävän suorittamista, että olet vienyt kaikki ne mukautukset, jotka ehkä tarvitset myöhemmin.

Käyttäjät, joilla on käytössään **Mukauttaminen**-sivu, voivat myös tuoda henkilökohtaisia tai mallinäkymiä toimintoruudun **Tuo näkymiä** -painikkeen avulla.

## <a name="personalizing-inventory-dimensions"></a>Varastodimensioiden mukauttaminen

Kun mukautat varastodimension asetuksia sivulla, pidä mielessä **Näytä dimensio** -asetuksen avulla luodut asetukset. Voit esimerkiksi piilottaa eränumeron varastodimension sarakkeen mukautuksen avulla. Sarake kuitenkin näkyy, kun sivu avataan seuraavan kerran. Tämä on mahdollista, koska **dimension näyttöasetukset** määrittävät varastodimension näytettävät sarakkeet. **Dimension näyttöasetuksia**käytetään kaikilla sivulla, ja ne korvaavat kaikki yksittäisten sivujen mukautetut varastodimension kenttien asetukset.

Jos et siis halua edellisessä esimerkissä, että varastodimension eränumero näkyy sivulla, kyseisen dimension valinta on poistettava kyseisen sivun taulukon **Näytä dimensiot** -vaihtoehdon osana.
