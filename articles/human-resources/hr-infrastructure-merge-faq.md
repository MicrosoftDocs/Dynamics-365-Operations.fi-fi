---
title: Dynamics 365 Human Resources -infrastruktuurin yhdistämisen usein kysytyt kysymykset
description: Tässä artikkelissa vastataan usein kysyttyihin kysymyksiin Microsoft Dynamics 365 Human Resourcesin sekä talous- ja toimintosovellusten infrastruktuurin yhdistämisestä.
author: twheeloc
ms.date: 11/15/2022
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
ms.openlocfilehash: 7325231718d7387450391b16b2866f9a2c05bdc4
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779632"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources -infrastruktuurin yhdistämisen usein kysytyt kysymykset

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Mikä on Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources sisältää työkaluja, joiden avulla HR-tiimit parantavat organisaation ketteryyttä, uudistavat työntekijäkokemuksen ja optimoivat HR-ohjelmat sekä luovat tällä tavoin työpaikan, jossa ihmiset ja liiketoiminta kukoistavat. Lisätietoja Dynamics 365 Human Resourcesissa on kohdassa [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Työntekijäkokemusten uudistaminen.** Tehokkaimmat työntekijät säilytetään tukemalla esihenkilöitä ja työntekijöitä yhdistettyjen osallistamista ja kasvua edistävillä itsepalvelukokemuksilla.
- **HR-ohjelmien optimointi.** Operatiiviset kustannusten pienentäminen sekä ihmiskeskeisten lomien ja poissaolojen, työajan, etuuksien sekä kompensaation hallintaohjelmien luominen.
- **Organisaation ketteryyden lisääminen.** Henkilöstöhallinto voi toimia ketterästi liiketoiminnan sitä edellyttäessä käyttämällä Dataversea ja Microsoft Power Platformia keskittämään ihmisiä koskevat tiedot sekä laajentamaan kätevästi Dynamics 365 Human Resourcesia.
- **Työvoimaa koskevien merkityksellisten tietojen löytäminen.** Tietopohjaisia päätökset voivat perustua ihmisiä koskevien tietojen analysointiin ja visualisointiin monipuolisissa koontinäytöissä, joita voi kaikenlaisissa laitteissa.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktuurin yhdistämisen arvo ja hyödyt

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Mikä on Dynamics 365 Human Resources -infrastruktuurin yhdistäminen?

Tällä hetkellä on käytössä kahdet eri HR-ominaisuudet kahdessa eri Dynamics 365 -infrastruktuurissa:

- **Dynamics 365 Human Resources** – Erillinen sovellus, joka suoritetaan itsenäisessä infrastruktuurissa. Kun tämä sovellus julkaistiin, infrastruktuuri oli erillään muista Dynamics 365 -toimintosovelluksista. Asiakkaat parantavat tämän sovelluksen avulla organisaation ketteryyttä, optimoivat HR-ohjelmia, uudistavat työntekijäkokemuksia ja hankkivat työvoimaa koskevia merkityksellisiä tietoja.
- **HR-moduuli** – Vanha ominaisuusjoukko, joka oli aiemmin Unified Operations -käyttöoikeuksien SKU:n (varastointiyksikön) osa. HR-moduuli suoritetaan talous- ja toimintosovellusinfrastruktuurissa, joka on sama kaikissa toimintosovelluksissa. Näitä sovelluksia ovat esimerkiksi Dynamics 365 Finance, Dynamics 365 Project Operations ja Dynamics 365 Supply Chain Management. Asiakkaat saavat HR-ominaisuudet Dynamics 365 Financen tai Dynamics 365 Supply Chain Managementin osana.

Microsoft ei ole lisännyt uusia ominaisuuksia tai parannuksia HR-moduuliin kolmen viimeisen vuoden aikana. Suunnittelut panostukset on sen sijaan keskitetty Dynamics 365 Human Resources -sovellukseen.

Näiden kahden ominaisuusjoukon tuominen samaan infrastruktuuriin tuo asiakkaille seuraavat edut:

- Dynamics 365 Human Resourcesin kuluneen kolmen vuoden aikana lisätyt parannukset, kuten parannettu loma- ja poissaolotoiminto, etuuksien hallinta ja raportointi.
- Parannettu laajennettavuus Microsoft Power Platformin kautta ja mahdollisuus mukauttaa sivuja liiketoimintalogiikkaa laajentamalla.
- Käyttöönoton, päivitysten ja ylläpidon parannukset ovat yhdenmukaisia esimerkiksi sovelluksen elinkaaren hallinnan (ALM), elinkaaripalvelujen ja maantieteellisen saatavuuden osalta.
- Teknologiset innovaatiot, joita syntyy suunnittelijoiden käyttäessä jaettuja palveluja ja työkaluja, minkä lisäksi ympäristökustannukset pienenevät.

Tämä siirtymän vaikuttaa asiakkaisiin, jotka ovat tällä hetkellä Dynamics 365 Human Resourcesin tai vanhan HR-moduulin käyttäjiä.

## <a name="glossary-of-terms-used-in-this-faq"></a>Näissä usein kysytyissä kysymyksissä käytetyt termit

- **Dynamics 365 Human Resources** – nykyinen ja tuleva tuote tarjoaa HR-ominaisuuksia markkinoille.
- **HR-moduuli** – Vanha ominaisuusjoukko, jonka käyttöoikeus liittyi aiemmin Unified Operations -tuotteisiin. Ominaisuudet otetaan käyttöön, kun asiakas omistaa Dynamics 365 Financen tai Dynamics 365 Supply Chain Managementin.
- **Talous- ja toimintosovellusinfrastruktuuri** – Kehitysarkkitehtuuri, jota toimintotuotteet, mukaan lukien Dynamics 365 Finance, Dynamics 365 Supply Chain Management ja Dynamics 365 Project Operations, käyttävät. Tätä infrastruktuuria käytetään jatkossa. Näissä usein kysytyissä kysymyksissä *yhdistetty arkkitehtuuri* viittaa talous- ja toimintosovellusympäristöön.
- **Human Resources -infrastruktuuri** – Kehitysarkkitehtuuri, jota historiallisesti käytettiin Dynamics 365 Human Resources -sovelluksessa. Infrastruktuurin yhdistämisprojekti tuo Dynamics 365 Human Resourcesin talous- ja toimintosovellusinfrastruktuuriin. Erillisen infrastruktuuri käyttö lopetetaan.

## <a name="general-questions-about-the-infrastructure-merge"></a>Yleisiä infrastruktuurin yhdistämistä koskevia kysymyksiä

### <a name="will-customers-lose-any-features-or-capabilities"></a>Menettävätkö asiakkaat toimintoja tai ominaisuuksia?

Tavoitteena on pitää tämän siirtymän vaikutus asiakkaisiin mahdollisimman vähäisenä. Toimintoja tai ominaisuuksia ei poisteta. Dynamics 365 Human Resourcesin ja HR-moduulin välillä tulee olemaan toiminnallinen pariteetti. Jos toiminto on molemmissa infrastruktuureissa, käytetään Dynamics 365 Human Resources -kokemusta.

### <a name="will-the-user-experience-change"></a>Muuttuuko käyttökokemus?

Käyttökokemus on yhdenmukainen Dynamics 365 -ympäristön vakiokokemuksen kanssa. Vaikka koontinäytön ja valikoiden yleinen käyttökokemus pysyy samankaltaisena, se yhdenmukaistetaan Dynamics 365 Finance -sovelluksen vakiokokemuksen kanssa. Siirtyminen sisältää kummankin moduulit ja työtilat sekä sallii muun muassa suosikkien käytön. Dynamics 365 Human Resources -työtilat, kuten **Henkilöstön hallinta** ja **Ihmiset**, yhdistetään talous- ja toimintosovellusinfrastruktuuriin. Jatkossa uudet ominaisuudet toimitetaan ominaisuuksien hallinnan kautta, joten asiakkaat voivat tarkastella uusia ominaisuuksia ja päättää, mitä niistä halutaan käyttää. Lisätietoja on kohdissa [Ominaisuuksien hallinnan yleiskatsaus](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja [Käyttöliittymän ohjeet](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Milloin Dynamics 365 Human Resourcesin infrastruktuurin yhdistäminen on valmis?

Infrastruktuurin yhdistäminen otetaan käyttöön vaiheittain, jotta asiakkaille jää aikaa suunnitteluun ja tarvittavien vaiheiden suorittamiseen. Ominaisuuksien käyttöönotto aloitettiin Dynamicsin vuoden 2021 2. julkaisuaallossa. Tämän projektin kaiken tuotekehityksen on tarkoitus valmistua vuoden 2022 2. julkaisuaallon päättyessä. On kuitenkin huomattava, että nämä ajankohdat voivat muuttua. Ajantasaisimmat tiedot kannattaa tarkistaa [julkaisusuunnitelmista](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Mitä infrastruktuurin yhdistämiseen liittyvää koulutusta ja resursseja on saatavana?

Käyttöön tulee ohjeita, jossa käsitellään infrastruktuurin yhdistämisprosessin kukin vaihe yksityiskohtaisesti. Käyttöön tulee tarpeen mukaan myös muita sellaisia koulutusresursseja, kuten videoita ja työpajoja, jotka auttavat sujuvoittamaan asiakkaiden ja kumppaneiden siirtymisprosessia.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Onko kehitysominaisuuksissa muutoksia infrastruktuurin yhdistämisen valmistuttua?

Lisätietoja kehitysominaisuuksista on kohdassa [Kehittämisen ja mukauttamisen aloitussivu](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Ominaisuuksien saatavuutta koskevat kysymykset

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Toimiiko LinkedIn Talent Hub -integrointi talous- ja toimintosovellusinfrastruktuurissa?

Ei. LinkedIn Talent Hub -integrointi ei ole osa yhdistettyä infrastruktuuria. Julkisia ohjelmointirajapintoja on saatavana integrointien muodostamiseen rekrytointi- ja hakijoiden seurantaratkaisujen kanssa. Asiakkaat, joiden tarkoituksena on käyttää LinkedIn Talent Hubia, on tehtävä integroinnin osalta yhteistyötä Microsoft-kumppanien kanssa ja hyödynnettävä annettuja ohjelmointirajapintoja. Lisätietoja hakijoiden seurantajärjestelmän (ATS) integroinnin ohjelmointirajapinnoista on kohdassa [Hakijan seurantajärjestelmän integroinnin ohjelmointirajapinnan esittely](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Ovatko tällä hetkellä vain Dynamics 365 Human Resourcesissa saatavana olevat ominaisuudet (kuten lomien hallinta ja etuuksien hallinta) saatava yhdistymisen valmistumisen jälkeen?

Kyllä. Kaikki Dynamics 365 Human Resources -sovelluksen ominaisuudet tuodaan talous- ja toimintosovellusinfrastruktuuriin. Ominaisuudet tulevat saataville vaiheittain. Ajantasaiset tiedot yhdistetyn infrastruktuurin ominaisuuden saatavuudesta kannattaa tarkistaa säännöllisesti [julkaisusuunnitelmista](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Ovatko Ceridianin Dynamics 365 Human Resources -integroinnit saatavana infrastruktuurin yhdistämisen valmistumisen jälkeen?

Ceridian on luomassa palkanlaskennan ohjelmointirajapintoja hyödyntävää V2-integrointia Dynamics 365 Human Resourcesin kanssa. Dynamics 365 Human Resourcesin nykyistä tiedostopohjaista integrointia ei siirretä talous- ja toimintosovellusinfrastruktuuriin. Lisätietoja on kohdassa [Johdanto palkanlaskennan ohjelmistorajapintaan](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Sisällytetäänkö työntekijätoiminnon hakijan seuranta- taikka perehdyttämis- tai työsuhteen päättymisominaisuudet?

Aiemmin julkaisuissa on luotiin ATS-integraation ohjelmointirajapinta, jonka avulla kumppanit ja asiakkaat voivat luoda ATS-integrointeja Human Resourcesiin. ATS-järjestelmään liittyvä lisätoiminto tuli saatavilla vuoden 2022 1. aallossa. Näitä ohjelmointirajapintoja parannetaan myös tulevissa julkaisuissa.

Talous- ja toimintosovellusinfrastruktuurissa tällä hetkellä oleva HR-toiminto sisältää joitakin rekrytoinnin hallintatoimintoja, joita ei ole Dynamics 365 Human Resourcesissa. Infrastruktuurin yhdistymisen valmistumisen jälkeen tämä toiminto on kaikkien Human Resources -asiakkaiden käytettävissä. Tämä toiminto ATS-toiminnon kevytversio. Tätä toiminnon laajentamista tulevaisuudessa ei kuitenkaan suunnitella. Asiakkaat, jotka tarvitset laajennetun toiminnon, voivat hyödyntää kumppanin ATS-integrointeja. Lisätietoja ATS-integroinnin ohjelmointirajapinnoista on kohdassa [Hakijan seurantajärjestelmän integroinnin ohjelmointirajapinnan esittely](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Käytetäänkö Dynamics AX 2012 -päivitystyökaluja päivittämään AX 2012:n HR-moduuli Dynamics 365 Human Resources -sovellukseen?

Kyllä. Dynamics AX 2012 päivitetään Dynamics 365 Human Resourcesiin noudattamalla samaa päivityspolkua ja käyttämällä samoja työkaluja, joita käytettiin päivittämiseen muiden Dynamics 365 -toimintosovellusten, kuten Dynamics 365 Financen tai Dynamics 365 Supply Chain Managementin, uusimpaan versioon.

Lisätietoja siirtymisestä talous- ja toimintosovellusinfrastruktuuriin on kohdassa [Human Resource -asiakkaiden siirtymistä koskevat usein kysytyt kysymykset](./customer-migration.md).
