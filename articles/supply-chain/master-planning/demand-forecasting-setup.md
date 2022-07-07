---
title: Kysynnän ennusteiden asetukset
description: Tässä artikkelissa kuvataan asetustehtävät, jotka sinun on suoritettava kysynnän ennusteita valmistellessasi.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fae2ac53dec8696075e7506d979c1cf9fb277af5
ms.sourcegitcommit: d98ecbd9457197ec8f8e281f9c2f24dcce7b8269
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960151"
---
# <a name="demand-forecasting-setup"></a>Kysynnän ennusteiden asetukset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään kysynnän ennusteen määrittämistä.  

## <a name="item-allocation-keys"></a>Nimikkeenkohdistustunnukset

Nimikkeiden kohdistustunnukset voivat luoda nimikeryhmiä. Kysynnän ennuste lasketaan nimikkeelle ja sen dimensioille vain, jos nimike on nimikkeen kohdistustunnuksen osa. Tätä sääntöä käytetään suurten nimikejoukkojen ryhmittämiseen niin, että kysynnän ennusteita voidaan luoda nopeammin. Ennusteet luodaan pelkästään historiallisten tietojen perusteella.

Nimikkeen ja sen dimensioiden on oltava osa vain yhtä nimikkeen kohdistustunnusta, jos tätä nimikkeen kohdistustunnusta käytetään ennusteen luonnin aikana.

Luo nimikkeiden kohdistustunnukset ja lisää niihin varastointiyksikkö (SKU), noudattamalla seuraavia ohjeita.

1. Avaa **Pääsuunnittelu \> Määritys \> Kysynnän ennuste \> Nimikkeen kohdistustunnukset**.
1. Valitse luetteloruudusta kohteen allokointiavain tai luo uusi valitsemalla toimintoruudusta **Uusi**. Määritä uutta tai valittua avaimen otsikkoa varten seuraavat kentät:

    - **Nimikkeenvarausavain** – Syötä avaimelle yksilöivä nimi.
    - **Nimi** – Anna avaimelle kuvaava nimi.

1. Lisää nimikkeitä valittuun nimikkeenvaraustunnukseen tai poista nimikkeitä noudattamalla seuraavia ohjeita:

    - Käytä **Kohteiden allokointi** -pikavälilehden työkalupalkin **Uusi**- ja **Poista**-painikkeita lisätäksesi tai poistaaksesi kohteita tarpeen mukaan. Valitse kullekin riville nimiketunnus ja määritä sitten dimensioarvot muihin sarakkeisiin tarpeen mukaan. Valitse työkalurivin **näyttödimensiot**, jos haluat muuttaa ruudukossa näkyvää dimensiosarakkeiden joukkoa. (**Prosentti**-sarakkeen arvo ohitetaan kysynnän ennusteita luotaessa.)
    - Jos haluat lisätä avaimeen useita nimikkeitä, avaa sivu, jossa voit etsiä ja liittää useita nimikkeitä valittuun avaimeen valitsemalla Toimintoruudusta **Liitä nimikkeitä**.

> [!IMPORTANT]
> Ole huolellinen ja sisällytä vain niihin nimikkeisiin, jotka sisältyvät kuhunkin nimikkeen kohdistustunnukseen. Tarpeettomat nimikkeet saattavat aiheuttaa lisäkustannuksia käyttäessäsi Microsoft Azuren koneoppimispalvelua.

## <a name="intercompany-planning-groups"></a>Konsernin sisäiset suunnitteluryhmät

Kysynnän ennusteet voivat luoda kaikki yritykset kattavia ennusteita. Dynamics 365 Supply Chain Managementissa yritykset, joiden suunnittelu suoritetaan yhdessä, ryhmitetään samaksi konsernin sisäiseksi suunnitteluryhmäksi. Voit määrittää yrityskohtaisesti, mitkä nimikkeiden allokointiavaimet tulee ottaa huomioon kysynnän ennustamisessa, yhdistämällä nimikkeiden allokointiavain yritysten väliseen suunnitteluryhmän jäseneen.

> [!IMPORTANT]
> Suunnittelun optimointi ei tällä hetkellä tue konsernin sisäisiä suunnitteluryhmiä. Jos haluat tehdä suunnittelua optimointia käyttävää konsernin sisäistä suunnittelua, määritä pääsuunnittelun erätyöt, jotka sisältävät kaikkien asiaankuuluvien yritysten pääsuunnitelmat.

Voit määrittää konsernin sisäiset suunnitteluryhmät seuraavasti.

1. Siirry kohtaan **Pääsuunnittelu \> Asetukset \> Konsernin sisäiset suunnitteluryhmät**.
1. Valitse luetteloruudussa joko suunnitteluryhmä tai luo uusi valitsemalla toimintoruudussa **Uusi**. Määritä uuden tai valitun ryhmän otsikossa seuraavat kentät:

    - **Nimi** – Anna suunnitteluryhmälle yksilöivä nimi.
    - **Kuvaus** – Anna suunnitteluryhmän lyhyt kuvaus.

1. **Konsernin sisäisen suunnitteluryhmän jäsenet** -pikavälilehdessä voit lisätä kullekin ryhmälle (yritykselle) rivin työkalurivin painikkeiden avulla. Määritä kullekin riville seuraavat kentät:

    - **Yritys** – Valitse sen yrityksen (oikeushenkilön) nimi, joka on valitun ryhmän jäsen.
    - **Ajoitusjärjestys** – Määritä järjestys, jossa yritys on käsiteltävä suhteessa muihin yrityksiin. Pienin arvo käsitellään ensimmäisenä. Tilaus voi olla tärkeä, kun yhden yrityksen kysyntä vaikuttaa muihin yrityksiin. Näissä tapauksissa vaatimusta tarjoava yritys on käsiteltävä viimeisenä.
    - **Pääsuunnitelma** – Valitse pääsuunnitelma, joka käynnistyy nykyiselle yritykselle.
    - **Automaattinen kopiointi staattista suunnitelmaa varten** – Valitsemalla tämän valintaruudun voit kopioida suunnitelman tuloksen staattista suunnitelmaa varten.
    - **Automaattinen kopiointi dynaamista suunnitelmaa varten** – Valitsemalla tämän valintaruudun voit kopioida suunnitelman tuloksen dynaamista suunnitelmaa varten.

1. Jos nimikkeen kohdistustunnuksia ei ole määritetty konsernin sisäisen suunnitteluryhmän jäsenille, kysynnän ennuste lasketaan oletusarvoisesti kaikille niille nimikkeille, jotka on määritetty kaikkiin nimikkeen kohdistustunnuksiin kaikista yrityksistä. Yritysten ja nimikkeiden kohdistustunnusten lisäsuodatusvaihtoehdot ovat käytettävissä **Luo tilastollinen perusennuste** -valintaikkunassa (**Pääsuunnittelu \> Ennuste \> Tarve-ennuste \> Muodosta tilastollinen perusennuste**). Voit määrittää nimikkeenvaraustunnukset yritykselle valitussa konsernin sisäisessä suunnitteluryhmässä valitsemalla yrityksen ja valitsemalla sitten **Konsernin sisäisen suunnitteluryhmän jäsenten** pikavälilehdellä työkalurivin **Nimikkeenvaraustunnukset**.

> [!IMPORTANT]
> Ole huolellinen ja sisällytä vain asiaankuuluvat nimikkeiden allokointiavaimet kuhunkin yritysten väliseen suunnitteluryhmään. Tarpeettomat nimikkeet saattavat aiheuttaa lisäkustannuksia käyttäessäsi Azuren koneoppimispalvelua.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Kysynnän ennusteen parametrien määrittäminen

**Tarve-ennusteen parametrit** -sivulla voit määrittää useita asetuksia, jotka ohjaavat tarve-ennusteiden toimimista järjestelmässä.

### <a name="open-the-demand-forecasting-parameters-page"></a>Avaa Kysynnän ennusteen parametrit -sivu

Määritä kysynnän ennusteen parametrit kohdassa **Pääsuunnittelu \> Asetukset \> Kysynnän ennuste \> Kysynnän ennusteen parametrit**. Koska kysynnän ennusteet suoritetaan kaikki yritykset kattavasti, asetukset yleiset. Toisin sanoen se koskee kaikkia oikeushenkilöitä (yrityksiä).

### <a name="general-settings"></a>Yleiset asetukset

**Tarve-ennusteen parametrit** -sivun **Yleiset**-välilehdessä voit määrittää kysynnän ennusteiden yleiset asetukset.

#### <a name="demand-forecast-unit"></a>Kysynnän ennusteen yksikkö

Kysynnän ennusteet luovat ennusteet lukumäärinä. Näin ollen mittayksikkö, jossa määrä ilmaistaan, on määritettävä **Kysynnän ennusteen yksikkö** -kentässä. Tässä kentässä määritetään yksikkö, jota käytetään kaikissa kysyntäennusteissa kunkin tuotteen tavallisista varastoyksiköistä riippumatta. Käyttämällä johdonmukaista ennusteyksikköä autat varmistamaan, että kooste- ja prosenttijakauma ovat järkeviä. Lisätietoja koosteesta ja prosenttijakaumasta on kohdassa [Manuaalisten muutosten tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md).

Varmista, että jokaiselle mittayksikölle, jota käytetään kysynnän ennusteeseen sisältyvälle varastointiyksikölle, on muuntosääntö kyseiselle mittayksikölle ja yleinen ennusteen mittayksikkö, jotka valitset. Kun luot ennusteen, luettelo kohteista, joilla ei ole mittayksikön muunnosta, kirjataan lokiin. Näin ollen voit helposti korjata asetukset. Mittayksikön luomista ja niiden välistä muuntamista koskevia lisätietoja on kohdassa [Mittayksiköiden hallinta](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Tapahtumatyypit

**Tapahtumatyypit**-pikavälilehden kenttien avulla voit valita tapahtumatyypit, joita käytetään tilastollisen perusennusteen luodessaan.

Kysynnän ennusteita voidaan käyttää ennustamaan sekä riippuvaista että riippumatonta kysyntää. Jos esimerkiksi vain **Myyntitilaus**-vaihtoehdon asetuksena on *Kyllä* ja jos kaikki kysynnän ennusteessa huomioitavat nimikkeet ovat myytäviä nimikkeitä, järjestelmä laskee riippumattoman kysynnän. Tärkeitä alikomponentteja voidaan kuitenkin lisätä nimikkeen kohdistustunnuksille ja sisällyttää kysynnän ennusteisiin. Tässä tapauksessa, jos **Tuotantolinja**-vaihtoehdon asetuksena on *Kyllä*, lasketaan riippuvainen ennuste.

Voit ohittaa yhden tai useamman tietyn nimikkeen kohdistustunnuksen tapahtumatyypit käyttämällä **Nimikkeen kohdistustunnukset** -välilehteä. Välilehdessä on samanlaisia kenttiä.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Perusennusteen luominen

**Ennusteen luonnin strategia** -kentässä voit valita menetelmän, jota käytetään perusennusteen luonnissa. Käytössä on kolme tapaa:

- *Kopioi historiallisen kysynnän yli* – Voit luoda ennusteita kopioimalla vain historiatiedot.
- *Azuren koneoppimispalvelu* – Käytä ennustemallia, joka käyttää Azuren koneoppimispalvelua. Azuren koneoppimispalvelu on koneen oppimisratkaisu, joka on Azuren tämän hetkinen koneoppimispalvelu. Siksi on suositeltavaa käyttää sitä, jos haluat käyttää ennustemallia.
- *Azuren koneoppiminen* – Käytä ennustemallia, joka käyttää Azuren koneoppimisstudioa (klassikko). Azuren koneoppimisstudio (klassinen) on vanhentunut, ja se poistetaan pian Azuresta. Siksi suosittelemme, että valitset *Azuren koneoppimispalvelun*, jos määrität ensimmäistä kertaa kysynnän ennusteita. Jos käytät tällä hetkellä Azuren koneoppimisstudiota (klassinen), sinun on suunniteltava vaihtaa Azuren koneoppimispalveluun mahdollisimman pian.

Voit ohittaa ennusteen luontitavan tietyn nimikkeen kohdistustunnuksen tapahtumatyypille käyttämällä **Nimikkeen kohdistustunnukset** -välilehteä. Välilehdessä on samanlaisia kenttiä.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Ennustealgoritmin oletusparametrien ohittaminen yleisessä käytössä

Ennustealgoritmien oletusparametrit ja -arvot määritetään **Tarve-ennusteen parametrit** -sivulla (**Pääsuunnittelu \> Asetukset \> Kysynnän ennusteet \> Tarve-ennusteen parametrit**). Voit kuitenkin ohittaa ne yleisesti käyttämällä **Tarve-ennuste-parametrit** -sivun **Yleiset**-välilehden **Ennustealgoritmien parametrit** -pikavälilehtiä. (Voit myös ohittaa ne tietyissä kohdistustunnuksissa käyttämällä **Tuotekohdistusavaimet**-välilehteä **Kysyntäennusteparametrit**-sivulla.)

Työkalupalkin **Lisää**- ja **Poista**-painikkeilla voit luoda tarvittavan parametrin ohitusjoukon. Valitse jokaiselle luettelon parametrille arvo **Nimi**-kentän arvoista ja anna sitten sopiva arvo **Arvo**-kentässä. Kaikki muut kuin tässä luettelossa mainitut parametrit tulevat **Tarve-ennusteparametrit** -sivun asetuksista. Lisätietoja vakioparametrijoukon käytöstä ja niiden arvojen valitsemista on [tarve-ennustemallien oletusparametreissa ja -arvoissa](#model-parameters).

### <a name="set-forecast-dimensions"></a>Määritä ennustedimensiot

Ennustedimensio osoittaa ennusteelle määritetyn erittelytason. Yritys, toimipaikka ja nimikkeenkohdistustunnus ovat pakollisia ennustedimensioita. Voit myös luoda ennusteita varaston, varaston tilan, asiakasryhmän, asiakastilin, maan/alueen, osavaltion ja/tai nimiketasolla ja kaikilla tuotedimensiotasoilla. Käytä **Ennusteen dimensiot** -välilehteä **Kysyntäennusteen parametrit** -sivulla valitaksesi ennusteulottuvuuksien joukko, jota käytetään kysynnän ennustetta luotaessa.

Voit missä tahansa vaiheessa lisätä ennustedimensioita kysynnän ennusteissa käytettävien dimensioiden luetteloon. Voit myös poistaa ennustedimensioita luettelosta. Manuaaliset muutokset kuitenkin menetetään, jos lisäät tai poistat ennustedimension.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Tiettyjen nimikkeenvaraustunnusten ohitusten asetukset

Kaikki nimikkeet eivät toimi samalla tavalla kysynnän ennusteiden näkökulmasta. Voit näin ollen määrittää kohdistustunnuksen – tietyt ohitukset useimmille **Yleiset**-välilehdessä määritetyille asetuksille. Poikkeuksena on tarve-ennusteyksikkö. Voit määrittää tietylle nimikkeenkohdistustunnukselle ohitukset noudattamalla seuraavia ohjeita.

1. **Tarve-ennusteen parametrit** -sivun **Nimikkeen kohdistustunnukset** -välilehdessä voit lisätä nimikkeenvaraustunnuksia vasemmalla ruudukkoon tai poistaa niitä tarpeen mukaan työkalurivin painikkeiden avulla. Valitse sitten kohdistustunnus, jota varten haluat määrittää ohitukset.
1. Ota **Tapahtumatyypit**-pikavälilehdessä käyttöön tapahtumatyypit, joita haluat käyttää valittuun kohdistustunnukseen kuuluville tuotteiden tilastollisen perusennusteen luonnille. Asetukset toimivat samoin kuin **Yleiset**-välilehdessä, mutta ne koskevat vain valittua nimikkeenvaraustunnusta. Kaikki tämän kohdan asetukset (sekä *Kyllä*-arvot että *Ei*-arvot) ohittavat **Yleiset**-välilehden kaikki **tapahtumatyyppien** asetukset.
1. Valitse **Ennustealgoritmin parametrit** -pikavälilehdessä ennusteen luonnin strategia ja ennustealgoritmin parametri ohittaa valittuun kohdistustunnukseen kuuluvat tuotteet. Nämä asetukset toimivat samoin kuin **Yleiset**-välilehdessä, mutta ne koskevat vain valittua nimikkeenvaraustunnusta. Työkalupalkin **Lisää**- ja **Poista**-painikkeilla voit määrittää tarvittavan parametrin ohitusjoukon. Valitse jokaiselle luettelon parametrille arvo **Nimi**-kentän arvoista ja anna sitten sopiva arvo **Arvo**-kentässä. Lisätietoja vakioparametrijoukon käytöstä ja niiden arvojen valitsemista on [tarve-ennustemallien oletusparametreissa ja -arvoissa](#model-parameters).

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Yhteyden määrittäminen Azuren koneoppimispalveluun

Voit määrittää yhteyden Azuren koneoppimispalveluun **Azuren koneoppimispalvelu** -välilehdessä. Tämä ratkaisu on yksi perusennusteen luontivaihtoehdoista. Näillä tämän välilehden asetuksilla on vaikutus vain, kun **Ennusteiden luontistrategia** -kentän arvoksi on määritetty *Azuren koneoppimispalvelu*.

Lisätietoja Azuren koneoppimispalvelun määrittämisestä ja sen yhdistämisestä täällä olevien asetusten avulla on kohdassa [Azuren koneoppimispalvelun määrittäminen](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Yhteyden määrittäminen Azuren koneoppimisstudioon (klassinen)

> [!IMPORTANT]
> Azuren koneoppimisstudio (klassinen) vanhentunut. Siksi et voi enää luoda sitä varten uusia työtiloja Azuressa. Sen on korvannut Azuren koneoppimispalvelu, joka tarjoaa samankaltaisia toimintoja ja muita toimintoja. Jos et vielä käytä Azuren koneoppimista, sinun on tulisi aloittaa Azuren koneoppimispalvelun käyttö. Jos sinulla on jo työtila, joka on luotu Azuren koneoppimisstudiolle (klassinen), voit jatkaa sen käyttöä, kunnes ominaisuus on poistettu kokonaan Azuresta. Suosittelemme kuitenkin, että päivität Azuren koneoppimispalveluun mahdollisimman nopeasti. Vaikka sovellus edelleen varoittaa, että Azuren koneoppimisstudio (klassinen) on vanhentunut, se ei vaikuta ennustamiseen. Lisätietoja Azuren koneoppimispalvelusta ja sen määrittämisestä on kohdassa [Azuren koneoppimispalvelun määrittäminen](#setup-amls).
>
> Voit vaihtaa vapaasti uusien ja vanhojen koneiden oppimiseen luotujen ratkaisujen ja Supply Chain Managementin välillä, jos vanha Azuren koneoppimisstudio (klassinen) -työtila on vielä käytettävissä.

Jos sinulla on jo käytettävissä oleva Azuren koneoppimisstudio (klassinen) -työtila, voit käyttää sitä ennusteiden luomiseen yhdistämällä sen Supply Chain Managementiin. Voit muodostaa yhteyden käyttäen **Tarve-ennusteen parametrit** -sivun sarkainta, kun käytät **Azuren koneoppimisen** -välilehteä. (Tämän välilehden asetuksilla on vaikutusta vain, kun **Ennusteen luontistrategia** -kenttä on asetettu *Azuren koneoppimiseen*.) Anna seuraavat tiedot Azuren koneoppimisstudio (klassinen) -työtilasta:

- Verkkopalvelun ohjelmointirajapinta- (API)-avain
- Verkkopalvelun päätepisteen URL-osoite
- Azuren tallennustilin nimi
- Azuren tallennustilin avain

> [!NOTE]
> Azuren tallennustilin nimi ja avain tarvitaan vain, jos käytät mukautettua tallennustiliä. Jos käytät paikallista versiota, sinulla on oltava mukautettu tallennustili Azuressa niin, että automaattianalyysi voi käyttää historiallisia tietoja.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Tarve-ennustemallien oletusparametrit ja -arvot

Kun käytät koneoppimista ennustesuunnittelumallien luomiseen, voit ohjata koneiden koulutusvaihtoehtoja määrittämällä arvot *ennustealgoritmin parametreille*. Nämä arvot lähetetään toimitusketjun hallinnasta Supply Chain Managementista Azuren koneoppimiseen. **Ennustealgoritmin parametrit** -sivun avulla voit määrittää, minkä tyyppisiä arvoja on annettava ja mitä arvoja kullakin pitäisi olla.

Jos haluat määrittää kysynnän ennustemalleissa käytetyt oletusparametrit ja -arvot, siirry kohtaan **Pääsuunnittelu \> Asetukset \> Kysynnän ennuste \> Ennustealgoritmin parametrit**. Käytettävissä on vakioparametrijoukko. Kullakin parametrillä on seuraavat kentät:

- **Nimi** – Parametrin nimi, jota käytetään Azuressa. Tätä nimeä ei yleensä pidä muuttaa, ellet ole mukauttanut koetta Azuren koneoppimisessa.
- **Kuvaus** – Parametrin yleinen nimi. Tätä nimeä käytetään parametrin tunnistamiseen muissa järjestelmän paikoissa (esimerkiksi **Tarve-ennusteen parametrit** -sivulla).
- **Arvo** – Parametrin oletusarvo. Annettava arvo riippuu muokattavasta parametrista. 
- **Kuvaus** – Parametrin ja sen käytön lyhyt kuvaus. Tämä kuvaus sisältää tavallisesti **Arvo**-kentän kelvollisia arvoja koskevat ohjeet.

Oletusarvon mukaan käytetään seuraavia parametreja. (Jos haluat palata koskaan tähän vakioluetteloon, valitse **Palauta** toimintoruudussa.)

- **Luotettavuustasoprosentti** – Luottamusväli koostuu arvoalueesta, joka toimii hyvinä ennusteina kysynnän ennusteelle. 95 prosentin luotettavuustasoprosentti osoittaa, että on 5 prosentin riski siitä, että tuleva kysyntä on luottamusvälin ulkopuolella.
- **Pakota kausivaihtelu** – Määrittää, pakotetaanko malli käyttämään tietyn kausivaihtelutyyppiä. Tämä parametri koskee vain vaihtoehtoja ARIMA ja ETS. Vaihtoehdot: *AUTO (oletus)*, *NONE*, *ADDITIVE*, *MULTIPLICATIVE*.
- **Ennustemalli** – Määrittää, mitä ennustemallia käytetään. Vaihtoehdot: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *ALL*. Valitaksesi parhaiten sopivan mallin käytä *ALL*-vaihtoehtoa.
- **Ennusteen enimmäisarvo** – Määrittää ennusteissa käytettävän enimmäisarvon. Muoto: +1E[n] tai numeerinen vakio.
- **Ennusteen vähimmäisarvo** – Määrittää ennusteissa käytettävän vähimmäisarvon. Muoto: -1E[n] tai numeerinen vakio.
- **Puuttuvan arvon korvaus** – Määrittää, miten historiallisten tietojen aukot täytetään. Vaihtoehdot: *(numeerinen arvo)*, *MEAN*, *PREVIOUS*, *INTERPOLATE LINEAR*, *INTERPOLATE POLYNOMIAL*.
- **Puuttuvan arvon korvausalue** – Määrittää, koskeeko arvon korvaus vain kunkin yksittäisen rakeisuusmääritteen päivämääräaluetta vai koko tietojoukkoa. Seuraavat vaihtoehdot ovat käytettävissä sen päivämääräalueen määrittämiseen, jota järjestelmä käyttää täyttäessään historiatietojen aukkoja:

    - *GLOBAL* – Järjestelmä käyttää kaikkien rakeisuusmääritteiden koko päivämääräalueita.
    - *HISTORY_DATE_RANGE* – Järjestelmä käyttää tiettyä **Luo tilastollinen perusennuste** -valintaruudun **Historiallinen horisontti** -kenttäryhmän **Alkamispäivä**- ja **Päättymispäivä**-kentissä määritettyä päivämääräaluetta.
    - *GRANULARITY_ATTRIBUTE* – Järjestelmä käyttää kulloinkin käsiteltävänä olevan rakeisuusmääritteen päivämääräaluetta.

    > [!NOTE]
    > Rakeisuusmäärite on yhdistelmä ennustedimensioita, joiden perusteella ennuste tehdään. Voit määrittää ennustedimensioita **Kysynnän ennusteen parametrit** -sivulla.

- **Kausivaihtelun vihje** – Anna ennustemallia varten kausivaihtelutietojen vihje ennusteen tarkkuuden parantamiseksi. Muoto: kokonaisluku, joka kuvaa niiden jaksojen pituutta, jolloin kysyntäkuvio toistuu. Syötä esimerkiksi luku *6*, jos tiedot toistuvat kuuden kuukauden välein.
- **Testijoukon koon prosenttiosuus** – Historiatietojen prosenttiosuus käytettäväksi testiaineistona ennusteen tarkkuuden laskennassa.

Voit ohittaa nämä arvot siirtymällä kohtaan **Pääsuunnittelu \> Määritys \> Kysynnän ennuste \> Kysynnän ennusteen parametrit**. Voit ohittaa nämä parametrit **Kysynnän ennusteen parametrit** -sivulla seuraavilla tavoilla:

- Käyttää **Yleistä**-välilehteä parametrien yleiseen ohittamiseen.
- Käyttää **Nimikkeenkohdistusavaimet**-välilehteä parametrien ohittamiseksi tiettyä nimikkeenkohdennusavainta kohden. Tietyn nimikkeen kohdistustunnuksella ohitettavat parametrit vaikuttavat vain kyseiseen nimikkeen kohdistustunnukseen määritettyjen nimikkeiden ennusteisiin.

> [!NOTE]
> **Ennustealgoritmin parametri** -sivulla voit lisätä parametreja luetteloon toimintoruudun painikkeiden avulla tai poistaa parametreja luettelosta. Tätä lähestymistapaa ei yleensä kuitenkaan pidä käyttää, ellet ole mukauttanut koetta Azuren koneoppimisessa.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Azuren koneoppimispalvelun määrittäminen

Supply Chain Management laskee kysyntäennusteet käyttäen Azuren koneoppimispalvelua, joka on määritettävä ja suoritettava omassa Azure-tilauksessasi. Tässä osassa kuvaillaan, kuinka muodostit Azuren koneoppimispalvelun Azuressa, ja liitä se sitten Supply Chain Management -ympäristöön.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Ota Azuren koneoppimispalvelu käyttöön ominaisuudenhallinnassa

Ennen kuin voit käyttää ennustamiseen Azuren koneoppimispalvelua, sinun on otettava Supply Chain Managementin ominaisuus käyttöön integroinnin mahdollistamiseksi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Pääsuunnittelu*
- **Ominaisuuden nimi:** *Azuren koneoppimispalvelu kysynnän ennusteiden luomiseen*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Koneoppimispalvelun määrittäminen Azuressa

Jotta Azure voi käyttää koneoppimista ennusteiden käsittelyyn, sinun on määritettävä Azuren koneoppimistyötila tätä tarkoitusta varten. Vaihtoehtoja on kaksi:

- Jos haluat määrittää työtilan suorittamalla Microsoftin toimittaman komentosarjan, noudata seuraavia ohjeita kohdassa [Vaihtoehto 1: Suorita komentosarja määrittääksesi koneoppimistyötilan](#ml-workspace-script) -osion ja siirry sitten kohtaan [Määritä Azuren koneoppimispalvelun yhteysparametrit Supply Chain Managementissa](#demand-forecast-parameters) -osiossa.
- Jos haluat määrittää työtilan manuaalisesti, noudata seuraavia ohjeita kohdassa [Vaihtoehto 2: Suorita komentosarja manuaalisesti määrittääksesi koneoppimistyötilan](#ml-workspace-manual) -osion ja siirry sitten kohtaan [Määritä Azuren koneoppimispalvelun yhteysparametrit Supply Chain Managementissa](#demand-forecast-parameters) -osiossa. Tämä vaihtoehto vie enemmän aikaa, mutta se antaa sinulle enemmän hallintaa.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Vaihtoehto 1: Koneoppimisen työtilan automaattinen määrittäminen komentosarjan suorittamalla

Tässä osassa kuvataan, kuinka voit määrittää koneoppimisen työtilan käyttämällä Microsoftin toimittamaa automaattista komentotiedostoa. Voit halutessasi määrittää kaikki resurssit manuaalisesti noudattamalla ohjeita [Kohdassa 2: Määritä koneoppimisen työtila manuaalisesti](#ml-workspace-manual) -osa. Molempia vaihtoehtoja ei tarvitse suorittaa.

1. Avaa GitHubissa [Dynamics 365 Supply Chain Managementin kysynnän ennusteiden mallit Azure koneoppimisen avulla](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) -säilö (repo) ja lataa seuraavat tiedostot:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Avaa PowerShell-ikkuna ja suorita **quick_setup.ps1**-komentotiedosto, jonka latasit edellisessä vaiheessa. Noudata näytön ohjeita. Komentosarja määrittää tarvittavat työtilan, tallennuksen, oletustietosäilön ja tietojenkäsittelyresurssit. Tarvittavat putket on kuitenkin luotava noudattamalla tämän menetelmän jäljellä olevia vaiheita. (Putket tarjoavat tavan aloittaa ennustekomentosarjat Supply Chain Managementissa.)
1. Azuren koneoppimisstudiossa voit ladata **sampleInput.csv**-tiedoston, jonka latasit vaiheessa 1 säilöön, jonka nimi on *demplan-azureml*. (quick_setup.ps1-komentosarja loi tämän kontin.) Tiedoston on julkaistava putki ja luotava testiennuste. Lisätietoja on kohdassa [Lataa blob-objektilohko](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. Valitse Azuren koneoppimispalvelustudion navigaattorissa **Notebooks**.
1. **Tiedosto**-rakenne sisältää seuraavan sijainnin: **Käyttäjät/\[nykyinen käyttäjä\]/src**.
1. Lataa loput neljä vaiheessa 1 lataamaasi tiedostoa sijaintiin, jotka ovat edellisessä vaiheessa.
1. Valitse juuri lataamasi **api_trigger.py**-tiedosto ja suorita se. Se luo putken, joka voidaan käynnistää sovellusliittymän kautta.
1. Työtila on nyt määritetty. Siirry eteenpäin [Määritä Azuren koneoppimispalvelu -yhteysparametrit Supply Chain Management](#demand-forecast-parameters) -osiossa.

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Vaihtoehto 2: Koneoppimisen työtilan määrittäminen manuaalisesti

Tässä osassa kuvataan, kuinka koneoppimisen työtila määritetään manuaalisesti. Suorita tämän osan toimenpiteet vain, jos et halua suorittaa automaattista määrityskomentosarjaa, joka kuvataan [Kohdassa 1: Komentosarjan suorittaminen koneoppimisen työtilan määrittämiseksi](#ml-workspace-script) -osassa.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Vaihe 1: Uuden työtilan luominen

Luo uusi koneoppimisen työtila seuraavien ohjeiden mukaan.

1. Kirjaudu Azure-portaaliisi.
1. Avaa **Automaattianalyysipalvelut**-palvelu.
1. Avaa ohjattu **luonti**-toiminto valitsemalla työkalurivillä **Luo**.
1. Suorita ohjattu toiminto loppuun noudattamalla näyttöön tulevia ohjeita. Pidä seuraavat seikat mielessäsi:

    - Käytä oletusasetuksia, ellei muissa tämän luettelon pisteissä suositella eri asetuksia.
    - Varmista, että valitset sen maantieteellisen alueen, joka vastaa sitä aluetta, jossa Supply Chain Managementin esiintymä on otettu käyttöön. Muutoin osa tiedoistasi voi läpäistä aluerajat. Lisätietoja on myöhemmin tässä artikkelissa kohdassa [Tietosuojailmoitus](#privacy).
    - Käytä varattuja resursseja, kuten resurssiryhmiä, varastointitilejä, konttirekisteröintejä, Azuren avainsäilöjä ja verkkoresursseja.
    - Määritä tallennustilin nimi ohjatussa toiminnossa **Määritä Azuren koneoppimispalvelun -yhteyden parametrit** -sivulla. Käytä kysyntäennusteeseen varattua tiliä. Tähän tallennustiliin tallennetaan tarve-ennusteen syöttö- ja tulostustiedot.

Lisätietoja on kohdassa [Työtilan luonti](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>Vaihe 2: Tallennusvaraston määrittäminen

Seuraavien ohjeiden avulla voit määrittää tallennusvälineitäsi.

1. Avaa GitHubissa [Dynamics 365 Supply Chain Managementin kysynnän ennusteiden mallit Azure koneoppimisen avulla](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) -säilö ja lataa seuraavat **sampleInput.csv**-tiedosto.
1. Avaa tallennustili, jonka loit [Vaiheessa 1: Luo uusi työtila](#create-workspace) -osa.
1. Seuraa ohjeita kohdassa [Luo säilö](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) luodaksesi säilön, jonka nimi on *demplan-azureml*.
1. Lataa vaiheessa 1 lataamasi **sampleInput.csv**-tiedosto luomaasi säilöön. Tiedoston on julkaistava putki ja luotava testiennuste. Lisätietoja on kohdassa [Lataa blob-objektilohko](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>Vaihe 3: Oletustietosäilön määrittäminen

Seuraavien ohjeiden avulla voit määrittää oletustietosäilöjäsi.

1. Valitse Azuren koneoppimispalvelustudion navigaattorissa **Tietosäilöt**.
1. Luo uusi *Azure Blob-säilö* -tyyppinen tietovarasto, joka osoittaa *demplan-azureml* Blob-tallennussäiliöön, jonka loit [Vaiheessa 2: Määritä tallennustila](#config-storage) -osiossa. (Jos uuden tietosäilön todennustyyppi on *Tiliavain*, anna luodun tallennustilin tiliavain luodulle tallennustilille. Lisätietoja on kohdassa [Tallennustilin avainavainten hallinta](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).)
1. Tee uudesta tietosäilöstä oletustietosäilö avaamalla sen tiedot ja valitsemalla **Määritä oletustietosäilöksi**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Vaihe 4: Tietojenkäsittelyresurssien määrittäminen

Suorita ennusteiden luonnin komentosarjat määrittämällä tietojenkäsittelyresurssi Azuren koneoppimisstudiossa seuraavien komentosarjojen avulla.

1. Avaa [vaiheessa 1: Luo uusi työtila](#create-workspace) -osassa luomasi koneoppimistyötilan tietosivu. Etsi **Studion verkko-URL-osoite** -arvo ja avaa se valitsemalla linkki.
1. Valitse toimintoruudussa **Käsittele**.
1. Avaa uusi ohjattu toiminto, joka auttaa uuden tietojenkäsittelyinstanssin luomisessa, valitsemalla **Käsittele instanssit**-välilehdessä **Uusi**. Noudata näytön ohjeita. Tietojenkäsittely-esiintymää käytetään tarve-ennusteen putken luomiseen. (Se voidaan poistaa putken julkaisemisen jälkeen.) Käytä oletusasetuksia.
1. Avaa uusi ohjattu toiminto, joka auttaa uuden tietojenkäsittelyklusterin luomisessa, valitsemalla **Käsittele klusterit**-välilehdessä **Uusi**. Noudata näytön ohjeita. Tietojenkäsittelyklusteria käytetään kysyntäennusteiden tuottamiseen. Sen asetukset vaikuttavat suorituskykyyn ja ajon rinnakkaisuuden enimmäistasoon. Määritä seuraavat kentät, mutta käytä kaikkien muiden kenttien oletusasetuksia:

    - **Nimi** – Syötä *e2ecpucluster*.
    - **Virtuaalikoneen koko** – Määritä tämä asetus sen mukaan, kuinka paljon tietoja haluat käyttää kysynnän ennusteen syötteenä. Solmujen määrä ei saa ylittää lukua 11, koska kysyntäennusteen luonti edellyttää yhtä solmua ja tämän jälkeen ennusteen luonnissa tarvittavien solmujen enimmäismäärä on 10. (Solmun laskenta määritetään myös parameters.py-tiedostossa [Vaiheessa 5: Putkien luominen](#create-pipelines) -osassa.) Jokaisessa solmussa on useita työntekijäprosesseja, jotka ajavat ennustekomentosarjoja rinnakkain. Työn työntekijäprosessien kokonaismäärä on *Solmun ytimien lukumäärä* × *solmujen määrä*. Jos esimerkiksi laskentaklusterin tyyppi on *Standard\_D4* (kahdeksan ydintä) ja enintään 11 solmua ja jos `nodes_count`-arvoksi on määritetty *10* parameters.py-tiedostossa, rinnakkaisuustaso on 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>Vaihe 5: Putkien luominen

Putket tarjoavat tavan aloittaa ennustekomentosarjat Supply Chain Managementissa. Seuraavia ohjeita noudattamalla voit luoda vaaditut putket.

1. Avaa GitHubissa [Dynamics 365 Supply Chain Managementin kysynnän ennusteiden mallit Azure koneoppimisen avulla](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) -säilö ja lataa seuraavat tiedostot:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Valitse Azuren koneoppimispalvelustudion navigaattorissa **Notebooks**.
1. **Tiedosto**-rakenne sisältää seuraavan sijainnin: **Käyttäjät/\[nykyinen käyttäjä\]/src**.
1. Lataa neljä vaiheessa 1 lataamaasi tiedostoa sijaintiin, jotka ovat edellisessä vaiheessa.
1. Avaa Azure ja tarkista juuri **parameters.py**-tiedosto, jonka olet juuri ladannut. Varmista, että `nodes_count`-arvo on pienempi kuin arvo, jonka määritit laskentaklusteriin vaiheessa [4: Määritä laskentaresurssit](#config-compute-resources) -osassa. Jos `nodes_count`-arvo on suurempi tai yhtä suuri kuin laskentaklusterin solmujen määrä, putkisuoritus voi käynnistyä. Tämän jälkeen se lopettaa vastaamisen, kun se odottaa tarvittavia resursseja. Lisätietoja solmujen inventointiin on kohdassa [Vaihe 4: Laske resurssien määritys](#config-compute-resources).
1. Valitse juuri lataamasi **api_trigger.py**-tiedosto ja suorita se. Se luo putken, joka voidaan käynnistää sovellusliittymän kautta.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Uuden Active Directory -sovelluksen käyttöönottaminen

Active Directory -sovellus on todennettava resursseilla, jotka on varattu kysynnän ennusteeseen palvelun pääomistamisen avulla. Sen vuoksi sovelluksella tulisi olla pienin oikeustaso, joka tarvitaan ennusteen luomiseen.

1. Kirjaudu Azure-portaaliisi.
1. Rekisteröi uusi hakemus vuokralaisen Azure Active Directoryn (Azure AD) kautta. Katso ohjeet kohdasta [Azure AD -sovelluksen ja resursseja käyttävän palvelun päänimen luonti portaalin avulla](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Suorita ohjattu toiminto loppuun noudattamalla näyttöön tulevia ohjeita. Oletusasetusten käyttäminen.
1. Anna uudelle Active Directory -sovellukselle käyttöoikeudet seuraaviin resursseihin, jotka olet luonut [Koneoppimisen määrittäminen Azuressa](#ml-workspace) -osassa. Ohjeita on kohdassa [Määritä Azure-rooleja Azure-portaalia käyttämällä](/azure/role-based-access-control/role-assignments-portal?tabs=current). Tämän vaiheen avulla järjestelmä voi tuoda ja viedä ennustetietoja sekä käynnistää koneiden opetella putkiajoja Supply Chain Managementista.

    - Osallistujarooli koneoppiminen -työtilassa
    - Osallistujarooli on varattu varastotilille.
    - Blob-säilön osallistujarooli on varattu varastotilille.

1. Luo sovellukselle salaisuus luomasi sovelluksen **Todistukset ja salaisuudet** -osassa. Lisätietoja on kohdassa [Asiakassalaisuuden lisääminen](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Kirjoita huomautus sovelluksen tunnuksesta ja sen salaisuudesta. Tämän sovelluksen tietoja tarvitaan myöhemmin, kun määrität **Tarve-ennusteen parametrit** -sivun Supply Chain Managementissa.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Siirry eteenpäin Määritä Azuren koneoppimispalvelu -yhteysparametrit Supply Chain Management -osiossa.

Käytä seuraavaa menettelyä yhdistääksesi Supply Chain Management -ympäristösi koneoppimispalveluun, jonka olet juuri määrittänyt Azuressa.

1. Kirjaudu Supply Chain Managementiin.
1. Siirry kohtaan **Pääsuunnittelu \> Asetukset \> Kysynnän ennuste \> Kysynnän ennusteen parametrit**.
1. Tarkista **Yleiset**-välilehdestä, että **Ennusteen luonnin strategia** -kentän arvoksi on määritetty *Azuren koneoppimispalvelu*.
1. Varmista **Nimikkeen kohdistustunnukset** -välilehdessä, että **Ennusteen luonnin strategia** -kentän arvoksi on määritetty *Azuren koneoppimispalvelu* jokaiselle kohdistustunnukselle, jonka on määrä käyttää Kysynnän ennusteiden tuotannossa Azuren koneoppimispalvelua.
1. Määritä **Azuren koneoppimispalvelu** -välilehdellä seuraavat kentät:

    - **Vuokraajan tunnus** – Syötä Azure-vuokraajan tunnus. Tämän tunnuksen avulla Supply Chain Management todentaa Azuren koneoppimispalvelun. Voit etsiä vuokralaisen tunnuksesi Azure AD:n **Yhteenveto**-sivulta, joka on Azure-portaalissa.
    - **Palvelun pääsovellustunnus** – Määritä [Active Directory -sovelluksen](#aad-app) osassa luomasi sovelluksen sovellustunnus. Tätä arvoa käytetään, kun sovellus valtuuttaa ohjelmointirajapintapyynnöt Azuren koneoppimispalvelulle.
    - **Palveluobjektin salaisuus** – Määritä palvelun pääsovelluksen salaisuus sovellukselle, jonka loit [Active Directory -sovelluksessa](#aad-app). Tätä arvoa käytetään hankkimaan käyttöoikeustunnus suojausperiaatteelle, jonka loit valtuutettujen toimintojen suorittamiseksi Azure-säilöä ja Azure Machine Language -työtilaa vastaan.
    - **Tallennustilin nimi** – Kirjoita Azure-tallennustilin nimi, jonka määritit, kun suoritit ohjatun asennustoiminnon Azure-työtilassa. (Lisätietoja on osassa [Määritä koneoppiminen Azuressa](#ml-workspace).)
    - **Putken päätepisteen osoite** – Kirjoita putken REST-päätepisteen URL-osoite Azuren koneoppimispalvelulle. Olet luonut putken viimeiseksi vaiheeksi, kun [määrität koneoppimisen Azuressa](#ml-workspace). Jos haluat ottaa putken URL-osoitteen käyttöön, kirjaudu sisään Azure-portaaliin ja valitse siirtymispalkista **Putket**. Valitse **Putki**-välilehdestä putken päätepiste, jonka nimi on **TriggerDemandForecastGeneration**. Kopioi sitten näkyvissä näkyvä REST-päätepiste.

    ![Parametrit Kysynnän ennustamisen parametrit -sivun Azuren koneoppimispalvelu -välilehdellä.](media/azure-ml-service-parameters.png "Parametrit Kysynnän ennustamisen parametrit -sivun Azuren koneoppimispalvelu -välilehdellä")

## <a name="privacy-notice"></a><a name="privacy"></a>Tietosuojatiedot

Kun valitset ennusteen luomisstrategiaksi *Azuren koneoppimispalvelun*, Supply Chain Management lähettää automaattisesti asiakastiedot historialliseen kysyntään, kuten koostettuihin määriin, tuotenimiin ja tuotedimensioihin, lähetys- ja vastaanottosijaintoihin, asiakastunnuksiin ja ennusteparametreihin, maantieteelliselle alueelle, jossa koneoppimistyötilasi ja siihen linkitetty tallennustilisi sijaitsevat, tulevaisuuden tarpeiden ennustamista varten. Azuren koneoppimispalvelun maantieteellinen alue voi olla eri kuin maantieteellinen alue, jolla Supply Chain Management otetaan käyttöön. Osa käyttäjistä voi määrittää, onko tämä toiminto käytössä, valitsemalla Ennusteen luontistrategia **Tarve-ennusteen parametrit** -sivulla.

## <a name="additional-resources"></a>Lisäresurssit

- [Kysynnän ennustepalveluiden yleiskatsaus](introduction-demand-forecasting.md)
- [Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md)
- [Manuaalisten oikaisujen tekeminen perusennusteeseen](manual-adjustments-baseline-forecast.md)
- [Verkkoseminaari: Kysynnän ennustaminen Azuren koneoppimispalvelun sarjojen avulla](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
