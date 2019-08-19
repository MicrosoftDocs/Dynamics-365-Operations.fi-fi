---
title: Käyttöomaisuuden poistokirjojen määrittäminen (Toukokuu 2016)
description: Tässä tehtävän ohjauksessa luodaan uusi poistokirja ja liitetään se käyttöomaisuusryhmään.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839854"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="7edc3-103">Käyttöomaisuuden poistokirjojen määrittäminen (Toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="7edc3-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7edc3-104">Tässä tehtävän ohjauksessa luodaan uusi poistokirja ja liitetään se käyttöomaisuusryhmään.</span><span class="sxs-lookup"><span data-stu-id="7edc3-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="7edc3-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="7edc3-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="7edc3-106">Poistokirjan luominen</span><span class="sxs-lookup"><span data-stu-id="7edc3-106">Create a depreciation book</span></span>
1. <span data-ttu-id="7edc3-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Poistokirjat.</span><span class="sxs-lookup"><span data-stu-id="7edc3-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="7edc3-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7edc3-108">Click New.</span></span>
3. <span data-ttu-id="7edc3-109">Kirjoita arvo Poistokirja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7edc3-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="7edc3-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7edc3-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7edc3-111">Valitse Laske poisto -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="7edc3-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="7edc3-112">Avaa haku valitsemalla Poistoprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7edc3-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7edc3-113">Etsi haluamasi poistoprofiili luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7edc3-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="7edc3-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7edc3-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7edc3-115">Avaa haku valitsemalla Vaihtoehtoinen poistoprofiili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7edc3-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="7edc3-116">Valitse luettelosta haluamasi poistoprofiili.</span><span class="sxs-lookup"><span data-stu-id="7edc3-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="7edc3-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7edc3-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7edc3-118">Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="7edc3-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="7edc3-119">Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="7edc3-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="7edc3-120">Valitse Luo poistojen oikaisut käyttäen perusoikaisuja -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="7edc3-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="7edc3-121">Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7edc3-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="7edc3-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7edc3-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="7edc3-123">Poistokirjan liittäminen käyttöomaisuusryhmään</span><span class="sxs-lookup"><span data-stu-id="7edc3-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="7edc3-124">Valitse Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="7edc3-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="7edc3-125">Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7edc3-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7edc3-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7edc3-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7edc3-127">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7edc3-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7edc3-128">Valitse vaihtoehto Poistomenetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7edc3-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="7edc3-129">Syötä Käyttöikä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7edc3-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="7edc3-130">Ota huomioon, että Poistokaudet-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7edc3-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

