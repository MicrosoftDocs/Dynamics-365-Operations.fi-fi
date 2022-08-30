---
title: Materiaalin käsittelylaitteiden rajapinta (MHAX)
description: Tässä artikkelissa kuvataan, miten materiaalin käsittelylaitteiden rajapinta (MHAX) määritetään siten, että voit muodostaa yhteyden fyysisiin ulkoisiin materiaalinkäsittelyjärjestelmiin (MH).
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1056c7aee3ea96ddcb012704be40bef6c363f323
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334352"
---
# <a name="material-handling-equipment-interface-mhax"></a>Materiaalin käsittelylaitteiden rajapinta (MHAX)

[!include [banner](../../includes/banner.md)]

*Materiaalin käsittelylaitteiden liittymää* (MHAX) voi käyttää yhteyden muodostamiseen varastonhallintaprosesseja (WMS) Microsoft Dynamics 365 Supply Chain Managementissa käyttävän varaston ja ulkoisten fyysisten materiaalinkäsittelyjärjestelmien (MH) välille. WMS- ja MH-järjestelmien välinen rajapinta koostuu kahdesta jonosta: yksi lähteville tapahtumille (WMS -> MH) ja toinen saapuville tapahtumille (MH -> WMS). WMS-järjestelmä luo lähteviä tapahtumia niiden työrivien perusteella, jotka luodaan työn luomisen ja suorittamisen eri prosessien aikana. Tämän jälkeen MH-järjestelmä kyselee WMS-järjestelmältä säännöllisesti uusia tapahtumia ja käsittelee vastaukset. Kun MH-järjestelmä on lopettanut tapahtumien käsittelyn työohjeiden mukaisesti, se lähettää saapuvia tapahtumia, kuten työrivien valmistumisia ja lyhyitä keräilyjä.

Seuraavassa kuvassa esitetään eri elementit sekä järjestys, jossa prosessit tapahtuvat, kun käytetään MHAX-integrointia.

![MHAXin komponentit ja vuorovaikutukset.](media/mhax-components.png "MHAXin komponentit ja vuorovaikutukset")

Seuraavassa on selitys edellisessä kuvassa näkyvistä vuorovaikutuksista:

1. Työn luomisen tai työn suorittamisen aikana lähtevät tapahtumat luodaan lähtevien jonoon.
2. MH-laitteisto muodostaa yhteyden MH-laitteistopalveluun, kyselee sen kannalta merkittäviä uusia tapahtumia ja käsittelee nämä tapahtumat.
3. Kun MH-laitteisto on valmis vastaamaan, se muodostaa yhteyden palveluun uudelleen ja lähettää saapuvia tapahtumia. Jonon käsittelyprosessi käsittelee nämä tapahtumat heti.
4. Riippuen saapuvien tapahtumien tiedoista, jonon käsittelyprosessi saattaa suorittaa olemassa olevia töitä, muokata niitä tai luoda uusia töitä.

## <a name="turn-on-the-mhax-feature"></a>MHAX-toiminnon käyttöönotto

Ennen kuin voit käyttää MHAX-toimintoa, sekä sen toiminto että sen määritysavain on otettava käyttöön.

1. Jos käytössä on Supply Chain Managementin versio 10.0.28 tai aiempi versio, tee seuraavat toiminnot:
    1. Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.
    1. Ota **[Toiminnonhallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**-työtilassa käyttöön *Materiaalin käsittelylaitteiden rajapinta* -toiminto. (Supply Chain Managementin versiosta 10.0.29 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä.)
1. Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
1. Laajenna **Kauppa \> Varaston- ja kuljetuksenhallinta** ja valitse sitten **Materiaalin käsittelylaitteiden rajapinta** -valintaruutu.
1. Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.

## <a name="set-mhax-parameters"></a>MHAX-parametrien määritys

Toiminnon määrittäminen edellyttää joidenkin yleisten parametrien määrittämistä **Materiaalin käsittelylaitteiden rajapinnan parametrit** -sivulla.

1. Siirry kohtaan **Materiaalin käsittelylaitteiden rajapinta \> Määritys \> Materiaalin käsittelylaitteiden rajapinnan parametrit**.
2. Määritä **Yleiset**-välilehdessä seuraavat kentät:

    - **Käyttäjätunnus** – Valitse työntekijä. Tätä työntekijää käytetään kaikkien saapuvien jonon käsittelemien työvaiheiden (poiminnat ja asetukset) suorittamiseen.
    - **Ota saapuvien sanomien tunnus käyttöön** – Kun tämän asetuksen arvona on *Kyllä* ja vastaanotetaan saapuvan sanoman tunnuksen kaksoiskappale, sanoma hylätään ja virheilmoituksessa ilmoitetaan, että sanoma on jo olemassa. Kun tämän asetuksen arvona on *Ei*, saapuvien sanomien tunnusten kaksoiskappaleet ovat sallittuja.

3. Valitse **Numerosarjat**-välilehdessä järjestelmän laajuiset numerosarjat, joita pitäisi käyttää yksilöllisten tunnusten luomiseen saapuvien jonon kohteille, lähtevien jonon kohteille ja työrivipareille.

## <a name="outbound-events"></a>Lähtevät tapahtumat

Järjestelmä määrittää tietyissä työn luomisen tai työn suorittamisen kohdissa, pitääkö sen luoda lähteviä tapahtumia MH-järjestelmään lähetettäväksi. Jos tilaus on määritetty tiettyyn kohtaan varastossa käsittelyä, järjestelmä luo tapahtuman tilauksen määrityksen mukaisesti.

### <a name="structure-of-outbound-events"></a>Lähtevien tapahtumien rakenne

Kullakin lähtevällä tapahtumalla on yksilöllinen lähtevän jonon tunnus. Lähtevän transaktion tyyppi määrittää tapahtuman tyypin. Tapahtumalle kirjataan myös varasto ja tapahtuman luoneen tilauksen tunnus.

Tietojen viemiseksi MH-järjestelmään lähtevä tapahtuma sisältää 10 tietokenttää (**tieto01**–**tieto10**). Nämä tietokentät vastaavat suoraan (1:1) olemassa olevia tietokantakenttiä. Tarkemmin sanoen ne haetaan työrivin ja työotsikkotaulukkojen kentistä. Kentät voidaan valita vapaasti. Ne määritetään tilausta luotaessa.

Tapahtuma voi olemassa olevia tietokantakenttiä suoraan vastaavien 10 tietokentän lisäksi sisältää ylimääräisen tietokentän, josta käytetään nimitystä *lisätiedot*. Tämän kentän sisältö luodaan mukautetulla X++-koodilla, jota kutsutaan *lisätietogeneraattoriksi*. Tilauksessa on määritetty mahdollisesti käytettävät lisätietogeneraattorit.

Sen varmistamiseksi, että MH-järjestelmä vastaanottaa jokaisen lähtevän jonon tunnuksen vain kerran, käytetään tilakenttää sen määrittämiseen, onko tapahtuma valmis lähetettäväksi ulkoiseen järjestelmään vai onko se jo lähetetty.

### <a name="outbound-queue-subscriptions"></a>Lähtevien jonon tilaukset

Ennen tapahtumien luomista on määritettävä tilaus, jolla MHAX-toiminnolle ilmoitetaan, luodaanko tapahtumia ja miten niitä mahdollisesti luodaan. Luoduille tapahtumille määritetään tilaustunniste. Siten useat MH-järjestelmät voivat muodostaa yhteyden samaan WMS-järjestelmään, mutta pitää tapahtumansa erillään. Kun MHAX-palvelulta kysellään uusia tapahtumia, tilaus on yksi vaihtoehdoista tapahtumien hakemiseksi.

Voit luoda tilauksen valitsemalla **Materiaalin käsittelylaitteiden rajapinta \> Määritys \> Tilaukset**. Seuraavat parametrit ovat käytettävissä kunkin tilauksen osalta:

- **Tilaustunnus** – Yksilöllinen nimi, jonka perusteella tilaus voidaan tunnistaa.
- **Kuvaus** – Vapaamuotoinen tilauksen kuvaus.
- **Varasto** – Ne varastot, joiden perusteella tapahtumat suodatetaan.
- **Lähtevän tapahtuman tyyppi** – Niiden tapahtumien tyyppi, joita tilauksen on sisällettävä.
- **Lisätietogeneraattori** – Valinnainen koodilaajennus, jolla voidaan lisätä tietoja lähtevän tapahtuman **Lisätiedot**-kenttään.

Kuhunkin tilaukseen voidaan liittää kysely. Tämä kysely suodattaa työrivejä ja otsikkoja, jotta rajoitettaisiin entisestään töitä, jotka käyttävät tilausta tapahtumien luomiseen. Voit lisätä kyselyn tilaukseen valitsemalla kulloisenkin tilauksen **Suorita kysely** -valintaruudun **Tilaukset**-sivulla ja valitsemalla sitten toimintoruudusta **Muokkaa kyselyä**. Näkyviin tulee vakiomuotoinen Supply Chain Managementin kyselyeditori.

Lisäksi tilauksella on *tilauskartta*, joka yhdistää kenttiä joko työn otsikosta tai työriviltä kaikkiin tai joihinkin lähtevän tapahtuman 10 vapaasta tietokentästä tarpeen mukaan. Tietojen palauttamiseksi MHAX-palveluun sisällytetään yleensä työrivitietueen tunnus tai *työriviparin tunnus*. (Työriviparin tunnus on uusi ominaisuus, jonka avulla järjestelmä voi käyttää yksittäistä palautuskomentoa poiminta- ja asetusrivien käsittelemiseen.) Muut kentät määräytyvät käyttötapauksen mukaan. Esimerkkejä esitetään myöhemmin tässä artikkelissa.

Voit luoda tilauskartan valitsemalla kulloisenkin tilauksen **Tilaukset**-sivulta ja valitsemalla sitten toimintoruudusta **Tilauskartta**. Näkyviin tulevassa **Tilauskartta**-valintaikkunassa voit määrittää taulukon ja kentän kullekin käytettävissä olevalle tietokentälle tarpeen mukaan.

### <a name="outbound-event-types"></a>Lähtevien tapahtumien tyypit

Tässä osassa kuvataan erilaiset käytettävissä olevat tapahtumatyypit. (Tapahtumatyypeistä käytetään myös nimitystä *transaktiotyypit*.) Lisäksi kuvataan, milloin kukin tapahtumatyyppi luodaan WMS-järjestelmässä.

#### <a name="work-creation-events"></a>Työnluontitapahtumat

Työnluontitapahtumat luodaan, kun sovellus on luonut työn. Tämä toiminta pätee useimpiin työnluontiprosessien tyyppeihin ja erityisesti poiminta- ja täydennystöiden luomiseen. Yleensä, kun työ luodaan tilassa *Avoin*, mikä tarkoittaa, että työ on valmiina työntekijän suoritettavaksi, luodaan työnluontitapahtuma. Lisäksi työnluontitapahtumia luodaan perustason siirtotöille (ei mallityöhön perustuville siirroille), vaikka kyseisiä töitä ei luotaisi avoimena työnä.

Merkittävä poikkeus tähän toimintaan on inventointityö, jota ei tällä hetkellä tueta. MH-järjestelmän varastomäärät ovat MHAX-järjestelmän sovellusalan ulkopuolella, ja laskentojen tulokset on tuotavat inventaarionlaskennan kirjauskansioon.

Kun työ on luotu, MHAX-palvelu käsittelee luodut työrivit ja märittää työriviparin tunnuksen kaikkien työotsikkojen kaikille luoduille työriveille. Tarkoituksena on ryhmittää kaikki poimintatyörivit niiden jälkeen tulevien asetusten jälkeen yhteisen työriviparin tunnuksen alle. (Ryhmät vastaavat työmallien poiminta-asetuspareja.) Tällä tavoin yksittäistä tunnusta voidaan käyttää ilmoittamaan kaikkien toisiinsa liittyvien poiminta- ja asetusrivien töiden valmistumisesta. Ryhmittelyprosessi alkaa ensimmäisestä rivistä ja jatkuu samalla tunnuksella, kunnes tavataan peräkkäinen pari asetus- ja poimintatyörivejä. Juokseva tunnus määritetään parin asetusriville. Tämän jälkeen seuraavan parin poimintariville määritetään uusi tunnus. Tämä prosessi jatkuu, kunnes kaikki työotsikkoon kuuluvat rivit on käsitelty.

Työnluontitapahtumien erikoisominaisuutena luoduilla tapahtumilla on tila *Estetty* tavanomaisen niiden MH-järjestelmään lähettämiseen käytettävän *Valmis*-tilan sijaan, jos työotsikon **Estetty aalto** -asetuksen arvona on *Kyllä*. Työotsikon **Estetty aalto** -merkintä ilmaisee, että työotsikko ei vielä ole valmis työntekijöiden suoritettavaksi. Syynä voi olla esimerkiksi valmistumaton täydennystyö. Kun **Estetty aalto** -merkintä poistetaan, jo luotujen tapahtumien esto poistetaan. Tällöin ne ovat valmiina MH-järjestelmän noudettavaksi jonosta.

#### <a name="work-initiation-events"></a>Työnalustustapahtumat

Työnalustustapahtumia luodaan, kun työn tila muuttuu tilasta *Avoin* tilaan *Käynnissä* työnpäivityksen yhteydessä.

#### <a name="work-completion-events"></a>Työnvalmistumistapahtumat

Työnvalmistumistapahtumia luodaan, kun työn tila muuttuu tilasta *Käynnissä* tilaan *Suljettu* työnpäivityksen yhteydessä.

#### <a name="work-cancellation-events"></a>Työnperuutustapahtumat

Työnperuutustapahtumia luodaan, kun työn tila muuttuu mistä tahansa muusta tilasta kuin tilasta *Peruutettu* tilaan *Peruutettu* työnpäivityksen yhteydessä. Lisäksi kaikki muut työotsikkoon liittyvät tapahtumat poistetaan kaikkien tilausten jonosta. Näin ulkoisia järjestelmiä estetään käsittelemästä tarpeettomia tapahtumia.

#### <a name="pickput-completion-events"></a>Poiminnan/asetuksen valmistumistapahtumat

Poiminnan/asetuksen valmistumistapahtumia luodaan, kun poiminta-/asetusrivin tila muuttuu tilasta *Käynnissä* tilaan *Suljettu* työrivin päivityksen yhteydessä.

### <a name="monitor-the-outbound-queue"></a>Lähtevien jonon seuranta

Voit tarkistaa lähtevien jonon valitsemalla **Materiaalin käsittelylaitteiden rajapinta \> Yhteiset \> Lähtevien jono**. **Lähtevien jono** -sivulla on luettelo kaikista lähtevien jonon kohteista ja niiden tiloista. Voit tarkastella jonokohteen tietoja valitsemalla sen. Näitä tietoja ovat esimerkiksi kohteen tapahtumatyyppi, käytetty tilaus sekä kunkin tietokentän (**tieto01**–**tieto10**) arvo ja lisätiedot.

### <a name="clean-up-the-outbound-queue"></a>Lähtevien jonon tyhjentäminen

Ennen pitkää lähtevien jono täyttyy jonokohteista, jotka on jo lähetetty. Voit poistaa nämä kohteet valitsemalla **Materiaalin käsittelylaitteiden rajapinta \> Säännölliset tehtävät \> Tyhjennys \> Lähtevien jonon tyhjennys**.

## <a name="inbound-events"></a>Saapuvat tapahtumat

Tässä osassa kuvataan erilaiset saapuvat tapahtumat, joista MH-järjestelmä voi ilmoittaa takaisin WMS-järjestelmälle. Siinä selitetään myös, että MH-järjestelmän on toimitettava tiedot, ja se, mitä kukin saapuva tapahtuma saa aikaan WMS-järjestelmässä.

### <a name="structure-of-inbound-events"></a>Saapuvien tapahtumien rakenne

Kun saapuva tapahtuma lähetetään, ulkoisen järjestelmän on toimitettava saapuvan transaktion tyyppi sekä enintään 10 parametria (**tieto01**–**tieto10**). Valinnaisen vahvistuksen avulla voidaan varmistaa, että MHAX-palvelu ei ole vastaanottanut saapuvaa tapahtumaa kuin yhden kerran. Jotta tämä vahvistus olisi käytössä, kullakin saapuvalla tapahtumalla on oltava yksilöllinen sanomatunnus. Jos sanomatunnuksen kaksoiskappale vastaanotetaan ja **Käytä saapuvan sanoman tunnusta** -asetuksen arvona **Materiaalin käsittelylaitteiden rajapinnan parametrit** -sivulla on *Kyllä*, sanoma hylätään. Virhesanoma ilmaisee, että sanoma on jo olemassa.

Saapuvien tietokenttien lisäksi järjestelmä määrittää tapahtumalle yksilöllisen saapuvan jonon tunnuksen.

### <a name="inbound-event-types"></a>Saapuvien tapahtumien tyypit

Tässä osiossa kuvataan saapuvien tapahtumien tyypit (transaktiotyypit), joita tuetaan, sekä tiedot, jotka on annettava, jotta tapahtumat käsitellään.

#### <a name="work-confirm-events"></a>Työn vahvistustapahtumat

Työn vahvistustapahtumat edellyttävät, että saapuvat tietokentät sisältävät seuraavat tiedot:

- **tieto01** – Työriviparin tunnus.
- **tieto02** – Työrivitietueen tunnus (`RecId`-arvo).

    > [!NOTE]
    > *Joko* kentällä **tieto01** *tai* kentällä **tieto02** on oltava arvo.

- **tieto03** – Sen rekisterikilven tunnus, josta poiminta suoritetaan.
- **tieto04** – Työotsikon kohteen rekisterikilven tunnus.

Jos työriviparin tunnus annetaan, suoritetaan peräkkäin kaikki poiminta-, asetus- tai muokatut työrivit, jotka on merkitty työriviparin tunnuksilla ja joiden tila on *Avoin* tai *Käynnissä*. Jos työrivitietueen tunnus (`RecId`arvo) on annettu, työrivin on oltava poiminta-, asetus- tai muokattu työrivi, jonka tilana on *Avoin* tai *Käynnissä*.

Paikat, joita hallitaan poimimalla rivejä rekisterikilvestä, edellyttävät, että **tieto03** määrittää rekisterikilven, josta poimitaan, riippumatta siitä, onko rivit merkitty työrivitietueen tunnuksella vai työriviparin tunnuksella. **tieto04**-kentässä on määritettävä työotsikon poiminnan kohteena oleva rekisterikilpi.

Asetusriveillä ei voi olla muita tietoja. Ne suoritetaan vain nykyisen työrivin sijainnin sekä työn kohteena olevan rekisterikilven perusteella. Jos asetus on suoritettava eri sijainnissa, muuta työrivin sijaintia myöhemmin tässä artikkelissa olevassa [Ohitustapahtumat](#override-events)-osassa kuvatulla tavalla.

Mukautetut työrivit eivät edellytä eivätkä tue muita tietoja saapuvassa tapahtumassa.

#### <a name="short-pick-events"></a>Lyhyiden poimintojen tapahtumat

Lyhyiden poimintojen tapahtumat edellyttävät, että saapuvat tietokentät sisältävät seuraavat tiedot:

- **tieto02** – Työtietueen tunnus (`RecId`-arvo).
- **tieto03** – Sen rekisterikilven tunnus, josta poiminta suoritetaan.
- **tieto04** – Poimittava määrä.
- **tieto05** – Lyhyen poiminnan poikkeuskoodi.
- **tieto06** – Työotsikon kohteen rekisterikilven tunnus.

> [!NOTE]
> **tieto01**-kenttää ei käytetä lyhyiden poimintatapahtumien osalta.

Tämä tapahtuma muistuttaa työnvahvistustapahtumaa, mutta se koskee vain poimintarivejä.

#### <a name="override-events"></a><a id="override-events"></a>Ohitustapahtumat

Ohitustapahtumat edellyttävät, että saapuvat tietokentät sisältävät seuraavat tiedot:

- **tieto01** – Työtietueen tunnus (`RecId`-arvo).
- **tieto02** – Uusi sijaintitunnus.

Työrivin tilana on oltava joko *Avoin* tai *Käynnissä* ja uuden sijainnin on oltava olemassa.

#### <a name="license-plate-receipt-events"></a>Rekisterikilpien vastaanottotapahtumat

Rekisterikilpien vastaanottotapahtumat edellyttävät, että saapuvat tietokentät sisältävät seuraavat tiedot:

- **tieto01** – Vastaanottavan saapuvan rekisterikilven tunnus.

Järjestelmä suorittaa rekisterikilven noutotoiminnon sen rekiserikilven perusteella, jota käytetään **tieto01**-kentän arvona.

### <a name="monitor-the-inbound-queue"></a>Saapuvien jonon seuranta

Voit tarkistaa saapuvien jonon valitsemalla **Materiaalin käsittelylaitteiden rajapinta \> Yhteiset \> Saapuvien jono**. **Saapuvien jono** -sivulla on luettelo kaikista saapuvien jonon kohteista ja niiden tiloista. Voit tarkastella jonokohteen tietoja valitsemalla sen. Näitä tietoja ovat esimerkiksi kohteen tapahtumatyyppi, sanoman tunnus sekä kunkin tietokentän (**tieto01**–**tieto10**) arvo.

Jos saapuvien tapahtumien käsittelyssä ilmenee virhe tai esiintyy muunlainen lokikohde, voit tarkastaa lokin valitsemalla toimintoruudusta **Virheloki**.

### <a name="inbound-event-processing"></a>Saapuvien tapahtumien käsittely

Saapuvat tapahtumat kirjoitetaan ensin tietokantaan ja suoritetaan sitten välittömästi (synkronisesti). Jos käsittelyn aikana tapahtuu virhe, tapahtuma kirjoitetaan tästä huolimatta jonoon, mutta tilaksi määritetään *Aiheutti virheen*. MHAX-palvelu palauttaa virhesanoman MH-järjestelmään ja tallentaa virhelokin saapuvien tapahtumien tietueeseen myöhempää tutkimista varten.

Tapahtumat, joiden tila *Aiheutti virheen*, voidaan käsitellä myöhemmin uudelleen, jos virhe on korjattu. Ne käsitellään uudelleen seuraavasti:

- Valitse **Materiaalin käsittelylaitteiden rajapinta \> Yhteiset \> Saapuvien jono**. Valitse asianomainen saapuvien jono ja valitse sitten toimintoruudusta **Käsittele uudelleen**.
- Valitse **Materiaalin käsittelylaitteiden rajapinta \> Yhteiset \> Käsittele virheen aiheuttanut saapuvien jono uudelleen**. näyttöön tulee vakioerätyön valintaikkuna. Siinä voit määrittää tietuesuodattimen sekä ajoittaa tai suorittaa erätyön jonon uudelleenkäsittelyä varten.

Kaikki työvaiheet (poiminnat ja asetukset) suoritetaan käyttäen sitä työntekijää, joka on valittu **Materiaalin käsittelylaitteiden rajapinnan parametrit** -sivun **Käyttäjätunnus**-kentässä.

### <a name="clean-up-the-inbound-queue"></a>Saapuvien jonon tyhjentäminen

Ennen pitkää saapuvien jono täyttyy jonokohteista, jotka on jo käsitelty. Voit poistaa nämä kohteet valitsemalla **Materiaalin käsittelylaitteiden rajapinta \> Säännölliset tehtävät \> Tyhjennys \> Saapuvien jonon tyhjennys**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Nopean yleiskuvan saaminen jononhallinnan avulla

Kun haluat nopean yleiskuvan kaikista saapuviin ja lähtevien jonoihin liittyvistä toimista, valitse **Materiaalin käsittelylaitteiden rajapinta \> Työtilat \> Jononhallinta**. **Jononhallinta**-sivulla on joukon välilehtiä ja ruutuja, joita voit käyttää jonojen valvomiseen ja tutkimiseen. Se sisältää myös hyödyllisiä linkkejä useimmille muille tässä artikkelissa mainituille sivuille.

## <a name="connect-to-the-mhax-service"></a>Yhteyden muodostaminen MHAX-palveluun

MHAX toteutetaan mukautettuna palveluna. Siksi se on käytettävissä SOAP- ja REST-kutsujen avulla. SOAP- ja REST-päätepisteiden osoitteet:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Sanomien noutaminen lähtevien jonosta

Sanomia voi noutaa lähtevien jonosta seuraavilla tavoilla:

- Nouda tapahtumia tilauksen tunnuksen perusteella käyttämällä komentoa `readOutboundSubscriptionQueue`.
- Nouda tapahtumia tapahtumatyypin ja varastotunnuksen perusteella useista tilauksista käyttämällä komentoa `readOutboundWarehouseQueue`.
