---
title: "Tilikauden sulkemisen työtila"
description: "Tässä artikkelissa on tilikauden sulkemisen työtilan ja liittyvän konfiguraation yleiskatsaus."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0bbf8f979aeb8b861164e345f9e46bb396f370ce
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="financial-period-close-workspace"></a>Tilikauden sulkemisen työtila

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on tilikauden sulkemisen työtilan ja liittyvän konfiguraation yleiskatsaus.

Tilikauden sulkemisen työtila

**Tilikauden sulkemisen**  työtilassa voit seurata tilikauden sulkemisprosesseja yritysten, alueiden ja henkilöiden osalta. **Tilikauden sulkemisen** työtilasta riippuen näkyvillä ovat kaikki sulkemisaikataulun tehtävät ja tilat tai vain sinulle määritetyt tehtävät. 

Valitse ensin sulkemisaikataulu työtilan yläosassa. Kaikki työtilassa näkyvät tiedot suodatetaan valitun sulkemisaikataulun mukaan.

### <a name="summary-tiles"></a>Yhteenvetoruudut

**Yhteenveto**-ruudut sisältävät prosessin yleiskuvauksen. Mittareiden avulla voit seurata sulkemisprosessia. Näkyvillä ovat erääntyneet tehtävät, kuluvan päivän jäljellä olevat tehtävät, kuluvana päivänä erääntyvät, mutta riippuvuuksien vuoksi estetyt tehtävät sekä kaikki prosessin jäljellä olevat tehtävät. Nämä tiedot koskevat kaikkia valittuun sulkemisaikatauluun liittyviä yrityksiä.

### <a name="tasks-and-status-section"></a>Tehtävät ja tila -osa

**Tehtävät ja tila** -osassa yleisen sulkemisaikataulun tila eritellään useilla eri tavoilla: tila yrityksen mukaan, tila alueen mukaan ja tila vastuuhenkilön mukaan. Voit tarkastella näiden tehtävien tilaa sulkemisaikataulussa, vain kuluvana päivänä erääntyvissä tehtävissä tai erääntyneissä tehtävissä, muuttamalla korttiluettelon yläosassa olevaa suodatinta. Voit myös valita yrityssuodattimen, kun haluat tarkastella tietyn yrityksen tilaa. Kukin tilavälilehti sisältää erittelyn sekä valmistuneiden prosenttiosuuden että jäljellä olevien tehtävien määrän mukaan. Suodata yksityiskohtainen tehtäväluettelo valitun kortin mukaan valitsemalla kortti tai **Näytä tiedot** -toiminto. 

Viimeinen välilehti sisältää yksityiskohtaisen kaikki tehtävät sisältävän tehtäväluettelon. Luettelo voidaan suodattaa niin, että näkyvillä ovat vain käyttäjää kiinnostavat tehtävät. Tehtäväluettelon voi suodattaa useilla eri tavoilla. Luettelo voidaan suodattaa esimerkiksi tehtävän eräpäivän, liittyvän yrityksen ja liittyvän alueen perusteella. Myös tehtäväluettelon valmiit tehtävät on mahdollista näyttää tai piilottaa. 

Tehtävissä käytetään kahta mittaria.

-   Huutomerkkikuvake osoittaa, että tehtävä on erääntynyt. Erääntyneiden tehtävien eräpäivä näkyy punaisena.
-   Lukkokuvake osoittaa, että tehtävä on riippuvainen muista tehtävistä, jotka eivät ole vielä valmiita. Tehtävää, joka on estetty riippuvuuksien vuoksi, ei voi merkitä valmiiksi. Voit määrittää tehtävän riippuvuudet **Määritä riippuvuus** -toiminnon avulla.

Tehtävän nimi on Microsoft Dynamics 365 for Operations -sivun tai muun sellaisen verkkosivun hyperlinkki, jolla käyttäjä suorittaa työn valmiiksi. Voit määrittää hyperlinkin valitsemalla **Tehtävälinkki**-kentän tehtävän muokkauksen tai luomisen yhteydessä. 

Voit liittää tehtäviin tiedostoja, huomautuksia, kuvia ja URL-osoitteita **Liitteet**-toiminnon avulla. Voit esimerkiksi osoittaa tehtävän osana käytettävien kirjauskansioiden määrän, lisätä tiettyä tehtävää koskevia kommentteja tai liittää tehtävälle tulostetun raporttitiedoston. Tehtävän **Liite**-sarakkeessa näkyy kuvake, jos liite on määritetty. 

**Tehtävä valmis** -vaihtoehto on valittava manuaalisesti tehtävän valmistuttua. **Valmistumispäivämäärä**-kenttään päivitetään automaattisesti kuluva päivämäärä ja kellonaika. Riippuvuuden mittarit päivitetään myös tarpeen mukaan.

## <a name="all-financial-period-close-tasks-list-page"></a>Kaikkien tilikauden sulkemisen tehtävien luettelosivu
Voit tarkastella kuluvan ja edellisen kauden suljettuja tehtäviä **Kaikki tilikauden sulkemisen tehtävät** -luettelosivulla. Luettelosivua kannattaa käyttää erityisesti sulkemisprosessin historiallisessa analyysissä, koska luettelosivu sisältää ajoitetun eräpäivän, toteutuneen valmistumispäivän ja tehtävän suorittaneen henkilön tietoja. Voit viedä luettelosivun tiedot helposti Microsoft Exceliin raportointia ja tarkistusta varten.

## <a name="financial-period-close-configuration-page"></a>Tilikauden sulkemisalueen konfigurointi -sivu
Ennen kuin **tilikauden sulkemisen** työtilaa voi käyttää, prosessi on määritettävä Microsoft Dynamics 365 for Finance and Operationsissa **Tilikauden sulkemisalueen konfigurointi** -sivulla. (Valitse **Kirjanpito** &gt; **Kauden sulkeminen** &gt; **Tilikauden sulkemisalueen konfigurointi**.)

### <a name="resources"></a>Resurssit

Määritä **Resurssit**-välilehdessä sulkemisprosesseissa mukana olevat henkilöt. Sulkemistehtävästä vastuussa oleva työntekijä on määritettävä tässä ensin. Myös työtilan työntekijän näkymä on määritettävä. Valittavissa ovat seuraavat vaihtoehdot:

-   **Vain määritetyt tehtävät** – Käyttäjä näkee vain hänelle määritetyt tehtävät.
-   **Kaikki tehtävät ja tila** – Käyttäjä näkee kaikki sulkemistehtävät ja yleisen prosessin tilan.

Käyttäjät, joilla on vain heille määritettyjen tehtävien katseluoikeus, eivät voi lisätä tehtäviä tehtäväluetteloon, muokata tehtäviä tai poistaa tehtäviä tehtäväluettelosta.

### <a name="task-areas"></a>Tehtäväalueet

Tehtäväalueiden avulla voi ryhmitellä sulkemistehtäviä omistusoikeuden loogisiin alueisiin organisaatiossa. Tehtäväalueina voidaan käyttää esimerkiksi ostoreskontraa, myyntireskontraa tai kirjanpitoa.

### <a name="calendars"></a>Kalenterit

Luo ja muokkaa tilikauden sulkemiskalentereita Kalenterit-välilehdessä. Välilehdessä määritetään sulkemisprosessien työpäivät. Sitä käytetään myös sulkemistehtävien ajoituksessa.  Luo uusi kalenteri ja määritä tehtävän ajoituksessa käytettävät työpäivät.  Kalenteri kannattaa luoda pitkälle aikavälille, kuten vuodeksi tai useiksi vuosiksi, koska sitä ei voi muokata luomisen jälkeen.  Kun kalenteri on luotu, kalenterin tietyt päivät, kuten lomat, päivitetään Muokkaa-painikkeen avulla.  Sulkemistehtävät ajoitetaan päiville, joiden Ohjausarvo-kohdan arvoksi on määritetty Avoin.  Jos sulkemistehtäviä ei ajoiteta tietylle päivälle, kyseisen päivän Ohjausarvo-kohdan arvoksi on määritettävä Suljettu.

### <a name="templates"></a>Mallit

Tilikauden sulkemismallin avulla voi määrittää kaikki sulkemisprosessin osana olevat tehtävät. Sulkemistehtävä on toistuva työ, joka määritetään henkilölle ja joka tehdään valmiiksi sulkemisprosessin osana. Jokaiselle sulkemistehtävälle on määritettävä suhteellinen eräpäivä mallissa. Suhteellinen eräpäivä tarkoittaa niiden päivien määrää, joka kunkin kauden erääntyvällä tehtävällä on jäljellä määritetyn kauden päättymispäivämäärään tai niiden päivien määrää, joka kyseisestä päättymispäivämäärästä on kulunut. Jokaiselle tehtävälle määritetään myös erääntymisaika. Erääntymisaika määritetään kunkin käyttäjän käyttämän aikavyöhykkeen kontekstissa. 

Voit määrittää tehtävän mallissa yhdelle yritykselle tai useille yrityksille, joissa tehtävä on käytössä. Jos tehtävän suorittava henkilö on eri kussakin yrityksessä, samalle työlle kannattaa ehkä luoda useita tehtäviä. Luo kullekin yritykselle yksi tehtävä. 

**Tehtävälinkki**-valikko liitetään tehtävän työhön. Sitä voidaan käyttää suoraan työtilan tehtävälinkin liittyvältä sivulta. Esimerkiksi ostoreskontran valuutan uudelleenarvostusprosessin suorittamisessa käytettävä sulkemistehtävä voidaan linkittää Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioniin liittyvään **Ulkomaanvaluutan uudelleenarvostus** -sivulle. Myös ulkoisen URL-osoitteen voi linkittää. 

> [!Vihje] Jos haluat linkittää tilikauden sulkemistehtävään tietyn Management Reporter -raportin, voit käyttää raportin URL-osoitetta. Voit käyttää raportin URL-osoitetta, kun avaat raportin Report Designer -ohjelmassa ja avaat raportin selaimeen valitsemalla **Tiedosto** &gt; **Näytä raportti**. Tämän jälkeen voit kopioida URL-osoitteen selaimen osoiteriviltä ja liittää sen **tehtävälinkin** **URL**-kenttään. 

Voit määrittää mallissa tehtävän riippuvuudet. Jos tehtävä on määritetty niin, että se riippuu vähintään yhdestä tehtävästä, sen voi merkitä valmiiksi vasta sitten, kun kaikki riippuvuudet on tehty valmiiksi. 

Voit luoda useita tilikauden sulkemismalleja. Eri mallien avulla voi seurata sulkemisprosesseja erilaisissa kausityypeissä, kuten kuukauden loppu tai vuoden loppu, tai yrityksiä, jotka käyttävät erilaisia sulkemisprosesseja. Kun yksi malli on luotu, voit kopioida sen uuteen malliin ja tehdä tarvittavat muutokset. Kuhunkin sulkemisaikatauluun voi liittää vain yhden mallin.

### <a name="closing-schedules"></a>Sulkemisaikataulut

Sulkemisaikataulua käytetään liitettäessä tilikauden sulkemismalli määritettyyn suljettavaan tilikauteen. Tämän jälkeen mallin tehtävät luodaan automaattisesti määritetylle kaudelle ja työtilaan lisätään uusi sulkemisaikataulu. Kun uusi sulkemisaikataulu luodaan, sulkemistehtävien toteutuneet eräpäivät määritetään **Kauden päättymispäivä** -kentän avulla tilikauden sulkemismalliin liitetyn suhteellisen eräpäivän perusteella. 

Liitä sulkemisaikatauluun sopiva kalenteri tehtävän ajoituksessa käytettävien työpäivien määrittämistä varten. Jos et määritä tiettyä kalenteria, tehtävien eräpäivissä käytetään kaikkia viikonpäiviä. 

Määritä myös sulkemisaikatauluun liittyvät yritykset. Jos mallin tehtävät liitetään useisiin yrityksiin, jokaiselle sulkemisaikatauluun liittyvälle ja mallin tehtävään liitetylle yritykselle luodaan erilliset tehtävät. 

Kun sulkemisaikataulu on valmis, valitse sille **Suljettu**-vaihtoehto. Tehtävän historia on yhä käytettävissä **Kaikki tilikauden sulkemisen tehtävät** -luettelosivulla, mutta sulkemisaikataulu poistetaan työtilasta. Kun sulkemisaikataulu on merkitty **suljetuksi**, aikatauluun ei voi lisätä tehtäviä, sen tehtäviä ei voi muokata eikä siitä voi poistaa tehtäviä.




