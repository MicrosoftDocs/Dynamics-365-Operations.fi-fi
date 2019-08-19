---
title: Määritä varastotyön käytännöt (Sovellus, Toukokuu 2016)
description: Varastointiprosessit eivät aina sisällä varastotyötä.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23ad33a2f070a33e4e658870561406c4604f4dce
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847060"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="e25f4-103">Määritä varastotyön käytännöt (Sovellus, Toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="e25f4-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e25f4-104">Varastointiprosessit eivät aina sisällä varastotyötä.</span><span class="sxs-lookup"><span data-stu-id="e25f4-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="e25f4-105">Voit määrittää työn käytännön, joka estää raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonnin tietyille tuotejoukoille tietyissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="e25f4-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="e25f4-106">Tämän tallenteen luomisessa käytetty demotietojen yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="e25f4-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="e25f4-107">Tämä tehtäväopas vaatii Dynamics AX -sovelluksen version 7.0.1 tai sitä uudemman.</span><span class="sxs-lookup"><span data-stu-id="e25f4-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="e25f4-108">Valitse Varastonhallinta > Asetukset > Työ > Työkäytännöt.</span><span class="sxs-lookup"><span data-stu-id="e25f4-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="e25f4-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e25f4-109">Click New.</span></span>
3. <span data-ttu-id="e25f4-110">Kirjoita Työkäytännön nimi -kenttään Ei poispanotyötä.</span><span class="sxs-lookup"><span data-stu-id="e25f4-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="e25f4-111">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e25f4-111">Click Save.</span></span>
5. <span data-ttu-id="e25f4-112">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e25f4-112">Click Add.</span></span>
6. <span data-ttu-id="e25f4-113">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e25f4-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e25f4-114">Valitse Työtilauksen tyyppi -kentässä Valmiiden tuotteiden poispano.</span><span class="sxs-lookup"><span data-stu-id="e25f4-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="e25f4-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e25f4-115">Click Add.</span></span>
9. <span data-ttu-id="e25f4-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e25f4-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="e25f4-117">Valitse Työtilauksen tyyppi -kenttään Rinnakkaistuotteen ja sivutuotteen poispano.</span><span class="sxs-lookup"><span data-stu-id="e25f4-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="e25f4-118">Laajenna Varastosijainnit-osa.</span><span class="sxs-lookup"><span data-stu-id="e25f4-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="e25f4-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e25f4-119">Click Add.</span></span>
13. <span data-ttu-id="e25f4-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e25f4-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e25f4-121">Kirjoita varasto-luetteloon arvo 51.</span><span class="sxs-lookup"><span data-stu-id="e25f4-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="e25f4-122">Syötä tai valitse Sijainti-kentän arvoksi 001.</span><span class="sxs-lookup"><span data-stu-id="e25f4-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="e25f4-123">Laajenna Tuotteet-osa.</span><span class="sxs-lookup"><span data-stu-id="e25f4-123">Expand the Products section.</span></span>
17. <span data-ttu-id="e25f4-124">Valitse Tuotteen valinta -kentän arvoksi Valittu.</span><span class="sxs-lookup"><span data-stu-id="e25f4-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="e25f4-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e25f4-125">Click Add.</span></span>
19. <span data-ttu-id="e25f4-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e25f4-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="e25f4-127">Syötä tai valitse Nimiketunnus-kentän arvoksi L0101.</span><span class="sxs-lookup"><span data-stu-id="e25f4-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="e25f4-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e25f4-128">Click Save.</span></span>

