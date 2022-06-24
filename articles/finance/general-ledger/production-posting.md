---
title: Tuotantotilauksen kirjaus
description: Tässä artikkelissa on tietoja tuotantotilausten erilaisista kirjauksista.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d41725325a82b24c1e5aa6bd2c1a5322f3078ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879621"
---
# <a name="production-postings"></a>Tuotannon kirjaukset

Tässä artikkelissa on tietoja tuotantotilausprosessin erityyppisistä kirjauksista.


## <a name="material-consumption"></a>Materiaalikulutus

Materiaalit kirjataan kulutetuiksi tuotannon aikana, kun tuotannon keräysluettelon kirjauskansio kirjataan. Tämä prosessi luo tapahtumia, jotka vähentävät käytettävissä olevaa varastoa. **Tuotantoparametreissä** voit määrittää, kirjataanko käynnissä olevien raaka-aineiden (keskeneräiset työt, KET) arvo kirjanpitoon.

Käynnissä olevien raaka-aineiden arvo (KET) kirjataan tileille **Arvioitu kulutettujen materiaalien kustannus** ja **Arvioitu kulutettujen materiaalien kustannus, KET**. Tuotantotilauksen keräysluetteloprosessi on tuotantotilaukseen liittyvien varastotapahtumien fyysinen päivitys. Kun tuotantotilaus rekisteröidään päättyneeksi, fyysiset tapahtumat palautetaan ja liittyvät varastotapahtumat päivitetään kirjanpitoon. Kun päättyvä kirjauskansio kirjataan, käytetään kirjaustyyppejä **Kulutettujen materiaalien kustannus** ja **Kulutettujen materiaalien kustannus, KET**.

**Varastokirjausprofiilit**-sivun **Tuotanto**-välilehden avulla voit hallita, miten tuotantotilaukset kirjataan kirjanpitoon. Tätä käytetään, kun **Kirjaus kirjanpitoon** -kenttä on määritetty arvoon **Nimike ja resurssi** tai **Nimike ja luokka** **Tuotannonhallinnan parametrit** -sivulla. 

Jotta keräysluettelon kirjauskansio kirjattaisiin tuotantotilauksen kirjanpitoon, seuraavien ehtojen on täytyttävä:

-   **Kirjaa keräysluettelo kirjanpitoon** -valintaruutu on valittava **Tuotannonhallinnan parametrit** -sivulla. Asetuksen voi ohittaa tietyn toimipaikan osalta **Tuotannonhallinnan parametrit toimipaikan mukaan** -sivulla.
-   **Kirjaa varastotilanne** -valintaruutu on valittava **Nimikemalliryhmät**-sivulla ostotilausrivillä valitulle nimikkeelle.
-   **Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:
    -   **Arvioitu kulutettujen materiaalien kustannus**
    -   **Arvioitu kulutettujen materiaalien kustannus, KET**

## <a name="time-consumption"></a>käytetty aika.

**Reitityskorttikirjauskansioon** tai **työkorttikirjauskansion** kirjataan aika, jonka työntekijät käyttävät tuotantotöihin. Kun nämä kirjauskansiot kirjataan, järjestelmä suorittaa kirjauksen keskeneräisiin töihin (KET) kuuluvien resurssien kohdennetulle tilille. Tämä kirjaus edustaa tuotantotilaukseen kuluvalle ajalle kuuluvaa arvoa. Kun tuotantotilaus kirjataan päättyneeksi, KET-tilit täsmäytetään.

On kolme mahdollista tapaa kirjata ajan kulutus riippuen vaihtoehdosta, joka on valittu **Kirjaus kirjanpitoon** -kentässä **Tuotannonhallinnan parametrit** -sivulla.

## <a name="reporting-finished-goods-and-error-quantities"></a>Valmiiden tuotteiden ja virheiden määrien raportointi

Kun tuotantotilaus **ilmoitetaan valmiiksi**, valmiiden tavaroiden määrä päivitetään Varastonhallintaan **Ilmoitettu valmiiksi** -kirjauskansion kautta. Jos käytät KET-kirjanpitoa, kirjanpidon kirjauskansio kirjataan, jotta KET-tilejä voidaan vähentää ja valmiiden tavaroiden varastoa voidaan lisätä. Kirjauskansio käyttää tuotteelle määritettyä vakiokustannusta. Jos **Käytä arvioitua kustannushintaa** -vaihtoehto on valittu **Tuotannonhallinnan parametrit** -sivulla, käytetään tuotantotilauksen arvioitua kustannusta.

Käynnissä olevien raaka-aineiden arvo (KET) kirjataan tileille **Arvioitu valmistuskustannus** ja **Arvioitu valmistuskustannus, KET**. **Ilmoita valmiiksi** -prosessi on tuotantotilaukseen liittyvien varastotapahtumien fyysinen päivitys. Kun tuotantotilaus on päättynyt, fyysiset tapahtumat palautetaan ja liittyvät varastotapahtumat päivitetään kirjanpitoon. Kun päättyvä kirjauskansio kirjataan, käytetään kirjaustyyppejä **Valmistuskustannus** ja **Valmistuskustannus, KET**.

**Varastokirjausprofiilit**-sivun **Tuotanto**-välilehden avulla voit hallita, miten tuotantotilaukset kirjataan kirjanpitoon. Tätä käytetään, kun **Kirjaus kirjanpitoon** -kenttä on määritetty arvoon **Nimike ja resurssi** tai **Nimike ja luokka** **Tuotannonhallinnan parametrit** -sivulla. **Kirjanpito - Nimikkeet** -pikavälilehteä **Tuotantoryhmät**-sivulla voi myös käyttää tuotantotilausten kirjausten hallintaan, kun kenttä on määritetty arvoon **Tuotantoryhmät**.

Jotta **Ilmoita valmiiksi** -kirjauskansio kirjattaisiin tuotantotilauksen kirjanpitoon, seuraavien ehtojen on täytyttävä:
-   **Kirjaa Ilmoita valmiiksi kirjanpitoon** -valintaruutu on valittava **Tuotannonhallinnan parametrit** -sivulla. Asetuksen voi ohittaa tietyn toimipaikan osalta **Tuotannonhallinnan parametrit toimipaikan mukaan** -sivulla.
-   **Kirjaa varastotilanne** -valintaruutu on valittava **Nimikemalliryhmät**-sivulla ostotilausrivillä valitulle nimikkeelle.
-   **Varastokirjausprofiili**-sivulla on määritettävä päätilit seuraaville kirjaustyypeille:
    -   **Arvioitu valmistuskustannus**
    -   **Arvioitu valmistuskustannus, KET**

## <a name="ending-the-production-order"></a>Tuotantotilauksen päättäminen

Ennen tuotantotilauksen lopettamista lasketaan tuotetun määrän toteutuneet kustannukset. Kaikki arvioidut materiaali-, työ- ja yleiskustannukset palautetaan ja korvataan toteutuneilla kustannuksilla. Valmiin nimikkeen kokonaiskustannukset veloitetaan **Valmistuskustannus**-tililtä ja hyvitetään **Valmistuskustannus, KET** -tilille. Materiaalit, jotka kulutettiin tuotantotilauksen aikana, hyvitetään **Kulutettujen materiaalien kustannus** -tilille ja veloitetaan **Kulutettujen materiaalien kustannus, KET** -tililtä.

Jos valitset **Lopeta työ** -valintaruudun suorittaessasi kustannuslaskennan, tuotantotilauksen tilaksi vaihdetaan **Päättynyt**. Tämä tila estää lisäkustannusten kirjaamisen vahingossa valmiiseen tuotantotilaukseen. Voit määrittää valmiiksi ilmoittamisen aikana raportoitavan virhemäärien arvon kohdistettavaksi ilmoitettuihin hyviin määriin. Vaihtoehtoisesti voit määrittää, että virheelliset määrät kirjataan kohdistetulle hävikkitilille. 

Määrittele erityinen hävikkitili seuraavasti:
1.  Siirry kohtaan **Tuotannonhallinta** > **Asetukset** > **Tuotannonhallinnan parametrit**.
2.  Valitse **Vakiopäivitys**-välilehti.
3.  Valitse **Hävikkimenetelmä**-kentässä **Hävikkitili**.
4.  Valitse **Hävikkitili**-kentässä päätili, johon virhemäärän hävikki kirjataan, kun tuotantotilaus on päättynyt. Valitse esimerkiksi kulutili 510380: tuotannon hävikki.

Jotta päättyvä kirjauskansio kirjattaisiin tuotantotilauksen kirjanpitoon, seuraavien ehtojen on täytyttävä:
-   Päätilit on määritettävä **Varastokirjausprofiili**- tai **Tuotantoryhmät**-sivulla seuraavia kirjaustyyppejä varten:
    -   **Kulutettujen materiaalien kustannus**
    -   **Kulutettujen materiaalien kustannus, KET**
    -   **Valmistuskustannus**
    -   **Valmistuskustannus, KET**
-   Päätilit on määritettävä **Kustannusluokat**-, **Resurssit**- tai **Resurssiryhmät**-sivulla seuraavia tyyppejä varten:
    -   **Valmistuksen absorboitu kustannushinta**
    -   **Kulutetun valmistuksen kustannus, KET**

## <a name="indirect-costs-for-production-orders"></a>Tuotantotilausten välilliset kustannukset

Kun käsittelet tuotantotilauksen tapahtumia, voit konfiguroida välilliset kustannukset niin, että yleiskustannukset tai lisämaksut siepataan kirjanpitoon. Välillisten kustannusten fyysiset tapahtumat huomioidaan varastossa, kun kirjaat keräyslistan kirjauskansion tai ilmoita valmiiksi -kirjauskansion. Välillisten kustannusten kirjanpitotapahtumat huomioidaan varastossa, kun kirjaat loppukirjauskansion.

Voit huomioida välilliset kustannukset ajan kulutuksessa, joka liittyy **Reitityskortti**-kirjauskansioihin tai **Työkortti**-kirjauskansioihin. Nämä tapahtumat palautetaan ja kirjataan kirjanpitotileille tuotantotilauksen päättyessä. Lisätietoja: [Kustannuslaskentalomakkeet](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Kirjanpitokirjausten tason hallinta

**Tuotannonhallinnan parametrit** -sivulla on mahdollista käyttää **Kirjaus kirjanpitoon** -kenttää määrittämään tuotantoprosessien kirjanpitokirjausten taso. 

Seuraavat kentät ovat käytettävissä:

### <a name="item-and-resource"></a>Nimike ja resurssi

Kun valitset **Nimike ja resurssi** -vaihtoehdon **Kirjaus kirjanpitoon** -kentässä, kirjaustilit tulevat reitityksen työvaiheen resurssista tai resurssiryhmästä. Tietyn resurssin tilit ovat ensimmäinen kirjausvaihtoehto. Jos tiliä ei määritetä, käytetään resurssiryhmälle määritettyjä tilejä. Reitityksen jokaisella työvaiherivillä voi olla yksi resurssi, joka on määritetty **Kustannusresurssiksi**. Tätä resurssia käytetään käytettävän tilin määrittämiseksi. Tätä vaihtoehtoa käytetään yleensä, kun organisaatio määrittää käyttökustannukset resursseille. Kustannukset ovat usein suurempia resursseissa, ja niiden avulla voidaan tehdä "make versus buy" -päätöksiä. Tämä on yksityiskohtaisin kirjauskonfiguraatio, ja se mahdollistaa tuotantoprosessin kirjausten tarkimman hallinnan sekä tuotantoprosessin hyvin yksityiskohtaisen analytiikan.

### <a name="item-and-category"></a>Nimike ja luokka

Kun valitset **Nimike ja luokka** -vaihtoehdon **Kirjaus kirjanpitoon** -kentässä, kirjaustilit tulevat **Kustannusluokka**-sivulta, joka liittyy reitityksen kuhunkin riviin. Reitityksen jokaisella työvaiherivillä voi olla kolme kustannusluokkaa: **Asetusaika**, **Suoritusaika** ja **Määrä**. Tätä vaihtoehtoa käytetään yleensä, kun organisaation pääpaino on prosessin tehokkuudessa ja tehtävän kestossa. Tämä kirjausvaihtoehto on yhteenvetotapa, ja sen avulla voit ryhmitellä kustannukset luokkiin.

### <a name="production-group"></a>Tuotantoryhmä

Kun valitset **Tuotantoryhmät**-vaihtoehdon **Kirjaus kirjanpitoon** -kentässä, kirjaustilit tulevat **Tuotantoryhmät**-sivulta. **Tuotantoryhmiä** käytetään tavallisesti silloin, kun enemmän kuin yksi tuotantorivi suorittaa samanlaisia tuotteita tai niillä on samanlaiset laitteet. Tämän vaihtoehdon avulla voit vertailla kahden eri tuotantoryhmän kustannuksia.  
  
> [!NOTE]
> Jos on käytetty valmiin nimikkeen kustannuslaskennan vakiomenetelmää, se näkyy lopullisista tapahtumista. Jos todellisten kustannusten ja vakiomenetelmän avulla laskettujen kustannusten välillä on eroja, ne kirjataan tilille tuottona tai tappiona.

### <a name="route-groups-and-ledger-posting"></a>Reititysryhmät ja kirjaukset kirjanpitoon

Reitityksen jokaiselle työvaiheriville on määritetty **Reititysryhmä**. Kenttiä **Asetusaika**, **Suoritusaika** ja **Määrä** **Reititysryhmässä**, **Arvio ja kustannuslaskelma** -ryhmässä, käytetään sen määrittämiseen, käytetäänkö aikaa kustannuslaskennassa, kun **Työkorttia** tai **Reitityskorttikirjauskansiota** kirjataan tuotantotilaukseen. Jos vaihtoehdot eivät ole käytössä, ajan kulutuksen tositetta ei luoda kirjanpitoon.

Jotta **Reitityskortti** tai **Työkorttikirjauskansio** kirjattaisiin tuotantotilauksen kirjanpitoon, seuraavien ehtojen on täytyttävä:

-   Kenttä **Asetusaika**, **Suoritusaika** tai **Määrä** on valittava **Arvio ja kustannuslaskelma** -ryhmässä **Reititysryhmä**-sivulla.
-   Päätilit on määritettävä joko sivulla **Kustannusluokka**, **Reititys**, **Reititysryhmä** tai **Tuotantoryhmä** seuraavia kirjaustyyppejä varten:
    -   Absorboidut arvioidut valmistuskustannukset
    -   Valmistuksen käyttämä arvioitu kustannus, KET

Seuraavassa kaaviossa esitetään reititysryhmän suhde tietyn reitityksen kunkin työvaiheen (reititysrivin) kokonaiskustannusten laskentaan. Jokaisella reititysrivillä on yksi reititysryhmä. Reititysryhmä hallinnoi asetusajan, suoritusajan ja määrän parametreja. **Kustannusluokka**-välilehdessä on kolme vaihtoehtoa **Asetusta**, **Suoritusta** ja **Määrää** varten, ja ne ovat käytettävissä reititysryhmäasetusten perusteella. **Ajoitukset**-pikavälilehdessä on kolme kenttää, jotka perustuvat reititysryhmään.

Käytettävä kaava perustuu siihen, onko vaihtoehto käytössä reititysryhmässä. Valitun kustannusluokan kustannus kerrotaan määrällä, joka on syötetty ajoituksiin kokonaiskustannusten laskemiseksi.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Reititysryhmien ja laskettujen kokonaiskustannusten suhde.":::
Reititysryhmien ja laskettujen kokonaiskustannusten suhde. Jokaisella reititysrivillä on yksi reititysryhmä. Reititysryhmä hallinnoi asetusajan, suoritusajan ja määrän parametreja. Kustannusluokka-välilehdessä on kolme vaihtoehtoa Asetusta, Suoritusta ja Määrää varten, ja ne ovat käytettävissä reititysryhmäasetusten perusteella. Ajoitukset-pikavälilehdessä on kolme kenttää, jotka on otettu käyttöön ja joiden osalta on suoritettu kustannuslaskenta perustuen reititysryhmään. Käytettävä kaava perustuu siihen, onko vaihtoehto käytössä reititysryhmässä. Valitun kustannusluokan kustannus kerrotaan määrällä, joka on syötetty ajoituksiin kokonaiskustannusten laskemiseksi.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Malli kirjausprofiilin konfiguraatiosta

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista. 

 - **Debet/kredit**-sarake osoittaa, onko tapahtuma tavallisesti debet vai kredit tai joissakin tapauksissa voi kirjata jommankumman. 
 - **Selvitystili**-sarake ilmaisee, onko kirjaustyyppi selvitystili. Tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan. 
 - **P/F**-sarakkeessa näkyy **P** fyysistä kirjausta varten ja **F** taloushallinnon kirjausta varten. 
 - **Seuraa**-sarakkeessa näkyy, onko tietyn kirjaustyypin päätili tavallisesti sama kuin toinen kirjaustyyppi. Sarakkeen arvo ilmaisee yleensä käytetyn kirjaustyypin.

> [!NOTE]
> Nämä päätilit ja päätilien nimet ovat vain ehdotuksia. Suosittelemme, että määrität yrityksesi tarpeille parhaan konfiguraation yhdessä kirjanpitäjän kanssa.


| Kirjaustyyppi  | Päätiliesimerkki. | Päätilin nimen esimerkki| Tilityyppi | Veloitus/hyvitys? | Selvitystili | Fyysinen tai kirjanpito | Seuraa | Kuvaus |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Arvioitu kulutettujen materiaalien kustannus      | 140100               | Materiaalivarasto        | Resurssi        | Hyvitys         | Y                | P                     | Kulutettujen materiaalien kustannus                | Tätä tiliä käytetään kirjattaessa tuotantotilauksen keräysluettelon kirjauskansio. Tilin vastatili on Arvioitu materiaalien kustannus, KET. Tälle tilille kirjattu summa palautetaan automaattisesti, kun tuotantotilaus on päättynyt. Tämä tili edustaa taseen varastoa.       |
| Arvioitu kulutettujen materiaalien kustannus, KET | 150150               | Tuotannon KET – Materiaalit | Resurssi        | Veloitus          | Y                | P                     | Arvioitu valmistuskustannus, KET          | Tätä tiliä käytetään kirjattaessa tuotantotilauksen keräysluettelon kirjauskansio. Tilin vastatili on Arvioitu kulutettujen materiaalien kustannus. Tälle tilille kirjattu summa palautetaan automaattisesti, kun tuotantotilaus on päättynyt. Tämä tili edustaa taseen KET:iä.                  |
| Arvioitu valmistuskustannus               | 140200               | Valmiiden tuotteiden varasto   | Resurssi        | Veloitus          | Y                | P                     | Valmistuskustannus                         | Tätä tiliä käytetään kirjattaessa tuotantotilauksen Ilmoita valmiiksi -kirjauskansio. Tilin vastatili on Arvioitu valmistuskustannus, KET. Tälle tilille kirjattu summa palautetaan automaattisesti, kun tuotantotilaus on päättynyt. Tämä tili edustaa taseen varastoa. |
| Arvioitu valmistuskustannus, KET          | 150150               | Tuotannon KET – Materiaalit | Resurssi        | Hyvitys         | Y                | P                     | Valmistuskustannus, KET                    | Tätä tiliä käytetään kirjattaessa tuotantotilauksen Ilmoita valmiiksi -kirjauskansio. Tilin vastatili on Arvioitu valmistuskustannus. Tälle tilille kirjattu summa palautetaan automaattisesti, kun tuotantotilaus on päättynyt. Tämä tili edustaa taseen KET:iä.                     |
| Kulutettujen materiaalien kustannus                | 140100               | Materiaalivarasto        | Resurssi        | Hyvitys         | N                 | F                     | Arvioitu kulutettujen materiaalien kustannus      | Tämän tilin avulla tunnistetaan tuotantotilauksessa päättämisprosessin aikana kulutettavat materiaalit. Tilin vastatili on Kulutettujen materiaalien kustannus, KET.                                                                                                    |
| Kulutettujen materiaalien kustannus, KET           | 150150               | Tuotannon KET – Materiaalit | Resurssi        | Veloitus          | N                 | F                     | Arvioitu kulutettujen materiaalien kustannus, KET | Tämän tilin avulla tunnistetaan tuotantotilauksessa päättämisprosessin aikana kulutettavat KET-materiaalit. Tilin vastatili on Kulutettujen materiaalien kustannus.                                                |
| Valmistuskustannus                         | 140200               | Valmiiden tuotteiden varasto   | Resurssi        | Veloitus          | N                 | F                     | Arvioitu valmistuskustannus               | Tämän tilin avulla tunnistetaan tuotantotilauksen valmiiden tuotteiden kustannukset, kun tuotantotilaus päätetään. Tilin vastatili on Valmistuskustannus, KET.                                                                  |
| Valmistuskustannus, KET                    | 150150               | Tuotannon KET – Materiaalit | Resurssi        | Hyvitys         | N                 | F                     | Arvioitu valmistuskustannus, KET          | Tämän tilin avulla tunnistetaan tuotantotilauksen valmiiden tuotteiden KET-kustannukset, kun tuotantotilaus päätetään. Tilin vastatili on Valmistuskustannus.                                     |

> [!NOTE]
> **Lean-palvelun keskeneräisen työn vastaanottoa** ja **Lean-palvelun KET-selvitystiliä** käytetään Lean-valmistuksen jälkikustannuslaskennassa. Lisätietoja: [Jälkikustannuslaskenta](/supply-chain/cost-management/backflush-costing.md).

