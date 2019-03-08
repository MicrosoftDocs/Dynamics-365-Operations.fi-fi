---
title: Kalenterin ja työaikojen luominen
description: Kalenterit kuvaavat operatiivisten resurssien kapasiteetin ja työajat.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a556367857890acdb926ed29518cf2f2f2b92ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "336011"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="fa2e4-103">Kalenterin ja työaikojen luominen</span><span class="sxs-lookup"><span data-stu-id="fa2e4-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa2e4-104">Kalenterit kuvaavat operatiivisten resurssien kapasiteetin ja työajat.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="fa2e4-105">Tämä menettely auttaa määrittämään työkalenterin työaikamallin perusteella.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="fa2e4-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="fa2e4-107">Siirry kohtaan Kaikki työtilat > Resurssin elinkaaren hallinta.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="fa2e4-108">Valitse Kalenterit.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-108">Click Calendars.</span></span>
3. <span data-ttu-id="fa2e4-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-109">Click New.</span></span>
4. <span data-ttu-id="fa2e4-110">Kirjoita Kalenteri-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="fa2e4-111">Tämä on kalenterin tunnus, jota käytetään viitteenä, kun kalentereita määritetään esimerkiksi operatiiviseen resurssiin tai resurssiryhmään.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="fa2e4-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="fa2e4-113">Lisää Tavallisen työpäivän kesto tunteina -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="fa2e4-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="fa2e4-115">Valitse Työajat.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-115">Click Working times.</span></span>
9. <span data-ttu-id="fa2e4-116">Valitse Kokoa työajat.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-116">Click Compose working times.</span></span>
    * <span data-ttu-id="fa2e4-117">Luo työtunnit jokaiselle päivälle kautena, jolloin haluat ajoittaa töitä.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="fa2e4-118">Ajan mittaan voit luo työaikoja lisäkausille.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="fa2e4-119">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="fa2e4-120">Tämä on ensimmäinen päivä, jolloin kalenterin on oltava avoinna.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="fa2e4-121">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="fa2e4-122">Tämä on viimeinen päivä, jolloin kalenteri on avoinna.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="fa2e4-123">Anna tai valitse Työaikamalli-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="fa2e4-124">Työaikamalli määrittää työtunnit viikon jokaiselle päivälle.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="fa2e4-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-125">Click OK.</span></span>
14. <span data-ttu-id="fa2e4-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa2e4-126">Close the page.</span></span>

