---
title: "Määritteet, määriteryhmät ja niiden liitokset Finance and Operationsin vähittäismyynnin yksiköiden kanssa"
description: "Näiden ohjeiden avulla voit kuvata tuotteen ja sen ominaisuudet käyttäjän kenttämääritteiden avulla."
author: ashishmsft
manager: AnnBe
ms.date: 04/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5e04b1f6ef58836eeac85be074e295e6d1f42c52
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="attributes-attribute-groups-and-their-associations-with-various-retail-entities-in-finance-and-operations"></a>Määritteet, määriteryhmät ja niiden liitokset Finance and Operationsin vähittäismyynnin yksiköiden kanssa

[!include [banner](includes/banner.md)]

*Määritteiden* avulla voidaan täydentää tuotteen ja sen ominaisuuksien kuvausta käyttäjän määrittämien kenttien avulla. (Näitä kenttiä ovat esimerkiksi **Muistin koko**, **Kiintolevyn kapasiteetti** ja **Energy Star -merkinnän mukainen**). Microsoft Dynamics 365 for Finance and Operations -sovelluksessa määritteitä voidaan liittää erilaisiin vähittäismyynnin yksiköihin, kuten tuoteluokkiin ja vähittäismyyntikanaviin, ja niille voidaan määrittää oletusarvoja. Tuotteet perivät sitten määritteet ja oletusarvot, kun ne liitetään tuoteluokkiin tai vähittäismyyntikanaviin. Oletusarvot voidaan ohittaa yksittäisen tuotteen tasolla, vähittäismyyntikanavan tasolla tai vähittäismyyntiluettelossa.
 
Tavallisella televisiotuotteella voi olla esimerkiksi seuraavat määritteet.

| Luokka   | Ominaisuus                | Sallitut arvot          | Oletusarvo |
|------------|--------------------------|-----------------------------|---------------|
| TV & Video | Brandi                    | Mikä tahansa voimassa oleva tuotemerkkiarvo       | None          |
| TV         | Näytön koko              | 20–80 tuumaa                | None          |
|            | Vertikaaliresoluutio      | 480i, 720p, 1080i, tai 1080p | 1080p         |
|            | Näytön päivitystaajuus      | 60 Hz, 120 Hz, tai 240 Hz       | 60 Hz          |
|            | HDMI-tuloja              | 0–10                        | 3             |
|            | DVI-tuloja               | 0–10                        | 1             |
|            | Komposiittituloja         | 0–10                        | 2             |
|            | Komponenttituloja         | 0–10                        | 1             |
| LCD-näyttö        | 3D-valmius                 | Kyllä tai Ei                   | Kyllä           |
|            | 3D käytössä               | Kyllä tai Ei                   | En            |
| Plasma     | Toimintalämpötila vähintään      | 0–43 astetta              | 32            |
|            | Toimintalämpötila korkeintaan        | 0–43 astetta              | 100           |
| Projektio | Projektiokuvaputken takuu | 6, 12, tai 18 kuukautta         | 12            |
|            | Projektiokuvaputkien lukumäärä    | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Määritteet ja määritetyypit

Määritteet perustuvat *määritetyyppeihin*. Määritetyyppi osoittaa minkälaista tietoa voi lisätä tiettyyn määritteeseen. Finance and Operations tukee tällä hetkellä seuraavia määritetyyppejä:

- **Valuutta** – Tämä tyyppi tukee valuutta-arvoja. Se voidaan sitoa (eli se voi tukea arvoaluetta) tai se voidaan jättää avoimeksi.
- **DateTime** – Tämä tyyppi tukee päivämäärä- ja aika-arvoja. Se voidaan sitoa tai jättää avoimeksi.
- **Desimaali** – Tämä tyyppi tukee numeerista arvoa, jota sisältää desimaaleja. Se tukee myös mittayksikköä. Se voidaan sitoa tai jättää avoimeksi.
- **Kokonaisluku** – Tämä tyyppi tukee numeerista arvoa. Se tukee myös mittayksikköä. Se voidaan sitoa tai jättää avoimeksi.
- **Teksti** – Tämä tyyppi tukee tekstiarvoa. Se tukee myös etukäteen määritettyä mahdollisten arvojen joukkoa (eli *luettelointia*).
- **Totuusarvo** – Tämä tyyppi tukee binaariarvoa (**tosi** tai **epätosi**).
- **Viite** – Tämä tyyppi viittaa muihin määritteisiin.

### <a name="set-up-attribute-types-in-finance-and-operations"></a>Määritetyyppien määrittäminen Finance and Operationsissa

1. Kirjaudu Finance and Operations -tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Tuotetietojen hallinta** &gt; **Asetukset** &gt; **Luokat ja määritteet** &gt; **Määritetyypit**.
3. Luo kaksi **Teksti**-tyyppistä määritetyyppiä, valitse **Kiinteä luettelo** -asetukseksi **Kyllä** ja lisää sitten arvoluettelo:

    - Anna toisen määritetyypin nimeksi **Linssin muoto** ja lisää seuraavat arvot: **Soikea**, **Neliö** ja **Suorakaide**.
    - Anna toisen määritetyypin nimeksi **Aurinkolasien merkki** ja lisää seuraavat arvot: **Ray ban**, **Aviator** ja **Oakley**.

![Määritetyypit](media/AttributeType.png)

### <a name="set-up-an-attribute-in-finance-and-operations"></a>Määritteen määrittäminen Finance and Operationsissa

1. Kirjaudu tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Tuotetietojen hallinta** &gt; **Asetukset** &gt; **Luokat ja määritteet** &gt; **Määritteet**.
3. Luo määrite, jonka nimi on **Linssi**.
4. Määritä **Määritteen tyyppi** -kentän arvoksi **Linssin muoto**.

![Ominaisuudet](media/Attribute.png)

## <a name="attribute-metadata"></a>Määritteen metatiedot

*Määritteen metatiedoissa* voit valita asetuksia, jotka määrittävät, miten kunkin tuotteen määritteet toimivat. Voit esimerkiksi määrittää, ovatko määritteet pakollisia sekä voiko niitä käyttää hauissa ja suodattimina.

Vähittäismyyntituotteiden määritteiden metatietoasetukset voidaan korvata kanavatasolla. Tätä ominaisuutta käsitellään myöhemmin tässä ohjeaiheessa.

Olet ehkä huomannutkin, että **Määritteet**-sivulla on määritteen metatietoihin liittyviä vaihtoehtoja. **POS:n määritteen metatiedot** -kohdan **Voidaan tarkentaa** -asetus vaikuttaa määritearvojen toimintaan vähittäismyyntipisteessä tai tapaan, jolla järjestelmä käsittelee kyseisiä määritearvoja. Vain määritteet, joiden **Voidaan tarkentaa** -asetukseksi voi valita **Kyllä**, näkyvät vähittäismyynnin myyntipisteessä tuotteiden tarkennusta tai suodatusta varten.

Muut **Määritteet**-sivun määritteen metatietoasetukset:

- Etsittävissä
- Noudettavissa
- Voidaan kysellä
- Lajiteltavissa
- Salli useat arvot
- Ohita kirjainkoko ja muoto
- Täysi vastaavuus

Nämä asetukset oli tarkoitettu alun perin verkkokaupan hakutoimintojen parantamista varten. Vaikka verkkokauppa ei ole heti käytettävissä Finance and Operationsissa, se sisältää eCommerce Publishing Software Development Kitin (SDK). Asiakkaat voivat viedä tuotteita tämän SDK:n avulla valitsemaansa hakuindeksiin. Vaikka tuotetiedot tuodaan, asiakkaiden on silti voitava erottaa toisistaan haettavissa olevat tiedot, tiedot, joissa voidaan tehdä hakuja ja niin edelleen. Tällä tavoin voidaan luoda optimaalinen indeksi, jolla voi varmistaa, että vain *heidän mielestään* indeksoitavat määritteet indeksoidaan.

Lisätietoja edellä mainittujen asetusten tarkoituksesta on kohdassa [SharePoint Server 2013 -hakumallin yleiskatsaus](https://technet.microsoft.com/en-us/library/jj219669.aspx).

## <a name="filter-settings-for-attributes"></a>Määritteiden suodatusasetukset

Voit määrittää määritteiden suodatusasetuksissa, miten määritteiden suodattimet näytetään vähittäismyynnin myyntipisteessä. Voit käyttää määritteen suodatusasetuksia valitsemalla Finance and Operationsin **Määritteet**-sivulla ensin määritteen ja sitten toimintoruudussa **Suodatusasetukset**.

**Suodatuksen näyttöasetukset** -sivulla on seuraavat kentät:

- **Nimi** – Tämä kentän arvo on oletusarvoisesti määritteen nimi. Voit kuitenkin muuttaa arvon.
- **Näyttöasetus** – Seuraavat asetukset ovat käytettävissä:

    - **Yksi arvo** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Totuusarvo**, **Valuutta**, **Desimaali**, **Kokonaisluku** ja **Teksti**. Tällä asetuksella näille määritteille voidaan valita yksi arvo tarkennettavaksi asiakasohjelmassa.
    - **Useita arvoja** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali**, **Kokonaisluku** ja **Teksti**. Tällä asetuksella tälle määritteelle voidaan valita useita arvoja tarkennettavaksi asiakasohjelmassa.

- **Näytön ohjaus** – Seuraavat asetukset ovat käytettävissä:

    - **Luettelo** – Tämä vaihtoehto on kaikkien määritetyyppien käytettävissä.
    - **Alue** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali** ja **Kokonaisluku**. 
    - **Liukusäädin** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali** ja **Kokonaisluku**.
    - **Liukusäädin palkeilla** – Tämä asetus on seuraavien määritetyyppien valittavissa: **Valuutta**, **Desimaali** ja **Kokonaisluku**.

- **Raja-arvo** – Tämä asetus on pakollinen, jos olet valinnut näytön ohjaustyypiksi **Alue**. Voit määrittää arvot käyttämällä puolipistettä (;) erottimena.

    Jos suodattimena on esimerkiksi **Laukkumäärä**, raja-arvo voi olla **10; 20; 50; 100; 200; 500; 1000; 5000**. Siinä tapauksessa seuraavat alueet näkyvät vähittäismyynnin myyntipisteessä. Jos jollakin tulosjoukon alueella ei ole tuotteita, kyseinen alue näkyy himmennettynä.

    - Alle 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 tai enemmän

![Määritteen suodatusasetukset](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Määriteryhmät

Kun määritteet on määritetty, ne voidaan määrittää määriteryhmiin *Määriteryhmää* käytetään komponentin tai alikomponentin yksittäisten määritteiden ryhmittelemiseen tuotemääritysmallissa. Määrite voi sisältyä useisiin määriteryhmiin. Määriteryhmät voivat auttaa käyttäjiä tuotteiden määrityksessä, sillä eri valinnat järjestetään tietyn kontekstin mukaan. Määriteryhmät voidaan määrittää vähittäismyyntiluokkiin tai vähittäismyyntikanaviin.

Voit määrittää oletusarvot myös määriteryhmään sisältyvillä määritteille. Voit esimerkiksi lisätä värin määritteen määriteryhmään ja valita määritteen oletusarvoksi **sinisen**. Kun määriteryhmä sitten lisätään vähittäismyyntituotteeseen, jossa väri on yksi määritteistä, **Sininen** näkyy kyseisen tuotteen oletusvärinä.

![Määriteryhmät](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Luo ominaisuusryhmä

1. Kirjaudu tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Tuotetietojen hallinta** &gt; **Asetukset** &gt; **Luokat ja määritteet** &gt; **Määriteryhmät**.
3. Luo määriteryhmä, jonka nimi on **Merkkiaurinkolasit**.
4. Lisää seuraavat määritteet: **Linssin muoto** ja **Aurinkolasien merkki**.

### <a name="assign-attribute-groups-to-retail-categories"></a>Määriteryhmien määrittäminen vähittäismyyntiluokkiin

Vähintään yksi määriteryhmä voidaan liittää luokkasolmuihin seuraavan tyyppisiä vähittäismyynnin luokkahierarkioissa: Vähittäismyynnin tuotehierarkia, Kanavan siirtymisluokkahierarkia ja Lisätuoteluokkahierarkia. Kun tuotteet sitten luokitellaan, ne perivät määriteryhmiin sisältyvät määritteet.

![Vähittäismyynnin tuotehierarkia – tuotemääriteryhmät](media/AGRetailProdHierarchy.PNG)

Määritä määriteryhmät luokkiin vähittäismyynnin tuotehierarkiassa seuraavasti.

1. Kirjaudu tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Vähittäismyynti** &gt; **Luokka- ja tuotehallinta** &gt; **Vähittäismyynnin tuotehierarkia**.
3. Valitse **muodin siirtymishierarkia**.
4. Valitse **Miesten vaatteet** -kohdassa **Housut**-luokka ja lisää sitten **Tuotemääriteryhmät**-pikavälilehdessä **Miesten vyöt** -määriteryhmä.
5. Valitse **Merkkiaurinkolasit**-luokka ja tarkista **Merkkiaurinkolasit**-määriteryhmän uudet määritteet valitsemalla **Näytä määritteet**.

    Määriteryhmässä pitäisi nyt näkyä uudet **Linssin muoto**- ja **Aurinkolasien merkki** -määritteet.

6. Valitse **Miesten vaatteet** -kohdassa **Housut**-luokka ja tarkista **Miesten vyöt**määriteryhmän määritteet valitsemalla **Näytä määritteet**.

    Määriteryhmässä pitäisi nyt näkyä määritteet **Miesten vyön merkki**, **Vyön materiaali** ja **Vyön koko**.

> [!NOTE]
> Tällä menettelyllä voi määrittää myös määriteryhmiä luokkiin kanavan siirtymisluokkahierarkiaan ja lisätuoteluokkahierarkiaan. Käytä vaiheessa 2 seuraavia siirtymispolkuja:
>
> - **Vähittäismyynti** &gt; **Luokka- ja tuotehallinta** &gt; **Kanavan siirtymisluokat**
> - **Vähittäismyynti** &gt; **Luokka- ja tuotehallinta** &gt; **Lisätuoteluokat**.

### <a name="assign-attribute-groups-to-retail-stores"></a>Määriteryhmien määrittäminen vähittäismyymälöihin

Vähintään yksi määriteryhmä voidaan liittää vähintään yhteen vähittäismyymälähierarkian vähittäismyymälään. Kun tuotteet sitten lisätään tiettyihin vähittäismyymälöihin, ne perivät määriteryhmään sisältyvät määritteet.

1. Kirjaudu tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Kanavaluokat ja tuotemääritteet**.
3. Määriteryhmien määrittäminen Houston-kanavaan:

    1. Valitse **Houston**-kanava.
    2. Valitse **Määriteryhmä**-pikavälilehdessä ensin **Lisää** ja sitten **Nimi**-kentässä **SharePointProvisionedProductAttributeGroup**.
    3. Valitse **Lisää** uudelleen ja valitse sitten **Nimi**-kentässä **Miesten vyöt**.
    4. Valitse **Lisää** uudelleen ja valitse sitten **Nimi**-kentässä **Merkkiaurinkolasit**.

        > [!NOTE]
        > Voit määrittää asetuksen avulla, että kanava perii määriteryhmät ylätason kanavasta hierarkiassa. Jos valitset **Peri**-asetukseksi **Kyllä**, alatason kanavasolmu perii kaikki määriteryhmät ja kaikki kyseisten määriteryhmien määritteet.

4. Määritteiden ottaminen käyttöön Houston-kanavaa varten:

    1. Valitse toimintoruudussa **Määritä määritteen metatiedot**.
    2. Valitse ensin **Muoti**-luokkasolmu ja valitse sitten **Kanavan tuotemääritteet** -pikavälilehdessä kunkin määritteen kohdalla **Sisällytä määrite**.
    3. Valitse ensin **Muodin asusteet** -luokkasolmu, sitten **Merkkiaurinkolasit**-luokka ja lopuksi **Kanavan tuotemääritteet** -pikavälilehdessä kunkin määritteen kohdalla **Sisällytä määrite**.
    4. Valitse ensin **Miesten vaatteet** -luokkasolmu, sitten **Housut**-luokka ja lopuksi **Kanavan tuotemääritteet** -pikavälilehdessä kunkin määritteen kohdalla **Sisällytä määrite**.

![Kanavaluokat ja tuotemääritteet – määriteryhmät](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Määritearvojen ohittaminen

Yksittäisten tuotteiden määritteiden oletusarvot voidaan ohittaa tuotetasolla. Myös sellaisten yksittäisten tuotteiden oletusarvot voidaan ohittaa, jotka ovat tietyissä tiettyihin vähittäismyyntikanaviin suunnatuissa luetteloissa.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Yksittäisen tuotteen määritearvojen ohittaminen

1. Kirjaudu tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Vähittäismyynti** &gt; **Luokka- ja tuotehallinta** &gt; **Vapautetut tuotteet luokittain**.
3. Valitse **Muoti** &gt; **Muodin asusteet** &gt; **Merkkiaurinkolasit**-luokkasolmu.
4. Valitse tarvittava tuote ruudukossa. Valitse sitten toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Tuotemääritteet**.
5. Valitse määrite vasemmassa ruudussa ja päivitä sen arvo oikeassa ruudussa.

![Tuotetiedot-sivu – tuotemääriteryhmät](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Luettelon tuotteiden määritearvojen ohittaminen

1. Kirjaudu tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Vähittäismyynti** &gt; **Luettelon hallinta** &gt; **Kaikki luettelot**.
3. Valitse **Fabrikamin perusluettelo** -luettelo.
4. Valitse **Muoti** &gt; **Muodin asusteet** &gt; **Merkkiaurinkolasit**-luokkasolmu.
5. Valitse **Tuotteet**-pikavälilehdessä tarvittava tuote ja valitse sitten **Määritteet** tuoteruudukon yläpuolella.
6. Päivitä tarvittavien määritteiden arvot seuraavissa pikavälilehdissä:

   - Jaettu tuotemedia
   - Yhteiset tuotemääritteet
   - Kanavamedia
   - Kanavan tuotemääritteet

     > [!NOTE]
     > Jos Finance and Operationsissa luodaan jaettu tuotemedia ja jaettuja tuotemääritteitä, niitä käytetään kaikkiin vähittäismyyntituotteisiin.

![Luettelon tuotemääriteryhmät](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Kanavan tuotteiden määritearvojen ohittaminen

1. Kirjaudu tausta-asiakasohjelmaan vähittäismyynnin myynninedistämispäällikkönä.
2. Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Kanavaluokat ja tuotemääritteet**.
3. Valitse **Houston**-kanava.
4. Valitse **Tuotteet**-pikavälilehdessä tarvittava tuote ja valitse sitten **Määritteet** tuoteruudukon yläpuolella.

    > [!NOTE]
    > Jos tuotteita ei ole käytettävissä, lisää tuotteita valitsemalla **Lisää** **Tuotteet**-pikavälilehdessä ja valitsemalla sitten tarvittavat tuotteet **Lisää tuotteita** -valintaikkunassa.

5. Päivitä tarvittavien määritteiden arvot seuraavissa pikavälilehdissä:

   - Jaettu tuotemedia
   - Yhteiset tuotemääritteet
   - Kanavamedia
   - Kanavan tuotemääritteet

     > [!NOTE]
     > Jos Finance and Operationsissa luodaan jaettu tuotemedia ja jaettuja tuotemääritteitä, niitä käytetään kaikkiin vähittäismyyntituotteisiin.

