---
title: Integroitu vero
description: Tässä aiheessa kuvataan verotietojen integraatiota Finance and Operationsin ja Dataversen välillä.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 14c22dd6602b5fbf866c8dc6b057f6c8acb1f48f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679293"
---
# <a name="integrated-tax"></a><span data-ttu-id="6791c-103">Integroitu vero</span><span class="sxs-lookup"><span data-stu-id="6791c-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="6791c-104">Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset</span><span class="sxs-lookup"><span data-stu-id="6791c-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="6791c-105">Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.</span><span class="sxs-lookup"><span data-stu-id="6791c-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="6791c-106">Mallit</span><span class="sxs-lookup"><span data-stu-id="6791c-106">Templates</span></span>

<span data-ttu-id="6791c-107">Verotiedot sisältävät taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6791c-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="6791c-108">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="6791c-108">Finance and Operations apps</span></span> | <span data-ttu-id="6791c-109">Dynamics 365:n mallipohjaiset sovellukset</span><span class="sxs-lookup"><span data-stu-id="6791c-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="6791c-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6791c-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="6791c-111">Nimikkeen arvonlisäveroryhmä</span><span class="sxs-lookup"><span data-stu-id="6791c-111">Item sales tax group</span></span> | <span data-ttu-id="6791c-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="6791c-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="6791c-113">Alv-viranomaiset</span><span class="sxs-lookup"><span data-stu-id="6791c-113">Sales tax authorities</span></span> | <span data-ttu-id="6791c-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="6791c-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="6791c-115">Arvonlisäveron verovapauskoodin yksikkö CDS:lle</span><span class="sxs-lookup"><span data-stu-id="6791c-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="6791c-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="6791c-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="6791c-117">Arvonlisäveroryhmät</span><span class="sxs-lookup"><span data-stu-id="6791c-117">Sales tax groups</span></span> | <span data-ttu-id="6791c-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="6791c-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="6791c-119">Arvonlisäveron kirjanpidon kirjausryhmät V2</span><span class="sxs-lookup"><span data-stu-id="6791c-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="6791c-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="6791c-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="6791c-121">Ennakonpidätyskoodit</span><span class="sxs-lookup"><span data-stu-id="6791c-121">Withholding tax codes</span></span> | <span data-ttu-id="6791c-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="6791c-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="6791c-123">Ennakonpidätysryhmät</span><span class="sxs-lookup"><span data-stu-id="6791c-123">Withholding tax groups</span></span> | <span data-ttu-id="6791c-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="6791c-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

