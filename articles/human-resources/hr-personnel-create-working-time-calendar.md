---
title: Kalenterien ja työaikojen luominen
description: Kalenterit kuvaavat operatiivisten resurssien kapasiteetin ja työajat. Tämä artikkeli auttaa määrittämään työkalenterin työaikamallin perusteella.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38c0482c62e86e3e12e4bdd67f6d8f090ddfbfeb
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008861"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="a710a-104">Kalenterien ja työaikojen luominen</span><span class="sxs-lookup"><span data-stu-id="a710a-104">Create calendars and generate working times</span></span>



<span data-ttu-id="a710a-105">Kalenterit kuvaavat operatiivisten resurssien kapasiteetin ja työajat.</span><span class="sxs-lookup"><span data-stu-id="a710a-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="a710a-106">Tämä artikkeli auttaa määrittämään työkalenterin työaikamallin perusteella.</span><span class="sxs-lookup"><span data-stu-id="a710a-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="a710a-107">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="a710a-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="a710a-108">Valitse aloitussivulla **Resurssin elinkaaren hallinta**.</span><span class="sxs-lookup"><span data-stu-id="a710a-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="a710a-109">Valitse **Kalenterit**.</span><span class="sxs-lookup"><span data-stu-id="a710a-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="a710a-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a710a-110">Select **New**.</span></span>
4. <span data-ttu-id="a710a-111">Luokittele kalenteri **Kalenteri**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a710a-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="a710a-112">Tämä on kalenterin tunnus, jota käytetään viitteenä, kun kalentereita määritetään esimerkiksi operatiiviseen resurssiin tai resurssiryhmään.</span><span class="sxs-lookup"><span data-stu-id="a710a-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="a710a-113">Syötä **Nimi**-kenttään kalenterin nimi.</span><span class="sxs-lookup"><span data-stu-id="a710a-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="a710a-114">Lisää **Tavallisen työpäivän kesto tunteina** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a710a-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="a710a-115">Varmista, että rivi on valittuna, ja valitse sitten **Työajat** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="a710a-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="a710a-116">Valitse **Kokoa työajat**.</span><span class="sxs-lookup"><span data-stu-id="a710a-116">Select **Compose working times**.</span></span> <span data-ttu-id="a710a-117">Luo työtunnit jokaiselle päivälle kautena, jolloin haluat ajoittaa töitä.</span><span class="sxs-lookup"><span data-stu-id="a710a-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="a710a-118">Ajan mittaan voit luo työaikoja lisäkausille.</span><span class="sxs-lookup"><span data-stu-id="a710a-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="a710a-119">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a710a-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="a710a-120">Tämä on ensimmäinen päivä, jolloin kalenterin on oltava avoinna.</span><span class="sxs-lookup"><span data-stu-id="a710a-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="a710a-121">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a710a-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="a710a-122">Tämä on viimeinen päivä, jolloin kalenteri on avoinna.</span><span class="sxs-lookup"><span data-stu-id="a710a-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="a710a-123">Anna tai valitse **Työaikamalli**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="a710a-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="a710a-124">Työaikamalli määrittää työtunnit viikon jokaiselle päivälle.</span><span class="sxs-lookup"><span data-stu-id="a710a-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="a710a-125">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a710a-125">Select **OK**.</span></span>
13. <span data-ttu-id="a710a-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a710a-126">Close the page.</span></span>
