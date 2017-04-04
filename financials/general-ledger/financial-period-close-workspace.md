---
title: "Tilikauden sulkemisen työtila"
description: "Tässä artikkelissa on tilikauden sulkemisen työtilan ja liittyvän konfiguraation yleiskatsaus."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Tilikauden sulkemisen työtila

Tässä artikkelissa on tilikauden sulkemisen työtilan ja liittyvän konfiguraation yleiskatsaus.

Tilikauden sulkemisen työtila

**Sulje tilikausi** työtilan avulla voit hallita sulkemisen taloudellisia prosesseja yritykset, alueet ja ihmiset. Näytön mukaan **Sulje tilikausi** työtila, näet joko kaikki tehtävät ja tilojen sulkeminen aikataulun tai juuri sinulle määritettyjä tehtäviä. 

Valitse työtilan yläosassa sulkeminen aikataulun. Työtilassa näkyvät kaikki tiedot on suodatettu sitten valittu sulkeminen aikataulun mukaan.

### <a name="summary-tiles"></a>Yhteenvetoruudut

**Yhteenveto**-ruudut sisältävät prosessin yleiskuvauksen. Mittareiden avulla voit seurata sulkemisprosessia. Saat näkyviin tehtävät, jotka edelliset jäljellä olevien tehtävien määräpäivä tänään, tehtävät, joiden määräaika on tänään, mutta koska riippuvuudet ja prosessin kaikki jäljellä olevat tehtävät. Nämä tiedot on tarkoitettu kaikille yrityksille, jotka sisältyvät valittu sulkeminen aikataulu.

### <a name="tasks-and-status-section"></a>Tehtävät ja tila -osa

- **Tehtävät ja tilan** kokonaisvaikutus tilan osan sulkeminen aikataulu on eriteltynä eri tavoin: yritys, alueen tila ja tilan mukaan henkilö, joka vastaa tilan. Voit tarkastella tilaa, sulkeminen kaikkien tehtävien ajoittaminen vain tehtävät, joiden määräpäivä on tänään, tai tehtäviä, jotka ovat erääntyneet vaihtamalla suodattimen kortti-luettelon yläosassa. Voit myös valita yrityksen suodatin voit tarkastella yrityksen tilaa. Jokainen tila-välilehti antaa jaottelu on suoritettu prosenttiosuus sekä jäljellä olevat tehtävien määrä. Valitse kortti tai **tarkastella** toiminnon yksityiskohtainen tehtäväluettelo suodatuksessa valittu kortti. 

Yksityiskohtainen tehtäväluettelo on viimeinen välilehti. Tämä luettelo näyttää koko tehtäväluettelon ja voidaan suodattaa niin, että siinä näkyvät vain ne tehtävät, joista olet kiinnostunut. Voit suodattaa tehtäväluettelon monin tavoin. Voit suodattaa esimerkiksi tehtävän määräpäivän, yrityksen ja liittää alueen mukaan. Voit myös valita, näyttää tai piilottaa valmiit tehtävät tehtäväluettelossa. 

Tehtävissä käytetään kahta mittaria.

-   Huutomerkki-kuvake ilmaisee, että tehtävä on myöhässä. Tehtävissä, jotka ovat erääntyneet eräpäivä on myös korostettu punaisella.
-   Lukkokuvake ilmaisee tehtävän riippuu muita tehtäviä, jotka eivät ole vielä valmiita. Tehtävä, joka on estänyt riippuvuuksia ei voi merkitä valmiiksi. Voit määrittää tehtävän riippuvuuksien **määrittää riippuvuus** toiminto.

Tehtävänimi on hyperlinkin Microsoft Dynamics-365 Toiminnot-sivun-tai muiden WWW-sivun, jossa käyttäjän täytyy mennä työn suorittamiseen. Voit määrittää hyperlinkin **tehtävälinkki** kentän mukaan, kun muokata tai luoda tehtävän. 

Voit liittää tiedostoja, muistiinpanoja, kuvia ja URL-osoitteiden tehtävän avulla **liitteet** toiminto. Voit esimerkiksi määrittää kirjauskansion numeroita, joita käytetään osana tehtävän, lisätä kommentteja tiettyyn tehtävään tai liitetiedoston lisääminen raportin, joka tulostettiin tehtävän. Kuvake näkyy **liitteen** -sarakkeesta tehtävä, jos liite on läsnä. 

**Tehtävän loppuun** vaihtoehto on manuaalisesti valittava tehtävän päättymisen jälkeen. Tehtävä on merkitty suoritetuksi, kun **päivämäärän suorittanut** kenttä päivittyy automaattisesti nykyinen päivämäärä ja aika. Riippuvuus indikaattoreita päivitetään tarpeen mukaan.

## <a name="all-financial-period-close-tasks-list-page"></a>Kaikkien tilikauden sulkemisen tehtävien luettelosivu
Voit tarkastella kaikkia nykyisen ja edellisen kauden sulkeminen tehtäviä **Sulje tilikausi kaikki tehtävät** sivulla. Tämä sivu kannattaa käyttää sulkemisprosessin, historiallinen analyysi, koska se sisältää tiedot suunnitellun eräpäivä, todellinen valmistumispäivä, ja henkilö, joka suorittaa tehtävän. Voit helposti viedä tiedot luetteloon tällä sivulla Microsoft Exceliin raportoinnin ja seurannan tarkoitusta.

## <a name="financial-period-close-configuration-page"></a>Tilikauden sulkemisalueen konfigurointi -sivu
Ennen kuin voit käyttää **Sulje tilikausi** työtila, prosessi on määritettävä Microsoft Dynamics-365 toimintojen avulla **taloudellisen kauden Sulje kokoonpanon** sivulla. (Valitse **kirjanpidon**&gt;**kauden sulkeminen**&gt;**taloushallinnon kauden Sulje kokoonpanon**.)

### <a name="resources"></a>Resurssit

- **Resurssien** -välilehdessä voit määrittää henkilöt, jotka osallistuvat sulkeminen prosessit ovat. Tahansa työntekijä, joka on vastuussa tehtävän sulkeminen on ensin määritettävä tähän. On myös määritettävä työntekijän Näytä työtilan. Valittavissa ovat seuraavat vaihtoehdot:

-   **Vain määritetyt tehtävät** – Käyttäjä näkee vain hänelle määritetyt tehtävät.
-   **Kaikki tehtävät ja tila** – Käyttäjä näkee kaikki sulkemistehtävät ja yleisen prosessin tilan.

Käyttäjät, joilla on vain heille määritettyjen tehtävien katseluoikeus, eivät voi lisätä tehtäviä tehtäväluetteloon, muokata tehtäviä tai poistaa tehtäviä tehtäväluettelosta.

### <a name="task-areas"></a>Tehtäväalueet

Tehtäväalueiden avulla voi ryhmitellä sulkemistehtäviä omistusoikeuden loogisiin alueisiin organisaatiossa. Tehtäväalueina voidaan käyttää esimerkiksi ostoreskontraa, myyntireskontraa tai kirjanpitoa.

### <a name="calendars"></a>Kalenterit

Luo ja muokkaa taloushallinnon sulkeminen kalenterin kalenterit-välilehdessä.  Tämä on missä määrittää työpäivän prosessien sulkeminen ja sitä käytetään sulkeminen tehtävien ajoitukseen.  Luo uusi kalenteri ja Määritä työpäivät, jota käytetään tehtävien ajoitukseen.  On parasta luoda kalenterin pitkän ajan kuluessa, kuten vuodessa tai usean vuoden jälkeen sitä voidaan muokata luomisen jälkeen.  Kun olet luonut kalenterin, valitse Muokkaa-painike päivittää kalenteri tietyille päiville, kuten lomat.  Sulkeminen tehtävät ajoitetaan päivinä, kun ohjausobjektin arvoksi on määritetty Avoin.  Tehtävien sulkeminen ei pitäisi aikataulun tiettynä päivänä, jos kyseisen päivän on suljettu ohjausobjektin arvo.

### <a name="templates"></a>Mallit

Sulje taloudellisen mallin avulla voit määrittää kaikki tehtävät, jotka ovat osa sulkemisen prosessia. Viimeinen tehtävä on toistuvan työn vaivalla, joka annetaan yksittäiselle suorittamiseen kunkin sulkemisen yhteydessä. Suhteellinen määräpäivä-mallissa päivämäärä on määritettävä kunkin tehtävän sulkeminen. Suhteellinen määräpäivä on, kuinka monta päivää ennen tai jälkeen määritetyn kauden viimeinen päivämäärä, jolloin tehtävä on saatava päätökseen kunkin kauden. Eräpäivä aika on määritelty myös kunkin tehtävän. Erääntymisaika on määritetty käyttämällä aikavyöhykkeen puitteissa ja muunnetaan aikavyöhykkeen kullekin käyttäjälle. 

Voit määrittää mallin tehtävän yhtiöihin, johon sovelletaan kyseiseen tehtävään. Jos henkilölle on määritetty loppuun jokaisen yrityksen työtä, vaivaa, voi olla helpompaa kannattaa luoda samaa työtä vaivaa useita tehtäviä. Luo kullekin yritykselle yksi tehtävä. 

**Tehtävälinkki** valikkovaihtoehto on liitetty tehtävän työn vaivaa ja avulla voit siirtyä suoraan siihen liittyvä sivu-työtilassa tehtävään-linkistä. Esimerkiksi tehtävän suoritettavaksi valuutan uudelleenarvostuksen prosessin ostoreskontran sulkemisen linkitetty liittyviin **ulkomaanvaluutan uudelleenarvostuksen** -sivulla Microsoft Dynamics-365 operaatioille. Myös ulkoisen URL-osoitteen voi linkittää. 

> [! Vihje] Jos haluat linkittää Management Reporter tietyn raportin taloushallinnon kauden sulje tehtävä, voit määrittää raportin URL-osoite. Avaa raportti report designer käyttää raportin URL-osoite, ja valitse sitten **tiedosto**&gt;**tarkastella raporttia** voit avata raportin web-selaimessa. Tämän jälkeen voit kopioida URL-osoitteen selaimen osoiteriviltä ja liittää sen **tehtävälinkin** **URL**-kenttään. 

Voit määrittää mallin tehtävien välisiä riippuvuussuhteita. Jos tehtävälle on määritetty, yksi tai useampi tehtävä vaikuttaa kyseistä tehtävää ei voi merkitä valmiiksi, kunnes kaikki riippuvuudet täyttyvät. 

Voit luoda useita Sulje taloudellisia malleja. Voit käyttää sitten eri mallien avulla voit seurata sulkemista käsitellään kauden tyyppejä, kuten kuukauden lopussa tai vuoden lopussa tai yritykset, jotka käyttävät sulkeminen eri prosessien seurata. Kun yksi malli on luotu, voit kopioida sen uuden mallin ja tee tarvittavat muutokset. Voit määrittää vain yhden mallin kunkin sulkemisen ajoitus.

### <a name="closing-schedules"></a>Sulkemisaikataulut

Sulkeminen aikataulun avulla voit määrittää tietyn tilikausi on suljettu, sulje taloudellinen malli. Mallin tehtävät luodaan sitten automaattisesti tietyn ajan ja sulkeminen uusi aikataulu on lisätä työtilaan. Luotaessa uusi sulkeminen, aikataulu **kauden päättymispäivä** kenttää käytetään määrittämään todellinen asianmukaisesti sulkeminen-tehtävien perusteella on suhteellinen eräpäivä Päivämäärä, jolloin on määritetty taloushallinnon Sulje malli. 

Osoittaa asianmukainen sulkemista aikataulun työpäivän Tehtävien ajoituksessa käytetään osoittamaan kalenteri. Jos et määritä haluamasi kalenterin, tehtävän määräpäivä päivämäärät on käyttää kaikki viikonpäivät. 

Voit myös määrittää yrityksiä, joihin ei liity päättävän aikataulusta. Jos mallin tehtävät on varattu useita yrityksiä, kullekin yritykselle, jolla on päättävän aikataulusta ja mallin tehtävään luodaan erilliset tehtävät. 

Aikataulun sulkemisen jälkeen, valitse **suljettu** se vaihtoehto. Tehtävähistoria on edelleen käytettävissä **Sulje tilikausi kaikki tehtävät** sivu, mutta sulkeminen aikataulu poistetaan työtilasta. Kun sulkeminen aikataulu on merkitty **suljettu**, et voi lisätä tehtäviä, muokata tehtäviä tai poistaa tehtäviä.


