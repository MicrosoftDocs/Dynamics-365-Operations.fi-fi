--- 
title: "Käyttöomaisuuden poistojen laskenta eri yrityksissä"
description: "Näissä ohjeissa kerrotaan, miten poistoprosessi määritetään ja suoritetaan useille yrityksille."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4221acf200f41ca39803bcd56c1b05e0d87bd948
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="1251c-103">Käyttöomaisuuden poistojen laskenta eri yrityksissä</span><span class="sxs-lookup"><span data-stu-id="1251c-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1251c-104">Käyttöomaisuuden poisto voidaan suorittaa useille yritykselle yhdellä kertaa.</span><span class="sxs-lookup"><span data-stu-id="1251c-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="1251c-105">Näissä ohjeissa kerrotaan, miten prosessi määritetään ja suoritetaan useille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="1251c-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="1251c-106">Prosessissa käytetään kirjanpitäjän roolia.</span><span class="sxs-lookup"><span data-stu-id="1251c-106">It uses the accountant role.</span></span>  

<span data-ttu-id="1251c-107">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="1251c-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="1251c-108">Vaiheiden (16) alitehtävä: Määritä yritysten väliset poistoajon kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="1251c-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="1251c-109">Ensin määritetään kirjauskansiot, joita käytetään yritysten välisessä poistoajossa jokaisessa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1251c-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="1251c-110">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden parametrit.</span><span class="sxs-lookup"><span data-stu-id="1251c-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="1251c-111">Laajenna Käyttöomaisuuden ehdotukset -osa.</span><span class="sxs-lookup"><span data-stu-id="1251c-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="1251c-112">Luo tietue, jolla on kirjauskansion nimi. Sitä käytetään yrityksen jokaisella kirjanpitotasolla.</span><span class="sxs-lookup"><span data-stu-id="1251c-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="1251c-113">Jos kirjoja ei kirjata kirjanpitoon, liitettylle kirjauskansiolle valitaan Ei mitään -kirjanpitotaso.</span><span class="sxs-lookup"><span data-stu-id="1251c-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="1251c-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="1251c-114">Click Add.</span></span> 
4. <span data-ttu-id="1251c-115">Syötä tai valitse arvo Kirjanpitotaso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1251c-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="1251c-116">Syötä tai valitse arvo Kirjauskansion nimi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1251c-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="1251c-117">Toista kirjauskansion asetukset kunkin yrityksen Käyttöomaisuuden parametrit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1251c-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="1251c-118">Alitehtävä: Poiston laskeminen</span><span class="sxs-lookup"><span data-stu-id="1251c-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="1251c-119">Aloita poistoajo yrityksissä Poistoehdotuksen luominen -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1251c-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="1251c-120">Siirry kohtaan Käyttöomaisuus > Kirjauskansioviennit > Luo poistoehdotus.</span><span class="sxs-lookup"><span data-stu-id="1251c-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="1251c-121">Syötä tai valitse arvo Kirjanpitotaso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1251c-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="1251c-122">Kirjauskansion nimen oletusarvo saadaan käyttömaisuuden parametreista.</span><span class="sxs-lookup"><span data-stu-id="1251c-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="1251c-123">Nykyisen yrityksen kirjauskansion nimi voidaan vaihtaa tässä.</span><span class="sxs-lookup"><span data-stu-id="1251c-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="1251c-124">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1251c-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="1251c-125">Valitse poistoajoon sisällytettävät yritykset.</span><span class="sxs-lookup"><span data-stu-id="1251c-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="1251c-126">Luettelo sisältää vain yritykset, joiden kirjauskansiot on määritetty Käyttöomaisuuden parametrit -sivun Käyttöomaisuuden ehdotukset -osassa.</span><span class="sxs-lookup"><span data-stu-id="1251c-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="1251c-127">Kun tämä vaihtoehto on käytössä, Kirjaa kirjauskansiot -vaihtoehto kirjaa poistokirjauskansiot automaattisesti niiden luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="1251c-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="1251c-128">Kun vaihtoehtoa ei ole valittu, kirjauskansiot luodaan, mutta niitä ei kirjata. Voit siis tarkistaa tiedot ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="1251c-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="1251c-129">Valitse Kirjaa kirjauskansiot -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="1251c-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="1251c-130">Kenttien suodattaminen sisältää kaiken yrityksen käyttöomaisuuden ja kaikki yrityksen ryhmät ja kirjat, jotka on valittu tähän poistoajoon.</span><span class="sxs-lookup"><span data-stu-id="1251c-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="1251c-131">Eräkäsittely-vaihtoehto on käytössä oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="1251c-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="1251c-132">Kun tämä vaihtoehto on käytössä, poistokirjauskansion luominen ja kirjaaminen suoritetaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="1251c-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="1251c-133">Valitse Luo kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="1251c-133">Click Create journal.</span></span> 
10. <span data-ttu-id="1251c-134">Yrityksissä luodut poistokirjauskansiot on tarkistettava.</span><span class="sxs-lookup"><span data-stu-id="1251c-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="1251c-135">Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="1251c-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

