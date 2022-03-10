---
title: Finance and Operations -sovellusten palvelunkuvaus
description: Tässä ohjeaiheessa esitetään Finance and Operations -sovellusten palvelunkuvaus.
author: tomhig
ms.date: 01/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 85f82a863f0bde4c0414760fa2477651242538f2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952363"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Finance and Operations -sovellusten palvelunkuvaus

[!include[banner](../includes/banner.md)]

Finance and Operations -sovellukset ovat yrityksen resurssisuunnittelun (ERP) ohjelmisto palveluna (SaaS) -tuotteita, jotka perustuvat [Microsoft Azureen](https://azure.microsoft.com/overview/what-is-azure/) ja on suunniteltu sitä varten. Finance and Operations -palvelu tarjoaa organisaatioille ERP-toimintoja, jotka tukevat niiden yksilöllisiä vaatimuksia ja auttavat niitä mukautumaan jatkuvasti muuttuviin liiketoimintaympäristöihin ilman tarvetta hallita infrastruktuuria. Finance and Operations -sovellukset voivat sisältää yhden tai useampia seuraavista ratkaisualueista:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Yhdessä [yritystietojen](/power-bi/fundamentals/power-bi-service-overview), [infrastruktuurin](https://azure.microsoft.com/global-infrastructure/), [laskennan](/azure/service-fabric/service-fabric-overview) ja [tietokantapalvelujen](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) kanssa nämä sovellukset mahdollistavat organisaatioille toimialakohtaisten ja toiminnallisten liiketoimintaprosessien suorittamisen. Asiakkaat määrittävät käyttöönottokumppaninsa tuella yrityssovelluksen logiikan määrityksen, joka sopii parhaiten sen yksilöllisille liiketoimintaprosesseille. Toimintoja ja liiketoimintaprosesseja voi kasvattaa tai laajentaa yhdellä tai useammalla seuraavista ratkaisuista:

- Sisäinen [mukautuskokemus](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md) -työkalut
- [Visual Studio](https://visualstudio.microsoft.com) -pohjainen [Finance and Operationsin ohjelmistonkehityspaketti (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) ja [Azure DevOpsin kehitysautomaatio](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Riippumattomien ohjelmistotoimittajien (ISV) ratkaisut [AppSourcesta](https://appsource.microsoft.com/partners)

Asiakkaat valitsevat ratkaisuvaihtoehtonsa vaatimustensa perusteella. Ne määrittävät, kehittävät ja testaavat ratkaisunsa yhteistyössä käyttöönottokumppaninsa kanssa käyttämällä [Microsoft Dynamics Lifecycle Servicesin (LCS)](../../dev-itpro/lifecycle-services/lcs.md) työkaluja ja parhaita käytäntöjä. Yleisiä skenaarioita on neljä:

- Vakiomallisten Finance and Operations -sovellusten käyttövalmis määritys (ei laajennuksia)
- Finance and Operations -sovellusten määritys, johon kuuluu vähintään yksi ISV-ratkaisu
- Finance and Operations -sovellusten määritys, johon kuuluu vähintään yksi asiakaskohtainen laajennus
- Finance and Operations -sovellusten määritys, johon kuuluu yhdistelmä asiakaskohtaisista laajennuksista ja vähintään yhdestä ISV-ratkaisusta

Organisaatiot voivat täsmätä liiketoiminnan kasvunsa lisäämällä käyttäjiä ja liiketoimintaprosesseja yksinkertaisen ja avoimen ylläpitosopimusmallin avulla. Lisätietoja: [Dynamics 365:n käyttöoikeusopas](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Toimintamalli

Finance and Operations -sovellusten toimintamalli määrittää asiakkaalle, käyttöönottokumppanille ja Microsoftille erityisiä rooleja ja vastuita palvelun koko elinkaaren ajalle. Lisätietoja: [Pilvipalvelut ja huolto](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Asiakkaan toimet

Asiakkaat työskentelevät kumppaninsa kanssa ottaakseen ratkaisunsa käyttöön käyttäen [Microsoft FastTrackia](/dynamics365/fasttrack/) noudattaen [Dynamics 365 -käyttöönotto-opasta](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), [Success by Design](/dynamics365/fasttrack/success-by-design-overview) -kehystä sekä [Lifecycle Servicesin](../../dev-itpro/lifecycle-services/lcs.md) työkaluja ja parhaiden käytäntöjen malleja. Yleisiä toimia ovat esimerkiksi:

- Käyttäjätietojen ja suojauksen hallinta
- Liiketoimintaprosessien määrittäminen, kehittäminen ja käyttö
- Laajennusten määrittäminen, kehittäminen, testaaminen ja käyttö
- Tuotannon ulkopuolisten käyttöönottojen seuranta ja hallinta
- Sovelluspäivitysten hallinta ja laajennusten vahvistaminen
- ISV-ratkaisujen ja kolmannen osapuolen integrointien hallinta

### <a name="microsoft-responsibilities"></a>Microsoftin vastuut

Microsoft hallitsee Finance and Operations -palvelua ottamalla käyttöön asiakkaan eristys- ja tuotantoympäristöjä Microsoft SaaS-ylläpitosopimuksessa sekä seuraamalla niitä aktiivisesti ja huoltamalla niitä. Tähän hallintaan kuuluu palvelun suorittamiseen vaadittavan järjestelmäinfrastruktuurin kohdistaminen sekä ennakoiva palvelun kuntoa koskeva viestintä asiakkaiden kanssa. Vastuualueisiin kuuluvat:

**Infrastruktuurinhallinta**
- Suojaus ja eristys
- Käyttöjärjestelmät ja virtualisointi
- Palvelimet, tallennustila ja verkkopalvelut
- Palvelinkeskuksen sähkö, verkkopalvelut ja jäähdytys

**Sovellusympäristön hallinta**
- Ympärivuorokautinen sovellusten seuranta ja ilmoitukset
- Diagnostiikka, ympäristöpäivitykset, korjaustiedostot, huoltopäivitykset
- Sovellusreititys, kuormituksen tasaus, sivuston replikointi
- Ympäristön valmistelu ja hallinta
- Tietokannan hallinta, korkea käytettävyys / järjestelmäpalautus, skaalaus, työvaiheet
- Käyttöönoton käsittely, skaalaus molempiin suuntiin

## <a name="system-configuration"></a>Järjestelmän konfigurointi

Finance and Operations -sovellukset skaalautuvat tapahtumakoon ja käyttäjäkuorman mukaan. Kunkin asiakastoteutuksen tuloksena on ainutkertainen ratkaisu, joka koostuu seuraavista osista:

- **Tietokokoonpano** – Yksilöllinen parametrijoukko, joka ohjaa toimintaa, organisaation rakennetta, päätietojen (kuten taloushallinto- ja varastodimensiot) rakennetta sekä tapahtumaseurannan tarkkuutta.
- **Laajennus ja määritys** – Laajennusmekanismeja, jotka käyttävät koodilaajennuksia, ISV-ratkaisuja ja yksilöityjä määrityksiä, jotka sisältävät työnkulkuja, integrointeja ja raportinmäärityksiä.
- **Käyttömallit** – Ainutkertainen online- ja eräkäytön yhdistelmä, kyky integroitua yläpuolisiin ja alapuolisiin järjestelmiin yhtenäistä tietovuota varten sekä mahdollisuus tehdä eroja asiakkaiden liiketoimintaprosesseissaan käyttämien tietonäkymien perusteella.

Microsoft määrittää asiakkaan tuotantoympäristöt, jotka mitoitetaan käsittelemään tapahtumakoot ja käyttäjien samanaikaisuus. Microsoft vastaa seuraavista tehtävistä:

- Tuotantoympäristöjen resurssien oikea kohdistaminen asiakkaan [LCS:n tilauksen arviointityökalussa](../../dev-itpro/lifecycle-services/subscription-estimator.md) olevien asiakkaan profilointitietojen perusteella
- Tuotantoympäristöjen palvelun käytettävyyden jatkuva seuranta
- Finance and Operations -sovellusten järjestelmän suorituskykyongelmien analysointi ja vianmääritys

Varmistaakseen, että toteutus on määritetty korkeaa suorituskykyä varten asiakkaiden on suoritettava seuraavat tehtävät:

- Tarkkojen Finance and Operations -toteutuksen käyttötietojen antaminen [LCS:n tilauksen arviointityökalussa](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Suorituskyvyn ja koon laajennusten kehittäminen ja testaus
- Tietomääritysten asianmukainen testaus suorituskyvyn osalta
- Skaalautuvuuden varmistaminen suorittamalla [suorituskykytestausta](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) ennen lopullista käyttöönottoa.

## <a name="onboarding-and-implementation"></a>Käyttöönotto ja toteutus

Seuraavassa taulukossa esitetään tyypillisiä käyttöönotto- ja toteutustapahtumia.

| Pyyntö | Odotettu Microsoftin toimenpide | Odotettu asiakkaan/käyttöönottokumppanin toimenpide |
|---|---|---|
| Alun tarjouksen ostaminen | Tarjouksen ostamisen jälkeen luodaan LCS-projekti asiakkaan käynnistämän tapahtuman perusteella. | Käy läpi Enterprise Agreement (EA) -sopimuksen tai pilvipalveluratkaisujen toimittajan (CSP) [kaupallinen prosessi](before-you-buy.md). Kumppani luo asiakkaalle tarvittaessa vuokraajan. |
| Lisäosan osto | Antaa asiakkaalle käyttöoikeuden käyttöönoton aikana valittuun lisäosaan. | Ei käytettävissä |
| Käyttöönoton suunnittelu ja analyysi | Tarjoa LCS:ssä asianmukaisia työkaluja, kuten [Liiketoimintaprosessien mallintaja (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) ja [yhteiskäyttö Azure DevOpsin kanssa](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Projektisuunnittelun tekeminen, Azure DevOpsis määritys, järjestelmän käyttöönoton loppuun suorittaminen ja järjestelmänvalvojien tilien määritys. |

Lisätietoja: [Käyttöönotto- ja toteutusprojekti](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Maailmanlaajuinen toiminta

Finance and Operations -sovelluksia tarjotaan useilla eri Azure-alueilla ympäri maailmaa. Finance and Operations -sovellukset tukevat eri maita tai alueita ja äidinkieliä. Lisätietoja: [Lokalisointi- ja säädösominaisuudet](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Maa- tai aluekohtaiset seikat

- Säädellyissä teollisuus- tai kauppaorganisaatioissa toimivat asiakkaat, jotka harjoittavat liiketoimintaa sellaisten Ranskassa toimivien yritysten kanssa, joilta vaaditaan paikallista tietojen sijaintia, kannattaa tutustua aiheeseen [Finance and Operations Ranskassa](../../dev-itpro/deployment/france-local-deployment.md).
- Asiakkaiden, jotka toimivat Kiinassa kannattaa tutustua artikkeleihin [Azure Kiinassa -käsikirja](/azure/china/) ja [Finance and Operations 21Vianetin tarjoamana Kiinassa](../../dev-itpro/deployment/china-local-deployment.md).
- Venäjällä toimivien asiakkaiden kannattaa tutustua aiheeseen [Venäjän henkilötietojen lokalisointilaki](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Yleinen tietosuoja-asetus (GDPR)

Finance and Operations -sovelluksissa Microsoft toimii henkilötietojen käsittelijänä. Henkilötietojen käsittelijänä Finance and Operations tarjoaa prosesseja ja ominaisuuksia, joiden avulla asiakkaat voivat täyttää GDPR-velvollisuutensa rekisterinpitäjänä. Lisätietoja: [GDPR-yhteenveto](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Ympäristön- ja tiedonhallinta

Tässä osassa kuvataan tyypillisiä ympäristön- ja tiedonhallinnan tapahtumia, joita esiintyy palvelussa.

### <a name="environment-and-data-management-events-for-production-instances"></a>Tuotantoesiintymien ympäristö- ja tiedonhallintatapahtumat

LCS tarjoaa [itsepalvelutyökaluja](../../dev-itpro/deployment/infrastructure-stack.md) ja [tietokannan siirtotoimintoja](../../dev-itpro/database/dbmovement-operations.md), joita käytetään ympäristön- ja tiedonhallinnan tehtäviä. Seuraavassa on muutamia esimerkkejä:

**Tapahtuma:** [Tuotantoesiintymän pyytäminen](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Täytä [Lopullisen käyttöönoton tarkistuslista](../imp-lifecycle/prepare-go-live.md) ja lähetä se [Microsoft FastTrack](/dynamics365/fasttrack/) -tiimille.
- Suorita [LCS:n tilauksen arviointityökalu](../../dev-itpro/lifecycle-services/subscription-estimator.md), ennen kuin pyydät tuotantoesiintymää.
- Suorita kaikki [LCS-menetelmässä](../../dev-itpro/lifecycle-services/create-methodology.md) eritellyt käyttöönottotehtävät.

**Tapahtuma:** [Eristystietokannan kopiointi tuotantoesiintymään](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Suoritetaan lopullisen käyttöönoton testaukselle tai todelliselle lopulliselle käyttöönotolle.

**Tapahtuma:** [Ylläpitotila](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Ota ylläpitotila LCS:ssä.
2. Suorita tarvittavat ylläpitotoimet.
3. Poista ylläpitotila käytöstä LCS:ssä.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Muiden kuin tuotantoesiintymien ympäristö- ja tiedonhallintatapahtumat

LCS tarjoaa [valmistelua itsepalveluna](../../dev-itpro/deployment/infrastructure-stack.md) ja [tietokannan siirtotoimintoja](../../dev-itpro/database/dbmovement-operations.md), joita käytetään ympäristön- ja tiedonhallinnan tehtäviä. Seuraavassa on muutamia esimerkkejä:

**Tapahtuma:** [Uuden eristysesiintymän käyttöönotto](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Varmista, että kaikki tarvittavat esiintymät on [suunniteltu](../imp-lifecycle/environment-planning.md) ja että soveltuvat lisäosatarjoukset on ostettu.
- Suorita käyttöönottoprosessi LCS:ssä.
- Suorita kaikki LCS-tarkistusluettelossa eritellyt tehtävät.
    
>[!NOTE]
>Kehityksen eristysympäristö on näennäiskone (VM), joka [otetaan käyttöön asiakkaan Azure-tilauksessa](../../dev-itpro/dev-tools/access-instances.md) ja jonka hallinnasta vastaa asiakas.

**Tapahtuma:** [Ihannemääritystietokannan kopiointi eristyksestä tuotantoon](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Suoritetaan lopullisen käyttöönoton testaukselle tai todelliselle lopulliselle käyttöönotolle.

**Tapahtuma:** [Tuotannon tietyn ajankohdan varmuuskopion palautus muuhun kuin tuotantoesiintymään](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Suorita [Päivitä tietokanta](../../dev-itpro/database/database-refresh.md) -asetus LCS:ssä.
- Kopioinnin jälkeen: Poista tai piilota luottamukselliset tiedot komentosarjojen avulla, muokkaa ympäristökohtaisia sovellusmäärityksiä (kuten integroinnin päätepisteitä) ja ota käyttöön tai lisää käyttäjiä. Huomaa, että nämä muutokset tehdään käyttämällä [tietopakettia](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Tapahtuma:** [Muun kuin tuotantoesiintymän tietokannan tietyn ajankohdan palautus](../../dev-itpro/database/database-point-in-time-restore.md)

- Hyväksy, että prosessia ei voi peruuttaa.
- Suorita tietyn ajankohdan palautustoiminto LCS:ssä.

**Tapahtuma:** Tason 2 eristystietokannan kopiointi kehityseristysympäristöön vianmääritystä ja [virheenkorjausta](../../dev-itpro/database/dbmovement-scenario-debugdiag.md) varten

- Suorit tietokannan vientitoiminto LCS:ssä tason 2 eristysympäristölle.
- Tuo ja päivitä tietokanta kehitysympäristössä.

## <a name="data-backup-and-retention"></a>Tietojen varmuuskopiointi ja säilytys

SaaS-tilauksen Finance and Operations -ympäristöjen tietokannat suojataan automaattisin varmuuskopioin. Tuotantoympäristöjen osalta automaattisia varmuuskopioita säilytetään 28 päivää, ellei Microsoft suorita palautusta. Eristysympäristöjen (taso 2–) osalta ne säilytetään seitsemän päivää. Tuotantoympäristön palautus voidaan suorittaa, jos tapahtuu virhe minkä tahansa suunnitellun ylläpitopäivityksen yhteydessä.

Lisätietoja automaattisista varmuuskopioista: [Automaattiset varmuuskopiot – Azuren SQL-tietokanta ja SQL:n hallittu esiintymä](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Huoltotoimien vastuut

Seuraavassa taulukossa kuvataan palvelun tyypillisiä skenaarioita ja toimia. siinä ilmoitetaan myös, vastaako Microsoft, asiakas vai sekä Microsoft että asiakas toimista.

| Tehtävä | Microsoftin vastuulla | Asiakkaan vastuulla |
|---|---|---|
| **Alustavien vuokraajien valmistelu** | | |
| Ennustetun kuormituksen mitoitus LCS:ssä tilauksen arviointityökalun avulla ja tiettyjen ympäristöjen valmistelun pyytäminen. | | X |
| Kaikkien tuotantoesiintymien ja muiden kuin tuotantoympäristöjen valmistelu. | X | |
| Käyttöönotettujen tuotantoesiintymien ja muiden kuin tuotantoesiintymien vahvistaminen. | | X |
| **Palvelupäivitykset** | |
| Käytä palvelupäivityksiä tietyissä muissa kuin tuotantoesiintymissä ja tuotantoesiintymissä. | X | |
| Käytä palvelupäivityksiä manuaalisesti LCS:stä eristysesiintymiin. Määritä, kehitä ja testaa päivitys sekä toimita koodin päivityspaketti takaisin LCS:hen. | | X |
| Pyydä ja ajoita tuotantoesiintymään käytettävät laajennuspäivitykset. | | X |
| Koodi- ja tietovarmuuskopion luominen tuotantoesiintymälle, ennen kuin päivityksiä otetaan käyttöön. | X | |
| Tuotantoesiintymän palautus koodi- ja tietovarmuuskopioon, jos tapahtuu virheitä. | X | |
| **Tiedonhallinta (varmuuskopiointi, palautus ja päivitys)** | | |
| Tietokannan varmuuskopiointi. | X | |
| Korkean käytettävyyden ja järjestelmäpalautuksen suunnitelman määritys. | X | |
| Tuotantoesiintymän tietokannan suorituskyvyn seuranta. | X | |
| Tuotantoesiintymän tietokannan hienosäätö suorituskykyä varten. | X | |
| Suorita tuotantoesiintymän tietokannan tietyn ajankohdan päivitys muussa kuin tuotantoesiintymässä. | | X |
| **Infrastruktuurin päivittäminen** | | |
| Säännöllisten infrastruktuuripäivitysten ajoittaminen. | X | |
| **Skaalaus molempiin suuntiin (käyttäjät, tallennustila ja esiintymät)** | | |
| Lisäkäyttäjien ja muiden kuin tuotannon lisäosien ostaminen. | | X |
| Käyttömuutosten päivitys LCS:n tilauksen arviointityökaluun. | | X |
| Palvelun käyttöön vaikuttavien merkittävien suorituskykyongelmien ilmoittaminen. | | X |
| Käytettävään palveluun tarvittavien resurssien ennakoiva hallinta. | X | |
| Tapahtumien tutkiminen ja vianmääritys. | X | |
| **Suojaus (käyttöoikeudet)** | | |
| Palvelun käyttöoikeuksien myöntäminen käyttäjille. | | X |
| LCS-projektikäyttöoikeuksien myöntäminen LCS:n kautta käyttöönotettujen esiintymien hallintaa ja käyttöä varten. | | X |
| **Tuotantoesiintymien seuranta** | | |
| Tuotantoesiintymien ympärivuorokautinen seuranta. | X | |
| Ennakoiva tuotantoesiintymään liittyvien tapahtumien ilmoittaminen asiakkaalle. | X | |
| **Muiden kuin tuotantoesiintymien hallinta ja seuranta** | | |
| Muiden kuin tuotantoesiintymien hallinta LCS:n avulla. | | X |
| Muiden kuin tuotantoesiintymien seuranta. | | X |

## <a name="service-update-strategy"></a>Palvelun päivitysstrategia

Sovellukset noudattavat [ohjelmistojen elinkaarikäytännön](../../dev-itpro/migration-upgrade/versions-update-policy.md), Finance and Operations mukaisesti Microsoftin [modernia elinkaarikäytäntöä](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), joka kattaa jatkuvasti huolletut ja tuetut tuotteet. 

Microsoft julkaisee vuosittain kahdeksan Finance and Operations -sovellusten päivitystä seuraavina kuukausina:

- Tammikuu
- Helmikuu
- Huhtikuu
- Touko
- Heinäkuu
- Elokuu
- Lokakuu
- Marraskuu

>[!NOTE]
>Huhtikuussa ja lokakuussa kyseessä on merkittävä ominaisuuksien julkaisuaalto. Asiakkaat voivat keskeyttää yksittäisen palvelun päivitykset enintään kolmen peräkkäisen päivitysjakson ajaksi.

Lisätietoja on seuraavissa aiheissa:

- [One Version -palvelupäivitykset – yleiskatsaus](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [LCS:n kautta tapahtuvien palvelupäivityksien määritys](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [LCS:n kautta tapahtuvien palvelupäivitysten keskeyttäminen](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Vastaanota ilmoituksia LCS:n kautta tapahtuvista palvelupäivityksistä](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regressiontestaustyökalut palvelupäivitysten vahvistamiseen](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365:n toteutussuunnitelma ja julkaisuaallot](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Suojaus- ja järjestelmänvalvojan käyttöoikeudet

Järjestelmänvalvojan käyttöoikeuksia Finance and Operationsin tuotantoympäristöön valvotaan ja kirjataan lokiin tarkasti. Asiakastietoja käsitellään [Microsoftin online-palvelujen ehtojen](https://www.microsoft.com/licensing/terms/productoffering) mukaisesti. 

### <a name="customer-administrative-access"></a>Asiakkaan järjestelmänvalvojan käyttöoikeudet

Asiakkaan vuokraajajärjestelmänvalvoja voi käyttää tuotantoesiintymiä ja muita kuin tuotantoesiintymiä seuraavassa taulukossa kuvatulla tavalla:

| Ympäristön tyyppi | Tarkoitus | Asiakkaan käyttöoikeustaso |
|---|---|---|
| **Muu kuin tuotanto**<br>Tason 1 eristys | Muu kuin tuotantoympäristö, jonka asiakkaat ottavat käyttöön kehitystä, esittelyä tai koulutusta varten. | Tason 1 eristys (jota kutsutaan myös pilvipalveluympäristöksi) on asiakkaan hallitsema VM, joka otetaan käyttöön asiakkaan Azure-tilauksessa LCS:n kautta. Koska kyseessä on VM asiakkaan Azure-tilauksessa, asiakkaalla on täydet järjestelmänvalvojan käyttöoikeudet ympäristöön etätyöpöydän kautta. |
| **Muu kuin tuotanto**<br>Tier 2 (tai sitä suurempi) eristys | Muu kuin tuotantoympäristö, jonka asiakkaat ottavat käyttöön käyttäjähyväksyntätestausta, integraatiotestausta, koulutusta, valmistelua tai mitä tahansa muuta tuotantoa edeltävää skenaariota varten. | Tason 2 ja sitä korkeampien tasojen eristysympäristöt otetaan käyttöön Finance and Operationsin SaaS-tilauksessa. Käyttöoikeudet Azuren SQL-tietokantoihin, jotka on yhdistetty muuhun kuin tuotantoympäristöön, myönnetään [just-in-time-käyttöoikeuksien muodossa](../../dev-itpro/database/database-just-in-time-jit-access.md). Etätyöpöydän käyttö ei ole mahdollista. |
| **Tuotantoympäristö** | Tuotantoympäristö otetaan käyttöön, kun projekti on [valmis alustavaan lopulliseen käyttöönottoon](/imp-lifecycle/environment-planning.md#production-system-readiness). | Tuotantoympäristöjä otetaan käyttöön SaaS-tilauksessa. Niitä käytetään yksinomaan selaimen, palvelun päätepisteiden tai LCS:n kautta. |

### <a name="microsoft-administrative-access"></a>Microsoftin järjestelmänvalvojan käyttöoikeudet

Seuraavassa taulukossa esitetään Microsoftin eri järjestelmänvalvojien eri käyttöoikeustasot:

| Järjestelmänvalvoja | Asiakastiedot |
|---|---|
| Työvaiheiden vastausryhmä<br>(Rajoitettu vain avainhenkilöstöön) | Käyttöoikeus myönnetään tukipalvelupyynnön kautta. Käyttöä valvotaan ja se rajoittuu tukitoimen kestoon. |
| Microsoftin asiakastuki (CSS) | Ei suoria käyttöoikeuksia. Asiakas voi käyttää näytön jakamista tehdäkseen yhteistyötä tukihenkilöstön kanssa virheenkorjauksessa. |
| Suunnittelu | Ei suoria käyttöoikeuksia. Työvaiheiden vastausryhmä voi käyttää näytön jakamista tehdäkseen yhteistyötä suunnittelun kanssa virheenkorjauksessa. |
| Muut Microsoftissa | Ei käyttöoikeuksia. |

## <a name="monitoring"></a>Valvonta

Microsoft on investoinut laajaan työkalusarjaan asiakkaiden tuotantoesiintymien seurantaa ja diagnosointia varten. Microsoft seuraa asiakkaiden tuotantoympäristöjä 24 tuntia päivässä ja 7 päivää viikossa. Lisätietoja [Tuotannon tuki ja seuranta](../imp-lifecycle/production-support-monitoring.md).

| Microsoftin vastuut | Asiakkaan vastuut |
|---|---|
| <ul><li>Palvelun käytettävyyden seuranta.</li><li>Kriittisten komponenttien (kuten Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce ja Management Reporter) jatkuva seuranta ja hälytysten antaminen kuntomittareiden ja vahtiajastinten perusteella.</li><li>Infrastruktuuripalvelujen (kuten Azure Active Directory \[Azure AD\] ja Azure SQL) aiheuttaman suorituskyvyn heikkenemisen seuranta.</li><li>Jos Microsoft määrittää, että yksittäinen prosessi tai erätyö aiheuttaa poikkeamia, kyseinen prosessi tai työ lopetetaan asiakkaan kanssa käydyn viestinnän jälkeen.</li></ul> | <ul><li>Sellaisten sovellusten määritysten ja laajennusten muutosten seuranta, jotka voivat aiheuttaa toiminta- ja suorituskykyongelmia.</li><li>Sovellusvirheet on diagnosoitava seurantatyökaluilla. Näiden työkalujen käyttö käyttäjien ilmoittamien suorituskykypoikkeamien diagnosointiin.</li><li>Microsoftille ilmoittaminen, jos järjestelmän odotettu kuormitus ylittää ennustetun huippukäytön.</li><li>Jos kulloinenkin palvelu ei ole käytettävissä tuotantoesiintymässä, asiakas voi käyttää LCS:ää [tuotantokatkoksesta](../../dev-itpro/lifecycle-services/report-production-outage.md) ilmoittamiseen.</li></ul> |

Lähettämällä tukipyyntöjä verkossa LCS:n kautta asiakkaat mahdollistavat Microsoftille nopean ja syvän teknisen asiantuntemuksen toimittamisen mahdollisimman tehokkaasti ja vaikuttavasti. Vaikka puhelinvaihtoehto on käytettävissä, sitä pitäisi käyttää vain, jos verkkovaihtoehto ei ole käytettävissä. Lisätietoja: [Puhelintukivaihtoehdot](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Tapaushallinta

Microsoft vastaa tapauksiin ja korjaa niitä vakavuustasojen perustella. Microsoftin tapausten vakavuustasot voivat vaihtua tapauksen alustavan arvioinnin yhteydessä ja kun lisää tietoja sen vaikutuksista ja laajuudesta tulee saataville. Jos tapaus korjataan, tapauksen vakavuus pysyy muuttumattomana.

Lisätietoja vakavuustasoista esitetään [tässä vakavuustaulukossa](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Liiketoiminnan jatkuvuus korean käytettävyyden ja järjestelmäpalautuksen kautta 

Microsoft tarjoaa liiketoiminnan jatkuvuutta ja järjestelmäpalautusta Finance and Operations -sovellusten tuotantoesiintymille, Azuren alueellisten käyttökatkojen tapauksissa. Lisätietoja [Liiketoiminnan jatkuvuus ja järjestelmäpalautus](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Korkea käytettävyys** – Korkean käytettävyyden toiminto tarjoaa tapoja sellaisten käyttökatkojen vähentämiseksi, jotka aiheutuvat yksittäisestä solmusta Azure-palvelinkeskuksessa. Kunkin palvelun pilviarkkitehtuuri käyttää Azuren käytettävyyssarjoja käsittelytasolla estääkseen yksittäisten vikakohtien tapaukset. Tietokantojen korkea käyttävyys tarjotaan [Azure SQL:n korkean käytettävyyden ominaisuuksilla](/azure/azure-sql/database/high-availability-sla).
- **Järjestelmäpalautus** – [Azuren järjestelmäpalautusominaisuudet](/azure/best-practices-availability-paired-regions) suojaavat jokaista palvelua käyttökatkoilta, jotka vaikuttavat laajasti kokonaiseen Azure-palvelinkeskukseen. Tässä on esimerkkejä näistä ominaisuuksista:

    - Azure SQL:n aktiivinen maantieteellinen replikointi päätietokannasta (yritystietokannasta).
    - Maantieteellisesti päällekkäiset kopiot Azuren blob-tallennustilasta (joka sisältää asiakirjaliitteitä) muilla Azure-alueilla.
    - Toissijainen alue Azure SQL:n ja Azuren blob-tallennustilan replikoinneille.

Ensisijaisten tietosäiliön replikointia tuetaan. Siksi kunkin palvelun komponentit, kuten Management Reporter ja yksikkösäilö, käyttävät ensisijaisesta tietokannasta muunnettuja tietoja. Nämä tiedot on luotava sen jälkeen, kun palautussivusto on määritetty ja palvelu on käynnistetty. Asiakkaan koodiartefakteja ja palautettuja tietosäiliöitä käytetään sijainnin uuteen käyttöönottoon. Uusi käyttöönotto mahdollistaa käsittelysolmujen sekä verkkopalvelujen ja muiden komponenttien tilan replikoinnin, jotta palautettuja tietosäilöjä voidaan käyttää toissijaisen sijainnin määrittämiseen. Jos järjestelmäpalautusta käytetään asiakkaan tuotantoesiintymän palauttamiseen, Microsoft ja asiakas täyttävät [tapauksenhallinnan](service-description.md#incident-management) velvollisuutensa.

Microsoftin järjestelmäpalautuksen suunnitelmia ja menettelyjä tutkitaan jatkuvasti järjestelmä- ja organisaatio-ohjauksen (SOC) auditoinneilla. Nämä vaatimustenmukaisuuden auditoinnit vahvistavat Microsoftin järjestelmänpalautuksen teknistä ja menettelyllistä prosessia, johon kuuluvat Dynamics 365 Finance and Operations -sovellukset. [SOC-vaatimustenmukaisuuden](/compliance/regulatory/offering-soc-2) auditointiraportit ja muut vaatimustenmukaisuusraportit ovat saatavilla [Microsoft Trust Centerin vaatimustenmukaisuustarjonnassa](/compliance/regulatory/offering-home).

| Microsoftin vastuut | Asiakkaan vastuut |
|---|---|
| Microsoft valmistelee Azuren yhdistettyyn palvelinkeskukseen toissijaisen ympäristön, kun ensisijainen tuotantoesiintymä otetaan käyttöön. Lisätietoja: [Liiketoiminnan jatkuvuus ja järjestelmäpalautus: Azuren yhdistetyt alueet](/azure/best-practices-availability-paired-regions). | None |
| Microsoft ottaa Azure SQL:n ja Azure blob-tallennustilan maantieteellisen päällekkäisyyden käyttöön, kun ensisijainen tuotantoesiintymä otetaan käyttöön. | None |
| Microsoft ottaa automaattisen varmuuskopioinnin käyttöön Azuren SQL-tietokannoissa. | None |
| <p>Käyttökatkoksen yhteydessä Microsoft märittää, onko asiakkaalle luotava vikasietoalue ja menetetäänkö tietoja. Asiakkaat voivat kokea tietojen menetystä jopa 15 minuuttia riippuen katkon luonteesta ja ajasta. | Tietojen häviämisen tapauksessa asiakkaan voi olla tarpeen antaa kirjallinen suostumus vikasietoalueen käynnistämistä varten. |
| Kun vikasietoalue otetaan käyttöön, kulloinenkin palvelu toimii rajoitetussa tilassa. Päivitysylläpitoa ei voi käynnistää vikasietotilassa. | Asiakas ei voi pyytää pakettien käyttöönottoa tai esittää muita tavanomaisia ylläpitopyyntöjä vikasietotilassa. |
| Kun palvelinkeskus tulee käyttöön, Microsoft palaa ensisijaisen Azure-alueen tuotantoesiintymään. Normaalit työvaiheet jatkuvat. | Asiakkaan voi olla tarpeen antaa suostumus tuotantoesiintymään palaamiseen ensisijaisella Azure-alueella. |

## <a name="finance-and-operations-support-offerings"></a>Finance and Operationsin tukitarjonta

Tekninen tuki on saatavilla markkina-alueilla, joilla tarjotaan Finance and Operations -palveluja. [Tukikokemukset](../../dev-itpro/lifecycle-services/lcs-support.md) tarjotaan LCS:ssä tai Finance and Operations -sovelluksissa. Seuraavassa on muutamia esimerkkejä:

- [Ongelmahaku](../../dev-itpro/lifecycle-services/issue-search-lcs.md) LCS:ssä
- [Integroitu tekninen tuki](../../dev-itpro/lifecycle-services/support-experience.md) Finance and Operations -sovelluksissa
- [Tuen pilvipalvelu](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) LCS:ssä

Microsoft tarjoaa Finance and Operationsin asiakkaille kolme tukisopimusta: Premier, suora ammattilaistuki ja tilaukseen sisältyvä tuki. Tuen taso vaihtelee sopimuksen mukaan. Seuraavassa taulukossa esitetään kolmen sopimuksen vertailu.

| Tukitoiminto | Premier | Suora Professional-tuki | Tilaus |
|---|---|---|---|
| Rajoittamaton häiriö-/korjaustapausten lähetys | Kyllä | Kyllä | Kyllä |
| Ympärivuorokautinen käyttö LCS:n kautta | Kyllä | Kyllä | Kyllä |
| Tapahtuman vastausaika | Alle yksi tunti | Alle yksi tunti | Seuraava arkipäiviä |
| Neuvonta-ajat | Poolit hankitaan sopimuksen mukaan. | Ei | Ei |
| Erillinen tukitilivastaava | Kyllä | Ei | Ei |
| Erillinen tukiasiantuntija | Saatavilla erillisestä sopimuksesta | Ei | Ei |

Lisätietoja on kohdassa [Tuen yleiskatsaus](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Yhteydenotto tukeen

Tapauksissa, jotka liittyvät Finance and Operations -sovelluksiin, asiakkaat lähettävät Microsoftille tukipalvelupyyntöjä LCS:n kautta. CSS käsittelee tapaukset asiakkaan tukisopimuksen ja CSS:n määrittämän tapauksen vakavuuden perusteella.

### <a name="service-level-agreement"></a>Palvelutasosopimus

Microsoft on sitoutunut palvelun 99,9-prosenttiseen kuukausittaiseen käytettävyyteen. Jos Microsoft ei saavuta ja säilytä kulloisenkin palvelun palvelutasosopimuksessa (SLA) kuvattua palvelutasoa, asiakkaalla voi olla oikeus hyvitykseen kyseisen palvelun kuukausimaksujen alennusten muodossa. Lisätietoja palveluhyvityksen hakemisesta on [SLA:n](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services) Vaateet-osiossa.

## <a name="important-resources"></a>Tärkeät resurssit

- **[Trust Center](https://www.microsoft.com/trust-center)** – Hanki tietoja siitä, mihin Finance and Operations -tietosi on tallennettu sekä lisätietoja yksityisyyden, vaatimustenmukaisuuden ja suojauksen menettelyistä.
- **[Käyttöoikeusehdot ja -dokumentaatio](https://www.microsoftvolumelicensing.com/)** – Hanki nopea pääsy käyttöoikeuksien ehtoihin, edellytyksiin ja täydentäviin tietoihin, jotka ovat merkityksellisiä Microsoftin volyymikäyttöoikeusohjelmien kautta lisensoitujen tuotteiden ja palvelujen käytön kannalta.
- **[Käyttöoikeusehdot](https://www.microsoft.com/licensing/product-licensing/)** – Tämän sivun resurssit määrittävät niiden ohjelmisto- ja verkkopalvelutuotteiden ehdot ja edellytykset, jotka ostat Microsoftin kaupallisten lisensointiohjelmien kautta.
- **[Microsoftin elinkaarikäytäntö](/lifecycle/)** – Tämä sivu tarjoaa yhdenmukaisia ja ennustettavissa olevia ohjeita tuen käytettävyydestä koko tuotteen elinkaaren ajalta.
- **[Käyttöoikeusopas](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – Tämän oppaan avulla voit oppia lisää Dynamics 365:n lisensoinnista.
- **[Asiakastuki](https://dynamics.microsoft.com/support/)** – Hanki alan johtava tuki Dynamics 365 -sovelluksillesi.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – Hallitse sovelluksen elinkaarta ja siirry koti ennustettavissa olevia, toistettavia ja korkealuokkaisia käyttöönottoja.
- **[Dynamics 365 -käyttöönotto-opas](https://aka.ms/D365ImplementationGuideFlip)** - Dynamics 365 -käyttöönotto-opas dokumentoi aikatestatut Success by Design -periaatteet ja antaa ohjeita Dynamics 365 -ratkaisujen suunnitteluun, kehittämiseen, testaamiseen ja käyttöönottoon.

## <a name="definitions"></a>Määritelmät

### <a name="azure-region"></a>[Azure-alue](/azure/availability-zones/az-overview#regions)

Maantieteellinen alue, jolla on yksi tai useampi Azure-palvelinkeskus. Esimerkkejä ovat Yhdysvallat ja Eurooppa.

### <a name="business-process-modeler-bpm"></a>[Liiketoimintaprosessien mallintaja](../../dev-itpro/lifecycle-services/bpm-overview.md)

LCS:ssä oleva työkalu, joka auttaa jonkin käyttöönoton sovitus- ja aukkoanalyysin tekemisessä käyttämällä American Productivity & Quality Centerin (APQC) liiketoimintaprosessien määritelmiä, joita tuetaan Finance and Operations -sovelluksissa.

### <a name="cloud-solution-provider"></a>Pilviratkaisun tarjoaja

Microsoftin pilvipalveluratkaisujen toimittajien (CSP) ohjelmaan kuuluva kumppani, joka tarjoaa asiakkaille arvoa lisääviä pilvipalveluja, tukea, yhden laskun ja skaalautuvaa asiakashallintaa.

### <a name="customer"></a>Asiakas

Liiketoimintayksikkö, joka käyttää Finance and Operations -sovelluksia ja jota Office 365:ssa edustaa vuokraaja.

### <a name="development-environment"></a>Kehitysympäristö

Muun kuin tuotannon eristysympäristö, jota käytetään laajennusten kehittämiseen. Asiakkaat ottavat tämän ympäristön käyttöön omassa Azure-tilauksessaan LCS:stä. Tätä ympäristöä voi käyttää myös esittely-, koulutus- ja muihin testaustehtäviin. Se tunnetaan myös [tason 1 eristyksenä](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Käyttökatko

Mikä tahansa jakso, jonka aikana käyttäjät eivät voi kirjautua tai käyttää aktiivista vuokraajaansa voimassa olevassa ympäristössä tai palveluinfrastruktuurissa olevan häiriön vuoksi, jos Microsoft toteaa tämän automaattisen kunnonvalvonnan ja järjestelmälokien perusteella. Käyttökatkoihin eivät kuulu ajoitetut käyttökatkot, palvelujen lisäosaominaisuuksien pois käytöstä oleminen, palvelun käytön estyminen omien palveluun tehtyjen muutosten vuoksi eivätkä jaksot, joiden aikana scale unit -kapasiteetti on ylitetty.

### <a name="implementation-partner"></a>Käyttöönottokumppani

Kumppani, jonka asiakas valitsee Finance and Operations -ratkaisujensa mukauttamista, määrittämistä, käyttöönottoa ja hallintaa varten.

### <a name="incident"></a>Tapaus

Ongelma, jonka asiakkaat kohtaavat Finance and Operations -palvelun käytön aikana ja josta he lähettävät palvelupyynnön LCS:n kautta.

### <a name="microsoft-customer-support-services-css"></a>Microsoftin asiakastuki (CSS)

Microsoftin maailmanlaajuinen tukiryhmä, joka on sitoutunut tarjoamaan korkealaatuista palveluja Finance and Operations -sovelluksia varten.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Finance and Operations -sovellusten koekäytöstä käyttöönottoon, tuotannonjälkeiseen hallintaan ja tukeen ulottuvan elinkaarihallinnan hallintaportaali. Lisätietoja: [Lifecycle Services -resurssit](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Muu kuin tuotantoesiintymä

Mikä tahansa seuraavista palveluesiintymistä, jota asiakas käyttää laajennusten vahvistamiseen ja muiden kehitystehtävien suorittamiseen:

- **Eristystaso 1** – Kehittäjäesiintymä (asiakkaan isännöimä)
- **Eristystaso 2** – Vakiomuotoinen hyväksymistestausesiintymä
- **Eristystasot 3–5** – Lisäosien eristykset

Lisätietoja tasoista 2–5: [Oikean tason 2 tai sitä korkeamman tason ympäristön valinta](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Tuotantoesiintymä

Finance and Operations -ympäristö, jota asiakas käyttää "suorien" päivittäisten tapahtumiensa ja liiketoimintaprosessiensa hallintaan.

### <a name="sandbox-environment"></a>Eristysympäristö

Muu kuin tuotantoympäristö, jota asiakas käyttää esittelyihin, koulutuksen, käyttäjien hyväksyntätestaukseen, laajennusten vahvistamiseen ja muihin testaustehtäviin.

### <a name="service"></a>Huolto

Mikä tahansa Finance and Operations -sovelluksiin sisältyvä ydinprosessi.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Microsoftin verkkopalveluita koskeva palvelutasosopimus (SLA)

Microsoftin verkkopalveluihin sovellettava palvelutasosopimus. Lisätietoja: [Palvelutasosopimukset](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Palvelupäivitys

Microsoft huoltaa Finance and Operations -ympäristöjä jatkuvasti palvelupäivitysten kautta. Asiakkaat määrittävät oman palvelupäivityskalenterinsa liiketoiminnan tarpeiden mukaan. Lisätietoja: [Yhden version palvelupäivitykset](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Kehys, joka ohjaa toteutusta järjestelmällisesti arvioinneilla kriittisissä vaiheissa, jotta voidaan varmistaa Dynamics 365 -ratkaisun optimaalinen arkkitehtuuri, suojaus, suorituskyky ja käyttäjäkokemus.

### <a name="user"></a>Käyttäjä

Yksittäinen henkilö, joka käyttää Finance and Operations -ympäristöjä ja joka liittyy asiakkaan vuokraajaan.
