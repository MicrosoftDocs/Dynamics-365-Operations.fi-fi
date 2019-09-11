---
title: Finance and Operationsin ja Common Data Servicen alkuperäisen sykronoinnin toteuttamisjärjestys
description: Tässä ohjeaiheessa määritetään synkronoinnin järjestys, jota on noudatettava alkuperäisten tietojen luomiseen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873125"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="26362-103">Finance and Operationsin ja Common Data Servicen alkuperäisen sykronoinnin toteuttamisjärjestys</span><span class="sxs-lookup"><span data-stu-id="26362-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="26362-104">Ennen kuin käytät tietojen integrointia, sinun on luotava asiakkaille, toimittajille ja yhteyshenkilöille tarvittavat alkuperäiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="26362-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="26362-105">Haluat esimerkiksi luoda uuden **Toimittajaryhmä**-nimikkeen ja määrittää sen **Maksuehdot**-arvoksi **Net30**.</span><span class="sxs-lookup"><span data-stu-id="26362-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="26362-106">Tässä tapauksessa, ennen kuin yrität luoda **Toimittajaryhmä**-nimikkeen, varmista, että **Net30** on sekä Microsoft Dynamics 365 for Finance and Operationsissa että Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="26362-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="26362-107">(Tulevaisuudessa Microsoft julkaisee kaksoiskirjoitusalustan toiminnallisuuden nimeltä Alkusynronointi. Tämä ominaisuus tekee tietojen kertasynkronoinnin Finance and Operationsin ja Common Data Servicen välillä osana kaksoiskirjoituksen määritystä.)</span><span class="sxs-lookup"><span data-stu-id="26362-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="26362-108">Microsoft julkaisee kaksoiskirjoituksen yhdistämismääritykset kaikille viitetiedoille, mukaan lukien **Maksuehdot** (maksuehdot).</span><span class="sxs-lookup"><span data-stu-id="26362-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="26362-109">Jos sinulla on jo alkuperäiset tiedot yhdessä järjestelmässä, tietueen pieni päivitystoiminto voi laukaista kaksoiskirjoitustoiminnon kyseiseen tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="26362-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="26362-110">Sinun on noudatettava seuraavaa järjestystä ja varmistettava, että alkuperäiset tiedot ovat käytettävissä sekä Finance and Operationsissa että Common Data Servicessa.</span><span class="sxs-lookup"><span data-stu-id="26362-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="26362-111">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="26362-111">Vendor</span></span>

<span data-ttu-id="26362-112">Tässä on **Toimittaja**-kohteen suoritusjärjestys:</span><span class="sxs-lookup"><span data-stu-id="26362-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="26362-113">Toimittajaryhmä</span><span class="sxs-lookup"><span data-stu-id="26362-113">Vendor group</span></span>

    1. <span data-ttu-id="26362-114">Maksuehto</span><span class="sxs-lookup"><span data-stu-id="26362-114">Terms of payment</span></span>

        1. <span data-ttu-id="26362-115">Maksupäivä ja -rivit</span><span class="sxs-lookup"><span data-stu-id="26362-115">Payment day and lines</span></span>
        2. <span data-ttu-id="26362-116">Maksusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="26362-116">Payment schedule</span></span>

2. <span data-ttu-id="26362-117">Toimittajan maksutapa</span><span class="sxs-lookup"><span data-stu-id="26362-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="26362-118">Asiakas (organisaatio)</span><span class="sxs-lookup"><span data-stu-id="26362-118">Customer (Organization)</span></span>

<span data-ttu-id="26362-119">Tässä on **Asiakas**-kohteen suoritusjärjestys:</span><span class="sxs-lookup"><span data-stu-id="26362-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="26362-120">Asiakasryhmä</span><span class="sxs-lookup"><span data-stu-id="26362-120">Customer group</span></span>

    1. <span data-ttu-id="26362-121">Maksuehto</span><span class="sxs-lookup"><span data-stu-id="26362-121">Terms of payment</span></span>

        1. <span data-ttu-id="26362-122">Maksupäivä ja -rivit</span><span class="sxs-lookup"><span data-stu-id="26362-122">Payment day and lines</span></span>
        2. <span data-ttu-id="26362-123">Maksu</span><span class="sxs-lookup"><span data-stu-id="26362-123">Payment</span></span> 

2. <span data-ttu-id="26362-124">Asiakkaan maksutapa</span><span class="sxs-lookup"><span data-stu-id="26362-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="26362-125">Yhteyshenkilö (henkilö)</span><span class="sxs-lookup"><span data-stu-id="26362-125">Contact (Person)</span></span>

<span data-ttu-id="26362-126">Tässä on **Yhteyshenkilö**-kohteen suoritusjärjestys:</span><span class="sxs-lookup"><span data-stu-id="26362-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="26362-127">Asiakas</span><span class="sxs-lookup"><span data-stu-id="26362-127">Customer</span></span>
2. <span data-ttu-id="26362-128">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="26362-128">Vendor</span></span>
