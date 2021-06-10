---
title: Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin hakijan seurantajärjestelmän (ATS) integraation API.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c043ac9c19a810d1718f0d4907cd5e9d651d778f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055289"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin hakijan seurantajärjestelmän (ATS) integraation API. API-liittymän tarkoituksena on ottaa käyttöön tehokkaat integroinnit Dynamics 365 Human Resourcesin ja ATS-kumppanisovellusten välillä.

![ATS-integroinnin työnkulku](media/hr-admin-integration-ats-api-introduction-flow.png)

Integroitu kokemus alkaa Human Resourcesista, kun työhönottopäällikkö luo työhönottopyynnön. Kun pyyntö aktivoidaan, ATS tuo työhönottoprojektin luontipyynnön tiedot. Tämän jälkeen rekrytointiputken avulla voit valita ja palkata hakijan toimia varten. Lopuksi ATS suorittaa integraaton takaisin lähettämällä valitun hakijan tietueen Human Resourcesiin. Tämän jälkeen hakijatietue voi luoda työntekijätietueen käymällä läpi lisää rekorytoinnin oikeellisuustarkistuksia ja työnkulkuja.

Integroinnin mahdollistamiseksi Human Resources on lisännyt seuraavat komponentit:

1.  Työhönottopyynnön luontitoiminto.
2.  Laajennettu hakijan profiili ja liittyvät työnkulut.
3.  Integroinnin API-sovellusliittymä, joka avaa uudet toiminnot integroiduille sovelluksille.

Lisätietoja työhönottopyynnön ja hakijan toimintojen määrittämisestä ja käyttämisestä on kohdassa [Ehdokkaiden työhönotto](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Tämä sovellusliittymä perustuu Microsoft Dataverseen (aiemmin Common Data Service). Kaikki RESTful-vuorovaikutus tämän sovellusliittymän kanssa tapahtuu ODataa käyttävän Microsoft Dataverse -verkkoliittymän kautta. Tämä sovellusliittymä on Dataverse-verkkoliittymän osajoukko. Dataverse-verkkoliittymä määrittää ominaisuuksia, kuten todennuksen, SLA-sopimukset, erän, samanaikaisuustarkistuksen ja virheiden käsittelyn.

Yleisiä tietoja Microsoft Dataverse -verkkoliittymästä:

- [Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse -verkkoliittymän käyttäminen](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataversen kehittäjäopas](/powerapps/developer/data-platform)

Yllä olevat dokumentaatiot sisältävät yksityiskohtaisia tietoja ja kehittäjän ohjeita Dataverse-verkkoliittymän käyttämisestä. Tällaisia ohjeita ovat esimerkiksi [todennuksen hallinta](/powerapps/developer/data-platform/webapi/authenticate-web-api), [toimintojen suorittaminen](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postmanin käyttäminen API:n kanssa](/powerapps/developer/data-platform/webapi/use-postman-web-api) sekä [muutosseurannan tai delta-tunnusten käyttäminen](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) liittymän avulla.

### <a name="option-sets"></a>Asetusjoukot

Tässä asiakirjassa kuvattu ATS-integroinnin API:n tietomalli sisältää asetusjoukot, joiden luettelo sisältää yksikön ominaisuuksiin liittyvät luetteloarvot. Lisätietoja asetusjoukkojen käyttämisestä Dataverse-verkkoliittymässä on kohdassa [Asetusjoukkojen luominen ja päivittäminen verkkoliittymän avulla](/powerapps/developer/data-platform/webapi/create-update-optionsets). Asetusjoukot määritetään kullekin Dataverse-ympäristölle.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Human Resourcesin virtuaalitaulut Dataversessa

ATS-integroinnin API:n päätepisteet käyttävät Microsoft Dataversen virtuaalitaulujen ominaisuuksia. Oletusarvon mukaan virtuaalitauluja ja niihin liittyviä API-päätepisteitä ei ole otettu käyttöön Human Resources -ympäristöissä, minkä ansiosta organisaatiot voivat määrittää, mitkä OData-päätepisteet julkistetaan ympäristölle. Jotta sovellusliittymää voidaan käyttää, Human Resourcesin yksiköiden virtuaalitaulut on luotava ympäristöä varten. 

Lisätietoja virtuaalitaulujen luomisesta liittymää varten on kohdassa [Dataverse-virtuaalitaulujen konfiguroiminen](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Tietomalli

Tietomalli on keskitetty kahden pääyksikön ympärille:

- **RecruitingRequest** edustaa pyyntöä ATS:lle, että rekrytoidaan yhteen tai useampaan avoinna olevaan toimeen. Esimerkkikysely on kohdassa [Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** esittää tietoja hakijasta, joka on hyväksynyt toimen tarjouksen. **Henkilö** edustaa hakijaa. Henkilöllä voi olla useita rooleja yrityksessä, kuten hakija, työntekijä tai alihankkija. Esimerkkikysely on kohdassa [Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Seuraava kaavio kuvaa suhteita API:n sisällä. Useilla tyypeillä on viiteavaimet muihin Human Resourcesin aiemmin luotuihin yksiköihin, joita ei ole kuvattu tässä. Tässä asiakirjassa on tietoja yksiköistä, jotka liittyvät erityisesti rekrytoinnnin integrointiskenaarioihin. Dataverse-verkkoliittymässä on kuitenkin useita muita yksiköitä Dynamics 365 Human Resourcesille, jotka voivat myös olla oleellisia integrointisi kannalta. Voit esimerkiksi tarvita yksityiskohtaisia tietoja myös työntekijöistä, töistä, toimista tai muista yksiköistä, joita ei ole määritetty tässä. Moniin näistä yksiköistä viitataan viiteavainsuhteissa tai siirtymisominaisuuksissa.

![ATS-integroinnin API-tietomalli](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Työhönottopyyntö ja siihen liittyvät entiteetit ja asetusjoukot

Esimerkkikysely: 

- [Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Yksiköt:

- [Työhönottopyyntö](hr-admin-integration-ats-api-recruiting-request.md)
- [Työhönottopyynnön toimi](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Työhönottopyynnön taito](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Työhönottopyynnön koulutus](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Työhönottopyynnön sijainti](hr-admin-integration-ats-api-recruiting-request-location.md)

Asetusjoukot:

- [Työn vapautustila](hr-admin-integration-ats-api-job-exempt-status.md)
- [Työhönottopyynnön toimen tila](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Työhönottopyynnön tila](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Säännösten mukainen tehtäväluokka](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Palkattava hakija ja siihen liittyvät yksiköt ja asetusjoukot

Esimerkkikysely:

- [Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Yksiköt:

- [Palkattava ehdokas](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Henkilö](hr-admin-integration-ats-api-person.md)
- [Henkilön koulutus](hr-admin-integration-ats-api-person-education.md)
- [Henkilön ammattikokemus](hr-admin-integration-ats-api-person-professional-experience.md)
- [Henkilön osoite](hr-admin-integration-ats-api-person-address.md)
- [Osapuolen yhteyshenkilö](hr-admin-integration-ats-api-party-contact.md)
- [Henkilön osaamisalue](hr-admin-integration-ats-api-person-skill.md)
- [Luokitustaso](hr-admin-integration-ats-api-rating-level.md)
- [Henkilön todistus](hr-admin-integration-ats-api-person-certificate.md)
- [Varmenteen tyyppi](hr-admin-integration-ats-api-certificate-type.md)
- [Henkilön seulonta](hr-admin-integration-ats-api-person-screening.md)
- [Seulontatyypit](hr-admin-integration-ats-api-screening-types.md)
- [Henkilön tunnusnumero](hr-admin-integration-ats-api-person-identification-number.md)

Asetusjoukot:

- [Hakijatoimintojen integraation tulos](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Tyhjä Kyllä Ei](hr-admin-integration-ats-api-blank-yes-no.md)
- [Valmistumisen tila](hr-admin-integration-ats-api-completion-status.md)
- [Yhteyshenkilötyyppi](hr-admin-integration-ats-api-contact-type.md)
- [Koulutuksen hyvitysperuste](hr-admin-integration-ats-api-education-credit-basis.md)
- [Sukupuoli](hr-admin-integration-ats-api-gender.md)
- [Siviilisääty](hr-admin-integration-ats-api-marital-status.md)
- [Vuoden kuukaudet](hr-admin-integration-ats-api-months-of-year.md)
- [Ei Kyllä](hr-admin-integration-ats-api-no-yes.md)
- [Kausiyksikkö](hr-admin-integration-ats-api-period-unit.md)
- [Seulonnan tiheys](hr-admin-integration-ats-api-screening-frequency.md)
- [Seulonnan tiheys luo kohteesta](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Osaamisaluetason tyyppi](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Lisätietoja

[Ehdokkaiden työhönotto](hr-personnel-recruit.md)<br>
[Mikä on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse -verkkoliittymän käyttäminen](/powerapps/developer/data-platform/webapi/overview)<br>
[Asetusjoukkojen luominen ja päivittäminen verkkoliittymän avulla](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]