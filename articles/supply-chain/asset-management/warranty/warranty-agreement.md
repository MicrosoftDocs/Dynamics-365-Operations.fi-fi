---
title: Takuusopimukset
description: Tässä ohjeaiheessa kerrotaan takuusopimuksista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427213"
---
# <a name="warranty-agreements"></a><span data-ttu-id="79caa-103">Takuusopimukset</span><span class="sxs-lookup"><span data-stu-id="79caa-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="79caa-104">Käyttöomaisuuden hallinnassa voit määrittää takuuehdot, jotka voidaan liittää käyttöomaisuuserään tai käyttöomaisuuslajiin.</span><span class="sxs-lookup"><span data-stu-id="79caa-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="79caa-105">Takuuehdot luodaan tietylle kaudelle.</span><span class="sxs-lookup"><span data-stu-id="79caa-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="79caa-106">Takuun voi määrittää siten, että se sisältää täyden kattavuuden tai osittaisen kattavuuden, ja voit määrittää ehdot, jotka liittyvät tunteihin, kuluihin ja nimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="79caa-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="79caa-107">Ensimmäiseksi on luotava mahdolliset toimittajien takuusopimukset, jotka on tehty laitteillesi.</span><span class="sxs-lookup"><span data-stu-id="79caa-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="79caa-108">Tämän jälkeen voit liittää takuusopimukset käyttöomaisuuseriin tai omaisuustyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="79caa-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="79caa-109">Toimittajien takuusopimuksia käytetään vain tiedotustarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="79caa-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="79caa-110">Jos toimittajan takuu on määritetty käyttöomaisuuserään, voit nähdä käyttöomaisuuserän takuun kattavuuskauden.</span><span class="sxs-lookup"><span data-stu-id="79caa-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="79caa-111">Luo takuusopimus</span><span class="sxs-lookup"><span data-stu-id="79caa-111">Create a warranty agreement</span></span>

<span data-ttu-id="79caa-112">Takuusopimukseen voi kuulua useita sopimusrivejä, jotka kattavat työajan, kulujen ja nimikkeiden takuun.</span><span class="sxs-lookup"><span data-stu-id="79caa-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="79caa-113">Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssit** \> **Takuu**.</span><span class="sxs-lookup"><span data-stu-id="79caa-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="79caa-114">Luo tuote valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="79caa-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="79caa-115">Syötä **Takuu** -kenttään takuun tunnus.</span><span class="sxs-lookup"><span data-stu-id="79caa-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="79caa-116">Anna kuvaus **nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79caa-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="79caa-117">**Tiedot**-pikavälilehden **Resurssit**-kentässä näkyy takuusopimusta käyttävien aktiivisten resurssien määrä.</span><span class="sxs-lookup"><span data-stu-id="79caa-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="79caa-118">Lisää takuusopimukseen sisällytettävät rivit **Takuurivit**-pikavälilehdessä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="79caa-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="79caa-119">Voit lisätä uuden ehdon takuuseen valitsemalla **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="79caa-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="79caa-120">**Rivi**-kenttään syötetään automaattisesti rivin järjestysnumero.</span><span class="sxs-lookup"><span data-stu-id="79caa-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="79caa-121">Valitse **Kausi**-kentässä takuukauden tyyppi.</span><span class="sxs-lookup"><span data-stu-id="79caa-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="79caa-122">Syötä numero **Väli**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79caa-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="79caa-123">Tämä kenttä määrittää niiden kausien määrän, joiden takuun tulisi olla voimassa.</span><span class="sxs-lookup"><span data-stu-id="79caa-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="79caa-124">Kirjoita takuurivin kattavuusprosentti **Prosentti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79caa-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="79caa-125">Prosenttiosuus ilmaisee, kuinka paljon yrityksesi kattaa takuuta.</span><span class="sxs-lookup"><span data-stu-id="79caa-125">The percentage indicates how much is covered by your company.</span></span>

![Takuusivu](media/01-warranty.png)
