---
title: Sijaintidirektiivien käyttäminen
description: Tässä artikkelissa käsitellään sijaintidirektiivien käyttämistä. Sijaintidirektiivit ovat käyttäjän määrittämiä sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa.
author: Mirzaab
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ef8ec0732cd3bd50bca8d334c43d0354e9e3316
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689663"
---
# <a name="work-with-location-directives"></a>Sijaintidirektiivien käyttäminen

[!include [banner](../includes/banner.md)]

Sijaintidirektiivit ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään ja minne kerätyt nimikkeet sijoitetaan. Sijaintidirektiiveissä on otsikko ja liitettyjä rivejä. Niitä luodaan tietyille *työtilaustyypeille*.

> [!NOTE]
> Tämä artikkeli koskee **Varastonhallinta**-moduulin ominaisuuksia. Se ei koske [Inventoinnin- ja varastonhallinta](../inventory/inventory-home-page.md) -moduulin ominaisuuksia.

Voit käyttää sijaintidirektiiviä seuraavien tehtävien suorittamiseen:

- Aseta pois saapuvat nimikkeet.
- Kerää ja vaiheista lähteväin tapahtumien nimikkeet.
- Valitse ja sijoita tuotannon raaka-aineet.
- Täydennyssijainnit.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit luoda sijaintidirektiivin, sinun on varmistettava, että edellytykset ovat olemassa, noudattamalla näitä ohjeita.

1. Varmista, että tarvittava käyttöoikeusavain on otettu käyttöön. Valitse **Järjestelmän hallinta \> Määritys \> Käyttöoikeuden konfiguraatio**, laajenna **Kauppa**-käyttöoikeusavain ja valitse sitten **Varaston ja kuljetusten hallinta** -määritysavain. Huomaa, että tähän vaiheeseen tarvitaan järjestelmänvalvojan käyttöoikeudet.
1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
1. Luo varasto.
1. Valitse **Varasto**-pikavälilehdellä **Käytä varastonhallintaprosesseja** -vaihtoehdon arvoksi *Kyllä*.
1. Luo toimipaikat, toimipaikkojen tyypit, toimipaikkojen profiilit ja toimipaikkojen muodot. Lisätietoja on kohdassa [Sijaintien määrittäminen VHJ-yhteensopivassa varastossa](./tasks/configure-locations-wms-enabled-warehouse.md).
1. Luo toimipaikkoja, alueita ja vyöhykeryhmiä. Lisätietoja on kohdassa [Varaston määrittäminen](../../commerce/channels-setup-warehouse.md) ja [Sijaintien määrittäminen VHJ-yhteensopivassa varastossa](./tasks/configure-locations-wms-enabled-warehouse.md).

## <a name="turn-the-location-directive-scopes-feature-on-or-off"></a><a name="scopes-feature"></a>Sijaintidirektiivin vaikutusalueiden toiminnon käyttöönotto tai käytöstäpoisto

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

*Sijaintidirektiivin vaikutusalueet* -ominaisuuden avulla voit suunnitella sijaintidirektiivejä vapaasti. Se myös auttaa vähentämään turhia määrityksiä. Se lisää **Vaikutusalue**-vaihtoehdon, joka korvaa edellisen **Useita varastointiyksiköitä**-vaihtoehdon. **Useita varastointiyksiköitä** -vaihtoehdon arvoksi voi määrittää vain *Kyllä* tai *Ei*. **Vaikutusalue**-vaihtoehto taas määrittää nämä kaksi asetusta (*Yksi nimike*- ja *Useita nimikkeitä* -arvojen avulla) sekä kaksi muuta (*Yksi nimike tai tilaus* ja *Kaikki*-arvojen avulla). Lisätietoja näistä asetuksista on kohdassa [Sijaintidirektiivit-pikavälilehti](#location-directives-tab).

Kun tämä on käytössä, **Vaikutusalue**-vaihtoehto korvaa **Useita varastointiyksiköitä** -vaihtoehdon. Se on täysin yhteensopiva olemassa olevien määritysten kanssa.

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat tarkistaa toiminnon tilan ja ottaa sen käyttöön tai poistaa sen käytöstä [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetusten avulla. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Sijaintidirektiivin vaikutusalueet*

## <a name="work-order-types-for-location-directives"></a>Sijaintidirektiivien työtilaustyypit

Monet sijaintidirektiiveille määritettävät kentät ovat samoja kaikissa työtilaustyypeissä. Muut kentät ovat kuitenkin työtilaustyyppikohtaisia.

![Sijaintidirektiivien työtilaustyypit.](media/Location_Directives_Work_Order_Types.png "Sijaintidirektiivien työtilaustyypit")

> [!NOTE]
> Kaksi työtilaustyyppiä, *Peruutettu työ* ja *Inventointi*, ovat vain järjestelmän käytössä. Sijaintidirektiivejä ei voi luoda näille työtilaustyypeille.

Seuraavissa aliosissa käsitellään yhteisiä ja työtilaustyyppikohtaisia kenttiä, jotka ovat käytettävissä sijaintidirektiiviä määritettäessä.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Kaikkien työtilaustyyppien yhteiset kentät

Seuraavassa taulukossa on kaikille työtilaustyypeille yhteiset kentät.

| Pikavälilehti | Kenttä |
|---|---|
| Sijaintidirektiivit | Työtyyppi |
| Sijaintidirektiivit | Toimipaikka |
| Sijaintidirektiivit | Varasto |
| Sijaintidirektiivit | Direktiivikoodi |
| Sijaintidirektiivit | Vaikutusalue *tai* Useita varastointiyksiköitä |
| Rivit | Järjestysnumero |
| Rivit | Määrästä |
| Rivit | Määrälle |
| Rivejä | Yksikkö |
| Rivejä | Etsi määrä |
| Rivejä | Rajoita yksikön mukaan |
| Rivejä | Kokoa yksikköön |
| Rivejä | Etsi pakkausmäärä |
| Rivejä | Salli jakaminen |
| Sijaintidirektiivin toiminnot | Järjestysnumero |
| Sijaintidirektiivin toiminnot | Nimi |
| Sijaintidirektiivin toiminnot | Kiinteän sijainnin käyttö |
| Sijaintidirektiivin toiminnot | Salli negatiivinen varasto |
| Sijaintidirektiivin toiminnot | Erä käytössä |
| Sijaintidirektiivin toiminnot | Strategia |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Työtilaustyyppikohtaiset kentät

Seuraavassa taulukossa on työtilaustyyppikohtaiset kentät.

| Pikavälilehti | Kenttä | Työtilaustyyppi |
|---|---|---|
| Sijaintidirektiivit | Etsintäperuste | Ostotilaukset |
| Sijaintidirektiivit | Soveltuva käsittelykoodi | Ostotilaukset |
| Sijaintidirektiivit | Käsittelykoodi | Ostotilaukset |
| Sijaintidirektiivit | Soveltuva käsittelykoodi | Valmiiden tuotteiden poispano |
| Sijaintidirektiivit | Käsittelykoodi | Valmiiden tuotteiden poispano |
| Sijaintidirektiivit | Soveltuva käsittelykoodi | Palautustilaukset |
| Sijaintidirektiivit | Käsittelykoodi | Palautustilaukset |
| Sijaintidirektiivit | Soveltuva käsittelykoodi | Kanban-poispano |
| Sijaintidirektiivit | Soveltuva käsittelykoodi | Kanban-keräily |
| Rivejä | Välittömän täydennyksen malli | Myyntitilaukset |
| Rivejä | Välittömän täydennyksen malli | Raaka-aineiden keräily |
| Rivejä | Välittömän täydennyksen malli | Siirtovarasto-otto |
| Rivejä | Välittömän täydennyksen malli | Kanban-keräily |

## <a name="open-the-location-directives-page"></a>Sijaintidirektiivisivun avaaminen

Avaa **Sijaintidirektiivit**-sivu valitsemalla **Varaston hallinta \> Määritys \> Sijaintidirektiivit**.

Tällä sivulla voi tarkastella, luoda ja muokata sijaintidirektiivejä toimintoruudun komennoilla. Tämä artikkelin muissa osissa on tietoja kaikkien sivulla olevien kenttien käyttämisestä.

## <a name="action-pane"></a>Toimintoruutu

**Sijaintidirektiivit**-sivun toimintoruudussa on painikkeita, joilla voi luoda, muokata ja poistaa direktiivejä (**Muokkaa**, **Uusi** ja **Poista**). Siinä on myös seuraavat painikkeet, joilla voi muokata sijaintidirektiivin käsittelyjärjestystä ja määrittää sijaintidirektiivin käytön ehdot määrittävän kyselyn:

- **Siirrä ylös** – Siirrä valittua sijaintidirektiiviä ylöspäin järjestyksessä. Voit esimerkiksi muuttaa sen järjestysnumeron 4:stä 3:ksi.
- **Siirrä alas** – Siirrä valittua sijaintidirektiiviä alaspäin järjestyksessä. Voit esimerkiksi muuttaa sen järjestysnumeron 4:stä 5:ksi.
- **Kopioi** – Avaa valintaikkuna, jossa voit luoda tarkan kopion nykyisestä sijaintidirektiivistä.
- **Muokkaa kyselyä** – Avaa valintaikkuna ja määritä ehdot, joiden mukaan valittu sijaintidirektiivi käsitellään. Voit esimerkiksi päättää käyttää sitä vain tietyssä varastossa.
- **Hyväksyntätestit** – Avaa sivu, jossa voit määrittää automaattiset testit määrittääksesi, miten sijaintidirektiivit toimivat erilaisissa aloitusolosuhteissa. Näin voit tarkistaa nopeasti direktiivit niiden luomisen ja ylläpitämisen yhteydessä. Lisätietoja on kohdassa [Sijaintidirektiivien testaaminen hyväksyntätestien avulla](location-directive-acceptance-tests.md).

## <a name="location-directives-header"></a>Sijaintidirektiivien otsikko

Sijaintidirektiivin otsikko sisältää seuraavat järjestysnumeron kentät ja sijaintidirektiivin kuvaava nimi:

- **Järjestysnumero** – Tämä kenttä ilmaisee järjestyksen, jossa järjestelmä yrittää käyttää kutakin valitun työtilaustyypin sijaintidirektiiviä. Pienet numerot käytetään ensin. Järjestystä voi muuttaa toimintoruudun **Siirrä ylös**- ja **Siirrä alas** -painikkeilla.
- **Nimi** – Anna sijaintidirektiiville kuvaava nimi. Tämä nimi auttaa tunnistamaan direktiivin yleisen tarkoituksen. Anna nimeksi esimerkiksi *Myyntitilauksen keräily varastossa 24*.

## <a name="location-directives-fasttab"></a><a name="location-directives-tab"></a>Sijaintidirektiivit-pikavälilehti

**Sijaintidirektiivit**-pikavälilehden kentät ovat työtilaustyyppikohtaisia, joka on valittu luetteloruudun **Työtilaustyyppi**-kentässä.

- **Työn tyyppi** – Valitse suoritettavan työn tyyppi. Käytettävissä olevat arvot määräytyvät sen varastotapahtuman tyypin mukaan, jonka valitsit **Työtilaustyyppi**-kentässä. Valitse jokin seuraavista:

    - **Hyllytys** – Sijaintidirektiivi yrittää löytää parhaan sijainnin varastonimikkeiden hyllytykselle tai sijoittamiselle, kun varastonimike tulee järjestelmään vastaanoton, tuotannon tai varaston oikaisujen avulla. Sen avulla voidaan myös määrittää hyllytyksen väliaikaiseen sijaintiin tai lopulliseen lähetyssijaintiin lastausovella.
    - **Poiminta** – Sijaintidirektiivi yrittää löytää parhaat sijainnit, jotta varastoa voidaan varata fyysisesti (eli luoda työ). Keräilyvaihe voidaan suorittaa loppuun (eli keräilytyörivi voidaan sulkea), vaikka työ ei ole valmis. Käyttäjä voi suorittaa fyysisen keräyksen. Järjestelmässä tämä toimenpide on poimintavaihe. Käyttäjä voi sitten peruuttaa työn mobiililaitteella ja suorittaa työn loppuun myöhemmin. Työn otsikko kuitenkin ensin suljetaan, kun lopullinen Aseta-vaihe on valmis.

    > [!IMPORTANT]
    > Muut **Työtyyppi**-kentän arvot eivät koske sijaintidirektiivejä. Ne ovat näkyvissä vain siksi, että kenttää ei ole suodatettu valittua työtilaustyyppiä vastaavaksi.

- **Toimipaikka** – tämä on pakollinen kenttä, koska sijaintidirektiivin on voitava määrittää toimipaikka ja varasto, jossa sitä voi käyttää.
- **Varasto** – tämä on pakollinen kenttä, koska sijaintidirektiivin on voitava määrittää toimipaikka ja varasto, jossa sitä voi käyttää.
- **Direktiivikoodi** – Valitse liitettävän työmallin tai täydennysmallin direktiivikoodi. Voit luoda **Direktiivikoodi**-sivulla uusia koodeja, joilla työmallit tai täydennysmallit voidaan yhdistää sijaintidirektiiveihin. Direktiivikoodeja voidaan käyttää myös linkin luomiseen työmallin rivin ja sijaintidirektiivin välille (kuten lastausovi tai väliaikainen sijainti).

    > [!TIP]
    > Jos direktiivikoodi on määritetty, järjestelmä ei etsi sijaintidirektiivejä järjestysnumeron perustella, kun työ on luotava. Sen sijaan haku tehdään direktiivikoodin perusteella. Tällä tavoin voit tarkentaa tietyssä työmallin vaiheessa käytettävää sijaintidirektiiviä. Kyse voi olla esimerkiksi materiaalien valmisteluvaihe.

- **Vaikutusalue** – Tämän vaihtoehdon avulla voit määrittää skenaariot, joissa sijaintidirektiivejä käytetään. Tämä vaihtoehto korvaa **Useita varastointiyksiköitä** -vaihtoehdon. Se on käytettävissä vain, jos *Sijaintidirektiivin vaikutusalueet* -ominaisuus on otettu käyttöön järjestelmässä. (Lisätietoja on kohdassa [Sijaintidirektiivin vaikutusalueiden toiminnon käyttöönotto tai käytöstäpoisto](#scopes-feature).)

    | Vaikutusalueasetus | Yksi tilaus ja yksi nimike | Useita tilauksia ja sama nimike | Yksi tilaus ja useita nimikkeitä | Useita tilauksia ja useita nimikkeitä |
    |---|---|---|---|---|
    | Yksittäinen nimike | Kyllä | Kyllä | En | En |
    | Useita nimikkeitä | En | En | Kyllä | Kyllä |
    | Yksittäinen nimike tai tilaus | Kyllä | Kyllä | Kyllä | En |
    | Kaikki | Kyllä | Kyllä | Kyllä | Kyllä |

    Seuraavassa taulukossa kuvataan, milloin vaikutusalue on käytettävissä ja onko **Muokkaa kyselyä** -toiminto käytettävissä.

    | Vaikutusalue | Tuettu työtyyppi | Tuetut työtilausten tyypit | Muokkauskyselyn salliminen |
    |---|---|---|---|
    | Yksittäinen nimike | Kaikki | Kaikki | Kyllä |
    | Useita nimikkeitä | Kaikki | Kaikki | En |
    | Yksittäinen nimike tai tilaus | Hyllytykset | Rinnakkaistuotteen ja sivutuotteen hyllytys, valmiiden tavaroiden hyllytys, kanban-hyllytys, ostotilaukset, laatutilaukset, täydennys, palautustilaukset, myyntitilaukset, siirto-otto ja siirron vastaanotto | Kyllä |
    | Kaikki | Hyllytykset | Kaikki | En |

    > [!NOTE]
    > - Jos tehdään useiden nimikkeiden ja yhden nimikkeen hyllytyksiä, varmista, että olemassa on molemmat skenaariot kattavat sijaintidirektiivit. Saatat esimerkiksi haluta määrittää vähintään yhden *Yksittäinen nimike tai tilaus* -sijaintidirektiivin kattamaan skenaariot, joissa vaaditaan hienosäätöä (kuten kyselyn muokkauksia) ja tämän jälkeen vähintään yhden *Kaikki*-sijaintidirektiivit kattamaan jäljellä olevat skenaariot.
    > - Vaikka *Yksi nimike*- ja *Useita nimikkeitä* -vaikutusalueita voi käyttää hyllytyksissä, tämä lähestymistapa yleensä johtaa tarpeettomiin määrityksiin. Harkitse *Yksi nimike tai tilaus*- ja *Kaikki*-vaikutusalueiden käyttämistä sen sijaan, koska tämä lähestymistapa tuottaa siistin asetuksen.

- **Useita varastointiyksiköitä** – Tämän vaihtoehdon avulla voit määrittää skenaarion, jossa sijaintidirektiivejä käytetään. Tämä asetus korvataan **vaikutusalueella**, jos *Sijaintidirektiivien vaikutusalueet* -ominaisuus on otettu käyttöön järjestelmässä. (Lisätietoja on kohdassa [Sijaintidirektiivin vaikutusalueiden toiminnon käyttöönotto tai käytöstäpoisto](#scopes-feature).) Määritä tämän vaihtoehdon arvoksi *Kyllä*, jos haluat ottaa käyttöön useat varastointiyksiköt tässä sijainnissa. Useita varastointiyksiköitä voidaan ottaa käyttöön esimerkiksi lastausovisijainnissa. Jos otat useat varastointiyksiköt käyttöön, hyllytyssijainti määritetään odotetusti työssä. Hyllytyssijainti voi kuitenkin käsitellä vain moninimikkeisen hyllytyksen (jos työ sisältää useita varastointiyksiköitä, joita on kerättävä ja hyllytettävä). Se ei voi käsitellä yhden varastointiyksikön hyllytystä. Jos asetuksena on *Ei*, hyllytyssijainti määritetään vain, jos hyllytyksessä on vain yhdenlaista varastointiyksikköä.

    > [!IMPORTANT]
    > Sekä moninimikkeisen hyllytyksen että yhden varastointiyksikön hyllytyksen käyttöönottaminen edellyttää kahden sellaisen rivin määrittämistä, jolla on sama rakenne ja samat määritykset. Toisen rivin **Useita varastointiyksiköitä** -asetukseksi on valittava *Kyllä* ja toisen *Ei*. Tämän vuoksi hyllytystoimintoja on oltava kaksi samanlaista sijaintidirektiiviä, vaikka työn tunnuksessa ei tehdä erottaa yhtä varastointiyksikköä ja useita varastointiyksiköitä. Jos molempia sijaintidirektiivejä ei määritetä, käytetystä sijaintidirektiivistä tulee usein esille odottamattomia liiketoimintaprosessisijainteja. Sijaintidirektiiveillä, joiden **työtyyppi** on *keräily*, on oltava samanlaisen määritys, jos käsiteltävissä tilauksissa on useita varastointiyksiköitä.

    Käytä **Useita varastointiyksiköitä** -vaihtoehtoa työriveillä, joilla käsitellään useita nimiketunnuksia. (Nimiketunnus on tyhjä työn tiedoissa, ja sen arvona näytetään **Useita** varastonhallinnan mobiilisovelluksen käsittelysivuilla.)

    Tyypillisessä skenaariossa työmalli määritetään siten, että siinä on useita keräily/hyllytys-pareja Tässä tapauksessa kannattaa ehkä hakea tietty valmistelusijainti käytettäväksi riveillä, joiden **Työntyyppi** on *Hyllytys*.

    > [!NOTE]
    > Jos **Useita varastointiyksiköitä** -asetuksena *Kyllä*, et voi valita **Muokkaa kyselyä** toimintoruudussa, sillä kysely ei voi arvioida nimiketasolla, onko nimikkeitä useita. Toivotun sijaintidirektiivin valinta voidaan varmistaa käyttämällä **Direktiivikoodi**-kenttää, ja tämä kenttä ohjaa niiden hyllytysriveihin liittyvien sijaintidirektiivin valintaa, joissa direktiivikoodi on määritetty työmalliin.

    Jos et käytä aina joko yhden nimikkeen tai yhdistelmänimikkeen toimintoja, kahden sijaintidirektiivin määrittäminen *Hyllytys*-työtyypille on tärkeää. Toisessa näistä **Useita varastointiyksiköitä** -asetuksena on *Kyllä* ja toisessa asetuksena on *Ei*.

- **Käytettävä jakelukoodi** – Määritä, onko sijaintidirektiivin käsittelykoodin vastattava nimikettä vastaanotettaessa käytettävää käsittelykoodia vai voiko sijaintidirektiivin valita minkä tahansa käsittelykoodin perusteella. Jos valitset *Tarkka vastine* ja **Käsittelykoodi**-kenttä on tyhjä, vain käsittelykoodit otetaan huomioon tässä sijaintidirektiivissä.

    > [!NOTE]
    > Tämä kenttä on käytettävissä vain valituissa työtilaustyypeissä, joissa sallitaan täydennys. Täydellinen on aiemmin tässä artikkelissa kohdassa [Työtilaustyyppikohtaiset kentät](#fields-specific-types).

- **Etsintäperuste** – Määritä, onko hyllytysmäärä koko rekisterikilven määrä vai onko se nimikekohtainen. Tämän kentän avulla voi varmistaa, että koko rekisterikilven sisältö hyllytetään yhteen sijaintiin ja että järjestelmä ei ehdota sisällön jakamista useisiin sijainteihin seuraavissa prosesseissa: **ASN** (rekisterikilven vastaanotto), **Yhdistetyn rekisterikilven vastaanotto** ja **Klusteri**-vastaanotto. (**Klusteri**-vastaanottoprosessi edellyttää, että [klusterihyllytystoiminto](putaway-clusters.md) on otettu käyttöön.) Sijaintidirektiivikyselyn, rivien ja sijaintidirektiivitoimintojen toiminta vaihtelee valitun arvon mukaan. **Rivit**-pikavälilehteä käytetään vain, kun **etsintäperusteena** on *nimike*.

    > [!NOTE]
    > Tämä kenttä on käytettävissä vain valituissa työtilaustyypeissä, joissa sallitaan täydennys. Täydellinen on kohdassa [Työtilaustyyppikohtaiset kentät](#fields-specific-types).

- **Käsittelykoodi** – Tätä kenttää käytetään sijaintidirektiiveissä, joiden työtilaustyyppi on *Ostotilaukset*, *Valmiiden tuotteiden hyllytys* tai *Palautustilaukset* ja työtilaus on *Hyllytys*. Ohjaa sen avulla työnkulku käyttämään tiettyä sijaintidirektiiviä työntekijän varastonhallinnan mobiilisovelluksessa valitseman käsittelykoodin mukaan. Voit esimerkiksi ohjata palautetut tuotteet tarkastussijaintiin, ennen kuin palautetaan varastoon. Käsittelykoodi voidaan linkittää varaston tilaan. Tällä tavoin sitä voidaan käyttää muuttamaan varaston tila vastaanottoprosessin osana. Esimerkiksi käsittelykoodi *Laadunvalvonta* määrittä varastoon *Laadunvalvonta*-tilaan. Voit sitten käyttää erillistä sijaintidirektiiviä siirtämän kyseisen varaston karanteenisijaintiin.

    > [!NOTE]
    > Tämä kenttä on käytettävissä vain valituissa työtilaustyypeissä, joissa sallitaan täydennys. Täydellinen on kohdassa [Työtilaustyyppikohtaiset kentät](#fields-specific-types).

## <a name="lines-fasttab"></a>Rivit-pikavälilehti

Muodosta **Rivit**-välilehdessä ehdot **Sijaintidirektiivitoiminnot**-pikavälilehdessä määritettyjen liittyvien toimintojen käyttämiseen. Voit määrittää kullekin riville vähimmäismäärän ja enimmäismäärän, joissa toimintoja käytetään. Voit myös määrittää, että toimintoja käytetään tietyssä varastoyksikössä.

- **Järjestysnumero** – Anna järjestys, jossa kukin valitun työtyypin sijaintidirektiivin rivi on käsiteltävä. Voit järjestystä tarpeen mukaan työkalurivin **Siirrä ylös**- ja **Siirrä alas** -painikkeilla.
- **Määrästä** – Määritä määräalue, josta rivi aloittaa käyttämisen. Määritä määrä mittayksikössä, joka on valittu **Yksikkö**-kentässä.
- **Määrälle** – Määritä määräalue, jossa rivi lopettaa käyttämisen. Määritä määrä mittayksikössä, joka on valittu **Yksikkö**-kentässä.
- **Yksikkö** – Valitse nimikkeiden mittayksikkö. Voit määritellä vähimmäis- ja enimmäismäärät, joihin direktiiviä tulisi soveltaa ja voit määrittää, että direktiivi koskee määrättyä varastoyksikköä. **Yksikkö**-kenttää käytetään *vain* määrän arviointiin. Järjestelmä määrittää, käytetäänkö sijaintidirektiivin riviä lainkaan käyttämällä määrää siinä yksikössä, jossa kyseinen rivi määritettiin. Aina kun direktiivisijainnin riville saavutaan, järjestelmä yrittää muuntaa kysynnän yksikön rivillä määritetyksi yksiköksi. Jos mittayksikkömuunnosta ei ole, järjestelmä siirtyy seuraavalle riville.
- **Etsi määrä** – Tätä kenttää käytetään vain yritettäessä hyllyttää tai etsiä nimikkeitä varastossa. (Tämän vuoksi sitä käytetään vain, kun **Työtyyppi**-kentän asetuksena on *Hyllytys*.) Määritä valitsemalla jokin seuraavista arvoista määrä, jolla arvioidaan, onko määrä **Määrästä**- ja **Määrälle**-arvojen alueella:

    - **Rekisterikilven määrä** – käytä vastaanotettavassa rekisterikilvessä olevaa määrää.
    - **Määrä, jolle määrätty yksikkö** – Käytä määrää, jota käytetään tapahtuman aikana. Esimerkki: varastossa vastaanotettava määrä on 1 000 ja se eritellään 10 rekisterikilveksi, jossa kussakin on määränä 100. Tässä tapauksessa määränä voi olla käytössä 1 000 rekisterikilven määrän, 100, sijasta.
    - **Jäljellä oleva määrä** – käytä määrää, joka on vastaanotettava käsiteltävänä olevalta ostotilausriviltä.
    - **Odotettu määrä** – käytä ostotilausrivin kokonaismäärää riippumatta siitä, mitä on jo vastaanotettu.

- **Rajoita yksikön mukaan** – Tämän valintaruudun avulla sijaintidirektiivin rivistä voidaan tehdä mittayksikkökohtainen tai useita mittayksiköitä koskeva. Valitse se, jos haluat rajoittaa mittayksiköitä, joita pidetään sijaintidirektiivin rivien kelvollisena valintaperusteena. Tätä toimintoa voi käyttää vain sijaintidirektiiveissä, joissa **Työn tyyppi** -kentän asetuksena on *Keräily*.

    Esimerkiksi määriä varattaessa varataan kuormalavoja vain tietyssä sijaintijoukossa. Tässä tapauksessa rivit rajoittavat tämän järjestyksen kuormalavoille siten, että mitään kuormalavaa alittavaa määrää ei valita sijaintidirektiiviin.

    Huomaa, että **Rajoita yksiköittäin** -valintaruutu ei ohjaa työriveillä käytössä olevaan yksikköön tai yksiköihin. Yksikkörajoitus koskee vain yksiköitä, jotka on asetettu saataville yksikkösarjaryhmän kautta. Esimerkiksi nimike liitetään yksikkösarjaryhmään, joka sisältää sekä *kuormalava*- että *kpl*-yksikön. Määritetyssä mittayksikössä 1 kuormalava = 100 kpl ja sijaintidirektiivissä käytetään **Rajoita yksikön mukaan** -toimintoa vain kuormalavoille. Lisäksi on määritetty työmalli, joka rajoittaa työotsikon luomisen 50 kappaleeseen. Tässä tapauksessa luodaan 50 kappaleen työrivit. Voit määrittää rajoituksen mittayksikön seuraavasti:

    1. Valitse **Rivit**-pikavälilehden työkalurivillä **Rajoita yksikön mukaan**. (Tämä painike on käytettävissä vain, kun valitset ensin rivin **Rajoita yksiköittäin** -valintaruudun ja sitten **Tallenna**.)
    1. Valitse **Rajoita yksikön mukaan** -sivun **Yksikkö**-kentässä mittayksikkö, jolla keräily- ja hyllytysprosesseja rajoitetaan.

- **Kokoa yksikköön** – Tätä kenttää käytetään **Rajoita yksikön mukaan** -valintaruudun kanssa. Jos sijaintidirektiivin rivillä valitaan **Rajoita yksikön mukaan** ja **Kokoa yksikköön**, direktiivistä luotu työ raaka-aineen keräämistä varten olisi koottava käsittely-yksikön kerrannaiseen, joka on määritetty **Rajoita yksikön mukaan** -sivulla.

    > [!NOTE]
    > **Kokoa yksikköön** -määritys toimii vain, jos työtilauksen tyyppi on *Raaka-aineiden keräily*, ja vain sijaintidirektiiveissä, joissa **Työn tyyppi** -asetuksena on *Keräily*.

- **Etsi pakkausmäärä** – Jos määrität pakkausmäärän myynti-, siirto- tai tuotantotilauksessa, tällä valintaruudulla voi rajoittaa järjestelmän valitsemaan vain sijainnit, joissa on vähintään kyseinen pakkausmäärä.

    > [!NOTE]
    > Tätä toimintoa voi käyttää vain *Keräily*-tyypin sijaintidirektiivien kanssa.

- **Salli jakaminen** – määrittää, voiko sijaintidirektiivi jakaa vastaanotettavan tai varattavan määrän useisiin varastosijainteihin tai onko koko määrän sijaittava yhdessä sijainnissa vai onko se varattava yhdestä sijainnista työn luontia varten.
- **Välittömän täydennyksen malli** – Käytä tätä kenttää muodostamaan yhteys täydennysmalliin, jotta täydennys voidaan aloittaa välittömästi, jos kohteita ei kohdisteta. Jos jätät kentän tyhjäksi, kohteiden täydennystä ei aloiteta, ennen kuin sijaintidirektiivin kaikki rivit on käsitelty.

    > [!NOTE]
    > Tämä kenttä on käytettävissä vain valituissa työtilaustyypeissä, joissa sallitaan täydennys. Täydellinen on kohdassa [Työtilaustyyppikohtaiset kentät](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Sijaintidirektiivitoiminnot-pikavälilehti

Voit määrittää useita sijaintidirektiivin toimintoja kullekin riville. Jälleen kerran järjestysnumeroa käytetään määrittämään järjestys, jossa arvioidaan toimia. Voit määrittää tällä tasolla kyselyn määrittämään, miten paras varastosijainti löydetään. Voit myös käyttää esimääritettyjä **Strategia**-arvoja parhaan sijainnin etsimiseen.

- **Järjestysnumero** – Tässä kentässä näkyy, missä järjestyksessä valitun työtyypin toiminnot käsitellään. Järjestystä voi muuttaa työkalurivin **Siirrä ylös**- ja **Siirrä alas** -painikkeilla.
- **Nimi** – Anna sijaintidirektiivin toiminnon nimi. Varmista, että nimi ilmaisee selkeästi, mikä suoritettava toiminto on.
- **Kiinteän sijainnin käyttö** – määritä sijainnit, joita sijaintidirektiivin on harkittava. Valitse jokin seuraavista:

    - **Kiinteät ja ei-kiinteät sijainnit** – Sijaintidirektiivi harkitsee kaikkia sijainteja.
    - **Vain kiinteät sijainnit tuotteelle** – Sijaintidirektiivi harkitsee vain kiinteitä sijainteja tuotteille.
    - **Vain kiinteät sijainnit tuotevariantille** – Sijaintidirektiivi harkitsee vain kiinteitä sijainteja tuotevarianteille.

- **Salli negatiivinen varasto** – valitse tämä valintaruutu, jos haluat sallia sijaintidirektiiveissä negatiivisen varaston määritetyssä varastosijainnissa.
- **Erä käytössä** – Valitse tämä valintaruutu, jos haluat käyttää erästrategioita nimikkeille, joissa eriä voi käyttää. On tärkeää, että tämä valintaruutu valitaan prosesseissa, jotka käyttävät sijaintidirektiivejä etsimään sijainteja eränumeroseurattujen nimikkeiden keräilyyn. Tällä tavoin voidaan sisällyttää myös eränumeroseurattuja nimikkeitä sisältävien sijaintien haku. Jos tämä valintaruutu on valittuna ja **strategia**-kentän arvoksi on määritetty *ei mitään*, järjestelmä siirtyy seuraavaan toimenpideriviin.
- **Strategia** – Voit helpottaa ja nopeuttaa kuhunkin sijaintidirektiiviriviin liitettyjen toimintojen määrittämistä valitsemalla jonkin seuraavista esimääritetyistä strategioista:

    - **Ei mitään** – Strategiaa ei käytetä.
    - **Täsmäytä pakkausmäärä** – Tämä strategia tarkistaa, onko keräilysijainnille määritetty pakkausmäärä. Tämä strategia on voimassa vain, kun **työtyyppi**-kentän arvona on *poiminta*.
    - **Konsolidoi** – Tämä strategia konsolidoi tietyssä sijainnissa olevia nimikkeitä, kun vastaavat nimikkeet ovat jo käytettävissä.. Tämä strategia on voimassa vain, kun **työtyyppi**-kentän arvona on *Aseta*. Tyypillisessä hyllytysmäärityksessä yritetään konsolidointia ensimmäiselle toimintoriville ja sitten toisella rivillä hyllytystä ilman konsolidointia. Tuotteiden konsolidointi tehostaa keräystä vastaisuudessa.
    - **FEFO-erävaraus** – Tämä strategia käyttää FEFO-erävarauksia. Käytä sitä, kun varastoa etsitään käyttämällä erän vanhentumispäivää ja kohdistetaan erävaraukseen. Voit käyttää tämän strategian vain eränimikkeissä. Käytettävissä vain, kun **Työn tyyppi** -asetuksena on *Keräily*.
    - **Pyöristä kokonaiseen rekisterikilpeen ja FEFO-erään** – Tämä strategia yhdistää *FEFO-erävarauksen*- ja *Pyöristä kokonaiseen rekisterikilpeen* -strategioiden elementtejä. Se on käytettävissä vain eränimikkeissä ja sijaintidirektiiveissä, joiden työtyyppi on *Keräily*. *FEFO-erävaraus*-strategian käyttäminen edellyttää eränimikkeiden käyttöä rivillä. *Pyöristä kokonaiseen rekisterikilpeen* -strategiaa voidaan käyttää vain täydennykseen. Jos tämä strategia on määritetty yhdessä sijainnin varastointirajan kanssa, se voi aiheuttaa valitun hyllytystyösijainnin ylitäyttymisen ja varastointirajojen ohittamisen.
    - **Pyöristä kokonaiseen rekisterikilpeen** – Tällä strategialla pyöristetään varastomäärä vastaamaan rekisterimerkinnän määrää, joka on määritetty kerättäville nimikkeille. Tätä strategiaa voi käyttää vain *Keräily*-tyypin täydennyksen sijaintidirektiiveihin. Jos tämä strategia on määritetty yhdessä sijainnin varastointirajan kanssa, se voi aiheuttaa valitun hyllytystyösijainnin ylitäyttymisen ja varastointirajojen ohittamisen.
    - **Rekisterikilpiopastus** – Käytä tätä strategiaa, kun vapautat tilauksen varastoon keräily- ja hyllytystyön luontia varten. Tätä menetelmää voi käyttää useissa rekisterikilvissä. Strategia yrittää varata ja luoda keräilytöitä sijainneissa, joissa on pyydettyjä siirtotilausriveihin liitettyjä rekisterikilpiä. Jos näitä toimintoja ei kuitenkaan voi suorittaa loppuun mutta keräilytyö halutaan silti luoda, käytä jotain muuta sijaintidirektiivitoimintojen strategiaa. Liiketoiminnan tarpeiden mukaan on mahdollista, että varastohaku halutaan tehdä varaston toisella alueella.
    - **Tyhjä sijainti ilman saapuvia töitä** – Käytä tätä strategiaa tyhjien sijaintien etsimiseen. Sijainnin katsotaan olevan tyhjä, jos sillä ei ole fyysistä varastoa, eikä odotettuja saapuvia töitä. Voit käyttää tätä strategiaa vain sijaintidirektiiveille, joiden työtyyppi on *Hyllytys*.
    - **Sijainnin FIFO-erääntyminen** – Käytä FIFO-strategiaa sekä eräseurattujen nimikkeiden että ei-eräseurattujen nimikkeiden lähettämiseen sen päivämäärän perusteella, jolloin varastoa saapui fyysiseen varastoon. Tätä ominaisuus voi kätevä etenkin ei-eräseuratun varaston osalta, jos vanhentumispäivä ei ole käytettävissä lajittelua varten. FIFO-strategia etsii vanhimman erääntymispäivämäärän sisältävän sijainnin ja kohdistaa sitten keräilyn kyseisen päivämäärän perusteella.
    - **Sijainnin LIFO-erääntyminen** – Käytä LIFO-strategiaa sekä eräseurattujen nimikkeiden että ei-eräseurattujen nimikkeiden lähettämiseen sen päivämäärän perusteella, jolloin varastoa saapui fyysiseen varastoon. Tätä ominaisuus voi kätevä etenkin ei-eräseuratun varaston osalta, jos vanhentumispäivä ei ole käytettävissä lajittelua varten. LIFO-strategia etsii uusimman erääntymispäivämäärän sisältävän sijainnin ja kohdistaa sitten keräilyn kyseisen päivämäärän perusteella.

## <a name="example-using-location-directives"></a>Esimerkki: sijaintidirektiivien käyttäminen

Tarkastele tätä esimerkkiä varten ostotilausprosessia, jossa sijaintidirektiivin on löydettävä varastosta vapaata kapasiteettia varastonimikkeille, jotka on juuri rekisteröity vastaanottolaiturilla. Sinun on ensin löydettävä varastosta vapaata kapasiteettia konsolidoimalla nykyiseen käsillä olevaan varastoon. Jos konsolidointi ei ole mahdollista, sinun on löydettävä tyhjä sijainti.

Tätä skenaariota varten sinun on määritettävä kaksi sijaintidirektiivitoimintoa. Sarjan ensimmäisen toiminnon on käytettävä *Konsolidointi*-strategiaa, ja toisen tulisi käyttää *Tyhjä sijainti ilman saapuvia töitä* -strategiaa. Jollet määritä kolmatta toimintoa käsittelemään ylivuotoskenaariota, on mahdollista saada kaksi lopputulosta, kun varastossa ei ole enää kapasiteettia: työ voidaan luoda, vaikka sijainteja ei ole määritetty, tai työn luontiprosessi saattaa epäonnistua. Tulos määrittyy **Sijaintidirektiivivirheet**-sivun määrityksen mukaan. Sivulla voi valita, valitaanko **Pysäytä työ sijaintidirektiivivirheeseen** -asetus kullekin työtilaustyypille.

## <a name="next-step"></a>Seuraava vaihe

Kun olet luonut sijaintidirektiivit, voit liittää kunkin direktiivikoodin työmallin koodiin työn luomista varten. Lisätietoja on kohdassa [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](./control-warehouse-location-directives.md).

## <a name="additional-resources"></a>Lisäresurssit

- Video: [Perusteellinen varastonhallinnan määrityksen tarkastelu](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Ohjeartikkeli: [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
