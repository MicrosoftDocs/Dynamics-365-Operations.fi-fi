--- 
title: "Luo korkoryhmäalue"
description: "Korkoryhmät voidaan määrittää laskemaan eri korkosummat arvoalueiden perusteella."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 05ca41dd5d660e9f0ef72ee5bd49d800645081a5
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="a9bce-103">Luo korkoryhmäalue</span><span class="sxs-lookup"><span data-stu-id="a9bce-103">Create an interest code with a range</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9bce-104">Korkoryhmät voidaan määrittää laskemaan eri korkosummat arvoalueiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="a9bce-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="a9bce-105">Tämä menettely näyttää, miten korkoryhmä lisätään ja miten siihen lisätään alue.</span><span class="sxs-lookup"><span data-stu-id="a9bce-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="a9bce-106">Valitse Luotonvalvonta > Korko > Korkokoodien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="a9bce-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="a9bce-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a9bce-107">Click New.</span></span>
3. <span data-ttu-id="a9bce-108">Kirjoita Korkoryhmä-kenttään korkoryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="a9bce-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="a9bce-109">Kirjoita Kuvaus-kenttään korkoryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a9bce-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="a9bce-110">Valitse Kuukausi.</span><span class="sxs-lookup"><span data-stu-id="a9bce-110">Select Month.</span></span>
6. <span data-ttu-id="a9bce-111">Laajenna Ansiot-osa.</span><span class="sxs-lookup"><span data-stu-id="a9bce-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="a9bce-112">Laajenna Ansiot valuutan mukaan -osa.</span><span class="sxs-lookup"><span data-stu-id="a9bce-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="a9bce-113">Määritä Kirjanpitotili-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="a9bce-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="a9bce-114">Valitse Korko alueen mukaan -kentässä Kuukautta.</span><span class="sxs-lookup"><span data-stu-id="a9bce-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="a9bce-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a9bce-115">Click Add.</span></span>
11. <span data-ttu-id="a9bce-116">Kirjoita tämän valuutan ja alueen kuvaus Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a9bce-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="a9bce-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a9bce-117">Click Save.</span></span>
13. <span data-ttu-id="a9bce-118">Valitse Alueet.</span><span class="sxs-lookup"><span data-stu-id="a9bce-118">Click Ranges.</span></span>
14. <span data-ttu-id="a9bce-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a9bce-119">Click New.</span></span>
15. <span data-ttu-id="a9bce-120">Anna ensin Arvosta-asetukseksi 0 ja sitten kuukausikorkoprosentti, jolla korko lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a9bce-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="a9bce-121">Esimerkissä se on 1,5.</span><span class="sxs-lookup"><span data-stu-id="a9bce-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="a9bce-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a9bce-122">Click New.</span></span>
17. <span data-ttu-id="a9bce-123">Anna seuraavaksi Arvosta-asetukseksi 4, joka on ensimmäinen kuukausi, jolla uusi korkosumma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a9bce-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="a9bce-124">Anna kuukausikorkoprosentti, jolla lasketaan korko kuukaudesta 4 alkaen.</span><span class="sxs-lookup"><span data-stu-id="a9bce-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="a9bce-125">Tässä esimerkissä se on 2,0.</span><span class="sxs-lookup"><span data-stu-id="a9bce-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="a9bce-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a9bce-126">Click New.</span></span>
20. <span data-ttu-id="a9bce-127">Anna seuraavaksi Arvosta-asetukseksi 7, joka on seuraava kuukausi, jolla uusi korkosumma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a9bce-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="a9bce-128">Anna kuukausikorkoprosentti, jolla lasketaan korko kuukaudesta 7 alkaen.</span><span class="sxs-lookup"><span data-stu-id="a9bce-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="a9bce-129">Tässä esimerkissä se on 2,5.</span><span class="sxs-lookup"><span data-stu-id="a9bce-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="a9bce-130">Lopeta asetusten määritys valitsemalla Sulje.</span><span class="sxs-lookup"><span data-stu-id="a9bce-130">Click Close to complete the setup.</span></span>


