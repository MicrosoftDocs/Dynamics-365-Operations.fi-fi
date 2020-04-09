---
title: Integroitu vero
description: Tässä aiheessa kuvataan verotietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173082"
---
# <a name="integrated-tax"></a><span data-ttu-id="e8bec-103">Integroitu vero</span><span class="sxs-lookup"><span data-stu-id="e8bec-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e8bec-104">Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset</span><span class="sxs-lookup"><span data-stu-id="e8bec-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="e8bec-105">Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.</span><span class="sxs-lookup"><span data-stu-id="e8bec-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="e8bec-106">Mallit</span><span class="sxs-lookup"><span data-stu-id="e8bec-106">Templates</span></span>

<span data-ttu-id="e8bec-107">Verotiedot sisältävät entiteettikarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e8bec-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="e8bec-108">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="e8bec-108">Finance and Operations apps</span></span> | <span data-ttu-id="e8bec-109">Dynamics 365:n mallipohjaiset sovellukset</span><span class="sxs-lookup"><span data-stu-id="e8bec-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e8bec-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e8bec-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="e8bec-111">Verokoodit</span><span class="sxs-lookup"><span data-stu-id="e8bec-111">Tax codes</span></span>                   | <span data-ttu-id="e8bec-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e8bec-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="e8bec-113">Veroryhmät</span><span class="sxs-lookup"><span data-stu-id="e8bec-113">Tax groups</span></span>                 | <span data-ttu-id="e8bec-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e8bec-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="e8bec-115">Veronimikeryhmät</span><span class="sxs-lookup"><span data-stu-id="e8bec-115">Tax item groups</span></span>             | <span data-ttu-id="e8bec-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="e8bec-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="e8bec-117">Verovapaudet</span><span class="sxs-lookup"><span data-stu-id="e8bec-117">Tax Exemptions</span></span>             | <span data-ttu-id="e8bec-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="e8bec-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="e8bec-119">Veroviranomaiset</span><span class="sxs-lookup"><span data-stu-id="e8bec-119">Tax Authorities</span></span>             | <span data-ttu-id="e8bec-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="e8bec-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="e8bec-121">Ennakonpidätyskoodit</span><span class="sxs-lookup"><span data-stu-id="e8bec-121">Withholding tax codes</span></span>       | <span data-ttu-id="e8bec-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e8bec-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="e8bec-123">Ennakonpidätysryhmät</span><span class="sxs-lookup"><span data-stu-id="e8bec-123">Withholding tax groups</span></span>     | <span data-ttu-id="e8bec-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e8bec-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="e8bec-125">Verokirjanpidon tiliryhmä</span><span class="sxs-lookup"><span data-stu-id="e8bec-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="e8bec-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="e8bec-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

