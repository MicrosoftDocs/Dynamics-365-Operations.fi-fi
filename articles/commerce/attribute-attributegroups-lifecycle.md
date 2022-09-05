---
title: Määritteiden ja määriteryhmien hallinta
description: Tämä artikkeli kuvaa, kuinka määritteitä ja määriteryhmiä hallitaan tuotteiden ja niiden ominaisuuksien kuvaamiseen Microsoft Dynamics 365 Commercessa.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386969"
---
# <a name="manage-attributes-and-attribute-groups"></a>Määritteiden ja määriteryhmien hallinta

[!include [banner](includes/banner.md)]

Tämä artikkeli kuvaa, kuinka määritteitä ja määriteryhmiä hallitaan tuotteiden ja niiden ominaisuuksien kuvaamiseen Microsoft Dynamics 365 Commercessa.

*Määritteet* tarjoavan tavan kuvata tuotteita ja niiden ominaisuuksia käyttäjän määrittämien kenttien avulla. Esimerkkeihin kuuluvat muistin koko, kovalevyn kapasiteetti ja Energy Star -yhteensopivuus.

Määritteitä voidaan liittää erilaisiin Commerce-yksiköihin, kuten tuoteluokkiin ja kanaviin, ja niille voidaan määrittää oletusarvoja. Kun määritteet liittyvät tuoteluokkiin tai -kanaviin, tuotteet perivät nämä määritteet ja niiden oletusarvot. Määritteiden oletusarvot voidaan ohittaa yksittäisen tuotteen tasolla, kanavan tasolla tai luettelossa.

Tavallisella televisiotuotteella voi olla esimerkiksi seuraavat määritteet.

| Luokka   | Ominaisuus           | Sallitut arvot                        | Oletusarvo |
|------------|---------------------|-------------------------------------------|---------------|
| TV & Video | Tuotemerkki               | Mikä tahansa voimassa oleva tuotemerkkiarvo                     | Ei mikään          |
| TV         | Näytön koko         | 20–85 tuumaa                              | 55 tuumaa     |
|            | Vertikaaliresoluutio | 4K (2160p), Täysi HD (1080p) tai HD (720p) | 4K (2160p)    |
|            | Näytön päivitystaajuus | 60 Hz, 120 Hz, tai 240 Hz                     | 60 Hz          |
|            | HDMI-tuloja         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Määritteet ja määritetyypit

Määritteet perustuvat *määritetyyppeihin*. Määritetyyppi osoittaa minkälaista tietoa voi lisätä tiettyyn määritteeseen. Commercessa tuetaan seuraavia määritetyyppejä:

- **Valuutta** – Tämä tyyppi tukee valuutta-arvoja. Se voidaan sitoa (eli se voi tukea arvoaluetta) tai se voidaan jättää avoimeksi.
- **DateTime** – Tämä tyyppi tukee päivämäärä- ja aika-arvoja. Se voidaan sitoa tai jättää avoimeksi.
- **Desimaali** – Tämä tyyppi tukee numeerista arvoa, jota sisältää desimaaleja. Se tukee myös mittayksikköä. Se voidaan sitoa tai jättää avoimeksi.
- **Kokonaisluku** – Tämä tyyppi tukee numeerista arvoa. Se tukee myös mittayksikköä. Se voidaan sitoa tai jättää avoimeksi.
- **Teksti** – Tämä tyyppi tukee tekstiarvoa. Se tukee myös etukäteen määritettyä mahdollisten arvojen joukkoa, kun **Kiinteä luettelo** -asetus on käytössä.
- **Totuusarvo** – Tämä tyyppi tukee binaariarvoa (**tosi** tai **epätosi**).
- **Viite** – Tämä tyyppi viittaa muihin määritteisiin.

> [!NOTE]
> [Azure-hakuindeksin rajoituksista](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search) johtuen **Desimaali**-määritetyyppiä ei tueta pilvipohjaisille hakukokemuksille. Azure Cognitive Search ei tue **Desimaali**-määritetyyppien muuntamista **Edm.Double** -kohdeindeksin kenttätyypeiksi , koska tämä muunto vähentäisi tarkkuutta.

### <a name="set-up-attribute-types"></a>Määritä määritetyypit

Määritä määritetyypit noudattamalla tämän esimerkkitoimenpiteen vaiheita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Siirry kohtaan **Tuotetietojen hallinta \> Määritys \> Luokat ja määritteet \> Määritetyypit**.
1. Valitse toimintoruudussa **Uusi**.
1. Syötä  **Määritetyypin nimi** -kenttään **Laukkutyyppi**.
1. Valitse **Tyyppi**-kentässä **Teksti**.
1. Määritä **Kiinteä luettelo** -asetuksen arvoksi **Kyllä**.
1. Valitse **Arvot**-pikavälilehdessä **Lisää**.
1. Syötä uuden rivin **Arvo**-kenttään **Olkalaukku**.
1. Lisää viisi riviä. Syötä kunkin **Arvo**-kenttään eri arvo: **Pideltävä**, **Käsilaukku**, **Reppu**, **Postilaukku** tai **Lompakko**.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Uusi**.
1. Syötä  **Määritetyypin nimi** -kenttään **Aurinkolasimerkki**.
1. Valitse **Tyyppi**-kentässä **Teksti**.
1. Määritä **Kiinteä luettelo** -asetuksen arvoksi **Kyllä**.
1. Valitse **Arvot**-pikavälilehdessä **Lisää**.
1. Syötä uuden rivin **Arvo**-kenttään **Ray ban**.
1. Lisää kaksi riviä. Syötä kunkin **Arvo**-kenttään eri arvo: **Aviator** tai **Oakley**.
1. Valitse toimintoruudussa **Tallenna**.

![Määritetyypit-sivu.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Määritteen määrittäminen

Määritä määritetyyppi noudattamalla tämän esimerkkitoimenpiteen vaiheita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Siirry kohtaan **Tuotetietojen hallinta \> Määritys \> Luokat ja määritteet \> Määritteet**.
1. Valitse toimintoruudussa **Uusi**.
1. Syötä **Nimi**-kentään **Laukkutyyppi**.
1. Valitse  **Määritetyyppi** -kentässä **Laukkutyyppi**.
1. Valitse toimintoruudussa **Tallenna**.

![Määritteet-sivu.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Määritteen metatiedot

*Määritteen metatiedoissa* voit valita asetuksia, jotka määrittävät, miten kunkin tuotteen määritteet toimivat. Voit esimerkiksi määrittää, ovatko määritteet pakollisia sekä voiko niitä käyttää hauissa ja suodattimina.

Tuotteiden määritteiden metatietoasetukset voidaan korvata kanavatasolla.

**Määritteet**-sivulla on useita määritteen metatietoihin liittyviä vaihtoehtoja. Voit esimerkiksi määrittää **Voidaan tarkentaa** -valinnaksi **Kyllä** kohdan **Määritteiden metatiedot Commerce-kanaville** alla ja määrite näytetään tuotteiden tarkennusta tai suodatusta varten hakutuloksissa ja luokkien selaussivuilla. Voit määrittää määritteen tarkennettavaksi valitsemalla ensin **Suodatusasetukset** toimintopaneelissa ja vahvistamalla määritteen suodatusasetukset.

## <a name="filter-settings-for-attributes"></a>Määritteiden suodatusasetukset

Voit määrittää määritteiden suodatusasetuksissa, miten määritteiden suodattimet näytetään myyntipisteessä (POS). Voit käyttää määritteen suodatusasetuksia valitsemalla määritteen **Määritteet**-sivulla toimintoruudussa **Suodatusasetukset**.

**Suodatusasetukset**-sivulla on seuraavat kentät:

- **Nimi** – Tämä kentän arvo on oletusarvoisesti määritteen nimi. Voit kuitenkin muuttaa arvon.
- **Näyttöasetus** – Seuraavat asetukset ovat käytettävissä:

    - **Yksi arvo** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Totuusarvo**, **Valuutta**, **Desimaali**, **Kokonaisluku** ja **Teksti**. Se sallii vain yksittäisen arvon valinnan tuoteluettelosivujen tarkennuksille, kuten luokkien selaamiselle ja tuotehakutulossivuille.
    - **Useita arvoja** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali**, **Kokonaisluku** ja **Teksti**. Se mahdollistaa useiden arvojen valinnan määritteelle asiakasohjelmassa tarkennusta varten.

- **Näytön ohjaus** – Seuraavat asetukset ovat käytettävissä:

    - **Luettelo** – Tämä vaihtoehto on kaikkien määritetyyppien käytettävissä.
    - **Alue** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali** ja **Kokonaisluku**.
    - **Liukusäädin** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali** ja **Kokonaisluku**.
    - **Liukusäädin palkeilla** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali** ja **Kokonaisluku**.

- **Raja-arvo** – Tämä asetus on pakollinen, jos olet valinnut näytön ohjaustyypiksi **Alue**. Voit määrittää arvot käyttämällä puolipistettä (;) erottimena.

    Esimerkiksi **Laukun tilavuus** -määritteelle, jonka määritetyyppi on **Kokonaisluku**, kynnysarvo voi olla **10; 20; 50; 100; 200; 500; 1000; 5000**. Siinä tapauksessa seuraavat alueet näkyvät myyntipisteessä. Jos jollakin tulosjoukon alueella ei ole tuotteita, kyseinen alue näkyy himmennettynä.

    - Alle 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 tai enemmän

Suodatinasetukset määritteille soveltuvat vain tuotemääritteille ja niitä voidaan käyttää tuotehaun ja luokkien selaamisen tulosten tarkentamiseen. Niitä ei käytetä asiakashakuun tai tilaushakuun, vaikka samoja määritteitä voidaan käyttää rikastamaan asiakas-tai tilaustietoja.

Commercen oletusmoduuleissa ei ole mukana tukea **Näytön hallinta** -suodatinasetuksille, kuten **Alue**, **Liukukytkin** ja **Liukukytkin palkeilla**. The **Väli**- ja **Liukusäädin**-asetuksia tuetaan jatkossakin myyntipisteratkaisuille, kun taas **Liukusäädin palkeilla** -asetusta käytetään vanhoissa SharePoint-verkkokaupoissa ja se on jatkossakin saatavilla kolmannen osapuolen integrointeja ja mukautettuja skenaarioita varten.

Suosittelemme, että tarkennettavilla määritteillä on **Teksti**-tyyppinen määrite, jossa **Kiinteä luettelo** -valinta on käytössä ja että luettelo pidetään hallittavan kokoisena (enintään 100-200 yksilöllistä arvoa). Jos tarkentajalla on 1 000 tai useampia yksilöllisiä arvoja, on sopivampaa käyttää **Teksti**-tyyppistä määritettä, jossa **Kiinteä luettelo** -valinta on pois käytöstä.

Käännökset ovat kriittisiä määritteiden nimien ja niiden arvojen kannalta. **Teksti**-tyyppisille määritteille, joissa **Kiinteä luettelo** -valinta on käytössä, käännöksen voidaan määrittää määritteiden arvoille kohdan **Määritetyyppi** alla. Voit määrittää muille määritetyypeille käännökset sivulla, jolla määritteiden arvot määritetään. Voit esimerkiksi määrittää **Teksti**-tyyppiselle määritteelle oletusarvon käännökset määritteen **Määritteet**-sivulla. Jos kuitenkin ohitat oletusarvon tuotetasolla, voit määrittää määritteen käännökset tuotteen **Tuotemääritteet**-sivulla .

Kun määrite on merkitty tarkennettavaksi kanavalle, määritetyyppiä ei tule päivittää. Muutoin vaikutat tuotetietojen julkaisemiseen hakuindeksiin. Suosittelemme sen sijaan, että luot uuden määritteen uudelle tarkentajatyypille ja poistat määritteen käytöstä muista määriteryhmistä.

Järjestelmä tukee hakutuloksia määritteiden perusteella, mutta hakee vain hakusanojen tarkat vastaavuudet. Esimerkiksi **Kangas**-määritteen arvo on **Cashmere-puuvilla**. Jos asiakas etsii haulla "Cash", mitään tuotteita, joissa **Cashmire-puuvilla** kankaana, ei noudeta. Jos asiakas kuitenkin etsii haulla "Cashmere", "Puuvilla" tai "Cashmere Puuvilla", tuotteet, joiden kankaana on **Cashmere-puuvilla** haetaan.

### <a name="additional-attribute-metadata-options"></a>Lisämääritteiden metatietojen asetukset

> [!NOTE]
> Nämä määritteen metatietojen vaihtoehdot koskevat vain vanhoja SharePoint online -kauppoja ja ulkoisia integrointeja. Lisätietoja näistä määritteiden metatietoasetuksista on kohdassa [SharePoint Server 2013 -hakumallin yleiskatsaus](/SharePoint/search/search-schema-overview).

Seuraavat määritteiden metatietojen lisäasetukset ovat myös käytettävissä **Määritteet**-sivulla:

- Etsittävissä
- Noudettavissa
- Voidaan kysellä
- Lajiteltavissa
- Ohita kirjainkoko ja muoto
- Täysi vastaavuus

Nämä asetukset oli tarkoitettu alun perin vanhojen SharePoint-pohjaisten verkkokauppojen hakutoimintojen parantamista varten. Ne eivät välttämättä koske Commercen sähköisen kaupankäynnin internet-sivustoja tai pos-päätteet. Koska headless -integrointia tuetaan edelleen, nämä vaihtoehdot ovat käytettävissä määritteen metatietojen viemiseen Commerce software development kit (SDK) -rakenteen avulla. Commerce SDK:n avulla voit asettaa tuotteet mukautettuun, optimoituun ulkoiseen hakuindeksiin. Näin voit varmistaa, että vain määritteet, jotka pitää indeksoida, indeksoidaan.

## <a name="attribute-groups"></a>Määriteryhmät

*Määriteryhmää* käytetään komponentin tai alikomponentin yksittäisten määritteiden ryhmittelemiseen tuotemääritysmallissa. Määrite voi sisältyä useisiin määriteryhmiin. Määriteryhmät voivat auttaa käyttäjiä tuotteiden määrityksessä, sillä eri valinnat järjestetään tietyn kontekstin mukaan. Määriteryhmät voidaan määrittää luokkiin tai kanaviin. Voit määrittää oletusarvot myös määriteryhmään sisältyvillä määritteille.

![Määriteryhmät-sivu.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Luo ominaisuusryhmä

Luo määriteryhmä noudattamalla tämän esimerkkitoimenpiteen vaiheita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Valitse **Tuotetietojen hallinta \> Asetukset \> Luokat ja määritteet \> Määriteryhmät**.
1. Luo määriteryhmä, jonka nimi on **Kauluspaidat**.
1. Lisää seuraavat määritteet: **PesuTapa**, **KaulusTyyppi**, **Kokoelma** ja **Malli**.

> [!NOTE]
> Määriteryhmän määritteiden näyttöjärjestysarvot eivät vaikuta haku- ja luokkaselaustulosten järjestykseen tai määritteiden järjestykseen. Ne koskevat vain tilausmääriteskenaariota.

### <a name="assign-attribute-groups-to-categories"></a>Määriteryhmien määrittäminen luokkiin

Määriteryhmiä voi liittää seuraavantyyppisten luokkahierarkioiden luokkasolmuihin:

- Kaupankäynnin tuotehierarkia
- Vähittäismyyntikanavan luokkahierarkia
- Lisätuoteluokan hierarkia

Kun tuotteet luokitellaan määriteryhmiin liitettyihin luokkiin, ne perivät näihin määriteryhmiin sisältyvät määritteet.

![Tuotteen määriteryhmien pikavälilehti Commercen tuotehierarkiasivulla.](media/AGRetailProdHierarchy_2022Series.png)

Määritä määriteryhmät luokkiin Commerce-tuotehierarkiassa seuraamalla tämän esimerkkikäytännön vaiheita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Valitse **Retail ja Commerce \> Luokka- ja tuotehallinta \> Commerce-tuotehierarkia**.
1. Valitse siirtymishierarkia **Muoti**.
1. Valitse **Miesten vaatteet** -kohdassa **Housut**-luokka ja lisää sitten **Tuotemääriteryhmät**-pikavälilehdessä **Miesten vyöt** -määriteryhmä.
1. Valitse **Merkkiaurinkolasit**-luokka ja tarkista **Merkkiaurinkolasit**-määriteryhmän uudet määritteet valitsemalla **Näytä määritteet**. Määriteryhmässä pitäisi nyt näkyä uudet **Linssin muoto**- ja **Aurinkolasien merkki** -määritteet.
1. Valitse **Housut**-luokka ja tarkista **Miesten vyöt** määriteryhmän määritteet valitsemalla **Näytä määritteet**. Määriteryhmässä pitäisi nyt näkyä määritteet **Miesten vyön merkki**, **Vyön materiaali** ja **Vyön koko**.

Samalla perusmenettelyllä voi määrittää myös määriteryhmiä luokkiin kanavan siirtymisluokkahierarkiaan ja lisätuoteluokkahierarkiaan. Vaiheessa 2 voit kuitenkin käyttää yhtä seuraavista polkuista sen hierarkian mukaan, johon haluat liittää määriteryhmiä:

- **Kanavan siirtymisluokkahierarkia:** Siirry kohtaan **Vähittäismyynti ja Commerce \> Luokkien ja tuotteiden hallinta \> Kanavan siirtymisluokat**.
- **Lisätuoteluokkahierarkia:** Siirry kohtaan **Vähittäismyynti ja Commerce \> Luokkien ja tuotteiden hallinta \> Lisätuoteluokat**.

> [!NOTE]
> Varmista, että liität määriteryhmiä luokkahierarkiaan vain **Tuotteen määriteryhmät** -pikavälilehdellä, ei **Luokan määritearvot** -pikavälilehdellä. Jos määritteet näkyvät Luokkamääritteen **Luokkamääritteen arvot** -pikavälilehdellä, valitse **Muokkaa luokkahierarkiaa** toimintoruudusta. Valitse sitten **Luokkamääritteen ryhmät** -pikavälilehdessä luokkasolmut ja valitse **Poista**. Määritteitä ei voi hakea luokan mukaan Commerce Scale Unitin kautta.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Commerce-kanavien tarkasteltavat ja tarkennettavissa olevat määritteet oletustuotekokoelmaa varten

Kun olet liittänyt useita määriteryhmiä eri hierarkioiden luokkiin (Commerce-tuotehierarkia tai kanavasiirtymäluokat) ja kunkin tuotteen määritearvot luokkaliitoksen perusteella, sinun on otettava **Näytä määrite kanavassa** käyttöön, jotta nämä määritteet näkyvät tietyssä kanavassa.

1. Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse **Määritä määritteen metatiedot** ja valitse sitten määrite vasemmassa siirtymäruudussa.
1. Määritä **Kanavan tuotemääritteet** -pikavälilehdellä (ei **Luokan määritteet** -pikavälilehdellä) **Näytä määrite kanavassa** -valinnaksi **Kyllä** näyttääksesi määritteen.
1. Jos haluat määritteen olevan myös tarkennettavissa, määritä **Voiko tarkentaa** -asetukseksi **Kyllä**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Dimensioihin perustuvien tarkentajien näkyvyyden hallinta, esimerkiksi koko, tyyli ja väri

Tuotedimensiot, kuten koko, tyyli ja väri, ovat useimmin käytettyjä tarkentajia. Jos haluat määrittää nämä tuotedimensiot käyttöön tarkennuksissa, liitä se määriteryhmä kanavatasolla, joka sisältää viitteen määritteen tyyppiin, joka perii arvot automaattisesti tuotedimensioarvoista.

Voit määrittää, että tuotedimensiot ovat näkyviä ja tarkennettavissa päivittämällä **kanavaluokkien ja tuotemääritteiden** sivun merkinnät. Valitse siirtymisruudussa juurisolmu ja aseta sitten **Kanavan tuotemääritteet** -pikavälilehdellä **Näytä määrite kanavassa** -valinnaksi **Kyllä** määritteille **Koko**, **Tyyli** ja **Väri**. Jos haluat näiden määritteiden olevan myös tarkennettavissa, määritä jokaisen **Voiko tarkentaa** -asetukseksi **Kyllä**.

![Dimension tarkentajien määritteen metatietojen määrittäminen.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Jos haluat ottaa määritteet käyttöön esittelytietoihin perustuvassa Houston-kanavassa, seuraa esimerkkikäytännön vaiheita.

1. Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse **Houston**-kanava.
1. Valitse toimintoruudussa **Määritä määritteen metatiedot**.
1. Valitse ensin **Muoti**-luokkasolmu ja valitse sitten **Kanavan tuotemääritteet** -pikavälilehdessä kunkin määritteen kohdalla **Sisällytä määrite**.
1. Valitse ensin **Muodin asusteet** -luokkasolmu, sitten **Merkkiaurinkolasit**-luokka ja lopuksi **Kanavan tuotemääritteet** -pikavälilehdessä kunkin määritteen kohdalla **Sisällytä määrite**.
1. Valitse ensin **Miesten vaatteet** -luokkasolmu, sitten **Housut**-luokka ja lopuksi **Kanavan tuotemääritteet** -pikavälilehdessä kunkin määritteen kohdalla **Sisällytä määrite**.
1. Kun olet päivittänyt aiottujen määritteiden ja tarkentajien määritteen metatiedot, varmista, että tallennat muutokset ja suoritat **Julkaise kanavan päivitys** -työn. Päivitysten julkaisemisen jälkeen on sitten suoritettava seuraavat työt: **1070** (**kanavan konfiguraatio**), **1040** (**Tuotteet**) ja **1150** (**luettelo**).

> [!NOTE]
> - Jos yrityksesi edellyttää, että lisäät tai poistat usein tuotteita siirtymishierarkiassa tai teet muutoksia, kuten näyttötilausten arvojen päivittämistä, uusien luokkien lisäämistä ja uusien määriteryhmien lisäämistä luokkiin, suosittelemme, että määrität **Julkaise kanavan päivitykset** -työn suoritettavaksi säännöllisenä erätyönä. Vaihtoehtoisesti voit käynnistää manuaalisesti **Julkaise kanavan päivitykset** -työn ja sitten seuraavat Commerce Data Exchange (CDX) -työt: **1070** (**Kanavan määritys**), **1040** (**Tuotteet**) ja **1150** (**Luettelo**).
> - Voit määrittää **Perintä**-asetuksen avulla, että kanava perii määriteryhmät ylätason kanavasta hierarkiassa. Jos valitset **Peri**-asetukseksi **Kyllä**, alatason kanavasolmu perii kaikki määriteryhmät ja kaikki kyseisten määriteryhmien määritteet.
> - Jos toimintoruudun **Määritä määritteen metatiedot** -painike ei ole käytettävissä, varmista,että **siirtymishierarkia** on liitetty **Yleinen**-pikavälilehdellä kanavaan.
> - Et saa liittää määriteryhmiä lukuun ottamatta dimensioihin perustuvia määriteryhmiä kanavan tasolla (esimerkiksi **Määriteryhmiä**  **Kanavaluokat ja tuotemääritteet**-sivulla).
> - Kun asiakaskohtaisille B2B-luetteloille on tehty tuki Commerce-versiolle 10.0.27, sinun odotetaan tunnistavan kunkin B2B-luettelon tarkentajan ja määritteen asetukset samalla tavalla kuin tässä artikkelissa on kuvattu.

## <a name="override-attribute-values"></a>Määritearvojen ohittaminen

Yksittäisten tuotteiden määritteiden oletusarvot voidaan ohittaa tuotetasolla. Ne voidaan myös ohittaa yksittäisille tuotteille, jotka ovat tietyissä tiettyihin kanaviin suunnatuissa luetteloissa.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Yksittäisen tuotteen määritearvojen ohittaminen

Voit ohittaa yksittäisen tuotteen määritteen arvot noudattamalla tämän esimerkin ohjeita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Valitse **Vähittäismyynti ja Commerce \> Luokka- ja tuotehallinta \> Julkaistut tuotteet luokittain**.
1. Valitse **Muoti \> Asusteet \> Aurinkolasit**.
1. Valitse tarvittava tuote ruudukossa. Valitse sitten toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Tuotemääritteet**.
1. Valitse määrite vasemmassa ruudussa ja päivitä sen arvo oikeassa ruudussa.

![Tuotemääritearvot-sivu.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Luettelon kaikkien tuotteiden määritearvojen ohittaminen

Voit ohittaa kaikkien tuotteiden määritteiden arvot noudattamalla tämän esimerkin ohjeita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Valitse **Retail ja Commerce \> Luettelon hallinta \> Kaikki luettelot**.
1. Valitse **Fabrikamin perusluettelo** -luettelo.
1. Valitse **Muoti \> Asusteet \> Aurinkolasit**.
1. Valitse **Tuotteet**-pikavälilehdessä tarvittava tuote ja valitse sitten **Määritteet** tuoteruudukon yläpuolella.
1. Päivitä tarvittavien määritteiden arvot seuraavissa pikavälilehdissä:

    - Jaettu tuotemedia
    - Yhteiset tuotemääritteet
    - Kanavamedia
    - Kanavan tuotemääritteet

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Kanavan kaikkien tuotteiden määritearvojen ohittaminen

Voit ohittaa kaikkien kanavan tuotteiden määritteiden arvot noudattamalla tämän esimerkin ohjeita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse **Houston**-kanava.
1. Valitse **Tuotteet**-pikavälilehdessä tarvittava tuote ja valitse sitten **Määritteet** tuoteruudukon yläpuolella.
1. Jos tuotteita ei ole käytettävissä, valitse **Lisää** **Tuotteet**-pikavälilehdessä ja valitse sitten tarvittavat tuotteet **Lisää tuotteita** -valintaikkunassa.
1. Päivitä tarvittavien määritteiden arvot seuraavissa pikavälilehdissä:

    - Jaettu tuotemedia
    - Yhteiset tuotemääritteet
    - Kanavamedia
    - Kanavan tuotemääritteet

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Muuttujakohtaisten määritteen arvojen määrittäminen ja useiden arvojen määrittäminen tuotemääritteitä varten

Jos haluat määrittää muuttujakohtaisia määritteen arvoja ja määrittää tuotemääritteitä varten useita arvoja, noudata tämän esimerkin ohjeita.

1. Kirjaudu Commerce headquartersiin tuotepäällikkönä.
1. Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse **Houston**-kanava.
1. Valitse **Tuotteet**-pikavälilehdessä tarvittava tuotevariantti ja valitse sitten **Määritteet** tuoteruudukon yläpuolella.
1. Jos tuotteita ei ole käytettävissä, valitse **Lisää** **Tuotteet**-pikavälilehdessä ja valitse sitten tarvittavat tuotevariantit **Lisää tuotteita** -valintaikkunassa.
1. Päivitä tarvittavien määritteiden arvot seuraavissa pikavälilehdissä:

    - Jaettu tuotemedia
    - Yhteiset tuotemääritteet
    - Kanavamedia
    - Kanavan tuotemääritteet

#### <a name="example-of-variant-specific-attribute-configuration"></a>Esimerkki varianttikohtaisesta määritteen määrityksestä
        
Tässä esimerkissä **P001-Päätuote** on monitehtäväinen, ja siinä on kolme muuttujaa: **Juokseminen**, **Kävely** ja **Vaellus**. Jokaiselle muuttujalle on määritettävä **tehtävä**-määritteen arvo erikseen. Määritä **Tuotteet**-pikavälilehdellä kanavan **kanavaluokat ja tuotemääritteet** -sivulla **aktiviteetti**-määritteen arvon varianteille, kuten on kuvattu seuraavassa taulukossa.

| Muuttuja     | Aktiviteettimääritteen arvo |
|-------------|--------------------------|
| P001-Päätuote | Urheilu                   |
| P001-1      | Käynnissä                  |
| P001-2      | Kävely                  |
| P001-3      | Vaellus                 |

Jos käyttäjä etsii hakusanaa "kenkä", **P001-päätuote** näkyy hakutuloksissa. Jos määritit **Aktiviteetti**-määritteen tarkennettavaksi, **Aktiviteetti**-tarkentaja luetteloi vain **Urheilun** tarkennettavaksi arvoksi, koska kyseinen arvo määritettiin **Aktiviteetti**-määritteelle **P001-Päätuote**-tuotetasolla.

Oletusarvon mukaan muuttujatason määritteitä on tarkoitus käyttää vain tuotetietosivuilla (PDPt). Kun valitset tietyn tuotevariantin PDP:ssä, PDP-tuotemääritykset päivitetään kyseiselle variantille.

Jotta tarkentajat poimivat tuotemuuttujatasolla määritetyt määritteen arvot, sinun on määritettävä määrite tuotteen päätasolla, valittava **Salli useita arvoja** -valintaruutu ja määritettävä määritteen tyypiksi **Teksti**.

Seuraavaksi tuotemuuttujan kaikki mahdolliset arvot on määritettävä. Tämän esimerkin **Aktiviteetti**-määritteen mahdolliset arvot ovat **Juoksu**, **Kävely**, **Lenkkeily**, **Vaellus**, **Telttailu**, **Vesiurheilu** ja **Talviurheilu**.

Kun olet määrittänyt variantin määritteen arvot, voit määrittää ne tuotteen päätasolla käyttämällä pystyviivoin erotettuja arvoja. Voit määrittää **Aktiviteetti**-määritteelle tuotteen päätietoihin määritteen arvon **Juoksu|Kävely|Lenkkeily|Vaellus|Telttailu|Vesiurheilu|Talviurheilu**.

Kunkin variantin määritteen arvot voidaan sitten määrittää kirjoittamalla joko pystyviivoin erotellut arvot tai yksittäiset arvot. **Aktiviteetti**-määritteen yksittäinen tuotevariantti voidaan määrittää esimerkiksi **Juoksu|Kävely|Lenkkeily**, **Juoksu**, **Juoksu|Lenkkeily|Vesiurheilu** ja niin edelleen.

Kun olet määrittänyt variantin määritteen arvot, valitse **Kanavaluokat ja tuotemääritteet** -sivun toimintoruudussa **Julkaise kanavapäivitykset** ja suorita työt **1150**, **1040** ja **1070**.

Kun työt on tehty ja hakuindeksi on päivitetty, odotettujen arvojen pitäisi näkyä hakutuloksissa ja luokkien selaustuloksissa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
