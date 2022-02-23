---
title: Sijaintidirektiivien käyttäminen
description: Tässä aiheessa käsitellään sijaintidirektiivien käyttämistä. Sijaintidirektiivit ovat käyttäjän määrittämiä sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa.
author: Mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b1b3bafb24ff6eb0c42d901fac3b6668cedf39ef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963307"
---
# <a name="work-with-location-directives"></a>Sijaintidirektiivien käyttäminen

[!include [banner](../includes/banner.md)]

Sijaintidirektiivit ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään ja minne kerätyt nimikkeet sijoitetaan. Sijaintidirektiiveissä on otsikko ja liitettyjä rivejä. Niitä luodaan tietyille *työtilaustyypeille*.

> [!NOTE]
> Tämä ohjeaihe koskee **Varastonhallinta**-moduulin ominaisuuksia. Se ei koske [Inventoinnin- ja varastonhallinta](../inventory/inventory-home-page.md) -moduulin ominaisuuksia.

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
1. Luo toimipaikat, toimipaikkojen tyypit, toimipaikkojen profiilit ja toimipaikkojen muodot. Lisätietoja on kohdassa [Sijaintien määrittäminen VHJ-yhteensopivassa varastossa](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Luo toimipaikkoja, alueita ja vyöhykeryhmiä. Lisätietoja on kohdassa [Varaston määrittäminen](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) ja [Sijaintien määrittäminen VHJ-yhteensopivassa varastossa](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="work-order-types-for-location-directives"></a>Sijaintidirektiivien työtilaustyypit

Monet sijaintidirektiiveille määritettävät kentät ovat samoja kaikissa työtilaustyypeissä. Muut kentät ovat kuitenkin työtilaustyyppikohtaisia.

![Sijaintidirektiivien työtilaustyypit](media/Location_Directives_Work_Order_Types.png "Sijaintidirektiivien työtilaustyypit")

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
| Sijaintidirektiivit | Useita varastointiyksiköitä |
| Rivejä | Järjestysnumero |
| Rivejä | Määrästä |
| Rivejä | Määrälle |
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

Tällä sivulla voi tarkastella, luoda ja muokata sijaintidirektiivejä toimintoruudun komennoilla. Tämä aiheen muissa osissa on tietoja kaikkien sivulla olevien kenttien käyttämisestä.

## <a name="action-pane"></a>Toimintoruutu

**Sijaintidirektiivit**-sivun toimintoruudussa on painikkeita, joilla voi luoda, muokata ja poistaa direktiivejä (**Muokkaa**, **Uusi** ja **Poista**). Siinä on myös seuraavat painikkeet, joilla voi muokata sijaintidirektiivin käsittelyjärjestystä ja määrittää sijaintidirektiivin käytön ehdot määrittävän kyselyn:

- **Siirrä ylös** – Siirrä valittua sijaintidirektiiviä ylöspäin järjestyksessä. Voit esimerkiksi muuttaa sen järjestysnumeron 4:stä 3:ksi.
- **Siirrä alas** – Siirrä valittua sijaintidirektiiviä alaspäin järjestyksessä. Voit esimerkiksi muuttaa sen järjestysnumeron 4:stä 5:ksi.
- **Muokkaa kyselyä** – Avaa valintaikkuna ja määritä ehdot, joiden mukaan valittu sijaintidirektiivi käsitellään. Voit esimerkiksi päättää käyttää sitä vain tietyssä varastossa.

## <a name="location-directives-header"></a>Sijaintidirektiivien otsikko

Sijaintidirektiivin otsikko sisältää seuraavat järjestysnumeron kentät ja sijaintidirektiivin kuvaava nimi:

- **Järjestysnumero** – Tämä kenttä ilmaisee järjestyksen, jossa järjestelmä yrittää käyttää kutakin valitun työtilaustyypin sijaintidirektiiviä. Pienet numerot käytetään ensin. Järjestystä voi muuttaa toimintoruudun **Siirrä ylös**- ja **Siirrä alas** -painikkeilla.
- **Nimi** – Anna sijaintidirektiiville kuvaava nimi. Tämä nimi auttaa tunnistamaan direktiivin yleisen tarkoituksen. Anna nimeksi esimerkiksi *Myyntitilauksen keräily varastossa 24*.

## <a name="location-directives-fasttab"></a>Sijaintidirektiivit-pikavälilehti

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
    > Jos direktiivikoodi on määritetty, järjestelmä ei etsi sijaintidirektiivejä järjestysnumeron perustella, kun työ on luotava. Sen sijaan haku tehdään direktiivikoodin perusteella. Tällä tavoin voit tarkentaa tietyssä työmallin vaiheessa käytettävää sijaintimallia. Kyse voi olla esimerkiksi materiaalien valmisteluvaihe.

- **Useita varastointiyksiköitä** – Valitse tässä asetukseksi *Kyllä*, jos haluat, että sijainnissa voi käyttää useita varastointiyksiköitä. Useita varastointiyksiköitä voidaan ottaa käyttöön esimerkiksi lastausovisijainnissa. Jos otat useat varastointiyksiköt käyttöön, hyllytyssijainti määritetään odotetusti työssä. Hyllytyssijainti voi kuitenkin käsitellä vain moninimikkeisen hyllytyksen (jos työ sisältää useita varastointiyksiköitä, joita on kerättävä ja hyllytettävä). Se ei voi käsitellä yhden varastointiyksikön hyllytystä. Jos asetuksena on *Ei*, hyllytyssijainti määritetään vain, jos hyllytyksessä on vain yhdenlaista varastointiyksikköä.

    > [!IMPORTANT]
    > Sekä moninimikkeisen hyllytyksen että yhden varastointiyksikön hyllytyksen käyttöönottaminen edellyttää kahden sellaisen rivin määrittämistä, jolla on sama rakenne ja samat määritykset. Toisen rivin **Useita varastointiyksiköitä** -asetukseksi on valittava *Kyllä* ja toisen *Ei*. Tämän vuoksi hyllytystoimintoja on oltava kaksi samanlaista sijaintidirektiiviä, vaikka työn tunnuksessa ei tehdä erottaa yhtä varastointiyksikköä ja useita varastointiyksiköitä. Jos molempia sijaintidirektiivejä ei määritetä, käytetystä sijaintidirektiivistä tulee usein esille odottamattomia liiketoimintaprosessisijainteja. Sijaintidirektiiveillä, joiden **työtyyppi** on *keräily*, on oltava samanlaisen määritys, jos käsiteltävissä tilauksissa on useita varastointiyksiköitä.

    Käytä **Useita varastointiyksiköitä** -vaihtoehtoa työriveillä, joilla käsitellään useita nimiketunnuksia. (Nimiketunnus on tyhjä työn tiedoissa, ja sen arvona näytetään **Useita** varastosovelluksen käsittelysivuilla.)

    Tyypillisessä skenaariossa työmalli määritetään siten, että siinä on useita keräily/hyllytys-pareja Tässä tapauksessa kannattaa ehkä hakea tietty valmistelusijainti käytettäväksi riveillä, joiden **Työntyyppi** on *Hyllytys*.

    > [!NOTE]
    > Jos **Useita varastointiyksiköitä** -asetuksena *Kyllä*, et voi valita **Muokkaa kyselyä** toimintoruudussa, sillä kysely ei voi arvioida nimiketasolla, onko nimikkeitä useita. Toivotun sijaintidirektiivin valinta voidaan varmistaa käyttämällä **Direktiivikoodi**-kenttää, ja tämä kenttä ohjaa niiden hyllytysriveihin liittyvien sijaintidirektiivin valintaa, joissa direktiivikoodi on määritetty työmalliin.

    Jos et käytä aina joko yhden nimikkeen tai yhdistelmänimikkeen toimintoja, kahden sijaintidirektiivin määrittäminen *Hyllytys*-työtyypille on tärkeää. Toisessa näistä **Useita varastointiyksiköitä** -asetuksena on *Kyllä* ja toisessa asetuksena on *Ei*.

- **Käytettävä jakelukoodi** – Määritä, onko sijaintidirektiivin käsittelykoodin vastattava nimikettä vastaanotettaessa käytettävää käsittelykoodia vai voiko sijaintidirektiivin valita minkä tahansa käsittelykoodin perusteella. Jos valitset *Tarkka vastine* ja **Käsittelykoodi**-kenttä on tyhjä, vain käsittelykoodit otetaan huomioon tässä sijaintidirektiivissä.

    > [!NOTE]
    > Tämä kenttä on käytettävissä vain valituissa työtilaustyypeissä, joissa sallitaan täydennys. Täydellinen on aiemmin tässä aiheessa kohdassa [Työtilaustyyppikohtaiset kentät](#fields-specific-types).

- **Etsintäperuste** – Määritä, onko hyllytysmäärä koko rekisterikilven määrä vai onko se nimikekohtainen. Tämän kentän avulla voi varmistaa, että koko rekisterikilven sisältö hyllytetään yhteen sijaintiin ja että järjestelmä ei ehdota sisällön jakamista useisiin sijainteihin seuraavissa prosesseissa: **ASN** (rekisterikilven vastaanotto), **Yhdistetyn rekisterikilven vastaanotto** ja **Klusteri**-vastaanotto. (**Klusteri**-vastaanottoprosessi edellyttää, että *klusterihyllytystoiminto* on otettu käyttöön.) Sijaintidirektiivikyselyn, rivien ja sijaintidirektiivitoimintojen toiminta vaihtelee valitun arvon mukaan. **Rivit**-pikavälilehteä käytetään vain, kun **etsintäperusteena** on *nimike*.

    > [!NOTE]
    > Tämä kenttä on käytettävissä vain valituissa työtilaustyypeissä, joissa sallitaan täydennys. Täydellinen on kohdassa [Työtilaustyyppikohtaiset kentät](#fields-specific-types).

- **Käsittelykoodi** – Tätä kenttää käytetään sijaintidirektiiveissä, joiden työtilaustyyppi on *Ostotilaukset*, *Valmiiden tuotteiden hyllytys* tai *Palautustilaukset* ja työtilaus on *Hyllytys*. Ohjaa sen avulla työnkulku käyttämään tiettyä sijaintidirektiiviä työntekijän varastosovelluksessa valitseman käsittelykoodin mukaan. Voit esimerkiksi ohjata palautetut tuotteet tarkastussijaintiin, ennen kuin palautetaan varastoon. Käsittelykoodi voidaan linkittää varaston tilaan. Tällä tavoin sitä voidaan käyttää muuttamaan varaston tila vastaanottoprosessin osana. Esimerkiksi käsittelykoodi *Laadunvalvonta* määrittä varastoon *Laadunvalvonta*-tilaan. Voit sitten käyttää erillistä sijaintidirektiiviä siirtämän kyseisen varaston karanteenisijaintiin.

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
    - **Tyhjä sijainti ilman saapuvia töitä** – Käytä tätä strategiaa tyhjien sijaintien etsimiseen. Sijainnin katsotaan olevan tyhjä, jos sillä ei ole fyysistä varastoa, eikä odotettuja saapuvia töitä. Tätä strategiaa voi käyttää vain sijaintidirektiiveissä, joiden työtyyppi on *Keräily*.
    - **Sijainnin FIFO-erääntyminen** – Käytä FIFO-strategiaa sekä eräseurattujen nimikkeiden että ei-eräseurattujen nimikkeiden lähettämiseen sen päivämäärän perusteella, jolloin varastoa saapui fyysiseen varastoon. Tätä ominaisuus voi kätevä etenkin ei-eräseuratun varaston osalta, jos vanhentumispäivä ei ole käytettävissä lajittelua varten. FIFO-strategia etsii vanhimman erääntymispäivämäärän sisältävän sijainnin ja kohdistaa sitten keräilyn kyseisen päivämäärän perusteella.
    - **Sijainnin LIFO-erääntyminen** – Käytä LIFO-strategiaa sekä eräseurattujen nimikkeiden että ei-eräseurattujen nimikkeiden lähettämiseen sen päivämäärän perusteella, jolloin varastoa saapui fyysiseen varastoon. Tätä ominaisuus voi kätevä etenkin ei-eräseuratun varaston osalta, jos vanhentumispäivä ei ole käytettävissä lajittelua varten. LIFO-strategia etsii uusimman erääntymispäivämäärän sisältävän sijainnin ja kohdistaa sitten keräilyn kyseisen päivämäärän perusteella.

## <a name="example-using-location-directives"></a>Esimerkki: sijaintidirektiivien käyttäminen

Tarkastele tätä esimerkkiä varten ostotilausprosessia, jossa sijaintidirektiivin on löydettävä varastosta vapaata kapasiteettia varastonimikkeille, jotka on juuri rekisteröity vastaanottolaiturilla. Sinun on ensin löydettävä varastosta vapaata kapasiteettia konsolidoimalla nykyiseen käsillä olevaan varastoon. Jos konsolidointi ei ole mahdollista, sinun on löydettävä tyhjä sijainti.

Tätä skenaariota varten sinun on määritettävä kaksi sijaintidirektiivitoimintoa. Sarjan ensimmäisen toiminnon on käytettävä *Konsolidointi*-strategiaa, ja toisen tulisi käyttää *Tyhjä sijainti ilman saapuvia töitä* -strategiaa. Jollet määritä kolmatta toimintoa käsittelemään ylivuotoskenaariota, on mahdollista saada kaksi lopputulosta, kun varastossa ei ole enää kapasiteettia: työ voidaan luoda, vaikka sijainteja ei ole määritetty, tai työn luontiprosessi saattaa epäonnistua. Tulos määrittyy **Sijaintidirektiivivirheet**-sivun määrityksen mukaan. Sivulla voi valita, valitaanko **Pysäytä työ sijaintidirektiivivirheeseen** -asetus kullekin työtilaustyypille.

## <a name="next-step"></a>Seuraava vaihe

Kun olet luonut sijaintidirektiivit, voit liittää kunkin direktiivikoodin työmallin koodiin työn luomista varten. Lisätietoja on kohdassa [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="additional-resources"></a>Lisäresurssit

- Video: [Perusteellinen varastonhallinnan määrityksen tarkastelu](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Ohjeaihe: [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md)
