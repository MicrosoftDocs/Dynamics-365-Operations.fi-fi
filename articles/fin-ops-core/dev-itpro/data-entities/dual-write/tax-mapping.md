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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979326"
---
# <a name="integrated-tax"></a><span data-ttu-id="980c2-103">Integroitu vero</span><span class="sxs-lookup"><span data-stu-id="980c2-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="980c2-104">Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset</span><span class="sxs-lookup"><span data-stu-id="980c2-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="980c2-105">Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.</span><span class="sxs-lookup"><span data-stu-id="980c2-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="980c2-106">Mallit</span><span class="sxs-lookup"><span data-stu-id="980c2-106">Templates</span></span>

<span data-ttu-id="980c2-107">Verotiedot sisältävät entiteettikarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="980c2-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="980c2-108">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="980c2-108">Finance and Operations apps</span></span> | <span data-ttu-id="980c2-109">Dynamics 365:n mallipohjaiset sovellukset</span><span class="sxs-lookup"><span data-stu-id="980c2-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="980c2-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="980c2-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="980c2-111">Nimikkeen arvonlisäveroryhmä</span><span class="sxs-lookup"><span data-stu-id="980c2-111">Item sales tax group</span></span> | <span data-ttu-id="980c2-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="980c2-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="980c2-113">Alv-viranomaiset</span><span class="sxs-lookup"><span data-stu-id="980c2-113">Sales tax authorities</span></span> | <span data-ttu-id="980c2-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="980c2-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="980c2-115">Arvonlisäveron verovapauskoodin yksikkö CDS:lle</span><span class="sxs-lookup"><span data-stu-id="980c2-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="980c2-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="980c2-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="980c2-117">Arvonlisäveroryhmät</span><span class="sxs-lookup"><span data-stu-id="980c2-117">Sales tax groups</span></span> | <span data-ttu-id="980c2-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="980c2-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="980c2-119">Arvonlisäveron kirjanpidon kirjausryhmät V2</span><span class="sxs-lookup"><span data-stu-id="980c2-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="980c2-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="980c2-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="980c2-121">Ennakonpidätyskoodit</span><span class="sxs-lookup"><span data-stu-id="980c2-121">Withholding tax codes</span></span> | <span data-ttu-id="980c2-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="980c2-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="980c2-123">Ennakonpidätysryhmät</span><span class="sxs-lookup"><span data-stu-id="980c2-123">Withholding tax groups</span></span> | <span data-ttu-id="980c2-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="980c2-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

