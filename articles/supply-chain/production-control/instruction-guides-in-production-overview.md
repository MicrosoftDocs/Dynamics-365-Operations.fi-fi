---
title: Yhdistetyn todellisuuden oppaiden tuottaminen tuotannon työntekijöille
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin tuotannon hallintamoduulin ja Dynamics 365 Guidesin integrointia.
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 48e0dfeba1a9744c90608d4d9009484df91c4b85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246138"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Yhdistetyn todellisuuden oppaiden tuottaminen tuotannon työntekijöille

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tuotantoprosesseissa työskenteleville työntekijöille on apua oikea-aikaisesti toimitetuista työtilanteeseen liittyvistä ohjeista. *Ohjeet* koskevat monia työalueita, kuten kokoonpanoa, huoltoa, työvaiheita, sertifiointia ja turvallisuutta. Näitä liiketoiminnan perustoimintoja koskevat jatkuvasti kehittyvät koulutusohjeet auttavat työntekijöitä toimimaan tehokkaammin ja paremmin.

## <a name="introduction"></a>Johdanto

Ohjeita voidaan antaa eri tavoin. Yksi tehokas, heti käyttövalmis järjestelmä käyttää [Dynamics 365 Guidesia](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guidesin avulla työntekijöille voidaan antaa käytännön opastusta. Voit määrittää standardoidut prosessit vaiheittaisilla ohjeilla, jotka opastavat työntekijöitä valitsemaan tarvittavat työkalut ja osat. Lisäksi nämä oppaat näyttävät työntekijöille, miten kyseisiä työkaluja käytetään todellisissa työtilanteissa.

Oppaita voi liittää esimerkiksi seuraaviin tuotannonhallinnan osiin:

- [Resurssit](#resources)
- [Resurssiryhmät](#resource-groups)
- [Vapautetut tuotteet](#released-products)
- [Reseptit](#formulas)
- [Kaavaversiot](#formula-versions)
- [Tuoterakenteet](#bom)
- [Tuoterakenneversiot](#bom-versions)
- [Reititykset](#routes)
- [Reititysversiot](#route-versions)
- [Reitityksen työvaihesuhteet](#route-operation-relations)

> [!NOTE]
> Oppaita voi liittää myös käyttöomaisuuden hallinnan avulla. Lisätietoja tästä vaihtoehdosta on kohdassa [Dynamics 365 Supply Chain Managementin (Käyttöomaisuuden hallinta) ja Dynamics 365 Guidesin integrointi](../asset-management/asset-management-guides-integration.md).

Kun tuotannon työntekijä valitsee työn tuotannossa Supply Chain Managementissa, työntekijä näkee työkortissa olevat työhön [liittyvät oppaat](#logic). Kun työntekijä valitsee tietyn oppaan, näyttöön tulee kyseisen oppaan QR-koodi. Työntekijä käynnistää sitten oppaat skannaamalla sitten QR-koodin HoloLens-laitteella, jolloin liittyvät ohjeet tulevat näkyviin.

Seuraavissa alaosioissa käsitellään joitakin skenaarioita, joissa eri toimialojen yrityksille on eniten hyötyä tuotannon ohjeiden esittämisestä oppaiden avulla.

### <a name="assembly"></a>Kokoonpano

![Oppaiden käyttäminen kokoonpanotehtävissä](media/instruction-guides-hero-assembly.png "Oppaiden käyttäminen huoltotehtävissä")

Kokoonpanotoimintojen ohjeet näyttävät työntekijöille, mitä työkaluja ja osia he tarvitsevat ja miten niitä käytetään käytännössä käytetään.

Tuotantopäälliköt voivat luoda ja määrittää oppaita esimerkiksi [tuotantoreittejä](routes-operations.md), [työvaiheiden suhteita](routes-operations.md#operation-relations) tai [tuoterakennetta](bill-of-material-bom.md) varten. Työntekijät saavat käyttöönsä tuotannon työvaihetta koskevat ohjeet.

### <a name="service"></a>Huolto

![Oppaiden käyttäminen huoltotehtävissä](media/instruction-guides-hero-service.png "Oppaiden käyttäminen huoltotehtävissä")

Teknikoille voidaan antaa opastetut ohjeet työkohteessa, joten lisäkäyntejä ei tarvitse aikatauluttaa.

Huoltopäälliköt voivat määrittää esimerkiksi tietyille [tuotteille](../../commerce/product.md) oppaita, joissa käydään läpi kaikki laadunarviointitoimet.

### <a name="quality"></a>Laatu

![Oppaiden käyttäminen laadunvalvontatehtävissä](media/instruction-guides-hero-quality.png "Oppaiden käyttäminen laadunvalvontatehtävissä")

Uusien prosessien käyttöönottaminen ja yhdenmukaisuuden paranemisen varmistaminen muuttamalla työntekijöiden tietämyksen toistettavaksi työkaluksi.

Laadunvalvontapäälliköt voivat määrittää esimerkiksi [tuotteille](../../commerce/product.md) oppaita, joissa käydään läpi kaikki laadunarviointitoimet.

### <a name="certifications"></a>Varmenteet

![Oppaiden käyttäminen sertifiointiin liittyvissä tehtävissä](media/instruction-guides-hero-certification.png "Oppaiden käyttäminen sertifiointiin liittyvissä tehtävissä")

Tunnistamalla nopeasti, ketkä työntekijät tarvitsevat apua ja missä apua tarvitaan, voidaan varmistaa, että kaikki työntekijät ovat korkeiden standardien mukaisia.

### <a name="safety"></a>Turvallisuus

![Oppaiden käyttäminen työturvallisuusohjeistuksessa](media/instruction-guides-hero-safety.png "Oppaiden käyttäminen työturvallisuusohjeistuksessa")

Vaarallisten toimenpiteiden käyminen läpi virtuaalisesti ohjeiden avulla ennen niiden suorittamista fyysisessä ympäristössä. Yhdistetyn todellisuuden avulla työntekijät voivat kokeilla vaarallisia toimenpiteitä virtuaalisesti.

Tuotantopäälliköt voivat antaa tarkkoja vaarallisten materiaalien tai helposti särkyvien tuotteiden käsittelyohjeita määrittämällä ohjeet [tuotenimikkeille](../../commerce/product.md), [reiteille](routes-operations.md) ja [työvaiheille](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Ohjeiden ja oppaiden käytön aloittaminen

Dynamics 365 Guides voidaan integroida heti Supply Chain Managementiin, mikä mahdollistaa ohjeiden antamisen tuotantoprosesseissa. Tuotannon resursseja ja töitä koskevien yhdistetyn todellisuuden ohjeiden muodostaminen, ylläpitäminen ja määrittäminen edellyttää käyttöoikeudellista asennettua Guidesin sovellusesiintymää.

### <a name="prerequisites"></a>Edellytykset

Tämän toiminnon käyttö edellyttää, että järjestelmä sisältää seuraavat:

- Dynamics 365 Supply Chain Management versio 10.0.15 tai uudempi
- Supply Chain Management -sovellusten [kaksoiskirjoitus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write)
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) -versio 400.0.1.48 tai sitä uudempi

### <a name="turn-on-the-feature"></a>Toiminnon ottaminen käyttöön

Toiminnon käyttäminen järjestelmässä edellyttää, että sen määritysavaimet on otettu käyttöön. Se on tehtävä vain kerran. Järjestelmänvalvojan on tehtävä sitä varten seuraavat toimet:

1. Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
1. Laajenna **Yhdistetty todellisuus** -osa ja valitse sitten **Yhdistetyn todellisuus opas** -valintaruutu.
1. Laajenna **Tuotannon hallinta** -osa ja valitse sitten **Tuotanto-ohjeet** -valintaruutu.
1. Poista järjestelmä ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Oppaiden näkymisen määrittäminen tuotantoon

Määritä tapa, jolla oppat näkyvät tuotannossa, valitsemalla **Yhdistetty todellisuus \> Dynamics 365 Guides \> Määritä oppaiden integrointi**.

![Oppaan integroinnin määrittäminen tuotantoa varten](media/instruction-guides-configure-integration.png "Oppaan integroinnin määrittäminen tuotantoa varten")

Määritä seuraavat kentät:

- **Microsoft Dataverse URL** – Määritä sen Microsoft Dataverse -ympäristön URL-osoite, jossa luot Guides-sovelluksen. Muodossa contoso.crm4.dynamics.com URL-osoitteen ensimmäinen osa nimetään yleensä organisaation (kuten contoso.) mukaan, toinen osa ympäristön tietoalueen mukainen (kuten crm4.) ja viimeinen osa on toimialue (kuten dynamics.com). Yksi tapa etsiä oikea URL-osoite on siirtyä sivustoon [home.dynamics.com](https://home.dynamics.com/) ja avata Guides-sovellus. Kun Guides avautuu, URL-osoite on selaimen osoiterivillä (käytä vain URL-perusosoitetta, jonka pitäisi olla edellisen esimerkin kaltainen). Tätä arvoa käytetään oppaisen osoitteiden laatimiseen, ja se koodataan QR-koodeihin.
- **QR-koodin koko** – Määritä hahmonnetun QR-koodin koko. Järkevintä on valita koko, joka täyttää suurimman osan näytöstä mutta ei enemmän. *15* on yleensä hyvä arvo.
- **QR-koodin virheen korjaustaso** – Määritä QR-koodin tarkkuus. Mitä tarkempi koodi on, sitä luotettavampi se on. **QR-koodin koon** on kuitenkin oltava riittävän suuri, jotta se tukee valitun korjaustason mukaista tietojen tasoa.

> [!TIP]
> - Näyttöön liian suurien QR-koodien kokojen hahmontaminen kestää kauemmin, ja ne on sitten pienennettävä näyttöön sopivaksi. Tästä ei ole mitään hyötyä.
> - Jos QR-koodin koko on taas liian pieni, on mahdollista, että HoloLens ei lue koodia oikein joissakin ympäristöissä.
> - Tämä asetus kannattaakin testata jokaisessa laitteessa, jolla QR-koodi näytetään HoloLens-käyttäjille. Valitse asetukset, joilla saadaan riittävän hyvä luettavuus tuotantoympäristössä.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Kaikkien oppaan tehtävien yleiskatsaus

Valitsemalla **Kaikki oppaat** -sivun näet luettelon kaikista organisaatiossa käytettävissä olevista oppaista sekä kaikista tuotannon prosessien ja resurssien tehtävistä. Avaa se valitsemalla **Yhdistetty todellisuus \> Oppaat \> Kaikki oppaat**. Yläosassa on kaikki käytettävissä olevat oppaat sisältävä luettelo, ja voit suodattaa luetteloa suodatuskentän avulla. Alaosassa on kaikki oppaan tehtävät sisältävä luettelo sekä työkalurivi, jolla niitä voi hallita.

![Oppaiden hallinta](media/instruction-guides-allguides.png "Oppaiden hallinta")

Seuraavissa osissa käsitellään objektityyppejä, joille voidaan määrittää oppaita. Kukin määritetty ohje sisältää ohjeet, jotka liitetään automaattisesti kyseisiin tuotantotöihin ja joita voi käyttää tuotannossa.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Oppaan liittäminen resurssiin

Kun opas liitetään [resurssiin](operations-resources.md), kyseistä opasta voi käyttää soveltuvan tuotantotyön yhteydessä.

### <a name="typical-scenario-using-resources"></a>Tyypillinen resursseja käyttävä skenaario

Voit liittää oppaan esimerkiksi konetyyppisen resurssin yleisiin turvallisuusohjeisiin tai käsittelyohjeisiin. Tämän jälkeen opas on käytettävissä jokaisessa kyseisessä laitteessa tehtävässä työssä.

### <a name="add-a-guide-to-a-resource"></a>Oppaan liittäminen resurssiin

Oppaan liittäminen resurssiin:

1. Valitse **Tuotannonhallinta \> Asetukset \> Resurssit \> Resurssit**.
1. Valitse luetteloruudussa resurssi, johon haluat määrittää oppaan.
1. Laajenna **Liitetyt oppaat** -pikavälilehti.
1. Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä. Uusi rivi lisätään ruudukkoon.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa. Jos oppaita on paljon, oikean oppaan voi etsiä luetteloa suodattamalla.
    ![Oppaiden hallinta](media/instruction-guides-allguides.png "Oppaiden hallinta")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Oppaan liittäminen resurssiryhmään

Oppaan voi lisätä [resurssiryhmiin](tasks/define-discrete-manufacturing-resource-group.md), jos niillä hallitaan koneiden, tuotantolinjojen ja työsolujen ryhmiä.

### <a name="typical-scenarios-using-resource-groups"></a>Tyypillisiä resurssiryhmiä käyttäviä skenaariota

**Esimerkki 1:** Resurssiryhmä on määritetty useille saman mallin koneille. Sen sijaan että konemallin käsittelyohjeiden opas määritettäisiin jokaiselle kyseiselle resurssille, opas voidaan määrittää resurssiryhmälle, joka vastaa kyseistä konemallia.

**Esimerkki 2:** Resurssiryhmä on määritetty erilaisia koneita sisältävälle työsolulle ja käytössä on opas, jossa on työsolun ylläpidon yleiset ohjeet. Opas koskee kaikkia tämän työsolun tuotantotehtäviä.

### <a name="add-a-guide-to-a-resource-group"></a>Oppaan liittäminen resurssiryhmään

Oppaan liittäminen resurssiryhmään:

1. Valitse **Tuotannonhallinta \> Asetukset \> Resurssit \> Resurssiryhmät**.
1. Valitse luetteloruudussa resurssiryhmä, johon haluat määrittää oppaan.
1. Laajenna **Liitetyt oppaat** -pikavälilehti.
1. Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä. Uusi rivi lisätään ruudukkoon.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa. Jos oppaita on paljon, oikean oppaan voi etsiä luetteloa suodattamalla.
    ![Oppaan lisääminen resurssiryhmään](media/instruction-guides-resourcegroup.png "Oppaan lisääminen resurssiryhmään")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Oppaan liittäminen vapautettuun tuotteeseen

Opas voidaan lisätä mihin tahansa [vapautettuun tuotteeseen](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Tyypillinen vapautettuja tuotteita käyttävä skenaario

Tuotantotason oppaissa on tuotannon työntekijöiden apuna ohjeita, jotka liittyvät tietyn vapautetun tuotteen tai nimikkeen käyttämiseen tai käsittelemiseen.

### <a name="add-a-guide-to-a-released-product"></a>Oppaan lisääminen vapautettuun tuotteeseen

Oppaan lisääminen vapautettuun tuotteeseen:

1. Mene **Tuotantotietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa tuote, jolle opas määritetään.
1. Avaa toimintoruudussa **Suunnittele**-välilehti ja valitse **Näytä**-ryhmässä **Liitetyt oppaat**.
1. Valitun tuotteen **Liitetyt oppaat** -sivu avautuu.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**. 
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa.
    ![Oppaan lisääminen vapautettuun tuotteeseen](media/instruction-guides-ReleasedProduct-AddGuides.png "Oppaan lisääminen vapautettuun tuotteeseen")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Oppaan liittäminen kaavaan

Opas voidaan lisätä mihin tahansa [kaavaan](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Tyypillinen kaavoja käyttävä skenaario
  
Kaavatason oppaista tuotannon työtekijät saavat opastetut käsittelyohjeet kaavojen tai reseptien yhteydessä. Oppaat voidaan määrittää kaavan versioille.

> [!NOTE]
> Kaavaan perustuvan tuotantoprosesseihin liittyvän opastuksen voi määrittää reitille, reittiversioon tai reitin työvaihesuhteisiin.  

> Oppaita ei voi tällä hetkellä liittää yksittäisille kaavariveille.

### <a name="add-a-guide-to-a-formula"></a>Oppaan lisääminen kaavaan

Oppaan lisääminen kaavaan:

1. Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Kaavat**.
1. Avaa kaava, jolle opas määritetään.
1. Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko**-välilehti.
1. Laajenna **Liitetyt oppaat** -pikavälilehti.
1. Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä. Uusi rivi lisätään ruudukkoon.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa.
    ![Oppaan lisääminen kaavaan](media/instruction-guides-Formula.png "Oppaan lisääminen kaavaan")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Oppaan liittäminen kaavaversioon

Opas voidaan lisätä mihin tahansa [kaavaversioon](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Tyypillinen kaavaversioita käyttävä skenaario

Kaavan yksittäiseen versioon liitetyt oppaat antavat tuotannon työntekijöille ohjeita, joissa käydään läpi kaavan kyseisen version tuotanto.

> [!TIP]
> Kaavan tähän versioon perustuvan tuotantoprosesseihin liittyvän opastuksen voi määrittää reitille, reittiversioon tai reitin työvaihesuhteisiin.  

> [!NOTE]
> Oppaita ei voi tällä hetkellä liittää yksittäisille kaavariveille.

### <a name="add-a-guide-to-a-formula-version"></a>Oppaan lisääminen kaavaversioon

Oppaan lisääminen kaavaversioon:

1. Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Kaavat**.
1. Avaa sen version sisältävä kaava, jolle opas määritetään.
1. Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko**-välilehti.
1. Valitse **Kaavaversiot**-pikavälilehdessä versio, jolla opas määritetään.
1. Valitse **Kaavaversiot**-työkalurivillä **Liitetyt oppaat**.
    ![Valittuun kaavaversioon liittyvien oppaiden avaaminen](media/instruction-guides-FormulaVersion.png "Valittuun kaavaversioon liittyvien oppaiden avaaminen")
1. Kaavaversion **Liitetyt oppaat** -sivu avautuu.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**. 
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa.
    ![Oppaan lisääminen kaavaversioon](media/instruction-guides-FormulaVersionAddGuide.png "Oppaan lisääminen kaavaversioon")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Oppaan liittäminen tuoterakenteeseen

Oppaan voi lisätä mihin tahansa [tuoterakenteeseen](bill-of-material-bom.md).

### <a name="typical-scenario-using-bills-of-materials"></a>Tyypillinen tuoterakennetta käyttävä skenaario

Tuoterakenteeseen liitetyissä oppaissa on tuotannon työntekijöille ohjeita tuoterakenteen materiaalin valmisteluun ja käsittelyyn. Oppaat voidaan määrittää tuoterakenteen versioille.

> [!NOTE]
> Oppaita ei voi tällä hetkellä liittää yksittäisille tuoterakenteen riveille.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Oppaan lisääminen tuoterakenteeseen

Oppaan lisääminen tuoterakenteeseen:

1. Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Tuoterakenteet**.
1. Avaa tuoterakenne, jolle opas määritetään.
1. Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko**-välilehti.
1. Laajenna **Liitetyt oppaat** -pikavälilehti.
1. Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä. Uusi rivi lisätään ruudukkoon.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa.
    ![Oppaan lisääminen tuoterakenteeseen](media/instruction-guides-BOM.png "Oppaan lisääminen tuoterakenteeseen")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Oppaan liittäminen tuoterakenteen versioon

Oppaan voi lisätä mihin tahansa [tuoterakenteen versioon](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Tyypillinen tuoterakenteen versioita käyttävä skenaario

Yksittäiseen tuoterakenteen versioon liitetyissä oppaissa on tuotannon työntekijöille ohjeita, jotka selittävät yleisestä tuoterakenteesta tai sen muista versioista poikkeavan tuoterakenteen version materiaalien valmistelua ja käsittelyä.

> [!NOTE]
> Oppaita ei voi tällä hetkellä liittää yksittäisille tuoterakenteen riveille.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Oppaan lisääminen tuoterakenteen versioon

Oppaan lisääminen tuoterakenteen versioon:

1. Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Tuoterakenteet**.
1. Avaa sen version sisältävä tuoterakenne, jolle opas määritetään.
1. Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko**-välilehti.
1. Valitse **Tuoterakenteen versiot**-pikavälilehdessä versio, jolla opas määritetään.
1. Valitse **Tuoterakenteen versiot**-työkalurivillä **Liitetyt oppaat**.
    ![Valittuun tuoterakenteen versioon liittyvien oppaiden avaaminen](media/instruction-guides-BOMVersion.png "Valittuun tuoterakenteen versioon liittyvien oppaiden avaaminen")
1. Tuoterakenteen version **Liitetyt oppaat** -sivu avautuu.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa.
    ![Oppaan lisääminen tuoterakenteen versioon](media/instruction-guides-BOMVersionAddGuide.png "Oppaan lisääminen tuoterakenteen versioon")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Oppaan liittäminen reittiin

Opas voidaan lisätä mihin tahansa [reittiin](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Tyypillinen reittejä käyttävä skenaario

Reittejä käytetään tyypillisesti määrittämään, miten tietty vapautettu tuote tuotetaan tuoterakenteen tai tuoterakenteen version ja resurssijoukon tai resurssiryhmien perusteella.

Opas määritetään reittiin antamaan kyseisen tuotantoprosessin vaiheittaiset ohjeet.

### <a name="add-a-guide-to-a-route"></a>Oppaan lisääminen reittiin

Oppaan lisääminen reittiin:

1. Valitse **Tuotannonhallinta \> Kaikki reitit**.
1. Avaa reitti, jolle opas määritetään.
1. Laajenna **Liitetyt oppaat** -pikavälilehti.
1. Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä. Uusi rivi lisätään ruudukkoon.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa.
    ![Oppaan lisääminen reittiin](media/instruction-guides-Route.png "Oppaan lisääminen reittiin")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Oppaan liittäminen reitin versioon

Opas voidaan lisätä mihin tahansa [reitin versioon](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Tyypillinen reitin versioita käyttävä skenaario

Reitin versioita käytetään tyypillisesti määrittämään tuotantoprosessien variantteja aiemmin luodun reitin perusteella. Kullekin reitin versiolle voi määrittää eri oppaat.

### <a name="add-a-guide-to-a-route-version"></a>Oppaan lisääminen reitin versioon

Oppaan lisääminen reitin versioon:

1. Valitse **Tuotannonhallinta \> Kaikki reitit**.
1. Avaa reitti, jolle opas määritetään.
1. Valitse **Versiot**-pikavälilehdessä versio, jolle opas määritetään.
1. Valitse **Versiot**-työkalurivillä **Liitetyt oppaat**.
    ![Valittuun reitin versioon liittyvien oppaiden avaaminen](media/instruction-guides-RouteVersion.png "Valittuun reitin versioon liittyvien oppaiden avaaminen")
1. Tuoterakenteen version **Liitetyt oppaat** -sivu avautuu.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa.
    ![Oppaan lisääminen reitin versioon](media/instruction-guides-RouteVersionAddGuide.png "Oppaan lisääminen reitin versioon")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Oppaan liittäminen reitin työvaihesuhteeseen

Opas voidaan lisätä mihin tahansa [reitin työvaihesuhteeseen](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Tyypillinen reitin työvaihesuhteita käyttävä skenaario

Työvaihesuhteet ovat tarkoin tapa lisätä ohjeita tuoteprosessin ja siihen liittyviin työvaiheisiin. Reitin kullekin työvaiheelle voidaan määrittää ohje, ja määritetty ohje voi vaihdella reitille määritetyn suhteen tyypin mukaan. Ohje voi siis olla erilainen esimerkiksi sen mukaan, mikä nimike tai määritys on kyseessä. Lisäksi voidaan määrittää, mitä työvaiheen osavaiheetta (kuten määritystä, jonoon asettamista, käsittelyä tai kuljetusta) ohjeet koskevat.

> [!NOTE]
> Jos reitin useille työvaihesuhteille määritetään oppaita, näistä oppaista vain tarkimmin suhdetta vastaava opas näytetään luodulle työlle tuotannossa.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Oppaan lisääminen reitin työvaihesuhteeseen

Oppaan lisääminen reitin työvaihesuhteeseen:

1. Valitse **Tuotannonhallinta \> Kaikki reitit**.
1. Avaa reitti, jolle opas määritetään.
1. Avaa toimintoruudussa **Reitti**-välilehti ja valitse **Ylläpito** -ryhmässä **Reititystiedot**.
1. Valitun reitin **Reititystiedot**-sivu avautuu.
1. Valitse yläruudukosta työvaihe, jolle ohjeet annetaan.
1. Valitse alaruudukossa tietty suhde (tai yleinen **Kaikki**-suhde).
    ![Työvaiheen ja sen jälkeen suhteen valitseminen](media/instruction-guides-RouteOperationRelation.png "Työvaiheen ja sen jälkeen suhteen valitseminen")
1. Avaa alaruudukon yläpuolella **Liitetyt oppaat** -välilehti. ![Liitetyt oppaat -välilehti](media/instruction-guides-RouteOperationRelation-AddGuide.png "Liitetyt oppaat -välilehti")
1. Lisää ruudukkoon uusi rivi valitsemalla alaruudukon yläosan työkalurivillä **Lisää**.
1. Valitse uudelle riville määritettävä opas **Nimi**-sarakkeen avattavassa luettelossa. Valitse rivin muilta osin valintaruutu jokaiselle tilanteelle, jossa valittu opas on oltava käytettävissä.

> [!NOTE]
> Kunkin työvaiheen kuhunkin osavaiheeseen voi lisätä useita oppaita.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Oppaiden valitseminen tuotannon käyttöliittymässä

Kun työntekijä avaa työluettelon tuotannon käyttöliittymässä, Supply Chain Management etsii näkyvissä olevia töitä koskevat oppaat. Voit tarkastella liittyviä oppaita **Oppaat**-painikkeella.

![Oppaat-painike tuotannon käyttöliittymässä](media/instruction-guides-Shopfloor1.png "Oppaat-painike tuotannon käyttöliittymässä")

Aseta HoloLens sitten paikalleen ja siirry soveltuvaan oppaaseen vilkaisemalla QR-koodia ja aktivoimalla opas tällä tavoin.

![QR-koodi oppaiden käyttämiseen HoloLensin avulla](media/instruction-guides-Shopfloor2.png "QR-koodi oppaiden käyttämiseen HoloLensin avulla")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Oppaiden valintalogiikan ratkaiseminen

Oppaita voi lisätä seuraaviin tuotantotietoihin:

- [Resurssit](#resources)
- [Resurssiryhmät](#resource-groups)
- [Vapautetut tuotteet](#released-products)
- [Reseptit](#formulas)
- [Kaavaversiot](#formula-versions)
- [Tuoterakenteet](#bom)
- [Tuoterakenneversiot](#bom-versions)
- [Reititykset](#routes)
- [Reititysversiot](#route-versions)
- [Reitityksen työvaihesuhteet](#route-operation-relations)

Kun Supply Chain Management luo tuotannon töitä, se kerää liittyvät oppaat kyseisistä lähteistä. Ota huomioon seuraavat tärkeät säännöt.

- Jos liität tuoterakenteen tai kaavan version reittiin tai tuotantotilaukseen, niin kyseiseen versioon ja myös sen päätuoterakenteeseen tai -kaavaan liitetyt oppaat näytetään työssä.
- Jos liität reitin version tuotantotilaukseen, niin kyseiseen versioon ja myös sen pääreittiin liitetyt oppaat näytetään työssä.
- Jos määrität useita reitityksen työvaiheita, jotka sisältävät *Kaikki*-suhteen, ja määrität niille oppaita, vain tarkimman suhteen oppaat näytetään työssä.  

![Kaavio oppaiden soveltuvuuden ratkaisemisesta](media/instruction-guides-Resolve.png "Kaavio oppaiden soveltuvuuden ratkaisemisesta")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]