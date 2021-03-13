---
title: Budjettisuunnittelun yleiskatsaus
description: Tässä ohjeaiheessa kuvataan budjettisuunnittelua. Se sisältää tietoja, jotka voivat auttaa budjettisuunnittelun ja budjettisuunnitteluprosessien määrittämisessä.
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 847ae83102345a8005a8b2a630805d22ccfd736d
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019225"
---
# <a name="budget-planning-overview"></a>Budjettisuunnittelun yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan budjettisuunnittelua. Se sisältää tietoja, jotka voivat auttaa budjettisuunnittelun ja budjettisuunnitteluprosessien määrittämisessä.

## <a name="overview-of-budget-planning"></a>Yleiskatsaus budjettisuunnitteluun

Organisaatio voi määrittää budjetin suunnittelun ja määrittää sitten budjetin suunnitteluprosessit, jotka vastaavat organisaation käytäntöjä, toimenpiteitä ja budjetin valmistuksen vaatimuksia. Kun Microsoft Dynamics 365 Financen käyttämät käsitteet ja terminologia ovat tuttuja, organisaation budjettisuunnittelu on helpompi ja tehokkaampi toteuttaa.

### <a name="key-terms"></a>Tärkeimmät termit

- **Budjettisuunnitteluprosessit** – Budjettisuunnitteluprosessit määrittävät, miten budjettisuunnitelmat voidaan päivittää, reitittää, tarkastella ja hyväksyä budjetoinnin organisaatiohierarkiassa. Budjettisuunnitteluprosessi on linkitetty budjettijaksoon ja organisaatioon yrityksen kautta.
- **Budjettisuunnitelmat** – Budjettisuunnitelmat sisältävät budjetin tiedot budjettijakson ajalta. Budjettisuunnitelmia voi olla useita eri tarkoituksia varten. Budjettisuunnitelmien avulla voit esimerkiksi luoda budjettisummia eri organisaatioyksiköille. Niiden avulla voit myös tehdä vertailuja ja perusteltuja päätöksiä.
- **Budjettiskenaariot** – Budjettiskenaariot määrittävät budjettisuunnitelmien tietojen luokat. Määrität budjettisuunnitelman skenaariot tukemaan rahaluokkia ja muita mittayksikköluokkia, kuten määriä. Esimerkkejä rahamääräisistä budjettisuunnitelman skenaarioista ovat osaston edellinen vuosi ja osaston pyynnöt. Edellisen vuoden tukipuhelut ja kokoaikavastaavuusmäärät (FTE) ovat esimerkkejä budjettiskenaarioista, joissa käytetään määriä.
- **Budjettisuunnittelun vaiheet** – Budjettisuunnittelun vaiheet määrittävät budjettisuunnitelman alusta sen lopulliseen hyväksyntään asti noudatettavat vaiheet. Budjetin suunnitteluvaiheet on järjestetty budjetin suunnittelun työnkuluiksi.
- **Budjettisuunnittelun työnkulut** – Budjettisuunnittelun työnkulut sisältävät ja määrittävät budjettisuunnittelun vaiheet. Budjettisuunnittelun työnkulut on liitetty budjetoinnin työnkulkuihin. Budjetoinnin työnkulut ovat automaattisia ja manuaalisia prosesseja, jotka siirtävät budjettisuunnitelmia budjetin suunnitteluprosessin vaiheiden läpi.

[![Budjettisuunnittelun käsitteistö](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Tyypilliset tehtävät

Voit käyttää budjettisuunnittelua seuraaviin tehtäviin:

- Luo budjettisuunnitelmia budjettijakson odotettujen tuottojen ja menojen määrittämistä varten.
- Analysoi ja päivitä useiden skenaarioiden budjettisuunnitelmat.
- Reititä automaattisesti budjettisuunnitelmia yhteen työlistojen, perusteluasiakirjojen ja muiden liitteiden kanssa, tarkastuksia ja hyväksymisiä varten.
- Konsolidoi useita budjettisuunnitelmia alemmalta tasolta organisaatiossa yhdeksi budjetin pääsuunnitelmaksi ylemmällä tasolla. Voit myös kehittää yksittäisen budjettisuunnitelman organisaation korkeammalla tasolla ja jakaa budjetin alemmille tasoille.

Budjettisuunnittelu on integroitu toisten moduulien kanssa. Tämän vuoksi voit sisällyttää aiempien budjettien tietoja, toteutuneita menoja, käyttöomaisuuden ja henkilöstöresurssit. Koska budjettisuunnittelu on integroitu myös Microsoft Exceliin ja Microsoft Wordiin, budjettisuunnittelutietoja voidaan käsitellä näillä ohjelmilla. Budjettipäällikkö voi viedä osaston budjettipyynnön Excelin laskentataulukkoon budjettiskenaariosta. Tiedot voidaan sitten analysoida, päivittää ja taulukoida laskentataulukolle, ja julkaista sitten takaisin budjettisuunnitelman riveille.

## <a name="configuring-budget-planning"></a>Määritä budjettisuunnittelu

Toiminto, joka sisältyy Dynamics 365 Financen versioon 10.0.9 (huhtikuu 2020) sisältää toiminnon, joka parantaa suorituskykyä **Julkaise**-painikkeen käyttämistä olemassa olevien tietueiden päivittämisessä Excelissä ja tämän jälkeen niiden julkaisemisessa takaisin asiakasohjelmaan. Tämä toiminto nopeuttaa päivitysprosessia ja auttaa vähentämään päivityksen eston todennäköisyyttä, kun päivität useita tietueita samaan aikaan. Jos haluat ottaa tämän toiminnon käyttöön, siirry **ominaisuuksien hallinnan** työtilaan ja ota **Budjettisuunnittelun kyselyn optimointi suorituskykyä varten** -toiminto käyttöön **Budgetointi**-kohdassa. Suosittelemme, että otat tämän toiminnon käyttöön.

**Budjettisuunnittelun konfigurointi** -sivu sisältää useimmat budjettisuunnittelussa tarvittavat asetukset. Seuraavissa osissa kuvataan joitakin tärkeimpiä budjettisuunnittelun määrittämisessä huomioitavia tekijöitä. Konfiguroinnin valmistuttua voidaan määrittää budjettisuunnitteluprosessit.

### <a name="budget-planning-schema-optional"></a>Budjettisuunnittelumalli (valinnainen)

Mallin luominen on valinnainen vaihe, mutta sen suorittaminen on suositeltavaa. Se näyttää organisaation budjetin laatimismenettelyn. Voit käyttää mallin luomisessa mitä tahansa menetelmää.

Seuraavassa kuvassa esitetään yleinen esimerkki, jossa budjettisuunnittelun työnkulut luodaan organisaation eri tasoille. Jokaisessa työnkulussa määritetään vaiheet, ja jokaiselle vaiheelle liitetään tietyt skenaariot budjettitietojen tallentamista varten. Tiedot siirretään yhdestä vaiheesta toiseen valmiiden tehtävien avulla. Esimerkiksi summat voidaan kohdistaa tai yhdistää erilaisille tileille, erilaisiin hyväksyntöihin tai muihin tarkistuksiin. Tässä kuvassa kursiivi teksti osoittaa skenaarion, jota ei voi muokata vaiheen aikana. Se voi osoittaa myös aiemmat tiedot tai aiemmassa vaiheessa hyväksytyt tiedot, joita ei muuttaa.

[![Budjettisuunnittelun yleinen malli](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Seuraavassa kuvassa yrityksen pääkonttori arvioi alkuperäisen budjetin perussummat ja jakaa summan myyntiosastojen välille. Myyntiosastot tekevät tämän jälkeen arvioinnit ja lähettävät ennusteen takaisin pääkonttorille, jossa budjettipäällikkö yhdistää ennusteet ja oikaisee lopullisen ennusteen. Lopuksi budjettipäällikkö lähettää oikaistut budjettisummat talousjohtajalle tarkistusta, lopullisia oikaisuja ja hyväksyntää varten.

[![Budjettisuunnittelumallin esimerkki](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Budjettisuunnittelun organisaatiohierarkia

Voit määrittää organisaatiohierarkian kunkin budjettisuunnitteluprosessin budjettisuunnittelun hierarkiaksi **Organisaatiohierarkia**-sivulla. Budjettisuunnittelun hierarkian ei tarvitse vastata muihin tarkoituksiin käytettävää vakio-organisaatiohierarkiaa. Koska tätä hierarkiaa käytetään tietojen yhdistämisessä ja jakelussa, sen rakenne kannattaa muokata erilaiseksi. Esimerkkimallissa myyntiorganisaatiot ovat budjetin ja talousosastot sisältävän pääkonttorin tason alla. Rakenne on luultavasti erilainen kuin myyntiosaston toimintojen hallinnassa käytettävä rakenne. Kuhunkin budjettisuunnitteluprosessiin voidaan määrittää vain yksi organisaatiohierarkia.

Lisätietoja on kohdassa [Organisaatiot ja organisaatiohierarkiat](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Käyttäjän suojaus

Budjettisuunnittelun käyttäjäoikeuksien määrittämistä varten on kaksi eri suojausmallia. Voit määrittää suojausmallin määrittämällä budjettisuunnittelun parametrin **Budjettisuunnittelun konfigurointi** -sivulla.

### <a name="budget-planning-workflows-stages"></a>Budjettisuunnittelun työnkulkujen vaiheet

Budjettisuunnittelun työnkulkuja ja budjetoinnin työnkulkuja käytetään yhdessä budjettisuunnitelmien luomisen hallinnassa.

Budjettisuunnittelun työnkulku koostuu järjestetystä joukosta vaiheita, joiden läpi budjettisuunnitelma kulkee. Jokainen budjettisuunnittelun työnkulku on liitetty budjetoinnin työnkulkuun. Budjetoinnin työnkulut ovat eräs Dynamics 365 Financessa käytettävä työnkulkutyyppi. Ne reitittävät budjettisuunnitelmat yhdessä laskentataulukoiden, perusteiden ja liitteiden kanssa organisaation arvioitaviksi ja hyväksyttäviksi.

Budjettisuunnittelun työnkulku luodaan **Budjettisuunnittelun konfigurointi** -sivun **Työnkulun vaiheet** -osassa. Tämän jälkeen valitaan vaiheet ja käytettävä budjetoinnin työnkulku. Lisäasetukset määritetään myös tässä vaiheessa.

Budjettisuunnittelun työnkulku kannattaa luoda jokaiselle budjetointihierarkian tasolle. Tämän jälkeen liitetään budjettisuunnittelun työnkulun vaiheita vastaavia elementtejä sisältävä budjetoinnin työnkulku. Aiemmin tässä ohjeaiheessa esitetyssä esimerkkimallissa luodaan yksi budjettisuunnittelun työnkulku myyntiosastoille ja toinen pääkonttorille. Budjetoinnin työnkulku siirtää budjettisuunnitelmat vaiheiden läpi.

Budjettisuunnittelun budjetoinnin työnkulku luodaan **Budjetoinnin työnkulut** -sivulla. Prosessi muistuttaa muiden työnkulkujen luontia. Seuraavassa kuvassa on esimerkki pääkonttorin työnkulusta.

[![Budjettisuunnittelun budjetoinnin työnkulku](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Työnkulku sisältää seuraavat elementit:

- Kohdistaminen myyntiosastoille ja niiden lähetysten koostaminen
- Budjettipäällikön tarkistus
- Talousjohtajan hyväksyntä
- Väliaikaiset siirtymät budjettisuunnitelman työnkulun kunkin vaiheen välillä

Budjetoinnin työnkulku liitetään kuhunkin budjettisuunnittelun työnkulkuun **Budjettisuunnittelun konfigurointi** -sivun **Työnkulun vaiheet** -osassa.

### <a name="parameters-scenarios-and-stages"></a>Parametrit, skenaariot ja vaiheet

**Budjettisuunnittelun konfigurointi** -sivun alkuasetuksissa voidaan luoda joitakin rakenneosia myöhempiä konfigurointivaiheita varten.

- **Parametrit** – Parametrit määrittävät budjettisuunnitelmiin ja taloushallinnon oletusdimensioihin kohdistettavat suojaussäännöt, joita käytetään käyttäjien siirtyessä budjettisuunnitelman skenaarion summiin.
- **Skenaariot** – Skenaariot sisältävät budjettisuunnitelmissa tarvittavien tietojen luokat. Määrität budjettisuunnitelman skenaariot tukemaan rahaluokkia ja muita mittayksikköluokkia, kuten määrää. Skenaariot edustavat budjettisuunnitelmassa budjettisuunnittelun tietojen yhtä versiota. Esimerkkejä budjettiskenaarioista ovat edellisen vuoden myynti ja allekirjoitetut sopimukset. Myyntipuheluiden lukumäärä ja kokoaikavastaavuusmäärät (FTE) ovat esimerkkejä skenaarioista, joissa käytetään määriä.
- **Vaiheet** – Vaiheet määrittävät budjettisuunnitelman vaiheet budjettisuunnitelman alkamisesta sen lopulliseen hyväksyntään asti. Budjettisuunnittelun vaiheiden esimerkkejä ovat pääkonttorin koonti, talousjohtajan tarkistus ja viimeistelyvaihe.

### <a name="allocation-schedules"></a>Kohdistusaikataulut

Budjettisuunnittelussa voidaan kohdistaa budjettisuunnitelmarivien summat tai määrät yhdestä skenaariosta toiseen tai jopa saman skenaarion sisällä. Samaan skenaarioon voidaan kohdistaa summia tai määriä, jos muutokset halutaan kohdistaa kyseisen skenaarion talousdimensioihin tai summien päivämääriin. Kohdistus voidaan tehdä budjettisuunnitelman sisällä tai yhdestä budjettisuunnitelmasta toiseen.

Kohdistusaikataulut kohdistavat budjettisuunnitelmarivit automaattisesti työnkulun käsittelyn aikana. Voit suorittaa kohdistukset minkä tahansa seuraavan **kohdistusmenetelmäluettelon** menetelmän avulla:

- **Kohdista kausille** – Voit käyttää kaudenkohdistustunnusta kohdistaessasi lähdebudjettiskenaarion budjettisuunnitelman rivit kohdeskenaarion kausiin.

    > [!NOTE]
    > Huomautus: Ennen kuin kohdistus kausiin voidaan suorittaa, kaudenkohdistustunnukset on määritettävä **Kaudenkohdistusluokat**-sivulla.

- **Kohdista dimensioille** – Budjettisuunnitelman rivit kohdistetaan budjettisuunnitelman lähdeskenaarion ja kohdeskenaarion taloushallinnon dimensioiden välillä.

    > [!NOTE]
    > Huomautus: Ennen kuin kohdistus dimensioihin voidaan suorittaa, budjetin kohdistusehdot on määritettävä **Budjetin kohdistusehto** -sivulla.

- **Yhdistä** – Budjettisuunnitelman rivit yhdistetään liittyvien budjettisuunnitelmien lähdebudjettiskenaariosta päätason budjettisuunnitelman kohdeskenaarioon.
- **Jaa**– Budjettisuunnitelman rivit jaetaan ylätason budjettisuunnitelman lähdebudjettiskenaariosta liittyvien budjettisuunnitelmien kohdeskenaarioon.
- **Käytä kirjanpidon kohdistussääntöjä** – Budjettisuunnitelman rivit jaetaan lähdebudjettiskenaariosta kohdebudjettiskenaarioon valitun kirjanpidon kohdistussäännön perusteella.
- **Kopioi budjettisuunnitelmasta** – Voit valita kohdistuksen lähteeksi toisen budjettisuunnitelman.

### <a name="stage-allocations"></a>Vaiheen kohdistukset

Vaiheen kohdistuksia käytetään budjettisuunnitelmien automaattiseen kohdistukseen työnkulun käsittelyn aikana. Kun vaiheen kohdistuksia käytetään, kohdeskenaarion budjettisuunnitelman rivit voidaan luoda ja niitä voidaan muokata ilman budjettisuunnitelman valmistelijan tai tarkistajan toimia.

Määrittäessäsi vaiheen kohdistuksen liität budjetti suunnitelman työnkulun ja vaiheen kohdistuksen aikatauluun. Budjettisuunnittelun työnkulku on liitettävä budjetoinnin työnkulkuun, joka käyttää automatisoitua **Budjetin suunnitteluvaiheen kohdistus** -työnkulkutehtävää. Työnkulun saavuttaessa tietyn vaiheen kohdistus tapahtuu automaattisesti. Automaattista tehtävää voidaan käyttää budjettisuunnitelmarivien luomiseen uudessa skenaariossa.

Aiemmin tässä ohjeaiheessa esitetyssä esimerkkimallissa suoritetaan kohdistus, jossa siirretään summat pääkonttorin perusvaiheen budjettisuunnitelmasta ja -skenaarioista myyntiosaston arviointivaiheen toiseen budjettisuunnitelmaan ja -skenaarioihin. Seuraavassa kuvassa näytetään esimerkkimallin kyseinen osa.

[![Vaiheen kohdistus](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Lisäksi esimerkkimallissa yhdistely tehdään myyntiosaston lähetettyjen vaiheen budjettisuunnitelmista ja -skenaarioista pääkonttorin koontivaiheen päätason suunnitelmaan. Seuraavassa kuvassa näytetään esimerkkimallin kyseinen osa.

[![Koostaminen](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteetit

Voit halutessasi käyttää budjettisuunnitelman prioriteetteja määrittämiesi budjettisuunnitelmien luokkien ja tavoitteiden määrittämisessä. Prioriteettien avulla voit myös järjestää, luokitella ja arvioida useita budjettisuunnitelmia. Voit esimerkiksi luoda budjettisuunnitelman prioriteetin terveydelle ja turvallisuudelle ja arvioida budjettisuunnitelmat, jotka on määritetty tähän prioriteettiin. Voit myös määrittää budjettisuunnitelmille numeron, joka osoittaa sijoituksen.

### <a name="columns-and-layouts"></a>Sarakkeet ja asettelut

Budjetin arvot näkyvät budjettisuunnitelman riveillä ja sarakkeilla. Määritä ensin sarakkeet. Tämän jälkeen voit luoda asettelun, jossa määritetään sarakkeiden esitysmuoto.

Valitse budjettiskenaario, kun haluat määrittää sarakkeen. Kyseisen skenaarion rivisummat näkyvät budjettisuunnitelmassa. Voit valita kauden, jonka mukaan summa suodatetaan. Voit myös käyttää kirjanpitotiliin perustuvia suodattimia.

Kun määrität asettelua, valitse kirjanpidon dimensiojoukko näytettävien budjettisuunnitelman rivien luomista varten. Valitse myös sarakkeet asetteluelementeiksi. Voit luoda useita asetteluita, jolloin budjettisuunnitelma näyttää haluamasi tiedot budjettisuunnitteluprosessin eri vaiheissa.

Budjettisummien sarakkeiden lisäksi voit määrittää projektin, ehdotetun projektin, käyttöomaisuuden ja ehdotettujen käyttöomaisuuskenttien sarakkeet budjettisuunnitelmasta. Voit määrittää myös budjetoitujen sijaintien sarakkeen. Tämä vaihtoehto on hyödyllinen henkilöstöbudjetin analysoimisessa.

Esimerkkimallissa voidaan luoda sarakkeet Edellisen vuoden myynti-, Sopimukset- ja Ennuste-skenaarioille. (Seuraava kuva sisältää malliin liittyvän osan). Tämän jälkeen voit eritellä yhden skenaarion tai useita skenaarioita erillisiksi sarakkeiksi kullekin tilikauden vuosineljännekselle niin, että myyntiosaston esimies voi syöttää kunkin kauden ennustesummat tarkasti.

[![Sarakkeet](./media/columns.png)](./media/columns.png)

Voit myös määrittää, ovatko asetteluelementit (sarakkeet) muokattavissa ja asettelulle luotujen laskentataulukkomallien käytettävissä. Esimerkkimallin arviointivaiheessa käytetyssä asettelussa Ennuste-sarakkeet ovat muokattavissa, mutta Edellisen vuoden myynti- ja Sopimukset-sarakkeet vain luku -tilassa.

> [!NOTE]
> Oletusarvoisesti rajoitus on 36 saraketta, ellet laajenna budjetoinnin suunnittelua seuraavilla kohdan [Laajenna budjettisuunnittelun asettelua](./extending-budget-planning-layout.md) vaiheilla.

### <a name="templates"></a>Mallipohjat

Voit luoda, tarkastella ja ladata kunkin asettelun Excel-malleja **Budjettisuunnittelun konfigurointi** -sivun **Asettelut**-osassa. Nämä mallit ovat työkirjoja, jotka on linkitetty budjettisuunnitelmaan lisäanalyysiä, kaavioita ja tiedonsyöttöominaisuuksia varten.

Kun malli on luotu, asettelu lukitaan. Tämän jälkeen sitä ei voi muokata. Lukitus varmistaa sen, että mallimuoto vastaa budjettisuunnitelman asettelua ja sisältää samat tiedot. Kun malli on luotu, sitä voidaan tarkastella ja muokata. Voit lisätä malliin esimerkiksi kaavioita ja mukauttaa sen ulkoasua.

> [!NOTE]
> Malli on tallennettava sijaintiin, josta käyttäjä voi käyttää sitä. Malli ladataan asetteluun sen jälkeen, kun muokkaus on tehty. Näin mallia käytetään budjettisuunnitelmissa, jotka käyttävät kyseistä asettelua.

### <a name="descriptions"></a>Kuvaukset

**Asettelut**-osassa voit liittää kuvauksia, jotka näyttävät tähän asetteluun sisältyvän taloushallinnon dimension nimen. Organisaatio voi esimerkiksi haluta näyttää päätilin nimen budjettisuunnitelman päätilin numeron vieressä. Se voi kuitenkin haluta jättää nimet pois muista talousdimensioista. Näin näytöstä ei tule liian sekava.

## <a name="setting-up-budget-planning-processes"></a>Budjettisuunnitteluprosessien määrittäminen

Kun budjettisuunnittelun konfiguroiminen on tehty, voit määrittää budjettisuunnitteluprosessit **Budjettisuunnitteluprosessi**-sivulla. Budjettisuunnitteluprosessit ovat sääntöjoukkoja, jotka määrittävät, miten budjettisuunnitelmat voidaan päivittää, reitittää, tarkastella ja hyväksyä budjetoinnin organisaatiohierarkiassa.

Budjettisuunnitteluprosessissa valitaan ensin budjettijakso ja kirjanpito. Kukin budjettisuunnitteluprosessi liittyy vain yhteen budjettijaksoon ja yhteen kirjanpitoon. Valitse sitten budjettiorganisaatiohierarkia **Budjettisuunnitteluprosessin hallinta** -pikavälilehdessä ja määritä budjettisuunnittelun työnkulku kaikille organisaation ruudukossa näkyville vastuupaikoille.

Voit määrittää budjettisuunnittelun työnkulun tai muuttaa sitä saman tyyppisille vastuupaikoille valitsemalla **Määritä työnkulku** -kohdan ja valitsemalla sitten kohdeorganisaatiotyypin ja käytettävän budjettisuunnittelun työnkulun. Budjetoinnin työnkulkutunnus, joka on liitetty kuhunkin budjettisuunnittelun työnkulkuun, lisätään ruudukkoon automaattisesti.

Kun vaihesäännöt ja mallit määritetään **Budjettisuunnittelun vaiheen säännöt ja asettelut** -pikavälilehdessä, voit määrittää erilaisia sääntöjoukkoja ja oletusasetteluita kutakin budjetin suunnitteluvaihetta varten. Esimerkiksi myyntiosaston arviointivaiheessa käyttäjät voivat muokata budjettisuunnitelman rivejä, mutta eivät lisätä rivejä. Lähetetty-vaiheessa käyttäjät voivat tarkastella rivejä, mutta eivät lisätä tai muokata niitä, koska työ tässä vaiheessa on tehty valmiiksi, eikä budjettisuunnitelmiin voi tehdä muutoksia. Voit valita budjettisuunnitelmissa käytettävissä olevat asettelut valitsemalla **Vaihtoehtoiset asettelut**.

Vaihtoehtoisesti voit valita budjettisuunnittelun prioriteetit **Budjettisuunnitelman prioriteetin rajoitukset** -pikavälilehdessä. Tämän jälkeen prioriteetit voidaan valita budjettisuunnitelmissa.

Viimeinen vaihe on budjettisuunnitteluprosessin aktivoiminen **Toiminnot**-valikon avulla. Budjettisuunnitteluprosessia ei voi käyttää, ennen kuin se on aktivoitu.

**Toiminnot**-valikossa voit luoda myös uuden prosessin kopioimalla aiemmin luodun prosessin. Tämä toiminto on hyödyllinen organisaatioissa, joiden prosessinkulku on täysin tai lähes samanlainen eri budjettijaksossa.

Toinen **Toiminnot**-valikon hyödyllinen komento on **Näytä budjettiprosessin tila**. Tämä komento näyttää graafisesti prosessin budjettisuunnitelmat ja niihin liittyvät tiedot, kuten suunnitelmien työnkulun tilan, yhteenvedot summan ja yksikön mukaan sekä budjettisuunnitelmiin siirtymisen yhdellä napsautuksella.

[![Budjetin suunnitteluprosessin tila](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)
