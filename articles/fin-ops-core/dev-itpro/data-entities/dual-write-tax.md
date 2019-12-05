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
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772407"
---
## <a name="integrated-tax"></a><span data-ttu-id="cb94f-103">Integroitu vero</span><span class="sxs-lookup"><span data-stu-id="cb94f-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb94f-104">Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset</span><span class="sxs-lookup"><span data-stu-id="cb94f-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="cb94f-105">Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.</span><span class="sxs-lookup"><span data-stu-id="cb94f-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="cb94f-106">Mallit</span><span class="sxs-lookup"><span data-stu-id="cb94f-106">Templates</span></span>

<span data-ttu-id="cb94f-107">Verotiedot sisältävät entiteettikarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="cb94f-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="cb94f-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cb94f-108">Finance and Operations</span></span>   | <span data-ttu-id="cb94f-109">Customer Engagement -sovellus</span><span class="sxs-lookup"><span data-stu-id="cb94f-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="cb94f-110">Verokoodit</span><span class="sxs-lookup"><span data-stu-id="cb94f-110">Tax codes</span></span>                  | <span data-ttu-id="cb94f-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="cb94f-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="cb94f-112">Veroryhmät</span><span class="sxs-lookup"><span data-stu-id="cb94f-112">Tax groups</span></span>               | <span data-ttu-id="cb94f-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="cb94f-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="cb94f-114">Veronimikeryhmät</span><span class="sxs-lookup"><span data-stu-id="cb94f-114">Tax item groups</span></span>          | <span data-ttu-id="cb94f-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="cb94f-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="cb94f-116">Verovapaudet</span><span class="sxs-lookup"><span data-stu-id="cb94f-116">Tax Exemptions</span></span>           | <span data-ttu-id="cb94f-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="cb94f-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="cb94f-118">Veroviranomaiset</span><span class="sxs-lookup"><span data-stu-id="cb94f-118">Tax Authorities</span></span>          | <span data-ttu-id="cb94f-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="cb94f-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="cb94f-120">Ennakonpidätyskoodit</span><span class="sxs-lookup"><span data-stu-id="cb94f-120">Withholding tax codes</span></span>      | <span data-ttu-id="cb94f-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="cb94f-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="cb94f-122">Ennakonpidätysryhmät</span><span class="sxs-lookup"><span data-stu-id="cb94f-122">Withholding tax groups</span></span>   | <span data-ttu-id="cb94f-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="cb94f-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="cb94f-124">Verokirjanpidon tiliryhmä</span><span class="sxs-lookup"><span data-stu-id="cb94f-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="cb94f-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="cb94f-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

