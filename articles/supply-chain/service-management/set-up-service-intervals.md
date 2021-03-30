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
ms.openlocfilehash: aee440226c4bda40f9f14b3b6b1edc2cc495574d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242466"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="dc0b1-103">Huoltovälien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dc0b1-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc0b1-104">Huoltoväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="dc0b1-105">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltovälit**.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="dc0b1-106">Luo uusi huoltoväli.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-106">Create a new service interval.</span></span>
3. <span data-ttu-id="dc0b1-107">Anna huoltovälin tunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="dc0b1-108">Valitse alue **Alue**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="dc0b1-109">Kirjoita **Tiheys**-kenttään tiheys.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="dc0b1-110">Tiheys on tekijä, jolla alue on kerrottava, jotta huoltosopimusväli saadaan.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="dc0b1-111">Tallenna huoltoväli näppäinyhdistelmällä **Alt+S**.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="dc0b1-112">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="dc0b1-112">Example</span></span>

<span data-ttu-id="dc0b1-113">Haluat luoda 10 päivän huoltovälin.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="dc0b1-114">**10 päivän huoltovälin luonti**</span><span class="sxs-lookup"><span data-stu-id="dc0b1-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="dc0b1-115">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltovälit**.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="dc0b1-116">Luo uusi huoltoväli.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-116">Create a new service interval.</span></span>
3. <span data-ttu-id="dc0b1-117">Anna huoltovälin tunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="dc0b1-118">Valitse **Alue**-kentässä **Päivittäin**.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="dc0b1-119">Kirjoita **Tiheys**-kenttään 10.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="dc0b1-120">Tallenna huoltoväli näppäinyhdistelmällä **Alt+S**.</span><span class="sxs-lookup"><span data-stu-id="dc0b1-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc0b1-121">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="dc0b1-121">Related topics</span></span>

[<span data-ttu-id="dc0b1-122">Huoltovälit </span><span class="sxs-lookup"><span data-stu-id="dc0b1-122">Service intervals</span></span>](service-intervals.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]