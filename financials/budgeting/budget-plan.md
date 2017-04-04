---
title: Budjettisuunnittelu
description: "Tämän kurssin tavoitteena on antaa näkymän Ohjattu Microsoft Dynamics-365 budjettisuunnittelun alueen toimintoja päivitysten toiminnot. Tämä kurssi sisältää nopean konfiguraatioesimerkin budjettisuunnittelumoduulista ja esittelee, miten budjettisuunnittelu voidaan suorittaa tämän konfiguraation avulla.  Tällä kurssilla keskitytään erityisesti seuraavista liiketoimintaprosessien tai tehtävien--organisaation hierarkian luominen budjetin suunnittelussa ja käyttäjän suojauksen konfiguroinnissa - budjettisuunnitelman skenaariot, budjettisuunnitelman sarakkeet, asetteluja ja luominen ja aktivoiminen talousarvion suunnittelun prosessi - luodaan budjettisuunnitelman asiakirjan mukaan todelliset kirjanpidon sisäänpäin - avulla voit säätää suunnitelman asiakirjan budjettitiedot kohdistukset - muokkausta budjettisuunnitelman asiakirjan tietoja Excelissä Excel - mallien määrittäminen"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Budjettisuunnittelu

Tämän kurssin tavoitteena on antaa näkymän Ohjattu Microsoft Dynamics-365 budjettisuunnittelun alueen toimintoja päivitysten toiminnot. Tämä kurssi sisältää nopean konfiguraatioesimerkin budjettisuunnittelumoduulista ja esittelee, miten budjettisuunnittelu voidaan suorittaa tämän konfiguraation avulla.  Tällä kurssilla keskitytään erityisesti seuraavista liiketoimintaprosessien tai tehtävien--organisaation hierarkian luominen budjetin suunnittelussa ja käyttäjän suojauksen konfiguroinnissa - budjettisuunnitelman skenaariot, budjettisuunnitelman sarakkeet, asetteluja ja luominen ja aktivoiminen talousarvion suunnittelun prosessi - luodaan budjettisuunnitelman asiakirjan mukaan todelliset kirjanpidon sisäänpäin - avulla voit säätää suunnitelman asiakirjan budjettitiedot kohdistukset - muokkausta budjettisuunnitelman asiakirjan tietoja Excelissä Excel - mallien määrittäminen 

<a name="prerequisites"></a>Edellytykset 
------------------

Varten tämä opetusohjelma sinun on käyttää Dynamics-365 Contoso esittely tietoja ympäristön toimintojen ja valmisteltava esiintymässä järjestelmänvalvojana. Älä käytä selaimen yksityinen-tilassa - kurssin tarvittaessa ulos muiden selaimessa tililtä ja kirjaudu sisään Dynamics 365 toimintoja järjestelmänvalvojan tunnistetietoja. Kirjautumalla järjestelmään Dynamics 365 toimintoja, kun olet **on** "Pysy kirjautuneena"-valintaruutu. Se luo Excel-sovellukseen pysyvän esteen, jota se parhaillaan tarvitsee. Jos kirjaudut Dynamics-365 toimintoihin kuin IE-selaimella, sitten sinua pyydetään kirjautumaan sisällä Excel-sovellus. Kun valitset "Kirjaudu sisään" Excel-sovelluksessa, Internet Explorer -ponnahdusikkuna avautuu ja kun kirjaudut sisään, sinun **TÄYTYY** merkitä valintaruutu "Pidä minut sisäänkirjautuneena". Jos mitään ei tapahdu, kun napsautat Excel-sovelluksen "Kirjaudu sisään" -painiketta, sitten sinun kannattaa tyhjentää Internet Explorerin väimuistin evästeet.

## <a name="scenario-overview"></a>**Scenario overview**
Julia toimii talouspäällikkönä Contoso Entertainment Systemsissä Saksassa (DEMF). Kun FY2016 lähestyy, hänen on määritettävä yrityksen budjetti tulevalle vuodelle. Budjetin valmistelu näyttää seuraavanlaiselta:

1.  Julia käyttää edellisvuoden toteutuneita summia budjetin luomisen lähtökohtana.
2.  Perustuen edellisen vuoden toteutuneisiin summiin, hän luo 12 kuukauden arviot seuraavalle vuodelle
3.  Julia tarkistaa budjettitapahtumat talousjohtajan kanssa. Kun se on tehty, hän tekee tarvittavat oikaisut budjettisuunnitelmaan ja viimeistelee budjetin valmistelun.

Budjetin rakenteen kokoonpano skenaario näyttää seuraavalla tavalla:

![Screenshot1](./media/screenshot1-300x152.png)

Julia valmistelee talousarvion käyttää seuraavassa Excel-malli:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Harjoitus 1: Määritys
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Vaihe 1: Luo organisaation hierarkian**
Koska kaikki budjetointiprosessissa tapahtuu talousosastolla, Julian on luotava helppo organisaatiohierarkia, joka koostuu vain taloushallinto-osastosta. 1.1. Siirry organisaatiohierarkiat (organisaation hallinta &gt;organisaatioissa &gt;organisaatiohierarkiat) ja napsauta Uusi-painiketta

![Screenshot3](./media/screenshot3.png) 

1.2. Organisaation hierarkian nimi ja valitse painike Määritä tarkoitus

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Valitse budjetin tarkoituksen, napsauttamalla Lisää-painiketta ja juuri luotu Organisaatiohierarkian määrittäminen: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Toista edellä oleva vaihe "Organisaation tarkoituksen turvatoimille". Sulje lomake kun se on tehty.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Organisaation hierarkiat -lomakkeessa klikkaa "Näytä"-painiketta. Valitse "Muokkaa" Hierarkian suunnittelussa ja luo hierarkia klikkaamalla "Lisää"-painiketta.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Valitse "Talousosasto" budjetoinnin hierarkiaan. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kun olet valmis, klikkaa painiketta "Julkaise" ja "Sulje". Valitse 1/1/2015 hierarkian julkaisemisen voimaantulopäiväksi.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Vaihe 2: Käyttäjäryhmän suojauksen määrittäminen
Budjettisuunnittelussa käytetään erityisiä suojauskäytäntöjä määrittämään pääsy budjettisuunnitelmien tietoihin. Julian on annettava käyttöoikeus taloushallinnon budjettisuunnitelmiin itselleen. 2.1. Siirry DEMF oikeushenkilöön yhteydessä: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Siirry budjetoinnin &gt;asennus &gt;budjettisuunnittelua &gt;budjettisuunnittelun konfiguraatio. Parametrit-välilehdessä arvo on suojaus malli perustuu organisaatioiden tietoturva- [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Siirry järjestelmän hallinta &gt;käyttäjät &gt;käyttäjille. Anna käyttäjien hallinnalle (Julia Funderburk) budjetin hallitsijan rooli. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Käyttäjäroolin Poimi ja valitse Määritä organisaatiot [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Valitse "Myönnä käyttöoikeudet yksittäisille organisaatioille". Valitse ensimmäisessä vaiheessa luotu "Organisaatiohierarkia". Poimi viivästyskululaskun solmu ja valitse avustuksen lasten painikkeella ***tärkeää!*** *– Varmista, että että olet DEMF oikeushenkilöön yhteydessä suoritettaessa tämän tehtävän suojauksen sovellettuna oikeushenkilöittäin*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Tehtävä 3: Luo skenaarioita
3.1. Siirry budjetoinnin&gt;asennus &gt;budjettisuunnittelua &gt;budjettisuunnittelun konfiguraatio. "Skenaariot"-sivulla, pane merkille ne skenaariot, joita käytämme myöhemmin tällä kurssilla: edellisen vuoden todeutuneet ja budjetoidut. *Huomautus: Voit luoda tarvittaessa uusia tilanteita tähän harjoitukseen ja käyttää niitä näiden sijaan.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Huomautus: Julia ei käytä muodollista hyväksymisprosessin budjetin valmistelua varten, emme ohittaa vaiheita työnkulut ja työnkulun vaiheita tällä asetukset ja käyttää olemassa olevat asetukset automaattinen – Hyväksy työnkulkua. Katso liite tämän työnkulkumääritystä varten.*

## <a name="task-4-create-budget-plan-columns"></a>Tehtävä 4: Luo budjettisuunnitelmalle sarakkeet
Budjettisuunnitelman sarakkeet ovat joko rahaan tai määrään perustuvia sarakkeita, joita voidaan käyttää budjettisuunnitelman asiakirjan asetteluun. Esimerkissämme meidän on luotava sarake edellisen vuoden todellisille arvoille ja 12 saraketta, jotka edustavat budjetoidun vuoden kutakin kuukautta. Sarakkeita voidaan luoda joko klikkaamalla "Lisää"-painiketta ja kirjoittamalla arvot, tai tietoyksikön avulla. Tällä kurssilla käytämme tietoyksikköä syöttämään arvot. 4.1. Budjetoinnissa&gt;asennus &gt;budjettisuunnittelua &gt;budjetin suunnittelu Avaa sarakkeita määrityssivulla. Napsauta Office-painiketta lomakkeen oikeaan yläkulmaan ja valitse sarakkeet (suodattamattoman) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Järjestelmä avaa Excel-työkirjan, jota käytetään arvojen kirjoittamiseen. Pyydettäessä, valitse Ota muokkaus käyttöön ja luota tämän sovelluksen [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Tarvitsemme enemmän sarakkeiden arvojen täyttäminen. Napsauta rakenne-oikeanpuoleisessa ruudussa voit lisätä ruudukon sarakkeet: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Valitsemalla vähän kynä vieressä, jos haluat nähdä käytettävissä olevat sarakkeet voit lisätä ruudukon PlanColumns [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Kaksoisnapsauta käytettävissä olevat kenttien lisääminen valitut kentät ja valitse Päivitä- [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Lisää kaikki sarakkeet, jotka on luotava, Excel-taulukkoon. Lisää rivejä nopeasti Excelin automaattisnen täyttö -toiminnon avulla. Varmista, että rivit lisätään taulukon osana (Pystysuora käärö käytettäessä voidaan nähdä seuraavia ruudukon sarakkeiden otsikoita) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Palaa Dynamics 365 operaatioille ja Päivitä sivu. Julkaistu arvot näkyvät Dynamics 365 operaatioille. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Tehtävä 5: Luo budjettisuunnitelma asiakirjan suunnitelmat ja mallit
Asettelu määrittää, miltä budjettisuunnitelman asiakirjan rivien ruudukko näyttää, kun käyttäjä avaa budjettisuunnitelma-asiakirjan. On myös mahdollista siirtää budjettisuunnitelman asiakirjan tekstin asettelu niin, että voidaan katsoa samoja tietoja eri suunnalta. Nyt kun hän on määrittänyt sarakkeet, joita käytetään budjettisuunnittelu asiakirjassa, Julian on luotava budjettisuunnitelma asiakirjan asettelu, joka näyttää samanlaiselta kuin Excel-taulukko, jota hän käyttää budjettitietojen luomiseen (Katso "Skenaarion yhteenveto" -osa tässä kurssissa) 5.1. Budjetoinnissa&gt;asennus &gt;budjettisuunnittelua &gt;budjetin suunnittelu Avaa asettelut määrityssivulla. Luo uusi asettelu kuukausittaiselle budjettitapahtumalle:

-   Valitse MA+BU dimensioyhdistelmä sisällyttämään päätilit ja liiketoimintayksiköt asettelussa.
-   Listaa kaikki budjettisuunnitelman sarakkeet, jotka luotiin edellisessä vaiheessa "Elementit"-osiossa. Tee kaikista paitsi edellisen vuoden todellisista arvoista muokattavia.
-   Klikkaa "Kuvaukset"-painiketta valitaksesi minkä taloushallinnon dimensioiden tulisi näkyä "Kuvaukset"-ruudukossa.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) suunnitella talousarvion pohjalta voimme luoda vaihtoehtoinen tapa muokata budjettitietoja käytetään Excel-mallin asettelun määritykset. Koska Excel-mallin tulee vastata budjettisuunnitelman asettelun määrityksiä, et voi muokata budjettisuunnitelman asettelua sen jälkeen kun Excel-malli on luotu, joten tämä tehtävä tulisi tehdä sen jälkeen, kun kaikki asettelun osatekijät on määritetty. 5.2. 5.1 luoda asettelun. Vaihe, napsauta painiketta malli &gt;Luo. Vahvista varoitussanoma. Jos haluat nähdä mallin, valitse malli &gt;Näytä. *Huomautus: Varmista, että Valitse "Tallenna nimellä" ja valitse sijainti, johon malli tallennetaan muokata sitä. Jos käyttäjä valitsee "Avaa-valintaikkunan tallentamatta,-tiedostoon tehdyt muutokset eivät säily, kun tiedosto suljetaan.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Valinnainen vaihe&gt; muokata Excel-malli, jotta se näyttäisi enemmän käyttäjä friendly – Lisää yhteensä kaavat, muotoilut jne otsikkokentät. Tallenna muutokset ja lataa tiedosto budjetti suunnitelma asettelua valitsemalla asettelu &gt;ladata [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Tehtävä 6: Luo budjettisuunnitteluprosessi
Julian on luotava ja aktivoitava uusi budjettisuunnitteluprosessi, joka yhdistää kaikki edellä olevat asetukset, alkaakseen kirjoittamaan budjettisuunnitelmia. Budjetin suunnitteluprosessi määrittää, mitä budjetointiorganisaatioita, työnkulkuja, asetteluja ja malleja käytetään budjettisuunnitelmien luomiseen. 6.1. Siirry budjetoinnin &gt;asennus &gt;budjettisuunnittelua &gt;budjetin suunnitteluprosessin ja luo uusi tietue.

-   Budjettisuunnitteluprosessi – DEMF budjetointi FY2016
-   Budjettijakso – FY2016
-   Kirjanpito – DEMF
-   Tilin oletusrakenne – Valmistus P&L
-   Organisaatiohierarkia – valitse hirarkia, joka luotiin kurssin alussa
-   Budjettisuunnittelun työnkulku – Määritä automaattisesti – Hyväksy työnkulku talousosastoa varten
-   Budjettisuunnitteluvaiheen säännöissä ja malleissa, kullekin työnkulun budjettisuunnitteluvaiheelle, valitse onko "Lisää rivejä" ja "Muokkaa rivejä" sallittua ja mitä asettelua tulee käyttää oletuksena

*Huomautus: Voit luoda lisää asiakirja-asetteluja ja määrittää ne käytettävissä olevaan budjettisuunnittelun työnkulun vaiheeseen klikkaamalla "Muut asettelut" -painiketta.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Valitse Toiminnot &gt;budjettisuunnittelun työnkulun aktivointi Aktivoi [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Harjoitus 2: Prosessin simulointi
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Tehtävä 7: Luo budjettisuunnitelmalle alkuperäiset tiedot kirjanpitotilistä
7.1. Siirry budjetoinnin &gt;Kausittainen &gt;Luo budjettisuunnitelma kirjanpidosta. Täytä kausittaisen prosessin parametrit ja klikkaa Lu-painiketta. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Siirry budjetoinnin &gt;budjetin aikoo löytää luo prosessin luomat budjettisuunnitelman. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Avaa asiakirjan tiedot klikkaamalla "Asiakirjan numero" -hyperlinkkiä. Budjettisuunnitelman näytetään kurssin aikana luotu asettelu määritelty [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Vaihe 8: Luo kuluvan vuoden budjetti perustuen edellisen vuoden ilmoitettaviin todellisiin arvoihin
Kohdistusmenetelmiä voidaan käyttää budjettisuunnitelmassa kopioimaan tietoja helposti budjettisuunnitelmia varten yhdestä skeenariosta toiseen / levittäen ne eri aikakausille / liitettäen dimensioihin. Käytämme kohdistuksia luomaan kuluvan vuoden budjetin edellisen vuoden ilmoitettavista todellisista arvoista. 8.1. Poiminta kaikille riveille budjettisuunnitelman Asiakirjaruudukko ja valitse Kohdista budjetti [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Valitse kohdistusmenetelmä, Kausiavain, lähde- ja kohdeosoitteen skenaarioita ja Kohdista 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

Edellisen vuoden todellisten summien kopioidaan kuluvan vuoden talousarvioon ja Kohdista niiden myynti käyrä Kausiavaimen avulla kausille. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Tehtävä 9: Oikaise budjettisuunnitelmaasiakirja käyttämällä Exceliä ja viimeistele asiakirja
9.1. Napsauta painiketta laskentataulukon Excel avaa tiedoston sisältö

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Kun Excel-työkirja avautuu, muokkaa budjettisuunnitelmaasiakirjan määriä ja klikkaa "Julkaise".

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Palaa-operaatioille 365 Dynamics budjettisuunnitelman asiakirjan. Valitse työnkulun &gt;asiakirjan lähettäminen automaattisesti

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Kun työnkulku on valmis, asiakirja budjettisuunnitelman vaihe muuttuu hyväksytty. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Liite
========

### <a name="auto-approve-workflow-configuration"></a>Hyväksy automaattisesti työnkulun konfigurointi

A. Budjetointi &gt;asennus &gt;budjettisuunnittelua &gt;budjetointityönkulut Luo uusi työnkulku käyttämällä mallin budjettisuunnittelun työnkulut:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Tämä työnkulku sisältää vain yksi tehtävä: vaihe siirtymä budjettisuunnitelma 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Tallenna ja Aktivoi työnkulku. 

B. Siirry budjetoinnin &gt;asennus &gt;budjettisuunnittelua &gt;budjettisuunnittelun konfiguraatio. Luoda vaiheita 2 – alku- ja lähetetty vaiheet-välilehti 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Siirry budjetoinnin &gt;asennus &gt;budjettisuunnittelua &gt;budjettisuunnittelun konfiguraatio. Työnkulun vaiheet-välilehdessä Liitä työnkulku automaattisesti – Hyväksy luotiin vaiheessa vaihetta alku ja lähetetty 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


