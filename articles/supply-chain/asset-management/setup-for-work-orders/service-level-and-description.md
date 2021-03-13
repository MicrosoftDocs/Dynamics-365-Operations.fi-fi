---
title: Palvelutaso ja kuvaus
description: Tässä ohjeaiheessa kerrotaan palvelutasosta ja kuvauksesta resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bb56e5103bd9e18e88c164cd308e55d48e64823
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019376"
---
# <a name="service-level-and-description"></a><span data-ttu-id="6750e-103">Palvelutaso ja kuvaus</span><span class="sxs-lookup"><span data-stu-id="6750e-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6750e-104">Kun luot työtilauksen, haluat ehkä määrittää sen palvelutasot ja lisätä siihen yleisen kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="6750e-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="6750e-105">Voit luoda työtilauspalvelutasoja **Työtilauksen palvelutasot** -sivulla ja kuvaukset **Työtilauksen kuvaus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6750e-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="6750e-106">Luo palvelutaso</span><span class="sxs-lookup"><span data-stu-id="6750e-106">Create a service level</span></span>

1. <span data-ttu-id="6750e-107">Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Palvelutaso**.</span><span class="sxs-lookup"><span data-stu-id="6750e-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="6750e-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6750e-108">Select **New**.</span></span>
3. <span data-ttu-id="6750e-109">Kirjoita **Palvelutaso**-kenttään palvelutaso (esimerkiksi numero).</span><span class="sxs-lookup"><span data-stu-id="6750e-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="6750e-110">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6750e-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="6750e-111">**Työtilaukset**-pikavälilehdessä voit määrittää odotetut alkamis- ja päättymispäivämäärät sekä -ajat.</span><span class="sxs-lookup"><span data-stu-id="6750e-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="6750e-112">Tämän pikavälilehden kentissä määritetään kausi, jolloin työtilaukset aloitetaan ja päätetään.</span><span class="sxs-lookup"><span data-stu-id="6750e-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="6750e-113">Niitä käytetään manuaalisesti luoduissa työtilauksissa ja kunnossapitopyyntöjen perusteella luoduissa työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="6750e-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="6750e-114">Kirjoita **Aloituspäivä**-kenttään päivien lukumäärä, joka määrittää työtilauksen aloitusajan ajanjakson.</span><span class="sxs-lookup"><span data-stu-id="6750e-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="6750e-115">Päivien määrä lasketaan työtilauksen luontipäivästä.</span><span class="sxs-lookup"><span data-stu-id="6750e-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="6750e-116">Jos esimerkiksi työtilauksen pitäisi alkaa luonnin yhteydessä, kirjoita **0.**</span><span class="sxs-lookup"><span data-stu-id="6750e-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="6750e-117">Jos työtilauksen pitäisi alkaa viikko luonnin jälkeen, kirjoita **7.**</span><span class="sxs-lookup"><span data-stu-id="6750e-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="6750e-118">Jos haluat määrittää työtilaukselle aloitusajan aloituspäivämäärän lisäksi, määritä **Aseta aloitusaika** -asetukseksi **Kyllä.**</span><span class="sxs-lookup"><span data-stu-id="6750e-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="6750e-119">Kirjoita aloitusaika **Aloitusaika**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6750e-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="6750e-120">Jos määrität asetukseksi **Ei**, käytetään nykyistä kellonaikaa.</span><span class="sxs-lookup"><span data-stu-id="6750e-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="6750e-121">Kirjoita **Päättymispäivä**-kenttään päivien lukumäärä, joka määrittää työtilauksen päättymisajan ajanjakson.</span><span class="sxs-lookup"><span data-stu-id="6750e-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="6750e-122">Päivien määrä lasketaan työtilauksen aloituspäivästä.</span><span class="sxs-lookup"><span data-stu-id="6750e-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="6750e-123">Jos esimerkiksi työtilauksen pitäisi päättyä viikon kuluttua sen alkamispäivästä, kirjoita **7.**</span><span class="sxs-lookup"><span data-stu-id="6750e-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="6750e-124">Jos haluat määrittää työtilaukselle päättymisajan päättymispäivämäärän lisäksi, määritä **Aseta päättymisaika** -asetukseksi **Kyllä.**</span><span class="sxs-lookup"><span data-stu-id="6750e-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="6750e-125">Kirjoita päättymisaika **Päättymisaika**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6750e-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="6750e-126">Jos määrität asetukseksi **Ei**, käytetään nykyistä kellonaikaa.</span><span class="sxs-lookup"><span data-stu-id="6750e-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="6750e-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6750e-127">Select **Save**.</span></span>

![Työtilausten palvelutasosivu](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="6750e-129">Luo kuvaus</span><span class="sxs-lookup"><span data-stu-id="6750e-129">Create a description</span></span>

1. <span data-ttu-id="6750e-130">Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Kuvaukset**.</span><span class="sxs-lookup"><span data-stu-id="6750e-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="6750e-131">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6750e-131">Select **New**.</span></span>
3. <span data-ttu-id="6750e-132">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6750e-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="6750e-133">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6750e-133">Select **Save**.</span></span>
