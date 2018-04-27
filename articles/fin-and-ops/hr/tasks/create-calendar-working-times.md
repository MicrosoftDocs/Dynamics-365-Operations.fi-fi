--- 
title: "Kalenterin ja työaikojen luominen"
description: "Kalenterit kuvaavat operatiivisten resurssien kapasiteetin ja työajat."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a8dcef8d8ba6f6d41a997b5b0623cb9577ce00d3
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="4ce29-103">Kalenterin ja työaikojen luominen</span><span class="sxs-lookup"><span data-stu-id="4ce29-103">Create a calendar and generate working times</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ce29-104">Kalenterit kuvaavat operatiivisten resurssien kapasiteetin ja työajat.</span><span class="sxs-lookup"><span data-stu-id="4ce29-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="4ce29-105">Tämä menettely auttaa määrittämään työkalenterin työaikamallin perusteella.</span><span class="sxs-lookup"><span data-stu-id="4ce29-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="4ce29-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="4ce29-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="4ce29-107">Siirry kohtaan Kaikki työtilat > Resurssin elinkaaren hallinta.</span><span class="sxs-lookup"><span data-stu-id="4ce29-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="4ce29-108">Valitse Kalenterit.</span><span class="sxs-lookup"><span data-stu-id="4ce29-108">Click Calendars.</span></span>
3. <span data-ttu-id="4ce29-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4ce29-109">Click New.</span></span>
4. <span data-ttu-id="4ce29-110">Kirjoita Kalenteri-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="4ce29-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="4ce29-111">Tämä on kalenterin tunnus, jota käytetään viitteenä, kun kalentereita määritetään esimerkiksi operatiiviseen resurssiin tai resurssiryhmään.</span><span class="sxs-lookup"><span data-stu-id="4ce29-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="4ce29-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4ce29-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="4ce29-113">Lisää Tavallisen työpäivän kesto tunteina -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4ce29-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="4ce29-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="4ce29-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4ce29-115">Valitse Työajat.</span><span class="sxs-lookup"><span data-stu-id="4ce29-115">Click Working times.</span></span>
9. <span data-ttu-id="4ce29-116">Valitse Kokoa työajat.</span><span class="sxs-lookup"><span data-stu-id="4ce29-116">Click Compose working times.</span></span>
    * <span data-ttu-id="4ce29-117">Luo työtunnit jokaiselle päivälle kautena, jolloin haluat ajoittaa töitä.</span><span class="sxs-lookup"><span data-stu-id="4ce29-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="4ce29-118">Ajan mittaan voit luo työaikoja lisäkausille.</span><span class="sxs-lookup"><span data-stu-id="4ce29-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="4ce29-119">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4ce29-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4ce29-120">Tämä on ensimmäinen päivä, jolloin kalenterin on oltava avoinna.</span><span class="sxs-lookup"><span data-stu-id="4ce29-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="4ce29-121">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4ce29-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="4ce29-122">Tämä on viimeinen päivä, jolloin kalenteri on avoinna.</span><span class="sxs-lookup"><span data-stu-id="4ce29-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="4ce29-123">Anna tai valitse Työaikamalli-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="4ce29-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="4ce29-124">Työaikamalli määrittää työtunnit viikon jokaiselle päivälle.</span><span class="sxs-lookup"><span data-stu-id="4ce29-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="4ce29-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4ce29-125">Click OK.</span></span>
14. <span data-ttu-id="4ce29-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4ce29-126">Close the page.</span></span>


