---
title: Tuotannon varianssien yleiset lähteet
description: Tässä artikkelissa selitetään tyypillisiä tuotannon varianssin tyyppien lähteitä.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55d108ff71f0af773fa521833d57ce96d36251fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008238"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="5c851-103">Tuotannon varianssien yleiset lähteet</span><span class="sxs-lookup"><span data-stu-id="5c851-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c851-104">Tässä artikkelissa selitetään tyypillisiä tuotannon varianssin tyyppien lähteitä.</span><span class="sxs-lookup"><span data-stu-id="5c851-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="5c851-105">Seuraavassa on joitakin tyypillisiä **eräkoon** varianssin lähteitä:</span><span class="sxs-lookup"><span data-stu-id="5c851-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="5c851-106">Tuotantotilauksen hyväksytty määrä poikkeaa vakiokustannuslaskennassa käytetystä laskelman määrästä.</span><span class="sxs-lookup"><span data-stu-id="5c851-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="5c851-107">Määrää käytetään vakiokustannusten kuoletuksen perustana.</span><span class="sxs-lookup"><span data-stu-id="5c851-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="5c851-108">Tuotantotilauksen vakiokustannusten arvo poikkeaa vakiokustannuslaskennassa käytetyistä vakiokustannuksista.</span><span class="sxs-lookup"><span data-stu-id="5c851-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="5c851-109">Tuotantotilauksen vakiokustannukset voivat olla erilaisia monista eri syistä.</span><span class="sxs-lookup"><span data-stu-id="5c851-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="5c851-110">Vakiokustannuksiin voivat vaikuttaa esimerkiksi seuraavat tekijät:</span><span class="sxs-lookup"><span data-stu-id="5c851-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="5c851-111">Tuotannon tuoterakenteen (BOM) tai reitityksen manuaaliset muutokset</span><span class="sxs-lookup"><span data-stu-id="5c851-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="5c851-112">Toisen tuoterakenneversion (BOM) tai reititysversion valinta tuotantotilausta luotaessa</span><span class="sxs-lookup"><span data-stu-id="5c851-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="5c851-113">Suunnitellut muutokset nimikkeelle määritetyssä tuoterakenneversiossa tai reitityksessä.</span><span class="sxs-lookup"><span data-stu-id="5c851-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="5c851-114">Seuraavassa on joitakin tyypillisiä **tuotantohinnan** varianssin lähteitä:</span><span class="sxs-lookup"><span data-stu-id="5c851-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="5c851-115">Reititystoiminnon ilmoitetun kulutuksen kustannusluokka (ja kustannusluokan hinta) eroavat vakiokustannuslaskennassa käytettävästä kustannusluokasta.</span><span class="sxs-lookup"><span data-stu-id="5c851-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="5c851-116">Kustannusluokan hinnan aktiivinen kustannus eroaa vakiokustannuslaskennassa käytettävästä kustannusluokan hinnasta.</span><span class="sxs-lookup"><span data-stu-id="5c851-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="5c851-117">Seuraavassa on joitakin tyypillisiä **tuotantomäärän** varianssin lähteitä:</span><span class="sxs-lookup"><span data-stu-id="5c851-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="5c851-118">Materiaalikomponentteja otetaan varastosta liikaa tai liian vähän.</span><span class="sxs-lookup"><span data-stu-id="5c851-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="5c851-119">Reititystoiminnon raportointiaika on liian pitkä tai liian lyhyt.</span><span class="sxs-lookup"><span data-stu-id="5c851-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="5c851-120">Tilauksen määrään liittyvän päänimikkeen hyväksytty määrä ylitetään tai alitetaan.</span><span class="sxs-lookup"><span data-stu-id="5c851-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="5c851-121">Kuitenkin tuotantotilauksen tilausmäärään perustuvat komponentit otetaan samalla varastosta kokonaan ja tuotantotilauksen tilausmäärään perustuvat toiminnot raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="5c851-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="5c851-122">Seuraavassa on joitakin tyypillisiä **Tuotannon korvaus** varianssin lähteitä:</span><span class="sxs-lookup"><span data-stu-id="5c851-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="5c851-123">Varastosta otetaan materiaalikomponentti, jota ei ole tuotannon tuoterakenteessa.</span><span class="sxs-lookup"><span data-stu-id="5c851-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="5c851-124">Tuotannon tuoterakenteeseen lisätään komponentti ja raportoidaan se kulutetuksi manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5c851-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="5c851-125">Raportoidaan nimike kulutetuksi, muttei lisätä sitä manuaalisesti tuotannon tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="5c851-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="5c851-126">Tuotannon reititykseen lisätään toiminto, joka raportoidaan kulutetuksi manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5c851-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="5c851-127">Valitaan eri tuoterakenneversio tuotantotilausta luotaessa, jolloin tuoterakenneversio eroaa vakiokustannuslaskennassa käytettävästä tuoterakenneversiosta.</span><span class="sxs-lookup"><span data-stu-id="5c851-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="5c851-128">Valitaan eri reititysversio tuotantotilausta luotaessa, jolloin reititysversio eroaa vakiokustannuslaskennassa käytettävästä reititysversiosta.</span><span class="sxs-lookup"><span data-stu-id="5c851-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




