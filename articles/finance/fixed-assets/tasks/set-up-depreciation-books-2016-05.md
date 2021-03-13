---
title: Määritä poistokirjat
description: Tämä menettely käy läpi uuden poistokirjan luomisprosessin ja liittää sen käyttöomaisuus ryhmään.
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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e1d934bffd0a5daacf27fcd5a2e00043fe3daf8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009215"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="c584a-103">Määritä poistokirjat</span><span class="sxs-lookup"><span data-stu-id="c584a-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c584a-104">Tämä menettely käy läpi uuden poistokirjan luomisprosessin ja liittää sen käyttöomaisuus ryhmään.</span><span class="sxs-lookup"><span data-stu-id="c584a-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="c584a-105">Poistokirjan luominen</span><span class="sxs-lookup"><span data-stu-id="c584a-105">Create a depreciation book</span></span>
1. <span data-ttu-id="c584a-106">Siirry kohtaan Käyttöomaisuus > Asetukset > Poistokirjat.</span><span class="sxs-lookup"><span data-stu-id="c584a-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="c584a-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c584a-107">Click New.</span></span>
3. <span data-ttu-id="c584a-108">Kirjoita arvo Poistokirja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c584a-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="c584a-109">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c584a-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c584a-110">Valitse Laske poisto -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="c584a-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="c584a-111">Avaa haku valitsemalla Poistoprofiili-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c584a-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c584a-112">Etsi haluamasi poistoprofiili luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c584a-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="c584a-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c584a-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c584a-114">Avaa haku valitsemalla Vaihtoehtoinen poistoprofiili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c584a-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c584a-115">Valitse luettelosta haluamasi poistoprofiili.</span><span class="sxs-lookup"><span data-stu-id="c584a-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="c584a-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c584a-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c584a-117">Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="c584a-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="c584a-118">Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="c584a-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="c584a-119">Valitse Luo poistojen oikaisut käyttäen perusoikaisuja -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="c584a-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="c584a-120">Avaa haku valitsemalla Kalenteri-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c584a-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="c584a-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c584a-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="c584a-122">Poistokirjan liittäminen käyttöomaisuusryhmään</span><span class="sxs-lookup"><span data-stu-id="c584a-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="c584a-123">Valitse Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="c584a-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="c584a-124">Avaa haku valitsemalla Käyttöomaisuusryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="c584a-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c584a-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c584a-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c584a-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="c584a-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c584a-127">Valitse vaihtoehto Poistomenetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c584a-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="c584a-128">Syötä Käyttöikä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c584a-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="c584a-129">Ota huomioon, että Poistokaudet-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c584a-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

