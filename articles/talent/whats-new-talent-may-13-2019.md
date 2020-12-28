---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (13. toukokuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
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
ms.openlocfilehash: 11c9f03f4b3915d81b624115a1d97a0c7bc31709
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529729"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-13-2019"></a><span data-ttu-id="2af50-103">Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (13. toukokuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="2af50-103">What's new or changed in Dynamics 365 Talent (May 13, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2af50-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="2af50-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="2af50-105">Tulossa pian Attractiin</span><span class="sxs-lookup"><span data-stu-id="2af50-105">Coming soon in Attract</span></span>

### <a name="job-approvals-on-home-page"></a><span data-ttu-id="2af50-106">Työn hyväksynnät kotisivulla</span><span class="sxs-lookup"><span data-stu-id="2af50-106">Job approvals on home page</span></span>

<span data-ttu-id="2af50-107">Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa.</span><span class="sxs-lookup"><span data-stu-id="2af50-107">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="2af50-108">Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät.</span><span class="sxs-lookup"><span data-stu-id="2af50-108">Approvers can review their approvals under **Assigned to you**, which displays the job ID, title, other approvers, and date assigned.</span></span> <span data-ttu-id="2af50-109">Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.</span><span class="sxs-lookup"><span data-stu-id="2af50-109">Users who submit a job for approval can review their jobs under **Requested by you**, which displays the approvers who still need to approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="2af50-110">Onboardin muutokset</span><span class="sxs-lookup"><span data-stu-id="2af50-110">Changes in Onboard</span></span>

<span data-ttu-id="2af50-111">Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="2af50-111">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="2af50-112">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="2af50-112">Changes in Core HR</span></span>

<span data-ttu-id="2af50-113">Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2297.</span><span class="sxs-lookup"><span data-stu-id="2af50-113">Changes described in this section apply to build number 8.1.2297.</span></span> <span data-ttu-id="2af50-114">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.</span><span class="sxs-lookup"><span data-stu-id="2af50-114">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="2af50-115">Määritä esiintymätyyppi, kun Talentia valmistellaan</span><span class="sxs-lookup"><span data-stu-id="2af50-115">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="2af50-116">Uuden Talent-esiintymän valmistelun yhteydessä voit määrittää, onko esiintymän tyyppi **Tuotanto** vai **Eristys**, mikä mahdollistaa uusien ominaisuuksien varhaisen testaamisen.</span><span class="sxs-lookup"><span data-stu-id="2af50-116">When provisioning a new instance of Talent, you can indicate whether the instance type is **Production** or **Sandbox**, which allows for early testing of new features.</span></span> <span data-ttu-id="2af50-117">Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="2af50-117">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="2af50-118">Jos haluat, että jokin olemassa olevista instansseista päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [Tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.</span><span class="sxs-lookup"><span data-stu-id="2af50-118">If you want one of your existing instances to be updated to the **Sandbox** instance type, please contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="2af50-119">Common Data Service mukautettujen kenttien yksikkötuki</span><span class="sxs-lookup"><span data-stu-id="2af50-119">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="2af50-120">Tämän viikon versiossa seuraavat Common Data Service entiteetit tukevat nyt mukautettuja kenttiä: Työllisyys, etuuden laskentataajuus, etuuden laskenta, työlomakalenteri ja tunnustyypit.</span><span class="sxs-lookup"><span data-stu-id="2af50-120">In this week's release, the following Common Data Service entities now support custom fields: Employment, Benefit calc frequency, Benefit calc rate, Work calendar holiday, and Identification type.</span></span>

### <a name="common-data-service-integration-page"></a><span data-ttu-id="2af50-121">Common Data Service -integrointisivu</span><span class="sxs-lookup"><span data-stu-id="2af50-121">Common Data Service integration page</span></span>

<span data-ttu-id="2af50-122">Tämä versio sisältää **Järjestelmänhallinnan > Linkkien > Integroinnin > Common Data Service -määrityksen** uuden vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="2af50-122">This release provides a new option in **System Administration > Links > Integrations > Common Data Service configuration**.</span></span> <span data-ttu-id="2af50-123">**Common Data Service** -vaihtoehdon avulla järjestelmänvalvoja tai tietojen hallinnan järjestelmänvalvoja voi tehdä joustavuutta ja oivalluksia Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="2af50-123">The **Common Data Service configuration** option allows an administrator or data management administrator some flexibility and insights with the Common Data Service.</span></span> <span data-ttu-id="2af50-124">Tämän vaihtoehdon voit ottaa käyttöön tai poistaa Common Data Service -integroinnissa Talent-esiintymässä ja tarkastella synkronoinnin tietoja Talent-instanssin ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="2af50-124">With this option, you can enable or disable Common Data Service integration with a Talent instance and view the sync details between the Talent instance and the Common Data Service.</span></span>

### <a name="import-performance-data-with-final-employee-rating-316710"></a><span data-ttu-id="2af50-125">Tuo suorituskykytiedot lopullisen työntekijäluokituksen kanssa (316710)</span><span class="sxs-lookup"><span data-stu-id="2af50-125">Import performance data with final employee rating (316710)</span></span>

<span data-ttu-id="2af50-126">Tässä versiossa voit tuoda aiempia työntekijän luokitustietoja.</span><span class="sxs-lookup"><span data-stu-id="2af50-126">In this release, you can import historical employee rating data.</span></span> <span data-ttu-id="2af50-127">**FinalEmployeeRatingId**-kentällä on nyt kirjoitusoikeus.</span><span class="sxs-lookup"><span data-stu-id="2af50-127">The **FinalEmployeeRatingId** field now has write permission.</span></span>

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a><span data-ttu-id="2af50-128">Ei voi luoda työntekijän Common Data Service -osoitetta ja synkronoida sitä Talentin (317555) kanssa</span><span class="sxs-lookup"><span data-stu-id="2af50-128">Can't create Worker address in Common Data Service and sync it with Talent (317555)</span></span>

<span data-ttu-id="2af50-129">Tämä muutos sallii Common Data Service -järjestelmään luotujen osoitetietojen synkronoinnin Talentin kanssa.</span><span class="sxs-lookup"><span data-stu-id="2af50-129">This change allows address data created in Common Data Service to sync with Talent.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2af50-130">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="2af50-130">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="2af50-131">Uusi sivu sijaintihierarkian tietojen tarkistamista varten</span><span class="sxs-lookup"><span data-stu-id="2af50-131">New page to validate position hierarchy data</span></span>

<span data-ttu-id="2af50-132">Henkilöstöhallinto (HR) ja järjestelmänvalvojat voivat vahvistaa johtamishierarkian mahdollisesti vahingossa tuotuja kehäviittauksia varten.</span><span class="sxs-lookup"><span data-stu-id="2af50-132">Human resources (HR) and administrators can validate the managerial hierarchy for any circular references that might have been inadvertently imported.</span></span> <span data-ttu-id="2af50-133">Voit käyttää tätä uutta sivua kohdasta **Organisaation hallinta > Linkit > Tehtävät > Tehtävähierarkian oikeellisuustarkistus**.</span><span class="sxs-lookup"><span data-stu-id="2af50-133">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="2af50-134">Määritä lomatyyppien syykoodit</span><span class="sxs-lookup"><span data-stu-id="2af50-134">Specify reason codes on leave types</span></span>

<span data-ttu-id="2af50-135">Organisaatiot saattavat vaatia lisätietoja, jotka liittyvät lomapyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="2af50-135">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="2af50-136">Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.</span><span class="sxs-lookup"><span data-stu-id="2af50-136">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="2af50-137">Vaadi syykoodeja määrätyille poissaolopyyntöjen lomatyypeille</span><span class="sxs-lookup"><span data-stu-id="2af50-137">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="2af50-138">Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaolopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="2af50-138">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="2af50-139">Tämä vaatimus voi olla olemassa yrityksen käytäntöjen tai lakisääteisten vaatimusten vuoksi.</span><span class="sxs-lookup"><span data-stu-id="2af50-139">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="2af50-140">Voit määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.</span><span class="sxs-lookup"><span data-stu-id="2af50-140">You can specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="2af50-141">Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot</span><span class="sxs-lookup"><span data-stu-id="2af50-141">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="2af50-142">Mahdollisuus seurata työntekijöiden aikaa ja ymmärtää, kuinka aikaa lasketaan, ei ainoastaan auta henkilöstöresursseja vastaamaan työntekijäkysymyksiin, vaan myös auttaa varmistamaan työntekijöille tarkat aikakatkaisuehdotukset.</span><span class="sxs-lookup"><span data-stu-id="2af50-142">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="2af50-143">Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt), jolloin henkilöstöhallinto voi nähdä poissaolosaldon syyt.</span><span class="sxs-lookup"><span data-stu-id="2af50-143">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind time-off balances.</span></span>
