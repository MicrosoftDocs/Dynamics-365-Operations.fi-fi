---
title: Konsolidoitujen raporttien laatiminen
description: Tässä ohjeaiheessa käsitellään erilaisia skenaariota, joissa konsolidoituja raportteja voidaan laatia.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 76e675373212195cbe3f6cf43d128b2104f92fc6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "355193"
---
# <a name="generate-consolidated-financial-statements"></a>Konsolidoitujen raporttien laatiminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään erilaisia skenaariota, joissa konsolidoituja raportteja voidaan laatia.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Yksi- ja monitasoiset yritysten väliset konsolidoinnit
Yksinkertaisin raportteja hyödyntävä konsolidointimenetelmä on koota raporttipuiden avulla tietoja samaa tilikarttaa ja tilikautta käyttävistä yrityksistä. Yleistasolla raporttipuuta käyttävä konsolidointi sisältää seuraavat vaiheet.

1. Luo rivin määritys ja varmista, että rivit sisältävät kaikkien yritysten kaikki soveltuvat tilit.
2. Luo sarakkeen määritys, joka sisältää kaikki luotavaan raporttiin tarvittavat sarakkeet.
3. Luo raporttipuu, joka sisältää raporttisolmun kullekin konsolidointiraportissa käytetylle yritykselle.

> [!TIP]
> Lisätietoja rivin ja sarakkeen määritysten sekä raporttipuiden luomisesta ja hallinnasta on kohdassa [Raportin komponentit](../../dev-itpro/analytics/financial-report-components.md).

Seuraava kuva näyttää, miten raporttien raporttipuun määrityksellä voi tunnistaa kunkin konsolidoitavan yrityksen.

![Raporttipuun määritykset](./media/reporting-tree-definition.png "Raporttipuun määritykset")

Seuraavan kuvan konsolidoitu raportti näyttää, miten kutakin yritystä voi tarkastella erikseen, kun raporttipuuta ja raportin määritystä käytetään yhdessä. Konsolidoidut summat näytetään yhteenvetotasolla.

![Konsolidoidun summan yhteenvetotaso](./media/consolidate-amount-summary-level.png "Konsolidoidun summan yhteenvetotaso")

Voit luoda myös monitasoisen raporttipuun, joka sisältää tarvittavan määrän tasoja. Seuraavassa kuvassa on monitasoinen raporttipuun määritys, jossa koonti tapahtuu koko maailman alueiden mukaan.

![Monitasoinen raporttipuun määritys aluekohtaisilla koonneilla](./media/multilevel-reporting-tree-definition-roll-ups%20-worldwide-region.png "Monitasoinen raporttipuun määritys aluekohtaisilla koonneilla")

Seuraavassa kuvassa on monitasoinen raporttipuun määritys, jossa koonti tapahtuu toiminnon mukaan.

![Monitasoinen raporttipuun määritys toimintokohtaisilla koonneilla](./media/multilevel-reporting-tree-definition-roll-ups%20-by-function.png "Monitasoinen raporttipuun määritys toimintokohtaisilla koonneilla")

### <a name="viewing-companies-side-by-side"></a>Yritysten tarkastelu rinnakkain
Monet asiakkaat käyttävät mielellään raportteja, joissa yritykset näkyvät rinnakkain ja joissa konsolidoitu kokonaissumma näkyy sarakkeessa. Tämä muoto on helppo toteuttaa raporttipuun luonnin jälkeen. Yleistasolla konsolidoitujen raporttien yritysten näyttäminen rinnakkain sisältää seuraavat vaiheet.

1. Luo sarakkeen määritys, jossa jokaisella yrityksellä on **Taloushallinnon dimensio** -sarake.
2. Valitse kunkin sarakkeen puu ja raporttiyksikkö **Raporttiyksikkö**-kentän avulla.
3. Valinnainen: lisää otsikot ja kokonaissummasarakkeet.

Seuraavassa kuvassa on sarakkeen määritys rinnakkaismuodossa.

![Sarakkeen määritys rinnakkaismuodossa](./media/column-definition-side-by-side-format.png "Sarakkeen määritys rinnakkaismuodossa")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Yrityksistä luotuja organisaatiorakenteita käyttävät konsolidoinnit
Dimensioita tai yrityksiä sisältävät organisaatiohierarkiat luovat dynaamisesti taloushallinnon raportoinnin raporttipuun määritykset. Konsolidointeja voi yksinkertaistaa kätevästi lisäämällä organisaatiohierarkian taloushallinnon raportoinnin raporttiin. Taloushallinnon raportointi valitsee raportin päivämäärän perusteella organisaatiohierarkian voimaantulopäivänä tai sitä ennen, kuten seuraavassa kuvassa.

![Raporttipuun määrityksen luonti dynaamisesti](./media/dynamically-create-reporting-tree-definitions.png "Raporttipuun määrityksen luonti dynaamisesti")

## <a name="consolidations-that-involve-eliminations"></a>Eliminointeja sisältävät konsolidoinnit
Eliminointitapahtumat ovat yleinen osa konsolidointiprosessia. Tässä esimerkissä viisi tiliä eliminoidaan konsolidoinnin aikana: 142600, 211400, 401420, 401180 ja 510820. Yritykset voivat määrittää konsernin sisäiset tilit eri tavalla. Joillakin yrityksillä tilin viimeinen numero on esimerkiksi 9, jos tiliä käytetään konsernin sisäisissä tapahtumissa. Jos tiedät konsernin sisäiset tilit, voit menetelmästä riippumatta näyttää eliminoinnit konsolidoiduissa raporteissa.

Seuraavassa kuvassa on konsolidoidun tuloslaskelman sarakemääritys. Kolme konsernin sisäistä tulostiliä on määritetty kullekin tilille dimensiosuodattimen avulla. Sarake D sisältää vain yrityksen USMF eliminointitilit ja sarake E vain yrityksen DEMF eliminoinnit. Sekä sarake D että sarake E on määritetty siten, että niitä **ei** tulosteta raporttiin.

![Konsolidoidun tuloslaskelman sarakemääritys](./media/column-definition-consolidated-income-statement.png "Konsolidoidun tuloslaskelman sarakemääritys")

Kun raportti laaditaan, eliminointisummat lasketaan sarakkeissa F, G ja H, ja yhteenlaskettu summa on sarakkeessa I. Konsolidoidut summat ovat sarakkeessa J. Nämä konsolidoidut summat eivät sisällä yritysten USMF, USRT ja DEMF eliminointeja.

> [!TIP]
> Luo toinen, vain eliminointimerkinnät näyttävä raportti ja käytä sitä konsolidoidun iraportin sisältävässä raporttiryhmässä. Tällä tavoin saat käyttöösi kaikki tiedot, joita tarvitset tarvittavien kirjauskansiovientien luontiin.

Seuraavassa kuvassa on konsolidoitu raportti.

![Konsolidoidun raportin tuloslaskelma](./media/consolidated-report-income-statement.png "Konsolidoidun raportin tuloslaskelma")

Riippumatta siitä käytätkö tilejä, dimensioita tai molempia, eliminointimerkinnät voidaan suodattaa taloushallinnon raportoinnissa pois dimension suodatustoiminnoilla.

## <a name="minority-interest"></a>Vähemmistöosuus
Yritys voi omistaa osan toisesta yrityksestä. Kun muodostat tässä tilanteessa konsolidoitua raporttia, on tärkeää ottaa huomioon vain yrityksen omistama osuus. Taloushallinnon raportoinnissa on useita, käyttäjän asetusten mukaan määräytyviä tapoja, joilla vähemmistöosuus näytetään. Yksi tapa on käyttää koonnin prosenttiosuutta raporttipuun määrityksessä. Toisessa tavassa vähemmistöomistaja näytetään raportissa erillisellä rivillä.

### <a name="using-the-reporting-tree-definition"></a>Raporttipuun määrityksen käyttäminen
Anna raporttipuun määrityksessä omistusosuus **Koontiprosentti**-sarakkeessa (sarake H), kuten seuraavassa kuvassa. Kun raportti laaditaan, tämä konsolidoitu summa lasketaan tämän prosenttiosuuden perusteella. Tässä esimerkissä Contoson omistusosuus Contoso Germanysta on vain 80 prosenttia. Voit antaa **Koontiprosentti**-sarakkeessa joko **80** tai **,8**, jonka jälkeen 80 prosenttia kootaan konsolidoidulle tasolle.

> [!NOTE]
> Voit käyttää tätä omistusosuutta missä tahansa raporttiyksikössä myös muualla kuin yritystasolla. 

![Raporttipuun määrityksen prosenttiosuuden käyttäminen](./media/Using-reporting%20tree-definition-percentage.png "Raporttipuun määrityksen prosenttiosuuden käyttäminen")

Kun raportti laaditaan, Contoso Germany -raportti näyttää 100 prosenttia myyntisummasta. 80 prosenttia tästä summasta kohdistetaan ja kootaan myynnin konsolidoidulle tasolle.

Jos yrityksen omistusosuus on alle 1 prosenttia, voit valita **Salli alle 1 prosentin koonti** -valintaruudun **Raporttiasetukset**-sivun **Lisäasetukset**-välilehdessä, kuten seuraavassa kuvassa. Siinä tapauksessa raporttipuun **Koontiprosentti**-sarakkeen arvoja käsitellään siten kuin ne olisivat alle 1 prosenttia. Jos esimerkiksi annat arvon **,8**, konsolidoidulle tasolle kootaan 0,8 eikä 80 prosenttia. Saat saman tuloksen myös jättävät **Salli alle 1 prosentin koonti** -valintaruudun valitsematta ja antamalla arvon **,008** **Koontiprosentti**-sarakkeessa.

![Raporttiasetuksen vaihtoehdot](./media/reporting-setting-options.png "Raporttiasetuksen vaihtoehdot")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Omistajuuden näyttäminen konsolidoidun raportin erillisellä rivillä
Toinen vaihtoehto vähemmistöosuuden näyttämiseen on tytäryhtiön 100 prosenttia raportin jokaisella rivillä mutta vähentää vähemmistöosuus nettotuotosta.

Kuten seuraavassa kuvassa näytetään, vähemmistöosuuden voi laskea raporteissa käyttämällä rivimäärityksen **IF THEN ELSE** -lauseketta ja sarakerajoitusta.

![Omistusosuuden näyttäminen konsolidoidun raportin erillisellä rivillä](./media/Showing-ownership-separate-row-consolidated-report.png "Omistusosuuden näyttäminen konsolidoidun raportin erillisellä rivillä")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Useita yritysten välisiä tilikarttoja
Vaikka eri yrityksillä on usein erilaiset tilikartat, niille kuitenkin halutaan muodostaa konsolidoituja raportteja. Tässä tapauksessa tiedot voidaan konsolidoida taloushallinnon raportoinnin avulla, jonka jälkeen voit laatia konsolidoituja raportteja. Yleistasolla erilaisia tilikarttoja käyttävien yritysten konsolidointi sisältää seuraavat vaiheet.

1. Luo rivimääritys, jossa on useita linkkejä taloushallinnon dimensioihin. Jokaiseen tilikarttaa on oltava yksi linkki.
2. Määritä kullekin yritykselle sarake käyttämällä sarakemäärityksen raporttiyksikön rajoitusta.


Kun yksittäisen yrityksen tilikartan rivimäärityksessä kullekin riville voidaan lisätä useita linkkejä taloushallinnon dimensioihin. Seuraavassa kuvassa USMF-yritys käyttää ensimmäisen **Linkki taloushallinnon dimensioihin** -sarakkeen (sarake J) tilijoukkoa, kun taas DEMF-yritys käyttää toisen **Linkki taloushallinnon dimensioihin** -sarakkeen (sarake K) tilejä.

> [!TIP]
> Lisätietoja **Linkki taloushallinnon dimensioihin** -solusta on kohdassa Taloushallinnon dimensiot -solulinkin määrittäminen.

![Tilien ensimmäisen taloushallinnon dimensiolinkin määrittäminen](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Tilien ensimmäisen taloushallinnon dimensiolinkin määrittäminen")

Voit määrittää raporttipuun avulla, mitä rivimäärityksen linkkiä taloushallinnon dimensioihin käytetään kunkin yrityksen yhteydessä. Valitse rivimääritys sarakkeessa E ja valitse sitten sopiva rivilinkki sarakkeessa F, kuten seuraavassa kuvassa.

![Käytetty rivimäärityksen taloushallinnon dimensioiden linkki](./media/link-financial-dimensions-row-definition-used.png "Käytetty rivimäärityksen taloushallinnon dimensioiden linkki")

> [!TIP]
> Kun luot linkkejä taloushallinnon dimensioihin, käytä kuvauksia, sillä niiden avulla tunnistetaan yritykset, joita kunkin yrityksen kanssa käytetään. Tämä helpottaa oikean yrityksen valitsemista rapottipuuta luotaessa. Sarakemäärityksen **Raporttiyksikkö**-kentän avulla voit rajoittaa kunkin sarakkeen johonkin raporttipuun yksikköön, joten voit tarkastella tietoja rinnakkain. Jos et liitä sarakkeeseen tiettyä yritystä, kaikkien yritysten konsolidoidut tiedot näytetään.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Erilaiset kirjanpidon kalenterit useiden yritysten välillä
Vaikka eri yrityksillä voi olla erilaiset kirjanpidon vuosikalenterit, niille on kuitenkin muodostettava konsolidoituja raportteja. Yritysten erilaiset tilikaudet voidaan konsolidoida kahdella tavalla:

- Luo sarakemääritys ja käytä kautta ja vuotta tekemään yhdistämismääritys kunkin yrityksen soveltuviin kausiin.
- Valitse ensin **Asetukset** \> **Muu** \> **Lisäasetukset** ja valitse sitten, tehdäänkö konsolidointi kauden päättymispäivän vai kauden numeron avulla.

Kun suunnittelet sarakemääritystä useille yrityksille, joiden tilikaudet ovat erilaiset, on tärkeää ottaa huomioon, mikä yritys määritetään raportin määrityksen **Yrityksen nimi** -kenttään. Kyseisen yrityksen kirjanpidon vuosikalenteria käytetään raportin määrityksen kirjanpidon vuosikalenteriperustana. Seuraavassa taulukossa on esimerkkinä USMF- ja INMF-yritysten tilikausimääritykset. Konsolidoiduissa raporteissa käytetään USMF-yrityksen käyttämään kirjanpidon vuosikalenteria. Yhdistämismääritys-sarakkeessa on kunkin yrityksen vastaava kausi ja vuosi, jos raportti on laadittu 30.6.2018.

| Yritys    | Tilikausi                                  | Kartoitus                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Tilikausi, 1.7.–30.6.          | Kausi 12, tilikausi 2018 | 
| INMF      | Kalenterivuosi, 1.1.–31.12. | Kausi 6, tilikausi 2018  |

Seuraavassa kuvassa USMF-yritys on määritetty raportin määrityksen **Yrityksen nimi** -kentässä. Tämän vuoksi USMF-yrityksen kirjanpidon vuosikalenteria käytetään kirjanpidon vuosikalenteriperustana. Kun tässä esimerkissä raportti laaditaan 30.6.2018, USMF-yritys käyttää BASE-kautta, joka on määritetty raportin määrityksessä kaudeksi 12. INMF-yritys käyttää kautta BASE–6, joka on kausi 6. Kummassakin sarakkeessa on kesäkuun 2018 tiedot.

![Raportin peruskausi](./media/report-base-period.png "Raportin peruskausi")

Seuraavassa kuvassa on raportin määrityksen asetukset, joilla voit valita, käytetäänkö konsolidoinnissa kauden numeroa vai kauden päättymispäivää.

![Raportin määrityksen jaksonumeroon asetukset](./media/options-report-definition-period-number.png "Raportin määrityksen jaksonumeroon asetukset")

## <a name="business-unit-consolidations"></a>Liiketoimintayksikön konsolidoinnit
Tässä ohjeaiheessa on keskitetty raporttipuun määritysten ja organisaatiohierarkioiden käyttöön konsolidoinnissa taloushallinnon raportoinnissa. Voit luoda raporttipuun myös liiketoimintayksikön konsolidointiraportteja, kuten raportteja maailmanlaajuisesti myynnistä tai toiminnoista. Nämä raportit ovat yleinen vaatimus. Voit luoda ne valitsemalla kullekin konsolidoitavalle yksikölle yrityksen ja dimension. Esimerkiksi seuraavassa kuvassa liiketoimintayksikön koonti suoritetaan toistamalla jokainen yritys **Yritys**-sarakkeessa (sarake A) ja määrittämällä yrityskohtainen osaston dimensioarvojen ryhmä **Dimensiot**-sarakkeessa (sarake D).

![Liiketoimintayksikön konsolidointiraportit](./media/business-unit-consolidation-reports.png "Liiketoimintayksikön konsolidointiraportit")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Useita raportointivaluuttoja sisältäviä konsolidointeja
Taloushallinnon raportointia voi käyttää entistä joustavammin toteutuneiden, budjetoitujen, budjetin hallinnan ja budjetin suunnittelutietojen tarkasteluun useissa valuutoissa. Koska keskeiset asetustiedot tuodaan mukana, taloushallinnon raportoinnissa ei tarvitse tehdä lisämäärityksiä raporttien katsomista varten valuutasta, ajankohdasta ja käyttäjästä riippumatta.

### <a name="prerequisites"></a>Edellytykset
Jotta muunnetut saldot voitaisiin laskea oikein, taloushallinnon raportointi edellyttää, että **kerrytystililuokka** määritetään **Päätili**-luettelon kerrytystilille. Taloushallinnon raportointi ei tue kirjausta kerrytystilille. Jos tapahtuma kirjataan kerrytystilille, muunnettuja saldoja ei voi laskea oikein. Käyttäjiä suositellaan määrittämään lisäkerrytystili, johon kerrytystilin oikaisut kirjataan.

Päätilin **Taloushallinnon raportointi** -pikavälilehden **Talousraportoinnin vaihtokurssin tyyppi**- ja **Valuutan muuntotyyppi** -kentät on määritettävä kullekin tilille seuraavassa kuvassa näkyvällä tavalla. Voit tehdä tämän tehtävän tili kerrallaan tai voit ottaa muutokset kätevästi käyttöön tilimalleja käyttämällä.

- Valitse **Talousraportoinnin vaihtokurssin tyyppi** -kentässä vaihtokurssin tyyppi, joka sisältää tilillä käytettävät valuutat ja vaihtokurssit. Tätä valuutta- ja vaihtokurssitaulukkoa käytetään toteutuneisiin tietoihin taloushallinnon raportoinnissa.
- Valitse **Valuutan muuntotyyppi** -kentässä menetelmä, jolla tilin vaihtokurssit lasketaan. Tätä valuuttamenetelmää käytetään taloushallinnon raportoinnissa sekä toteutuneissa että budjetin tiedoissa.

![Taloushallinnon raportoinnin päätilit](./media/Financial-reporting-main-accounts.png "Taloushallinnon raportoinnin päätilit")

Budjetin, budjetin hallinnan ja budjetin suunnittelun tietojen vaihtokurssin tyyppi on määritetty **Kirjanpito**-sivulla. Tästä taulukosta noudetaan vaihtokurssit ja käytettävälle tilille määritetty valuutan muuntotyyppi.

### <a name="currency-translation-methods"></a>Valuutan muuntomenetelmät
Vaihtokurssit voidaan laskea taloushallinnon raportoinnissa neljällä tavalla:

- **Painotettu keskiarvo** – Tätä menetelmää käytetään useimmiten tulostileillä. Siinä käytetään seuraavaa kaavaa:

    (Vaihtokurssi × Päivien määrä, jonka voimassa) ÷ Kauden päivät

- **Keskimääräinen** – Tätä on vaihtoehtoinen menetelmä tulostileille. Siinä käytetään seuraavaa kaavaa:

    Vaihtokurssit yhteensä ÷ Vaihtokurssien määrä

- **Valittu** – Tätä menetelmää käytetään useimmiten tasetileillä. Käytetty vaihtokurssi on taloushallinnon raportoinnin raportin tai sarakkeen päivämäärä tai sitä edeltävä päivämäärä.
- **Tapahtumapäivä** – Tätä menetelmää käytetään käyttöomaisuuden tileillä. Käytettävä vaihtokurssi on sen päivän kurssi, jolloin käyttöomaisuus hankittiin. Jos kyseisen päivän kurssia ei ole annettu, käytetään aiempaa kurssia, joka on lähinnä käyttöomaisuuden hankintapäivämäärää.

### <a name="report-designer-options-for-currency-translation"></a>Valuutan muunnon asetukset raportin suunnittelutoiminnossa
Taloushallinnon raportoinnissa mikä tahansa raportti voidaan näyttää niin monessa raportointivaluutassa kuin on tarpeellista. Seuraavat raportin määrityksen kentät tukevat tätä ominaisuutta:

- **Raportin määritys** -sivun **Valuuttatiedot**-osa. Tässä osassa näkyy valuutta, jolla arvot näytetään, kun raportti muodostetaan.
- Uusi **Sisällytä kaikki raportointivaluutat** -valintaruutu. Kun tämä valintaruutu on valittu, kullekin raportointivaluutalle lisätään raportti raporttijonoon sen jälkeen, kun yrityksen perusvaluuttaa käyttävä raportti on muodostettu. Jos valintaruutua ei ole valittu, raportointivaluutta on edelleen valittava verkkokatseluohjelmassa. Siinä tapauksessa raportointivaluutta käsitellään vasta, kun valitset sen.

Raportin määrityksen asetusten avulla on helppo muuntaa raportti kaikille raportointivaluutoille. Niinpä voitkin ehkä eliminoida sellaiset raportin määrityksen kaksoiskappaleet, joiden ainoa ero on käytetty valuutta. Jos tarvitse raportin, jossa on näkyvissä useita valuuttoja rinnakkain, voit jatkaa **Sarakemääritys**-sivun **Valuutan näyttö** -kentän käyttöä ja muuntaa vain raportin kyseisen sarakkeen valuttu vaihtoehtoiseksi raportointivaluutaksi.

### <a name="currency-translation-adjustment"></a>Valuutan muunnon oikaisu
Valuutan muunnon oikaisu (CTA) on tasetilien laskennassa käytettyjen kurssien ja tuloslaskelmatileillä käytetyn kurssin välinen ero. Tämä ero voi aiheuttaa sen, että tasetili ei täsmää. Voit laskea valuutan muunnon oikaisun taloushallinnon raportoinnissa kahdella tavalla:

- Käytä rivimäärityksen **Pyöristysoikaisut**-sivua, kuten seuraavassa kuvassa.

    ![Valuutan muunnon oikaisun pyöristysoikaisut](./media/Currency-translation-adjustment-rounding-adjustments.png "Valuutan muunnon oikaisun pyöristysoikaisut")

    Kun määrität rivin, joka näyttää pyöritysoikaisun (valuutan muunnon oikaisu), kokonaiskäyttöomaisuuden rivin, kokonaisvelan ja -pääoman rivin sekä raja-arvon, jonka hyväksyt, taloushallinnon raportointi laskee eron ja siirtää sen halutulle riville. **Pyöristysoikaisu**-rivi luodaan ja se näytetään porautumisen yhteydessä seuraavassa kuvassa esitetyllä tavalla.

    ![Pyöristysoikaisuun porautuminen](./media/rounding-adjustment-drill-down.png "Pyöristysoikaisuun porautuminen")

- Kaikkien tilien pitäisi olla valittavissa varoitus kuluihin. Kuten seuraavassa kuvassa näyttään, ero on sama summa kuin pyöristysoikaisussa (valuutan muunnon oikaisu). Voitkin käyttää sitä kokonaissumman tarkistuksena ja varmistamassa, että pyöristysoikaisusivu ei sisällytä mitään puuttuvia tilin saldoja.

    ![Pyöristysoikaisun muodon tarkistus](./media/rounding-adjustment-form-check.png "Pyöristysoikaisun muodon tarkistus")

### <a name="balance-calculation-approach"></a>Saldo laskentamenetelmä
Jos valuuttoja käytettäessä saataisiin oikein muunnetut summat, taloushallinnon raportointi käyttää seuraavia saldojen laskentamenetelmiä:

- **Painotettu keskiarvo ja keskimääräinen** – jokaisen kauden painotettu keskiarvo lasketaan ja sarakkeet, kuten neljännesvuosittain ja kuluva vuosi, lasketaan yhteen.
- **Historiallinen** – Kaikki historiallista muuntotapaa käyttävä menetelmä palaa tapahtumapäivään. Jos hankintapäivä on liitetty tapahtumaan, vaihtokurssi haetaan kyseisen päivämäärän avulla. Jokainen kausi lasketaan sitten yhteen ja tallennetaan, mikä nopeuttaa laskentaa.
- **Valittu** – Lasketut ja yhteenlasketut sarakkeet, kuten neljännesvuosittain ja kuluva vuosi, lasketaan yhteen spot-kurssilla, joka määritetään sarakkeessa tai raportissa. Esimerkiksi **Vuosineljännes 1** -sarake käyttää maaliskuun 31. päivän kurssia, jos käytössä on kalenterivuosi.

## <a name="additional-resources"></a>Lisäresurssit

Lisätietoja konsolidoinnista ja valuutan muuntamisesta on tämän ohjeaiheen pääaiheessa [Taloushallinnon konsolidoinnit ja valuutan muunto](./financial-consolidations-currency-translation.md).

Lisätietoja konsolidointitietojen antamisesta verkossa on kohdassa [Konsolidoi verkossa](./consolidate-online.md).
