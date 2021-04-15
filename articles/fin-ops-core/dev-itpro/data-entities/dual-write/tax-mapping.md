---
title: Integroitu vero
description: Tässä aiheessa kuvataan verotietojen integraatiota Finance and Operationsin ja Dataversen välillä.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750639"
---
# <a name="integrated-tax"></a><span data-ttu-id="6d74a-103">Integroitu vero</span><span class="sxs-lookup"><span data-stu-id="6d74a-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="6d74a-104">Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset</span><span class="sxs-lookup"><span data-stu-id="6d74a-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="6d74a-105">Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.</span><span class="sxs-lookup"><span data-stu-id="6d74a-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="6d74a-106">Mallit</span><span class="sxs-lookup"><span data-stu-id="6d74a-106">Templates</span></span>

<span data-ttu-id="6d74a-107">Verotiedot sisältävät taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6d74a-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="6d74a-108">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="6d74a-108">Finance and Operations apps</span></span> | <span data-ttu-id="6d74a-109">Dynamics 365:n mallipohjaiset sovellukset</span><span class="sxs-lookup"><span data-stu-id="6d74a-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="6d74a-110">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6d74a-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="6d74a-111">Nimikkeen arvonlisäveroryhmä</span><span class="sxs-lookup"><span data-stu-id="6d74a-111">Item sales tax group</span></span> | <span data-ttu-id="6d74a-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="6d74a-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="6d74a-113">Alv-viranomaiset</span><span class="sxs-lookup"><span data-stu-id="6d74a-113">Sales tax authorities</span></span> | <span data-ttu-id="6d74a-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="6d74a-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="6d74a-115">Arvonlisäveron verovapauskoodin yksikkö CDS:lle</span><span class="sxs-lookup"><span data-stu-id="6d74a-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="6d74a-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="6d74a-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="6d74a-117">Arvonlisäveroryhmät</span><span class="sxs-lookup"><span data-stu-id="6d74a-117">Sales tax groups</span></span> | <span data-ttu-id="6d74a-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="6d74a-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="6d74a-119">Arvonlisäveron kirjanpidon kirjausryhmät V2</span><span class="sxs-lookup"><span data-stu-id="6d74a-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="6d74a-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="6d74a-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="6d74a-121">Ennakonpidätyskoodit</span><span class="sxs-lookup"><span data-stu-id="6d74a-121">Withholding tax codes</span></span> | <span data-ttu-id="6d74a-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="6d74a-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="6d74a-123">Ennakonpidätysryhmät</span><span class="sxs-lookup"><span data-stu-id="6d74a-123">Withholding tax groups</span></span> | <span data-ttu-id="6d74a-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="6d74a-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]