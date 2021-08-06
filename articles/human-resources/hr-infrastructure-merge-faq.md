---
title: Dynamics 365 Human Resources -infrastruktuurin yhdistämisen usein kysytyt kysymykset
description: Tässä ohjeaiheessa vastataan usein kysyttyihin kysymyksiin Microsoftin Dynamics 365 Human Resourcesin ja Finance and Operationsin infrastruktuurin yhdistämisestä.
author: rachel-profitt
ms.date: 07/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fee4fea9b67ff8a0c8d813940a65cf882bd13abe
ms.sourcegitcommit: bf2daeccbe3f2826e734f409bfc823820144aa23
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/15/2021
ms.locfileid: "6617988"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources -infrastruktuurin yhdistämisen usein kysytyt kysymykset

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa vastataan usein kysyttyihin kysymyksiin Microsoftin Dynamics 365 Human Resourcesin ja Finance and Operationsin infrastruktuurin yhdistämisestä.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Mikä on Dynamics 365 Human Resources -infrastruktuurin yhdistäminen?

Dynamics 365 Human Resources on itsenäinen sovellus, joka käyttää eri infrastruktuuria kuin Finance and Operations -sovellukset, kuten Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Project Operations. Infrastruktuurin yhdistäminen tuo Dynamics 365 Human Resourcesin samaan infrastruktuuriin muiden Finance and Operations -sovellusten kanssa.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktuurin yhdistämisen arvo ja hyödyt

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia henkilöstöhallintonsa toimintoihin. Mitä hyötyä näistä muutoksista on?

- Nämä muutokset poistavat useita henkilöstöhallinnon ominaisuuksia Dynamics 365:ssä.
- Ne tarjoavat sekä Microsoft Power Platform -laajennettavuutta että tavan laajentaa liiketoimintalogiikkaa ja ominaisuusvaihtoehtoja.
- Ne yhdenmukaistavat sovellusten elinkaaren hallintaa Dynamics 365 Human Resourcesin ja muiden Finance and Operations -sovellusten välillä sekä Microsoft Dynamics Lifecycle Servicesin (LCS) suhteen, maantieteellistä saatavuutta ja paljon muuta.
- Niiden avulla voit hyödyntää jaettuja palveluita ja työkaluja ja auttaa vähentämään kustannuksia.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia Dynamics 365 Financessa, Supply Chain Managementissa, Commercessa tai Project Operationsissa. Mitä hyötyä näistä muutoksista on?

Dynamics 365 Human Resourcesin ominaisuudet ja investoinnit ovat nyt niiden asiakkaiden käytettävissä, jotka käyttävät -järjestelmän henkilöstöhallintomoduulia Dynamics 365 Financessa. Joitakin näistä ominaisuuksista ovat loman- ja poissaolojen hallinta, etujen hallinta ja tehtävien hallinta.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Menetänkö tällä hetkellä käytössä olevat ominaisuudet?

Dynamics 365 Human Resourcesin ja Finance and Operations -sovellusten henkilöstöhallinnon moduulin välillä on toiminnallisia samankaltaisuuksia. Dynamics 365 Human Resources on etusijalla samankaltaisissa ominaisuuksissa. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Muuttuuko käyttökokemus käyttäjilleni?

Uusia HR-ominaisuuksia hallitaan ominaisuuksien hallinnan avulla. Asiakkaat päättävät, haluavatko he ottaa ne vastaan. Joissakin tapauksissa ominaisuuksia saatetaan muokata. Näissä tapauksissa toimitetaan dokumentaatio.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Miten tämä muutos vaikuttaa minuun, jos olen olemassa oleva asiakas ja käytän sekä henkilöstöhallintomoduulia Finance and Operations -infrastruktuurissa että Dynamics 365 Human Resourcesia mukautettujen integraatioiden kautta?

Mukautettuja integraatioita Dynamics 365 Human Resourcesin ja Dynamics 365 Financen henkilöstöhallintomoduulin välillä ei enää tarvita. Kaikki henkilöstöhallinnon tiedot sijaitsevat samassa tietokannassa kuin muut Finance and Operations -sovellukset.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Siirtyminen Dynamics 365 Human Resourcesista Finance and Operations -sovelluksiin

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia henkilöstöhallintonsa toimintoihin. Mitä on suunniteltava uuteen kokemukseen siirtymistä varten?

Jos organisaatiosi käyttää Dynamics 365 Human Resourcesia mutta ei käytä muita Finance and Operations -sovelluksia, henkilöstöhallintoympäristösi siirretään uuteen infrastruktuuriin. Suuri osa tästä siirtoprosessista automatisoidaan. Käytössä on prosesseja tietokannan siirtämiseksi ja synkronoimiseksi uuden infrastruktuurin kanssa.

Lisäksi käytössä on työkalut, jotta voit testata siirtoprosessia ja tarkistaa tietosi ja kokemuksesi ennen tuotantoympäristön siirtämistä.

Jos organisaatiosi käyttää sekä Dynamics 365 Human Resourcesia että Finance and Operationsin muita sovelluksia, sinun on varattava enemmän aikaa validointiin varmistaaksesi, että tiedot siirretään oikein uuteen ympäristöön. Siirtyminen uuteen infrastruktuuriin yhdistää henkilöstöhallintoympäristön tiedot Finance and Operations -ympäristöön. Työkaluja on saatavilla tietojen yhdistämisprosessin automatisoimiseksi mahdollisimman paljon. Ristiriitaisten tietojen esiintymät edellyttävät kuitenkin käyttäjän syötettä, jotta voidaan määrittää, miten ristiriita ratkaistaan. Käyttäjien ja järjestelmänvalvojien on hallittava tietojen yhdistämismäärityksiä, joissa on ristiriitoja, ja testattava siirto eristysympäristöissä ennen tuotantoympäristön siirtämistä.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia Dynamics 365 Financessa, Supply Chain Managementissa, Commercessa tai Project Operationsissa. Mitä on suunniteltava uuteen kokemukseen siirtymistä varten?

Organisaatioissa, jotka käyttävät HR-moduulia Finance and Operations -sovelluksissa, Dynamics 365 Human Resourcesin uudet toiminnot otetaan käyttöön ympäristössäsi vakiomuotoisen yhden version päivitysprosessin avulla. Voit odottaa uusia toimintoja ympäristöösi, kun niitä on saatavilla kussakin päivityksessä. Voit käyttää ominaisuuksien hallintaa uusien ominaisuuksien ottamiseksi käyttöön. Sinun on kuitenkin suunnitelmien mukaan vahvistettava nämä ominaisuudet. Seuraa käytössä olevia prosesseja muiden ympäristöpäivitysten tarkistamiseksi. Lisätietoja päivitysten käytöstä Finance and Operations -sovelluksissa on kohdassa [Yksi versio -yleiskatsaus](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Milloin organisaationi siirretään?

Kunkin organisaation siirto riippuu sen nykyisestä kokoonpanosta ja valmiudesta siirtyä uuteen infrastruktuuriin. Nämä päivämäärät voivat muuttua.

- Organisaatiot, jotka tällä hetkellä käyttävät henkilöstöhallintomoduulia Finance and Operations -sovelluksissa, saavat Dynamics 365 Human Resourcesin henkilöstöhallintotoiminnot osana tavallista yhden version päivitysprosessia. Uusien ominaisuuksien on tarkoitus tulla yleisesti saataville lokakuusta 2021 alkaen.
- Organisaatiot, jotka käyttävät tällä hetkellä vain Dynamics 365 Human Resourcesia saavat pääsyn siirtotyökaluihin testauksen ja siirron aloittamiseksi vuoden 2022 alussa tai keskivaiheilla. Päivämäärää, jolloin siirtyminen uuteen infrastruktuuriin on saatettava päätökseen, ei ole vielä määritetty. Se on kuitenkin vähintään vuoden sen jälkeen, kun siirtötyökalut tulevat saataville.
- Organisaatiot, jotka käyttävät tällä hetkellä sekä Dynamics 365 Human Resourcesia että muita Finance and Operations -sovelluksia, saavat pääsyn siirtotyökaluihin voidakseen aloittaa testauksen ja siirron vuoden 2022 lopussa. Päivämäärää, jolloin siirtyminen uuteen infrastruktuuriin on saatettava päätökseen, ei ole vielä määritetty. Se on kuitenkin vähintään vuoden sen jälkeen, kun siirtötyökalut tulevat saataville.

Lisätietoja Dynamics 365 Human Resourcesin uusista toiminnoista on aiheessa [Uudet ja muuttuneet ominaisuudet Human Resourcesissa](./hr-admin-whats-new.md).

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Käytän uusia ominaisuuksia, jotka ovat saatavilla vain Dynamics 365 Human Resourcesissa (kuten **Vapaa ja poissaolot** ja **Etujen hallinta**). Ovatko nämä ominaisuudet nyt käytettävissä myös Finance and Operations -infrastruktuurin Henkilöstöhallinto-moduulissa?

Kyllä, kaikki Dynamics 365 Human Resourcesin moduulit toimivat Finance and Operations -sovelluksissa sellaisenaan, ja ominaisuuspariteetti on 100 prosenttia. Osana yleistä siirtostrategiaa asiakkaille, jotka tällä hetkellä käyttävät näitä ominaisuuksia henkilöstöhallinnossa, asiakastiedot siirretään niin, että ne toimivat edelleen Finance and Operations -infrastruktuurissa.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Käytän uusia Dynamics 365 Human Resourcesin etujenhallintaominaisuuksia. Olen rakentanut räätälöityjä integraatioita henkilöstöhallintomoduulin kanssa Finance and Operations -infrastruktuuriin, jotta voin hyödyntää palkanlaskentaominaisuuksia etuustietojen avulla. Tarvitaanko näitä mukautettuja integraatioita jatkossa?

Osana infrastruktuurin yhdistämistä henkilöstöhallintotiedot tuodaan samaan tietokantaan muiden Finance and Operations -sovellusten kanssa. Moduulien välistä integrointia Finance and Operations -sovelluksissa ei tarvita enää.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Organisaationi käyttää vähintään yhtä ISV-ratkaisua Dynamics 365 Human Resourcesssa. Siirretäänkö ISV-ratkaisumme automaattisesti?

Kunkin riippumattoman ohjelmistotoimittajan (ISV) ratkaisun siirtokokemus vaihtelee ratkaisun integrointimenetelmän mukaan. Microsoft tekee tiivistä yhteistyötä riipumattomien ohjelmistotoimittajien kanssa varmistaakseen sujuvan siirtymisen uuteen infrastruktuuriin.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Organisaationi käyttää LinkedIn Talent Hub -integraatiota Dynamics 365 Human Resourcesin kanssa. Toimiiko tämä integrointi infrastruktuurimuutoksen jälkeen?

Kyllä, LinkedIn Talent Hub -integraatio toimii edelleen uuteen infrastruktuuriin siirtymisen jälkeen.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Organisaationi käyttää Teamsin Human Resources -sovellusta. Toimiiko tämä sovellus infrastruktuurimuutoksen jälkeen?

Kyllä, Teamsin Human Resources -sovellus toimii edelleen uuteen infrastruktuuriin siirtymisen jälkeen.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Organisaationi on määrittänyt mukautetun suojauksen Dynamics 365 Human Resourcesssa. Toimiiko mukautettu suojaus vielä infrastruktuurimuutoksen valmistuttua?

Kyllä, mukautetut suojausmääritykset sisällytetään tietojen siirtoon uuteen infrastruktuuriin.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Käytämme dataintegraattoria tietojen ja sovellusten siirtoon Dynamics 365 Human Resourcesin ja Finance and Operationsin välillä. Mitä integroitaville tiedoille tapahtuu?

Dynamics 365 Human Resourcesista lähtöisin olevat henkilöstöhallinnon tiedot synkronoidaan Dataversen kanssa. Tietointegraattoria voidaan sitten käyttää yksisuuntaiseen synkronointiin Finance and Operations -sovellusten kanssa. Uuteen infrastruktuuriin siirtymisen jälkeen henkilöstöhallinnon tiedot ovat alkuperäisiä Finance and Operations -sovelluksille. Tietointegraattoria ei enää tarvita tietojen synkronointiin Finance and Operations -sovellusten ja henkilöstöhallinnon välillä.

Nykyiset alkuperäiset Dataversen tietotaulut henkilöstöresursseille jatkavat tietojen synkronointia ympäristöstä uudessa infrastruktuurissa. Entiteetit muunnetaan tukemaan kaksoiskirjoitusta. Kaikki muut tietointegraatiot, jotka on määritetty tietointegraattorin avulla näitä taulukoita kohti muissa Dynamics 365 -sovelluksissa, toimivat edelleen nykyisten määritysten mukaisesti.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Käytämme kaksoiskirjoitusta henkilöstöhallinnon tietojen siirtoon Dataversen ja muiden Finance and Operations -sovellusten välillä. Miten uuteen infrastruktuuriin siirtyminen vaikuttaa tällä hetkellä integroitaisiin tietoihin?

Henkilöstöhallinnon tiedot ovat alkuperäisiä Finance and Operations -sovelluksille uuden infrastuktuurin ympäristössä. Tämän jälkeen kaksoiskirjoitusta käytetään henkilöstöhallinnon tietojen välittämiseen uuden ympäristön ja Dataverse-ympäristön välillä.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Olemme rakentaneet räätälöityjä integraatioita Dynamics 365 Human Resourcesista yhteen tai useampaan ulkoiseen järjestelmään. Onko meidän kehitettävä uusi integraatio infrastruktuurimuutoksen jälkeen?

Se riippuu integroinnin päätepisteestä. Lisätietoja Finance and Operations -sovelluksissa käytettävissä olevista integrointitekniikoista ja parhaan integrointitekniikan valitsemisesta on kohdassa [Integraation yleiskatsaus](../fin-ops-core/dev-itpro/data-entities/integration-overview.md) .

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Olemme laajentaneet Dataversea Dynamics 365 Human Resourcesille. Siirretäänkö nämä laajennukset automaattisesti?

Jos Dynamics 365 Human Resources ja Finance and Operations -ympäristöt, jotka liitetään uuden infrastruktuurin ympäristöön yhdistyvät samaan Dataverse-ympäristöön, nämä kaksi sovellusta yhdistyvät jatkossakin samaan  Dataverse-ympäristöön siirron jälkeen. Tämän vuoksi Dataverse-laajennuksia varten ei tarvita siirtoa.

Jos kuitenkin Dynamics 365 Human Resources ja Finance and Operations -ympäristöt yhdistyvät tällä hetkellä eri Dataverse-ympäristöihin, nämä kaksi Dataverse-ympäristöä on yhdistettävä, jotta ne yhdistyvät yhteen ympäristöön uudessa infrastruktuurissa. Tätä Dataverse-siirtoa varten Dataverse-henkilöstöresurssiratkaisuissa vakiona olevat taulut voidaan yhdistää ja synkronoida uudelleen uuden Dataverse-ympäristön kanssa. Dataverse-ympäristön laajennuksia ei kuitenkaan siirretä automaattisesti, vaan ne on otettava uudelleen käyttöön uuteen ympäristöön. Suosittelemme, että käytät hallittuja ratkaisuja Dataverse-laajennusten hallintaan. Lisätietoja on kohdassa [Johdanto ratkaisuihin](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Olemme määrittäneet Microsoft Power Automate -työnkulkuja ja/tai Microsoft Power Appsin työskentelemään Dynamics 365 Human Resources -järjestelmän kanssa. Siirretäänkö nämä Microsoft Power Platform -komponentit ja toimivatko ne automaattisesti infrastruktuurin muutoksen valmistuttua?

Power Apps- ja Power Automate -työnkulut ja muut Microsoft Power Platform -mukautukset ovat samankaltaisia Dataverse-laajennusten kanssa. Se, toimivatko ne automaattisesti uuteen infrastruktuuriin siirtymisen jälkeen, riippuu siitä, ovatko Human Resources -sovellus ja Finance and Operations -sovellukset yhteydessä samaan Power Apps -ympäristöön ennen siirtoa.

Jos sovellukset ovat tällä hetkellä yhteydessä samaan Power Apps -ympäristöön, ne ovat edelleen yhteydessä tähän Power Apps -ympäristöön uuteen infrastruktuuriin siirtymisen jälkeen. Tässä tapauksessa Power Apps- ja Power Automate -työnkulkujen ja muiden Microsoft Power Platform -mukautusten toiminta jatkuu ilman lisämäärityksiä. Suosittelemme, että käytät hallittuja ratkaisuja sovellusten laajennusten hallintaan Dataversessa. Lisätietoja on kohdassa [Johdanto ratkaisuihin](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

Jos Human Resources-sovellus ja Finance and Operations -sovellukset on kuitenkin yhdistetty erillisiin Power Apps -ympäristöihin, ne on yhdistettävä osana siirtoa. Tämä tehtävä edellyttää, että kaikki Power Apps -mukautukset ja muut mukautukset on tehtävä uudelleen uudessa ympäristössä.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Olemme ottanut käyttöön Dataverse-virtuaalitaulukot Dynamics 365 Human Resourcesille. Mitä näille taulukoille tapahtuu siirron aikana?

Siirron jälkeen, jos uuden infrastruktuurin ympäristö pysyy yhteydessä Dataverse-ympäristöön, joka on tällä hetkellä yhteydessä Dynamics 365 Human Resources -ympäristöön, ympäristössä luodut Dataverse-näennäistaulukot toimivat edelleen ilman lisämäärityksiä.

Jos uuden infrastruktuurin ympäristö kuitenkin liitetään siirron jälkeen toiseen Dataverse-ympäristöön, virtuaalitaulukot on luotava uudelleen uudessa Dataverse-ympäristössä.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Olemme kehittäneet integroinnin käyttämällä Applicant Tracking System (ATS) -ohjelmointirajapintaa, Payroll-ohjelmointirajapintaa, Dataversen näennäistauluja Dynamics 365 Human Resourcesille tai muita Dataversen verkko-ohjelmointirajapinnan entiteettejä. Toimivatko nämä ntegroinnit infrastruktuurimuutoksen jälkeen?

Siirron jälkeen, jos uuden infrastruktuurin ympäristö pysyy yhteydessä Dataverse-ympäristöön, joka on tällä hetkellä yhteydessä Dynamics 365 Human Resources -ympäristöön, Dataverse-verkko-ohjelmointirajapinnan avulla kehitetyt integraatiot toimivat siirron jälkeen.

Jos kuitenkin uuden infrastruktuurin ympäristö yhdistyy eri Dataverse-ympäristöön siirron jälkeen, Dataverse-verkko-ohjelmointirajapinnan avulla kehitetyt integroinnit on määritettävä uudelleen siten, että ne yhdistyvät uuteen Dataverse-ympäristöön.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Vaikuttaako ympäristöni siirtyminen Azure-alueeseen?

Henkilöstöhallinnon odotetaan pysyvän yleensä samalla Azuren alueella siirron aikana. Ainoa poikkeus ilmenee, jos henkilöstöhallinnon ympäristö yhdistetään Finance and Operations -ympäristöön, joka sijaitsee eri alueella. Tässä tapauksessa henkilöstöhallinnon ympäristö siirretään Finance and Operations -ympäristön Azure-alueelle.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Organisaationi liiketoimintaprosessit tarvitsevat Dynamics 365 Human Resourcesin työnkulkuja. Siirretäänkö nämä työnkulut automaattisesti?

Kyllä, työnkulun määritykset, työnkulkuhistoria ja nykyiset käynnissä olevat työnkulut siirretään.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Mitä koulutusta ja resursseja on käytettävissä siirtoprosessissa?

Yksityiskohtaiset asiakirjat, joissa kuvataan yksityiskohtaisesti siirtoprosessin jokainen vaihe, toimitetaan. Lisäkoulutusresursseja, kuten videoita ja työpajoja, saattaa myös olla saatavilla tarpeen mukaan.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Organisaationi on luonut tallennettuja näkymiä Dynamics 365 Human Resourcesissa käyttöliittymän käytettävyyden parantamiseksi. Siirretäänkö nämä tallennetut näkymät automaattisesti?

Kyllä, tallennetut näkymät siirretään uuteen infrastruktuuriin.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Käytämme Ceridiania Dynamics 365 Human Resourcesin kanssa. Ovatko Ceridian-ntegroinnit käytettävissä infrastruktuurimuutoksen jälkeen? 

Integrointi Ceridianin kanssa siirretään Palkanlaskennan ohjelmistorajapinta -pohjaiseen integraatioon. Dynamics 365 Human Resources -järjestelmän tiedostopohjaista integrointia ei siirretä Finance and Operations -infrastruktuuriin. Lisätietoja on kohdassa [Johdanto palkanlaskennan ohjelmistorajapintaan](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Miten siirto vaikuttaa palvelun päivitysprosessiin?

Siirron jälkeen asiakkailla on paljon enemmän joustavuutta ALM:n ja palvelupäivitysten suhteen. Palvelupäivityksiä ei enää suoriteta automaattisesti Human Resources -ympäristöissä. Sen sijaan palvelu noudattaa One Version -palvelun päivitysprosesseja ja -toimintoja. Tämän vuoksi päivitysten määritysasetukset ovat käytettävissä LCS:n kautta. Lisätietoja on kohdassa [One Version -yleiskatsaus](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Miten siirtyminen vaikuttaa LCS-projektiini Dynamics 365 Human Resourcesissa?

Siirtyminen uuteen infrastruktuuriin siirtää Dynamics 365 Human Resources -ympäristöjen hallinnan LCS:n käyttöönottoprojektiin. Jos siirto yhdistää Dynamics 365 Human Resourcesin aiemmin luotuun Finance and Operations -ympäristöön, Human Resources LCS -projekti yhdistetään Finance and Operations -sovelluksen LCS-käyttöönottoprojektiin.  Jos käytössäsi on vain Dynamics 365 Human Resources, uusi LCS-käyttöönottoprojekti luodaan ja nykyinen Human Resources LCS -projekti siirretään uuteen projektiin.

Uusi projekti on samantyyppinen projekti, jota Finance and Operations -sovellukset käyttävät. Sillä on samat ominaisuudet ja toiminnot ympäristön hallintaan. Lisätietoja on kohdassa [Lifecycle Services -resurssit](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Olemme linkittäneet tehtävätallenteemme Human Resourcesin liiketoimintaprosessien mallintajaan. Miten liiketoimintaprosessin mallintaja siirretään ja yhdistetään LCS:hen?

LCS-projektin liiketoimintaprosessikirjastot siirretään uuteen Human Resources -LCS-projektiin.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Organisaationi käyttää tällä hetkellä vain Dynamics 365 Human Resourcesia. Mitä resursseja on käytettävissä, jotta saamme lisätietoja kehitysvalmiuksista infrastruktuurimuutoksen valmistuttua?

Sekä Microsoft Power Platformin laajennusvaihtoehdot että Finance and Operationsin laajennusvaihtoehdot ovat saatavilla, ja niitä voidaan käyttää kehitykseen. Lisätietoja on kohdassa [Kotisivun kehittäminen ja mukauttaminen](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Olemme ottaneet toimintoja käyttöön Dynamics 365 Human Resourcesissa. Otetaanko nämä ominaisuudet käyttöön automaattisesti siirron aikana?

Se, otetaanko ominaisuus automaattisesti käyttöön uudessa infrastruktuurissa, määritetään erikseen kullekin ominaisuudelle. Nämä tiedot sisältyvät ominaisuusdokumentaatioon.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Mitä BYOD-tietokannalleni tapahtuu siirron aikana?

Oman tietokantasi (BYOD) tuonti- ja vientimääritykset siirretään uuteen infrastruktuuriin.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Mitä Azure Data Lakelleni tapahtuu siirron aikana?

Mikä tahansa vienti, joka on nykyisellään määritetty Azure Data Lake Storagelle Finance and Operations -sovelluksissa, säilyttää saman määrityksen siirron jälkeen. 

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Käytämme tällä hetkellä Dynamics AX 2012:ta. Käytetäänkö tällä hetkellä käytettävissä olevia päivitystyökaluja HR-moduulin päivittämiseen AX 2012:sta Dynamics 365 Human Resourcesiin?

Kyllä. Dynamics 365 Human Resources sisällytetään yhdistettyyyn koodikantaan ja Finance and Operations -sovellusten infrastruktuuriin. Dynamics AX 2012:sta Dynamics 365 Human Resourcesiin käyttää samaa päivityspolkua ja työkaluja, joita käytetään Finance and Operations -sovellusten uusimpaan versioon päivittämiseen.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Käytämme asiakirjojen käsittelyä Dynamics 365 Human Resourcesissa. Mitä näille asiakirjoille tapahtuu siirron aikana?

Asiakirjat säilyvät aiemmin luodussa asiakirjojen tallennustilassa. Ne yhdistetään uudelleen ympäristöön uudessa infrastruktuurissa.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Mitä tapahtuu erätöille, jotka olemme määrittäneet Dynamics 365 Human Resourcesissa siirron jälkeen?

Soveltuvat erätyöt siirretään automaattisesti uuteen infrastruktuuriin.

## <a name="licensing-impact"></a>Vaikutus lisensseihin

Tämä dokumentaatio ei ylitä tai korvaa mitään käyttöoikeuksia käsittelevää oikeudellista dokumentaatiota.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia henkilöstöhallintonsa toimintoihin. Muuttuvatko lisensointimme tai kustannuksemme?

Tämä ei vaikuta Dynamics 365 Human Resources -asiakkaisiin, jotka ovat ostaneet käyttöoikeuksia. Näille asiakkaalle ei ole lisensointisiirtoa. Human Resourcesille määritettyä ylimääräistä eristysvarastointiyksikköä (SKU) ei enää sovelleta. Sen sijaan asiakkaat voivat ostaa Finance and Operations -sovellusten Tason 2 eristysympäristön hieman halvemmalla. Nykyiset asiakkaat, jotka ovat ostaneetHuman Resources-eristysympäristön, siirretään Finance and Operations -sovellusten Taso 2 -eristysympäristöön ilman lisäkustannuksia.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia Dynamics 365 Financessa, Supply Chain Managementissa, Commercessa tai Project Operationsissa. Muuttuvatko lisensointini tai kustannukseni?

Dynamics 365 -sovellusten nykyiset käyttäjät ja itsenäisen Dynamics 365 Financen, Supply Chain Managementin, Commercen ja Project Operationsin käyttäjät voivat käyttää Human Resources osana kyseisiä lisenssejä helmikuuhun 2025 asti tai nykyisen käyttöoikeussopimuksen päättymiseen saakka sen mukaan, kumpi ajankohta on aikaisempi. Voit siirtyä Human Resources -lisensseihin aikaisemmin, jos se auttaa sinua saavuttamaan parempia kustannussäästöjä. Helmikuusta 2025 alkaen kaikkien nykyisten CSP- ja EA-asiakkaiden on otettava HR-moduuli käyttöön ja ostettava Human Resources -lisenssit hyödyntääkseen Finance and Operations -sovelluksiin tuotavat uudet ominaisuudet.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Organisaationi käyttää Dynamics 365 Financea, Supply Chain Managementia, Commercea tai Project Operationsia tuotantokäytössä. Vaaditaanko meidän ostavan lisäympäristön infrastruktuurin yhdistämisen tueksi?

Infrastruktuurin muutoksen tueksi ei tarvita lisäympäristöjä.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Minne minun pitäisi mennä, jos minulla on lisäkysymyksiä tuotteiden lisensoinnista?

Jos sinulla on käyttöoikeuskysymyksiä, löydät lisätietoja kohteesta [Biz Apps Hub – D365-hinnoittelu ja lisensointi](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Jos nämä tiedot eivät auta ongelmassasi, avaa pyyntö LicenseQ:ssa.
