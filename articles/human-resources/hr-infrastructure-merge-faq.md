---
title: Dynamics 365 Human Resources -infrastruktuurin yhdistämisen usein kysytyt kysymykset
description: Tässä ohjeaiheessa vastataan usein kysyttyihin kysymyksiin Microsoft Dynamics 365 Human Resourcesin ja taloushallinnon ja toimintojen sovellusten infrastruktuurin yhdistämisestä.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 766ee49c17749841d8acac6637a0262e87e52e92
ms.sourcegitcommit: d38d2fe85dc2497211ba5731617f590029d07145
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809610"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources -infrastruktuurin yhdistämisen usein kysytyt kysymykset

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tässä ohjeaiheessa vastataan usein kysyttyihin kysymyksiin Microsoft Dynamics 365 Human Resourcesin ja taloushallinnon ja toimintojen sovellusten infrastruktuurin yhdistämisestä.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Mikä on Dynamics 365 Human Resources -infrastruktuurin yhdistäminen?

Dynamics 365 Human Resources on itsenäinen sovellus, joka käyttää eri infrastruktuuria kuin muut taloushallinnon ja toimintojen sovellukset, kuten Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Project Operations. Infrastruktuurin yhdistäminen tuo Dynamics 365 Human Resourcesin samaan infrastruktuuriin muiden taloushallinnon ja toimintojen sovellusten kanssa.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktuurin yhdistämisen arvo ja hyödyt

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia henkilöstöhallintonsa toimintoihin. Mitä hyötyä näistä muutoksista on?

- Nämä muutokset poistavat Dynamics 365:n useiden henkilöstöhallinnon ominaisuuksien aiheuttamaa sekaannusta.
- Ne tarjoavat sekä Microsoft Power Platform -laajennettavuutta että tavan laajentaa liiketoimintalogiikkaa ja ominaisuusvaihtoehtoja.
- Ne yhdenmukaistavat sovellusten elinkaaren hallintaa Dynamics 365 Human Resourcesin ja muiden taloushallinnon ja toimintojen sovellusten välillä sekä Microsoft Dynamics Lifecycle Servicesin (LCS) suhteen, maantieteellistä saatavuutta ja paljon muuta.
- Niiden avulla voit hyödyntää jaettuja palveluita ja työkaluja ja auttaa vähentämään kustannuksia.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Organisaation käyttää henkilöstöhallintomoduulia Dynamics 365 Financessa, Supply Chain Managementissa, Commercessa tai Project Operationsissa. Mitä hyötyä näistä muutoksista on?

Dynamics 365 Human Resourcesin ominaisuudet ja investoinnit ovat nyt niiden asiakkaiden käytettävissä, jotka käyttävät Dynamics 365 Financen henkilöstöhallintomoduulia. Joitakin näistä ominaisuuksista ovat loman- ja poissaolojen hallinta, etujen hallinta ja tehtävien hallinta.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Menetänkö tällä hetkellä käytössä olevat ominaisuudet?

Dynamics 365 Human Resourcesin ja taloushallinnon ja toimintojen sovellusten henkilöstöhallinnon moduulin välillä on toiminnallisia samankaltaisuuksia. Dynamics 365 Human Resources on etusijalla samankaltaisissa ominaisuuksissa. Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Muuttuuko käyttökokemus käyttäjilleni?

Uusia HR-ominaisuuksia hallitaan ominaisuuksien hallinnan avulla. Asiakkaat päättävät, haluavatko he ottaa ne vastaan. Joissakin tapauksissa ominaisuuksia saatetaan muokata. Näissä tapauksissa toimitetaan dokumentaatio.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Miten tämä muutos vaikuttaa minuun, jos olen olemassa oleva asiakas ja käytän sekä henkilöstöhallintomoduulia taloushallinnon ja toimintojen infrastruktuurissa että Dynamics 365 Human Resourcesia mukautettujen integraatioiden kautta?

Mukautettuja integraatioita Dynamics 365 Human Resourcesin ja Dynamics 365 Financen henkilöstöhallintomoduulin välillä ei enää tarvita. Kaikki henkilöstöhallinnon tiedot sijaitsevat samassa tietokannassa kuin muut taloushallinnon ja toimintojen sovellukset.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Siirtyminen Dynamics 365 Human Resourcesista taloushallinnon ja toimintojen sovelluksiin

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia henkilöstöhallintonsa toimintoihin. Mitä on suunniteltava uuteen kokemukseen siirtymistä varten?

Jos organisaatiosi käyttää Dynamics 365 Human Resourcesia mutta ei käytä muita taloushallinnon ja toimintojen sovelluksia, henkilöstöhallintoympäristösi siirretään uuteen infrastruktuuriin. Suuri osa tästä siirtoprosessista automatisoidaan. Käytössä on prosesseja tietokannan siirtämiseksi ja synkronoimiseksi uuden infrastruktuurin kanssa.

Lisäksi käytössä on työkalut, jotta voit testata siirtoprosessia ja tarkistaa tietosi ja kokemuksesi ennen tuotantoympäristön siirtämistä.

Jos organisaatiosi käyttää sekä Dynamics 365 Human Resourcesia että muita taloushallinnon ja toimintojen sovelluksia, sinun on varattava enemmän aikaa validointiin varmistaaksesi, että tiedot siirretään oikein uuteen ympäristöön. Siirtyminen uuteen infrastruktuuriin yhdistää Human Resources -ympäristön tiedot taloushallinnon ja toimintojen ympäristöön. Ristiriitaisten tietojen vuoksi käyttäjän on päätettävä, miten ristiriita ratkaistaan. Käyttäjien ja järjestelmänvalvojien on hallittava tietojen yhdistämismäärityksiä, joissa on ristiriitoja, ja testattava siirto eristysympäristöissä ennen tuotantoympäristöjen siirtämistä.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Organisaation käyttää henkilöstöhallintomoduulia Dynamics 365 Financessa, Supply Chain Managementissa, Commercessa tai Project Operationsissa. Mitä on suunniteltava uuteen kokemukseen siirtymistä varten?

Organisaatioissa, jotka käyttävät HR-moduulia taloushallinnon ja toimintojen sovelluksissa, Dynamics 365 Human Resourcesin uudet toiminnot otetaan käyttöön ympäristössäsi vakiomuotoisen One Version -päivitysprosessin avulla. Voit odottaa uusia toimintoja ympäristöösi, kun niitä on saatavilla kussakin päivityksessä. Vaikka uudet ominaisuudet voidaan ottaa käyttöön ominaisuuksien hallinnassa, kannattaa kuitenkin varautua näiden ominaisuuksien tarkistamiseen. Seuraa käytössä olevia prosesseja muiden ympäristöpäivitysten tarkistamiseksi. Lisätietoja päivitysten käytöstä taloushallinnon ja toimintojen sovelluksissa on kohdassa [One Version -yleiskatsaus](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Milloin organisaationi siirretään?

Kunkin organisaation siirto riippuu sen nykyisestä kokoonpanosta ja valmiudesta siirtyä uuteen infrastruktuuriin. Nämä päivämäärät voivat muuttua.

- Organisaatiot, jotka tällä hetkellä käyttävät henkilöstöhallintomoduulia taloushallinnon ja toimintojen sovelluksissa, saavat Dynamics 365 Human Resourcesin henkilöstöhallintotoiminnot osana tavallista One Version -päivitysprosessia. Uusien ominaisuuksien on tarkoitus olla yleisesti saatavana tammikuusta 2022 alkaen.
- Organisaatiot, jotka käyttävät vain Dynamics 365 Human Resourcesia saavat siirtotyökalujen käyttöoikeuden, joten ne voivat aloittaa testauksen ja käynnistää siirron vuoden 2022 keskivaiheilla. Päivämäärää, jolloin siirtyminen uuteen infrastruktuuriin on saatettava päätökseen, ei ole vielä määritetty. Se on kuitenkin vähintään vuoden sen jälkeen, kun siirtötyökalut tulevat saataville.
- Organisaatiot, jotka käyttävät tällä hetkellä sekä Dynamics 365 Human Resourcesia että muita taloushallinnon ja toimintojen sovelluksia, saavat pääsyn siirtotyökaluihin voidakseen aloittaa testauksen ja siirron vuoden 2022 lopussa. Päivämäärää, jolloin siirtyminen uuteen infrastruktuuriin on saatettava päätökseen, ei ole vielä määritetty. Se on kuitenkin vähintään vuoden sen jälkeen, kun siirtötyökalut tulevat saataville.

Lisätietoja Dynamics 365 Human Resourcesin uusista toiminnoista on aiheessa [Uudet ja muuttuneet ominaisuudet Human Resourcesissa](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Organisaatio ei ole vielä ottanut Dynamics 365 Human Resourcesia käyttöön. Kannattaako henkilöstöhallintamoduuli ottaa käyttöön taloushallinnon ja toimintojen sovelluksissa tai vanhassa infrastruktuurissa Dynamics 365 Human Resources -sovelluksessa?

Olennaista on pohtia, mitä henkilöstöhallintotoimintoja tarvitaan ja milloin kyseiset toiminnot ovat saatavana uudessa infrastruktuurissa. Jos organisaatio tarvitsee henkilöstöhallinnon perustoimintoja, ne ovat tällä hetkellä saatavana uuden infrastruktuurin taloushallinnon ja toimintojen sovellusten henkilöstöhallintomoduulissa. Taloushallinnon ja toimintojen sovellusten henkilöstöhallintamoduulin ja Dynamics 365 Human Resources -sovelluksen ominaisuuksien pariteetin odotetaan toteutuvan versiossa 10.0.25, joka on aikataulutettu julkaistavaksi maaliskuussa 2022. Integrointiominaisuudet, kuten Teams-sovelluksen ja Dataverse-entiteetin integroinnit, ovat saatavana myöhemmissä versioissa.

Jos organisaation henkilöstöhallintotoimintojen oltava saatavana uudessa infrastruktuurissa sinä aikana, kun organisaatio ottaa sen käyttöön, käyttöönotto voi olla helpompaa taloushallinnon ja toimintojen sovellusten henkilöstöhallintamoduulissa. Tämä helpottaa siirtymistä, sillä se tulee olemaa Dynamics 365 Human Resources -sovelluksen vakiosovelluspäivitys, joten asiakas on jo valmiiksi uudessa infrastruktuurissa. Jos organisaatio päättää ottaa käyttöön Dynamics 365 Human Resources -sovelluksen vanhassa infrastruktuurissa, ympäristön siirto on sitten siirrettävä uuteen infrastruktuuriin. Tämä voidaan välttää tekemällä käyttöönotto uudessa infrastruktuurissa.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Käytän uusia ominaisuuksia, jotka ovat saatavilla vain Dynamics 365 Human Resourcesissa (kuten **Vapaa ja poissaolot** ja **Etujen hallinta**). Ovatko nämä ominaisuudet nyt käytettävissä myös taloushallinnon ja toimintojen infrastruktuurin Henkilöstöhallinto-moduulissa?

Kyllä, kaikki Dynamics 365 Human Resourcesin moduulit toimivat taloushallinnon ja toimintojen sovelluksissa sellaisenaan, ja ominaisuuspariteetti on 100 prosenttia. Osana yleistä siirtostrategiaa asiakkaille, jotka tällä hetkellä käyttävät näitä ominaisuuksia henkilöstöhallinnossa, asiakastiedot siirretään niin, että ne toimivat edelleen taloushallinnon ja toimintojen infrastruktuurissa.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Käytän uusia Dynamics 365 Human Resourcesin etujenhallintaominaisuuksia. Olen rakentanut räätälöityjä integraatioita henkilöstöhallintomoduulin kanssa taloushallinnon ja toimintojen infrastruktuuriin, jotta voin hyödyntää palkanlaskentaominaisuuksia etuustietojen avulla. Tarvitaanko näitä mukautettuja integraatioita jatkossa?

Osana infrastruktuurin yhdistämistä henkilöstöhallintotiedot tuodaan samaan tietokantaan muiden taloushallinnon ja toimintojen sovellusten kanssa. Moduulien välistä integrointia taloushallinnon ja toimintojen sovelluksissa ei tarvita enää.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Organisaationi käyttää vähintään yhtä ISV-ratkaisua Dynamics 365 Human Resourcesssa. Siirretäänkö ISV-ratkaisumme automaattisesti?

Kunkin riippumattoman ohjelmistotoimittajan (ISV) ratkaisun siirtokokemus vaihtelee ratkaisun integrointimenetelmän mukaan. Microsoft tekee tiivistä yhteistyötä riipumattomien ohjelmistotoimittajien kanssa varmistaakseen sujuvan siirtymisen uuteen infrastruktuuriin.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Organisaationi käyttää LinkedIn Talent Hub -integraatiota Dynamics 365 Human Resourcesin kanssa. Toimiiko tämä integrointi infrastruktuurimuutoksen jälkeen?

Ei, LinkedIn Talent Hub -integraatio ei toimi uuteen infrastruktuuriin siirtymisen jälkeen. LinkedIn Talent Hub -integraatiopalvelu poistetaan käytöstä vanhan Dynamics 365 Human Resources -infrastruktuurin ohella.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Organisaationi käyttää Teamsin Human Resources -sovellusta. Toimiiko tämä sovellus infrastruktuurimuutoksen jälkeen?

Kyllä, Teamsin Human Resources -sovellus toimii edelleen uuteen infrastruktuuriin siirtymisen jälkeen.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Organisaationi on määrittänyt mukautetun suojauksen Dynamics 365 Human Resourcesssa. Toimiiko mukautettu suojaus vielä infrastruktuurimuutoksen valmistuttua?

Kyllä, mukautetut suojausmääritykset sisällytetään tietojen siirtoon uuteen infrastruktuuriin.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Käytämme dataintegraattoria tietojen ja sovellusten siirtoon Dynamics 365 Human Resourcesin ja taloushallinnon ja toimintojen sovellusten välillä. Mitä integroitaville tiedoille tapahtuu?

Dynamics 365 Human Resourcesissa tällä hetkellä olevat henkilöstöhallinnon tiedot synkronoidaan Dataversen kanssa. Tietointegraattoria voidaan sitten käyttää yksisuuntaiseen synkronointiin taloushallinnon ja toimintojen sovellusten kanssa. Uuteen infrastruktuuriin siirtymisen jälkeen henkilöstöhallinnon tiedot ovat alkuperäisiä taloushallinnon ja toimintojen sovellusten tietoja. Tietointegraattoria ei enää tarvita tietojen synkronointiin taloushallinnon ja toimintojen sovellusten ja henkilöstöhallinnon välillä.

Nykyiset alkuperäiset Dataversen tietotaulut henkilöstöresursseille jatkavat tietojen synkronointia ympäristöstä uudessa infrastruktuurissa. Entiteetit muunnetaan tukemaan kaksoiskirjoitusta. Kaikki muut tietointegraatiot, jotka on määritetty tietointegraattorin avulla näitä taulukoita kohti muissa Dynamics 365 -sovelluksissa, toimivat edelleen nykyisten määritysten mukaisesti.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Käytämme kaksoiskirjoitusta henkilöstöhallinnon tietojen siirtoon Dataversen ja muiden taloushallinnon ja toimintojen sovellusten välillä. Miten uuteen infrastruktuuriin siirtyminen vaikuttaa tällä hetkellä integroitaisiin tietoihin?

Henkilöstöhallinnon tiedot ovat alkuperäisiä taloushallinnon ja toimintojen sovelluksille uuden infrastruktuurin ympäristössä. Kaksoiskirjoitusta käytetään henkilöstöhallinnon tietojen siirtämiseen uuden ympäristön ja Dataverse-ympäristön välillä.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Olemme rakentaneet räätälöityjä integraatioita Dynamics 365 Human Resourcesista yhteen tai useampaan ulkoiseen järjestelmään. Onko meidän kehitettävä uusi integraatio infrastruktuurimuutoksen jälkeen?

Se riippuu integroinnin päätepisteestä. Lisätietoja taloushallinnon ja toimintojen sovelluksissa käytettävissä olevista integrointitekniikoista ja parhaan integrointitekniikan valitsemisesta on kohdassa [Integraation yleiskatsaus](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Olemme laajentaneet Dataversea Dynamics 365 Human Resourcesille. Siirretäänkö nämä laajennukset automaattisesti?

Jos Dynamics 365 Human Resources ja taloushallinnon ja toimintojen ympäristöt, jotka liitetään uuden infrastruktuurin ympäristöön yhdistyvät samaan Dataverse-ympäristöön, nämä kaksi sovellusta yhdistyvät jatkossakin samaan Dataverse-ympäristöön siirron jälkeen. Dataverse-laajennuksia varten ei tarvita siirtoa.

Jos kuitenkin Dynamics 365 Human Resources ja taloushallinnon ja toimintojen ympäristöt yhdistyvät tällä hetkellä eri Dataverse-ympäristöihin, nämä kaksi Dataverse-ympäristöä on yhdistettävä, jotta ne yhdistyvät yhteen ympäristöön uudessa infrastruktuurissa. Tätä Dataverse-siirtoa varten Dataverse-henkilöstöresurssiratkaisuissa vakiona olevat taulut voidaan yhdistää ja synkronoida uudelleen uuden Dataverse-ympäristön kanssa. Dataverse-ympäristön laajennuksia ei siirretä automaattisesti, vaan ne on otettava uudelleen käyttöön uudessa ympäristössä. Suosittelemme, että käytät hallittuja ratkaisuja Dataverse-laajennusten hallintaan. Lisätietoja on kohdassa [Johdanto ratkaisuihin](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-utilized-the-custom-field-functionality-within-dynamics-365-human-resources-will-those-custom-fields-migrate-automatically"></a>Käytössä ovat Dynamics 365 Human Resourcesin mukautetut kenttätoiminnot, siirtyvätkö nämä mukautetut kentät automaattisesti?
Kyllä, lisätyt mukautetut kentät siirtyvät uuteen infrastruktuuriin.

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Olemme määrittäneet Microsoft Power Automate -työnkulkuja ja/tai Microsoft Power Appsin työskentelemään Dynamics 365 Human Resources -järjestelmän kanssa. Siirretäänkö nämä Microsoft Power Platform -komponentit ja toimivatko ne automaattisesti infrastruktuurin muutoksen valmistuttua?

Power Apps- ja Power Automate -työnkulut ja muut Microsoft Power Platform -mukautukset ovat samankaltaisia Dataverse-laajennusten kanssa. Se, toimivatko ne automaattisesti uuteen infrastruktuuriin siirtymisen jälkeen, riippuu siitä, ovatko Human Resources -sovellus ja taloushallinnon ja toimintojen sovellukset yhteydessä samaan Power Apps -ympäristöön ennen siirtoa.

Jos sovellukset ovat tällä hetkellä yhteydessä samaan Power Apps -ympäristöön, ne ovat edelleen yhteydessä tähän Power Apps -ympäristöön uuteen infrastruktuuriin siirtymisen jälkeen. Tässä tapauksessa Power Apps- ja Power Automate -työnkulkujen ja muiden Microsoft Power Platform -mukautusten toiminta jatkuu ilman lisämäärityksiä. Suosittelemme, että käytät hallittuja ratkaisuja sovellusten laajennusten hallintaan Dataversessa. Lisätietoja on kohdassa [Johdanto ratkaisuihin](/powerapps/developer/data-platform/introduction-solutions).

Jos Human Resources-sovellus ja taloushallinnon ja toimintojen sovellukset on kuitenkin yhdistetty erillisiin Power Apps -ympäristöihin, ne on yhdistettävä osana siirtoa. Tämä tehtävä edellyttää, että kaikki Power Apps -mukautukset ja muut mukautukset on tehtävä uudelleen uudessa ympäristössä.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Olemme ottanut käyttöön Dataverse-virtuaalitaulukot Dynamics 365 Human Resourcesille. Mitä näille taulukoille tapahtuu siirron aikana?

Siirron jälkeen, jos uuden infrastruktuurin ympäristö pysyy yhteydessä Dataverse-ympäristöön, joka on tällä hetkellä yhteydessä Dynamics 365 Human Resources -ympäristöön, ympäristössä luodut Dataverse-näennäistaulukot toimivat edelleen ilman lisämäärityksiä.

Jos uuden infrastruktuurin ympäristö kuitenkin liitetään siirron jälkeen toiseen Dataverse-ympäristöön, virtuaalitaulukot on luotava uudelleen uudessa Dataverse-ympäristössä.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Olemme kehittäneet integroinnin käyttämällä Applicant Tracking System (ATS) -ohjelmointirajapintaa, Payroll-ohjelmointirajapintaa, Dataversen näennäistauluja Dynamics 365 Human Resourcesille tai muita Dataversen verkko-ohjelmointirajapinnan entiteettejä. Toimivatko nämä ntegroinnit infrastruktuurimuutoksen jälkeen?

Siirron jälkeen, jos uuden infrastruktuurin ympäristö pysyy yhteydessä Dataverse-ympäristöön, joka on tällä hetkellä yhteydessä Dynamics 365 Human Resources -ympäristöön, Dataverse-verkko-ohjelmointirajapinnan avulla kehitetyt integraatiot toimivat siirron jälkeen.

Jos kuitenkin uuden infrastruktuurin ympäristö yhdistyy eri Dataverse-ympäristöön siirron jälkeen, Dataverse-verkko-ohjelmointirajapinnan avulla kehitetyt integroinnit on määritettävä uudelleen siten, että ne yhdistyvät uuteen Dataverse-ympäristöön.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Vaikuttaako ympäristöni siirtyminen Azure-alueeseen?

Henkilöstöhallinnon odotetaan pysyvän yleensä samalla Azuren alueella siirron aikana. Ainoa poikkeus on henkilöstöhallintoympäristön yhdistäminen eri alueella sijaitsevaan taloushallinnon ja toimintojen ympäristöön. Tässä tapauksessa henkilöstöhallinnon ympäristö siirretään taloushallinnon ja toimintojen ympäristön Azure-alueelle.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Organisaationi liiketoimintaprosessit tarvitsevat Dynamics 365 Human Resourcesin työnkulkuja. Siirretäänkö nämä työnkulut automaattisesti?

Kyllä, työnkulun määritykset, työnkulkuhistoria ja nykyiset käynnissä olevat työnkulut siirretään.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Mitä koulutusta ja resursseja on käytettävissä siirtoprosessissa?

Yksityiskohtaiset asiakirjat, joissa kuvataan yksityiskohtaisesti siirtoprosessin jokainen vaihe, toimitetaan. Lisäkoulutusresursseja, kuten videoita ja työpajoja, saattaa myös olla saatavilla tarpeen mukaan.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Organisaationi on luonut tallennettuja näkymiä Dynamics 365 Human Resourcesissa käyttöliittymän käytettävyyden parantamiseksi. Siirretäänkö nämä tallennetut näkymät automaattisesti?

Kyllä, tallennetut näkymät siirretään uuteen infrastruktuuriin.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Käytämme Ceridiania Dynamics 365 Human Resourcesin kanssa. Ovatko Ceridian-ntegroinnit käytettävissä infrastruktuurimuutoksen jälkeen? 

Integrointi Ceridianin kanssa siirretään Palkanlaskennan ohjelmistorajapinta -pohjaiseen integraatioon. Dynamics 365 Human Resourcesin tiedostopohjaista integrointia ei siirretä taloushallinnon ja toimintojen infrastruktuuriin. Lisätietoja on kohdassa [Johdanto palkanlaskennan ohjelmistorajapintaan](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Miten siirto vaikuttaa palvelun päivitysprosessiin?

Siirron jälkeen asiakkailla on paljon enemmän joustavuutta ALM:n ja palvelupäivitysten suhteen. Palvelupäivityksiä ei enää suoriteta automaattisesti Human Resources -ympäristöissä. Sen sijaan palvelu noudattaa One Version -palvelun päivitysprosesseja ja -toimintoja. Tämän vuoksi päivitysten määritysasetukset ovat käytettävissä LCS:n kautta. Lisätietoja on kohdassa [One Version -yleiskatsaus](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Miten siirtyminen vaikuttaa LCS-projektiini Dynamics 365 Human Resourcesissa?

Siirtyminen uuteen infrastruktuuriin siirtää Dynamics 365 Human Resources -ympäristöjen hallinnan taloushallinnon ja toimintojen käyttöönottoprojektiin LCS:ssä. Jos siirto yhdistää Dynamics 365 Human Resourcesin aiemmin luotuun taloushallinnon ja toimintojen ympäristöön, Human Resources LCS -projekti yhdistetään taloushallinnon ja toimintojen sovelluksen LCS-käyttöönottoprojektiin. Jos käytössäsi on vain Dynamics 365 Human Resources, uusi LCS-käyttöönottoprojekti luodaan ja nykyinen Human Resources LCS -projekti siirretään uuteen projektiin.

Uusi projekti on samantyyppinen projekti, jota taloushallinnon ja toimintojen sovellukset käyttävät. Sillä on samat ominaisuudet ja toiminnot ympäristön hallintaan. Lisätietoja on kohdassa [Lifecycle Services -resurssit](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Olemme linkittäneet tehtävätallenteemme Human Resourcesin liiketoimintaprosessien mallintajaan. Miten liiketoimintaprosessin mallintaja siirretään ja yhdistetään LCS:hen?

LCS-projektin liiketoimintaprosessikirjastot siirretään uuteen Human Resources -LCS-projektiin.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Organisaationi käyttää tällä hetkellä vain Dynamics 365 Human Resourcesia. Mitä resursseja on käytettävissä, jotta saamme lisätietoja kehitysvalmiuksista infrastruktuurimuutoksen valmistuttua?

Sekä Microsoft Power Platformin laajennusvaihtoehdot että taloushallinnon ja toimintojen laajennusvaihtoehdot ovat saatavilla, ja niitä voidaan käyttää kehitykseen. Lisätietoja on kohdassa [Kotisivun kehittäminen ja mukauttaminen](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Olemme ottaneet toimintoja käyttöön Dynamics 365 Human Resourcesissa. Otetaanko nämä ominaisuudet käyttöön automaattisesti siirron aikana?

Se, otetaanko ominaisuus automaattisesti käyttöön uudessa infrastruktuurissa, määritetään erikseen kullekin ominaisuudelle. Nämä tiedot sisältyvät ominaisuusdokumentaatioon.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Mitä BYOD-tietokannalleni tapahtuu siirron aikana?

Oman tietokantasi (BYOD) tuonti- ja vientimääritykset siirretään uuteen infrastruktuuriin.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Mitä Azure Data Lakelleni tapahtuu siirron aikana?

Mikä tahansa vienti, joka on nykyisellään määritetty Azure Data Lake Storagelle taloushallinnon ja toimintojen sovelluksissa, säilyttää saman määrityksen siirron jälkeen.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Käytämme tällä hetkellä Dynamics AX 2012:ta. Käytetäänkö tällä hetkellä käytettävissä olevia päivitystyökaluja HR-moduulin päivittämiseen AX 2012:sta Dynamics 365 Human Resourcesiin?

Kyllä. Dynamics 365 Human Resources sisällytetään yhdistettyyn koodikantaan ja taloushallinnon ja toimintojen sovellusten infrastruktuuriin. Päivitys Dynamics AX 2012:sta Dynamics 365 Human Resourcesiin käyttää samaa päivityspolkua ja työkaluja, joita käytetään taloushallinnon ja toimintojen sovellusten uusimpaan versioon päivittämiseen.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Käytämme asiakirjojen käsittelyä Dynamics 365 Human Resourcesissa. Mitä näille asiakirjoille tapahtuu siirron aikana?

Asiakirjat säilyvät aiemmin luodussa asiakirjojen tallennustilassa. Ne yhdistetään uudelleen ympäristöön uudessa infrastruktuurissa.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Mitä tapahtuu erätöille, jotka olemme määrittäneet Dynamics 365 Human Resourcesissa siirron jälkeen?

Soveltuvat erätyöt siirretään automaattisesti uuteen infrastruktuuriin.

## <a name="licensing-impact"></a>Vaikutus lisensseihin

Tämä dokumentaatio ei ylitä tai korvaa mitään käyttöoikeuksia käsittelevää oikeudellista dokumentaatiota.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Organisaationi käyttää Dynamics 365 Human Resourcesia henkilöstöhallintonsa toimintoihin. Muuttuvatko lisensointimme tai kustannuksemme?

Tämä ei vaikuta Dynamics 365 Human Resources -asiakkaisiin, jotka ovat ostaneet käyttöoikeuksia. Näille asiakkaalle ei ole lisensointisiirtoa. Human Resourcesille määritettyä ylimääräistä eristysvarastointiyksikköä (SKU) ei enää sovelleta. Sen sijaan asiakkaat voivat ostaa taloushallinnon ja toimintojen sovellusten Tason 2 eristysympäristön hieman halvemmalla. Nykyiset asiakkaat, jotka ovat ostaneet Human Resources -eristysympäristön, siirretään taloushallinnon ja toimintojen sovellusten Taso 2 -eristysympäristöön ilman lisäkustannuksia.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Organisaation käyttää henkilöstöhallintomoduulia Dynamics 365 Financessa, Supply Chain Managementissa, Commercessa tai Project Operationsissa. Muuttuvatko lisensointini tai kustannukseni?

Dynamics 365 -sovellusten nykyiset käyttäjät ja itsenäisen Dynamics 365 Financen, Supply Chain Managementin, Commercen ja Project Operationsin käyttäjät voivat käyttää Human Resourcesia osana kyseisiä lisenssejä helmikuuhun 2025 asti tai nykyisen käyttöoikeussopimuksen päättymiseen saakka sen mukaan, kumpi ajankohta on aikaisempi. Voit siirtyä Human Resources -lisensseihin aikaisemmin, jos se auttaa sinua saavuttamaan parempia kustannussäästöjä. Helmikuusta 2025 alkaen kaikkien nykyisten CSP- ja EA-asiakkaiden on otettava HR-moduuli käyttöön ja ostettava Human Resources -lisenssit hyödyntääkseen taloushallinnon ja toimintojen sovelluksiin tuotavat uudet ominaisuudet.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Organisaationi käyttää Dynamics 365 Financea, Supply Chain Managementia, Commercea tai Project Operationsia tuotantokäytössä. Vaaditaanko meidän ostavan lisäympäristön infrastruktuurin yhdistämisen tueksi?

Infrastruktuurin muutoksen tueksi ei tarvita lisäympäristöjä.

