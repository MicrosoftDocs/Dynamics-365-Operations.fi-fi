---
title: Luo korkoryhmäalue
description: Korkoryhmät voidaan määrittää laskemaan eri korkosummat arvoalueiden perusteella.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d684eedd5b40ee9775ab779c243d05cdc6e01f58
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188852"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="51843-103">Luo korkoryhmäalue</span><span class="sxs-lookup"><span data-stu-id="51843-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51843-104">Korkoryhmät voidaan määrittää laskemaan eri korkosummat arvoalueiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="51843-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="51843-105">Tämä menettely näyttää, miten korkoryhmä lisätään ja miten siihen lisätään alue.</span><span class="sxs-lookup"><span data-stu-id="51843-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="51843-106">Valitse Luotonvalvonta > Korko > Korkokoodien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="51843-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="51843-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="51843-107">Click New.</span></span>
3. <span data-ttu-id="51843-108">Kirjoita Korkoryhmä-kenttään korkoryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="51843-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="51843-109">Kirjoita Kuvaus-kenttään korkoryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="51843-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="51843-110">Valitse Kuukausi.</span><span class="sxs-lookup"><span data-stu-id="51843-110">Select Month.</span></span>
6. <span data-ttu-id="51843-111">Laajenna Ansiot-osa.</span><span class="sxs-lookup"><span data-stu-id="51843-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="51843-112">Laajenna Ansiot valuutan mukaan -osa.</span><span class="sxs-lookup"><span data-stu-id="51843-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="51843-113">Määritä Kirjanpitotili-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="51843-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="51843-114">Valitse Korko alueen mukaan -kentässä Kuukautta.</span><span class="sxs-lookup"><span data-stu-id="51843-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="51843-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="51843-115">Click Add.</span></span>
11. <span data-ttu-id="51843-116">Kirjoita tämän valuutan ja alueen kuvaus Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="51843-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="51843-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="51843-117">Click Save.</span></span>
13. <span data-ttu-id="51843-118">Valitse Alueet.</span><span class="sxs-lookup"><span data-stu-id="51843-118">Click Ranges.</span></span>
14. <span data-ttu-id="51843-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="51843-119">Click New.</span></span>
15. <span data-ttu-id="51843-120">Anna ensin Arvosta-asetukseksi 0 ja sitten kuukausikorkoprosentti, jolla korko lasketaan.</span><span class="sxs-lookup"><span data-stu-id="51843-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="51843-121">Esimerkissä se on 1,5.</span><span class="sxs-lookup"><span data-stu-id="51843-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="51843-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="51843-122">Click New.</span></span>
17. <span data-ttu-id="51843-123">Anna seuraavaksi Arvosta-asetukseksi 4, joka on ensimmäinen kuukausi, jolla uusi korkosumma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="51843-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="51843-124">Anna kuukausikorkoprosentti, jolla lasketaan korko kuukaudesta 4 alkaen.</span><span class="sxs-lookup"><span data-stu-id="51843-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="51843-125">Tässä esimerkissä se on 2,0.</span><span class="sxs-lookup"><span data-stu-id="51843-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="51843-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="51843-126">Click New.</span></span>
20. <span data-ttu-id="51843-127">Anna seuraavaksi Arvosta-asetukseksi 7, joka on seuraava kuukausi, jolla uusi korkosumma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="51843-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="51843-128">Anna kuukausikorkoprosentti, jolla lasketaan korko kuukaudesta 7 alkaen.</span><span class="sxs-lookup"><span data-stu-id="51843-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="51843-129">Tässä esimerkissä se on 2,5.</span><span class="sxs-lookup"><span data-stu-id="51843-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="51843-130">Lopeta asetusten määritys valitsemalla Sulje.</span><span class="sxs-lookup"><span data-stu-id="51843-130">Click Close to complete the setup.</span></span>

