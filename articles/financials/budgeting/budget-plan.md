---
title: Budjettisuunnittelu
description: "Tämän kurssin tavoite on tarjota Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin toimintojen päivitysten ohjattu näkymä Budjettisuunnittelu-alueella. Tämä kurssi sisältää nopean konfiguraatioesimerkin budjettisuunnittelumoduulista ja esittelee, miten budjettisuunnittelu voidaan suorittaa tämän konfiguraation avulla.  Tällä kurssilla keskitytään erityisesti seuraaviin liiketoimintaprosesseihin tai tehtäviin: -    - organisaatiohierarkian luominen budjettisuunnittelulle ja käyttäjän suojauksen määrittäminen - budjettisuunnitelmien skenaarioiden, budjettisuunnitelmien sarakkeiden, asettelujen ja Excel-mallien määrittäminen   - budjettisuunnitteluprosessien luominen ja aktivoiminen   - budjettisuunnitelman asiakirjan luominen noutamalla toteutuneet tiedot kirjanpidosta   - kohdistusten käyttäminen budjettisuunnitelman asiakirjan tietojen oikaisussa   - budjettisuunnitelman asiakirjan tietojen muokkaaminen Excelissä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 608ec87233acb05b0d46e367bcb7cd14985d7813
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning"></a>Budjettisuunnittelu

[!include[banner](../includes/banner.md)]


Tämän kurssin tavoite on tarjota Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin toimintojen päivitysten ohjattu näkymä Budjettisuunnittelu-alueella. Tämä kurssi sisältää nopean konfiguraatioesimerkin budjettisuunnittelumoduulista ja esittelee, miten budjettisuunnittelu voidaan suorittaa tämän konfiguraation avulla.  Tällä kurssilla keskitytään erityisesti seuraaviin liiketoimintaprosesseihin tai tehtäviin: -    - organisaatiohierarkian luominen budjettisuunnittelulle ja käyttäjän suojauksen määrittäminen - budjettisuunnitelmien skenaarioiden, budjettisuunnitelmien sarakkeiden, asettelujen ja Excel-mallien määrittäminen   - budjettisuunnitteluprosessien luominen ja aktivoiminen   - budjettisuunnitelman asiakirjan luominen noutamalla toteutuneet tiedot kirjanpidosta   - kohdistusten käyttäminen budjettisuunnitelman asiakirjan tietojen oikaisussa   - budjettisuunnitelman asiakirjan tietojen muokkaaminen Excelissä. 

<a name="prerequisites"></a>Edellytykset 
------------------

Tätä opasta varten sinulla on oltava Dynamics 365 for Finance and Operations -ympäristö, jossa on Contoson esittelytiedot, ja sinun on oltava esiintymän järjestelmänvalvoja. Älä käytä selaimen yksityistä tilaa tällä kurssilla. Kirjaudu sen sijaan tarvittaessa ulos selaimen muilta tileiltä ja kirjaudu sisään Dynamics 365 for Finance and Operationsiin järjestelmänvalvojan oikeuksilla. Kun kirjaudut sisään Dynamics 365 for Finance and Operationsiin, sinun **ON** valittava Pidä minut kirjautuneena -valintaruutu Se luo Excel-sovellukseen pysyvän esteen, jota se parhaillaan tarvitsee. Jos kirjaudut sisään Dynamics 365 for Finance and Operationsiin käyttäen jotain muuta selainta kuin Internet Exploreria, järjestelmä kehottaa sinua sisäänkirjautumaan Excel-sovelluksen kautta. Kun valitset "Kirjaudu sisään" Excel-sovelluksessa, Internet Explorer -ponnahdusikkuna avautuu ja kun kirjaudut sisään, sinun **TÄYTYY** merkitä valintaruutu "Pidä minut sisäänkirjautuneena". Jos mitään ei tapahdu, kun napsautat Excel-sovelluksen "Kirjaudu sisään" -painiketta, sitten sinun kannattaa tyhjentää Internet Explorerin väimuistin evästeet.

## <a name="scenario-overview"></a>**Tilanteen yleiskuvaus**
Julia toimii talouspäällikkönä Contoso Entertainment Systemsissä Saksassa (DEMF). Kun FY2016 lähestyy, hänen on määritettävä yrityksen budjetti tulevalle vuodelle. Budjetin valmistelu näyttää seuraavanlaiselta:

1.  Julia käyttää edellisvuoden toteutuneita summia budjetin luomisen lähtökohtana.
2.  Perustuen edellisen vuoden toteutuneisiin summiin, hän luo 12 kuukauden arviot seuraavalle vuodelle
3.  Julia tarkistaa budjettitapahtumat talousjohtajan kanssa. Kun se on tehty, hän tekee tarvittavat oikaisut budjettisuunnitelmaan ja viimeistelee budjetin valmistelun.

Budjetin suunnittelun kokoonpanomalli skenaariolle näyttää seuraavalta:

![Budjettisuunnittelun skeema](./media/screenshot1-300x152.png)

Julia valmistelee budjetin käyttäen seuraavaa Excel-mallia:

[![Excel-malli](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Harjoitus 1: Määritys
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Tehtävä 1: Luo organisaatiohierarkia.**
Koska kaikki budjetointiprosessissa tapahtuu talousosastolla, Julian on luotava helppo organisaatiohierarkia, joka koostuu vain taloushallinto-osastosta. 1.1. Siirry organisaatiohierarkioihin (Organisaation hallinto &gt; Organisaatiot &gt; Organisaatiohierarkiat) ja klikkaa "Uusi"-painiketta

![Organisaatiohierarkia](./media/screenshot3.png) 

1.2. Kirjoita organisaatiohierarkian nimi ja klikkaa sitten painiketta "Aseta tarkoitus"

[![Nimi](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Valitse budjettisuunnittelun tarkoitus, klikkaa "Lisää"-painiketta ja määritä juuri luotu organisaatiohierarkia: 

[![Määritä tarkoitus](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Toista edellä oleva vaihe "Organisaation tarkoituksen turvatoimille". Sulje lomake kun se on tehty.

[![Suojaus org](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Organisaation hierarkiat -lomakkeessa klikkaa "Näytä"-painiketta. Valitse "Muokkaa" Hierarkian suunnittelussa ja luo hierarkia klikkaamalla "Lisää"-painiketta.

[![Lisää](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Valitse "Talousosasto" budjetoinnin hierarkiaan. 

[![Myyntitiedot](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kun olet valmis, klikkaa painiketta "Julkaise" ja "Sulje". Valitse 1/1/2015 hierarkian julkaisemisen voimaantulopäiväksi.

[![Voimaantulopäivä](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Vaihe 2: Käyttäjäryhmän suojauksen määrittäminen
Budjettisuunnittelussa käytetään erityisiä suojauskäytäntöjä määrittämään pääsy budjettisuunnitelmien tietoihin. Julian on annettava käyttöoikeus taloushallinnon budjettisuunnitelmiin itselleen. 

2.1. Siirry DEMF-yrityskontekstiin. 


2.2. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Parametrit-välilehdessä, aseta suojausmallin arvo organisaatioiden suojaukseen perustuen 

[![Parametrit](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Siirry: Järjestelmänvalvojat &gt; Käyttäjät &gt; Käyttäjät. Anna käyttäjien hallinnalle (Julia Funderburk) budjetin hallitsijan rooli. 

[![Budjettipäällikkö](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Valitse käyttäjärooli ja klikkaa "Määritä organisaatiot" 

[![Määritä org](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Valitse "Myönnä käyttöoikeudet yksittäisille organisaatioille". Valitse ensimmäisessä vaiheessa luotu "Organisaatiohierarkia". Valitse "Myyntitiedot"-solmu ja klikkaa "Myönnä" alatason painikkeella 

***Tärkeää!*** *Tarkista, että olet DEMF-yrityksen yhteydessä, kun suoritat tätä tehtävää, sillä organisaatioiden suojaus sovelletaan yrityksittäin* 

[![Myönnä käyttöoikeus](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Tehtävä 3: Luo skenaarioita
3.1. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. "Skenaariot"-sivulla, pane merkille ne skenaariot, joita käytämme myöhemmin tällä kurssilla: edellisen vuoden todeutuneet ja budjetoidut. 

*Huomautus: Voit luoda tarvittaessa uusia tilanteita tähän harjoitukseen ja käyttää niitä näiden sijaan.* 

[![Uudet skenaariot](./media/screenshot15.png)](./media/screenshot15.png) 

*Huomautus: Koska Julia ei käytä virallista hyväksymisprosessia budjetin valmisteluun, ohitamme työnkulun, vaiheiden ja työnkulun vaiheiden asetukset tällä kurssilla ja käytämme aiemmin määritettyjä asetuksia "Automaattinen – hyväksy työnkulku". Katso liitteestä tämän työnkulun konfiguraatio.*

## <a name="task-4-create-budget-plan-columns"></a>Tehtävä 4: Luo budjettisuunnitelmalle sarakkeet
Budjettisuunnitelman sarakkeet ovat joko rahaan tai määrään perustuvia sarakkeita, joita voidaan käyttää budjettisuunnitelman asiakirjan asetteluun. Esimerkissämme meidän on luotava sarake edellisen vuoden todellisille arvoille ja 12 saraketta, jotka edustavat budjetoidun vuoden kutakin kuukautta. Sarakkeita voidaan luoda joko klikkaamalla "Lisää"-painiketta ja kirjoittamalla arvot, tai tietoyksikön avulla. Tällä kurssilla käytämme tietoyksikköä syöttämään arvot. 

4.1. Avaa "Sarakkeet"-sivu kohdassa Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Napsauta lomakkeen oikeassa yläkulmassa olevaa "Office"-painiketta ja valitse "Sarakkeet" (suodattamaton) 

[![Suodattamattomat sarakkeet](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Järjestelmä avaa Excel-työkirjan, jota käytetään arvojen kirjoittamiseen. Napsauta pyydettäessä "Salli muokkaus" ja "Luota tähän sovellukseen" 

[![Ota muokkaus käyttöön](./media/screenshot18.png)](./media/screenshot18.png) 

[![Luota tähän sovellukseen](./media/screenshot17.png)](./media/screenshot17.png)

4.3. Tarvitsemme enemmän sarakkeita arvojen täyttämiseen. Napsauta Rakenne oikeanpuoleisessa ruudussa lisätäksesi ruudukkoon sarakkeet: 

[![Rakenne](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Klikkaa pientä kynän kuvaa "Suunnittele sarakkeita"-painikkeen vieressä, jotta voit tarkastella käytettävissä olevia sarakkeita, lisätäksesi niitä ruudukkoon 

[![Muokkaa](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Kaksoisnapsauta jokaista käytettävissä olevaa kenttää lisätäksesi ne valittuihin kenttiin ja klikkaa "Päivitä" 

![Päivitä](./media/screenshot21.png)](./Media/screenshot21.png) 

4.6. Lisää kaikki sarakkeet, jotka on luotava, Excel-taulukkoon. Lisää rivejä nopeasti Excelin automaattisnen täyttö -toiminnon avulla. Varmista, että rivit on lisätty taulun osana (käytettäessä pystyvierityspalkkia, sarakeotsikot pitäisi näkyä ruudukon yläosassa) 

[![Automaattinen täyttö](./media/screenshot22.png)](./media/screenshot22.png) 

4.7. Palaa Dynamics 365 for Finance and Operationsiin ja päivitä sivu. Julkaistut arvot näkyvät Finance and Operationsissa. 

[![Päivitä](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Tehtävä 5: Luo budjettisuunnitelma asiakirjan suunnitelmat ja mallit
Asettelu määrittää, miltä budjettisuunnitelman asiakirjan rivien ruudukko näyttää, kun käyttäjä avaa budjettisuunnitelma-asiakirjan. On myös mahdollista siirtää budjettisuunnitelman asiakirjan tekstin asettelu niin, että voidaan katsoa samoja tietoja eri suunnalta. Nyt kun hän on määrittänyt sarakkeet, joita käytetään budjettisuunnittelu asiakirjassa, Julian on luotava budjettisuunnitelma asiakirjan asettelu, joka näyttää samanlaiselta kuin Excel-taulukko, jota hän käyttää budjettitietojen luomiseen (Katso "Skenaarion yhteenveto" -osa tässä kurssissa) 

5.1. Avaa "Asettelut"-sivu kohdassa Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Luo uusi asettelu kuukausittaiselle budjettitapahtumalle:

-   Valitse MA+BU dimensioyhdistelmä sisällyttämään päätilit ja liiketoimintayksiköt asettelussa.
-   Listaa kaikki budjettisuunnitelman sarakkeet, jotka luotiin edellisessä vaiheessa "Elementit"-osiossa. Tee kaikista paitsi edellisen vuoden todellisista arvoista muokattavia.
-   Klikkaa "Kuvaukset"-painiketta valitaksesi minkä taloushallinnon dimensioiden tulisi näkyä "Kuvaukset"-ruudukossa.

[![Kuvaukset](./media/screenshot24.png)](./media/screenshot24.png) 

Perustuen budjettisuunnitelman asettelun määritykseen, voimme luoda Excel-mallin, jota käytetään vaihtoehtoisena tapana muokata budjettitietoja. Koska Excel-mallin tulee vastata budjettisuunnitelman asettelun määrityksiä, et voi muokata budjettisuunnitelman asettelua sen jälkeen kun Excel-malli on luotu, joten tämä tehtävä tulisi tehdä sen jälkeen, kun kaikki asettelun osatekijät on määritetty. 

5.2. Kohdassa 5.1. luodulle asettelulle, napsauta painiketta Malli &gt; Luo. Vahvista varoitussanoma. Napsauta Malli &gt; Näytä, jos haluat tarkastella mallia. 

*Huomautus: Varmista, että valitset "Tallenna nimellä" -painikkeen ja valitset sijainnin, johon malli tallennetaan muokkausta varten. Jos käyttäjä valitsee valintaikkunassa Avaa tallentamatta,tiedostoon tehdyt muutokset eivät säily, kun tiedosto suljetaan.* 
[![Mallinäkymä](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Vaihtoehtoinen työvaihe&gt; Muokkaa Excel-mallia, jotta se näyttää enemmän käyttäjäystävälliseltä: Lisää summa-kaavoja, otsikkokenttiä, muotoiluja jne. Tallenna muutokset ja lataa tiedosto budjettisuunnitelman asetteluun valitsemalla Asettelu &gt; Lataa [![Lataa](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Tehtävä 6: Luo budjettisuunnitteluprosessi
Julian on luotava ja aktivoitava uusi budjettisuunnitteluprosessi, joka yhdistää kaikki edellä olevat asetukset, alkaakseen kirjoittamaan budjettisuunnitelmia. Budjetin suunnitteluprosessi määrittää, mitä budjetointiorganisaatioita, työnkulkuja, asetteluja ja malleja käytetään budjettisuunnitelmien luomiseen. 

6.1. Siirry: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnitteluprosessi ja luo uusi tietue.

-   Budjettisuunnitteluprosessi – DEMF budjetointi FY2016
-   Budjettijakso – FY2016
-   Kirjanpito – DEMF
-   Tilin oletusrakenne – Valmistus P&L
-   Organisaatiohierarkia – valitse hirarkia, joka luotiin kurssin alussa
-   Budjettisuunnittelun työnkulku – Määritä automaattisesti – Hyväksy työnkulku talousosastoa varten
-   Budjettisuunnitteluvaiheen säännöissä ja malleissa, kullekin työnkulun budjettisuunnitteluvaiheelle, valitse onko "Lisää rivejä" ja "Muokkaa rivejä" sallittua ja mitä asettelua tulee käyttää oletuksena

*Huomautus: Voit luoda lisää asiakirja-asetteluja ja määrittää ne käytettävissä olevaan budjettisuunnittelun työnkulun vaiheeseen klikkaamalla "Muut asettelut" -painiketta.* 

[![Vaihtoehtoiset asettelut](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Valitse Toiminnot &gt; Aktivoi aktivoidaksesi budjettisuunnittelun työnkulun 

[![Aktivoi](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Harjoitus 2: Prosessin simulointi
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Tehtävä 7: Luo budjettisuunnitelmalle alkuperäiset tiedot kirjanpitotilistä
7.1. Siirry: Budjetointi &gt; Kausittainen &gt; Luo budjettisuunnitelma kirjanpidosta. Täytä kausittaisen prosessin parametrit ja klikkaa Lu-painiketta. 

[![Luo](./media/screenshot29.png)](./media/screenshot29.png) 

7.2. Siirry: Budjetointi &gt; Budjettisuunnitelmat löytääksesi sen budjettisuunnitelman, joka luotiin Luo-prosessissa. 

[![Budjettisuunnitelma](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Avaa asiakirjan tiedot klikkaamalla "Asiakirjan numero" -hyperlinkkiä. Budjettisuunnitelma näkyy määritettynä asettelussa, joka luotiin kurssin aikana 

[![Budjettisuunnitelman näyttö](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Vaihe 8: Luo kuluvan vuoden budjetti perustuen edellisen vuoden ilmoitettaviin todellisiin arvoihin
Kohdistusmenetelmiä voidaan käyttää budjettisuunnitelmassa kopioimaan tietoja helposti budjettisuunnitelmia varten yhdestä skeenariosta toiseen / levittäen ne eri aikakausille / liitettäen dimensioihin. Käytämme kohdistuksia luomaan kuluvan vuoden budjetin edellisen vuoden ilmoitettavista todellisista arvoista. 

8.1. Valitse kaikki rivit budjettisuunnitelman asiakirjan ruudukossa ja klikkaa painiketta kohdistaaksesi budjetin 

[![Kaikki rivit](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Valitse kohdistusmenetelmä, kausiavain sekä lähde- ja kohdeskenaariot ja klikkaa Kohdista 

[![Kohdista](./media/screenshot33.png)](./media/screenshot33.png)

Edellisen vuoden todelliset summat kopioidaan kuluvan vuoden budjettiin ja kohdistetaan ne myyntikäyrän kausiavaimen avulla eri kausille. 

[![Myyntikäyrä](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Tehtävä 9: Oikaise budjettisuunnitelmaasiakirja käyttämällä Exceliä ja viimeistele asiakirja
9.1. Napsauta painiketta avataksesi laskentataulukon sisällön Excelissä

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Kun Excel-työkirja avautuu, muokkaa budjettisuunnitelmaasiakirjan määriä ja klikkaa "Julkaise".

[![Julkaise](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Palaa budjettisuunnitteluasiakirjaan Finance and Operationsissa. Valitse Työnkulun &gt; Lähetä hyväksyäksesi asiakirjan automaattisesti

[![Automaattinen hyväksyntä](./media/screenshot37.png)](./media/screenshot37.png) 

Kun työnkulku on valmis, budjettisuunnitelman asiakirjavaihe muuttuu tilaan Hyväksytty. [![Hyväksytty](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Liite
========

### <a name="auto-approve-workflow-configuration"></a>Hyväksy automaattisesti työnkulun konfigurointi

A. Budjetointi &gt; Asetukset &gt; Budjetin suunnittelu &gt; Budjetoinnin työnkulut Luo uusi työnkulku käyttäen budjetin suunnittelun työnkulun mallia:

[![Uuden työnkulun luonti.](./media/screenshot39.png)](./media/screenshot39.png)

Tämä työnkulku sisältää vain yhden tehtävän: Budjettisuunnitelman vaiheen siirtymä 

[![Budjettisuunnitelman vaiheen siirtymä](./media/screenshot40.png)](./media/screenshot40.png) 

Tallenna ja aktivoi työnkulku. 

B. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Luo Vaiheet-välilehdessä kaksi vaihetta: Aloitus ja Lähetetty 

[![Aloitus ja Lähetetty](./media/screenshot41.png)](./media/screenshot41.png)

C. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Työnkulun vaiheet -välilehdessä, liitä työnkulun automaattinen hyväksyntä, joka luotiin A-vaiheessa, vaiheisiin Alkuperäinen ja Lähetetty 

[![Budjetointi ja budjetin suunnittelu](./media/screenshot42.png)](./media/screenshot42.png)  




