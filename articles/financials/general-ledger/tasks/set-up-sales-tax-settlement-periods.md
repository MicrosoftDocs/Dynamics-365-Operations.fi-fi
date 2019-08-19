---
title: Määritä arvonlisäveron tilityskaudet
description: Arvonlisäveron tilityskaudet sisältävät tietoja kausiväleistä, joilta arvonlisävero on raportoitava ja maksettava.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862985"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="f650d-103">Määritä arvonlisäveron tilityskaudet</span><span class="sxs-lookup"><span data-stu-id="f650d-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f650d-104">Arvonlisäveron tilityskaudet sisältävät tietoja kausiväleistä, joilta arvonlisävero on raportoitava ja maksettava.</span><span class="sxs-lookup"><span data-stu-id="f650d-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="f650d-105">Tilitysprosessi voidaan suorittaa tietyn päivämäärävälin tilityskaudelle.</span><span class="sxs-lookup"><span data-stu-id="f650d-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="f650d-106">Kaikki tilityskauteen liittyvät verokoodit on tilitettävä.</span><span class="sxs-lookup"><span data-stu-id="f650d-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="f650d-107">Liittyvän arvonlisäveroviranomaisen määrityksestä riippuen verovelka kirjataan joko toimittajan tilille tai kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="f650d-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="f650d-108">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="f650d-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="f650d-109">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveron tilityskaudet.</span><span class="sxs-lookup"><span data-stu-id="f650d-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="f650d-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f650d-110">Click New.</span></span>
3. <span data-ttu-id="f650d-111">Kirjoita arvo Tilityskausi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f650d-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="f650d-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f650d-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f650d-113">Valitse Viranomainen-kentästä arvonlisäveroviranomainen, joka vastaanottaa tilityskaudelle luodut raportit ja maksut.</span><span class="sxs-lookup"><span data-stu-id="f650d-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="f650d-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f650d-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f650d-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f650d-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f650d-116">Avaa haku valitsemalla Maksuehdot-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f650d-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f650d-117">Liittyvä arvonlisäveroviranomainen voidaan määrittää toimittajaksi. Arvonlisäveron tilitys luo avoimen toimittajan laskun.</span><span class="sxs-lookup"><span data-stu-id="f650d-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="f650d-118">Maksuehdot määrittävät avoimen toimittajan laskun eräpäivän.</span><span class="sxs-lookup"><span data-stu-id="f650d-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="f650d-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f650d-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f650d-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f650d-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f650d-121">Valitse tilityskauden välien tyyppi.</span><span class="sxs-lookup"><span data-stu-id="f650d-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="f650d-122">Syötä kausivälien yksiköiden määrä kautta kohti.</span><span class="sxs-lookup"><span data-stu-id="f650d-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="f650d-123">Esimerkiksi neljännesvuosi sisältää 3 kuukautta.</span><span class="sxs-lookup"><span data-stu-id="f650d-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="f650d-124">Valitse Käytä arvonlisäveron tilitykseen eräprosessia -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="f650d-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="f650d-125">Tilityskauden tilitysprosessi voidaan käsitellä taustalla erätyönä.</span><span class="sxs-lookup"><span data-stu-id="f650d-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="f650d-126">Tätä suositellaan, jos kausiväli sisältää paljon verotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="f650d-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="f650d-127">Tällä hetkellä tätä ei tueta Itävallassa, Belgiassa, Espanjassa, Italiassa, Japanissa tai Alankomaissa.</span><span class="sxs-lookup"><span data-stu-id="f650d-127">Currently this is not supported in Austria, Belgium, Spain, Italy, Japan, and the Netherlands.</span></span>
14. <span data-ttu-id="f650d-128">Valitse Estä verotapahtumien vastakirjauksien luonti -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="f650d-128">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="f650d-129">Järjestelmä luo oletusarvoisesti verotapahtumien vastakirjauksia selvitysprosessin aikana, mikä voi heikentää suorituskykyä, jos kausiväliin sisältyy suuri määrä verotapahtumia.</span><span class="sxs-lookup"><span data-stu-id="f650d-129">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="f650d-130">Estä verotapahtumien vastakirjauksien luonti valitsemalla tämä valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f650d-130">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="f650d-131">Laajenna Kausivälit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f650d-131">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="f650d-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f650d-132">Click Add.</span></span>
17. <span data-ttu-id="f650d-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f650d-133">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="f650d-134">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f650d-134">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="f650d-135">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f650d-135">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="f650d-136">Valitse Uusi kausiväli.</span><span class="sxs-lookup"><span data-stu-id="f650d-136">Click New period interval.</span></span>
    * <span data-ttu-id="f650d-137">Kun ensimmäinen kausiväli on syötetty, uudet kaudet voidaan luoda automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="f650d-137">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="f650d-138">Voit siirtyä takaisin ja lisätä tarvittaessa uusia kausivälejä.</span><span class="sxs-lookup"><span data-stu-id="f650d-138">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="f650d-139">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f650d-139">Close the page.</span></span>

