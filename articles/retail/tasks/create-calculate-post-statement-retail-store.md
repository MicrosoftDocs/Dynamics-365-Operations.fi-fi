--- 
title: "Luo, laske ja kirjaa laskelmat vähittäismyymälälle"
description: "Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 1c31c849c4c72762f0fdeb3f1d256cd3529394b2
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="4fe61-103">Luo, laske ja kirjaa laskelmat vähittäismyymälälle</span><span class="sxs-lookup"><span data-stu-id="4fe61-103">Create, calculate, and post statements for a retail store</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4fe61-104">Tässä menettelyssä kerrotaan myymälän laskelman luomisen, laskemisen ja kirjaamisen manuaaliset vaiheet.</span><span class="sxs-lookup"><span data-stu-id="4fe61-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="4fe61-105">Samalle tehtävälle voidaan määrittää myös erätöitä.</span><span class="sxs-lookup"><span data-stu-id="4fe61-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="4fe61-106">Erätöiden määrittämisen ja suorittamisen vaiheet löytyvät myös muista aiheista.</span><span class="sxs-lookup"><span data-stu-id="4fe61-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="4fe61-107">Tämän menettelyn suorittaminen edellyttää myyntipisteellä tehtyjä ja Dynamics AX:ään siirrettyjä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="4fe61-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="4fe61-108">Tämä tallenne käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="4fe61-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="4fe61-109">Tämä ohje voi viitata Microsoft Dynamics AX -nimeen.</span><span class="sxs-lookup"><span data-stu-id="4fe61-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="4fe61-110">Huomaa, että Dynamics AX on nyt nimeltään Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="4fe61-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="4fe61-111">Valitse Kaikki työtilat > ..</span><span class="sxs-lookup"><span data-stu-id="4fe61-111">Go to All workspaces > ..</span></span> <span data-ttu-id="4fe61-112">> Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="4fe61-112">> Retail store financials.</span></span>
2. <span data-ttu-id="4fe61-113">Valitse Uusi laskelma.</span><span class="sxs-lookup"><span data-stu-id="4fe61-113">Click New statement.</span></span>
3. <span data-ttu-id="4fe61-114">Avaa haku valitsemalla Myymälä numero -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4fe61-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4fe61-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4fe61-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4fe61-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4fe61-116">Click OK.</span></span>
    * <span data-ttu-id="4fe61-117">Asetusryhmässä on asetuksia, jotka ohjaavat laskelmaan sisällytettävien tapahtumien valintaa sekä tapahtumien laskentariveiksi ryhmittelyä.</span><span class="sxs-lookup"><span data-stu-id="4fe61-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="4fe61-118">Voit avata asetusryhmän ja muuttaa asetuksia tai käyttää oletusarvoja.</span><span class="sxs-lookup"><span data-stu-id="4fe61-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="4fe61-119">Laskelmatapa-kentässä määritetään, miten laskelmarivit ryhmitellään.</span><span class="sxs-lookup"><span data-stu-id="4fe61-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="4fe61-120">Valitse henkilökunnan jäsen tai kassakone, jos haluat tehdä laskelman vain tietylle henkilökunnan jäsenelle tai kassakoneelle.</span><span class="sxs-lookup"><span data-stu-id="4fe61-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="4fe61-121">Valitse vaihtoehto Sulkemistapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="4fe61-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="4fe61-122">Valitse Laske laskelma.</span><span class="sxs-lookup"><span data-stu-id="4fe61-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="4fe61-123">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="4fe61-123">Click Yes.</span></span>
    * <span data-ttu-id="4fe61-124">Kun laskelma on tehty, jokaiselle käytetylle maksu- ja laskelmatavalle on luotu rivejä, jotka sisältävät kokonaissummat.</span><span class="sxs-lookup"><span data-stu-id="4fe61-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="4fe61-125">Voit syöttää kullekin riville lasketun summan, jos summia on syötettävä tai päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="4fe61-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="4fe61-126">Laskettuun kenttää siirretään myyntipisteellä kassan maksuvälineittäin tehtyjen laskemistapahtumien summat.</span><span class="sxs-lookup"><span data-stu-id="4fe61-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="4fe61-127">Valitse Kirjaa laskelma.</span><span class="sxs-lookup"><span data-stu-id="4fe61-127">Click Post statement.</span></span>
10. <span data-ttu-id="4fe61-128">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="4fe61-128">Click Close.</span></span>
11. <span data-ttu-id="4fe61-129">Siirry kohtaan Vähittäismyynti ja kauppa > Kanavat > Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="4fe61-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="4fe61-130">Valitse Kirjatut laskelmat -välilehti.</span><span class="sxs-lookup"><span data-stu-id="4fe61-130">Click the Posted statements tab.</span></span>


