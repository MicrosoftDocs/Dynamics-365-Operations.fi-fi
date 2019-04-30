---
title: Dynamics 365 for Talent -sovelluksen uudet tai muuttuneet ominaisuudet (2.4.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8f488b0bf844fc04f07fedfa447073cdeabacc15
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/12/2019
ms.locfileid: "954128"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-2-2019"></a>Dynamics 365 for Talent -sovelluksen uudet tai muuttuneet ominaisuudet (2.4.2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset

### <a name="approval-emails-in-attract"></a>Attractin hyväksyntä sähköpostiviestit
Uudet hyväksynnän sähköpostiviestit parantavat näkyvyyttä hyväksyntäprosessiin. Sähköpostiviestit lähetetään hyväksyjille seuraavissa tilanteissa:

- Pyytäjä lähettää työn hyväksyttäväksi.
- Työ on joko hylätty tai hyväksytty.
- Hyväksyjä ei ole ratkaisuut hyväksynnän pyyntöä 24 tunnin aikana.

Voit mukauttaa hyväksynnän sähköpostiviestien sisältöä uusien mallien avulla.

### <a name="application-and-profile-attachments"></a>Hakemuksen ja profiilin liitteet
**Asiakirjat**-välilehden parannukset hakemuksissa ja kykypoolin profiileissa näyttävät nyt sekä tiedostonimen että -tyypin.

## <a name="changes-in-onboard"></a>Onboardin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboardin ohjelmakorjauksia.

## <a name="coming-soon-attract-and-onboard"></a>Tulossa (Attract ja Onboard)

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Servicesin (LCS) integrointi ongelman raportoinnin kanssa
Attractissa ja Onboardissa loppukäyttäjien kirjaamat ongelmat Ilmoita ongelmasta -ominaisuuden kautta luovat nyt automaattisesti tukitapauksen asiakkaan LCS projektissa. Järjestelmänvalvojat voivat sitten tarkistaa ongelmat ja lähettää ne Microsoftille tarpeen mukaan. Tämä vastaa sitä, miten Core HR käsittelee loppukäyttäjän tukitapauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2216.

### <a name="platform-update-25"></a>Ympäristön update 25 -päivitys
Lisätietoja Platform update 25:stä on artikkelissa [Dynamics 365 for Finance and Operations platform update 25:n esiversio-ominaisuudet (huhtikuu 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Kompensaation lisäsuojaus (kiinteä ja muuttuva)
Monissa yrityksissä etuuspäälliköillä on ehkä vain määrättyjen kompensaatiotietueiden käyttöoikeus. Ne voivat olla johtajien tai alueellisten työntekijöiden tietueita. Tämä muutoksen ansiosta henkilöstöhallinto voi hallita ja ylläpitää organisaation erilaisten työntekijäryhmien kompensaatiosuunnitelmia. Voit määrittää käyttöoikeusrooleja kiinteille ja muuttuville suunnitelmille. Nämä käyttöoikeusroolit määrittävät käyttöoikeudet suunnitelmiin ja liittyviin työntekijätietoihin, kuten palkan tai bonuksen tietueisiin, jotta vain nämä roolit voivat käsitellä työntekijäryhmien kompensaatioita.

### <a name="upgrade-to-common-data-service"></a>Päivitä Common Data Serviceen
Common Data Serviceen päivityksen määräajat lähestyvät nopeasti. Kirjaudu PowerApps-hallintakeskukseen ja tarkista, onko tietokanta päivitettävä. Lisätietoja määräajoista ja päivityksen vaiheista on kohdassa [Päivittäminen Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Esiversiossa

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Syykoodit on määritettävä lomatyyppien avulla.
Organisaatiot saattavat tarvita lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Vaadi syykoodeja tietyille poissaolopyyntöjen lomatyypeille
Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaoloja. Syynä voi olla yrityksen käytäntö tai säännöstenmukaisuuden vaatimuksia. Voit nyt määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

## <a name="coming-soon"></a>Tulossa pian

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Työntekijöiden kaksoiskappaleen tarkistuksen käyttöliittymän parannukset
Tällä muutoksella tunnistetaan duplikaatit, kun syötät nimikenttiä, ja tila näyttää löytyneiden kopioiden määrän. Voit valita uuden sivun sisältävän linkin arvioidaksesi, käytetäänkö tunnistettua vastausta. Tietojen syöttämisen keskeyttämisen välttämiseksi kaksoiskappale ei avaudu automaattisesti.

###  <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille
Platform update 25:n avulla käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät automaattisesti sähköpostiviestejä yhteystietoihin, kun tapahtuma käynnistyy. 
