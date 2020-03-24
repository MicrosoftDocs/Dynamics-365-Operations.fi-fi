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
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127974"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="42388-103">Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="42388-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42388-104">Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.</span><span class="sxs-lookup"><span data-stu-id="42388-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="42388-105">*Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="42388-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="42388-106">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="42388-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="42388-107">Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.</span><span class="sxs-lookup"><span data-stu-id="42388-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="42388-108">Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="42388-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="42388-109">Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="42388-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="42388-110">Financen version 10.0.12 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="42388-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="42388-111">Puolan SSRS-raportit, maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri - toimintojen viite PL-00014</span><span class="sxs-lookup"><span data-stu-id="42388-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="42388-112">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="42388-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="42388-113">Ei lakisääteistä edellytystä.</span><span class="sxs-lookup"><span data-stu-id="42388-113">Not legally required.</span></span>  |
| <span data-ttu-id="42388-114">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="42388-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="42388-115">Kyllä (Excel-muoto vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="42388-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="42388-116">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="42388-116">**Product areas affected**</span></span>         | <span data-ttu-id="42388-117">Sovellus</span><span class="sxs-lookup"><span data-stu-id="42388-117">Application</span></span> |
| <span data-ttu-id="42388-118">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="42388-118">**Deployment option**</span></span>              | <span data-ttu-id="42388-119">Kaikki</span><span class="sxs-lookup"><span data-stu-id="42388-119">All</span></span> |
| <span data-ttu-id="42388-120">**Tila**</span><span class="sxs-lookup"><span data-stu-id="42388-120">**Status**</span></span>                         | <span data-ttu-id="42388-121">Vanhentunut: 1.7.2021 jälkeen emme enää tue SSRS-raportteja: **Maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri – toimintojen viite PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="42388-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="42388-122">Excel-muodon esimerkki vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa (JPK_VDEK) otetaan sen sijaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="42388-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="42388-123">Financen version 10.0.7 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="42388-123">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="42388-124">Työnkulun pyynnön muutoksen valintaikkuna ei enää sisällä käyttäjän valinnan avattavaa luetteloa</span><span class="sxs-lookup"><span data-stu-id="42388-124">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="42388-125">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="42388-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="42388-126">Siirrytty ominaisuuteen, jossa on tiliryhmävalinta.</span><span class="sxs-lookup"><span data-stu-id="42388-126">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="42388-127">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="42388-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="42388-128">Kyllä</span><span class="sxs-lookup"><span data-stu-id="42388-128">Yes</span></span> |
| <span data-ttu-id="42388-129">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="42388-129">**Product areas affected**</span></span>         | <span data-ttu-id="42388-130">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="42388-130">Workflow</span></span> |
| <span data-ttu-id="42388-131">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="42388-131">**Deployment option**</span></span>              | <span data-ttu-id="42388-132">Kaikki</span><span class="sxs-lookup"><span data-stu-id="42388-132">All</span></span> |
| <span data-ttu-id="42388-133">**Tila**</span><span class="sxs-lookup"><span data-stu-id="42388-133">**Status**</span></span>                         | <span data-ttu-id="42388-134">Vanhentunut: Suunnittelemme lopettavamme Kiinalaisten tositetyyppimäärityksen tukemisen ilman tiliryhmävalintaa 1.12.2020 mennessä.</span><span class="sxs-lookup"><span data-stu-id="42388-134">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="42388-135">Lisätietoja uudesta suunnitelmasta on kohdassa [Uutta versiossa 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="42388-135">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="42388-136">Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="42388-136">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="42388-137">Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="42388-137">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
