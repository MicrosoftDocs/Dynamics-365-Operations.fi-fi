---
title: Myyntisopimukset
description: "Tässä artikkelissa on tietoja myyntisopimuksista. Myyntisopimus on sopimus, jolla asiakas vahvistaa ostavansa tuotetta tietyn määrän tai tietyn summan tietyssä ajassa saadakseen erikoishinnan ja alennuksia."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 4eaa4fef65fb310524f25d052aeefb58c5f20fe4
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Myyntisopimukset
<a id="sales-agreements" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tietoja myyntisopimuksista. Myyntisopimus on sopimus, jolla asiakas vahvistaa ostavansa tuotetta tietyn määrän tai tietyn summan tietyssä ajassa saadakseen erikoishinnan ja alennuksia.

Myyntisopimus vahvistaa, että asiakas ostaa tuotteita tietyn määrän tai tietystä summasta ajan mittaan tiettyjä hintoja, erikoisalennuksia ja muita erityisehtoja, kuten maksu- ja toimitusehtoja, vastaan. Myyntisopimuksen hinnat ja alennukset korvaavat muissa kauppasopimuksissa määritetyt hinnat ja alennukset.  

Myyntisopimuksen voimassaoloaika määräytyy sopimuksen **Voimaantulopäivä**- ja **Vanhentumispäivä**-kenttien mukaan. Asiakkaan myyntitilaus täyttää sopimusehdot, jos tilauksen pyydetty toimituspäivä on sopimuksen voimassaolojaksolla. Kaikki myyntitilauksen rivit, jotka on linkitetty myyntisopimukseen, vaikuttavat myyntisopimuksen ehtojen täyttymiseen.  

Voit luoda myyntitilauksen suoraan myyntisopimuksesta käyttämällä **Vapauta tilaus** -toimintoa. Vaihtoehtoisesti voit valita voimassa olevan myyntisopimuksen ottaessasi vastaan tilauksia (katso tämän artikkelin kohtaa Myyntisopimusten käyttäminen tilausprosessissa).  

**Huomautus:** aiemmissa versioissa myyntisopimuksia kutsuttiin nimellä Myynnin yleistilaukset.

## Vahvistustyypit
<a id="commitment-types" class="xliff"></a>
Jokainen myyntisopimuksen rivi ilmaisee sitoutumisen myydä jotain. Yleensä sitoumuksia on kahdentyyppisiä:

-   **Arvositoumus**– Asiakas suostuu ostamaan tuotteita tietystä summasta.
-   **Määräsitoumus**– Asiakas suostuu ostamaan tietyn määrän tuotteita.

Sopimus voi myös sitoa asiakkaan ostamaan tuoteluokan tiettyä tuotetta tai tuotteita. Kun nämä kaksi tekijää (arvo vs. määrä ja tietyt tuotteet vs. tuoteluokat) yhdistetään, saadaan neljäntyyppisiä sitoumuksia:

-   **Tuotemääräsitoumus** – Asiakas suostuu ostamaan tietyn määrän tuotteita. Tätä sitoumustyyppiä käyttäviä rivejä määrittävät nimikenumero sekä määrä ja yksikkö, joista on sovittu. **Summa**-kenttä ei ole käytettävissä.
-   **Tuotearvositoumus** – Asiakas suostuu ostamaan tiettyjä tuotteita tietystä summasta. Tätä sitoumustyyppiä käyttäviä rivejä määrittävät nimikenumero sekä summa, josta on sovittu. **Määrä**- ja **Yksikkö**-kentät eivät ole käytettävissä.
-   **Tuoteluokan arvositoumus** – Asiakas suostuu ostamaan tietyn myyntiluokan tuotteita tietystä summasta. Tätä sitoumustyyppiä käyttäviä rivejä määrittävät myyntiluokkien hierarkiassa määritetty myyntiluokka sekä summa. **Määrä**- ja **Yksikkö**-kentät eivät ole käytettävissä.
-   **Arvositoumus** – Asiakas suostuu ostamaan minkä tahansa ostoluokan tuotetta tai tuotteita tietystä summasta. **Määrä**- ja **Yksikkö**-kentät eivät ole käytettävissä.

Saman myyntisopimuksen riveillä voi olla erityyppisiä sitoumuksia.

## Myyntisopimusten hintaehdot
<a id="pricing-terms-for-sales-agreements" class="xliff"></a>
Hintaehdot voivat olla erilaisia, riippuen sitoumustyypistä. Myyntisopimukseen linkitetyssä myyntitilauksessa sopimuksen hinnoitteluehdot kumoavat muihin kauppasopimuksiin perustuvat hinnoitteluehdot. Seuraava taulukko kuvailee hintoihin liittyvät kentät, joihin eri sitoumustyypit vaikuttavat. Kyllä-arvo osoittaa, että kentän voi päivittää tilausrivillä.

| Vahvistustyyppi                   | Yksikköhinta | Hintayksikkö | Alennusprosentti | Käteisalennussumma |
|-----------------------------------|------------|------------|------------------|----------------------|
| Tuotteen määrän vahvistus       | Kyllä        | Kyllä        | Kyllä              | Kyllä                  |
| Tuotteen arvon vahvistus          |            |            | Kyllä              |                      |
| Tuoteluokan arvon sitoutuminen |            |            | Kyllä              |                      |
| Arvon sitoutuminen                  |            |            | Kyllä              |                      |

## Myyntisopimuskäytännöt
<a id="policies-for-sales-agreements" class="xliff"></a>
Seuraavat käytännöt vaikuttavat siihen, miten myyntisopimussitoumuksen ja sitä vastaavien myyntitilausrivien välinen yhteys toimii:

-   **Maksimi pakotetaan** – Kaikkien tilausrivien kokonaismäärä tai summa ei voi olla enempää kuin sitä vastaavan sitoumuksen määrä tai summa.
-   **Hinta ja alennus on kiinteä** – Tilausrivin ja sitä vastaavan sitoumuksen hinnat eivät voi olla erilaiset. Jos tilausrivin hintaa muutetaan, yhteys sitoumukseen rikkoutuu. Jos yhteys rikkoutuu, tilausrivi ei edistä sitoumuksen täyttymistä.
-   **Vapautuksen vähimmäissumma** ja **Vapautuksen enimmäissumma** – Jos määrä on asetettu ja yrität tehdä tilausriviin muutoksia, joiden seurauksena tilausrivi poikkeaa siihen liittyvästä sitoumuksesta, näyttöön tulee ilmoitus.

## Myyntisopimusten täytäntöönpanolaskelmat
<a id="fulfillment-calculations-for-sales-agreements" class="xliff"></a>
**Myyntisopimukset**-sivun **Rivin tiedot** -pikavälilehdessä olevassa **Täytäntöönpano**-välilehdessä näkyvät täytäntöönpanon määrät ja summat.  

**Täytäntöönpano**-alueessa voit tarkastella kaikkien määritettyyn myyntisopimukseen yhdistettyjen tilausrivien kokonaismääriä ja -summia. Voit myös katsoa jäljellä olevat summat tai määrät, jotka tarvitaan sitoumuksen toteuttamiseen.  

**Sopimus**-alueessa voit tarkastella tietyn myyntisopimuksen määriä sekä summia. Nämä määrät ja summat ovat ne kokonaismäärät ja summat, jotka ilmoitettiin.

## Myyntisopimusten vahvistukset ja versiohistoria
<a id="confirmations-and-version-history-for-sales-agreements" class="xliff"></a>
Kun vahvistat myyntisopimuksen, sen nykyinen versio tallennetaan historiatauluun. Jos muutat myyntisopimusta, voit vahvistaa sen uudestaan, jolloin siitä tallentuu historiaan toinen versio.  

Jos et vahvista myyntisopimusta, voit yhä luoda myyntitilauksia sen pohjalta. Myyntisopimuksen historiatietoja ei kuitenkaan säilytetä.  

Voit esikatsella tai printata kaikki vahvistusten korjaukset. Tämän jälkeen voit jakaa korjaukset asiakkaalle saadaksesi hyväksynnän.

## Myyntisopimusten käyttäminen tilausprosessissa
<a id="applying-sales-agreements-during-the-ordering-process" class="xliff"></a>
Jos et vapauta myyntitilauksia suoraan myyntisopimuksista, voit silti yhdistää myyntisopimuksen tilaukseen tilaustenkäsittelyprosessissa. Kun luot uutta myyntitilausta ja valitset myyntisopimuksen, kyseisen sopimuksen ehdot, kuten maksu- ja toimitusehdot sekä toimitusosoite, täytetään tilauksen otsikkoon, ja järjestelmä luo sopimuksen ja tilauksen välille linkin. Tämän jälkeen myyntisopimuksessa olevat hinnat ja alennukset kopioidaan tilausriveille, ja voit valita myyntisopimuksessa määritellyistä tuotteista ja luokista haluamasi. Sama myyntitilaus voi sisältää sekä rivejä, jotka eivät liity myyntisopimukseen, että rivejä, joilla on myyntisopimusta koskeva sitoumus.

## Myyntisopimuksiin linkitettyjen myyntitilausten muokkaaminen
<a id="modifying-sales-orders-that-are-linked-to-sales-agreements" class="xliff"></a>
Jos olet luonut (vapautetun) myyntitilauksen myyntisopimuksesta, joitakin myyntitilausrivien kenttiä voi muokata vain, jos poistat linkin niihin liittyviin myyntisopimuksen riveihin. Seuraavassa taulukossa on esitetty joitakin näistä kentistä.

| Kenttä                                                             | Kuvaus                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pyydetty lähetyspäivämäärä                                               | Jos muutat pyydetyn lähetyspäivämäärän myyntisopimuksen rivillä olevaa **Voimaantulopäivä**-arvoa aikaisemmaksi, sinun täytyy poistaa linkki myyntisopimuksen riviin, ennen kuin voit tallentaa muutetun lähetyspäivän. Jos muutat pyydetyn lähetyspäivämäärän myyntisopimuksen rivillä olevaa **Vanhentumispäivä**-arvoa myöhäisemmäksi, sinun täytyy poistaa linkki myyntisopimuksen riviin, ennen kuin voit tallentaa muutetun lähetyspäivän. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet-summa | Jos muutat näiden kenttien arvoa ja liittyvältä myyntisopimuksen riviltä on poistettu **Hinta ja alennus on kiinteä** -valintaruudun valinta, näkyviin tulee sanomaruutu, jossa kysytään, haluatko tallentaa muutoksen. Valitsemalla **Kyllä** voit poistaa linkin myyntisopimuksen riviin ja laskea hinnan uudelleen. Valitsemalla **Ei** voit poistaa linkin myyntisopimuksen riviin laskematta hintaa uudelleen.                                                                   |
| Nettosumma                                                        | Jos määrittämäsi summa ylittää sellaisella myyntisopimuksen rivillä määritetyn summan, jossa **Maksimi pakotetaan** -valintaruutu on valittuna, näyttöön tulee sanomaruutu, joka kysyy, haluatko tallentaa muutetun summan. Valitsemalla **Kyllä** voit poistaa linkin myyntisopimuksen riviin ja laskea hinnan uudelleen. Valitsemalla **Ei** voit poistaa linkin myyntisopimuksen riviin laskematta hintaa uudelleen.                                                                 |
| Määrä                                                          | Jos määrittämäsi määrä ylittää sellaisella myyntisopimuksen rivillä määritetyn määrän, jossa **Maksimi pakotetaan** -valintaruutu on valittuna, näyttöön tulee sanomaruutu, joka kysyy, haluatko tallentaa muutetun määrän. Valitsemalla **Kyllä** voit poistaa linkin myyntisopimuksen riviin ja laskea hinnan uudelleen. Valitsemalla **Ei** voit poistaa linkin myyntisopimuksen riviin laskematta hintaa uudelleen.                                                            |

## Myyntisopimuksesta tilatun nimikkeen palauttaminen
<a id="returning-an-item-that-was-ordered-from-a-sales-agreement" class="xliff"></a>
Kun asiakas palauttaa tuotteen, joka on tilattu myyntisopimuksen kautta, Microsoft Dynamics 365 for Finance and Operations voi etsiä liittyvän myyntisopimuksen sitoumuksen ja päivittää sen automaattisesti vastaamaan muuttunutta määrää tai summaa. Luomalla myyntisopimukseen linkitettyyn alkuperäiseen myyntitilaukseen perustuvan palautustilauksen muodostat suhteen myyntisopimuksen sitoumuksen, myyntitilausrivin ja palautustilauslaskun välille.  

Jos et halua vähentää palautettua nimikemäärää myyntisopimuksen sitoumuksesta, **Palautustilaus**-sivun **Poista linkki** -ohjausobjektilla voit poistaa palautustilauksen ja myyntisopimuksen sitoumuksen välisen linkin. Jos haluat muodostaa linkin uudelleen myöhemmin, valitse **Luo linkki**.  

**Huomautus:** Palautustilaus voidaan linkittää vain yhteen myyntisopimukseen. Jos asiakas palauttaa useita tuotteita, jotka on tilattu usean myyntisopimuksen kautta, sinun on luotava uusi palautustilaus kullekin tuotteelle ja linkki vastaavaan myyntisopimukseen.

## Automaattinen haku myyntisopimuksia varten
<a id="automatic-search-for-sales-agreements" class="xliff"></a>
Joissakin tilanteissa, joissa myyntitilauksia luodaan epäsuorasti, esimerkiksi luodessasi hyvityslaskua tai konsernin sisäisiä myyntitilauksia, voit määrittää, hakeeko Microsoft Dynamics 365 for Finance and Operations automaattisesti käyttökelpoisia myyntisopimuksia.

## Taloushallinnon dimensiot myyntisopimuksissa
<a id="financial-dimensions-on-sales-agreements" class="xliff"></a>
Voit kopioida taloushallinnon dimensiot joko asiakirjojen ylätunnisteisiin tai myyntisopimusten yksittäisille riveille. Sopimuksen otsikon tai sopimusrivin dimensioita voi muuttaa milloin tahansa. Tässä tapauksessa dimensiot kopioidaan automaattisesti vapautustilausten otsikkoon tai vapautusriville.




