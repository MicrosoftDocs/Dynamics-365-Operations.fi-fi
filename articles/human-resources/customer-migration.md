---
title: Human Resourcesin asiakkaiden siirtoa koskevat usein kysytyt kysymykset
description: Tässä artikkelissa vastataan usein kysyttyihin kysymyksiin Microsoft Dynamics 365 Human Resourcesin siirrosta talous- ja toimintosovelluksiin yhdistetystä infrastruktuurista.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151079"
---
# <a name="human-resources-customer-migration"></a>Human Resourcesin asiakkaiden siirto

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Miten Dynamics 365 Human Resources -asiakkaiden pitäisi suunnitella siirtyminen talous- ja toimintosovellusinfrastruktuuriin?

Tämä koskee kahta Microsoft Dynamics 365 Human Resources -asiakasluokkaa, joiden on tehtävä muutoksia ja varmistettava tällä tavoin, että heillä on talous- ja hallintosovelluksen viimeisin infrastruktuuri:

- Dynamics 365 Human Resourcesia käyttävät asiakkaat, joilla ei ole muista Dynamics 365:n toimintosovelluksia
- Asiakkaat, jotka käyttävät sekä Dynamics 365 Human Resourcesia että Dynamics 365 Financea, Dynamics 365 Supply Chain Managementia, Dynamics 365 Commercea tai Dynamics 365 Project Operationsia

Kyseisten asiakkaiden on luokasta riippumatta siirrettävä tiedot uuteen talous- ja hallintasovellusinfrastruktuurin ympäristöön sekä tarkistettava, että yhdistyminen on onnistunut.

Jatkossa Dynamics 365 Human Resources -sovelluksessa on oma talous- ja toimistosovellusympäristö, joka on erillään muista toimintosovelluksista. Tällä tavoin asiakkaat voivat hyödyntää laajennettavuusvaihtoehtoja ilman, että nykyiset tiedot olisi yhdistettävä. Microsoft toimittaa työkalut ja eristysympäristön, jossa asiakkaat voivat testata tietojen siirtoa ja varmistaa sen ennen tuotantoympäristöön siirtymistä. Työkalut mahdollistavat lähes automaattisen prosessin, ja ne ovat käytettävissä elokuun ja marraskuun välisenä aikana vuonna 2022.

Muita sovelluksia talous- ja toimintosovellusinfrastruktuurissa käyttävillä asiakkailla on mahdollisuus yhdistää Human Resources -tiedot aiemmin luotuun ympäristöön. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Milloin asiakkaat siirretään talous- ja toimintosovellusinfrastruktuuriin?

Kunkin yrityksen siirtymä määräytyy yrityksen nykyisistä määrityksistä ja valmiudesta siirtyä talous- ja toimintosovellusinfrastruktuuriin. Asiakkaita suositellaan määrittämään yhdessä Microsoft-kumppanin kanssa paras tapa edetä.

- **Human Resources** -moduulia Dynamics 365 Financessa käyttävien organisaatioiden on otettava Dynamics 365 Human Resourcesin uudet ominaisuudet käyttöön tavanomaisen One Version -päivitysprosessin osana. Uusien ominaisuuksien on tarkoitus olla yleisesti saatavana tammikuusta 2022 alkaen.
- Dynamics 365 Human Resourcesia käyttävillä organisaatioilla on mahdollisuus käyttää työkaluja, joiden avulla infrastruktuurin yhdistäminen voidaan viimeistellä. Microsoft tekee yhteistyötä asiakkaiden kanssa siirtymän aikana, jotta palvelukatkoksilta vältyttäisiin. Asiakkailla 12–18 kuukautta aikaa siirtymiseen. Tämä aika alkaa siitä, kun siirtymistyökalut tulevat saataville.
- Sekä Dynamics 365 Human Resourcesia että **Human Resources** -moduulia käyttävät asiakkaat voivat siirtää erillisen Human Resources -infrastruktuurin talous- ja toimintosovellusinfrastruktuuriin. Toinen vaihtoehto on siirtää ympäristöt samaan ympäristöön yhdistämistyökalujen avulla. Kahden ympäristön yhdistämiselle ei ole mitään tarvetta eikä aikarajaa.

Ajantasaiset tiedot kannattaa tarkistaa säännöllisesti [julkaisusuunnitelmista](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Tarvitsevatko asiakkaat mukautettuja Dynamics 365 Human Resourcesin ja Human Resources -moduulin integrointeja?

- Asiakkaat, joilla on sekä Dynamics 365 Human Resources- että muita talous- ja toimintosovellusinfrastruktuurin ympäristöjen integrointeja, on jatkettava kahden ympäristön integrointia myös yhdistämisen jälkeen.
- Asiakkaiden, jotka päättävät pitää Dynamics 365 Human Resources -ympäristön erillään aiemmin luodusta talous- ja toimintosovellusympäristöstä, on jatkettava ympäristöjen integrointia, jotta tiedot ovat käytettävissä molemmissa ympäristöissä.
- Asiakkaat voivat jatkaa tietojen integrointitoiminnon käyttöä tietojen kopioimiseen kahden ympäristön välillä. Asiakkaiden, jotka yhdistävät tiedot yhteen ympäristöön, ei tarvitse integroida tietoja siirron jälkeen, sillä kaikki ovat yksittäistietokannassa.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Siirretäänkö asiakkaan ISV-ratkaisut automaattisesti?

Kunkin riippumattoman ohjelmistotoimittajan (ISV) ratkaisun siirtokokemus vaihtelee ratkaisun integrointimenetelmän mukaan. Microsoft tekee tiivistä yhteistyötä ISV-toimittajien kanssa ja auttaa näin toteuttamaan sujuvan siirtymisen talous- ja toimintosovellusinfrastruktuuriin. Monet ISV-ratkaisut perustuvat Dataverseen, sillä niissä käytetään Microsoft Power Platformin ominaisuuksia. Nämä ratkaisut ovat riippuvaisia Dataverse-integroinnista Dynamics 365 Human Resources- ja Dataverse-ympäristöjen välillä. Dataverse-integrointi vanhentuu infrastruktuurin yhdistämisen osana. Talous- ja toimintosovellusinfrastruktuurissa uusien kaksoiskirjoitusmääritysten on tarkoitus korvata Dataverse-integroinnin toiminnot.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Mikä on vaikutus tietoja Dynamics 365 Human Resourcesin ja muiden Dynamics 365 -sovellusten välillä siirtämään tietojen integrointitoimintoon?

Kun asiakkaat siirtyvät talous- ja toimintosovellusinfrastruktuuriin, heidän on jatkettava tietojen integrointia kahden ympäristön välillä. Asiakkaat voivat jatkaa näiden tietojen integrointitehtävien suorittamiseen tietojen integrointitoiminnon avulla. Asiakkaiden, joiden tarkoitus on pitää Dynamics 365 Human Resources -ympäristön erillään aiemmin luodusta talous- ja toimintosovellusympäristöstä, on jatkettava tietojen integrointia kahden ympäristön välillä. Jos asiakkaat yhdistävät kaksi ympäristöä yhdeksi ympäristöksi, tietojen integrointia kahden ympäristön välillä ei enää tarvita.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Miten tietoja siirretään talous- ja toimintosovellusinfrastruktuurissa olevan Dynamics 365 Human Resourcesin ja Dataversen välillä siirron jälkeen?

Nykyinen Dynamics 365 Human Resourcesin ja Dataversen välinen Dataverse-integrointi vanhentuu talous- ja toimintosovellusinfrastruktuurin osana. Kaksoiskirjoitusmäärityksiä on tarkoitus ottaa käyttöön yhdistämään talous- ja toimintosovellusentiteetit Dataverse-taulukoihin. Asiakkaiden on päätettävä, mitä kaksoiskirjoitusmäärityksiä tarvitaan toteutuksessa. Virtuaalitaulukoiden käyttö on suositeltavaa integroinneissa ja ISV-ratkaisuissa, ellei tietty liiketoimintarve edellytä tietojen monistamista Dataverseen liiketoimintalogiikan suorittamista varten.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Miten siirtyminen vaikuttaa Dynamics 365 Human Resourcesin Dataverse-laajennuksiin?

Asiakkaiden on siirryttävä eristysympäristöön ennen tuotantoympäristön siirtämistä. Kun asiakkaat siirtävät eristysympäristön, heidän on luotava Dataverse-ympäristöstä kopio, jolla muodostetaan yhteys uuteen, yhdistettyyn talous- ja toimintosovellusympäristöön. On suositeltavaa, että asiakas kopioi sekä ympäristön tiedot että sen ratkaisut, jotta ne vastaavat asiakkaan nykyistä tuotantoympäristöä.

Kun asiakkaat ovat valmiita siirtämään Dynamics 365 Human Resources -tuotantoympäristön, Microsoft siirtää tietokannan ja Azure Blob -säilön automaattisesti. Siirretty tietokanta ja tallennustila osoittavat talous- ja toimintosovellusinfrastruktuurin uuden ympäristöön saamaan Dataversen tuotantoympäristöön. Ennen kuin tietojen kopiointia Dataverseen voidaan jatkaa, asiakkaiden on otettava käyttöön kaksoiskirjoitusmääritykset, joita tarvitaan integroinneissa, laajennuksissa ja Dataverseen perustuvissa ISV-ratkaisuissa.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Toimivatko Dynamics 365 Human Resourcesia varten muodostetut Microsoft Power Platform -komponentit automaattisesti infrastruktuurin siirron valmistumisen jälkeen?

Power Appsissa luodut sovellukset, Power Automatessa luodut työnkulut ja muut Microsoft Power Platform -mukautukset ovat Dataverse-laajennusten kaltaisia. Asiakkaan tuotantoympäristöjen siirrolla ei ole mitään vaikutusta Dataverse-ympäristöön tai sen laajennuksiin. Sovellusten, työnkulkujen ja muiden Power Microsoft Platform -mukautusten pitäisi toimia jatkossakin ilman lisämäärityksiä.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Mitä Dynamics 365 Human Resourcesin Dataverse-virtuaalitaulukkoentiteeteille tapahtuu siirron aikana?

Kun asiakkaat siirtävät Dynamics 365 Human Resources -ympäristön talous- ja toimintosovellusinfrastruktuuriin, ympäristön yhteys tällä hetkellä Dynamics 365 Human Resourcesiin yhteydessä olevaan Dataverse-ympäristöön säilyy. Ympäristössä luodut Dataversen virtuaalitaulukot toimivat edelleen ilman lisämäärityksiä. Virtuaalitaulukot on ehkä luotava uudelleen siinä Dataverse-ympäristössä, joka on yhdistetty asiakkaan aiemmin luotuun talous- ja toimintosovellusympäristöön.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Miten hakijan seurantajärjestelmän (ATS) ohjelmointirajapintaa, palkanlaskennan ohjelmointirajapintaa, Dynamics 365 Human Resourcesin Dataverse-virtuaalitaulukoita tai muita Dataverse-verkko-ohjelmointirajapinnan entiteettejä käyttävä integraatio toimii infrastruktuurin yhdistämisen valmistumisen jälkeen?

Kun asiakkaat siirtävät Dynamics 365 Human Resources -ympäristön talous- ja toimintosovellusinfrastruktuuriin, ympäristön yhteys tällä hetkellä Dynamics 365 Human Resourcesiin yhteydessä olevaan Dataverse-ympäristöön säilyy. Dataverse-verkko-ohjelmointirajapintaa hyödyntämällä kehitetyt integroinnit toimivat edelleen siirron valmistumisen jälkeen.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Organisaatio on määrittänyt mukautetun suojauksen Dynamics 365 Human Resourcesssa. Toimiiko se edelleen infrastruktuurin siirron valmistuttua?

Kyllä. Mukautetut suojausmääritykset sisällytetään tietojen siirtoon.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Siirretäänkö Dynamics 365 Human Resourcesissa olevat työnkulut automaattisesti?

Kyllä. Työnkulun määritykset, työnkulkuhistoria ja nykyiset käynnissä olevat työnkulut siirretään yhdistettyyn infrastruktuuriin.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Siirretäänkö Dynamics 365 Human Resourcesissa tallennetut näkymät automaattisesti?

Kyllä. Tallennetut näkymät siirretään yhdistettyyn infrastruktuuriin.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Ovatko Dynamics 365 Human Resourcesissa käyttöönotetut ominaisuudet automaattisesti käytettävissä infrastruktuurin yhdistämisen jälkeen?

- Jos asiakkailla on **Human Resources** -moduuli, vain Dynamics 365 Human Resourcesissa käytettävissä olevia ominaisuuksia hallitaan ominaisuuksien hallinnassa. Näitä ominaisuuksia ei ole yleensä otettu oletusarvoisesti käyttöön. Kaikki ominaisuudet, jotka on otettava oletusarvoisesti käyttöön, dokumentoidaan.
- Dynamics 365 Human Resourcesia käyttävillä asiakkailla ominaisuudet ovat käytettävissä infrastruktuurissa. Kaikki ominaisuudet, jotka eivät ole käytettävissä, dokumentoidaan. Jokainen ominaisuuden hallinta-avain, joka on otettuna käyttöön nykyisessä Dynamics 365 Human Resources -ympäristössä, otetaan käyttöön yhdistetyssä infrastruktuurissa. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Mitä BYOD-tietokannoille tapahtuu siirron aikana?

Oman tietokannan (BYOD) tuonti- ja vientimääritykset siirretään uuteen talous- ja toimintosovellusinfrastruktuuriin.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Vaikuttaako asiakkaan ympäristön siirto Azure-alueeseen?

Dynamics 365 Human Resources -ympäristö pysyy samalla Azure-alueella siirtoa varten. Jos on ympäristö on siirrettävä toiselle Azure-alueelle, asiakkaiden on noudatettava uudelle alueelle siirtymisen vakio-ohjeita siirron valmistumisen jälkeen.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Mitä Azure Data Lake -tallennusitiloille tapahtuu siirron aikana?

Mikä tahansa talous- ja toimintosovelluksissa tällä hetkellä Azure Data Lakeen määritetty vienti säilyttää saman määrityksen siirron jälkeen.

> [!NOTE]
> Kaksoiskirjoitusmääritysten on oltava otettuna käyttöön, jotta tietoja voidaan kirjoittaa Human Resources -ympäristöstä Dataverseen.

Asiakkaat, jotka haluavat viedä Human Resources -tietoja Data Lake -tallennustilaan, voivat ottaa tämän ominaisuuden käyttöön sen jälkeen, kun siirto talous- ja toimintosovellusinfrastruktuuriin on valmis. Lisätietoja on kohdassa [Data Lake -tallennustilat – Azuren arkkitehtuurikeskus](/azure/architecture/data-guide/scenarios/data-lake).

Asiakkaat voivat linkittää useita talous- ja toimintosovellusympäristöjä samaan Data Lake -tallennustilaan. Kukin ympäristön kuitenkin osoittaa eri kansioon ja säilöön. Asiakkaiden kannattaa suunnitella toimintatapa huolellisesti, jos heidän tarkoituksenaan on yhdistää ympäristöt myöhemmin.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Minkälainen siirto on välttämätön, jos asiakas käyttää tällä hetkellä Human Resources -moduulia?

**Human Resources** -moduulia käyttävien asiakkaiden ympäristössä otetaan käyttöön uusia Dynamics 365 Human Resources -toimintoja tavanomaisen One Version -päivitysprosessin avulla. Asiakkaat voivat odottaa näkevänsä ympäristössä uusia toimintoja, kun ne tulevat saataville kussakin päivityksessä. Asiakkaat voivat ottaa ominaisuuksia käyttöön ominaisuuksien hallinnassa. Asiakkaiden kannattaa suunnitella näiden uusien ominaisuuksien tarkistus käyttämällä jo käytössä olevia prosesseja, joiden avulla he ovat tarkistaneet muut ympäristöön tulevat päivitykset.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Miten tapahtuu ulkoisten järjestelmien mukautetuille integroinneille?

Asiakkaiden on siirrettävä integroinnit talous- ja toimintosovellusympäristöön. Koska tämän ympäristön päätepiste on erilainen, asiakkaiden on ehkä päivitettävä tai muutettava integrointeja siten, että osoittavat uuteen ympäristöön. Tämä tehtävä on pääsääntöisesti manuaalinen prosessi, ja tehtävät muutokset määräytyvät integroinnin arkkitehtuurin mukaan. Asiakkaiden on määritettävä yhdessä Microsoft-kumppanin kanssa, mikä on järkevin tapaa siirtää integraatiot.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Mitä tapahtuu Microsoft Power Platform (Dataverse) -laajennuksille, jos asiakkaat yhdistävät Dynamics 365 Human Resources -ympäristön aiemmin luotuun talous- ja toimintosovellusympäristöön?

Jos asiakkaat päättävät yhdistää Dynamics 365 Human Resources -ympäristön ja aiemmin luodun talous- ja toimintosovellusympäristön yhdeksi Dataverse-esiintymäksi siirron jälkeen, Dataverse-ympäristöt on yhdistettävä osana yhdistämisprosessia. Tämä tehtävä edellyttää, että kaikki Power Appsin avulla luodut sovellukset ja muut mukautukset otettava uudelleen käyttöön uudessa ympäristössä.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Mitä asiakirjoille tapahtuu siirron aikana?

Kun asiakkaat siirtävät Dynamics 365 Human Resources -ympäristön talous- ja toimintosovellusinfrastruktuuriin, asiakirjat jäävät aiemmin luotuun asiakirjasäilöön ja ne yhdistetään automaattisesti uuteen ympäristöön talous- ja toimintosovellusinfrastruktuurissa.

Tuleviin versioihin sisältyy uusi tietoentiteettejä. Kun tämä muutos on tehty, asiakkaat, jotka valitsevat Dynamics 365 Human Resources -ympäristön yhdistämisen aiemmin luotuun talous- ja toimintosovellusympäristöön, voivat sitten viedä asiakirjoja ja siirtää ne aiemmin luotuun ympäristöön.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Mitä Dynamics 365 Human Resourcesissa määritetyille erätöille tapahtuu siirron jälkeen?

Erätyöt on määritettävä uudelleen talous- ja toimintosovellusympäristössä. Asiakkaiden on arvioitava kukin erätyö ja verrattava sitä talous- ja toimintosovellusympäristössä olevien erätöiden luetteloon. Asiakkaiden on myös analysoitava koko eräaikataulu, kun kaksi erätyöjoukkoa yhdistetään, sekä määritettävä, mitä muutoksia eräaikatauluun, prioriteetteihin tai eräryhmiin on tehtävä.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Miten siirto Dynamics 365 Human Resourcesin LCS-projekteihin?

Asiakkaiden on luotava uusi Microsoft Dynamics Lifecycle Service (LCS) -projekti ja heidän on valittava talous- ja toimintosovellukset tuotteeksi ja **Toteutus** projektityypiksi. Lisäksi LCS-projektia luotaessa on saatavana uusi aliprojektityypin kenttä. Asiakkaiden valittava Dynamics 365 Human Resources -siirtovaihtoehto aiemmin luodun Human Resources LCS -projektin siirtämiseen talous- ja toimintosovellusinfrastruktuuriin.

Talous- ja toimintosovellusten LCS-projektien ominaisuudet poikkeavat Human Resourcesin LCS-projektien ominaisuuksista.

Julkaisua varten uusien asiakkaiden on suoritettava seuraavat tehtävät:

- Projektiin käyttöönoton viimeisteleminen.
- Menetelmän viimeisteleminen.
- Tilauksen arviointityökalun täyttäminen.
- Julkaisuvalmiusprosessien viimeisteleminen.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Miten liiketoimintaprosessin mallintaja siirretään?

Asiakkaiden on vietävä liiketoimintaprosessin mallintajakirjasto Human Resources LCS -projektista ja tuoda se talous- ja toimintosovellusten LCS-projektiin. Lisäksi asiakkaiden on päivitettävä sovelluksen Ohje-asetukset siten, että he osoittavat uuteen LCS-projektiin.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Miten siirto vaikuttaa palvelun päivitysprosessiin?

Siirron jälkeen asiakkaiden sovelluksen elinkaaren hallinta (ALM) ja palvelupäivitykset ovat paljon joustavampia. Palvelupäivityksiä ei enää suoriteta automaattisesti Human Resources -ympäristöissä. Palvelu noudattaa sen sijaan One Version -palvelupäivitysprosesseja ja toimintoja, minkä lisäksi otetaan käyttöön LCS:n kautta käytettävät päivitysvaihtoehdot.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Onko asiakkaille oikeus FastTrack-tukeen infrastruktuurin yhdistämisen yhteydessä.

Microsoft määrittää edelleen, mitkä FastTrackin työkalut ja resurssit ovat käytettävissä yhdistämisen tukena.

## <a name="licensing-impact"></a>Vaikutus lisensseihin

Lisätietoja vaikutuksista käyttöoikeuksiin on kohdassa [Dynamics 365 Human Resourcesin infrastruktuurin yhdistämisen usein kysytyt kysymykset](hr-infrastructure-merge-faq.md#licensing-impact).
