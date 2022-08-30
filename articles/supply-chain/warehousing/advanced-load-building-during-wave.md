---
title: Lisäkuormanluonti aallon aikana
description: Tässä artikkelissa on tietoa aallon lisäkuormanluonnista, joka liittää lähetyksiä automaattisesti aiemmin luotuihin aaltoihin aallon suorituksen aikana. Tämän ansiosta voit luoda järkeviä trukkien kaltaisia kuormia ilman, että käytät kuormasuunnittelun työtilaa.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c9d41645531fa4318289f32a564c34f0f92681df
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335837"
---
# <a name="advanced-load-building-during-wave"></a>Lisäkuormanluonti aallon aikana

[!include [banner](../includes/banner.md)]

Aallon lisäkuormanluonti liittää lähetyksiä automaattisesti aiemmin luotuihin aaltoihin aallon suorituksen aikana. Tämän ansiosta voit luoda järkeviä trukkien kaltaisia kuormia ilman, että käytät kuormasuunnittelun työtilaa. Tämä ominaisuus on hyödyllinen yrityksille, jotka haluavat hyödyntää kuormia trukissa/perävaunussa lähetettävien tavaroiden jäljittämisessä ja suunnittelussa, mutta eivät halua luoda kuormia manuaalisesti joka päivä.

Aallon käsittelyn aikana järjestelmä yleensä luo uuden kuorman kaikille lähetyksille, joihin ei vielä ole liitetty kuormaa. Jos aallon lisäkuormanluonti on otettu käyttöön, järjestelmä kuitenkin liittää jokaisen irrallisen lähetyksen aiemmin luotuun kuormaan (jos sopiva löytyy), ja uusia kuormia luodaan vain tarvittaessa. Aallon lisäkuormanluonti luo automaattisesti uusia kuormia sinun määrittämiesi ehtojen perusteella.

Toimintoa voi käyttää sen jälkeen, kun järjestelmä on määritetty seuraavasti:

- Luo *aaltomalleja*, joissa on uusi **buildLoads**-menetelmä. Tämän menetelmän avulla aallon lisäkuormanluonti on saatavilla kyseisiä malleja käyttäville aalloille.
- Määritä *kuormanluonnin mallipohjat*, joista jokainen on linkitetty tiettyyn aaltomalliin ja-menetelmään. Kuormanluonnin mallipohjat ohjaavat, mihin kuormaan (aiemmin luotuun tai uuteen) aallotetut kuormarivit lisätään. Voit yhdistää tai erottaa lähetyksiä kuormamallin, laitteiden ja muiden kuormarivin kenttien arvojen kaltaisten ehtojen perusteella.
- Määritä *kuorman yhdistelmäryhmät* ja päätä, mitä kohteita saa ja mitä ei saa yhdistää yksittäiseen kuormaan. Voit myös määrittää, aiheuttaako rajoitus varoituksen tai virheen ja pitääkö kuormamallin tilavuusrajoitusta arvioida.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Järjestelmäsi aallon lisäkuormanluonnin käyttöönotto

Ennen kuin voit käyttää aallon lisäkuormanluontia, sinun on otettava järjestelmäsi kaksi toimintoa käyttöön. Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksissa. Toiminnot on lueteltu **Toimintojen hallinta** -työtilassa seuraavalla tavalla:

- Aallon kuormanluonnin toiminto:

    - **Moduuli:** *Varastonhallinta*
    - **Toiminnon nimi:** *Aallon kuormanluonnin toiminto*

- Organisaationlaajuinen aallon vaihekoodi:

    - **Moduuli:** *Varastonhallinta*
    - **Toiminnon nimi:** *Organisaationlaajuinen aallon vaihekoodi*

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Tämän demon käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

Voit hyödyntää tätä esittelyä myös ohjeena, kun työskentelet tuotantojärjestelmän parissa ja käytät tätä toimintoa. Tässä tapauksessa sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Varmista, että tilanteen määrittämiseen on riittävästi käytettävissä olevaa varastoa

Jos käytät **USMF**-esittelytietoja, sinun on ensin varmistettava järjestelmäsi asetukset ja se, että kaikissa oleellisissa sijanneissa on tarpeeksi varastoa. Tätä esittelyä varten seuraavan varastomäärän on oltava vapaana varastossa *62*:

- **Nimike A0001:** 10 kpl
- **Nimike A0002:** 10 kpl
- **Nimike M9200:** 10 kpl

Nimike **M9200** on lisättävä varastoon. Viimeistele menettelyt seuraavien alakohtien mukaan ja lisää nimike varastoon.

#### <a name="create-a-new-license-plate-id"></a>Uuden rekisterikilven tunnuksen luominen

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Rekisterikilvet**.
1. Valitse toimintoruudussa **Uusi**.
1. Syötä uuden rivin **Rekisterikilpi**-kenttään koodi *LP6203*.
1. Valitse **Tallenna**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Nimikkeen M9200 standardikustannuksen luominen toimipaikassa 6

1. Siirry kohtaan **Tuotetietojen hallinta** \> **Tuotteet** \> **Vapautetut tuotteet**.
1. Hae nimikettä **M9200**.
1. Valitse nimikkeen rivi ja sitten toimintoruudun **Kustannusten hallinta** -välilehden **Määrittäminen**-ryhmässä kohta **Nimikkeen hinta**.
1. Valitse **Nimikkeen hinta** -sivulla **Odottavat hinnat** -välilehti.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Kustannuslaskelmatyyppi:** *Suunniteltu kustannus*
    - **Hintatyyppi:** *Kustannus*
    - **Versio:** *10*
    - **Toimipaikka:** *6*
    - **Hinta:** *1,60*

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa kohta **Aktivoi odottavat hinnat**.
1. Valitse **Aktiiviset hinnat** -välilehti ja tarkista, että toimipaikan *6* uusi kustannushinta on lisätty.

#### <a name="create-inventory-in-warehouse-62"></a>Varastomäärän luominen varastossa 62

1. Valitse **Varastonhallinta** \> **Kirjauskansioviennit** \> **Nimikkeet** \> **Varaston oikaisu**.
1. Valitse toimintoruudussa **Uusi**.
1. Syötä **Luo varastokirjauskansio** -valintaikkunan **Yleiskatsaus**-pikavälilehden **Varasto**-kenttään luku *62*. Hyväksy oletusarvot kaikkiin muihin kenttiin.
1. Sulje valintaikkuna valitsemalla **OK**.
1. **Varaston oikaisu** -sivu avataan. Lisää rivi valitsemalla **Kirjauskansion rivit**-pikavälilehdellä **Uusi**.
1. Määritä uudelle riville seuraavat arvot. Hyväksy oletusarvot kaikkiin muihin kenttiin.

    - **Nimiketunnus:** *M9200*
    - **Sijainti:** *bulkki-003*
    - **Määrä:** Muuta arvoksi *10*.

1. Valitse toimintoruudussa **Tallenna**.
1. Tarkista virheet valitsemalla toimintoruudussa **Vahvista**.
1. Aloita tarkistus valitsemalla **Tarkista kirjauskansio** -valintaikkunassa **OK**. Näyttöön tulee sanoma, kun tarkistus on valmis.
1. Vahvista varaston oikaisu valitsemalla toimintoruudussa **Kirjaa**.
1. Aloita kirjaus valitsemalla **Kirjaa kirjauskansio** -valintaikkunassa **OK**. Näyttöön tulee sanoma, kun kirjaus on valmis.

## <a name="set-up-advanced-wave-load-building"></a>Aallon lisäkuormanluonnin määrittäminen

### <a name="regenerate-wave-process-methods"></a>Aallon käsittelymenetelmien muodostaminen uudelleen

Sinun on ehkä muodostettava aallon käsittelymenetelmät uudelleen, jotta kuormanluontimenetelmä (**buildLoads**) tulee näkyville.

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Aallot** \> **Aallon käsittelymenetelmät**.
2. Varmista, että **buildLoads** näkyy luettelossa. Jos se ei ole näkyvissä, lisää se valitsemalla toimintoruudussa kohta **Muodosta menetelmät uudelleen**.

### <a name="set-up-wave-templates"></a>Aaltomallien määrittäminen

Voit hyödyntää aallon lisäkuormanluontia, jos olet lisännyt **buildLoads**-menetelmän kaikkiin olennaisiin [aaltomalleihin](tasks/configure-wave-processing.md).

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Aallot** \> **Aaltomallit**.
1. Valitse aaltomalli.

    Jos käytät **USMF**-esittelytietoja, valitse **62 Lähetysoletus** -malli.

1. Valitse toimintoruudussa **Muokkaa**, jotta saat sivun muokkaustilaan.
1. Valitse **Menetelmät**-pikavälilehden **Jäljellä olevat menetelmät** -ruudukosta **buildLoad**-menetelmä.
1. Siirrä **buildLoads**-menetelmä **Valitut menetelmät** -ruudukkoon valitsemalla oikea nuolipainike.
1. Jos haluat määrittää **Aallon vaihekoodi** -arvon **buildLoads**-menetelmälle, sinun on ensin luotava koodi **Aallon vaihekoodit** -sivulla. Voit valita haluamasi arvon, mutta muista valintasi, koska tarvitset tietoa myöhemmin. Luo koodi **WSC2112** seuraavien ohjeiden avulla:

    1. Napsauta **buildLoads**-menetelmä rivillä **Aallon vaihekoodi** -kentän alanuolta hiiren kakkospainikkeella ja valitse sitten **Näytä tiedot**.
    1. Valitse **Aallon vaihekoodit** -sivun toimintoruudussa **Uusi**.
    1. Syötä **Aallon vaihekoodi** -kenttään koodi *WSC2112*.
    1. Syötä **Aallon vaihekuvaus** -kenttään koodi *WSC2112*.
    1. Valitse **Aallon vaihetyyppi** -kentässä *Kuormanluonti*.

1. Valitse **Tallenna** ja sulje sivu.
1. Valitse juuri luomasi koodi (**WSC2112**) **buildLoads**-menetelmän rivillä **Aallon vaihekoodi** -kentässä.
1. Valitse toimintoruudussa **Tallenna**.

> [!NOTE]
> Aallon vaihekoodit ovat koodeja, joita käyttäjät voivat määrittää ja käyttää aaltomenetelmien tiettyjen esiintymien linkittämiseen vastaaviin malleihin. Mallit sisältävät malleja täydennykselle, konttijärjestelmälle, etikettien tulostamiselle, kuormituksen luonnille ja lajittelulle.
>
> Kun aallon vaihekoodeja ei käytetä, käyttäjien on kirjoitettava vapaamuotoista tekstiä viitatakseen aaltomenetelmän esiintymän tiettyyn malliin. Vapaamuotoinen teksti on altis virheille, koska käyttäjien on varmistettava, että heidän aaltomalliin tiettyä aallon vaihemenetelmää varten syöttämänsä aallon vaiheen teksti vastaa kohdemallissa olevaa aallon vaiheen tekstiä tarkalleen.
>
> Tietyn aallon vaihetyypin aallon vaihekoodit määritetään erillisellä sivulla. Aallon vaihekoodi on valittava avattavasta luettelosta jokaiselle aaltomallin aallon vaiheen menetelmän esiintymälle, joka edellyttää aallon vaihekoodia. Avattavasta luettelosta tehty valinta korvaa syötetyn vapaamuotoisen tekstin ja auttaa vähentämään inhimillisten virheiden riskiä ja vaikutusta. Asetuskoodeja käytetään aaltomallissa oleva aallon vaiheen menetelmän linkittämiseksi menetelmän kohdemalliin.

### <a name="set-up-load-mix-groups"></a>Kuorman yhdistelmäryhmien määrittäminen

Kuorman yhdistelmäryhmät luovat säännöt sellaisten nimikkeiden tyypeille, jotka voidaan liittää yksittäiseen kuormaan. Voit määrittää niin monta kuorman yhdistelmäryhmää kuin on tarpeen. Jos kuitenkin haluat käyttää aallon lisäkuormanluontia, niitä on oltava vähintään yksi. Luo kuorman yhdistelmäryhmä noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Kuorma** \> **Kuorman yhdistelmäryhmät**.
1. Valitse toimintoruudussa **Uusi** ja luo kuormaryhmä.
1. Kirjoita **Kuorman yhdistelmäryhmän tunnus** -kenttään uuden ryhmän nimi.

    Jos käytät **USMF**-esittelytietoja, määritä seuraavat arvot:

    - **Kuorman yhdistelmäryhmän tunnus:** *TV*
    - **Kuvaus:** *TV*

1. Valitse toimintoruudussa **Tallenna**, jotta **Kuorman yhdistelmäryhmän ehdot** -pikavälilehti tulee näkyville.
1. Lisää ruudukkoon uusi rivi **Kuorman yhdistelmäryhmän ehdot** -pikavälilehdessä valitsemalla **Uusi**.
1. Aseta uuden rivin kenttiin haluamasi arvot. Nämä arvot määrittävät nimikeryhmät, jotka otetaan huomioon kuormayhdistelmässä.

    Jos käytät **USMF**-esittelytietoja, valitse *TV ja video* **Nimikeryhmä**-kentässä.

1. Valitse toimintoruudussa **Tallenna**, jotta **Kuorman yhdistelmäryhmän rajoitukset** -pikavälilehti tulee saataville.
1. Lisää ruudukkoon uusi rivi **Kuorman yhdistelmäryhmän rajoitukset** -pikavälilehdessä valitsemalla **Uusi**.
1. Aseta uuden rivin kenttiin haluamasi arvot.

    Jos käytät **USMF**-esittelytietoja, määritä seuraavat arvot:

    - **Nimikeryhmä:** *CarAudio*
    - **Kuormanluontitoiminto:** *Rajoita* (Tämä arvo estää **CarAudio**-nimikeryhmään kuuluvien nimikkeiden pääsyn samaan kuormaan **TV ja video** -nimikeryhmään kuuluvien nimikkeiden kanssa.)

1. Jatka sääntöjen luomista kunnes olet lisännyt kaikki kuorman yhdistelmäryhmälle vaaditut ehdot ja rajoitukset.

Jos käytät **USMF**-esittelytietoja, tämä määritys on osaltasi valmis.

### <a name="set-up-load-build-templates"></a>Määritä kuormanluontimallit

Voit määrittää niin monta kuormanluontimallia kuin on tarpeen. Jos kuitenkin haluat käyttää aallon lisäkuormanluontia, niitä on oltava vähintään yksi. Luo kuormanluontimalli noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Kuorma** \> **Aallon kuormanluontimalli**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle riville seuraavat arvot.

    | Kenttä | kuvaus | USMF-esittelytietojen arvo |
    |---|---|---|
    | Järjestysnumero | Tilaus, jossa malli arvioidaan. | *1* |
    | Kuormituksen luontimallin nimi | Syötä kuormanluontimallin yksilöivä tunniste. Sinun on annettava mallille se nimi, jonka loit tai päivitit aiemmin tämän määrityksen aikana. | *62 Lähetysoletus* |
    | Aallon vaihekoodi | Syötä aallon vaihekoodi, jolla malli linkitetään aaltomenetelmään. Syötä **buildLoads**-menetelmälle koodi, jonka valitsit aiemmin aaltomallin asettamisen yhteydessä tämän määrityksen aikana. | *WSC2112* |
    | Kuorman mallitunnus | Valitse kuormamalli, jolla luodaan uusia kuormia ja johon vertailu tehdään, kun aiemmin luotuja kuormia määritetään. Kuormamalli määrittää, mikä on koko kuormalle sallittu enimmäispaino ja -tilavuus. | *Vakiokuormamalli* |
    | Laite | Laite, johon vertailu tehdään uusien kuormien määrityksessä ja jonka tiedot syötetään uusiin kuormiin. | Jätä tämä kenttä tyhjäksi. |
    | Kuormituksen yhdistelmäryhmän tunnus | Valitse kuorman yhdistelmäryhmä, jota käytetään, jos nimike saa olla kuormassa. Yhdistelmäryhmä luo säännöt sellaisten nimikkeiden tyypeille, jotka voidaan liittää yksittäiseen kuormaan. Sinun on valittava jokin tässä määrityksessä aiemmin luomistasi yhdistelmäryhmistä. | *TV* |
    | Käytä avoimia kuormituksia | Valitse, haluatko lisätä aiemmin luodut avatut kuormat. Käytettävissä ovat seuraavat asetukset:<ul><li>**Ei mitään** – Älä lisää avoimia kuormia mihinkään aiemmin luotuihin kuormiin.</li><li>**Mikä tahansa** – Lisää avoimet kuormat mihin tahansa aiemmin luotuun kyseiselle riville sallittuun kuormaan.</li><li>**Määritetty** – Lisää avoimet kuormat aallolle määritettyyn kuormaan.</li></ul> | *Mikä tahansa* |
    | Luo kuormitukset | Määritä, luodaanko uusia kuormia, jos ehtoja vastaavia kuormia ei löydy. | Valittu (= *Kyllä*) |
    | Salli lähetysrivin jakaminen | Määritä, voidaanko yksittäinen kuormarivi jakaa useille kuormille, jos koko rivin enimmäiskapasiteetti ylittää kuormamallille määritetyn kapasiteetin. | Selvitetyt (= *Ei*) |
    | Vahvista tilavuustiedot | Määritä, pitääkö kuormanluonnin tarkistaa paino ja tilavuus aina, kun kuormarivi lisätään ja tarkistaa, että kuormamallin tilavuusrajoissa pysytään. | Selvitetyt (= *Ei*) |

1. Valitse toimintoruudussa **Tallenna**, jotta **Muokkaa kyselyä** -vaihtoehto tulee näkyville.
1. Valitse toimintoruudussa kohta **Muokkaa kyselyä** ja avaa kyselyn muokkaamisen valintaikkuna.
1. Lisää ruudukkoon rivi valitsemalla valintaruudun **Lajittelu**-välilehdessä **Lisää**.
1. Määritä haluamasi lajitteluperusteet uudelle riville. Aseta esimerkiksi seuraavat arvot, jos haluat lajitella hakutulokset nousevassa järjestyksessä tilausnumeron perusteella:

    - **Taulukko:** *Kuorman tiedot*
    - **Johdettu taulukko:** *Kuorman tiedot*
    - **Kenttä:** *Tilausnumero*
    - **Hakusuunta:** *Laskeva*

1. Valitse **OK**, tallenna muutokset ja sulje valintaikkuna.
1. Määritä **Jakoperuste**-pikavälilehdessä säännöt, joiden mukaan kuormat jaetaan. Yleensä voit jakaa mukautetut kentät, jotka on laajennettu kuormariville – näitä ovat esimerkiksi **Reitti**, **Esittely** tai **Suorittaminen**. Jos haluat esimerkiksi luoda yhden kuorman tilausnumeroa kohti, valitse **Jakoperuste**-valintaruutu riville, jossa on seuraavat arvot:

    - **Viitetaulukon nimi:** *Kuorman tiedot*
    - **Viitekentän nimi:** *Tilausnumero*

## <a name="scenario"></a>Skenaario

Tässä tilanteessa näytetään, miten tässä artikkelissa aiemmin kuvaillut asetukset vaikuttavat varastotoimintoihin, kun myyntitilausta käsitellään. Tässä tilanteessa käytetään **USMF**-esittelytietoja ja muita kyseisissä määritysohjeissa annettuja esittelyarvoja.

### <a name="create-sales-orders"></a>Myyntitilausten luominen

1. Siirry kohtaan **Myynti ja markkinointi** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi** ja avaa **Luo myyntitilaus**-valintaikkuna.
1. Lisää valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-007*.
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *62*.

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilauksesi avataan. **Myyntitilausrivit**-pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi. Aseta uuden rivin **Nimiketunnus**-kentän arvoksi *A0001* ja **Määrä**-kentän arvoksi *1*.
1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Valitse **Varaus**-sivun toimintoruudussa kohta **Varaa erä**.
1. Valitse **Sulje**-painike (**X**) sivun oikeasta yläkulmasta ja palaa myyntitilaukseen.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**. Järjestelmä luo lähetyksen ja lisää sen uuteen kuormaan, koska aiemmin luoduissa kuormissa on jo tämän tilausnumeron sisältäviä kuormarivejä.

    Näyttöön tulee tietosanomia, joissa kerrotaan tälle tilaukselle luodut työ, aalto ja lähetys.

1. Vahvista kuorma, lähetys ja työn tiedot myyntirivillä, valitse rivi ja valitse sitten ruudukon yläpuolelta **Varasto**-valikko ja sieltä **Kuorman tiedot**, **Lähetystiedot** tai **Työn tiedot**.
1. Valitse juuri luomasi myyntitilaus ja lisää uusi rivi valitsemalla **Myyntitilausrivit**-pikavälilehdessä kohta **Lisää rivi**.
1. Aseta uuden rivin **Nimiketunnus**-kentän arvoksi *A0002* ja **Määrä**-kentän arvoksi *1*.
1. Varaa rivi toistamalla sama riveillä 6–9 ja vapauta se varastoon. Järjestelmä luo **uuden** lähetyksen lisäämällesi riville. Koska kuitenkin hyödynnät aallon kuormanluontia, järjestelmä lisää lähetyksen ja kuormarivin aiemmin luotuun aaltoon. Jos aallon lisäkuormanluonti ei ole käytössä, järjestelmä luo lähetykselle uuden kuorman.
1. Valitse juuri luomasi myyntitilaus ja lisää uusi rivi valitsemalla **Myyntitilausrivit**-pikavälilehdessä kohta **Lisää rivi**.
1. Aseta uuden rivin **Nimiketunnus**-kentän arvoksi *M9200* ja **Määrä**-kentän arvoksi *1*.
1. Varaa rivi toistamalla sama riveillä 6–9 ja vapauta se varastoon. Kuten aiemminkin, järjestelmä luo **uuden** lähetyksen lisäämällesi riville. Koska nimike on kuitenkin peräisin **CarAudio**-nimikeryhmästä, se **ei läpäise rajoitteita, jotka asetit kuorman yhdistelmäryhmälle**. Siksi se **lisätään uuteen kuormaan**. Jos et olisi määrittänyt kuorman yhdistelmäryhmää kuorman luontimallissa, tämä lähetys oltaisiin lisätty ensimmäiseen kuormaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]