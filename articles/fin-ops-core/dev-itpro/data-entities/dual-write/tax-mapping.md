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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019756"
---
# <a name="integrated-tax"></a><span data-ttu-id="8cda2-103">Integroitu vero</span><span class="sxs-lookup"><span data-stu-id="8cda2-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="8cda2-104">Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset</span><span class="sxs-lookup"><span data-stu-id="8cda2-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="8cda2-105">Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.</span><span class="sxs-lookup"><span data-stu-id="8cda2-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="8cda2-106">Mallit</span><span class="sxs-lookup"><span data-stu-id="8cda2-106">Templates</span></span>

<span data-ttu-id="8cda2-107">Verotiedot sisältävät entiteettikarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8cda2-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="8cda2-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8cda2-108">Finance and Operations</span></span>   | <span data-ttu-id="8cda2-109">Muut Dynamics 365 -sovellukset</span><span class="sxs-lookup"><span data-stu-id="8cda2-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="8cda2-110">Verokoodit</span><span class="sxs-lookup"><span data-stu-id="8cda2-110">Tax codes</span></span>                  | <span data-ttu-id="8cda2-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="8cda2-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="8cda2-112">Veroryhmät</span><span class="sxs-lookup"><span data-stu-id="8cda2-112">Tax groups</span></span>               | <span data-ttu-id="8cda2-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="8cda2-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="8cda2-114">Veronimikeryhmät</span><span class="sxs-lookup"><span data-stu-id="8cda2-114">Tax item groups</span></span>          | <span data-ttu-id="8cda2-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="8cda2-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="8cda2-116">Verovapaudet</span><span class="sxs-lookup"><span data-stu-id="8cda2-116">Tax Exemptions</span></span>           | <span data-ttu-id="8cda2-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="8cda2-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="8cda2-118">Veroviranomaiset</span><span class="sxs-lookup"><span data-stu-id="8cda2-118">Tax Authorities</span></span>          | <span data-ttu-id="8cda2-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="8cda2-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="8cda2-120">Ennakonpidätyskoodit</span><span class="sxs-lookup"><span data-stu-id="8cda2-120">Withholding tax codes</span></span>      | <span data-ttu-id="8cda2-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="8cda2-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="8cda2-122">Ennakonpidätysryhmät</span><span class="sxs-lookup"><span data-stu-id="8cda2-122">Withholding tax groups</span></span>   | <span data-ttu-id="8cda2-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="8cda2-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="8cda2-124">Verokirjanpidon tiliryhmä</span><span class="sxs-lookup"><span data-stu-id="8cda2-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="8cda2-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="8cda2-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

