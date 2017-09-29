--- 
title: "Useiden käyttöomaisuuserien poistokäytäntöjen muuttaminen"
description: "Tässä tehtävässä päivitetään määritetyn käyttöomaisuusryhmän poistomenetelmä."
author: saraschi2
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
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0f711d2e18a13ab972e548d3304652dee3f2e406
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="38af3-103">Useiden käyttöomaisuuserien poistokäytäntöjen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="38af3-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38af3-104">Tässä tehtävässä päivitetään määritetyn käyttöomaisuusryhmän poistomenetelmä.</span><span class="sxs-lookup"><span data-stu-id="38af3-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="38af3-105">Tässä tehtävän ohjauksessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="38af3-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="38af3-106">Siirry kohtaan Käyttöomaisuus > Kausittaiset tehtävät > Joukkopäivitys</span><span class="sxs-lookup"><span data-stu-id="38af3-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="38af3-107">Avaa haku valitsemalla Poistokirja-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="38af3-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="38af3-108">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="38af3-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="38af3-109">Syötä Käyttöönoton alku -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="38af3-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="38af3-110">Syötä Käyttöönoton loppu -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="38af3-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="38af3-111">Vain se käyttöomaisuuserä, joka sisältyy valitsemaasi poistokirjaan ja joka on otettu käyttöön määrittämiesi päivämäärien välillä, päivitetään.</span><span class="sxs-lookup"><span data-stu-id="38af3-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="38af3-112">Valitse vaihtoehto Nykyinen poistomenetelmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="38af3-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="38af3-113">Vain käyttöomaisuuserä, jolla on nykyinen poistomenetelmä, päivitetään.</span><span class="sxs-lookup"><span data-stu-id="38af3-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="38af3-114">Valitse vaihtoehto Uusi poistomenetelmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="38af3-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="38af3-115">Tarkista, että raportti tulostetaan haluttuun kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="38af3-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="38af3-116">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="38af3-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="38af3-117">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="38af3-117">Click Filter.</span></span>
10. <span data-ttu-id="38af3-118">Valitse luettelosta käyttöomaisuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="38af3-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="38af3-119">Avaa haku valitsemalla Ehdot-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="38af3-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="38af3-120">Valitse haluttu käyttöomaisuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="38af3-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="38af3-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="38af3-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="38af3-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38af3-122">Click OK.</span></span>
15. <span data-ttu-id="38af3-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38af3-123">Click OK.</span></span>
    *  <span data-ttu-id="38af3-124">Käsittelyn tulokset näytetään joukkopäivitysraportissa.</span><span class="sxs-lookup"><span data-stu-id="38af3-124">Results of the process are shown on the Mass update report.</span></span>     


