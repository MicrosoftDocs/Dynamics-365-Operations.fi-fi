---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (28. toukokuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c99e0f3637a8d958e31a046eaad6faa57ce3e1e7
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856278"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-28-2019"></a>Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (28. toukokuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="coming-soon-in-attract"></a>Tulossa pian Attractiin

### <a name="job-approvals-on-home-page"></a>Työn hyväksynnät kotisivulla

Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa. Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät. Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.

## <a name="changes-in-onboard"></a>Onboardin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboardin ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2319.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service mukautettujen kenttien yksikkötuki

Tässä versiossa seuraavat Common Data Service -entiteetit tukevat nyt mukautettuja kenttiä: etulaskurin yksityiskohdat, työkalenterin lomarivi ja työsuhde.

### <a name="copy-position-now-includes-payroll-details"></a>Kopioi sijainti sisältää nyt palkanlaskennan tiedot
Kun käytät **Kopioi sijainti** -toimintoa ja valitset kaikki vaihtoehdot, palkanlaskennan tiedot sisältyvät kopiotietoihin. 

## <a name="in-preview-in-core-hr"></a>Esikatselussa Core HR:ssä

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Rajoita lomatyyppejä vapaapyynnöissä

Organisaatiot voivat tarjota työntekijöille useita erilaisia vapaatyyppejä. Jotkin näistä vapaatyypeistä eivät ehkä sovi työntekijöiden syöttämään vapaaseen ja niitä hallitaan henkilöstöhallinnon (HR) avulla. Tämän version avulla voit määrittää, mitä vapaatyyppejä varten työntekijät voivat lähettää pyyntöjä. 

### <a name="new-page-to-validate-position-hierarchy-data"></a>Uusi sivu sijaintihierarkian tietojen tarkistamista varten

HR ja järjestelmänvalvojat voivat vahvistaa johtamishierarkian mahdollisesti vahingossa tuotuja kehäviittauksia varten. Voit käyttää tätä uutta sivua kohdasta **Organisaation hallinta > Linkit > Tehtävät > Tehtävähierarkian oikeellisuustarkistus**.

### <a name="specify-reason-codes-on-leave-types"></a>Määritä lomatyyppien syykoodit

Organisaatiot saattavat vaatia lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vaadi syykoodeja määrätyille poissaolopyyntöjen lomatyypeille

Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaolopyyntöjä. Tämä vaatimus voi olla olemassa yrityksen käytäntöjen tai lakisääteisten vaatimusten vuoksi. Voit määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot

Mahdollisuus seurata työntekijöiden aikaa ja ymmärtää, kuinka aikaa lasketaan, ei ainoastaan auta henkilöstöresursseja vastaamaan työntekijäkysymyksiin, vaan myös auttaa varmistamaan työntekijöille tarkat aikakatkaisuehdotukset. Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt), jolloin henkilöstöhallinto voi nähdä poissaolosaldon syyt.
