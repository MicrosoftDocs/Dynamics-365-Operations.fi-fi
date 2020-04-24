---
title: Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175105"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="6fd5b-103">Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6fd5b-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fd5b-104">Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="6fd5b-105">*Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="6fd5b-106">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="6fd5b-107">Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="6fd5b-108">Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="6fd5b-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="6fd5b-109">Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="6fd5b-110">Financen version 10.0.12 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6fd5b-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="6fd5b-111">Puolan SSRS-raportit, maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri - toimintojen viite PL-00014</span><span class="sxs-lookup"><span data-stu-id="6fd5b-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="6fd5b-112">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="6fd5b-113">Ei lakisääteistä edellytystä.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-113">Not legally required.</span></span>  |
| <span data-ttu-id="6fd5b-114">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="6fd5b-115">Kyllä (Excel-muoto vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="6fd5b-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="6fd5b-116">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-116">**Product areas affected**</span></span>         | <span data-ttu-id="6fd5b-117">Sovellus</span><span class="sxs-lookup"><span data-stu-id="6fd5b-117">Application</span></span> |
| <span data-ttu-id="6fd5b-118">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-118">**Deployment option**</span></span>              | <span data-ttu-id="6fd5b-119">Kaikki</span><span class="sxs-lookup"><span data-stu-id="6fd5b-119">All</span></span> |
| <span data-ttu-id="6fd5b-120">**Tila**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-120">**Status**</span></span>                         | <span data-ttu-id="6fd5b-121">Vanhentunut: 1.7.2021 jälkeen emme enää tue SSRS-raportteja: **Maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri – toimintojen viite PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="6fd5b-122">Excel-muodon esimerkki vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa (JPK_VDEK) otetaan sen sijaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a><span data-ttu-id="6fd5b-123">Financen version 10.0.11 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6fd5b-123">Features removed or deprecated in the Finance 10.0.11 release</span></span>

### <a name="norwegian-standard-main-accounts"></a><span data-ttu-id="6fd5b-124">Norjan vakiopäätilit</span><span class="sxs-lookup"><span data-stu-id="6fd5b-124">Norwegian Standard main accounts</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="6fd5b-125">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="6fd5b-126">Uudelleensuunnittelu</span><span class="sxs-lookup"><span data-stu-id="6fd5b-126">Redesign</span></span>  |
| <span data-ttu-id="6fd5b-127">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="6fd5b-128">Kyllä (sovelluskohtaiset parametrit korvattu ER-muodolla)</span><span class="sxs-lookup"><span data-stu-id="6fd5b-128">Yes (Replaced with ER format application-specific parameters)</span></span> |
| <span data-ttu-id="6fd5b-129">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-129">**Product areas affected**</span></span>         | <span data-ttu-id="6fd5b-130">Sovellus</span><span class="sxs-lookup"><span data-stu-id="6fd5b-130">Application</span></span> |
| <span data-ttu-id="6fd5b-131">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-131">**Deployment option**</span></span>              | <span data-ttu-id="6fd5b-132">Kaikki</span><span class="sxs-lookup"><span data-stu-id="6fd5b-132">All</span></span> |
| <span data-ttu-id="6fd5b-133">**Tila**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-133">**Status**</span></span>                         | <span data-ttu-id="6fd5b-134">Vanhentunut: 1. huhtikuuta 2021 mennessä emme enää tue vakiopäätileihin liittyviä toimintoja: viitekenttä, liittyvä taulu, tietoyksikkö.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-134">Deprecated: By April 1, 2021, we plan to no longer support functionality related to Standard main accounts: Reference field, related table, data entity.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="6fd5b-135">Financen version 10.0.7 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6fd5b-135">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="6fd5b-136">Työnkulun pyynnön muutoksen valintaikkuna ei enää sisällä käyttäjän valinnan avattavaa luetteloa</span><span class="sxs-lookup"><span data-stu-id="6fd5b-136">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="6fd5b-137">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-137">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="6fd5b-138">Siirrytty ominaisuuteen, jossa on tiliryhmävalinta.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-138">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="6fd5b-139">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-139">**Replaced by another feature?**</span></span>   | <span data-ttu-id="6fd5b-140">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6fd5b-140">Yes</span></span> |
| <span data-ttu-id="6fd5b-141">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-141">**Product areas affected**</span></span>         | <span data-ttu-id="6fd5b-142">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="6fd5b-142">Workflow</span></span> |
| <span data-ttu-id="6fd5b-143">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-143">**Deployment option**</span></span>              | <span data-ttu-id="6fd5b-144">Kaikki</span><span class="sxs-lookup"><span data-stu-id="6fd5b-144">All</span></span> |
| <span data-ttu-id="6fd5b-145">**Tila**</span><span class="sxs-lookup"><span data-stu-id="6fd5b-145">**Status**</span></span>                         | <span data-ttu-id="6fd5b-146">Vanhentunut: Suunnittelemme lopettavamme Kiinalaisten tositetyyppimäärityksen tukemisen ilman tiliryhmävalintaa 1.12.2020 mennessä.</span><span class="sxs-lookup"><span data-stu-id="6fd5b-146">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="6fd5b-147">Lisätietoja uudesta suunnitelmasta on kohdassa [Uutta versiossa 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="6fd5b-147">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="6fd5b-148">Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="6fd5b-148">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="6fd5b-149">Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="6fd5b-149">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
