---
title: "Huoltovälien määrittäminen"
description: "Huoltoväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 03ebf4fd4615eac77e6f990a2d4e7f7326c0d257
ms.contentlocale: fi-fi
ms.lasthandoff: 02/20/2018

---

# <a name="set-up-service-intervals"></a><span data-ttu-id="37479-103">Huoltovälien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="37479-103">Set up service intervals</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37479-104">Huoltoväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan.</span><span class="sxs-lookup"><span data-stu-id="37479-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="37479-105">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltovälit**.</span><span class="sxs-lookup"><span data-stu-id="37479-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="37479-106">Luo uusi huoltoväli.</span><span class="sxs-lookup"><span data-stu-id="37479-106">Create a new service interval.</span></span>
3. <span data-ttu-id="37479-107">Anna huoltovälin tunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="37479-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="37479-108">Valitse alue **Alue**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="37479-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="37479-109">Kirjoita **Tiheys**-kenttään tiheys.</span><span class="sxs-lookup"><span data-stu-id="37479-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="37479-110">Tiheys on tekijä, jolla alue on kerrottava, jotta huoltosopimusväli saadaan.</span><span class="sxs-lookup"><span data-stu-id="37479-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="37479-111">Tallenna huoltoväli näppäinyhdistelmällä **Alt+S**.</span><span class="sxs-lookup"><span data-stu-id="37479-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="37479-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="37479-112">Example</span></span>

<span data-ttu-id="37479-113">Haluat luoda 10 päivän huoltovälin.</span><span class="sxs-lookup"><span data-stu-id="37479-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="37479-114">**10 päivän huoltovälin luonti**</span><span class="sxs-lookup"><span data-stu-id="37479-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="37479-115">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltovälit**.</span><span class="sxs-lookup"><span data-stu-id="37479-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="37479-116">Luo uusi huoltoväli.</span><span class="sxs-lookup"><span data-stu-id="37479-116">Create a new service interval.</span></span>
3. <span data-ttu-id="37479-117">Anna huoltovälin tunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="37479-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="37479-118">Valitse **Alue**-kentässä **Päivittäin**.</span><span class="sxs-lookup"><span data-stu-id="37479-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="37479-119">Kirjoita **Tiheys**-kenttään 10.</span><span class="sxs-lookup"><span data-stu-id="37479-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="37479-120">Tallenna huoltoväli näppäinyhdistelmällä **Alt+S**.</span><span class="sxs-lookup"><span data-stu-id="37479-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37479-121">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="37479-121">Related topics</span></span>

[<span data-ttu-id="37479-122">Huoltovälit </span><span class="sxs-lookup"><span data-stu-id="37479-122">Service intervals</span></span>](service-intervals.md)  
