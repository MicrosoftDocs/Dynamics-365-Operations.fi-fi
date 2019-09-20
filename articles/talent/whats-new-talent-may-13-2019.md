---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (13. toukokuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ffeeb3e2f5279a84c4c060b04fe46836b778f6c5
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856445"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (13. toukokuuta 2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="coming-soon-in-attract"></a>Tulossa pian Attractiin

### <a name="job-approvals-on-home-page"></a>Työn hyväksynnät kotisivulla

Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa. Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät. Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.

## <a name="changes-in-onboard"></a>Onboardin muutokset

Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboardin ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset

Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2297. Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

### <a name="indicate-instance-type-when-provisioning-talent"></a>Määritä esiintymätyyppi, kun Talentia valmistellaan

Uuden Talent-esiintymän valmistelun yhteydessä voit määrittää, onko esiintymän tyyppi **Tuotanto** vai **Eristys**, mikä mahdollistaa uusien ominaisuuksien varhaisen testaamisen. Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin. Jos haluat, että jokin olemassa olevista instansseista päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [Tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service mukautettujen kenttien yksikkötuki

Tämän viikon versiossa seuraavat Common Data Service entiteetit tukevat nyt mukautettuja kenttiä: Työllisyys, etuuden laskentataajuus, etuuden laskenta, työlomakalenteri ja tunnustyypit.

### <a name="common-data-service-integration-page"></a>Common Data Service -integrointisivu

Tämä versio sisältää **Järjestelmänhallinnan > Linkkien > Integroinnin > Common Data Service -määrityksen** uuden vaihtoehdon. **Common Data Service** -vaihtoehdon avulla järjestelmänvalvoja tai tietojen hallinnan järjestelmänvalvoja voi tehdä joustavuutta ja oivalluksia Common Data Servicessä. Tämän vaihtoehdon voit ottaa käyttöön tai poistaa Common Data Service -integroinnissa Talent-esiintymässä ja tarkastella synkronoinnin tietoja Talent-instanssin ja Common Data Servicen välillä.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Tuo suorituskykytiedot lopullisen työntekijäluokituksen kanssa (316710)

Tässä versiossa voit tuoda aiempia työntekijän luokitustietoja. **FinalEmployeeRatingId**-kentällä on nyt kirjoitusoikeus.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Ei voi luoda työntekijän Common Data Service -osoitetta ja synkronoida sitä Talentin (317555) kanssa

Tämä muutos sallii Common Data Service -järjestelmään luotujen osoitetietojen synkronoinnin Talentin kanssa.

## <a name="in-preview"></a>Esiversiossa

### <a name="new-page-to-validate-position-hierarchy-data"></a>Uusi sivu sijaintihierarkian tietojen tarkistamista varten

Henkilöstöhallinto (HR) ja järjestelmänvalvojat voivat vahvistaa johtamishierarkian mahdollisesti vahingossa tuotuja kehäviittauksia varten. Voit käyttää tätä uutta sivua kohdasta **Organisaation hallinta > Linkit > Tehtävät > Tehtävähierarkian oikeellisuustarkistus**.

### <a name="specify-reason-codes-on-leave-types"></a>Määritä lomatyyppien syykoodit

Organisaatiot saattavat vaatia lisätietoja, jotka liittyvät lomapyyntöihin. Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Vaadi syykoodeja määrätyille poissaolopyyntöjen lomatyypeille

Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaolopyyntöjä. Tämä vaatimus voi olla olemassa yrityksen käytäntöjen tai lakisääteisten vaatimusten vuoksi. Voit määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot

Mahdollisuus seurata työntekijöiden aikaa ja ymmärtää, kuinka aikaa lasketaan, ei ainoastaan auta henkilöstöresursseja vastaamaan työntekijäkysymyksiin, vaan myös auttaa varmistamaan työntekijöille tarkat aikakatkaisuehdotukset. Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt), jolloin henkilöstöhallinto voi nähdä poissaolosaldon syyt.
