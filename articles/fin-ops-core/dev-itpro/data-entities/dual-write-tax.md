---
title: Integroitu vero
description: Tässä ohjeaiheessa käsitellään verotietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853856"
---
# <a name="integrated-tax"></a><span data-ttu-id="e3fc3-103">Integroitu vero</span><span class="sxs-lookup"><span data-stu-id="e3fc3-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3fc3-104">Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset</span><span class="sxs-lookup"><span data-stu-id="e3fc3-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="e3fc3-105">Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.</span><span class="sxs-lookup"><span data-stu-id="e3fc3-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="e3fc3-106">Mallit</span><span class="sxs-lookup"><span data-stu-id="e3fc3-106">Templates</span></span>

<span data-ttu-id="e3fc3-107">Verotiedot sisältävät entiteettikarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e3fc3-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="e3fc3-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e3fc3-108">Finance and Operations</span></span>   | <span data-ttu-id="e3fc3-109">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="e3fc3-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="e3fc3-110">Verokoodit</span><span class="sxs-lookup"><span data-stu-id="e3fc3-110">Tax codes</span></span>                  | <span data-ttu-id="e3fc3-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e3fc3-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="e3fc3-112">Veroryhmät</span><span class="sxs-lookup"><span data-stu-id="e3fc3-112">Tax groups</span></span>               | <span data-ttu-id="e3fc3-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e3fc3-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="e3fc3-114">Veronimikeryhmät</span><span class="sxs-lookup"><span data-stu-id="e3fc3-114">Tax item groups</span></span>          | <span data-ttu-id="e3fc3-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="e3fc3-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="e3fc3-116">Verovapaudet</span><span class="sxs-lookup"><span data-stu-id="e3fc3-116">Tax Exemptions</span></span>           | <span data-ttu-id="e3fc3-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="e3fc3-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="e3fc3-118">Veroviranomaiset</span><span class="sxs-lookup"><span data-stu-id="e3fc3-118">Tax Authorities</span></span>          | <span data-ttu-id="e3fc3-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="e3fc3-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="e3fc3-120">Ennakonpidätyskoodit</span><span class="sxs-lookup"><span data-stu-id="e3fc3-120">Withholding tax codes</span></span>      | <span data-ttu-id="e3fc3-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e3fc3-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="e3fc3-122">Ennakonpidätysryhmät</span><span class="sxs-lookup"><span data-stu-id="e3fc3-122">Withholding tax groups</span></span>   | <span data-ttu-id="e3fc3-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e3fc3-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="e3fc3-124">Verokirjanpidon tiliryhmä</span><span class="sxs-lookup"><span data-stu-id="e3fc3-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="e3fc3-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="e3fc3-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

