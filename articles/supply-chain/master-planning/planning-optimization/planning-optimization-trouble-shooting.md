---
title: Suunnittelun optimoinnin vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita suunnittelun optimoinnin käytössä voi esiintyä.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812880"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="0395f-103">Suunnittelun optimoinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="0395f-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0395f-104">Tässä ohjeaiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita suunnittelun optimoinnin käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="0395f-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="0395f-105">Suunnittelun optimoinnin lisäosa ei asennu loppuun asti</span><span class="sxs-lookup"><span data-stu-id="0395f-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="0395f-106">Suunnittelun optimointi edellyttää korkean käytettävyyden ympäristöä, jossa Lifecycle Services (LCS) on käytössä ja jonka taso on 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on lisäksi oltava Dynamics 365 Supply Chain Managementin versio 10.0.7 tai sitä uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="0395f-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="0395f-107">Jos lisäosa yritetään asentaa OneBox-ympäristöön, asennusta ei suoriteta loppuun.</span><span class="sxs-lookup"><span data-stu-id="0395f-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="0395f-108">**Korjaus**: peruuta asennus ja käytä korkean käytettävyyden tason 2 tai sitä korkeampaa ympäristöä (ei OneBox-ympäristöä).</span><span class="sxs-lookup"><span data-stu-id="0395f-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="0395f-109">Erätöiden suunnittelu epäonnistuu, kun suunnittelun optimointi on käytössä</span><span class="sxs-lookup"><span data-stu-id="0395f-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="0395f-110">Kun suunnittelun optimointi otetaan käyttöön, sisäinen pääsuunnittelumoduuli poistetaan automaattisesti käytöstä.</span><span class="sxs-lookup"><span data-stu-id="0395f-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="0395f-111">Supply Chain Managementin sisäiseen suunnittelumoduuliin luodut pääsuunnittelun erätyöt epäonnistuvat, jos ne ovat käynnistyneet suunnittelun optimoinnin ollessa käytössä.</span><span class="sxs-lookup"><span data-stu-id="0395f-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="0395f-112">Näkyviin voi tulla esimerkiksi seuraavankaltainen virhesanoma, jonka mukaan *tämä toiminto käynnisti pääsuunnittelun, jota ei tueta, kun suunnittelun optimointi on otettu käyttöön*.</span><span class="sxs-lookup"><span data-stu-id="0395f-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="0395f-113">**Korjaus**: peruuta kaikki pääsuunnittelutyöt, jotka luotiin Supply Chain Managementin sisäiseen suunnittelumoduuliin.</span><span class="sxs-lookup"><span data-stu-id="0395f-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="0395f-114">Suunnittelun optimoinnin tulokset poikkeavat aiemmista tuloksista</span><span class="sxs-lookup"><span data-stu-id="0395f-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="0395f-115">Suunnittelun optimointi poikkeaa sisäisestä pääsuunnittelun rakenteesta joillakin alueilla.</span><span class="sxs-lookup"><span data-stu-id="0395f-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="0395f-116">Myös odottavat toiminnot voivat aiheuttaa tämän.</span><span class="sxs-lookup"><span data-stu-id="0395f-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="0395f-117">**Korjaus**: Suorita suunnittelun optimoinnin kuntoanalyysi ja analysoi sitten tulokset samalla, kun selvität, mikä vaikutus niillä on liittyvän dokumentaation avulla.</span><span class="sxs-lookup"><span data-stu-id="0395f-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="0395f-118">Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0395f-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="0395f-119">Suunnittelun optimointia ei voi ottaa käyttöön</span><span class="sxs-lookup"><span data-stu-id="0395f-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="0395f-120">**Yhteystila**-arvon on oltava **Yhdistetty**, ennen kuin **Käytä suunnittelun optimointi** -asetukseksi voi määrittää **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0395f-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="0395f-121">Lisätietoja on kohdassa [Suunnittelun optimoinnin käytön aloittaminen](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="0395f-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="0395f-122">**Korjaus**: varmista, että suunnittelun optimoinnin lisäosa asennettiin oikein.</span><span class="sxs-lookup"><span data-stu-id="0395f-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="0395f-123">Saatavuuden (CTP:n) aikana näkyy virhesanoma</span><span class="sxs-lookup"><span data-stu-id="0395f-123">Error message is shown during CTP</span></span>

<span data-ttu-id="0395f-124">Jos yrittää suorittaa saatavuuden (CTP:n) myyntitilauksesta, kun suunnittelun optimointi on otettu käyttöön, näkyviin tulee seuraava virhesanoma, jonka mukaan *tämä toiminto käynnisti pääsuunnittelun, jota ei tuettu, kun suunnittelun optimointi on käytössä*.</span><span class="sxs-lookup"><span data-stu-id="0395f-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="0395f-125">Tämä liittyy odottavaan toimintoon, joka suunniteltu tuotantotilausten tuen osaksi.</span><span class="sxs-lookup"><span data-stu-id="0395f-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="0395f-126">**Korjaus:** vältä saatavuuden (CTP:n) laskelmia, kun suunnittelun optimointi on käytössä, kunnes saatavuuden (CTP:n) tuki on saatavana.</span><span class="sxs-lookup"><span data-stu-id="0395f-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0395f-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0395f-127">Additional resources</span></span>

[<span data-ttu-id="0395f-128">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="0395f-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="0395f-129">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="0395f-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]