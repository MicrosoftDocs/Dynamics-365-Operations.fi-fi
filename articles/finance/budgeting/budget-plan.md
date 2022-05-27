---
title: Budjettisuunnittelu
description: Tämän kurssin tavoite on tarjota Microsoft Dynamics 365 Financen toimintojen päivitysten ohjattu näkymä Budjettisuunnittelu-alueella. Tämä kurssi sisältää nopean konfiguraatioesimerkin budjettisuunnittelumoduulista ja esittelee, miten budjettisuunnittelu voidaan suorittaa tämän konfiguraation avulla.
author: panolte
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ebfddb1baf39e20c22d3ed9bb26dbb33765e20
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712001"
---
# <a name="budget-planning"></a>Budjettisuunnittelu

[!include [banner](../includes/banner.md)]

Tämän kurssin tavoite on tarjota Microsoft Dynamics 365 Financen toimintojen päivitysten ohjattu näkymä Budjettisuunnittelu-alueella. Tämä kurssi sisältää nopean konfiguraatioesimerkin budjettisuunnittelumoduulista ja esittelee, miten budjettisuunnittelu voidaan suorittaa tämän konfiguraation avulla.  Tällä kurssilla keskitytään erityisesti seuraaviin liiketoimintaprosesseihin tai tehtäviin:
- Organisaatiohierarkian luonti budjetin suunnittelua ja käyttäjän tietoturvan konfigurointia varten
- Budjettisuunnitelmaskenaarioiden, budjettisuunnitelmasarakkeiden ja Excel-mallien määrittäminen
- Luodaan ja aktivoidaan budjettisuunnitteluprosessi
- Budjettisuunnitelman luominen hakemalla kirjanpidon todelliset arvot
- Budjettisuunnitelman asiakirjan tietojen oikaisu kohdistusten avulla
- Budjettisuunnitelman asiakirjan tietojen muokkaaminen Excelissä 

## <a name="prerequisites"></a>Edellytykset 

Tätä opasta varten sinulla on oltava Microsoft Dynamics 365 Finance -ympäristö, jossa on Contoson esittelytiedot, ja sinun on oltava esiintymän järjestelmänvalvoja. Älä käytä henkilökohtaista selaimen tilaa tällä kurssilla, vaan kirjaudu ulos muista selaimen tileistä jos tarvittaessa ja kirjaudu sisään järjestelmänvalvojan tunnistetiedoilla. Kun kirjaudut sisään, sinun **ON** valittava Pidä minut kirjautuneena -valintaruutu. Se luo Excel-sovellukseen pysyvän esteen, jota se parhaillaan tarvitsee. Jos kirjaudut sisään sovellukseen käyttäen jotain muuta selainta kuin Internet Exploreria, järjestelmä kehottaa sinua sisäänkirjautumaan Excel-sovelluksen kautta. Kun valitset Kirjaudu sisään Excel-sovelluksessa, IE ponnahdusikkuna avautuu ja kun kirjaudut sisään, sinun **ON** valittava Pidä minut sisäänkirjautuneena -valintaruutu. Jos mitään ei tapahdu, kun napsautat Excel-sovelluksen "Kirjaudu sisään" -painiketta, sitten sinun kannattaa tyhjentää Internet Explorerin välimuistin evästeet.

## <a name="scenario-overview"></a>**Tilanteen yleiskuvaus**
Julia toimii talouspäällikkönä Contoso Entertainment Systemsissä Saksassa (DEMF). Kun FY2016 lähestyy, hänen on määritettävä yrityksen budjetti tulevalle vuodelle. Budjetin valmistelu näyttää seuraavanlaiselta:

1.  Julia käyttää edellisvuoden toteutuneita summia budjetin luomisen lähtökohtana.
2.  Perustuen edellisen vuoden toteutuneisiin summiin, hän luo 12 kuukauden arviot seuraavalle vuodelle
3.  Julia tarkistaa budjettitapahtumat talousjohtajan kanssa. Kun se on tehty, hän tekee tarvittavat oikaisut budjettisuunnitelmaan ja viimeistelee budjetin valmistelun.

Budjetin suunnittelun kokoonpanomalli skenaariolle näyttää seuraavalta:

![Budjetin suunnittelun kokoonpanomalli.](./media/screenshot1-300x152.png)

Julia valmistelee budjetin käyttäen seuraavaa Excel-mallia:

[![Excel-malli.](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Harjoitus 1: Määritys

### <a name="task-1-create-organizational-hierarchy"></a>**Tehtävä 1: Luo organisaatiohierarkia.**
Koska kaikki budjetointiprosessissa tapahtuu talousosastolla, Julian on luotava helppo organisaatiohierarkia, joka koostuu vain taloushallinto-osastosta. 

1.1. Siirry organisaatiohierarkioihin (Organisaation hallinto &gt; Organisaatiot &gt; Organisaatiohierarkiat) ja napsauta Uusi-painiketta

![Organisaatiohierarkiat.](./media/screenshot3.png) 

1.2. Kirjoita organisaatiohierarkian Nimi-ruutuun ja valitse sitten Määritä tarkoitus.

1.3. Valitse ensin budjettisuunnittelun tarkoitus ja sitten Lisää ja määritä juuri luotu organisaatiohierarkia. 

[![Määritä tarkoitus.](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Toista edellä oleva vaihe kohdassa Organisaation tarkoituksen suojaus. Sulje lomake kun se on tehty.

1.5. Valitse Organisaation hierarkiat -lomakkeessa Näytä. Valitse Muokkaa Hierarkian suunnittelu -kohdassa ja luo hierarkia valitsemalla Lisää.

[![Lisää.](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Valitse "Talousosasto" budjetoinnin hierarkiaan. 

[![Myyntitiedot.](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kun olet valmis, valitse Julkaise ja Sulje. Valitse 1.1.2015 hierarkian julkaisemisen voimaantulopäiväksi.

[![Voimassaolon alkamispäivämäärä.](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Vaihe 2: Käyttäjäryhmän suojauksen määrittäminen
Budjettisuunnittelussa käytetään erityisiä suojauskäytäntöjä määrittämään pääsy budjettisuunnitelmien tietoihin. Julian on annettava käyttöoikeus taloushallinnon budjettisuunnitelmiin itselleen. 

2.1. Siirry DEMF-yrityskontekstiin. 


2.2. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Määritä Parametrit-välilehdessä suojausmallin arvoksi Perustuu suojausorganisaatioihin. 

[![Parametrit.](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Siirry: Järjestelmänvalvojat &gt; Käyttäjät &gt; Käyttäjät. Anna käyttäjien hallinnalle (Julia Funderburk) budjetin hallitsijan rooli. 

[![Budjettipäällikkö.](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Valitse ensin käyttäjärooli ja sitten Määritä organisaatiot. 

[![Organisaatioiden määritys.](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Valitse "Myönnä käyttöoikeudet yksittäisille organisaatioille". Valitse ensimmäisessä vaiheessa luotu Organisaatiohierarkia. Valitse ensin Finance-solmu ja sitten Myönnä alatasot -painike. 

***Tärkeää!** _ _Tarkista, että olet DEMF yrityksen yhteydessä, kun suoritat tätä tehtävää, sillä organisaatioiden suojaus sovelletaan yrityksittäin* 

### <a name="task-3-create-scenarios"></a>Tehtävä 3: Luo skenaarioita
3.1. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. "Skenaariot"-sivulla, pane merkille ne skenaariot, joita käytämme myöhemmin tällä kurssilla: edellisen vuoden todeutuneet ja budjetoidut. 

*Huomautus: Voit luoda tarvittaessa uusia tilanteita tähän harjoitukseen ja käyttää niitä näiden sijaan.* 

[![Uudet skenaariot.](./media/screenshot15.png)](./media/screenshot15.png) 

*Huomautus: Koska Julia ei käytä virallista hyväksymisprosessia budjetin valmisteluun, ohitamme työnkulun, vaiheiden ja työnkulun vaiheiden asetukset tällä kurssilla ja käytämme aiemmin määritettyjä asetuksia "Automaattinen – hyväksy työnkulku". Katso liitteestä tämän työnkulun konfiguraatio.*

### <a name="task-4-create-budget-plan-columns"></a>Tehtävä 4: Luo budjettisuunnitelmalle sarakkeet
Budjettisuunnitelman sarakkeet ovat joko rahaan tai määrään perustuvia sarakkeita, joita voidaan käyttää budjettisuunnitelman asiakirjan asetteluun. Esimerkissämme meidän on luotava sarake edellisen vuoden todellisille arvoille ja 12 saraketta, jotka edustavat budjetoidun vuoden kutakin kuukautta. Sarakkeita voidaan luoda joko klikkaamalla "Lisää"-painiketta ja kirjoittamalla arvot, tai tietoyksikön avulla. Tällä kurssilla käytämme tietoyksikköä syöttämään arvot. 

4.1. Avaa Sarakkeet-sivu Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfigurointi. Napsauta lomakkeen oikeassa yläkulmassa Office-painiketta ja valitse Sarakkeet (suodattamaton). 

[![Suodattamattomat sarakkeet.](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Järjestelmä avaa Excel-työkirjan, jota käytetään arvojen kirjoittamiseen. Valitse pyydettäessä Ota muokkaus käyttöön ja Luota tähän sovellukseen. 

4.3. Tarvitsemme enemmän sarakkeita arvojen täyttämiseen. Lisää sarakkeet ruudukkoon valitsemalla Rakenne oikeassa ruudussa. 

[![Rakenne.](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Ruudukkoon lisättävissä olevat sarakkeet saa näkyviin napsauttamalla kynäkuvaketta Suunnittele sarakkeita -kohdan vieressä. 

[![Muokkaa.](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Lisää käytettävissä olevat kentät valittuihin kenttiin kaksoisnapsauttamalla kenttää ja valitsemalla Päivitä. 

4.6. Lisää kaikki luotavat sarakkeet Excel-taulukkoon. Lisää rivejä nopeasti Excelin automaattisen täytön avulla. Varmista, että rivit on lisätty taulun osana (pystyvierityspalkkia käytettäessä sarakeotsikoiden pitäisi näkyä ruudukon yläosassa). 

4.7. Palaa sovellukseen ja päivitä sivu. Julkaistut arvot tulevat näkyviin. 

[![Päivitä.](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Tehtävä 5: Luo budjettisuunnitelma asiakirjan suunnitelmat ja mallit
Asettelu määrittää, miltä budjettisuunnitelman asiakirjan rivien ruudukko näyttää, kun käyttäjä avaa budjettisuunnitelma-asiakirjan. On myös mahdollista siirtää budjettisuunnitelman asiakirjan tekstin asettelu niin, että voidaan katsoa samoja tietoja eri suunnalta. Nyt kun hän on määrittänyt sarakkeet, joita käytetään budjettisuunnittelu asiakirjassa, Julian on luotava budjettisuunnitelma asiakirjan asettelu, joka näyttää samanlaiselta kuin Excel-taulukko, jota hän käyttää budjettitietojen luomiseen (Katso "Skenaarion yhteenveto" -osa tässä kurssissa) 

5.1. Avaa asettelut sivu valitsemalla Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfigurointi. Luo uusi asettelu kuukausittaiselle budjettitapahtumalle:

-   Valitse MA+BU dimensioyhdistelmä sisällyttämään päätilit ja liiketoimintayksiköt asettelussa.
-   Listaa kaikki budjettisuunnitelman sarakkeet, jotka luotiin edellisessä vaiheessa "Elementit"-osiossa. Tee kaikista paitsi edellisen vuoden todellisista arvoista muokattavia.
-   Klikkaa "Kuvaukset"-painiketta valitaksesi minkä taloushallinnon dimensioiden tulisi näkyä "Kuvaukset"-ruudukossa.

[![Kuvaukset.](./media/screenshot24.png)](./media/screenshot24.png) 

Perustuen budjettisuunnitelman asettelun määritykseen, voimme luoda Excel-mallin, jota käytetään vaihtoehtoisena tapana muokata budjettitietoja. Koska Excel-mallin tulee vastata budjettisuunnitelman asettelun määrityksiä, et voi muokata budjettisuunnitelman asettelua sen jälkeen kun Excel-malli on luotu, joten tämä tehtävä tulisi tehdä sen jälkeen, kun kaikki asettelun osatekijät on määritetty. 

5.2. Kohdassa 5.1. luodulle asettelulle, napsauta painiketta Malli &gt; Luo. Vahvista varoitussanoma. Napsauta Malli &gt; Näytä, jos haluat tarkastella mallia. 

*Huomautus: Varmista, että valitset "Tallenna nimellä" -painikkeen ja valitset sijainnin, johon malli tallennetaan muokkausta varten. Jos käyttäjä valitsee valintaikkunassa "Avaa" tallentamatta, tiedostoon tehdyt muutokset eivät säily, kun tiedosto suljetaan.* 
[![Mallinäkymä.](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt;Valinnainen vaihe&gt; Muokkaa Excel-mallia käyttäjäystävällisemmäksi lisäämällä esimerkiksi summa-kaavoja, otsikkokenttiä ja muotoiluja. Tallenna muutokset ja lataa tiedosto budjettisuunnitelman asetteluun valitsemalla Asettelu &gt; Lataa. 


### <a name="task-6-create-a-budget-planning-process"></a>Tehtävä 6: Luo budjettisuunnitteluprosessi
Julian on luotava ja aktivoitava uusi budjettisuunnitteluprosessi, joka yhdistää kaikki edellä olevat asetukset, alkaakseen kirjoittamaan budjettisuunnitelmia. Budjetin suunnitteluprosessi määrittää, mitä budjetointiorganisaatioita, työnkulkuja, asetteluja ja malleja käytetään budjettisuunnitelmien luomiseen. 

6.1. Luo uusi tietue valitsemalla Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnitteluprosessi.

-   Budjettisuunnitteluprosessi – DEMF budjetointi FY2016
-   Budjettijakso – FY2016
-   Kirjanpito – DEMF
-   Tilin oletusrakenne – Valmistus P&L
-   Organisaatiohierarkia – valitse hirarkia, joka luotiin kurssin alussa
-   Budjettisuunnittelun työnkulku – Määritä automaattisesti – Hyväksy työnkulku talousosastoa varten
-   Budjettisuunnitteluvaiheen säännöissä ja malleissa, kullekin työnkulun budjettisuunnitteluvaiheelle, valitse onko "Lisää rivejä" ja "Muokkaa rivejä" sallittua ja mitä asettelua tulee käyttää oletuksena

*Huomautus: Voit luoda lisää asiakirja-asetteluja ja määrittää ne käytettävissä olevaan budjettisuunnittelun työnkulun vaiheeseen klikkaamalla "Muut asettelut" -painiketta.* 

[![Vaihtoehtoiset asettelut.](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Aktivoi tämä budjettisuunnittelun työnkulku valitsemalla Toiminnot &gt; Aktivoi. 

[![Aktivoi.](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Harjoitus 2: Prosessin simulointi

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Tehtävä 7: Luo budjettisuunnitelmalle alkuperäiset tiedot kirjanpitotilistä
7.1. Siirry: Budjetointi &gt; Kausittainen &gt; Luo budjettisuunnitelma kirjanpidosta. Täytä kausittaisen prosessin parametrit ja valitse Luo. 

7.2. Etsi luontiprosessilla luotu budjettisuunnitelma valitsemalla Budjetointi &gt; Budjettisuunnitelmat. 

[![Budjettisuunnitelma.](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Avaa asiakirjan tiedot klikkaamalla "Asiakirjan numero" -hyperlinkkiä. Budjettisuunnitelma näytetään määritettynä tämän kurssin aikana luodussa asettelussa. 

[![Budjettisuunnitelman näyttö.](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Vaihe 8: Luo kuluvan vuoden budjetti perustuen edellisen vuoden ilmoitettaviin todellisiin arvoihin
Kohdistusmenetelmiä voidaan käyttää budjettisuunnitelmassa kopioimaan tietoja helposti budjettisuunnitelmia varten yhdestä skeenariosta toiseen / levittäen ne eri aikakausille / liitettäen dimensioihin. Käytämme kohdistuksia luomaan kuluvan vuoden budjetin edellisen vuoden ilmoitettavista todellisista arvoista. 

8.1. Valitse kaikki rivit budjettisuunnitelma-asiakirjan ruudukossa ja valitse sitten Kohdista budjetti. 

[![Kaikki rivit.](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Valitse ensin kohdistusmenetelmä, kausiavain sekä lähde- ja kohdeskenaariot ja sitten Kohdista. 

[![Kohdista.](./media/screenshot33.png)](./media/screenshot33.png)

Edellisen vuoden toteutuneet summat kopioidaan kuluvan vuoden budjettiin ja kohdistetaan myyntikäyrän kausiavaimen avulla eri kausille. 

[![Myyntikäyrä.](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Tehtävä 9: Oikaise budjettisuunnitelmaasiakirja käyttämällä Exceliä ja viimeistele asiakirja
9.1. Avaa asiakirjan sisältö Excelissä napsauttamalla työkirjapainiketta.

9.2. Kun Excel-työkirja avautuu, muokkaa budjettisuunnitelma-asiakirjan lukuja ja napsauta Julkaisu-painiketta.

9.3. Palaa budjettisuunnitelma-asiakirjaan. Hyväksy asiakirja automaattisesti valitsemalla Työnkulku &gt; Lähetä.

[![Automaattinen hyväksyntä.](./media/screenshot37.png)](./media/screenshot37.png) 

Kun työnkulku valmistuu, budjettisuunnitelman-asiakirjan vaiheeksi tulee Hyväksytty. [![Hyväksytty.](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Liite

### <a name="auto-approve-workflow-configuration"></a>Hyväksy automaattisesti työnkulun konfigurointi

A. Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjetoinnin työnkulut. Lue uusi työnkulku käyttämällä budjettisuunnittelun työnkulkuja:

[![Uuden työnkulun luonti.](./media/screenshot39.png)](./media/screenshot39.png)

Tässä työnkulussa on vain yksi tehtävä – budjettisuunnitelman vaiheen siirtymä. 

[![Budjettisuunnitelman vaiheen siirtymä.](./media/screenshot40.png)](./media/screenshot40.png) 

Tallenna ja aktivoi työnkulku. 

B. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Luo Vaiheet-välilehdessä kaksi vaihetta – alkuperäinen ja lähetetty. 

[![Alkuperäinen ja Lähetetty.](./media/screenshot41.png)](./media/screenshot41.png)

C. Mene: Budjetointi &gt; Asetukset &gt; Budjettisuunnittelu &gt; Budjettisuunnittelun konfiguraatio. Liitä Työnkulun vaiheet -välilehdessä vaiheessa A luotuun työnkulun automaattiseen hyväksymiseen Aloitus- ja Lähetetty-vaiheet.

[![Budjetointi ja budjetin suunnittelu.](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
