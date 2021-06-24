---
title: Tuotannon suunnittelu
description: Tässä aiheessa käsitellään tuotannon suunnittelua ja suunniteltujen tuotantotilausten muokkaamista tuotannon optimoinnin avulla.
author: ChristianRytt
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ffee79f152141297ceb24e2d7a40523eac18ffaf
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129750"
---
# <a name="production-planning"></a>Tuotannon suunnittelu

Suunnittelun optimointi tukee useita tuotantoskenaarioita. Jos siirtyminen tapahtuu nykyisestä sisäisestä pääsuunnittelumoduulista, on tärkeää ottaa huomioon tietyt toiminnasta tapahtuneet muutokset.

Seuraavassa videossa esitetään lyhyt johdanto joihinkin tässä aiheessa käsiteltyihin käsitteisiin: [Dynamics 365 Supply Chain Management: Suunnitteluoptimoinnin parannukset](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Tämän ominaisuuden ottaminen käyttöön järjestelmällesi

Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Suunnitellut tuotantotilaukset tuotannon optimoinnille* -ominaisuus käyttöön.

## <a name="planned-production-orders"></a>Suunnitellut tuotantotilaukset

Kun pääsuunnittelu täyttää tarpeita luomalla suunniteltuja tilauksia, tilauksen tyyppi määritetään **Suunniteltu tilaustyyppi** -kentän arvon perusteella. Jos **Suunniteltu tilaustyyppi** -kentän asetuksena on *Tuotanto*, luodaan suunniteltuja tuotantotilauksia. Näissä suunnitelluissa tuotantotilauksissa on tietoja aktiivisista tuoterakenteista ja liittyvän tuotantomäärityksen reititystunnus.

## <a name="requirements-from-boms"></a>Tuoterakenteiden tarpeet

Tuoterakennetiedot otetaan huomioon pääsuunnittelun aikana. Suunnittelutulos sisältää materiaalin oston, joka kattaa tuotantoon liittyvän materiaalin kysynnän.

Pääsuunnittelun aikana nykyisen aktiivisen tuoterakenteen avulla määritetään tuotantoa varten tarvittavat materiaalit. Tämä vaihe tehdään kaikilla tarvittavaan tuotantotilaukseen liittyvillä tuoterakenteen tasoilla. Materiaalitarve täytetään käyttämällä käytettävissä olevaa varastoa, nykyistä tilausvarastoa ja hyväksyttyjä suunniteltuja tilauksia. Jos jossakin tarvitaan lisämateriaalia, kysyntää varten luodaan suunniteltu tilaus.

## <a name="scheduling-during-firming"></a>Aikatauluttaminen vahvistuksen aikana

Suunnitellut tuotantotilaukset sisältävä reititystunnuksen, jota tarvitaan tuotannon aikatauluttamiseen. Suunniteltujen tilausten aikataulutuksen tukea suunnitteluajon aikana odotetaan. Reititystunnusta käytetään suunniteltujen tuotantotilausten aikatauluttamiseen vahvistuksen aikana. Tämän vuoksi suunniteltujen tuotantotilausten läpimenoaika voi olla erilainen kuin niistä luotujen liittyvien aikataulutettujen ja vahvistettujen tuotantotilausten läpimenoaika. Selitys:

- **Suunniteltu tuotantotilaus** – läpimenoaika perustuu vapautetun tuotteen staattiseen läpimenoaikaan.
- **Vahvistettu tuotantotilaus** – läpimenoaika perustuu reititystietoja ja liittyviä resurssirajoituksia käyttävään aikataulutukseen.

Lisätietoja toiminnon odotetusta saatavuudesta on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).

Jos tarvitset sellaista tuotannon toimintoa, joka ei ole vielä saatavana tuotannon optimoinnissa, voit jatkaa sisäisen pääsuunnittelumoduulin käyttöä. Mitään poikkeusta ei tarvita.

## <a name="delays"></a>Viiveet

Jos tarvittavan materiaalin läpimenoaika on pidempi kuin kuluvan päivän ja materiaalin tarvepäivän väliin jäävä jakso, tarvittavan materiaalin ja liittyvän tuotantotilauksen suunniteltu tilaus viivästyy. Viive lasketaan suunnitelluissa tilauksissa vapautetun tuotteen läpimenoajan perusteella. Tämän jälkeen viivetiedot leviävät sitten kaikille tuoterakenteen tasoille. Tällä tavoin viivästyneen raaka-aineen vaikutusta voidaan seurata asiakkaan myyntitilaukseen saakka.

## <a name="modifying-planned-orders"></a>Suunniteltujen tilausten muokkaaminen

Suunnitellun tilauksen tietojen muuttaminen aiheuttaa seuraavan sanoman: Huomaa, että suunniteltujen tilausten manuaaliset muutokset näkyvät muualla suunnitelmassa vasta seuraavan pääsuunnitteluajon jälkeen.

Suunniteltuun tilaukseen tehdyn muutoksen vaikutus liittyviin materiaalitarpeisiin saadaan näkyviin seuraavasti:

1. Päivitä suunniteltu tilaus.
2. Hyväksy suunniteltu tilaus.
3. Suorita pääsuunnittelu.

Jos suunnitellut tuotantotilaukset sisältyvät suoritettavaan pääsuunnitteluun, suodattimia ei voi käyttää. Lisätietoja on myöhemmin tässä aiheessa kohdassa [Suodattimet](#filters).

> [!NOTE]
> Jos suunnitellun tilauksen toimituspäivä muutetaan myöhempään ajankohtaan, tarvekohdistus saatetaan tehdä uuden suunnitellun tilauksen perusteella. Näin tapahtuu, jos uusi tarjontapäivä viivästyttää tarvekohdistusta mutta läpimenoasetusten perusteella viive voidaan välttää.

## <a name="explosion-page"></a>Hajotussivu

**Hajotus**-sivulla voidaan analysoida tietyn tuotantotilauksen tai suunnitellun tuotantotilauksen, liittyvän kattavuuden ja tarvekohdistustietojen kysyntää. **Hajotus**-sivun tiedot päivitetään pääsuunnittelun aikana. Tietoja ei voi päivittää suoraan **Hajotus**-sivulta.

## <a name="filters"></a><a name="filters"></a>Suodattimet

Jotta suunnittelun optimoinnilla on varmasti kaikki tiedot, joita tarvitaan oikean tuloksen laskemiseen, siihen on sisällyttävä kaikki tuotteet, jotka liittyvät jollain tavoin koko suunnitellun tilauksen tuoterakenteeseen. Tuotannon sisältävissä suunnitteluskenaarioissa ei siksi kannata käyttää suodatettuja pääsuunnitteluajoja,

Vaikka riippuvaiset alikohteet havaitaan automaattisesti ja sisällytetään pääsuunnitteluajoihin sisäistä pääsuunnittelumoduulia käytettäessä, niin ei tapahdu tällä hetkellä suunnittelun optimoinnissa.

Jos esimerkiksi yhtä tuotteen A tuoterakenteen pulttia käytetään myös tuotteen B tuottamiseen, kaikkien tuotteiden A ja B tuoterakenteiden tuotteiden on sisällyttävä suodattimeen. Koska voi olla monimutkaista varmistaa, että kaikki tuotteet sisältyvät suodattimeen, suodatettuja pääsuunnitteluajoja kannattaa välttää, jos kyse on tuotantotilauksesta. Muutoin pääsuunnittelusta saadaan ei-toivottuja tuloksia.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Syyt, joiden vuoksi ei suositella suodattamaan pääsuunnittelun ajoja

Kun suoritat tuotteelle suodatetun pääsuunnittelun, suunnittelun optimointi (toisin kuin sisäänrakennettu pääsuunnittelumoduuli) ei havaitse kaikkia tuotteen tuoterakenteen osatuotteita ja raaka-aineita eikä siksi sisällytä niitä pääsuunnitteluajoon. Vaikka suunnittelun optimointi tunnistaa tuotteen tuoterakenteen ensimmäisen tason, se ei lataa tietokannasta mitään tuoteasetuksia (kuten oletustilaustyyppiä tai nimikkeen kattavuutta).

Suunnittelun optimoinnissa suorituksen tiedot ladataan etukäteen ja suodattimia käytetään. Jos tiettyyn tuotteeseen sisältyvä osatuote tai raaka-aine ei kuulu suodattimeen, sitä koskevia tietoja ei siepata ajoa varten. Jos lisäksi osatuote tai raaka-aine sisältyy myös toiseen tuotteeseen, suodatettu suoritus, joka sisältää vain alkuperäisen tuotteen ja sen komponentit, poistaa aiemmin luodun, tälle toiselle tuotteelle luodun suunnitellun kysynnän.

Tämä logiikka saattaa aiheuttaa sen, että suodatetut pääsuunnittelun suoritukset aiheuttavat odottamattomia tuloksia. Seuraavissa osissa on esimerkkejä, jotka kuvaavat odottamattomia tuloksia, jotka voivat ilmetä.

### <a name="example-1"></a>Esimerkki 1

Valmis tuote *VT* koostuu seuraavista komponenteista:

- Raaka-aine *R*
- Osatuote *S1*, joka koostuu osatuotteesta *S2*

Raaka-ainetta *R* on varastossa, mutta osatuotetta *S1* ei ole varastossa.

Kun teet suodatetun pääsuunnittelun ajon valmiille tuotteelle *VT* saat suunnitellun tuotantotilauksen valmiille tuotteelle *VT*, suunnitellun ostotilauksen raaka-aineelle *R* ja suunnitellun ostotilauksen ja osatuotteelle *S1*. Tämä on ei-toivottu tulos, koska suunnittelun optimointi on ohittanut sen seikan, että raaka-aineiden *R* ja osatuote *S1* on tuotettava käyttäen osatuotetta *S2* sen sijaan, että se tilattaisiin suoraan. Näin on tapahtunut, koska suunnittelun optimoinnilla on vain valmiin tuotteen *VT* komponenttiluettelon ilman siihen liittyviä tietoja, kuten sen komponenttien tarjontaa tai oletustilausasetuksia.

### <a name="example-2"></a>Esimerkki 2

Edellisessä esimerkissä valmis lisätuote *VT2* käyttää myös osatuotetta *S1*. On olemassa suunniteltu tilaus valmiille tuotteelle *VT2*, ja kaikilla sen komponenteilla, myös komponentilla *S1*, on suunniteltu kysyntä.

Päätät poistaa suodatetun pääsuunnittelun ei-toivotut tulokset edellisestä esimerkistä lisäämällä kaikki osatuotteet ja raaka-aineet valmiin tuotteen *VT* tuoterakenteesta suodattimeen ja suorittamalla sitten täyden uudelleenmuodostuksen.

Kun suoritat täyden uudelleenluomisen, järjestelmä poistaa kaikkien sisältyvien tuotteiden kaikki tulokset ja luo sitten tulokset uudelleen uusien laskelmien perusteella. Tämä tarkoittaa, että olemassa oleva suunniteltu tarve tuotteelle *S1* poistetaan ja sen jälkeen luodaan uudelleen ottaen huomioon vain valmiin tuotteen *VT* tarpeet, kun jätetään huomioimatta valmiin tuotteen *VT2* tarpeet. Näin tapahtuu, koska kun suoritat suunnittelun optimoinnin, se ei sisällä muiden suunniteltujen tuotantotilausten suunniteltua kysyntää, vain suorituksen aikana luotua suunniteltua kysyntää käytetään.

> [!NOTE]
> Jos olemassa oleva valmiin tuotteen *VT2* suunniteltu tilaus tilassa *Hyväksytty*, hyväksytty suunniteltu kysyntä sisällytetään myös silloin, kun päätuotetta ei lisätä suodattimeen.

Näin ollen jos et lisää kaikkia komponentteja valmiille tuotteelle *VT*, valmiille tuotteelle *VT2* ja muille tuotteille, joiden osia nämä komponentit ovat (omine komponentteineen), suodatettu pääsuunnittelun ajo tuottaa ei-toivotut tulokset.

Koska voi olla monimutkaista varmistaa, että kaikki tuotteet sisältyvät suodattimeen, suodatettuja pääsuunnitteluajoja kannattaa välttää, jos kyse on tuotantotilauksesta.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
