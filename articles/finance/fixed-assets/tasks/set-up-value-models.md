---
title: Arvomallien asetukset
description: Näiden ohjeiden avulla voit luoda uuden käyttöomaisuuskirjan ja liittää sen käyttöomaisuusryhmään.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a59bafe3099b50d34bdd9e125cfb7f43d219dcc6
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138135"
---
# <a name="set-up-value-models"></a><span data-ttu-id="7e409-103">Arvomallien asetukset</span><span class="sxs-lookup"><span data-stu-id="7e409-103">Set up value models</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e409-104">Näiden ohjeiden avulla voit luoda uuden käyttöomaisuuskirjan ja liittää sen käyttöomaisuusryhmään.</span><span class="sxs-lookup"><span data-stu-id="7e409-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="7e409-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="7e409-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="7e409-106">Luo uusi kirja</span><span class="sxs-lookup"><span data-stu-id="7e409-106">Create a book</span></span>
1. <span data-ttu-id="7e409-107">Valitse Käyttöomaisuudet > Asetukset > Kirjat.</span><span class="sxs-lookup"><span data-stu-id="7e409-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="7e409-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7e409-108">Click New.</span></span>
3. <span data-ttu-id="7e409-109">Kirjoita arvo Kirja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7e409-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="7e409-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7e409-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7e409-111">Jos Laske poisto -kohta on valittuna, liittyvän käyttöomaisuuserän kirja sisällytetään poistoehdotuksiin.</span><span class="sxs-lookup"><span data-stu-id="7e409-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="7e409-112">Jos sitä ei ole valittu, käyttöomaisuuskirjalle ei tehdä automaattisesti poistoa.</span><span class="sxs-lookup"><span data-stu-id="7e409-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="7e409-113">Valitse Laske poisto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7e409-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="7e409-114">Syötä tai valitse arvo Poistoprofiili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7e409-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="7e409-115">Vaihtoehtoinen poistoprofiili tunnetaan myös poiston vaihdosmenetelmänä.</span><span class="sxs-lookup"><span data-stu-id="7e409-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="7e409-116">Poistoehdotus vaihtaa tämän profiilin, kun vaihtoehtoinen profiili laskee poistosumman, joka on sama tai suurempi kuin oletuspoistoprofiili.</span><span class="sxs-lookup"><span data-stu-id="7e409-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="7e409-117">Lisäpoistoprofiilia käytetään käyttöomaisuuserän lisäpoistoon erityisissä tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="7e409-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="7e409-118">Voit esimerkiksi käyttää tätä luonnonkatastrofista johtuvan poiston kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="7e409-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="7e409-119">Jos Luo poistojen oikaisut käyttäen perusoikaisuja -kohta on valittuna, poiston oikaisut luodaan automaattisesti, kun käyttöomaisuuserän arvo päivitetään.</span><span class="sxs-lookup"><span data-stu-id="7e409-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="7e409-120">Jos sitä ei ole valittu, päivitetty käyttöomaisuuserän arvo vaikuttaa vain tuleviin poistolaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="7e409-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="7e409-121">Valitse Luo poistojen oikaisut käyttäen perusoikaisuja -valintaruudun arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7e409-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="7e409-122">Oletusarvon mukaan käyttöomaisuuskirjan tapahtumat kirjataan pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="7e409-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="7e409-123">Kirjanpitokirjaukset voi poistaa käytöstä asettamalla Kirjaa kirjanpitoon -kentän arvoksi Ei.</span><span class="sxs-lookup"><span data-stu-id="7e409-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="7e409-124">Kirjat, joita ei kirjata pääkirjanpitoon ovat yleensä veroraportointia varten.</span><span class="sxs-lookup"><span data-stu-id="7e409-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="7e409-125">Näin voit poistaa menneitä tapahtumia käyttöomaisuuskirjasta, koska niitä ei ole vahvistettu kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="7e409-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="7e409-126">Oletuskirjaustaso on nykyinen taso, jos kirjan kirjaukset tehdään kirjanpidon ja Ei mitään, jos kirjanpitokirjauksia ei tehdä.</span><span class="sxs-lookup"><span data-stu-id="7e409-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="7e409-127">Päivitä kirjanpitotaso, jos haluat kirjata tämän kirjan tapahtumia toiselle tasolle.</span><span class="sxs-lookup"><span data-stu-id="7e409-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="7e409-128">Syötä tai valitse arvo Kalenteri-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7e409-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="7e409-129">Johdettujen kirjojen tapahtumat kirjataan eri kirjoihin samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="7e409-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="7e409-130">Voit luoda tapahtumia ensisijaiseen kirjaan, joista luodaan kirjauksen aikana tarkka kopio johdettuun kirjaan.</span><span class="sxs-lookup"><span data-stu-id="7e409-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="7e409-131">Johdettujen kirjojen tapahtumille ei suoriteta uudelleenlaskentaa, joten niitä ei tule käyttää poistotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="7e409-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="7e409-132">Kirjan liittäminen käyttöomaisuusryhmään</span><span class="sxs-lookup"><span data-stu-id="7e409-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="7e409-133">Valitse Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="7e409-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="7e409-134">Syötä tai valitse arvo Käyttöomaisuusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7e409-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="7e409-135">Syötä Käyttöikä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="7e409-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="7e409-136">Ota huomioon, että Poistokaudet-kentän arvo lasketaan käyttöiän määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7e409-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="7e409-137">Voit määrittää poistomenetelmän verotustarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7e409-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  

