---
title: Useiden käyttöomaisuuserien poistokäytäntöjen muuttaminen
description: Tässä tehtävässä päivitetään määritetyn käyttöomaisuusryhmän poistomenetelmä.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177512"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="dcdad-103">Useiden käyttöomaisuuserien poistokäytäntöjen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="dcdad-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dcdad-104">Tässä tehtävässä päivitetään määritetyn käyttöomaisuusryhmän poistomenetelmä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="dcdad-105">Tässä tehtävän ohjauksessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="dcdad-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="dcdad-106">Siirry kohtaan Käyttöomaisuus > Kausittaiset tehtävät > Joukkopäivitys</span><span class="sxs-lookup"><span data-stu-id="dcdad-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="dcdad-107">Avaa haku valitsemalla Poistokirja-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="dcdad-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="dcdad-108">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dcdad-109">Syötä Käyttöönoton alku -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="dcdad-110">Syötä Käyttöönoton loppu -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="dcdad-111">Vain se käyttöomaisuuserä, joka sisältyy valitsemaasi poistokirjaan ja joka on otettu käyttöön määrittämiesi päivämäärien välillä, päivitetään.</span><span class="sxs-lookup"><span data-stu-id="dcdad-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="dcdad-112">Valitse vaihtoehto Nykyinen poistomenetelmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="dcdad-113">Vain käyttöomaisuuserä, jolla on nykyinen poistomenetelmä, päivitetään.</span><span class="sxs-lookup"><span data-stu-id="dcdad-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="dcdad-114">Valitse vaihtoehto Uusi poistomenetelmä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="dcdad-115">Tarkista, että raportti tulostetaan haluttuun kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="dcdad-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="dcdad-116">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="dcdad-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="dcdad-117">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="dcdad-117">Click Filter.</span></span>
10. <span data-ttu-id="dcdad-118">Valitse luettelosta käyttöomaisuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="dcdad-119">Avaa haku valitsemalla Ehdot-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="dcdad-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="dcdad-120">Valitse haluttu käyttöomaisuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="dcdad-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="dcdad-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="dcdad-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dcdad-122">Click OK.</span></span>
15. <span data-ttu-id="dcdad-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="dcdad-123">Click OK.</span></span>
    *  <span data-ttu-id="dcdad-124">Käsittelyn tulokset näytetään joukkopäivitysraportissa.</span><span class="sxs-lookup"><span data-stu-id="dcdad-124">Results of the process are shown on the Mass update report.</span></span>     

