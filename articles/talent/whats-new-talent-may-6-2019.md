---
title: Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (6. toukokuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c541bac532e878c8493a60d95c05c9104d4b96e1
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741541"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-6-2019"></a><span data-ttu-id="c7141-103">Dynamics 365 for Talentin uudet tai muuttuneet ominaisuudet (6. toukokuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="c7141-103">What's new or changed in Dynamics 365 for Talent (May 6, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7141-104">Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c7141-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="c7141-105">Attractin muutokset</span><span class="sxs-lookup"><span data-stu-id="c7141-105">Changes in Attract</span></span>

### <a name="select-optional-documents-upon-offer-creation"></a><span data-ttu-id="c7141-106">Valinnaisten tiedostojen valitseminen tarjouksen luonnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="c7141-106">Select optional documents upon offer creation</span></span>

<span data-ttu-id="c7141-107">Kun valitset tarjouspakettimallin, Attract pyytää sinua nyt valitsemaan sovellettavat, valinnaiset asiakirjat kyseisen paketin mallista.</span><span class="sxs-lookup"><span data-stu-id="c7141-107">When you select an offer package template, Attract now prompts you to select the applicable, optional documents from that package template.</span></span> <span data-ttu-id="c7141-108">Voit lisätä muita valinnaisia asiakirjoja tarjousta valmisteltaessa.</span><span class="sxs-lookup"><span data-stu-id="c7141-108">You can add other optional documents while preparing the offer.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="c7141-109">Onboardin muutokset</span><span class="sxs-lookup"><span data-stu-id="c7141-109">Changes in Onboard</span></span>

<span data-ttu-id="c7141-110">Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboardin ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="c7141-110">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="c7141-111">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="c7141-111">Changes in Core HR</span></span>

<span data-ttu-id="c7141-112">Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2282.</span><span class="sxs-lookup"><span data-stu-id="c7141-112">Changes described in this section apply to build number 8.1.2282.</span></span> <span data-ttu-id="c7141-113">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.</span><span class="sxs-lookup"><span data-stu-id="c7141-113">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="platform-update-26"></a><span data-ttu-id="c7141-114">Ympäristön update 26 -päivitys</span><span class="sxs-lookup"><span data-stu-id="c7141-114">Platform update 26</span></span>

<span data-ttu-id="c7141-115">Lisätietoja Platform update 26:stä on artikkelissa [Dynamics 365 for Finance and Operations platform update 26:n esiversio-ominaisuudet (toukokuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span><span class="sxs-lookup"><span data-stu-id="c7141-115">For additional details about Platform update 26, see [Preview features in Dynamics 365 for Finance and Operations platform update 26 (May 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26).</span></span> 

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="c7141-116">Common Data Service mukautettujen kenttien yksikkötuki</span><span class="sxs-lookup"><span data-stu-id="c7141-116">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="c7141-117">Tämän viikon versiossa seuraavat entiteetit tukevat nyt mukautettuja kenttiä: etuus Calc Frequency, etuus-Calc Rate, etutyyppi, työkalenteri, lomatyökalenteri, maksusykli ja työntekijän tunnustyypit.</span><span class="sxs-lookup"><span data-stu-id="c7141-117">In this week's release, the following entities now support custom fields: Benefit calc frequency, Benefit calc rate, Benefit type, Work calendar, Work calendar holiday, Pay cycle, and Worker identification types.</span></span>

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a><span data-ttu-id="c7141-118">Massarekisteröinnin jättäminen, määrittämistason muuttaminen aiemmaksi päivämääräksi ei päivitä alkuperäistä jaksotusprosenttia (318526)</span><span class="sxs-lookup"><span data-stu-id="c7141-118">Leave mass enrollment, changing the tier basis to "Seniority date" doesn't refresh the initial accrual rate (318526)</span></span>

<span data-ttu-id="c7141-119">Kun joukkorekisteröit työntekijöitä ja muutat tasoperustetta, alkuperäinen jaksotus vastaa valittua tasoperustetta.</span><span class="sxs-lookup"><span data-stu-id="c7141-119">When you mass enroll employees and change the tier basis, the initial accrual now reflects the tier basis that you selected.</span></span>

### <a name="workflow-showing-duplicate-place-holders-313636"></a><span data-ttu-id="c7141-120">Työnkulku, jossa on päällekkäisiä paikanhaltijoita (313636)</span><span class="sxs-lookup"><span data-stu-id="c7141-120">Workflow showing duplicate place holders (313636)</span></span>

<span data-ttu-id="c7141-121">Tämän version muutokset poistavat paikkamerkkien kaksoiskappaleet, kun työnkulkuilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="c7141-121">Changes in this release eliminate duplication of placeholders when workflow notifications are sent.</span></span>

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a><span data-ttu-id="c7141-122">Dimensiokenttiä ei päivitetä käytettäessä "Avaa Excelissä" (176261) -toimintoa</span><span class="sxs-lookup"><span data-stu-id="c7141-122">Dimension fields aren't updated when using "Open in Excel" (176261)</span></span>

<span data-ttu-id="c7141-123">Tämän version avulla voit nyt päivittää taloushallinnon dimension käyttämällä **Avaa Excelissä** -toimintoa **Työntekijä**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="c7141-123">With this release, you can now update financial dimension using **Open in Excel** from the **Worker** page.</span></span> 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a><span data-ttu-id="c7141-124">Common Data Servicessä järjestelmään luotua työntekijän osoitetta ei synkronoida Talentiin (317555)</span><span class="sxs-lookup"><span data-stu-id="c7141-124">Worker address created in Common Data Service isn't synced to Talent (317555)</span></span>

<span data-ttu-id="c7141-125">Tämän muutoksen osoitteet luodaan Common Data Servicessä ja päivitetään Talent Core HR:ssä.</span><span class="sxs-lookup"><span data-stu-id="c7141-125">With this change, addresses created in Common Data Service are updated in Talent Core HR.</span></span>


## <a name="in-preview"></a><span data-ttu-id="c7141-126">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="c7141-126">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="c7141-127">Uusi sivu sijaintihierarkian tietojen tarkistamista varten</span><span class="sxs-lookup"><span data-stu-id="c7141-127">New page to validate position hierarchy data</span></span>

<span data-ttu-id="c7141-128">Henkilöstöhallinto (HR) ja järjestelmänvalvojat voivat nyt vahvistaa johtamishierarkian mahdollisesti vahingossa tuotuja kehäviittauksia varten.</span><span class="sxs-lookup"><span data-stu-id="c7141-128">Human resources (HR) and administrators can now validate the managerial hierarchy for any circular references that might have inadvertently been imported.</span></span> <span data-ttu-id="c7141-129">Voit käyttää tätä uutta sivua kohdasta **Organisaation hallinta > Linkit > Tehtävät > Tehtävähierarkian oikeellisuustarkistus**.</span><span class="sxs-lookup"><span data-stu-id="c7141-129">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="c7141-130">Määritä lomatyyppien syykoodit</span><span class="sxs-lookup"><span data-stu-id="c7141-130">Specify reason codes on leave types</span></span>

<span data-ttu-id="c7141-131">Organisaatiot saattavat vaatia lisätietoja, jotka liittyvät lomapyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="c7141-131">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="c7141-132">Voit nyt määrittää lomalajien syykoodit ja antaa työntekijöille mahdollisuuden valita syykoodin lomapyynnöissään.</span><span class="sxs-lookup"><span data-stu-id="c7141-132">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="c7141-133">Vaadi syykoodeja määrätyille poissaolopyyntöjen lomatyypeille</span><span class="sxs-lookup"><span data-stu-id="c7141-133">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="c7141-134">Organisaatiot saattavat vaatia syykoodien asettamista tietylle lomalajeille, kun työntekijät kirjaavat poissaolopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="c7141-134">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="c7141-135">Tämä vaatimus voi olla olemassa yrityksen käytäntöjen tai lakisääteisten vaatimusten vuoksi.</span><span class="sxs-lookup"><span data-stu-id="c7141-135">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="c7141-136">Voit nyt määrittää mitkä lomatyypit edellyttävät syykoodin, ja voit vaatia työntekijöitä antamaan syykoodin näille lomatyypeille poissaolopyynnössä.</span><span class="sxs-lookup"><span data-stu-id="c7141-136">You can now specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="c7141-137">Tarjoa henkilöstöhallinnolle loma- ja poissaololuettelot</span><span class="sxs-lookup"><span data-stu-id="c7141-137">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="c7141-138">Mahdollisuus seurata työntekijöiden aikaa ja ymmärtää, kuinka aikaa lasketaan, ei ainoastaan auta henkilöstöresursseja vastaamaan työntekijäkysymyksiin, vaan myös auttaa varmistamaan työntekijöille tarkat aikakatkaisuehdotukset.</span><span class="sxs-lookup"><span data-stu-id="c7141-138">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="c7141-139">Henkilöstöhallinnolla on nyt uusi näkemys liiketoimista (apurahat, suoritukset, oikaisut ja pyynnöt), jolloin henkilöstöhallinto voi nähdä saldon syyt.</span><span class="sxs-lookup"><span data-stu-id="c7141-139">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c7141-140">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="c7141-140">Coming soon</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="c7141-141">Määritä esiintymätyyppi, kun Talentia valmistellaan</span><span class="sxs-lookup"><span data-stu-id="c7141-141">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="c7141-142">Uuden Talent-esiintymän valmistelun yhteydessä voit määrittää, onko esiintymän tyyppi **Tuotanto** vai **Eristys**, mahdollistaen uusien ominaisuuksien varhaisen testaamisen.</span><span class="sxs-lookup"><span data-stu-id="c7141-142">When provisioning a new instance of Talent, you will be able to indicate whether the instance type is **Production** or **Sandbox**, allowing for early testing of new features.</span></span> <span data-ttu-id="c7141-143">Kaikki aiemmin luodut Talent-esiintymät päivitetään tuotantoesiintymän tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="c7141-143">All existing Talent instances will be updated to the Production instance type.</span></span> <span data-ttu-id="c7141-144">Jos haluat, että jokin olemassa olevista instansseista päivitetään eristysesiintymätyypiksi, ota yhteyttä tukeen ja tee muutospyyntö.</span><span class="sxs-lookup"><span data-stu-id="c7141-144">If you want one of your existing instances to be updated to the Sandbox instance type, please contact Support to initiate the change request.</span></span>
