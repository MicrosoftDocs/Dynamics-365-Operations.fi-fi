---
title: Käyttöomaisuuden poistojen laskenta eri yrityksissä
description: Käyttöomaisuuden poisto voidaan suorittaa useille yritykselle yhdellä kertaa.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840094"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="b0f18-103">Käyttöomaisuuden poistojen laskenta eri yrityksissä</span><span class="sxs-lookup"><span data-stu-id="b0f18-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0f18-104">Käyttöomaisuuden poisto voidaan suorittaa useille yritykselle yhdellä kertaa.</span><span class="sxs-lookup"><span data-stu-id="b0f18-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="b0f18-105">Näissä ohjeissa kerrotaan, miten prosessi määritetään ja suoritetaan useille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="b0f18-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="b0f18-106">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="b0f18-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="b0f18-107">Yritysten välisten poistoajon kirjauskansioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b0f18-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="b0f18-108">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuuden parametrit.</span><span class="sxs-lookup"><span data-stu-id="b0f18-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="b0f18-109">Laajenna Käyttöomaisuuden ehdotukset -osa.</span><span class="sxs-lookup"><span data-stu-id="b0f18-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="b0f18-110">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="b0f18-110">Click Add.</span></span>
4. <span data-ttu-id="b0f18-111">Syötä tai valitse arvo Kirjanpitotaso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b0f18-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="b0f18-112">Syötä tai valitse arvo Kirjauskansion nimi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b0f18-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="b0f18-113">Toista kirjauskansion asetukset kunkin yrityksen Käyttöomaisuuden parametrit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b0f18-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="b0f18-114">Poiston suorittaminen</span><span class="sxs-lookup"><span data-stu-id="b0f18-114">Depreciation run</span></span>
1. <span data-ttu-id="b0f18-115">Siirry kohtaan Käyttöomaisuus > Kirjauskansioviennit > Luo poistoehdotus.</span><span class="sxs-lookup"><span data-stu-id="b0f18-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="b0f18-116">Syötä tai valitse arvo Kirjanpitotaso-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b0f18-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="b0f18-117">Kirjauskansion nimen oletusarvo saadaan käyttömaisuuden parametreista.</span><span class="sxs-lookup"><span data-stu-id="b0f18-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="b0f18-118">Nykyisen yrityksen kirjauskansion nimi voidaan vaihtaa tässä.</span><span class="sxs-lookup"><span data-stu-id="b0f18-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="b0f18-119">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b0f18-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="b0f18-120">Valitse poistoajoon sisällytettävät yritykset.</span><span class="sxs-lookup"><span data-stu-id="b0f18-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="b0f18-121">Luettelo sisältää vain yritykset, joiden kirjauskansiot on määritetty Käyttöomaisuuden parametrit -sivun Käyttöomaisuuden ehdotukset -osassa.</span><span class="sxs-lookup"><span data-stu-id="b0f18-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="b0f18-122">Valitse Kirjaa kirjauskansiot -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b0f18-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="b0f18-123">Kenttien suodattaminen sisältää kaiken yrityksen käyttöomaisuuden ja kaikki yrityksen ryhmät ja kirjat, jotka on valittu tähän poistoajoon.</span><span class="sxs-lookup"><span data-stu-id="b0f18-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="b0f18-124">Eräkäsittely-vaihtoehto on käytössä oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="b0f18-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="b0f18-125">Kun tämä vaihtoehto on käytössä, poistokirjauskansion luominen ja kirjaaminen suoritetaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="b0f18-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="b0f18-126">Valitse Luo kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="b0f18-126">Click Create journal.</span></span>
6. <span data-ttu-id="b0f18-127">Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="b0f18-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

