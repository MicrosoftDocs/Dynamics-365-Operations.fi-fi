---
title: Suunnittelun muutostenhallintatoiminnon esittely
description: Tässä aiheessa esitellään ja käsitellään kattavasti suunnittelun muutostenhallinnan käyttämistä.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c1c67559a8f2e9d0abb512f4231aea495d1957c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573990"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Suunnittelun muutostenhallintatoiminnon esittely

[!include [banner](../includes/banner.md)]

Tässä aiheessa esitellään ja käsitellään kattavasti suunnittelun muutostenhallinnan käyttämistä. Siinä käsitellään tärkeimmät skenaariot:

- Perustoiminnon määritys
- Uuden suunnittelutuotteen luonti suunnitteluyrityksessä
- Suunnittelutuotteen vapauttaminen suunnitteluyrityksestä paikalliselle yritykselle
- Suunnitteluyrityksen paikalliselle yritykselle vapauttaman tuotteen tarkistaminen ja hyväksyminen
- Suunnittelutuotteen käyttäminen paikallisen yrityksen vakiotapahtumissa
- Suunnittelutuotteen lisääminen myyntitilaukseen
- Muutosten pyytäminen suunnittelutuotteeseen luomalla suunnittelun muutospyyntö
- Pyydettyjen muutosten ajoittaminen ja toteuttaminen luomalla suunnittelun muutostilaus
- Muutetun tuotteen vapauttaminen

Kaikissa tämän aiheen harjoituksissa käytetään Microsoft Dynamics 365 Supply Chain Managementin vakiomallitietoja. Tämän lisäksi kukin harjoitus perustuu edelliseen harjoitukseen. Harjoitukset kannattaakin tämän vuoksi tehdä järjestyksessä alusta loppuun. Tämä on erityisen hyödyllistä silloin, jos suunnittelun muutoksenhallintatoimintoa ei ole käytetty aiemmin. Tällä tavoin toiminnosta kattava kokonaiskuva.

## <a name="set-up-for-the-sample-scenario"></a>Malliskenaarion määrittäminen

Tässä aiheessa olevan malliskenaarion toteuttaminen edellyttää, että toiminto valmistellaan ottamalla esittelytiedot käyttöön ja lisäämällä muutamia mukautettuja tietueita.

Ennen tässä aiheessa olevien harjoitusten tekemistä on toimittava seuraavien alaosien ohjeiden mukaisesti. Näissä alaosissa käsitellään useita tärkeitä asetussivuja, joita käytetään määritettäessä suunnittelun muutostenhallintaa organisaatiossa.

### <a name="make-standard-demo-data-available"></a>Vakioesittelytietojen ottaminen käyttöön

Käytä järjestelmää, johon [vakioesittelytiedot on asennettu](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Vakioesittelytiedot lisäävät useiden esittely-yritysten (yhtiöiden ja organisaatioiden) tietoja. Harjoituksia tehtäessä siirtymispalkin oikealla puolella on yritysvalitsin, jolla siirrytään yhdestä *suunnitteluorganisaatioksi* määritetystä yrityksestä (*DEMF*) toiseen *toiminnalliseksi organisaatioksi* määritettyyn yritykseen (*USMF*).

### <a name="set-up-an-engineering-organization"></a>Suunnitteluorganisaation määrittäminen

Suunnitteluorganisaatio omistaa suunnittelutiedot sekä vastaa tuotesuunnittelusta ja tuotemuutoksista. Suunnitteluorganisaatio määritetään seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta &gt; Määritys &gt; Suunnitteluorganisaatiot**.
1. Lisää rivi ruudukkoon valitsemalla **Uusi** ja määritä sitten seuraavat arvot:

    - **Suunnitteluorganisaatio:** *DEMF*
    - **Organisaation nimi:** *Contoso Entertainment System Germany*

    ![Suunnitteluorganisaation lisääminen.](media/engineering-org.png "Suunnitteluorganisaation lisääminen")

### <a name="set-up-the-version-product-dimension-group"></a>Version tuotedimensioryhmän määrittäminen

1. Valitse **Tuotetietojen hallinta &gt; Määritys &gt; Dimensiot ja varianttiryhmät &gt; Tuotedimensioryhmät**.
1. Luo tuotedimensioryhmä valitsemalla **Uusi**.
1. Valitse **Nimi** -kentän asetukseksi *Versio*.
1. Tallenna uusi dimensio ja lataa arvot **Tuotedimensiot**-pikavälilehteen valitsemalla **Tallenna**.
1. Määritä **Tuotedimensiot**-pikavälilehdessä **Versio** aktiiviseksi tuotedimensioksi.

    ![Tuotedimensioryhmän lisääminen.](media/product-dimension-groups.png "Tuotedimensioryhmän lisääminen")

### <a name="set-up-product-lifecycle-states"></a>Tuotteen elinkaaren tilojen määrittäminen

Suunnittelutuotteen elinkaaren eri vaiheissa on tärkeää, että kussakin elinkaaren tilassa sallittuja tapahtumia voidaan hallita. Määritä tuotteen elinkaaren tilat seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta &gt; Määritys &gt; Tuotteen elinkaaren tila**.
1. Lisää elinkaaren tila valitsemalla **Uusi** ja määritä sitten seuraavat arvot:

    - **Tila:** *Toiminnassa*
    - **Kuvaus:** *Toiminnassa*

1. Tallenna uusi elinkaaren tila ja lataa arvot **Käyttöönotetut liiketoimintaprosessit** -pikavälilehteen valitsemalla **Tallenna**.
1. Valitse **Käyttöönotetut liiketoimintaprosessit** -pikavälilehdessä liiketoimintaprosessit, joiden on oltava käytettävissä. Jätä tässä esimerkissä **Käytäntö**-kentän asetukseksi *Käytössä* kaikkien liiketoimintaprosessien osalta.

    ![Elinkaaren tilan liiketoimintaprosessien ottaminen käyttöön.](media/product-lifecycle-states-1.png "Elinkaaren tilan liiketoimintaprosessien ottaminen käyttöön")

1. Lisää toinen elinkaaren tila valitsemalla **Uusi** ja määritä sitten seuraavat arvot:

    - **Tila:** *Prototyyppi*
    - **Kuvaus:** *Prototyyppi*

1. Tallenna uusi elinkaaren tila ja lataa arvot **Käyttöönotetut liiketoimintaprosessit** -pikavälilehteen valitsemalla **Tallenna**.
1. Valitse **Käyttöönotetut liiketoimintaprosessit** -pikavälilehdessä liiketoimintaprosessit, joiden on oltava käytettävissä. Määritä tässä esimerkissä **Käytäntö**-kentän asetukseksi *Käytössä mutta varoitus* kaikkien liiketoimintaprosessien osalta.

    ![Elinkaaren tilan liiketoimintaprosessien ottaminen käyttöön (sisältää varoituksia).](media/product-lifecycle-states-2.png "Elinkaaren tilan liiketoimintaprosessien ottaminen käyttöön (sisältää varoituksia)")

### <a name="set-up-a-version-number-rule"></a>Versionumerosäännön määrittäminen

1. Valitse **Suunnittelun muutostenhallinta &gt; Määritys &gt; Tuoteversion numerosääntö**.
1. Lisää sääntö valitsemalla **Uusi** ja määritä sitten seuraavat arvot:

    - **Nimi:** *Automaattinen*
    - **Numerosääntö:** *Automaattinen*
    - **Muoto:** *V-\#\#*

    ![Tuoteversion numerosäännön lisääminen.](media/version-number-rule.png "Tuoteversion numerosäännön lisääminen")

### <a name="set-up-a-product-release-policy"></a>Tuotteen vapautuskäytännön määrittäminen

1. Valitse **Suunnittelun muutostenhallinta &gt; Määritys &gt; Tuotteen vapautuskäytännöt**.
1. Lisää vapautuskäytäntö valitsemalla **Uusi** ja määritä sitten seuraavat arvot:

    - **Nimi:** *Osat*
    - **Kuvaus:** *Osat*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Tuotetyyppi:** *Nimike*
    - **Käytä malleja:** *Aina*
    - **Aktiivinen:** *Kyllä*

1. Lisää rivi valitsemalla **Kaikki tuotteet** -pikavälilehdessä **Lisää** ja määritä sitten seuraavat arvot:

    - **Yhtiö:** *DEMF*
    - **Vapautettu mallituote:** *D0006*

1. Lisää toinen rivi valitsemalla **Lisää** ja määritä sille seuraavat arvot:

    - **Yrityksen tilien tunnus:** *USMF*
    - **Vapautettu mallituote:** *D0006*
    - **Vastaanoton tuoterakenne**: valitse tämä valintaruutu.
    - **Kopioi tuoterakenteen hyväksyntä:** valitse tämä valintaruutu.
    - **Kopioi tuoterakenteen aktivointi:** valitse tämä valintaruutu.
    - **Vastaanoton reitti**: valitse tämä valintaruutu.
    - **Kopioi reitin hyväksyntä:** valitse tämä valintaruutu.
    - **Kopioi reitin aktivointi:** valitse tämä valintaruutu.

    ![Tuotteen vapautuskäytännön lisääminen.](media/product-release-policy.png "Tuotteen vapautuskäytännön lisääminen")

### <a name="set-up-an-engineering-product-category"></a>Suunnittelun tuoteluokan määrittäminen 

Suunnittelun tuoteluokat muodostavat perustan suunnittelutuotteiden luonnille (eli tuotteille, joita versioidaan ja hallitaan suunnittelun muutostenhallinnan avulla). Suunnittelun tuoteluokat määritetään seuraavasti:

1. Valitse **Suunnittelun muutostenhallinta &gt; Suunnittelun tuoteluokan tiedot**.
1. Luo luokka valitsemalla **Uusi**.
1. Määritä **Tiedot**-pikavälilehdessä seuraavat arvot:

    - **Nimi:** *Osat*
    - **Suunnitteluorganisaatio:** *DEMF*
    - **Tuotetyyppi:** *Nimike*
    - **Version seuranta tapahtumissa:** *Kyllä*
    - **Tuotedimensioryhmä:** *Versio*
    - **Tuotteen elinkaaren tila luotaessa:** *Toiminnassa*
    - **Version numerosääntö:** *Automaattinen*
    - **Pakotettu voimassaolo:** *Ei*
    - **Käytä numerosäännön nimikkeistöä:** *Ei*
    - **Käytä nimisäännön nimikkeistöä:** *Ei*
    - **Käytä kuvaussäännön nimikkeistöä:** *Ei*

1. Määritä **Vapautuskäytäntö**-pikavälilehdessä **Tuotteen vapautuskäytäntö** -asetukseksi *Osat*.
1. Valitse **Tallenna**.

    ![Suunnittelun tuoteluokan lisääminen.](media/product-category-details.png "Suunnittelun tuoteluokan lisääminen")

### <a name="set-up-product-acceptance-conditions"></a>Tuotteen hyväksyntäehtojen määrittäminen

1. Käytä siirtymispalkin oikealla puolella olevaa yritysvalitsinta ja vaihda *USMF*-yritykseen (yhtiöön).
1. Valitse **Suunnittelun muutostenhallinta &gt; Määritys &gt; Suunnittelun muutostenhallinnan parametrit**.
1. Määritä **Vapauta hallinta** -välilehden **Tuotteen hyväksyntä** -osassa **Tuotteen hyväksyntä** -kentän asetukseksi *Manuaalinen*.

    ![Tuotteen hyväksyntäehtojen määrittäminen.](media/engineering-change-management-parameters.png "Tuotteen hyväksyntäehtojen määrittäminen")

## <a name="create-a-new-engineering-product"></a>Uuden suunnittelutuotteen luominen

Suunnittelutuote on tuote, jota versioidaan ja hallitaan suunnittelun muutostenhallinnassa. Toisin sanoen voit siis hallita muutoksia elinkaaren aikana, ja muutosten tiedot tallennetaan käyttämällä suunnittelun muutostilauksia. Suunnittelutuotteita luodaan seuraavasti:

1. Varmista, että olet suunnitteluorganisaation yrityksessä (tässä esimerkissä *DEMF*). Käytä tarvittaessa siirtymispalkin oikealla puolella olevaa yhtiövalitsinta.
1. Seuraa **Vapautetut tuotteet** -sivu jollakin seuraavista tavoista:

    - Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.
    - Valitse **Suunnittelun muutostenhallinta &gt; Yleinen &gt; Vapautetut tuotteet**.

1. Valitse toimintoruudun **Tuote**-välilehden **Uusi**-ryhmässä **Suunnittelutuote**.
1. Aseta **Uusi tuote** -valintaikkunassa seuraavat arvot:

    - **Suunnittelutuotteen luokka:** *Osat*
    - **Tuotenumero:** *Z0001*
    - **Tuotteen nimi:** *Kaiutinsarja*

    ![Suunnittelutuotteen lisääminen.](media/new-product-dialog.png "Suunnittelutuotteen lisääminen")

    Huomaa, että **Versio**-kenttä määritetään automaattisesti käyttämällä aiemmin määritettyä tuoteversion numerosääntöä.

1. Valitse **OK** luodaksesi tuotteen. Sulje valintaikkuna.
1. Uuden tuotteen tietosivu avautuu. Huomaa, että joidenkin kenttien arvot on jo täytetty. Tällaisia kenttiä ovat esimerkiksi **Varastodimensioryhmä**, **Seurantadimensioryhmä** ja/tai **Nimikemalliryhmä**. Nämä kentät määritettiin automaattisesti, koska tuote vapautetaan *DEMF*-yrityksessä ja tuotteen vapautuskäytäntönä on *Osat*, mikä on liitetty suunnittelutuotteen *Osat*-luokkaan. Koska aiemmin käytettiin nimikettä *D0006* mallina *DEMF*-yrityksen rivin määrittämiseen, täytetyt arvot otettiin nimikkeestä *D0006*.

    ![Vapautetun tuotteen tiedot.](media/product-details.png "Vapautetun tuotteen tiedot")

1. Voit tarkastella tuotteen versioita valitsemalla toimintoruudun **Suunnittele**-välilehden **Suunnittelun muutostenhallinta** -ryhmässä **Suunnitteluversiot**.

    ![Suunnitteluversiot.](media/engineering-versions-list.png "Suunnitteluversiot")

1. Huomaa, että **Suunnitteluversiot**-sivulla on vain yksi tuotteen versio, joka on aktiivinen.
1. Voit tarkastella version tietoja valitsemalla sen.

    ![Suunnitteluversion tiedot.](media/engineering-version-details.png "Suunnitteluversion tiedot")

1. Valitse **Suunnitteluversio**-sivun **Tuoterakenne**-pikavälilehdessä **Luo tuoterakenne**.
1. Määritä **Luo tuoterakenne** -valintaikkunassa seuraavat arvot:

    - **Tuoterakenteen numero:** Z0001
    - **Nimi**: Kaiutinsarja
    - **Toimipaikka:** 1

    ![Tuoterakenteen luominen.](media/create-bom.png "Tuoterakenteen luominen")

1. Lisää tuoterakenne valitsemalla **OK** ja sulje valintaikkuna.
1. Valitse **Tuoterakenne**-pikavälilehdessä **Tuoterakenne**.
1. Lisää **Tuoterakenne**-sivun **Tuoterakennerivit**-pikavälilehdessä kolme riviä, yksi kullekin nimiketunnukselle *D0001*, *D0003* ja *D0006*.

    ![Tuoterakennerivien lisääminen.](media/bom.png "Tuoterakennerivien lisääminen")

1. Valitse **Tallenna**.
1. Sulje sivu.
1. Valitse **Suunnitteluversio**-sivun **Tuoterakenne**-pikavälilehdessä **Hyväksy**.
1. Valitse avautuvassa valintaikkunassa **OK**.

    ![Tuoterakenteen hyväksyminen.](media/approve-dialog.png "Tuoterakenteen hyväksyminen")

1. Valitse **Suunnitteluversio**-sivun **Tuoterakenne**-pikavälilehdessä **Aktivoi**.
1. Huomaa, että tuoterakenteen **Aktiivinen**- ja **Hyväksytty**-valintaruudut on valittu.

    ![Aktiivinen ja hyväksytty tuoterakenne.](media/approved-bom.png "Aktiivinen ja hyväksytty tuoterakenne")

1. Sulje sivu.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Suunnittelutuotteen vapauttaminen paikalliseen yritykseen

Suunnitteluosasto on nyt suunnitellut tuotteen. Tässä esimerkissä tuote on prototyyppi, jonka suunnittelija on suunnitellut asiakkaalle. Koska asiakas on *USMF*-yrityksen asiakas, tuote on vapautettava kyseiselle yritykselle.

1. Säilytä yritysasetuksena *DEMF*. (Käytä tarvittaessa siirtymispalkin oikealla puolella olevaa yhtiövalitsinta.)
1. Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.
1. Valitse tuote *Z0001*.
1. Avaa ohjattu **Vapauta tuotteet** -toiminto valitsemalla toimintoruudun **Tuote**-välilehden **Ylläpito**-ryhmässä **Vapauta tuoterakenne**.
1. Valitse **Valitse vapautettavat suunnittelutuotteet** -sivulla tuotteen *Z0001* **Valitse**-valintaruutu.

    ![Vapautettavien suunnittelutuotteiden valitseminen.](media/select-eng-product-to-release.png "Vapautettavien suunnittelutuotteiden valitseminen")

1. Valitse **Vapauta tiedot**.
1. Voit tarkastella avautuvalla **Tuotteen vapautustiedot** -sivulla vapautettavan tuotteen tietoja ja sen tuoterakennetta. Huomaa, että **Lähetä tuoterakenne** -asetuksena on *Kyllä*. Niinpä sekä tuote *Z0001* että kaikki sen alinimikkeet vapautetaan tuoterakenteesta.

    Voit tarkastella alinimikkeiden tietoja valitsemalla sen vasemmassa ruudussa. Jos alinimikkeellä on tuoterakenne, voit valita myös kyseisen nimikkeen tuoterakenteen vapauttamisen.

    ![Tuotteen vapautustietojen tarkistaminen.](media/product-release-details.png "Tuotteen vapautustietojen tarkistaminen")

1. Palaa ohjattuun **Vapauta tuotteet** -toimintoon sulkemalla sivu.
1. Avaa **Valitse vapautettava tuote** -sivu valitsemalla **Seuraava**. Jos olit valinnut jonkin vakiotuotteen (ei suunnitellun tuotteen), ne näkyisivät tällä sivulla. Huomaa, että kun vapautat vakiotuotteen valitsemalla **Vapauta tuotteen rakenne**, myös sen tuoterakenne ja reitti vapautetaan.

    ![Vapautettavien vakiotuotteiden valitseminen.](media/select-std-product-to-release.png "Vapautettavien vakiotuotteiden valitseminen")

1. Avaa **Valitse vapautettavat tuotevariantit** -sivu valitsemalla **Seuraava**. Tässä esimerkissä ei ole variantteja.
1. Avaa **Valitse yhtiöt** -sivu valitsemalla **Seuraava**.
1. Valitse yhtiöt, joille tuote on vapautettava. Valitse tässä esimerkissä **USMF**-valintaruutu.

    ![Niiden yhtiöiden valinta, joita vapautus koskee.](media/select-release-companies.png "Niiden yhtiöiden valinta, joita vapautus koskee")

1. Avaa **Vahvista valinta** -sivu valitsemalla **Seuraava**.
1. Valitse **Valmis**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Tuotteen tarkistaminen ja hyväksyminen ennen vapauttamista paikalliselle yhtiölle

Suunnitteluosasto on nyt vapauttanut tiedot paikallisille yhtiöille, joissa tuotetta käytetään. Tässä esimerkissä paikallinen yhtiö on *USMF*.

Koska **Tuotteen hyväksyntä** -kentän asetukseksi on määritetty *Manuaalinen* *USMF*-yhtiön **Suunnittelun muutostenhallinnan parametrit** -sivulla, tuotteet on hyväksyttävä manuaalisesti, ennen kuin ne vapautetaan kyseiseen yhtiöön. Ne on siis tarkistettava ja hyväksyttävä, ennen kuin niistä tulee vapautettuja tuotteita.

Tuote arvioidaan ja vapautetaan *USMF*-yhtiöön seuraavasti:

1. Määritä yritykseksi *USMF*. (Käytä siirtymispalkin oikealla puolella olevaa yhtiövalitsinta.)
1. Valitse **Suunnittelun muutostenhallinta &gt; Yleinen &gt; Tuotevapautukset &gt; Avoimet tuotevapautukset**.

    **Avoimet tuotevapautukset** -sivulla on tuote *Z0001*, jonka tila on *Odottaa hyväksyntää*.

    ![Avaa tuotevapautukset.](media/open-product-releases.png "Avaa tuotevapautukset")

1. Avaa **Tuotteen vapautustiedot** -sivu valitsemalla arvo **Tuotenumero**-sarakkeessa. Ota seuraavat seikat huomioon:

    - **Yleinen**-pikavälilehdessä on tietoja tuotevapautuksesta, kuten vapauttava yhtiö (*DEMF* tässä esimerkissä), vapauttava toimipaikka (*1*) ja vastaanottava toimipaikka (*1*). Koska vastaanottavaa paikkaa ei määritetty ohjatussa **Vapauta tuotteet** -toiminnossa, vapauttavan toimipaikan arvo kopioidaan vastaanottavaan toimipaikkaan.
    - **Vapauta tiedot** -pikavälilehdessä on tietoja tuotteesta ja vapautetusta versiosta. Täällä voi muokata asetuksia, kuten voimassaolopäivämääriä.
    - **Reitti**-pikavälilehdessä on tuotteen reitti. Tässä esimerkissä reittejä ei kuitenkaan vapautettu.

    ![Tuotejulkaisun tiedot.](media/product-release-details-2.png "Tuotejulkaisun tiedot")

1. Kun tiedot on tarkistettu, olet valmis hyväksymään tuotteen ja siten myös vapauttamaan sen *USMF*-yhtiössä. Valitse toimintoruudussa **Toiminnot &gt; Hyväksy**
1. Tuote on nyt vapautettu *USMF*-yhtiössä. Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**. Nimikkeen *Z0001* pitäisi olla näkyvissä.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Tuotteen käyttäminen paikallisen yhtiön tapahtumissa

*USMF*-yhtiön päätietojen vastaava haluaa varmistaa, että tuotteen tila on *Prototyyppi*, sillä näin voidaan varmistaa, että käyttäjiä varoitetaan, jos he lisäävät sen vahingossa käyttämiinsä prosesseihin.

1. Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.
1. Avaa tuotteen *Z0001* tietosivu valitsemalla se. (Tuotteen voi etsiä suodattamalla.)
1. Valitse toimintoruudun **Suunnittele**-välilehden **Suunnittelun muutostenhallinta** -ryhmässä **Suunnitteluversiot**.
1. Valitse **Suunnitteluversiot**-sivulla versionumero *V-01*, jolloin sen tietosivu avautuu.
1. Valitse sitten toimintoruudun **Tuote**-välilehden **Elinkaaren tila** -ryhmässä **Vaihda elinkaaren tila**.
1. Määritä avattavassa **Vaihda elinkaaren tila** -valintaikkunassa **Tila**-kentän asetukseksi *Prototyyppi* ja valitse sitten **OK**.

    ![Elinkaaren tilan muuttaminen.](media/change-lifecycle-state.png "Elinkaaren tilan muuttaminen")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Suunnittelutuotteen lisääminen myyntitilaukseen

Tuote voidaan nyt myydä asiakkaalle. Tuote lisätään myyntitilaukseen seuraavasti:

1. Valitse **Myynti ja markkinointi &gt; Myyntitilaukset &gt; Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentän asetukseksi *US-0002* ja valitse sitten **OK**.
1. Uusi myyntitilaus avataan. Lisää **Myyntitilausrivit**-pikavälilehdessä rivi ja määritä sen **Nimiketunnus**-kentän asetukseksi *Z000*.
1. Valitse toimintoruudussa **Tallenna**.

    Avautuva varoitussanoma ilmoittaa, että nimikkeen tila on *Prototyyppi*. Koska sanoma on kuitenkin vain varoitus, myyntitilaus luodaan siitä huolimatta.

    ![Suunnittelutuotteen myyntitilaus.](media/sales-order-eng-product.png "Suunnittelutuotteen myyntitilaus")

## <a name="request-changes-in-the-engineering-product"></a>Muutosten pyytäminen suunnittelutuotteessa

Tuote lähetettiin asiakkaalle mutta asiakas ei ollut siihen täysin tyytyväinen. Asiakkaan antama palaute sisältää parannusehdotuksia. Kun asiakas keskustelee myyjän kanssa puhelimessa, myyjä voi pyytää asiakkaan kuvaamia muutoksia.

1. Valitse **Myynti ja markkinointi &gt; Myyntitilaukset &gt; Kaikki myyntitilaukset**.
1. Etsi ja avaa edellisessä harjoituksessa luotu myyntitilaus.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Suunnittelun muutostenhallinta &gt; Uusi suunnittelun muutospyyntö**.

    ![Suunnittelun muutospyynnön luominen myyntitilauksesta.](media/sales-order-eng-change-request.png "Suunnittelun muutospyynnön luominen myyntitilauksesta")

1. Täytä suunnittelun muutospyyntö asiakkaan palautteen perusteella. Määritä tässä esimerkissä seuraavat arvot:

    - **Muutospyyntö:** *555*
    - **Otsikko:** *Z0001 – asiakkaan muutos*
    - **Prioriteetti:** *alhainen*
    - **Luokka:** muutosmääritys
    - **Vakavuusaste:** *Keskitaso*

1. Lisää huomautus ruudukkoon valitsemalla **Tiedot**-pikavälilehdessä **Uusi &gt; Huomautus**.
1. Ilmaise uuden huomautuksen **Kuvaus**-kentässä, että nimike *D0003* on poistettava tuoterakenteesta. Jos huomautukseen on lisättävä muita tietoja, tekstiä voi kirjoittaa **Huomautukset**-kenttään.

    ![Suunnittelun muutospyyntö.](media/eng-change-request.png "Suunnittelun muutospyyntö")

1. Valitse toimintoruudussa **Tallenna**.
1. Huomaa, että nimi on lisätty automaattisesti **Tuotteet**-pikavälilehteen ja että suunnittelun muutospyynnön lähde (myyntitilaus) on lisätty **Lähde**-pikavälilehteen.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Muutosten tekeminen tuotteeseen suunnittelun muutostilauksen avulla

Myyjä tietää, että tuote on tärkeä ja että oli suunniteltu nimenomaisesti asiakkaalle. Tämän vuoksi myyjä ilmoittaa *DEMF*-yhtiön suunnittelijalle muutospyynnöstä. Tällä tavoin suunnittelija voi nopeuttaa prosessia.

Suunnittelija tarkistaa nyt asiakkaan pyynnön ja luo tuotteelle muutostilauksen.

1. Koska suunnittelija työskentelee *DEMF*-yhtiössä, määritä yritykseksi *DEMF*. (Käytä siirtymispalkin oikealla puolella olevaa yhtiövalitsinta.)
1. Valitse **Suunnittelun muutostenhallinta &gt; Yleinen &gt; Suunnittelun muutospyynnöt**.
1. Avaa muutospyyntö: *555*.
1. Tarkista tiedot ja hyväksy sitten muutos. Valitse toimintoruudun **Muutospyyntö**-välilehden **Muutoksen tila** -ryhmässä **Hyväksy**.
1. Valitse **Suunnittelun muutostenhallinta &gt; Yleinen &gt; Suunnittelun muutostilaukset**.
1. Luo muutostilaus valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:

    - **Muutostilaus:** *555*
    - **Otsikko:** *Z0001 – asiakkaan muutos*
    - **Luokka:** *Asiakkaan muutos*
    - **Prioriteetti:** *Alhainen*
    - **Vakavuusaste:** *Keskitaso*

1. Lisää rivi ruudukkoon valitsemalla **Tuotteet joihin vaikuttaa**-pikavälilehdessä **Uusi &gt; Lisää aiemmin luotu tuote** ja määritä sitten sille seuraavat arvot:

    - **Tuote:** *Z0001*
    - **Vaikutuksen kohteet:** *Uusi versio*

    ![Suunnittelun muutostilauksen luominen.](media/eng-change-order.png "Suunnittelun muutostilauksen luominen")

1. Huomaa, että koska **Vaikutuksen kohteet** -kentän asetuksena on *Uusi versio*, **Tuotteen tiedot** -pikavälilehden **Tiedot**-välilehden **Uusi versio** -kentässä näkyy tuleva uusi versionumero (tässä esimerkissä *V-02*).

    ![Suunnittelun muutostilauksen tuotetiedot.](media/eng-change-order-product-details.png "Suunnittelun muutostilauksen tuotetiedot")

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Tuotteen tiedot** -pikavälilehden **Tuoterakenne**-välilehdessä **Rivit**. Tuotteen *Z0001* version *V-01* tuoterakenne avautuu.

    ![Suunnittelutuotteen tuoterakennerivit.](media/eng-product-bom-lines.png "Suunnittelutuotteen tuoterakennerivit")

1. Valitse nimiketunnuksen *D0003* rivi ja valitse sitten toimintoruudussa **Poista**. Tämän rivin **Muuta tyyppi** -kentän arvo muuttuu arvoksi *Poistettu*.
1. Valitse toimintoruudussa **Tallenna**.

    ![Muokatut suunnittelutuotteen tuoterakennerivit.](media/eng-product-bom-lines-modified.png "Muokatut suunnittelutuotteen tuoterakennerivit")

1. Palaa **Suunnittelun muutostilaus** -sivun **Tuoterakennerivi**-sivulle.
1. Huomaa, että **Tuotteen tiedot** -pikavälilehden **Tuoterakenne**-välilehden tuoterakenteen *Z0001* **Muuta tyyppi** -kentän arvo on nyt *Muutettu*.

    ![Muutetun tuoterakenteen sisältävä suunnittelun muutostilaus.](media/eng-change-order-changed-bom.png "Muutetun tuoterakenteen sisältävä suunnittelun muutostilaus")

    Tilaus on nyt hyväksyttävä, jonka jälkeen muutokset voidaan käsitellä. Kun muutokset on käsitelty, tuotteet päivitetään suunnittelun muutostilaukseen sisältyneillä muutoksilla. Tässä esimerkissä hyväksyjäksi on määritetty henkilö, joka luo suunnittelun muutostilauksen.

1. Valitse toimintoruudun **Muutostilaus**-välilehden **Muutoksen tila** -ryhmässä **Hyväksy**.
1. Päivitä tuotteen tiedot valitsemalla **Käsittele**.

## <a name="release-the-changed-product"></a>Muutetun tuotteen vapauttaminen

Tuote voidaan nyt vapauttaa uudelleen *USMF*-yhtiölle ja lähettää sitten asiakkaalle. Tuote voidaan vapauttaa suoraan suunnittelun muutostilauksesta seuraavasti:

1. Avaa edellisessä harjoituksessa luotu suunnittelun muutostilaus, jos se ei ole vielä avoinna.
1. Valitse toimintoruudun **Muutostilaus**-välilehden **Tuotevapautukset** -ryhmässä **Haku**.
1. Hakutulokset osoittavat, mihin yhtiöihin tuotteet, joita muutos koskee, on vapautettu. Sulje hakutulokset.
1. Valitse toimintoruudun **Muutostilaus**-välilehden **Tuotevapautukset**-ryhmässä **Näytä**. **Vapautukset**-valintaikkuna avautuu, edellisen haun tuloksia tarkastella siellä.
1. Valitse kukin yhtiö, johon tuotteet halutaan vapauttaa.
1. Valitse **Vapautukset**-valintaikkuna valitsemalla **OK** ja palaa muutostilaukseen.
1. Vapauta kyseiset tuotteet valittuihin yhtiöihin valitsemalla toimintoruudun **Muutostilaus**-välilehden **Tuotevapautukset**-ryhmässä **Käsittele**. Aloita vapautusprosessi valitsemalla vaihtoehtoisesti **Vapauta tuotteen rakenne**.

## <a name="complete-the-change-order"></a>Muutostilauksen viimeistely

Valitse toimintoruudusta **Valmis** merkitäksesi muutostilauksen valmiiksi, mikä tarkoittaa, ettei muita toimenpiteitä ole jäljellä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
