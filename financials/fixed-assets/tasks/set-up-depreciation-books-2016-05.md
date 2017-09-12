--- 
title: "Määritä poistokirjat"
description: "Tässä tehtävän ohjauksessa luodaan uusi poistokirja ja liitetään se käyttöomaisuusryhmään."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: d2001da7b3487a07a91abd406f74558916ac9f23
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="3795c-103">Määritä poistokirjat</span><span class="sxs-lookup"><span data-stu-id="3795c-103">Set up depreciation books</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3795c-104">Tässä tehtävän ohjauksessa luodaan uusi poistokirja ja liitetään se käyttöomaisuusryhmään.</span><span class="sxs-lookup"><span data-stu-id="3795c-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="3795c-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="3795c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="3795c-106">Poistokirjan luominen</span><span class="sxs-lookup"><span data-stu-id="3795c-106">Create a depreciation book</span></span>
1. <span data-ttu-id="3795c-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Poistokirjat.</span><span class="sxs-lookup"><span data-stu-id="3795c-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="3795c-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3795c-108">Click New.</span></span>
3. <span data-ttu-id="3795c-109">Kirjoita arvo Poistokirja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3795c-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="3795c-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3795c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3795c-111">Valitse Laske poisto -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="3795c-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="3795c-112">Avaa haku valitsemalla Poistoprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3795c-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3795c-113">Etsi haluamasi poistoprofiili luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3795c-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="3795c-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3795c-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3795c-115">Avaa haku valitsemalla Vaihtoehtoinen poistoprofiili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3795c-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="3795c-116">Valitse luettelosta haluamasi poistoprofiili.</span><span class="sxs-lookup"><span data-stu-id="3795c-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="3795c-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3795c-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3795c-118">Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="3795c-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="3795c-119">Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="3795c-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="3795c-120">Valitse Luo poistojen oikaisut käyttäen perusoikaisuja -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="3795c-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="3795c-121">Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3795c-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="3795c-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3795c-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="3795c-123">Poistokirjan liittäminen käyttöomaisuusryhmään</span><span class="sxs-lookup"><span data-stu-id="3795c-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="3795c-124">Valitse Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="3795c-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="3795c-125">Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="3795c-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3795c-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3795c-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3795c-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3795c-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3795c-128">Valitse vaihtoehto Poistomenetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="3795c-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="3795c-129">Syötä Käyttöikä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="3795c-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="3795c-130">Ota huomioon, että Poistokaudet-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3795c-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


