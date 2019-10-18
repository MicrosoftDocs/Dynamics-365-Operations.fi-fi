---
title: Myymälän tuntien luominen ja päivittäminen
description: Tässä aiheessa kuvataan, miten myymälän tunnit luodaan ja päivitetään Retail Headquarters -sovelluksessa.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 811d499a3eb8133e5ffd29bb4ae6a0c57708accd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023439"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="e935b-103">Myymälän tuntien luominen ja päivittäminen</span><span class="sxs-lookup"><span data-stu-id="e935b-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e935b-104">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e935b-104">Overview</span></span>

<span data-ttu-id="e935b-105">Yhdestä paikasta vähittäiskauppiaat voivat luoda, ylläpitää ja hallita eri myymälöiden aukioloaikoja kaikilla maantieteellisillä alueilla.</span><span class="sxs-lookup"><span data-stu-id="e935b-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="e935b-106">Myymälätunnit voidaan sitten näyttää myyntipisteissä (POS).</span><span class="sxs-lookup"><span data-stu-id="e935b-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="e935b-107">Näin kassat voivat jakaa myymälätunteja asiakkaiden kanssa ja auttaa asiakkaita, jotka ovat kiinnostuneita muiden myymälöiden varastoista.</span><span class="sxs-lookup"><span data-stu-id="e935b-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="e935b-108">Myymälätunnit voidaan myös painaa kuitteihin, jos asiakkaat haluavat palata myymälään myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="e935b-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="e935b-109">Useita myymälätunteja voidaan määrittää eri kanavien kautta.</span><span class="sxs-lookup"><span data-stu-id="e935b-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="e935b-110">Näitä kanavia ovat esimerkiksi kivijalkamyymälät, puhelineskukset, mobiililaitteet ja verkkokauppapaikat.</span><span class="sxs-lookup"><span data-stu-id="e935b-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="e935b-111">Jos asiakkaalla on eri myymälään noutotilaus, kassanhoitaja voi valita päivämäärät, jolloin nouto on käytettävissä kyseisessä myymälässä.</span><span class="sxs-lookup"><span data-stu-id="e935b-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="e935b-112">Myymälähaku sisältää viittauksen päivämääriin ja aukioloaikoihin.</span><span class="sxs-lookup"><span data-stu-id="e935b-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="e935b-113">Kassanhoitaja voi valita päivämäärän ja sijainnin, ja hän voi myös tulostaa noutokuitin, joka sisältää myymälän tunnit.</span><span class="sxs-lookup"><span data-stu-id="e935b-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="e935b-114">Tämä toiminto on käytettävissä Microsoft Dynamics 365 Retail -versioissa 8.1.2 ja uudemmissa.</span><span class="sxs-lookup"><span data-stu-id="e935b-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="e935b-115">Myymälän tuntien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e935b-115">Configure store hours</span></span>

<span data-ttu-id="e935b-116">Jos haluat konfiguroida myymälän aukioloajat, noudata seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="e935b-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="e935b-117">Siirry kohtaan **Vähittäismyynti** \> **Kanavan asetukset** \> **Myymälän aukioloajat**.</span><span class="sxs-lookup"><span data-stu-id="e935b-117">Go to **Retail** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="e935b-118">Valitse **Uusi** luodaksesi uuden aukioloaikojen mallin.</span><span class="sxs-lookup"><span data-stu-id="e935b-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="e935b-119">Jos haluat käyttää aiemmin luotua mallia, valitse malli vasemmanpuoleisesta ruudusta.</span><span class="sxs-lookup"><span data-stu-id="e935b-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="e935b-120">Määritä **Lisää alue** -valintaikkunassa päivämääräväli, myymälätunnit ja kaikki tarvittavat vapaapäivät.</span><span class="sxs-lookup"><span data-stu-id="e935b-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="e935b-121">Jos myymälän tunnit eivät muutu, valitse **Päättymispäivä**-kentässä **Ei pääty koskaan**.</span><span class="sxs-lookup"><span data-stu-id="e935b-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="e935b-122">Jos myymälän tunnit koskevat tiettyä kuukautta, viikkoa tai päivää, määritä tarvittavat päivämäärät **Alkamispäivä**- ja **Päättymispäivä**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="e935b-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e935b-123">Voit luoda useita malleja, joiden alkamis- ja päättymispäivämäärät ovat päällekkäiset.</span><span class="sxs-lookup"><span data-stu-id="e935b-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="e935b-124">Näin voit esimerkiksi määrittää myymälän aukioloajat eri aikavyöhykkeillä oleville myymälöille.</span><span class="sxs-lookup"><span data-stu-id="e935b-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="e935b-125">![Lisää alue -valintaikkuna](../dev-itpro/media/Storehours1.png "Lisää alue -valintaikkuna")</span><span class="sxs-lookup"><span data-stu-id="e935b-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="e935b-126">Liitä myymälätuntien malli myymälöihin, joissa sitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="e935b-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="e935b-127">Valitse **Valitse organisaatiosolmut** -valintaikkunassa ne myymälät, alueet ja organisaatiot, joihin malli liitetään.</span><span class="sxs-lookup"><span data-stu-id="e935b-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="e935b-128">Kuhunkin myymälään voidaan liittää vain yksi myymälän tuntimalli.</span><span class="sxs-lookup"><span data-stu-id="e935b-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="e935b-129">Valitse myymälät, alueet tai organisaatiot nuolipainikkeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="e935b-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="e935b-130">Kalenteri on myymälöiden tai myymäläryhmien käytettävissä, ja se näkyy viitteenä myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="e935b-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="e935b-131">![Valitse organisaatiosolmut -valintaikkuna](../dev-itpro/media/Storehours2.png "Valitse organisaatiosolmut -valintaikkuna")</span><span class="sxs-lookup"><span data-stu-id="e935b-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="e935b-132">Suorita **Jakeluaikataulu**-sivulla työt **1070** ja **1090**, jotta myymälätunnit ovat käytettävissä myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="e935b-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="e935b-133">Aukioloaikojen lisääminen tulostettuihin kuitteihin</span><span class="sxs-lookup"><span data-stu-id="e935b-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="e935b-134">Seuraavia ohjeita noudattamalla voit lisätä myymälätunteja tulostetuihin myyntipisteen kuitteihin.</span><span class="sxs-lookup"><span data-stu-id="e935b-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="e935b-135">Avaa kuitin suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="e935b-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="e935b-136">Valitse vasemmassa alakulmassa **Alatunniste**.</span><span class="sxs-lookup"><span data-stu-id="e935b-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="e935b-137">Vedä **Myymälän aukioloajat** -elementti vasemmasta ruudusta kuittimallin alareunassa olevaan alatunnisteeseen.</span><span class="sxs-lookup"><span data-stu-id="e935b-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="e935b-138">Voit muokata **Myymälän aukioloajat** -elementin oletusotsikkoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e935b-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="e935b-139">Tallenna kuitti ja lopeta kuitin suunnittelu.</span><span class="sxs-lookup"><span data-stu-id="e935b-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="e935b-140">Suorita **Jakeluaikataulu**-sivulla työt **1070** ja **1090**.</span><span class="sxs-lookup"><span data-stu-id="e935b-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="e935b-141">Kirjaudu myyntipisteeseen.</span><span class="sxs-lookup"><span data-stu-id="e935b-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="e935b-142">Viimeistele myynti ja valitse kuitin tulostus.</span><span class="sxs-lookup"><span data-stu-id="e935b-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="e935b-143">Myyntipsiteen kuiteissa on nyt myymälän tunnit.</span><span class="sxs-lookup"><span data-stu-id="e935b-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="e935b-144">Jos malliin sisältyy vapaapäiviä, ne näkyvät kuitissa.</span><span class="sxs-lookup"><span data-stu-id="e935b-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="e935b-145">![Kuittiesimerkki](../dev-itpro/media/Storehours3.png "Kuittiesimerkki")</span><span class="sxs-lookup"><span data-stu-id="e935b-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
