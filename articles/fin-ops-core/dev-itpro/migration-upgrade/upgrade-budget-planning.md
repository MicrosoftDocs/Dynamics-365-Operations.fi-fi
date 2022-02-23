---
title: Budjettisuunnittelun päivitys
description: Microsoft Dynamics AX 2012:n ja Dynamics 365 Financein budjettisuunnittelutoiminnoissa on merkittäviä eroja. Tiettyjä ominaisuuksia ei ole päivitetty, jonka vuoksi ne on määritettävä uudelleen. Tässä aiheessa kuvataan, mitä on määritettävä uudelleen sekä kuvaillaan uudet ominaisuudet, joiden käyttöä tulee harkita, kun päivitys on valmis.
author: ryansandness
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 1c62771170212039112c777e55d45a0d88d2f49d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680995"
---
# <a name="upgrade-budget-planning"></a>Budjettisuunnittelun päivitys

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012:n ja Dynamics 365 Financein budjettisuunnittelutoiminnoissa on merkittäviä eroja. Tiettyjä ominaisuuksia ei ole päivitetty, jonka vuoksi ne on määritettävä uudelleen. Tässä aiheessa kuvataan, mitä on määritettävä uudelleen sekä kuvaillaan uudet ominaisuudet, joiden käyttöä tulee harkita, kun päivitys on valmis.  

Financen budjettisuunnittelu sisältää useita parannuksia, jotka eivät olleet saatavilla Dynamics AX 2012:ssa. Tässä ohjeaiheessa kerrotaan muutokset, jotka päivittävän asiakkaan on tehtävä. Siinä osoitetaan myös uudet ominaisuuksia, jotka tulisi ottaa huomioon päivitysprosessin aikana. Koska muutokset ovat kattavia, olemassa olevia budjettisuunnitelmia ei voi avata ennen kuin tässä ohjeaiheessa kuvatut muutokset on tehty. Raporttien tulisi toimia, eivätkä ne vaadi lisämuutoksia.

## <a name="overview-of-changes"></a>Muutosten yleiskatsaus
Finance and Operationsin budjetointiin on tehty merkittävä muutoksia. Nämä muutokset helpottavat budjettisuunnittelun määrittämistä ja uudelleen käyttöä, vähentäen ajan kuluessa tarvittavaa ylläpitoa ja määrittämistä. Seuraavat AX 2012:n alueet on poistettu Financesta:

-   Budjettisuunnitelman mallit (budjettisuunnittelun konfigurointi)
-   Budjettisuunnitelman kansiot (budjettisuunnittelun konfigurointi)
-   Skenaarion rajoitukset (budjettisuunnittelun konfigurointi)
-   Budjettisuunnittelun vaihesääntöjen mallit (budjettisuunnitteluprosessi)
-   Laskentataulukkomallien matriisin kentät
-   Ohjattu budjettisuunnitelman Microsoft Excel -mallitoiminto

Tiettyihin uusiin konsepteihin ei ole mahdollista päivittää suoraan aiemmista toiminnoista. Sinun on siis tehtävä uudelleenmäärityksiä uusia konsepteja varten. Seuraavissa osissa kuvataan konseptit, jotka ovat korvanneet edellä esitetyn luettelon kohteet.

### <a name="columns"></a>Sarakkeet

Sarakkeet ovat uusi konsepti, jotka korvaavat osia Excel-mallista sekä matriisin kentistä. Sarakkeet voivat edustaa kautta, kuukautta, vuosineljännestä, vuotta tai kaikkea. Aikaviite on dynaaminen. Se osoittaa suhteelliseen kauteen tai vuoteen budjettiprosessin viitteenä. Esimerkiksi **Edellinen vuosi Tammikuu** -sarake viittaa vuoden -1 tilikauteen 1. Sarakkeet koskevat tiettyä budjettiskenaariota, kuten todellinen tai budjettipyyntö.

### <a name="layouts"></a>Asettelut

Asettelut ovat uusi konsepti, joka korvaa Excel-mallin. Asettelut sisältävät sarakkeita, jotka määrittävät mitkä budjetti- tai todelliset tiedot ja kaudet tulisi näyttää. Asettelut ovat yhteisiä niin asiakasohjelmassa kuin Excel-apuohjelmassa. Tietojen syöttämisen tai katselun käyttökokemus on Finance and Operations -asiakasohjelmassa siis parempi kuin AX 2012:ssa. Tietojen syöttö Finance-asiakasohjelmassa ei ole enää rajoitettu yhden skenaarion syöttämiseen ja tarkasteluun tapahtumanäkymässä. Voit sen sijaan käyttää vertailunäkymää, josta voit tarkastella ja muokata helposti useiden kausien ja tilien summia samanaikaisesti. Asettelut voi myös määrittää niin, että voit syöttää ja tarkastella valuuttoja, kommentteja tai muita vaihtoehtoisia tietoja. Asettelujen avulla voit myös määrittää, mitkä kirjanpitodimensiot ja dimensiokuvaukset näytetään. Asettelut sisältävät myös skenaariorajoituksia, joilla voi määrittää mitkä mallin sarakkeet ovat muokattavissa ja mitkä niistä ovat käytettävissä Excelissä. Kun asettelu on määritetty, sille luodaan malli. Tämä malli sijastaan luo vastaavan Excel-mallin. Voit sitten muokata Excel-mallia ja lisätä siihen kaavoja ja muotoilua, ja ladata sen takaisin. Asettelut määritetään sitten kullekin vaihesäännölle **Budjettisuunnitteluprosessi**-sivulla. Asettelut siis korvaavat mallit, jotka määritettiin ja joita käytettiin samalla tavalla.

### <a name="budget-planning-processes"></a>Budjettisuunnitteluprosessit

Budjettisuunnitteluprosessit ovat pääsääntöisesti samat kuin AX 2012:ssa. Merkittävin muutos on, että mallit on korvattu asetteluilla. Jos sinulla on valmiita prosesseja AX 2012:ssa, ne siirretään käsiteltävään tilaan, jotta niihin voidaan tehdä muutoksia. Määritä asettelut, jotka tarvitset kullekin vaihesäännölle, jotta voit päättää, mitkä skenaariot ja aikajaksot näytetään, kun suunnitelma avataan asiakasohjelmassa. Asettelut määrittävät myös, mikä Excel-malli avataan Dynamics 365 Financen ulkopuolella, jotta voit tarkastella budjettia. **Oletustilirakenne** on uusi, pakollinen kenttä budjettisuunnitteluprosessissa. Määritä kullekin budjettisuunnitteluprosessille ensisijainen tilirakenne, jota budjetoinnissa tulee käyttää.

### <a name="attachments"></a>Liitteet

Perusteluasiakirjat tallennettiin liitekansioon AX 2012:ssa. Aiempia perusteluasiakirjoja ei päivitetä. Perusteluasiakirjat tallennetaan nyt tietokantaan. Jos nämä tiedot tulee tallentaa päivitettyyn versioon, voit ladata lopulliset perusteluasiakirjat kunkin suunnitelman liitteeksi käyttämällä toimintoruudun **Perustelu**-painiketta. AX 2012 loi Excel-työkirjat kullekin budjettisuunnitelmalle mallin perusteella. Kaikki suunnitelmat avaavat Financessa asettelun kopion. Excel-tiedostoon ei kuitenkaan tallenneta muutoksia. Kaikki kaavat tai tukitiedot, joita käytettiin suunnitelmakohtaisesti on lisättävä kommenteissa, perusteluasiakirjassa tai jossain toisessa täydentävässä prosessissa.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>AX 2012:sta päivitetyn ympäristön määrittäminen
Seuraavassa esimerkissä käytetään AX 2012 -esittelytiedoista päivitettyä budjettiprosessia, jonka avulla opit, miten päivitetty järjestelmä määritetään. Päivitysprosessin auttamiseksi sarakkeille on luotu oletusmääritykset. Voit päivittää tai poistaa nämä oletustiedot, jos ne eivät vastaa määritysvaatimuksiasi. **Huomautus:** järjestelmä ei aseta arvoja uusille, pakollisille kentille. Jos et pysty siirtymään pois esimerkiksi **Budjettisuunnittelun konfigurointi** -sivulta, voit sulkea selaimen ja avata sen uudelleen toiselle sivulle, jotta voit syöttää tiedot oikeassa järjestyksessä. Joitakin pakollisia kenttiä ei ole vielä määritetty. Voit siis kohdata ongelmia, kunnes kaikki on määritetty ja kaikki pakolliset kentät on asetettu. Tässä ohjeaiheessa selitetään, miten nämä kentät määritetään vaatimusten mukaisesti. Seuraavassa on joitakin näistä pakollisista kentistä:

-   **Budjettisuunnitteluprosessi**-sivu: **Oletustilirakenne**-kenttä
-   **Budjettisuunnitteluprosessi**-sivu: **Asettelu**-kenttä **Budjettisuunnittelun vaiheen säännöt ja asettelut** -pikavälilehdessä

### <a name="define-columns-and-layouts"></a>Määritä sarakkeet ja asettelut

1. Valitse **Budjettisuunnittelun konfiguraatio** -sivulla **Sarakkeet**-välilehti. Päivityksessä luodaan uusia sarakkeita automaattisesti budjettisuunnitelmasi rivien perusteella. Sarakkeet käyttävät nyt dynaamisia päivämääriä, jossa kellonaika ja vuosi ovat siirtymiä budjettisuunnitteluprosessissa määritetystä tilikaudesta. **Huomautus:** suorituskykysyistä päivitys olettaa, että kaikki budjettijaksot ovat kalenterivuosia tilikausien sijaan. Jos käytät tilikausia, sinun on muokattava sarakkeita käsin, jotta ne vastaavat oikeita tilikausia. AX 2012 sisälsi esimerkiksi seuraavat elementit:
   -   Budjettisuunnitelman skenaariot: Todellinen, Perusarvo, Budjettipyyntö, Budjetti hyväksytty
   -   Budjettisuunnitelman rivit kaikille vuoden 2017 skenaarioille ja Todelliset sekä vuodelle 2016 että vuodelle 2017

   Seuraavat sarakkeet luodaan Finance and Operationsissa:

   | Sarakkeen nimi    | Budjettisuunnitelman skenaario | Sarakkeen ajanjakso | Vuoden siirtymä |
   |----------------|----------------------|--------------------|-------------|
   | Tam Skenaario 1 | Todelliset              | 1                  | 0           |
   | Tam Skenaario 2 | Perusrivi             | 1                  | 0           |
   | Tam Skenaario 3 | Budjettipyyntö       | 1                  | 0           |
   | Tam Skenaario 4 | Budjetti hyväksytty      | 1                  | 0           |
   | Tam Skenaario 5 | Todelliset              | 1                  | -1          |
   | Hel Skenaario 1 | Todelliset              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   Tässä esimerkissä luodaan sarake nimeltä **Tam Skenaario 1** uusimmalle budjettisuunnitelman tapahtumatiedolle, joka löydetään tammikuun tapahtumista. Vastaava sarake luodaan kullekin skenaariolle, joka sisältää tietoja. Kun kaikille vuoden kausille on luotu sarakkeet, järjestelmä luo sarakkeet edellisille vuosille.
2. Muuta sarakkeiden nimet ja kuvaukset sekä muut tiedot joko käsin asiakasohjelmassa tai tekemällä massapäivityksiä Excel-apuohjelman avulla, joka osoittaa budjettisuunnitelman sarakkeiden tietoyksikköön. Aiemmin matriisikentille asetetut suodattimet asetetaan nyt sarakkeille.
3. Luo uusi budjettisuunnitelman asettelu. Asettelu osoittaa useaan sarakkeeseen määrittääkseen näkymän, joka näytetään Excelissä ja asiakasohjelmassa. Asettelu edellyttää, että määrität ensin kirjanpidon dimensioyhdistelmän, joka määrittää syötettävissä olevat taloushallinnon dimensiot. Kun olet määrittänyt dimensioyhdistelmän, napsauta **Kuvaukset** ja valitse asetteluun sisällytettävät dimensiokuvaukset.
4. Valitse **Asetteluelementit**-pikavälilehdessä **Lisää** ja anna kullekin riville metatiedot, kuten valuutta, kommentti tai budjettiluokka, joka määrittää tuotto- tai kulurivit. Lisää seuraavaksi aikajakson sarakkeet ja nykyiseen budjettijaksoon- ja vaiheeseen kuuluvat skenaariot. Voit tehdä muutokset käsin asiakasohjelmassa tai Excel-apuohjelmassa, joka osoittaa budjettisuunnitelman asetteluelementtien tietoyksikköön.
5. Valitse kutakin asetteluelementtiä varten, onko sarake muokattavissa ja että näytetäänkö sarake myös asettelun Excel-työkirjassa. **Huomautus:** jos käytössäsi on historiallinen suunnitelma, harkitse käyttäväsi 12 kuukausittaista saraketta näyttävää asettelua kaikille kyseisen prosessin budjettisuunnitelman skenaarioille.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Päivitä budjettisuunnittelun prosessit käyttämään asiaankuuluvaa asettelua kussakin budjettivaiheessa

1.  Valitse konfiguroitava prosessi **Budjettisuunnittelun prosessi** -sivulla.
2.  Napsauta Toimintoruudussa **Muokkaa**.
3.  Määritä budjettiprosessin oletustilirakenne. **Oletustilirakenne** on uusi, pakollinen kenttä, joka on asetettava.
4.  Valitse **Budjettisuunnittelun vaiheen säännöt ja asettelut** -pikavälilehden **Asettelu**-kentässä asettelu, joka on aiemmin määritetty ja sopiva tähän vaiheeseen.
5.  Jatka valitsemalla sama tai eri asettelu budjettisuunnittelun eri vaiheille ja tallenna sitten muutokset.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Lisäominaisuuksia käytettäväksi budjetointiprosessissasi
### <a name="budget-planning-workspace"></a>Budjettisuunnittelun työtila

Työtila on tarkoitettu sekä budjetin omistajalle että sen suunnitteluun osallistuville. Se sisältää linkit kaikkiin huomiotasi vaativiin budjettiasiakirjoihin. Se sisältää myös budjettiprosessin raportit ja suorituskykymittarit (KPI:t). Budjetin järjestelmänvalvoja voi määrittää nykyisen budjetin suunnitteluprosessin kaikille käyttäjille **Budjetoinnin parametrit** -sivulla. **Työtilan asetukset** -välilehden **Budjettisuunnittelu**-pikavälilehti sisältää kentän, jossa voit valita budjettisuunnittelun prosessin.

### <a name="alternate-layouts"></a>Vaihtoehtoiset asettelut

Vaihtoehtoiset asettelut ovat uusi ominaisuus, jonka avulla voit tarkastella suunnitelmia eri asetteluissa. Vaihtoehtoina voi tarjota yhden tai useamman asettelun. Voit sitten tarkastella budjettisuunnitelmaa joko kuukausi- tai vuosineljännesasettelussa. Voit määritellä vaihtoehtoiset asettelut **Budjettisuunnittelun prosessi** -sivun **Budjettisuunnittelun vaiheen säännöt ja asettelut** -pikavälilehdessä.

### <a name="budget-milestones"></a>Budjetin välitavoitteet

Budjettiprosessin osana on tärkeää, että ymmärrät tärkeät päivämäärät ja määräajat. Voit nyt määrittää päivämäärät niin, että niillä on kuvaus. Budjetoinnin käyttäjät näkevät nämä kuvaukset avatessaan budjetteja muokattavaksi tai kun he tarkastelevat mitään heille määrättyä.

### <a name="copy-from-budget-plan-allocation"></a>Kopiointi budjettisuunnitelman kohdistuksesta

Uusi kohdistusmenetelmä mahdollistaa ylätason suunnitelman jakamisen alatasolle ilman hierarkian välitason käyttöä. Tämä menetelmä on erityisen hyödyllinen asiakkaille, jotka ovat aiemmin luoneet kirjanpitodimension ainoastaan budjetin jakamista ja hyväksyntää varten.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Budjettisuunnitelmien kehittäminen uusista budjetin lähteistä

Kausittaisiin prosesseihin on lisätty seuraavat vaihtoehdot. Näiden vaihtoehtojen avulla voit luoda budjettisuunnitelman käyttämällä lähtökohtana toisen moduulin tietoja:

-   Muodosta budjettisuunnitelma kysynnän ennusteesta
-   Muodosta budjettisuunnitelma tarjontaennusteesta
-   Muodosta budjettisuunnitelma projektiennusteista
-   Muodosta budjettisuunnitelma budjettirekisteristä

### <a name="more-complete-tracking-of-amounts"></a>Lisätietoja summien seurannasta

AX 2012:ssa budjettisuunnittelu sisälsi yhden jokaiselle arvolle tallennetun summan. Tätä tietomallia on laajennettu Financessa. Kullakin arvolla on nyt erilliset kirjanpitovaluutan, tapahtumavaluutan ja raportointivaluutan summat. Näihin sarakkeisiin täytetään olemassa olevia tietoja päivityksen aikana.

### <a name="do-not-convert-currency-in-aggregation"></a>Älä muunna valuuttaa koosteessa

Summat muunnetaan yleensä automaattisesti tapahtumavaluutasta organisaation kirjanpitovaluuttaan, kun alatason suunnitelma yhdistetään ylätasoon. Kun **Älä muunna valuuttaa koosteessa** -asetus on **Ei**, kootut summat pidetään alkuperäisessä valuutassa. Tämä toiminto sallii siis tarkemmat korjaukset, joihin vaikuttavat vaihtokurssin muutokset.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Näkymä budjettisuunnitelmasta taaksepäin muihin moduuleihin, jotka osallistuivat budjettiin

Budjettisuunnitelmat voidaan muodostaa kysyntä- tai tarjontaennusteista, projektista tai muista alueista. Budjettisuunnitelmat dimensioyhdistelmän mukaan -kysely sisältää useita vaihtoehtoja, joiden avulla voit tunnistaa budjettisuunnitelman lähteenä olleen tiedon.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Korvaa tai liitä suunnitelma kohdistusaikatauluun

Jos jaettaville summille on useita lähteitä, voit määrittää summat lisättäviksi. Tällöin summat eivät korvaa nykyisiä summia. Sen sijaan ne liitetään aiempiin summiin.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Budjettisuunnittelun konfiguraation taloushallinnon oletusdimensioyhdistelmä

**Budjettisuunnittelun konfiguraatio** -sivulla on nyt kenttä, jossa voit määrittää taloushallinnon oletusdimensioyhdistelmän. Kenttä on valinnainen, mutta sitä saatetaan tarvita tietyissä kyselyissä. Sitä voi tarvita myös raporttien ryhmittelyyn tai suodattamiseen dimensioyhdistelmän mukaan.

### <a name="data-entities"></a>Tietoyksiköt

Järjestelmään on lisätty useita tietoyksiköitä, jotka mahdollistavat budjettisuunnittelun nopean toteutuksen. Yksiköiden avulla voit myös tehdä muutoksia Excelin kautta. Näin sinun ei tarvitse luoda kohteita yksi kerrallaan asiakasohjelmassa. Seuraavassa on luettelo uusista tietoyksiköistä:

-   Yksikön nimi
-   Budjettiparametrit
-   Budjettisuunnitelman parametri
-   Budjettisuunnitelman skenaariot
-   Budjettisuunnitelman vaiheet
-   Budjettisuunnitelman työnkulun vaihe
-   Budjettisuunnitelman kohdistusaikataulut
-   Budjettisuunnitelman vaiheiden kohdistukset
-   Budjettisuunnitelman prioriteetit
-   Budjettisuunnitelman sarakkeet
-   Budjettisuunnitelman asetteluelementit




