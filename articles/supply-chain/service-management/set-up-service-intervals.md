---
title: Huoltovälien määrittäminen
description: Huoltoväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815da6b24de401ad11febb0b0564738ce6967a9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991662"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="448f4-103">Huoltovälien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="448f4-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="448f4-104">Huoltoväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan.</span><span class="sxs-lookup"><span data-stu-id="448f4-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="448f4-105">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltovälit**.</span><span class="sxs-lookup"><span data-stu-id="448f4-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="448f4-106">Luo uusi huoltoväli.</span><span class="sxs-lookup"><span data-stu-id="448f4-106">Create a new service interval.</span></span>
3. <span data-ttu-id="448f4-107">Anna huoltovälin tunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="448f4-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="448f4-108">Valitse alue **Alue**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="448f4-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="448f4-109">Kirjoita **Tiheys**-kenttään tiheys.</span><span class="sxs-lookup"><span data-stu-id="448f4-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="448f4-110">Tiheys on tekijä, jolla alue on kerrottava, jotta huoltosopimusväli saadaan.</span><span class="sxs-lookup"><span data-stu-id="448f4-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="448f4-111">Tallenna huoltoväli näppäinyhdistelmällä **Alt+S**.</span><span class="sxs-lookup"><span data-stu-id="448f4-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="448f4-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="448f4-112">Example</span></span>

<span data-ttu-id="448f4-113">Haluat luoda 10 päivän huoltovälin.</span><span class="sxs-lookup"><span data-stu-id="448f4-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="448f4-114">**10 päivän huoltovälin luonti**</span><span class="sxs-lookup"><span data-stu-id="448f4-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="448f4-115">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltovälit**.</span><span class="sxs-lookup"><span data-stu-id="448f4-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="448f4-116">Luo uusi huoltoväli.</span><span class="sxs-lookup"><span data-stu-id="448f4-116">Create a new service interval.</span></span>
3. <span data-ttu-id="448f4-117">Anna huoltovälin tunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="448f4-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="448f4-118">Valitse **Alue**-kentässä **Päivittäin**.</span><span class="sxs-lookup"><span data-stu-id="448f4-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="448f4-119">Kirjoita **Tiheys**-kenttään 10.</span><span class="sxs-lookup"><span data-stu-id="448f4-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="448f4-120">Tallenna huoltoväli näppäinyhdistelmällä **Alt+S**.</span><span class="sxs-lookup"><span data-stu-id="448f4-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="448f4-121">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="448f4-121">Related topics</span></span>

[<span data-ttu-id="448f4-122">Huoltovälit </span><span class="sxs-lookup"><span data-stu-id="448f4-122">Service intervals</span></span>](service-intervals.md)  
