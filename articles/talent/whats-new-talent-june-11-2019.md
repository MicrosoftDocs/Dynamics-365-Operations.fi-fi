---
title: Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (11.6.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b06dc0556bd1461573cd56abed602d72333a3f39
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023927"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a><span data-ttu-id="f30e1-103">Dynamics 365 Talentin uudet tai muuttuneet ominaisuudet (11.6.2019)</span><span class="sxs-lookup"><span data-stu-id="f30e1-103">What's new or changed in Dynamics 365 Talent (June 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f30e1-104">Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talentin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f30e1-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="f30e1-105">Attractin muutokset</span><span class="sxs-lookup"><span data-stu-id="f30e1-105">Changes in Attract</span></span>

### <a name="search-engine-optimization-for-job-posts"></a><span data-ttu-id="f30e1-106">Työilmoitusten hakukoneoptimointi</span><span class="sxs-lookup"><span data-stu-id="f30e1-106">Search engine optimization for job posts</span></span>

<span data-ttu-id="f30e1-107">Kun **Hakukoneoptimointi** otetaan käyttöön Dynamics 365 Talent: Attract -hallintakeskuksessa, Attract pyytää Googlen indeksoinnin ohjelmointirajapintaa indeksoimaan verkkosivun aina, kun aktivoit ja julkaiset uuden työpaikan tai päivität aiemmin luodun työpaikan.</span><span class="sxs-lookup"><span data-stu-id="f30e1-107">After you turn on **Search Engine Optimization** in the Dynamics 365 Talent: Attract Admin center, Attract informs the Google Indexing application programming interface (API) to crawl the webpage whenever you activate and post a new job or update an existing job.</span></span> <span data-ttu-id="f30e1-108">Tällä tavoin työpaikka näkyy Googlen ja muiden hakukoneiden hakutuloksissa.</span><span class="sxs-lookup"><span data-stu-id="f30e1-108">In this way, the job will appear in the search results for Google and other search engines.</span></span>

<span data-ttu-id="f30e1-109">Vastaavasti aina, kun poistat työpaikan julkaisun, Attract ilmoittaa siitä indeksoinnin ohjelmointirajapintaan, jotta kyseinen työ, jonka julkaisu on poistettu, ei enää näy hakutuloksissa.</span><span class="sxs-lookup"><span data-stu-id="f30e1-109">Likewise, whenever you unpost a job, Attract informs the Indexing API, so that the unposted job will stop appearing in search results.</span></span>

> [!NOTE]
> <span data-ttu-id="f30e1-110">Hakuohjelmilla ei ole määritettyä aikarajaa verkkosivujen indeksointiin tai hakutulosten päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="f30e1-110">Web crawlers don't have a defined timeframe for crawling webpages or updating search results.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="f30e1-111">Tulossa pian Attractiin</span><span class="sxs-lookup"><span data-stu-id="f30e1-111">Coming soon in Attract</span></span>

### <a name="job-approvals-appear-on-the-home-page"></a><span data-ttu-id="f30e1-112">Työn hyväksynnät näkyvät aloitussivulla</span><span class="sxs-lookup"><span data-stu-id="f30e1-112">Job approvals appear on the home page</span></span>

<span data-ttu-id="f30e1-113">Hyväksynnät näkyvät koontinäytön **Hyväksynnät**-osassa.</span><span class="sxs-lookup"><span data-stu-id="f30e1-113">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="f30e1-114">Hyväksyjät voivat tarkistaa **Vastuualueensa** hyväksynnät, jolloin työn tunnus, otsikko, muut hyväksyjät ja määritetty päivämäärä näkyvät.</span><span class="sxs-lookup"><span data-stu-id="f30e1-114">Approvers can review their approvals under **Assigned to you**, which shows the job ID, the job title, other approvers, and the date when the job was assigned.</span></span> <span data-ttu-id="f30e1-115">Käyttäjät, jotka lähettävät työn hyväksyttäväksi, voivat tarkastella töitään kohdassa **Mitä olet pyytänyt**, joka näyttää hyväksyjät, joiden on vielä hyväksyttävä lähetetty työ.</span><span class="sxs-lookup"><span data-stu-id="f30e1-115">Users who submit a job for approval can review their jobs under **Requested by you**, which shows the approvers who must still approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="f30e1-116">Onboardin muutokset</span><span class="sxs-lookup"><span data-stu-id="f30e1-116">Changes in Onboard</span></span>

<span data-ttu-id="f30e1-117">Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboard:n ohjelmakorjauksia.</span><span class="sxs-lookup"><span data-stu-id="f30e1-117">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="f30e1-118">Core HR:n muutokset</span><span class="sxs-lookup"><span data-stu-id="f30e1-118">Changes in Core HR</span></span>

<span data-ttu-id="f30e1-119">Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2337.</span><span class="sxs-lookup"><span data-stu-id="f30e1-119">The changes that are described in this section apply to build number 8.1.2337.</span></span>

### <a name="platform-update-27-for-finance-and-operations"></a><span data-ttu-id="f30e1-120">Finance and Operationsin käyttöympäristöpäivitys 27</span><span class="sxs-lookup"><span data-stu-id="f30e1-120">Platform update 27 for Finance and Operations</span></span>

<span data-ttu-id="f30e1-121">Lisätietoja Finance and Operationsin käyttöympäristöpäivitys 27:stä on artikkelissa [Dynamics 365 Finance and Operations -käyttöympäristöpäivitys 27:n esikatselutoiminnot (kesäkuu 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span><span class="sxs-lookup"><span data-stu-id="f30e1-121">For more details about Platform update 27 for Finance and Operations, see [Preview features in Dynamics 365 Finance and Operations platform update 27 (June 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span></span>

### <a name="feature-management-workspace-in-talent"></a><span data-ttu-id="f30e1-122">Ominaisuushallinnan työtila Talentissa</span><span class="sxs-lookup"><span data-stu-id="f30e1-122">Feature management workspace in Talent</span></span>

<span data-ttu-id="f30e1-123">**Järjestelmänhallinnan** **Toimintojen hallinta** -työtilassa voit tarkastella, ottaa käyttöön, poistaa käytöstä ja ajoittaa kuhunkin julkaisuun sisältyviä toimintoja.</span><span class="sxs-lookup"><span data-stu-id="f30e1-123">The **Feature management** workspace in **System administration** lets you view, enable, disable, and schedule features that have been delivered in each release.</span></span> <span data-ttu-id="f30e1-124">Uudet asetukset ovat oletusarvoisesti poissa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="f30e1-124">By default, new features are turned off.</span></span> <span data-ttu-id="f30e1-125">**Toimintojen hallinta** -työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota.</span><span class="sxs-lookup"><span data-stu-id="f30e1-125">You can use the **Feature management** workspace to turn them on and view the documentation for them.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="f30e1-126">Common Data Service mukautettujen kenttien yksikkötuki</span><span class="sxs-lookup"><span data-stu-id="f30e1-126">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="f30e1-127">Myöntäjätaho-yksikkö tukee mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="f30e1-127">The Issuing agency entity now supports custom fields.</span></span>

### <a name="new-common-data-service-entities"></a><span data-ttu-id="f30e1-128">Uudet Common Data Service -yksiköt</span><span class="sxs-lookup"><span data-stu-id="f30e1-128">New Common Data Service entities</span></span>

<span data-ttu-id="f30e1-129">Tehtäväryhmäyksikkö on lisätty.</span><span class="sxs-lookup"><span data-stu-id="f30e1-129">The Task group entity has been added.</span></span>

## <a name="in-preview"></a><span data-ttu-id="f30e1-130">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="f30e1-130">In preview</span></span>

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a><span data-ttu-id="f30e1-131">Vain eritysympäristöissä käyttöönotettavat esiversiotoiminnot</span><span class="sxs-lookup"><span data-stu-id="f30e1-131">Preview features will be enabled only in sandbox environments</span></span>

<span data-ttu-id="f30e1-132">Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="f30e1-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="f30e1-133">Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi Tuotanto vai Eristys.</span><span class="sxs-lookup"><span data-stu-id="f30e1-133">When you provision a new instance of Talent, you can indicate whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="f30e1-134">Eristys-esiintymätyyppi mahdollistaa uusien toimintojen testaamisen varhaisessa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="f30e1-134">The Sandbox instance type allows for early testing of new features.</span></span> <span data-ttu-id="f30e1-135">Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="f30e1-135">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="f30e1-136">Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.</span><span class="sxs-lookup"><span data-stu-id="f30e1-136">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="restrict-the-leave-types-in-time-off-requests"></a><span data-ttu-id="f30e1-137">Poissaolopyyntöjen lomatyyppien rajoittaminen</span><span class="sxs-lookup"><span data-stu-id="f30e1-137">Restrict the leave types in time-off requests</span></span>

<span data-ttu-id="f30e1-138">Organisaatiot voivat tarjota työntekijöille useita lomatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="f30e1-138">Organizations can offer many types of leave to employees.</span></span> <span data-ttu-id="f30e1-139">Työntekijät eivät kuitenkaan ehkä voi lähettää joidenkin lomatyyppien poissaolopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="f30e1-139">However, it might not be appropriate for employees to submit time-off requests for some leave types.</span></span> <span data-ttu-id="f30e1-140">Kyseisiä lomatyyppejä hallitaan sen sijaan henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="f30e1-140">Those leave types might be managed by Human resources (HR) instead.</span></span> <span data-ttu-id="f30e1-141">Tässä versiossa voit määrittää, mitä lomatyyppejä varten työntekijät voivat lähettää pyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="f30e1-141">In this release, you can configure which leave types employees can submit time-off requests for.</span></span> 

## <a name="coming-soon-in-core-hr"></a><span data-ttu-id="f30e1-142">Tulossa pian Core HR:ään</span><span class="sxs-lookup"><span data-stu-id="f30e1-142">Coming soon in Core HR</span></span>

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a><span data-ttu-id="f30e1-143">Raportin laajennettujen suorituskykytietojen näyttäminen esimiehen itsepalvelutoiminnossa</span><span class="sxs-lookup"><span data-stu-id="f30e1-143">View extended information about report performance in manager self-service</span></span>

<span data-ttu-id="f30e1-144">Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista.</span><span class="sxs-lookup"><span data-stu-id="f30e1-144">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="f30e1-145">Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita.</span><span class="sxs-lookup"><span data-stu-id="f30e1-145">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="f30e1-146">Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti.</span><span class="sxs-lookup"><span data-stu-id="f30e1-146">In addition, direct managers and their employees can maintain and update performance journals to help guarantee that the performance review process goes smoothly.</span></span> <span data-ttu-id="f30e1-147">Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi.</span><span class="sxs-lookup"><span data-stu-id="f30e1-147">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="f30e1-148">Kehityskeskustelujen tulostaminen</span><span class="sxs-lookup"><span data-stu-id="f30e1-148">Print performance reviews</span></span>

<span data-ttu-id="f30e1-149">Työntekijät, esimiehet ja henkilöstöhallinto voi tulostaa työntekijän kehityskeskustelun.</span><span class="sxs-lookup"><span data-stu-id="f30e1-149">Employees, managers, and HR will be able to print an employee's performance review.</span></span>
