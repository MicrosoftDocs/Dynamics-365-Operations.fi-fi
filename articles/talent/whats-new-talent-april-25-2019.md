---
title: Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 23, 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a70be88e3ab65bb0bdd844347e8ba69e4ba61a5
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024111"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Dynamics 365 Talent -sovelluksen uudet tai muuttuneet ominaisuudet (huhtikuun 23, 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2253. Suluissa olevat luvut viittaavat tukinumeroihin Lifecycle Services (LCS) -palveluissa.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service mukautettujen kenttien yksikkötuki
Tämän viikon julkaisun jälkeen seuraavat entiteetit tukevat mukautettuja kenttiä: kompensaatiotaso, edun vaihtoehto, osaamisaluetyyppi ja kompensaatioalueet.

### <a name="additional-odata-entities-302992"></a>Muut OData-entiteetit (302992)
OData tukee nyt seuraavia entiteettejä: työntekijän ammattikokemus ja työntekijöiden koulutus.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Esimiesten ja työntekijöiden suorituskyvyn kirjauskansioliitteet (308248)
Tämän version avulla sekä esimiehet että työntekijät voivat nyt käyttää liitteitä luotaessa ja päivitettäessä suorituskykykirjauskansion merkintöjä.

### <a name="employee-rehire-flag-always-available-310047"></a>Työntekijän uudelleenvuokrauksen lippu on aina käytettävissä (310047)
Työntekijän uudelleenvuokrausvaihtoehto on nyt käytettävissä päivitysprosessin ulkopuolella. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>**Oman maksutavan** nimeä ei voi muuttaa (308815)
Mukauttaminen on otettu käyttöön, jotta **Oma maksutapa** -otsikko voidaan muuttaa työntekijän itsepalvelussa.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Taloushallinnon dimensioita toimea vasten ei voi poistaa (293908)
Taloushallinnon dimensiot voidaan nyt poistaa, kun ne pyytävät muutosta olemassa olevaan toimeen ja taloushallinnon dimensiot ylittävät yrityksen rajat. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Asiakas ei voi julkaista tietoja takaisin Talentiin, kun tiedot avataan Excelistä (302955)
Tämä muutos korjaa julkaisuongelman käytettäessä liittyviä tauluja.

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
## <a name="known-issues"></a>Tunnetut ongelmat

### <a name="email-support-for-alerts"></a>Sähköpostituki hälytyksille
Finance and Operations -käyttöympäristöpäivitys 26:n avulla käyttäjät voivat luoda hälytyssääntöjä, jotka lähettävät automaattisesti sähköposti-ilmoituksia yhteyshenkilöille, kun tapahtuma käynnistyy.
