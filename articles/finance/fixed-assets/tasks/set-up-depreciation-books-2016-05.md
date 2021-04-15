---
title: Määritä poistokirjat
description: Tämä menettely käy läpi uuden poistokirjan luomisprosessin ja liittää sen käyttöomaisuus ryhmään.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0ab7f9332e3224c3dadd62aae532ccffb05c82a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815593"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="a3458-103">Määritä poistokirjat</span><span class="sxs-lookup"><span data-stu-id="a3458-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3458-104">Tämä menettely käy läpi uuden poistokirjan luomisprosessin ja liittää sen käyttöomaisuus ryhmään.</span><span class="sxs-lookup"><span data-stu-id="a3458-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="a3458-105">Poistokirjan luominen</span><span class="sxs-lookup"><span data-stu-id="a3458-105">Create a depreciation book</span></span>
1. <span data-ttu-id="a3458-106">Siirry kohtaan Käyttöomaisuus > Asetukset > Poistokirjat.</span><span class="sxs-lookup"><span data-stu-id="a3458-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="a3458-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a3458-107">Click New.</span></span>
3. <span data-ttu-id="a3458-108">Kirjoita arvo Poistokirja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a3458-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="a3458-109">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a3458-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a3458-110">Valitse Laske poisto -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="a3458-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="a3458-111">Avaa haku valitsemalla Poistoprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a3458-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a3458-112">Etsi haluamasi poistoprofiili luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a3458-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="a3458-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a3458-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a3458-114">Avaa haku valitsemalla Vaihtoehtoinen poistoprofiili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a3458-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="a3458-115">Valitse luettelosta haluamasi poistoprofiili.</span><span class="sxs-lookup"><span data-stu-id="a3458-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="a3458-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a3458-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a3458-117">Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="a3458-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="a3458-118">Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="a3458-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="a3458-119">Valitse Luo poistojen oikaisut käyttäen perusoikaisuja -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="a3458-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="a3458-120">Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a3458-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="a3458-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a3458-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="a3458-122">Poistokirjan liittäminen käyttöomaisuusryhmään</span><span class="sxs-lookup"><span data-stu-id="a3458-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="a3458-123">Valitse Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="a3458-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="a3458-124">Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a3458-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a3458-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a3458-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a3458-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a3458-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a3458-127">Valitse vaihtoehto Poistomenetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a3458-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="a3458-128">Syötä Käyttöikä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a3458-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="a3458-129">Ota huomioon, että Poistokaudet-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a3458-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]