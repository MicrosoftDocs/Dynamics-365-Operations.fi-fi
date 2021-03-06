---
title: Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 30, 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2539baba84bffeb21d351cc307191eea3e940515
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528192"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 30, 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2270. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="provide-feedback"></a>Anna palautetta

Palautteen antamista koskeva vaihtoehto sijaitsee Talentin **Ohje**-valikossa (**?**). Tämän valikon avulla voit käyttää seuraavia resursseja:

- Palaute
- Ohje
- Aloittaminen
- Tuki
- Ideoita
- Tietoja

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Työntekijöiden kaksoiskappaleen tunnistuksen käyttöliittymän parannukset

Tämän muutoksen vuoksi kaksoiskappaleita havaitaan nyt, kun määrität nimikenttiä, ja tilailmaisimessa näkyy havaittujen kaksoiskappaleiden määrä. Linkki, joka on käytettävissä, avaa sivun, jossa voit arvioida, käytetäänkö joitakin kaksoiskappaleita. Tietojen syöttämisen keskeyttämisen välttämiseksi kaksoiskappalesivu ei avaudu automaattisesti. Sivun avauslinkki on valittava.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service mukautettujen kenttien yksikkötuki

Tämän viikon versiossa seuraavat entiteetit tukevat nyt mukautettuja kenttiä: työsuhde, etuustyyppi ja maksusykli.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Virhe ilmenee, kun käytöstä poistamisen tarkistusluettelo on määritetty (299877)

Tämä muutos korjaa virhesanoman, joka tulee näkyviin, kun määrität offboarding-tarkistusluettelon irtisanomisprosessin ulkopuoliselle työntekijälle.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Poistunut työntekijät-linkki avaa väärän työntekijän (309939)

Tämä muutos korjaa ongelman, joka ilmenee, kun työntekijä palkataan uudelleen toisesta yrityksestä ja kun työntekijä yritetään siirtää lähtenyt työntekijä -luettelosta.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Työntekijän itsepalvelun kompensaatiokortissa ei näy yhteenvetoarvoja, kun lisäsuojaus on käytössä (315231)

Tämä muutos korjaa ongelman, joka ilmenee, kun käytät lisäkompensaatiosuojausta. Kun lisäsuojaus on otettu käyttöön, työntekijän itsepalvelu näyttää nyt sekä työntekijöiden että esimiesten kompensaatiosummien yhteenvedon. Ennen tätä muutosta yhteenvetoarvot näkyivät nollana.

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Jos sijainti Common Data Servicessä, jossa ei ole otsikkoa, luodaan, Talent (314562) -asemaa ei luoda

Tämän viikon muutokset korjaavat ongelman, joka ilmenee, kun luot tehtäviä Common Data Servicessä, mutta et anna otsikkoa.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Työntekijän itsepalvelun suorituskyky kirjauskansion merkintöjen virhesanoma (314134)

Tämä muutos korjaa ongelman, joka ilmenee, kun suorituskykytavoitteet liitetään työntekijän itsepalvelun suorituskykykirjauskansiomerkintöihin.

## <a name="in-preview"></a>Esiversiossa

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Syykoodit on määritettävä lomatyyppien avulla.

Organisaatiot saattavat vaatia lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vaadi syykoodeja määrätyille poissaolopyyntöjen lomatyypeille

Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaolopyyntöjä. Tämä vaatimus voi olla olemassa yrityksen käytäntöjen tai lakisääteisten vaatimusten vuoksi. Voit nyt määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot

Mahdollisuus seurata työntekijöiden aikaa ja ymmärtää, kuinka aikaa lasketaan, ei ainoastaan auta henkilöstöresursseja vastaamaan työntekijäkysymyksiin, vaan myös auttaa takaamaan työntekijöille tarkat aikakatkaisuehdotukset. Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt), jolloin henkilöstöhallinto voi nähdä saldon syyt.

## <a name="coming-soon"></a>Tulossa pian

### <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille

Finance and Operationsin Platform update 26 -päivityksen jälkeen käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät sähköposti-ilmoitukset automaattisesti yhteyshenkilöille, kun tapahtuma käynnistää ilmoitukset.


[!INCLUDE[footer-include](../includes/footer-banner.md)]