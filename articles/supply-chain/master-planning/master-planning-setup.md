---
title: Pääsuunnittelun määrittäminen
description: Tässä ohjeaiheessa käsitellään erilaisia pääsuunnittelun määrittämisessä käytettäviä tärkeitä strategioita ja parametreja.
author: t-benebo
manager: tfehr
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: a74d2987eac7409b5f576a52eccc37cf29566c7b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426887"
---
# <a name="set-up-master-planning"></a>Pääsuunnittelun määrittäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään erilaisia pääsuunnittelun määrittämisessä käytettäviä tärkeitä strategioita ja parametreja. Siinä käsitellään yleisesti pääsuunnittelussa käytettäviä suunnitelmatyyppejä sekä selvitään liiketoimintatarpeiden perusteella, mikä on soveltuvin suunnitelmastrategia. Ohjeaiheessa käsitellään myös tärkeimmät suunnitelmaan vaikuttavat parametrit ja selitetään, miten nämä parametrit vaikuttavat ehdotettuihin suunniteltuihin tilauksiin.

## <a name="types-of-master-plans"></a>Pääsuunnitelmien tyypit

Pääsuunnittelussa on kahdenlaisia suunnitelmatyyppejä: staattisia ja dynaamisia. Nämä tyypit on suunniteltu erilaisiin käyttötarkoituksiin. Parhaan tuloksen saamiseksi kannattaa valita skenaarion kannalta sopivin suunnitelma.

### <a name="static-plan"></a>Staattinen suunnitelma

Staattinen suunnitelma ei muutu kysynnässä ja tarjonnassa tapahtuvien muutosten myötä, ennen kuin pääsuunnitelma suoritetaan seuraavan kerran.

Staattisen suunnitelman avulla voidaan hyväksyä ja vahvistaa ehdotetut tilaukset. Se on toimintasuunnitelma, jolla yrityksen henkilöstö (kuten ostojen ja tuotannon suunnittelija) voi perustella päätöksensä ja jota he voivat käyttää päivittäisten tehtävien ja toimintojen suorittamiseen.

Staattinen suunnitelma tukee myös täydellistä laskentaa. Täysin uusi optimoitu suunnitelma lasketaan aina, kun pääsuunnittelu suoritetaan. Samalla hyväksymättömät aiemmin luodut tilaukset poistetaan.

### <a name="dynamic-plan"></a>Dynaaminen suunnitelma

Dynaamisen suunnitelman pohjana on yleensä staattinen suunnitelma, mutta se voidaan päivittää aina, kun päätiedot muuttuvat. Niinpä esimerkiksi tietojen muuttuessa luodaan uusi myyntitilaus.

Dynaamista suunnitelmaa käytetään tilapäisessä suunnittelussa. Sen avulla yritys voi seurata muuttuvaa tilausverkostoa ja nimikkeiden saatavuutta ilman, että vaikuttaisi muiden työprosesseissaan käyttämään staattiseen suunnitelmaan. Sitä käytetään erityisesti saatavuuden (CTP) yhteydessä. Dynaaminen suunnitelma on tilaussivuilta (kuten myynti-, osto- tai tuotantotilaussivuilta) avattavien nettotarpeiden oletussuunnitelma.

Dynaaminen suunnitelma käyttää nettomuutosta, mikä varmistaa nopean suoritusajan.

## <a name="strategies-for-using-master-plans"></a>Pääsuunnitelmien käyttöstrategiat

Pääsuunnittelussa voi käyttää joko yhtä tai kahta suunnitelmaa. Käyttämäsi strategia määräytyy liiketoiminnan tarpeiden mukaan.

### <a name="one-plan-strategy"></a>Yhden suunnitelman strategia

Yhden suunnitelman strategiassa staattisessa ja dynaamisessa suunnitelmassa käytetään samaa pääsuunnitelmaa. Tätä strategiaa käytetään varastoon valmistusskenaarioissa, joissa ei yleensä tarvitse simuloida tilauksen täyttösuunnitelmaa.

Yhden suunnitelman strategiaa käytetään yleensä vähittäismyynti- ja jakelualalla tai tilanteissa, joissa toimituspäivät vahvistetaan palvelutasosopimusten tai läpimenoaikojen perusteella. Toimituspäivää voidaan hallita suunnitelmassa ilman saatavuus (CTP) -tietoja.

Jos simulaatio on tehtävä, suunnitelma voidaan suorittaa uudelleen simulaatiota edellyttävien nimikkeiden osalta. Tilaussimuloinneilla tuotetut suunnitellut tilaukset yleensä vahvistetaan.

### <a name="two-plan-strategy"></a>Kahden suunnitelman strategia

Kahden suunnitelman strategiassa käytetään staattista suunnitelmaa ja erilaista dynaamista suunnitelmaa. Kahden suunnitelman strategiaa käytetään yleensä tilaukseen määrittämisen ja tilauksen valmistamisen skenaarioissa, joissa on tehtävä myyntitilaussimulaatioita ja laskettava myyntitilausten tarkat toimituspäivät mutta joissa laskelmat eivät saa vaikuttaa päivittäisiin toimintoihin. Nämä simulaatiot tehdään aina dynaamisessa suunnitelmassa. Kahden suunnitelman strategiasta on hyötyä esimerkiksi autoteollisuudessa ja OEM-alalla.

Toimituspäivän saatavuutta (CTP) on mahdollista käyttää kahden suunnitelman strategiassa. Kun saatavuutta (CTP) käytetään, se käynnistää automaattisesti ajon dynaamisessa suunnitelmassa.

### <a name="setting-up-the-plans"></a>Suunnitelmien määrittäminen

Voit suunnitelmia **Pääsuunnitelmat**-sivulla (**Pääsuunnittelu \> Asetukset \> Suunnitelmat \> Pääsuunnitelmat**).

Voit määrittää, mitä suunnitelmia staattinen ja dynaaminen suunnitelma käyttävät, valitsemalla **Nykyinen staattinen pääsuunnitelma**- ja **Nykyinen dynaaminen pääsuunnitelma** -kentät **Pääsuunnittelun parametrit** -sivulla (**Pääsuunnittelu \> Asetukset \> Pääsuunnittelun parametrit**). Jos haluat käyttää yhden suunnitelman strategiaa, valitse sama suunnitelma **Nykyinen staattinen pääsuunnitelma**- ja **Nykyinen dynaaminen pääsuunnitelma** -kentissä.

## <a name="types-of-planning-methods"></a>Suunnittelumenetelmätyypit

Pääsuunnittelun suorittamisessa voidaan käyttää kolmea laskentamenetelmää: täydellistä laskentaa ja nettomuutosta. Syntynyt suunnitelma määräytyy suoritetun menetelmän perusteella.

Suunnittelumenetelmä määritetään **Pääsuunnitteluajo**-valintaikkunassa. Voit avata tämän valintaikkunan valitsemalla **Pääsuunnittelu \> Pääsuunnittelu \> Suorita \> Pääsuunnittelu**. Vaihtoehtoisesti voit valita **Suorita** **Pääsuunnittelu**-työtilassa.

### <a name="regeneration"></a>Täydellinen laskenta

Täydellisen laskennan suunnittelumenetelmässä aiemmin luodut suunnitellut tilaukset poistetaan, ellei niitä ole vahvistettu. Se luo uusia suunniteltuja tilauksia kaikkien tarpeiden perusteella. Täydellinen laskenta on ainoa suunnittelumenetelmä, jota voi käyttää staattisissa suunnitelmissa.

- Tarjonnan muutokset otetaan huomioon. Nämä muutokset sisältävät ennusteeseen tehdyt muutokset.
- Tässä menetelmässä hyväksytään **Kausi**-kattavuuskoodi.
- Tässä menetelmässä tuetaan tuotteen korvaustoimintoa (PI).

### <a name="net-change"></a>Nettomuutos

Nettomuutoksen suunnittelumenetelmä luo suunnittelut tilaukset, jotka kattavat edellisen pääsuunnitteluajon jälkeen luodut tai muutetut tarpeet. Tarjonnan muutoksia ei oteta huomioon tätä menetelmää suoritettaessa. Järjestelmä ei ota huomioon uusia toimituksia eikä aiemmin luotuja suunniteltuja tilauksia poisteta, jos niitä ei enää tarvita. Nettomuutoksen suunnittelumenetelmän suorittaminen on nopeampaa kuin täydellisen laskennan suorittaminen. Sitä voi käyttää vain dynaamisissa suunnitelmissa.

- Kaikkien tarpeiden toimintapäivät ja -viivästykset päivitetään.
- Tämä menetelmä ei noudata **Kausi**-kattavuuskoodia.
- Tämä menetelmä ei täytä ennustetta, vaikka se olisi valittu suunnitelmassa.
- Tässä menetelmä ei tue tuotteen korvaustoimintoa (PI).

### <a name="net-change-minimized"></a>Minimoitu nettomuutos

Minimoidun nettomuutoksen suunnittelumenetelmä luo suunnittelut tilaukset vain niille tarpeille, jotka on luotu tai joita on muutettu edellisen ajoitetun pääsuunnitteluajon jälkeen. Nettomuutosmenetelmästä poiketen tässä menetelmässä vain uusien tai muuttuneiden tarpeiden toimintopäivät ja viivästyspäivät päivitetään. Tätä suunnittelumenetelmää käytetään vain dynaamisissa suunnitelmissa.

## <a name="types-of-scheduling-methods"></a>Ajoitusmenetelmätyypit

Kullekin suunnitelmalle on valittava tuotantotilauksissa käytettävä ajoitusmenetelmä **Pääsuunnitelmat**-sivun **Yleiset**-pikavälilehdessä (**Pääsuunnittelu \> Asetukset \> Suunnitelmat \> Pääsuunnitelmat**). Voit ajoittaa tuotannon työvaiheiden tasolla ja työn tasolla.

### <a name="operations-scheduling"></a>Työvaiheiden ajoitus

Työvaiheiden ajoitusta voidaan käyttää, kun tuotantoprosessin kestosta halutaan yleisarvio. Työvaiheiden ajoituksessa reitityksen tuotannon työvaiheita ei hajoteta töiksi. Lisätietoja työvaiheiden ajoittamisesta on kohdassa [Työvaiheiden ajoitus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Töiden ajoitus

Töiden ajoitus on tarkka ajoitusmenetelmä, jossa jokainen työvaihe jaetaan yksittäisiin tehtäviin tai töihin. Töiden ajoitus sisältää tietoja kapasiteetista. Sitä käytetään yleensä yksittäisten töiden ajoituksessa tuotannossa, ja normaalisti se tapahtuu välittömästi tai lyhyen ajan kuluessa. Lisätietoja työn ajoittamisesta on kohdassa [Työn ajoitus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Aikarajat päivissä

Voit valita molemmissa suunnitelmissa, kuinka pitkälle tulevaisuuteen pääsuunnittelun on laskettava erilaiset tarpeet ja muut huomionarvoiset seikat. Kautta pidetään *aikarajana*. Pääsuunnittelu toimii parhaiten, kun erilaiset aikarajat säädetään liiketoiminnan tarpeiden mukaan. Voit etsiä molemmissa suunnitelmissa aikarajat **Pääsuunnitelmat**-sivun **Aikarajat päivissä**-pikavälilehdessä (**Pääsuunnittelu \> Asetukset \> Suunnitelmat \> Pääsuunnitelmat**).

> [!NOTE]
> Aikarajat ilmaisevat, kuinka pitkälle tulevaisuuteen pääsuunnittelu laskee erilaiset tarpeet ja muut huomionarvoiset seikat. Tällä sivulla valitut aikarajat ohittavat kattavuusryhmässä määritetyt aikarajat. Niinpä kyllä-valinta aikaraja-asetuksessa ja päivien määrittäminen ohittaa kattavuusryhmässä määritetyn aikarajan. Jos asetukseksi valitaan Ei, aikaraja määritetään kattavuusryhmässä. Jos et kuitenkaan halua käyttää tätä asetusta tai et tarvitse sitä (jos et esimerkiksi halua käyttää toimintosanomaa), valitse asetukseksi **Kyllä** ja määritä aikarajaksi sitten **0** (nolla) päivää.

### <a name="coverage"></a>Kattavuus

Kattavuuden aikaraja ilmaisee ajoituskauden tai sen, kuinka pitkältä ajalta kysyntä on sisällytettävä. Se siis ilmaisee suunnitteluhorisontin.

Kun **Kattavuus**-asetukseksi valitaan **Kyllä**, voit ohittaa nimikkeelle pääajoituksen aikana määritetyn kattavuuden aikarajan. Määritä siinä tapauksessa, kuinka monen päivän ajalta pääajoituksen laskennan on katettava tarpeet. Kattavuuden aikaraja lasketaan eteenpäin nykyisestä päivämäärästä lähtien. Ennen nykyistä päivämäärää tapahtuvat tarpeet käsitellään aina.

> [!NOTE]
> Pääsuunnittelu toimii parhaiten, kun kattavuuden aikarajat säädetään suunnitteluhorisonttiin.

### <a name="freeze"></a>Lukitse

Lukitusaikaraja ilmaisee ajanjakson, jolloin aiemmin luotuja suunniteltuja tilauksia ei muuteta, kun uusi pääsuunnitelman ajoitus suoritetaan. Suunnitellut tilaukset lukitaan eikä uusia suunniteltuja tilauksia ehdoteta.

Kun **Lukitse**-asetukseksi valitaan **Kyllä**, voit ohittaa nimikkeelle pääajoituksen aikana määritetyn lukitusaikarajan. Määritä tässä tapauksessa, kuinka monen päivän ajalta suunnittelutoiminta on lukittava. Muista, että tänä aikana ei luoda uusia suunniteltuja tilauksia eikä aiemmin luotuja suunniteltuja tilauksia voi muuttaa.

### <a name="firming"></a>Vahvistus

Vahvistuksen aikaraja ilmaisee aikahorisontin, jolloin suunnitellut tilaukset muunnetaan automaattisesti tuotanto- ja ostotilauksiksi. Tätä prosessia kutsutaan myös *suunniteltujen tilausten automaattiseksi vahvistukseksi*.

Kun **Vahvistus**-asetukseksi valitaan **Kyllä**, voit ohittaa nimikkeelle pääajoituksen aikana määritetyn vahvistuksen aikarajan. Määritä siinä tapauksessa kuinka monen päivän aikana suunnitellut osto- ja tuotantotilaukset vahvistetaan automaattisesti. Vahvistuksen aikaraja lasketaan eteenpäin pääajoituksen päivämäärästä. Suunnitellut ostotilauksen automaattinen vahvistus on mahdollista vain, jos nimike on liitetty toimittajaan.

### <a name="forecast-plan"></a>Ennustesuunnitelma

Ennustesuunnitelman aikaraja ilmaisee, kuinka pitkälle tulevaisuuteen pääsuunnittelu luo ennustetun nimikekysynnän suunniteltuja tilauksia.

Kun **Ennustesuunnitelma**-asetukseksi valitaan **Kyllä**, voit ohittaa nimikkeelle pääajoituksen aikana määritetyn ennustesuunnitelman aikarajan. Määritä siinä tapauksessa, miten monen päivän ajalta ennustesuunnitelman myyntiennuste sisällytetään pääsuunnitteluun.

### <a name="capacity"></a>Kapasiteetti

Kapasiteetin aikaraja ilmaisee, kuinka pitkälle tulevaisuuteen järjestelmä ottaa huomioon resurssien maksimikapasiteetin, kun se ajoittaa tilauksia. Toisin sanoen suunnitelma ajoittaa tuotantotilaukset käyttämällä nimikkeiden tuotantoreittiä. Se ottaa huomioon myös tuotantoreitin resurssit ja kunkin resurssin maksimikapasiteetin.

Kun **Kapasiteetti**-asetukseksi valitaan **Kyllä**, voit ohittaa nimikkeelle pääajoituksen aikana määritetyn kapasiteetin aikarajan. Määritä siinä tapauksessa, kuinka monta päivää kapasiteettia suunnitellaan suunniteltuja tuotantotilauksia varten. Pääajoituksessa käytetään nimikkeen aktiivista tuotantoreittiä, ja ajoitus tehdään taaksepäin tarvepäivästä lähtien. Jos suunnitellun tuotantotilauksen tarvepäivämäärä on kapasiteetin aikarajan ulkopuolella, läpimenoaika määritetään nimikkeen toimitusajan perusteella. Kapasiteetin aikaraja lasketaan eteenpäin nykyisestä päivämäärästä.

### <a name="action-message"></a>Toimenpidesanoma

Toimenpidesanomat ehdottavat aiemmin luotuun toimituksen tilaukseen muutoksia, jotka optimoivat toimitussuunnitelman. Ne voivat esimerkiksi suositella tilausten tuomista lähemmäksi tai niiden viivästyttämistä tai tilausmäärien suurentamista tai pienentämistä.

Kun **Toimenpidesanoma**-asetukseksi valitaan **Kyllä**, voit ohittaa nimikkeelle pääajoituksen aikana määritetyn toimenpidesanoman aikarajan. Määritä siinä tapauksessa, montako päivää pääajoituksen on luotava tarpeiden toimenpidesanomia. Toimenpidesanoman aikaraja lasketaan eteenpäin nykyisestä päivämäärästä.

Lisätietoja toimenpidesanomista on kohdassa [Toimenpidesanomat](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Toimenpidesanomien laskeminen pidentää pääsuunnittelun ajoaikaa. Jos toimenpidesanomia ei analysoida ja käytetä säännöllisesti (kuten päivittäin tai viikoittain), harkitse laskennan poistamista käytöstä pääsuunnitteluajon aikana. Voit poistaa laskennan käytöstä määrittämällä **Pääsuunnitelmat**-sivulla suoritettavan pääsuunnitelman **Toimenpidesanoma**-aikarajaksi **0** (nolla). Varmista myös, että **Toimenpidesanoma**-asetus on poistettu käytöstä kaikissa kattavuusryhmissä.

### <a name="calculated-delays"></a>Lasketut viiveet

Voit määrittää, kuinka pitkälle tulevaisuuteen mahdolliset suunniteltujen tilausten viiveet havaitaan ja raportoidaan. Tällä tavoin voit ajoittaa mahdolliset (viivästyneet) toimituspäivät.

Jos pyydetyn päivämäärän suunniteltua tilausta ei voi täyttää, se suunnitellaan tapahtuman aikaisimmaksi täyttämispäiväksi läpimenoaikojen sekä materiaalin ja kapasiteetin saatavuuden perusteella.

### <a name="approved-requisitions-time-fence"></a>Hyväksyttyjen ehdotusten aikaraja

Voit määrittää pääsuunnittelun luomaan ehdotuksen kysynnän suunnitellut tilaukset. Määritä **Sisällytä ehdotukset** -asetukseksi **Kyllä** **Pääsuunnitelmat**-sivun **Yleiset**-pikavälilehdessä. Kun hyväksytyn ehdotuksen tarkoitus on sitten täydennys, pääsuunnittelu luo automaattisesti sen täyttämiseen vastaavan suunnitellun tilauksen. Täydennysmenetelmä määritetään organisaation nimikkeille asettamien ostokäytäntöjen perusteella. Kun täydennysehdotus on luotu ja hyväksytty, käyttäjän lisätoimia ei tarvita.

Kun **Hyväksyttyjen ehdotusten aikaraja** -asetukseksi määritetään **Kyllä** **Aikarajat päivissä** -pikavälilehdessä, voit ohittaa nimikkeelle pääajoituksen aikana määritetyn hyväksyttyjen ehdotusten aikarajan. Määritä siinä tapauksessa, miten monen jo kuluneen päivän ajalta kysyntä täydennystarkoituksiin tehdyistä hyväksytyistä ehdotuksista on sisällytettävä pääajoitukseen. Voit esimerkiksi määrittää, että vain viimeisen 10 päivän aikana täyttämättömänä luodut ehdotukset huomioidaan ja otetaan mukaan suunnitelmaan.

### <a name="sequencing"></a>Järjestys

Järjestyksen avulla suunnitellut tilaukset voidaan järjestää valmiiseen tuotteeseen liitettyjen järjestysmääritteiden perusteella. Sitä käytetään usein valmistelemaan tuotantotilausten pakkaamista. Sitä voidaan käyttää esimerkiksi pakkaamaan laatikot tietyssä järjestyksessä värin ja koon perusteella.

Kun **Järjestys**-asetukseksi määritetään **Kyllä**, voit määrittää, kuinka pitkälle tulevaisuuteen työvaiheet tai työt järjestetään. Muista, että mitä pidempi aikaraja on, sitä kauemmin pääsuunnittelun suorittaminen kestää.

### <a name="calculated-delays"></a>Lasketut viiveet

Viiveasetusten avulla voidaan varmistaa, että tilausten suunnitellut päivämäärät ovat mahdollisia. Seuraavat asetukset ovat valittavissa **Pääsuunnitelmat**-sivun **Lasketut viiveet** -pikavälilehdessä:

- **Varmista, että suunniteltuja tilauksia ei luoda ennen pääsuunnittelun suorituspäivää** – kun asetukseksi määritetään **Kyllä**, tilauksia ei voi ajoittaa menneille päivämäärille.
- **Lisää laskettu viive tarvepäivämäärään** (**Suunnitellut ostotilaukset** -kohdassa) – kun asetuksessa valitaan **Kyllä**, tarpeelle laskettu viive lisätään.
- **Lisää laskettu viive tarvepäivämäärään** (**Suunnitellut tuotantotilaukset** -kohdassa) – kun asetuksessa valitaan **Kyllä**, tarpeelle laskettu viive lisätään.
- **Lisää laskettu viive tarvepäivämäärään** (**Suunniteltu siirto** -kohdassa) – kun asetuksessa valitaan **Kyllä**, tarpeelle laskettu viive lisätään.
- **Lisää laskettu viive tarvepäivämäärään** (**Suunniteltu kanban** -kohdassa) – kun asetuksessa valitaan **Kyllä**, tarpeelle laskettu viive lisätään.

Kun **Lisää laskettu viive tarvepäivämäärään** -asetukseksi määritetään **Kyllä**, jotta tarpeisiin voidaan lisätä viiveet, järjestelmä ottaa huomioon resurssien kapasiteetin ja luo mahdollisia suunniteltuja tilauksia. Suunniteltujen tilauspäivämäärien uudelleenlaskenta pidentää pääsuunnittelun suoritusaikaa. Jos et halua käyttää viiveitä, valitse asetuksissa **Ei.**

## <a name="positive-and-negative-days"></a>Positiiviset ja negatiiviset päivät

Positiiviset ja negatiiviset päivät vaikuttavat siihen, miten pääsuunnittelu ehdottaa suunniteltuja tilauksia ja toimenpiteitä. Positiiviset ja negatiiviset päivät määritetään nimikkeen kattavuusryhmässä. Voit määrittää eri kattavuusryhmiä ja määrittää niiden parametrit **Kattavuusryhmät**-sivulla (**Pääsuunnittelu \> Asetukset \> Kattavuus \> Kattavuusryhmät**).

### <a name="positive-days"></a>Positiiviset päivät

Positiiviset päivät ilmaisevat, kuinka pitkälle tulevaisuuteen pääsuunnittelu ottaa huomioon nykyisen varaston tai vastaanotot tulevan kysynnän täyttämisessä. Jos positiivisten päivien arvoksi on esimerkiksi määritetty **100**, nykyistä varastoa voidaan käyttää täyttämään kysyntää seuraavan 100 päivän ajan. Jos tilaus on 150 päivän päässä kuluvasta päivästä, pääsuunnittelu luo suunnitellun tilauksen täyttämään kyseisen kysynnän, vaikka nimikkeen varastosaldo riittäisi tilauksen täyttämiseen. Jos nimikkeen vaihtuvuus on suuri ja läpimenoaika on lyhyt, näin kaukana tulevaisuudessa olevassa tilauksessa ei ehkä kannata käyttää varastosaldoa. Tällaisessa suuren vaihtuvuuden tapauksessa nykyinen varastosaldo käytetään nopeasti ja tulevaisuuteen voidaan asettaa lisää tilauksia täyttämään tulevaa kysyntää, mikä on mahdollista nimikkeen lyhyen läpimenoajan vuoksi.

Positiiviset päivät vaikuttavat myös toimenpidesanomiin. Järjestelmä voi esimerkiksi suositella, että suunniteltua ostotilausta suurennetaan siten, että sisältää kysynnän, joka on tulevaisuuteen sijoittuvien positiivisten päivien alueella. Jos positiivisten päivien arvoksi on määritetty **100** ja jos nimikkeellä on kysyntää 30 päivän kuluttua kuluvasta päivästä, järjestelmä luo suunnitellun tilauksen vastaamaan tätä kysyntää. Jos samalla nimikkeellä on kysyntää 90 päivän kuluttua kuluvasta päivästä, järjestelmä suosittelee, että lisäät 30 päivän päässä kuluvasta päivästä oleva tilauksen määrää siten, että se kattaa myös 90 päivän kysynnän. Jos kysyntää on kuitenkin 150 päivän päässä kuluvasta päivästä, järjestelmä ei suosittele, että lisää jo suunnitellun tilauksen määrää. Sen sijaan luodaan uusi suunniteltu tilaus.

Positiivisten päivien määräksi määritetään säännönmukaisesti arvo, joka nimikkeen pisimmän läpimenoajan ja kattavuuden aikarajan välissä. Säännöllisesti hankitut tai tuotetut nimikkeet kannattaa määrittää kattavuusryhmään, jossa positiivisten päivien arvo on sama kuin nimikkeen läpimenoaika.

### <a name="negative-days"></a>Negatiiviset päivät

Negatiiviset päivät ilmaisevat, kuinka paljon nimikkeiden vastaanotot voivat olla myöhässä. Ne ilmaisevat päivien määrän, jonka olet valmis odottamaan ennen uuden täydennyksen tilaamista, kun varasto on negatiivinen tai varastoa ei ole riittävästi. Negatiivisten päivien avulla vastataan kysymykseen siitä, onko nimikkeelle luotava uusi ostotilaus vai käytetäänkö aiemmin luotua ostoa, vaikka nimikkeen tiedetään olevan myöhässä.

Esimerkki: sinulla on nimikkeen myyntitilaus 15 päivän päässä kuluvasta päivästä. Sinulla on myös saman nimikkeen ostotilaus. Tämä ostotilaus vastaanotetaan 20 päivän kuluttua kuluvasta päivästä. Haluatko, että järjestelmä luo kyseiselle myyntitilaukselle ostotilauksen, vai haluatko käyttää aiemmin luotua tilausta, vaikka et voi täyttää myyntitilausta ajoissa? Jos negatiivisten päivien määritetty arvo on pienempi kuin **5**, se ilmaisee, että nimike voi viivästyä enintään viisi päivää, järjestelmä luo uuden suunnittelun ostotilauksen täyttämään myyntitilauksen. Jos negatiivisten päivien määritetty arvo on suurempi kuin **5**, järjestelmä käyttää nimikkeen aiemmin luotua tilausta.

Negatiiviset päivät vaikuttavat myös pääsuunnittelun suorituskykyyn. Jos negatiivisten päivien arvo on suuri, toimenpidesanomia muodostetaan runsaasti.

Negatiivisten päivien arvon kannattaa olla pienempi kuin nimikkeen läpimenoaika.

### <a name="dynamic-negative-days"></a>Dynaamiset negatiiviset päivät

Dynaamiset negatiiviset päivät ottavat huomioon nimikkeen läpimenoajan ja määritetyt negatiiviset päivät. Järjestelmä luo uuden suunnitellun ostotilauksen sen negatiivisten päivien aikarajan perusteella, joka lasketaan seuraavalla kaavalla:

läpimenoaika + negatiiviset päivät + kuluva päivä – tarvepäivä.

Järjestelmä käyttää vain tälle aikarajalle sijoittuvia suunniteltuja toimitustilauksia, ja se luo uuden suunnitellun tilauksen aikarajan ulkopuolelle. Dynaamisten negatiivisten päivien etuna on, että siihen sisältyy yksittäisen tuotteen läpimenoaika. Lisäksi se käyttää uudelleen aiemmin luotuja tilauksia ja välttää sellaisten uusien suunniteltujen tilausten luomisen, joiden päivämäärä tulee olemaan myöhäisempi läpimenoajan aiheuttamien viiveiden vuoksi. 

Lisätietoja on kohdassa [Negatiiviset päivät ja dynaamiset negatiiviset päivät](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]