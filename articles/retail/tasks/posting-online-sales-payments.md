--- 
title: Online-myynti- ja maksujen kirjaaminen
description: "Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="a8ec9-103">Online-myynti- ja maksujen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="a8ec9-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a8ec9-104">Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="a8ec9-105">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a8ec9-106">Siirry kohtaan Kaikki työtilat > Vähittäismyymälän myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="a8ec9-107">Valitse Synkronoi tilaukset.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="a8ec9-108">Valitse Organisaatiohierarkia-kentässä Vähittäismyymälät alueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="a8ec9-109">Valitse tietty verkkokauppa tai solmu, jos haluat luoda myymäläryhmälle erätyön.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="a8ec9-110">Lisää valinta nuolen avulla.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="a8ec9-111">Valitse Laajenna Suorita taustalla -välilehti.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="a8ec9-112">Valitse Eräkäsittely-valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="a8ec9-113">Valitse Toistuminen.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-113">Click Recurrence.</span></span>
7. <span data-ttu-id="a8ec9-114">Valitse päättymispäivämääräasetuksen arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-114">Select the No end date option.</span></span>
8. <span data-ttu-id="a8ec9-115">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="a8ec9-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-116">Click OK.</span></span>
10. <span data-ttu-id="a8ec9-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a8ec9-117">Click OK.</span></span>


