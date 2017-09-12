--- 
title: "Luo, laske ja kirjaa laskelma vähittäismyymälälle"
description: "Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="80e4d-103">Luo, laske ja kirjaa laskelma vähittäismyymälälle</span><span class="sxs-lookup"><span data-stu-id="80e4d-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="80e4d-104">Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.</span><span class="sxs-lookup"><span data-stu-id="80e4d-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="80e4d-105">Samalle tehtävälle voidaan määrittää myös erätöitä.</span><span class="sxs-lookup"><span data-stu-id="80e4d-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="80e4d-106">Erätöiden määrittämisen ja suorittamisen vaiheet löytyvät myös muista aiheista.</span><span class="sxs-lookup"><span data-stu-id="80e4d-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="80e4d-107">Tämän menettelyn suorittaminen edellyttää myyntipisteellä tehtyjä ja Dynamics AX:ään siirrettyjä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="80e4d-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="80e4d-108">Tämä tallenne käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="80e4d-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="80e4d-109">Tämä ohje voi viitata Microsoft Dynamics AX -nimeen.</span><span class="sxs-lookup"><span data-stu-id="80e4d-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="80e4d-110">Huomaa, että Dynamics AX on nyt nimeltään Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="80e4d-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="80e4d-111">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="80e4d-111">Go to All workspaces > ..</span></span> <span data-ttu-id="80e4d-112">> Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="80e4d-112">> Retail store financials.</span></span>
2. <span data-ttu-id="80e4d-113">Valitse Uusi laskelma.</span><span class="sxs-lookup"><span data-stu-id="80e4d-113">Click New statement.</span></span>
3. <span data-ttu-id="80e4d-114">Avaa haku valitsemalla Myymälä numero -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="80e4d-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="80e4d-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="80e4d-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="80e4d-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="80e4d-116">Click OK.</span></span>
    * <span data-ttu-id="80e4d-117">Asetusryhmässä on asetuksia, jotka ohjaavat laskelmaan sisällytettävien tapahtumien valintaa sekä tapahtumien laskentariveiksi ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="80e4d-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="80e4d-118">Voit avata asetusryhmän ja muuttaa asetuksia tai käyttää oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="80e4d-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="80e4d-119">Laskelmatapa-kentässä määritetään, miten laskelmarivit ryhmitellään.</span><span class="sxs-lookup"><span data-stu-id="80e4d-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="80e4d-120">Valitse henkilökunnan jäsen tai kassakone, jos haluat tehdä laskelman vain tietylle henkilökunnan jäsenelle tai kassakoneelle.</span><span class="sxs-lookup"><span data-stu-id="80e4d-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="80e4d-121">Valitse vaihtoehto Sulkemistapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="80e4d-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="80e4d-122">Valitse Laske laskelma.</span><span class="sxs-lookup"><span data-stu-id="80e4d-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="80e4d-123">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="80e4d-123">Click Yes.</span></span>
    * <span data-ttu-id="80e4d-124">Kun laskelma on tehty, jokaiselle käytetylle maksu- ja laskelmatavalle on luotu rivejä, jotka sisältävät kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="80e4d-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="80e4d-125">Voit syöttää kullekin riville lasketun summan, jos summia on syötettävä tai päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="80e4d-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="80e4d-126">Laskettuun kenttää siirretään myyntipisteellä kassan maksuvälineittäin tehtyjen laskemistapahtumien summat.</span><span class="sxs-lookup"><span data-stu-id="80e4d-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="80e4d-127">Valitse Kirjaa laskelma.</span><span class="sxs-lookup"><span data-stu-id="80e4d-127">Click Post statement.</span></span>
10. <span data-ttu-id="80e4d-128">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="80e4d-128">Click Close.</span></span>
11. <span data-ttu-id="80e4d-129">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="80e4d-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="80e4d-130">Valitse Kirjatut laskelmat -välilehti.</span><span class="sxs-lookup"><span data-stu-id="80e4d-130">Click the Posted statements tab.</span></span>


