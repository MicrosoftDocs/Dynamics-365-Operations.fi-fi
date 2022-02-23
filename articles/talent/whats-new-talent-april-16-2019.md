---
title: Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 16, 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d9802848c90b2b1c8d5e3cb3280dfa6ebc948ff2
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527172"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 16, 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="process-auditing"></a>Prosessin valvonta

Voit nyt jäljittää ehdokkaisiin, avoimiin työpaikkoihin ja työsovelluksiin tehtyjä muutoksia. Lisätietoja on kohdassa [Rekrytointitietojen muutosten seuraaminen](process-auditing.md).

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2239. Suluissa olevat luvut viittaavat tukinumeroihin Lifecycle Services (LCS) -palveluissa.

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Kompensaatioalue, kompensaatiotaso, edunvaihtoehto ja osaamisaluetyypin Common Data Service -entiteetit, jotka on päivitetty sisältämään asiakaskentän tuen

Tässä julkaisussa nämä Common Data Service -entiteetit on päivitetty sisältämään mahdollisuuden sisällyttää mukautettu kenttä, joka on lisätty Talent: Core HR:n kautta.

### <a name="powerbi-refresh-issues-314342"></a>PowerBI-päivitysongelmat (314342)

Tämä muutos korjaa ongelman, jossa PowerBI-raportit päivitetään oikein.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>Työntekijän itsepalvelun siirtymätehtävien kautta ei voi napsauttaa suoraan (303309)

Tämän muutoksen ansiosta käyttäjät, joilla on työntekijän rooli, voivat valita ja päivittää siirtotehtävät Talentin tehtäväluettelosta.

### <a name="performance-feedback-email-message-updated-309615"></a>Suorituspalautesähköpostiviesti päivitetty (309615)

Tämän muutoksen yhteydessä näkyviin tulee vahvistussanoma, kun palaute on lähetetty onnistuneesti.

### <a name="missing-tables-in-word-template-308048"></a>Puuttuvat taulukot Word-mallissa (308048)

Tämän muutoksen yhteydessä, kun luot Word-mallin, jossa on työntekijöiden ja osaamisalueiden tietoja, vain valitun työntekijän osaamisalueet näkyvät Word-asiakirjassa.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>Offboarding-tarkistusluetteloa käytettäessä näyttöön tulee virhesanoma. (299877)

Tämä muutos korjaa ongelman, kun offboarding-tarkistusluetteloa käytetään suoraan työntekijälomakkeesta.

## <a name="in-preview"></a>Esiversiossa

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Syykoodit on määritettävä lomatyyppien avulla.

Organisaatiot saattavat tarvita lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Vaadi syykoodeja tietyille poissaolopyyntöjen lomatyypeille

Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät lähettävät aikaa. Syynä voi olla yrityksen käytäntö tai säännöstenmukaisuuden vaatimuksia. Voit nyt määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot

Työntekijöiden aikaa jäljittää ja ymmärtää, miten loma-aika lasketaan, ei ainoastaan auta henkilöstöä vastaamaan työntekijäkysymyksiin, vaan myös varmistavat työntekijöille tarkat aikapalkinnot. Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt) nähdäksesi saldon syyt.

## <a name="coming-soon"></a>Tulossa pian

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Työntekijöiden kaksoiskappaleen tarkistuksen käyttöliittymän parannukset

Tällä muutoksella tunnistetaan duplikaatit, kun syötät nimikenttiä, ja tila näyttää löytyneiden kopioiden määrän. Voit valita uuden sivun sisältävän linkin arvioidaksesi, käytetäänkö tunnistettua vastausta. Tietojen syöttämisen keskeyttämisen välttämiseksi kaksoiskappale ei avaudu automaattisesti.

### <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille

Finance and Operationsin Platform update 25:n avulla käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät automaattisesti sähköpostiviestejä yhteystietoihin, kun tapahtuma käynnistyy.


