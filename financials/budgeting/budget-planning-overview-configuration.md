---
title: Budjetin suunnittelun yleiskuvaus
description: "Tämä artikkeli esittelee budjettisuunnittelun ja sisältää tietoja, joiden avulla voit määrittää budjettisuunnittelun ja budjettisuunnitteluprosessit."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 55553e9a791201b2707d2d9e98385e549d8417f6
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="budget-planning-overview"></a>Budjetin suunnittelun yleiskuvaus

[!include[banner](../includes/banner.md)]


Tämä artikkeli esittelee budjettisuunnittelun ja sisältää tietoja, joiden avulla voit määrittää budjettisuunnittelun ja budjettisuunnitteluprosessit.

<a name="overview-of-budget-planning"></a>Yleiskatsaus budjettisuunnitteluun
---------------------------

Budjetin suunnittelu suoritetaan valmisteltaessa budjetteja, jotka toteutetaan organisaatiossa. Organisaatio voi määrittää budjetin suunnittelun ja määrittää sitten budjetin suunnitteluprosessit, jotka vastaavat organisaation käytäntöjä, toimenpiteitä ja budjetin valmistuksen vaatimuksia. 

Kun Microsoft Dynamics 365 for Operationsin käyttämät käsitteet ja terminologia ovat tuttuja, organisaation budjettisuunnittelu on helpompi toteuttaa.

### <a name="key-terms"></a>Tärkeimmät termit

-   **Budjettisuunnitteluprosessit** – Budjettisuunnitteluprosessit määrittävät, miten budjettisuunnitelmat voidaan päivittää, reitittää, tarkastella ja hyväksyä budjetoinnin organisaatiohierarkiassa. Budjettisuunnitteluprosessi on linkitetty budjettijaksoon ja organisaatioon yrityksen kautta.
-   **Budjettisuunnitelmat** – Budjettisuunnitelmat sisältävät budjetin tiedot budjettijakson ajalta. Budjettisuunnitelmia voi olla useita eri tarkoituksia varten. Budjettijaksoja voidaan käyttää esimerkiksi luotaessa budjettisummia eri organisaatioyksiköille. Ne myös auttavat vertailujen tekemisessä ja tarjoavat tietoja päätöksiä tehtäessä.
-   **Budjettiskenaariot** – Budjettiskenaariot määrittävät budjettisuunnitelmien tietojen luokat. Määrität budjettiskenaariot tilanteissa tukemaan raha- ja muita mittayksikköluokkia, kuten määrää. Esimerkkejä budjettiskenaarioista ovat osaston edellinen vuosi ja osaston pyynnöt. Edellisen vuoden tukipuhelut ja kokoaikavastaavuusmäärät (FTE) ovat esimerkkejä budjettiskenaarioista, joissa käytetään määriä.
-   **Budjettisuunnittelun vaiheet** – Budjettisuunnittelun vaiheet määrittävät budjettisuunnitelman luonnista sen lopulliseen hyväksyntään asti noudatettavat vaiheet. Budjetin suunnitteluvaiheet on järjestetty budjetin suunnittelun työnkuluiksi.
-   **Budjettisuunnittelun työnkulut** – Budjettisuunnittelun työnkulut sisältävät ja määrittävät budjettisuunnittelun vaiheet. Budjettisuunnittelun työnkulut on liitetty budjetoinnin työnkulkuihin. Budjetoinnin työnkulut ovat automaattisia ja manuaalisia prosesseja, jotka siirtävät budjettisuunnitelmia budjetin suunnitteluprosessin vaiheiden läpi.

[![Budjettisuunnittelun käsitteistö](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Yleiset tehtävät

Voit käyttää budjettisuunnittelua seuraaviin tehtäviin:

-   Luo budjettisuunnitelmia budjettijakson odotettujen tuottojen ja menojen määrittämistä varten.
-   Analysoi ja päivitä useiden skenaarioiden budjettisuunnitelmat.
-   Reititä automaattisesti budjettisuunnitelmia yhteen työlistojen, perusteluasiakirjojen ja muiden liitteiden kanssa, tarkastuksia ja hyväksymisiä varten.
-   Konsolidoi useita budjettisuunnitelmia alemmalta tasolta organisaatiossa yhdeksi budjetin pääsuunnitelmaksi organisaation ylemmällä tasolla. Voit myös kehittää yksittäisen budjettisuunnitelman organisaation korkeammalla tasolla ja jakaa budjetin organisaation alemmille tasoille.

Budjettisuunnittelu integroituu muiden Microsoft Dynamics 365 for Operations -moduulien kanssa. Tämän vuoksi voit tuoda aiempien budjettien tietoja, toteutuneita menoja, käyttöomaisuuden ja henkilöstöresurssit. Koska budjettisuunnittelu on integroitu myös Microsoft Excelin ja Microsoft Wordin kanssa, voit käsitellä budjettisuunnittelun tietoja näillä ohjelmilla. Budjettipäällikkö voi viedä osaston budjettipyynnön Excelin laskentataulukkoon budjettiskenaariosta. Tiedot voidaan analysoida, päivittää ja taulukoida laskentataulukolle, ja julkaista sitten takaisin budjettisuunnitelman riveille.

## <a name="configuring-budget-planning"></a>Määritä budjettisuunnittelu
**Budjettisuunnittelun konfigurointi** -sivu sisältää useimmat budjettisuunnittelussa tarvittavat asetukset. Seuraavissa osissa kuvataan joitakin tärkeimpiä budjettisuunnittelun määrittämisessä huomioitavia tekijöitä. Konfiguroinnin valmistuttua määritetään budjettisuunnitteluprosessit.

### <a name="create-a-budget-planning-schema"></a>Budjettisuunnittelun kaavan luominen

Kaavan luominen on valinnainen, mutta suositeltava vaihe. Se näyttää organisaation budjetin laatimismenettelyn. Voit käyttää mallin luomisessa mitä tahansa menetelmää. Seuraavassa kuvassa esitetään yleinen esimerkki, jossa budjettisuunnittelun työnkulut luodaan organisaation eri tasoille. Jokaisessa työnkulussa määritetään vaiheet, ja jokaiselle vaiheelle liitetään tietyt skenaariot budjettitietojen tallentamista varten. Tiedot siirretään yhdestä vaiheesta toiseen tehtävien avulla. Esimerkiksi summat voidaan kohdistaa tai yhdistää erilaisille tileille, erilaisiin hyväksyntöihin tai muihin tarkistuksiin. Tässä esimerkissä kursiivi teksti osoittaa skenaarion, jota ei voi muokata vaiheen aikana. Se voi osoittaa myös aiemmat tiedot tai aiemmassa vaiheessa hyväksytyt tiedot, joita ei muuttaa. 

[![Budjettisuunnittelun yleinen malli](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Seuraavassa esimerkissä yrityksen pääkonttori arvioi alkuperäisen budjetin perussumman ja jakaa summan myyntiosastojen välille. Myyntiosastot tekevät tämän jälkeen arvioinnit ja lähettävät ennusteen takaisin pääkonttorille, jossa budjettipäällikkö yhdistää ennusteet ja oikaisee lopullisen ennusteen. Lopuksi budjettipäällikkö lähettää oikaistut budjettisummat talousjohtajalle tarkistusta, lopullisia oikaisuja ja hyväksyntää varten. 

[![Budjettisuunnittelumallin esimerkki](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Budjettisuunnittelun organisaatiohierarkia

Voit määrittää organisaatiohierarkian kunkin budjettisuunnitteluprosessin budjettisuunnittelun hierarkiaksi **Organisaatiohierarkia**-sivulla. Budjettisuunnittelun hierarkian ei tarvitse vastata muihin tarkoituksiin käytettävää vakio-organisaatiohierarkiaa. Koska tätä hierarkiaa käytetään tietojen yhdistämisessä ja jakelussa, sen rakenne kannattaa muokata erilaiseksi. Esimerkkimallissa myyntiorganisaatiot ovat budjetin ja talousosastot sisältävän pääkonttorin tason alla. Rakenne on luultavasti erilainen kuin myyntiosaston toimintojen hallinnassa käytettävä rakenne. Kuhunkin budjettisuunnitteluprosessiin voidaan määrittää vain yksi organisaatiohierarkia. 

Lisätietoja on kohdassa [Organisaatiot ja organisaatiohierarkiat](/dynamics365/operations/organization-administration/organizations-organizational-hierarchies).

### <a name="user-security"></a>Käyttäjän suojaus

Budjettisuunnittelun käyttäjäoikeuksien määrittämistä varten on kaksi eri suojausmallia. Voit määrittää suojausmallin määrittämällä budjettisuunnittelun parametrin **Budjettisuunnittelun konfigurointi** -sivulla.

### <a name="budget-planning-workflows-stages"></a>Budjettisuunnittelun työnkulkujen vaiheet

Budjettisuunnittelun työnkulkuja ja budjetoinnin työnkulkuja käytetään yhdessä budjettisuunnitelmien luomisen hallinnassa.

Budjettisuunnittelun työnkulku koostuu järjestetystä joukosta vaiheita, joiden läpi budjettisuunnitelma kulkee. Jokainen budjettisuunnittelun työnkulku on liitetty budjetoinnin työnkulkuun. Budjetoinnin työnkulut ovat eräs Microsoft Dynamics 365 for Operationsissa käytettävä työnkulkutyyppi. Budjetoinnin työnkulku reitittää budjettisuunnitelmat yhdessä laskentataulukoiden, perusteiden ja liitteiden kanssa organisaation arvioitaviksi ja hyväksyttäviksi. 

Budjettisuunnittelun työnkulku luodaan **Budjettisuunnittelun konfigurointi** -sivun **Työnkulun vaiheet** -osassa. Tämän jälkeen valitaan vaiheet ja käytettävä budjetoinnin työnkulku. Lisäasetukset määritetään myös tässä vaiheessa. 

Budjettisuunnittelun työnkulku kannattaa luoda jokaiselle budjetointihierarkian tasolle. Tämän jälkeen liitetään budjettisuunnittelun työnkulun vaiheita vastaavia elementtejä sisältävä budjetoinnin työnkulku. Aiemmin tässä artikkelissa esitetyssä esimerkkimallissa luodaan yksi budjettisuunnittelun työnkulku myyntiosastoille ja toinen pääkonttorille. Budjetoinnin työnkulku siirtää budjettisuunnitelmat vaiheiden läpi. 

Budjettisuunnittelun budjetoinnin työnkulku luodaan **Budjetoinnin työnkulut** -sivulla. Prosessi muistuttaa muiden työnkulkujen luomista Microsoft Dynamics 365 for Operationsissa. Seuraavassa kuvassa on pääkonttorin työnkulun esimerkki. 

[![Budjettisuunnittelun budjetoinnin työnkulku](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Työnkulku sisältää elementtejä myyntiosastoihin kohdistusta ja lähetysten yhdistämistä varten sekä budjettipäällikön tarkistuksen, toimitusjohtajan hyväksynnän ja vaiheiden välillä siirtymiset. 

Budjetoinnin työnkulku liitetään kuhunkin budjettisuunnittelun työnkulkuun **Budjettisuunnittelun konfigurointi** -sivun **Työnkulun vaiheet** -osassa.

### <a name="parameters-scenarios-and-stages"></a>Parametrit, skenaariot ja vaiheet

**Budjettisuunnittelun konfigurointi** -sivun alkuasetuksissa voidaan luoda joitakin rakenneosia myöhempiä konfigurointivaiheita varten.

-   **Parametrit** – Parametrit määrittävät budjettisuunnitelmiin ja taloushallinnon oletusdimensioihin kohdistettavat suojaussäännöt, joita käytetään käyttäjien siirtyessä budjettisuunnitelman skenaarion summiin.
-   **Skenaariot** – Skenaariot sisältävät budjettisuunnitelmissa tarvittavien tietojen luokat. Määrität budjettiskenaariot tilanteissa tukemaan raha- ja muita mittayksikköluokkia, kuten määrää. Skenaariot edustavat budjettisuunnitelmassa budjettisuunnittelun tietojen yhtä versiota. Esimerkkejä budjettiskenaarioista ovat edellisen vuoden myynti ja allekirjoitetut sopimukset. Myyntipuheluiden lukumäärä ja kokoaikavastaavuusmäärät (FTE) ovat esimerkkejä skenaarioista, joissa käytetään määriä.
-   **Vaiheet** – Vaiheet määrittävät budjettisuunnitelman vaiheet budjettisuunnitelman luonnista sen lopulliseen hyväksyntään asti. Budjettisuunnittelun vaiheiden esimerkkejä ovat pääkonttorin koonti, talousjohtajan tarkistus ja viimeistelyvaihe.

### <a name="allocation-schedules"></a>Kohdistusaikataulut

Budjettisuunnittelussa voidaan kohdistaa budjettisuunnitelmarivien summat tai määrät yhdestä skenaariosta toiseen tai jopa saman skenaarion sisällä. Samaan skenaarioon voidaan kohdistaa, jos muutokset halutaan kohdistaa kyseisen skenaarion talousdimensioihin tai summien päivämääriin. Kohdistus voidaan tehdä budjettisuunnitelman sisällä tai yhdestä budjettisuunnitelmasta toiseen. 

Kohdistusaikataulut kohdistavat budjettisuunnitelmarivit automaattisesti työnkulun käsittelyn aikana. Voit suorittaa kohdistukset minkä tahansa seuraavan **kohdistusmenetelmäluettelon** menetelmän avulla:

-   **Kohdista kausille** – Voit käyttää kaudenkohdistustunnusta kohdistaessasi lähdebudjettiskenaarion budjettisuunnitelman rivit kohdeskenaarion kausiin. **Huomautus:** Ennen kuin kohdistus kausiin voidaan suorittaa, kaudenkohdistustunnukset on määritettävä ****Kaudenkohdistusluokat****-sivulla.
-   **Kohdista dimensioille** – Budjettisuunnitelman rivit kohdistetaan budjettisuunnitelman lähdeskenaarion ja kohdeskenaarion taloushallinnon dimensioiden välillä. **Huomautus:** Ennen kuin kohdistus dimensioihin voidaan suorittaa, budjetin kohdistusehdot on määritettävä ****Budjetin kohdistusehto**** -sivulla.
-   **Yhdistä** – Budjettisuunnitelman rivit yhdistetään liittyvien budjettisuunnitelmien lähdebudjettiskenaariosta päätason budjettisuunnitelman kohdeskenaarioon.
-   **Jaa**– Budjettisuunnitelman rivit jaetaan ylätason budjettisuunnitelman lähdebudjettiskenaariosta liittyvien budjettisuunnitelmien kohdeskenaarioon.
-   **Käytä kirjanpidon kohdistussääntöjä** – Budjettisuunnitelman rivit jaetaan lähdebudjettiskenaariosta kohdebudjettiskenaarioon valitun kirjanpidon kohdistussäännön perusteella.
-   **Kopioi budjettisuunnitelmasta** – Voit valita kohdistuksen lähteeksi toisen budjettisuunnitelman.

### <a name="stage-allocations"></a>Vaiheen kohdistukset

Vaiheen kohdistuksia käytetään budjettisuunnitelmien automaattiseen kohdistukseen työnkulun käsittelyn aikana. Kun vaiheen kohdistuksia käytetään, kohdeskenaarion budjettisuunnitelman rivit voidaan luoda ja niitä voidaan muokata ilman budjettisuunnitelman valmistelijan tai tarkistajan toimia.

Määrittäessäsi vaiheen kohdistuksen liität budjetti suunnitelman työnkulun ja vaiheen kohdistuksen aikatauluun. Budjettisuunnittelun työnkulku on liitettävä budjetoinnin työnkulkuun, joka käyttää automatisoitua ****Budjetin suunnitteluvaiheen kohdistus**** -työnkulkutehtävää. Työnkulun saavuttaessa tietyn vaiheen kohdistus tapahtuu automaattisesti. Automaattista tehtävää voidaan käyttää budjettisuunnitelmarivien luomiseen uudessa skenaariossa. 

Aiemmin tässä artikkelissa esitetyssä esimerkkimallissa suoritetaan kohdistus, jossa siirretään summat pääkonttorin perusvaiheen budjettisuunnitelmasta ja -skenaarioista myyntiosaston arviointivaiheen toiseen budjettisuunnitelmaan ja -skenaarioihin. Seuraavassa kuvassa näytetään esimerkkimallin kyseinen osa.

[![Vaiheen kohdistus](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Esimerkkimallissa yhdistely tehdään myyntiosaston lähetettyjen vaiheen budjettisuunnitelmista ja -skenaarioista pääkonttorin koontivaiheen päätason suunnitelmaan. Seuraavassa kuvassa näytetään esimerkkimallin kyseinen osa.

[![Koostaminen](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteetit

Voit halutessasi käyttää budjettisuunnitelman prioriteetteja määrittämiesi budjettisuunnitelmien luokkien ja tavoitteiden määrittämisessä. Prioriteettien avulla voit myös järjestää, luokitella ja arvioida useita budjettisuunnitelmia. Voit esimerkiksi luoda budjettisuunnitelman prioriteetin terveydelle ja turvallisuudelle ja arvioida budjettisuunnitelmat, jotka on määritetty tähän prioriteettiin. Voit määrittää numeron luokittamaan budjettisuunnitelmat kaikkien budjettisuunnitelmien kesken.

### <a name="columns-and-layouts"></a>Sarakkeet ja asettelut

Budjetin arvot näkyvät budjettisuunnitelman riveillä ja sarakkeilla. Määritä ensin sarakkeet. Tämän jälkeen voit luoda asettelun, jossa määritetään sarakkeiden esitysmuoto. 

Valitse budjettiskenaario, kun haluat määrittää sarakkeen. Kyseisen skenaarion rivisummat näkyvät budjettisuunnitelmassa. Voit valita kauden, jonka mukaan summa suodatetaan. Voit myös käyttää kirjanpitotiliin perustuvia suodattimia. 

Kun määrität asettelua, valitse kirjanpidon dimensiojoukko näytettävien budjettisuunnitelman rivien luomista varten. Valitse myös sarakkeet asetteluelementeiksi. Voit luoda useita asetteluita, jolloin budjettisuunnitelma näyttää haluamasi tiedot budjettisuunnitteluprosessin eri vaiheissa. 

Budjettisummien sarakkeiden lisäksi voit määrittää projektin, ehdotetun projektin, käyttöomaisuuden ja ehdotettujen käyttöomaisuuskenttien sarakkeet budjettisuunnitelmasta. Voit määrittää myös budjetoitujen sijaintien sarakkeen. Tämä on erittäin hyödyllinen henkilöstöbudjetin analysoimisessa. 

Esimerkkimallissa voidaan luoda sarakkeet edellisen vuoden myynnille, sopimuksille ja ennusteskenaarioille (seuraava kuva sisältää malliin liittyvän osan). Tämän jälkeen voit eritellä yhden skenaarion tai useita skenaarioita erillisiksi sarakkeiksi kullekin tilikauden vuosineljännekselle niin, että myyntiosaston esimies voi syöttää kunkin kauden ennustesummat tarkasti.

[![Sarakkeet](./media/columns.png)](./media/columns.png) 

Voit myös määrittää, ovatko asetteluelementit (sarakkeet) muokattavissa ja asettelulle luotujen laskentataulukkomallien käytettävissä. Esimerkkimallin arviointivaiheessa käytetyssä asettelussa Ennuste-sarakkeet ovat muokattavissa, kun taas Edellisen vuoden myynti- ja Sopimukset-sarakkeet vain luku -tilassa.

### <a name="templates"></a>Mallit

Voit luoda, tarkastella ja ladata Excel-malleja **Budjettisuunnittelun konfigurointi** -sivun **Asettelut**-osassa. Nämä mallit ovat työkirjoja, jotka on linkitetty budjettisuunnitelmaan lisäanalyysiä, kaavioita ja tiedonsyöttöominaisuuksia varten. 

Voit luoda tai ladata kullekin asettelulle mallin tai tarkastella sitä. Kun malli on luotu, asettelu lukitaan. Tämän jälkeen sitä ei voi muokata. Lukitus varmistaa sen, että mallimuoto vastaa budjettisuunnitelman asettelua ja sisältää samat tiedot. Kun malli on luotu, sitä voidaan tarkastella ja muokata. Voit lisätä malliin esimerkiksi kaavioita ja mukauttaa sen ulkoasua.

> [!NOTE] 
> Malli on tallennettava sijaintiin, josta käyttäjä voi käyttää sitä. Malli ladataan asetteluun sen jälkeen, kun muokkaus on tehty. Näin mallia käytetään budjettisuunnitelmissa, jotka käyttävät kyseistä asettelua.

### <a name="descriptions"></a>Kuvaukset

Kuvauksia, jotka voidaan liittää **Asettelut**-osaan, käytetään tähän asetteluun sisältyvän taloushallinnon dimension nimen näyttämisessä. Organisaatiossa voidaan esimerkiksi haluta näyttää päätilin nimi päätilin numeron vieressä budjettisuunnitelmassa, mutta haluat ohittaa muiden taloushallinnon dimensioiden nimet, jotta näytöstä ei tule liian sekavaa.

## <a name="setting-up-budget-planning-processes"></a>Budjettisuunnitteluprosessien määrittäminen

Kun budjettisuunnittelun konfiguroiminen on tehty, voit määrittää budjettisuunnitteluprosessit **Budjettisuunnitteluprosessi**-sivulla. Budjettisuunnitteluprosessit ovat sääntöjoukkoja, jotka määrittävät, miten budjettisuunnitelmat voidaan päivittää, reitittää, tarkastella ja hyväksyä budjetoinnin organisaatiohierarkiassa. 

Budjettisuunnitteluprosessissa valitaan ensin budjettijakso ja kirjanpito. Kukin budjettisuunnitteluprosessi liittyy vain yhteen budjettijaksoon ja yhteen kirjanpitoon. Valitse sitten budjettiorganisaatiohierarkia **Budjettisuunnitteluprosessin hallinta** -pikavälilehdessä ja määritä budjettisuunnittelun työnkulku kaikille organisaation ruudukossa näkyville vastuupaikoille. 

Voit määrittää budjettisuunnittelun työnkulun tai muuttaa sitä saman tyyppisille vastuupaikoille napsauttamalla **Määritä työnkulku** ja valitsemalla sitten kohdeorganisaatiotyypin ja käytettävän budjettisuunnittelun työnkulun. Budjetoinnin työnkulkutunnus, joka on liitetty kuhunkin budjettisuunnittelun työnkulkuun, lisätään ruudukkoon automaattisesti. 

Kun vaihesäännöt ja mallit määritetään **Budjettisuunnittelun vaiheen säännöt ja asettelut** -pikavälilehdessä, voit määrittää erilaisia sääntöjoukkoja ja oletusasetteluita kutakin budjetin suunnitteluvaihetta varten. Esimerkiksi myyntiosaston arviointivaiheessa käyttäjät voivat muokata budjettisuunnitelman rivejä, mutta eivät lisätä rivejä. Lähetettyjen vaiheessa käyttäjät voivat tarkastella rivejä, mutta eivät lisätä tai muokata niitä, koska työ tässä vaiheessa on tehty valmiiksi, eikä budjettisuunnitelmiin voi tehdä muutoksia. Voit valita budjettisuunnitelmissa käytettävissä olevat asettelut valitsemalla **Vaihtoehtoiset asettelut**. 

Vaihtoehtoisesti voit valita budjettisuunnittelun prioriteetit **Budjettisuunnitelman prioriteetin rajoitukset** -pikavälilehdessä. Tämän jälkeen prioriteetit voidaan valita budjettisuunnitelmissa. 

Viimeinen vaihe on budjettisuunnitteluprosessin aktivoiminen **Toiminnot**-valikossa. Budjettisuunnitteluprosessia ei voi käyttää, jos sitä ei ole aktivoitu. 

**Toiminnot**-valikossa voi luoda myös uuden prosessin kopioimalla aiemmin luodun prosessin. Tämä toiminto on hyödyllinen organisaatioissa, joiden prosessinkulku on täysin tai lähes samanlainen eri budjettijaksossa. 

Toinen **Toiminnot**-valikon hyödyllinen komento on **Näytä budjettiprosessin tila**. Tämä komento näyttää graafisesti prosessin budjettisuunnitelmat ja niihin liittyvät tiedot, kuten suunnitelmien työnkulun tilan, yhteenvedot summan ja yksikön mukaan sekä budjettisuunnitelmiin siirtymisen yhdellä napsautuksella.

[![Budjetin suunnitteluprosessin tila](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)




