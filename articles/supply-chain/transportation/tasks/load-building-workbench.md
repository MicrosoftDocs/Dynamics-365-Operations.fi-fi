---
title: Kuormituksen luonnin työtila
description: Tässä aiheessa käsitellään kuormituksen luonnin työtilan käyttämistä.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8633adbab43c95366d42cf409f5e508771c906
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809035"
---
# <a name="load-building-workbench"></a><span data-ttu-id="d464f-103">Kuormituksen luonnin työtila</span><span class="sxs-lookup"><span data-stu-id="d464f-103">Load building workbench</span></span>

<span data-ttu-id="d464f-104">Kuormituksen luonnin työtilassa voidaan käyttää kuormituksen luontistrategioita kuormia luotaessa.</span><span class="sxs-lookup"><span data-stu-id="d464f-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="d464f-105">Kuormituksen luontistrategian luominen</span><span class="sxs-lookup"><span data-stu-id="d464f-105">Create a load building strategy</span></span>

<span data-ttu-id="d464f-106">Kuormitusten luontistrategioita käytetään kuormien automaattiseen luontiin.</span><span class="sxs-lookup"><span data-stu-id="d464f-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="d464f-107">Tämä ominaisuus voi olla kätevä seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="d464f-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="d464f-108">Tietty tuotejoukko lähetetään säännöllisesti, kuormitusstrategiat auttavat säästämään aikaan, sillä samaa kuormaa ei tarvitse luoda joka kerta.</span><span class="sxs-lookup"><span data-stu-id="d464f-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="d464f-109">Jos haluat tehostaa toimintaa välttämällä puoliksi täytettyjä kuormia, kuormitusstrategia voivat auttaa täyttämään kunkin kuorman mahdollisimman hyvin.</span><span class="sxs-lookup"><span data-stu-id="d464f-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="d464f-110">Kuormituksen luontistrategian `TMSLoadBuildingVolumeStrategy`-nimisessä luokassa on *Tilavuuteen perustuva kuormituksen luontistrategia* -niminen strategia.</span><span class="sxs-lookup"><span data-stu-id="d464f-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="d464f-111">Sen avulla voit käyttää kuormamallissa määritettyjä suurimpia korkeus- ja painoarvoja tai korvata asetukset syöttämällä uudet arvot.</span><span class="sxs-lookup"><span data-stu-id="d464f-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="d464f-112">Tämä strategia on ainoa heti käytettävissä oleva strategia.</span><span class="sxs-lookup"><span data-stu-id="d464f-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="d464f-113">(Käytössä voi kuitenkin olla muutamia mukautettuja strategioita.)</span><span class="sxs-lookup"><span data-stu-id="d464f-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="d464f-114">Voit käyttää valmista *Tilavuuteen perustuva kuormituksen luontistrategia* -strategiaa valitsemalla se **Kuormituksen luonnin työtila** -sivun **Kuormituksen luontistrategia** -kentässä (**Kuljetustenhallinta &gt; Suunnittelu &gt; Kuormituksen luonnin työtila**).</span><span class="sxs-lookup"><span data-stu-id="d464f-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="d464f-115">Kuormituksen luontistrategia luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d464f-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="d464f-116">Valitse **Kuljetustenhallinta &gt; Määritys &gt; Kuormituksen luonti &gt; Kuormituksen luontistrategiat**.</span><span class="sxs-lookup"><span data-stu-id="d464f-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="d464f-117">Varmista, että käytössä on kaikkien luokkien uusimmat versiot valitsemalla toimintoruudussa **Luo luokkaluettelo**.</span><span class="sxs-lookup"><span data-stu-id="d464f-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="d464f-118">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d464f-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d464f-119">Anna strategialle yksilöivä nimi, valitse sille kuormituksen luontistrategia ja anna kuvaus.</span><span class="sxs-lookup"><span data-stu-id="d464f-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="d464f-120">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d464f-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d464f-121">Valitse toimintoruudussa **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="d464f-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="d464f-122">Valitse **Kuormituksen luontistrategian parametrit** -sivun luettelossa **Tilavuuskapasiteetti** ja anna sitten **Arvo**-kenttään se prosenttiosuus kuorman kokonaistilavuuskapasiteetista, jota käytetään uudessa kuormituksen luontistrategiassa.</span><span class="sxs-lookup"><span data-stu-id="d464f-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="d464f-123">Valitse luettelossa **Painokapasiteetti** ja anna sitten **Arvo**-kenttään se prosenttiosuus kuorman kokonaispainokapasiteetista, jota käytetään uudessa kuormituksen luontistrategiassa.</span><span class="sxs-lookup"><span data-stu-id="d464f-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="d464f-124">Sulje **Kuormituksen luontistrategian parametrit** -sivu.</span><span class="sxs-lookup"><span data-stu-id="d464f-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="d464f-125">Sulje **Kuormituksen luontistrategiat** -sivu.</span><span class="sxs-lookup"><span data-stu-id="d464f-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="d464f-126">Kuormituksen luontistrategia voidaan nyt määrittää kuormituksen luontimalliin.</span><span class="sxs-lookup"><span data-stu-id="d464f-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="d464f-127">Vaihtoehtoisesti voit käyttää sitä suoraan kuormasuunnittelun työtilassa.</span><span class="sxs-lookup"><span data-stu-id="d464f-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="d464f-128">Kuormituksen luontistrategian käyttäminen kuormituksen luonnin työtilassa</span><span class="sxs-lookup"><span data-stu-id="d464f-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="d464f-129">Valitse **Kuljetustenhallinta &gt; Suunnittelu &gt; Kuormituksen luonnin työtila**.</span><span class="sxs-lookup"><span data-stu-id="d464f-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="d464f-130">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="d464f-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="d464f-131">Valitse strategia **Kuormituksen luontistrategia** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="d464f-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="d464f-132">Jos olet määrittänyt kuormituksen luontimallin ja määrittänyt siihen kuormituksen luontistrategian, valitse toimintoruudun **Mallien hallinta** -välilehdessä **Käytä mallia**.</span><span class="sxs-lookup"><span data-stu-id="d464f-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="d464f-133">Valitse sitten avattavassa **Käytä kuormituksen luontimallia** -valintaikkunassa malli **Kuormituksen luontimallin nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="d464f-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="d464f-134">Valitse **Kuormitusmallien järjestys** -pikavälilehdessä vähintään yksi [kuormitusmalli](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="d464f-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="d464f-135">Työtila yrittää sovittaa kuormituksen tämän tyyppisiin kontteihin tässä määritetyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="d464f-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="d464f-136">Yleensä pienin kontti kannattaa sijoittaa ensimmäiseksi luetteloon, sillä näin varmistetaan, että pienin mahdollinen kontti valitaan ensimmäisenä.</span><span class="sxs-lookup"><span data-stu-id="d464f-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="d464f-137">Valitse toimintoruudussa **Ehdota kuormia**.</span><span class="sxs-lookup"><span data-stu-id="d464f-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="d464f-138">Tarkista ehdotetut kuormat ja ehdotetut kuormarivit.</span><span class="sxs-lookup"><span data-stu-id="d464f-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="d464f-139">Luo **Ehdotetut kuormarivit** -pikavälilehden lähdeasiakirjan riveihin perustuvat kuormat valitsemalla toimintoruudussa **Luo kuormat**.</span><span class="sxs-lookup"><span data-stu-id="d464f-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="d464f-140">Sulje **Kuormituksen luonnin työtila** -sivu.</span><span class="sxs-lookup"><span data-stu-id="d464f-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]