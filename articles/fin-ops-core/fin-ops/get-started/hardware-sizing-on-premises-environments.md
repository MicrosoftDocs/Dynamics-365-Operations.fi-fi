---
title: Laitteiston kokovaatimukset paikallisissa ympäristöissä
description: Tässä ohjeaiheessa käsitellään laitteiston kokovaatimukset paikallisissa ympäristöissä
author: sericks007
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: c5e6e96ea1ce821233d7104bb9a7af8e793f4264
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923477"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Laitteiston kokovaatimukset paikallisissa ympäristöissä

[!include [banner](../includes/banner.md)]

Tutustu ennen laitteiston ja infrastruktuurin koon määrittämistä paikallisiin ympäristöihin ja [pilvikäyttöönottojen järjestelmävaatimuksiin](system-requirements.md) sekä [asennus- ja käyttöönotto-ohjeisiin](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), sillä saat niiden avulla selkeän käsityksen perustana olevasta infrastruktuurista.

> [!NOTE]
> Perehdy huolellisesti järjestelmän asetuksen parhaisiin käytäntöihin, jotta järjestelmä toimisi mahdollisimman hyvin.

Kun olet perehtynyt dokumentaatioon, voit aloittaa tapahtumien ja samanaikaisten käyttäjien määrää sekä määrittämään ympäristön koon ytimen keskimääräisen siirtomäärän perusteella.

## <a name="factors-that-affect-sizing"></a>Kokoon vaikuttavia tekijöitä

Kaikki seuraavan kuvan tekijät vaikuttavat koon. Mitä tarkempia kerätyt tiedot ovat, sitä tarkemmin voit määrittää koon. Jos laitteiston koko määritetään ilman taustatietoja, lopputulos ei ole todennäköisesti tarkka. Suurin tapahtumarivien määrä tunnissa on tieto, joka vähintäänkin tarvitaan.

[![Laitteiston koon määrittäminen paikallisissa ympäristöissä](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Vasemmalta oikealle tarkasteltaessa tärkein tekijä, jonka avulla koko voidaan määrittää tarkasti, on tapahtumaprofiili tai tapahtuman kuvaus. On tärkeää, että suurin tapahtumien määrä tunnissa on tiedossa. Jos kuormitushuippuja on useita, nämä jaksot on määritettävä tarkasti.

Kun tiedät, miten kuormitus vaikuttaa infrastruktuuriin, sinun on saatava tarkemmat tiedot myös seuraavista tekijöistä:

- **Tapahtumat** – Tapahtumilla on tavallisesti tietty huippu päivän tai viikon aikana. Se puolestaan määräytyy lähinnä tapahtumatyypin mukaan. Aika- ja tapahtumakirjauksissa huippu on yleensä kerran viikossa, kun taas myyntitilauskirjaukset tapahtuvat usein kerralla integroinnin kautta tai vähitellen päivän mittaan.
- **Yhtäaikaisten käyttäjien määrä** – Yhtäaikaisten käyttäjien määrä on toiseksi tärkein kokoon vaikuttava tekijä. Kokoarvioita ei saa luotettavasti yhtäaikaisten käyttäjien määrän perusteella, joten jos sinulla on vain nämä tiedot, arvioi määrä suunnilleen ja palaa tähän kohtaan, kun sinulla on enemmän tietoja. Yhtäaikaisen käyttämän tarkan määritelmän mukaan

    - nimetyt käyttäjät eivät ole yhtäaikaisia käyttäjiä
    - yhtäaikaiset käyttäjät ovat aina nimettyjen käyttäjien alijoukko 
    - suurin kuormitus määrittää suurimman yhtäaikaisten käyttäjien määrän kokoa määritettäessä.

    Yhtäaikainen käyttäjä on käyttäjä, joka täyttää kaikki seuraavat ehdot:

    - kirjautunut sisään
    - käyttää tapahtumia tai kyselyjä laskennan aikana
    - istunto ei ole käyttämätön.

- **Tietoja kokoonpano** – Tämä tarkoittaa lähinnä sitä, miten järjestelmä asennetaan ja määritetään. Kyse voi olla esimerkiksi yritysten, nimikkeiden ja tuoterakennetasojen määrästä sekä suojausasetusten monimutkaisuudesta. Kukin näistä tekijöistä voi vaikuttaa jonkin verran suorituskykyyn, joten älykkäät infrastruktuuriratkaisut voivat kumota näiden tekijöiden vaikutuksen.
- **Laajennukset** – Mukautukset voivat olla yksinkertaisia tai monimutkaisia. Mukautusten määrä ja niiden monimutkaisuus ja käyttö vaikuttavat eri tavoin tarvittavan infrastruktuurin kokoon. Monimutkaisissa mukautuksissa kannattaa suorittaa suorituskykyarviointeja ja varmistaa näin teho testataan. Samalla saadaan parempi käsitys infrastruktuurin tarpeista. Tämä on entistäkin tärkeämpää, kun laajennuksia ei ole koodattu suorituskyvyn ja skaalautuvuuden parhaiden käytäntöjen mukaisesti.
- **Raportointi ja analytiikka** – Nämä tekijät sisältävät yleensä raskaiden kyselyjen tekemistä useissa järjestelmän tietokannoissa. Tieto siitä, milloin laajoja raportteja ajetaan, ja niiden vähentäminen auttaa ymmärtämään, mikä vaikutus niillä on.
- **Kolmannen osapuolen ratkaisut** – näillä ratkaisuilla, kuten riippumattomilla ohjelmistotoimittajilla, on samat vaikutukset ja suositukset kuin laajennuksilla.

## <a name="sizing-your-environment"></a>Ympäristön mitoitus

Sinun on tiedettävä suurin käsiteltävä tapahtumien määrä kokovaatimusten selvittämiseksi. Useimmat lisäjärjestelmät, kuten Management Reporter tai SSRS, eivät ole toiminnan kannalta yhtä tärkeitä. Tämän vuoksi tässä asiakirjassa käsitellään lähinnä AOS-palvelinta ja SQL Serveriä.

> [!NOTE]
> Yleensä ottaen laskentatasot skaalautuvat ylöspäin ja ne on syytä määrittää muodossa N+1 – toisin sanoen jos arvioit tarpeeksi kolme AOS-palvelinta, lisää neljäs AOS. Tietokantataso on määritettävä aina päällä olevana suuren käytettävyyden asennuksena.

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Koko

- 3 000–15 000 tapahtumariviä/tunti/ydin tietokantapalvelimessa.
- Ensisijaisen SQL Serverin tavallinen AOS–SQL-ydinsuhde on 3:1. Lisäytimiä tarvitaan valitun suuren käyttävyyden määrityksen perusteella.

    - Paljon tietokantoja käyttävien toimenpiteiden käsittely jo pienentää suhteeksi 2:1.

- Seuraavat tekijät vaikuttavat vaihteluun:

    - Käytettävät parametriasetukset.
    - Laajennusten tasot.
    - Lisätietojen, kuten tietokantalokin ja hälytysten, käyttö. Suuri tietokantalokiin kirjaus pienentää entisestään tunti- ja ydinkohtaisen siirtomäärän alle 3 000 riviin.
    - Tietojen kokopanon monimutkaisuus – esimerkiksi yksinkertaisen tilikartan tai tarkan ja yksityiskohtaisen tilikartan valitsimen vaikuttaa siirtomäärään.
    - Tapahtuman kuvaus.
    - 2–16 Gt muistia/ydin.
    - Tietokantapalvelimen lisätietokannat, kuten Management Reporter- ja SSRS-tietokannat.
    - Tilapäistietokanta = 15 prosenttia tietokannan koosta, ja tiedostoja on yhtä paljon kuin fyysisiä suorittimia.
    - SAN-koko ja -siirtomäärä yhtäaikaisten tapahtumien yhteismäärän ja -käytön perusteella.

### <a name="high-availability"></a>Suuri käytettävyys

SQL Serveriä kannattaa aina käyttää joko klusterina tai peilaavana asennuksena. Toisessa SQL-solmussa on oltava yhtä monta ydintä kuin ensisijaisessa solmussa.

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory -liittoutumispalvelut (AD FS)

Lisätietoja AD FS -kokomäärityksistä on [AD FS:n palvelinkapasiteetin dokumentaatiossa](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Käyttöönoton esiintymien määrän suunnittelua varten on [kokotaulukko](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx).

## <a name="aos-online-and-batch"></a>AOS (verkko ja erä)

### <a name="sizing"></a>Koko

- Tapahtumien määrän ja käytön mukaan tapahtuva koon määritys

    - 2 000–6 000 riviä/ydin
    - 16 Gt/esiintymä
    - Vakiorunko – 4–24 ydintä
    - 10–15 Enterprise-käyttäjää/ydin
    - 15–25 tehtäväkäyttäjää/ydin
    - 25–50 ryhmän jäsentä/ydin

- Erä

    - 1–4 eräsäiettä/ydin
    - Koko perustuu eräikkunan kuvaukseen

- Huomaa, että AOS, tietojen hallinta ja erä ovat samassa roolissa Service Fabricissa. Koko on määritettävä näiden kolmen toiminnon yhdistetylle kuormitukselle eikä erikseen niin kuin Microsoft Dynamics AX 2012:ssa.
- SQL Serverin vaihtelutekijät koskevat myös näitä kokomäärityksiä.

### <a name="high-availability"></a>Suuri käytettävyys

- Varmista, että käytettävissä on vähintään 1–2 AOS-palvelinta enemmän kuin mitä arvioit.
- Varmista, että käytettävissä on ainakin 3–4 virtuaali-isäntää.

## <a name="management-reporter"></a>Management Reporter

Ellei käyttö ole erittäin suurta suositeltu vähimmäisvaatimus on useimmissa tapauksissa kaksi solmua. Vain siinä tapauksessa, että käyttö on erittäin runsasta, tarvitaan enemmän kuin kaksi solmua. Skaalaa tarpeen mukaan.

## <a name="sql-server-reporting-services"></a>SQL Server -raportointipalvelut.

Yleisesti saatavilla olevassa julkaisuversiossa voidaan ottaa käyttöön vain yksi SSRS-solmu. Seuraa SSRS-solmua testauksen aikana ja lisää SSRS:n käytössä olevien ytimien määrää tarvittaessa. Varmista, että virtuaali-isäntään valmiiksi määritetty toissijainen solmu ei ole sama kuin SSRS VM. Tämä on tärkeää, jos SSRS:ää isännöivässä virtuaalikoneessa tai virtuaali-isännässä on ongelma. Siinä tapauksessa ne on vaihdettava.

## <a name="environment-orchestrator"></a>Ympäristön Orchestrator-palvelu

Orchestrator-palvelu hallitsee käyttöönottoa ja siihen liittyviä LCS-yhteyksiä. Palvelu otetaan käyttöön ensisijaisena Service Fabric -palveluna, ja sitä varten tarvitaan vähintään kolme VM-konetta. Palvelu on samassa sijainnissa kuin Service Fabricin Orchestration-palvelut. Sen koon pitäisi perustua klusterin suurimpaan kuormitukseen. Lisätietoja on ohjeaiheessa [Service Fabric -klusterin erillisen käyttöönoton suunnittelu ja valmistelu](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="virtualization-and-oversubscription"></a>Virtualisointi ja ylitilaus

Toiminnan kannalta keskeiset palvelut, kuten AOS, on isännöitävä virtuaali-isännissä, joille on varattu omat resurssit (ytimet, muisti ja levy).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]