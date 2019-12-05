---
title: Finance and Operations -sovellusten ja Common Data Servicen alkuperäisen synkronoinnin toteuttamisjärjestys
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
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769634"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="9135d-103">Finance and Operations -sovellusten ja Common Data Servicen alkuperäisen synkronoinnin toteuttamisjärjestys</span><span class="sxs-lookup"><span data-stu-id="9135d-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9135d-104">Ennen kuin käytät tietojen integrointia, sinun on luotava asiakkaille, toimittajille ja yhteyshenkilöille tarvittavat alkuperäiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="9135d-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="9135d-105">Haluat esimerkiksi luoda uuden **Toimittajaryhmä**-nimikkeen ja määrittää sen **Maksuehdot**-arvoksi **Net30**.</span><span class="sxs-lookup"><span data-stu-id="9135d-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="9135d-106">Varmista tässä tapauksessa ennen **Toimittajaryhmä**-nimikkeen luomisen yrittämistä, että **Net30** on sekä sovelluksessa että Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="9135d-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="9135d-107">(Microsoft julkaisee tulevaisuudessa kaksoiskirjoitusalustan toiminnallisuuden nimeltä Alkusynkronointi. Tämä toiminto synkronoi tiedot kerran sovelluksen ja Common Data Servicen välillä osana kaksoiskirjoituksen määritystä.)</span><span class="sxs-lookup"><span data-stu-id="9135d-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="9135d-108">Microsoft julkaisee kaksoiskirjoituksen yhdistämismääritykset kaikille viitetiedoille, mukaan lukien **Maksuehdot** (maksuehdot).</span><span class="sxs-lookup"><span data-stu-id="9135d-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="9135d-109">Jos sinulla on jo alkuperäiset tiedot yhdessä järjestelmässä, tietueen pieni päivitystoiminto voi laukaista kaksoiskirjoitustoiminnon kyseiseen tietueeseen.</span><span class="sxs-lookup"><span data-stu-id="9135d-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="9135d-110">Sinun on noudatettava seuraavaa järjestystä ja varmistettava, että alkuperäiset tiedot ovat käytettävissä sekä sovelluksessa että Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="9135d-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="9135d-111">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="9135d-111">Vendor</span></span>

<span data-ttu-id="9135d-112">Tässä on **Toimittaja**-kohteen suoritusjärjestys:</span><span class="sxs-lookup"><span data-stu-id="9135d-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="9135d-113">Toimittajaryhmä</span><span class="sxs-lookup"><span data-stu-id="9135d-113">Vendor group</span></span>

    1. <span data-ttu-id="9135d-114">Maksuehto</span><span class="sxs-lookup"><span data-stu-id="9135d-114">Terms of payment</span></span>

        1. <span data-ttu-id="9135d-115">Maksupäivä ja -rivit</span><span class="sxs-lookup"><span data-stu-id="9135d-115">Payment day and lines</span></span>
        2. <span data-ttu-id="9135d-116">Maksusuunnitelma</span><span class="sxs-lookup"><span data-stu-id="9135d-116">Payment schedule</span></span>

2. <span data-ttu-id="9135d-117">Toimittajan maksutapa</span><span class="sxs-lookup"><span data-stu-id="9135d-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="9135d-118">Asiakas (organisaatio)</span><span class="sxs-lookup"><span data-stu-id="9135d-118">Customer (Organization)</span></span>

<span data-ttu-id="9135d-119">Tässä on **Asiakas**-kohteen suoritusjärjestys:</span><span class="sxs-lookup"><span data-stu-id="9135d-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="9135d-120">Asiakasryhmä</span><span class="sxs-lookup"><span data-stu-id="9135d-120">Customer group</span></span>

    1. <span data-ttu-id="9135d-121">Maksuehto</span><span class="sxs-lookup"><span data-stu-id="9135d-121">Terms of payment</span></span>

        1. <span data-ttu-id="9135d-122">Maksupäivä ja -rivit</span><span class="sxs-lookup"><span data-stu-id="9135d-122">Payment day and lines</span></span>
        2. <span data-ttu-id="9135d-123">Maksu</span><span class="sxs-lookup"><span data-stu-id="9135d-123">Payment</span></span> 

2. <span data-ttu-id="9135d-124">Asiakkaan maksutapa</span><span class="sxs-lookup"><span data-stu-id="9135d-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="9135d-125">Yhteyshenkilö (henkilö)</span><span class="sxs-lookup"><span data-stu-id="9135d-125">Contact (Person)</span></span>

<span data-ttu-id="9135d-126">Tässä on **Yhteyshenkilö**-kohteen suoritusjärjestys:</span><span class="sxs-lookup"><span data-stu-id="9135d-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="9135d-127">Asiakas</span><span class="sxs-lookup"><span data-stu-id="9135d-127">Customer</span></span>
2. <span data-ttu-id="9135d-128">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="9135d-128">Vendor</span></span>
