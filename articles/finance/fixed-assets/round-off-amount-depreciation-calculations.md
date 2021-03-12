---
title: Poistojen laskennan pyöristyssumma
description: Tässä artikkelissa käsitellään Kirja-asetussivuilta löytyvää Poiston pyöristys -kenttää.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8662f0731abd089c9039c16bb77e39c1d3e51
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976012"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="14e68-103">Poistojen laskennan pyöristyssumma</span><span class="sxs-lookup"><span data-stu-id="14e68-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14e68-104">Tässä artikkelissa käsitellään Kirja-asetussivuilta löytyvää Poiston pyöristys -kenttää.</span><span class="sxs-lookup"><span data-stu-id="14e68-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="14e68-105">Poiston pyöristyssummat määritetään erikseen jokaiselle kirjalle.</span><span class="sxs-lookup"><span data-stu-id="14e68-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="14e68-106">Poiston pyöristyssummia käytetään käyttöomaisuuserän poistoprofiilissa, joka sisältää tulevat poistot ja käyttöomaisuuserän arvon, ja lisäksi myös poistoehdotuksissa.</span><span class="sxs-lookup"><span data-stu-id="14e68-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="14e68-107">Kirjan pienin kirjalle sallittu poisto.</span><span class="sxs-lookup"><span data-stu-id="14e68-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="14e68-108">Viimeisen poistokauden poistosummaa ei määritetystä pyöristyksestä riippumatta pyöristetä.</span><span class="sxs-lookup"><span data-stu-id="14e68-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="14e68-109">Viimeisen poistokauden lopussa käyttöomaisuuden arvon on oltava 0 (nolla) tai jäännösarvo, jos jäännösarvot ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="14e68-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="14e68-110">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="14e68-110">Example</span></span>

<span data-ttu-id="14e68-111">Poistoksi on laskettu ilman pyöristyksiä 2 444,44.</span><span class="sxs-lookup"><span data-stu-id="14e68-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="14e68-112">Kuten seuraavasta taulukosta selviää, ehdotetut summat vaihtelevat sen mukaan, miten pyöristys on määritetty.</span><span class="sxs-lookup"><span data-stu-id="14e68-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="14e68-113">Pyöristystapa</span><span class="sxs-lookup"><span data-stu-id="14e68-113">Rounding method</span></span> | <span data-ttu-id="14e68-114">Poiston määrä</span><span class="sxs-lookup"><span data-stu-id="14e68-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="14e68-115">Pyöristys 0,1</span><span class="sxs-lookup"><span data-stu-id="14e68-115">Rounding 0.1</span></span>    | <span data-ttu-id="14e68-116">2 444,40</span><span class="sxs-lookup"><span data-stu-id="14e68-116">2,444.40</span></span>            |
| <span data-ttu-id="14e68-117">Pyöristys 1,00</span><span class="sxs-lookup"><span data-stu-id="14e68-117">Rounding 1.00</span></span>   | <span data-ttu-id="14e68-118">2 444,00</span><span class="sxs-lookup"><span data-stu-id="14e68-118">2,444.00</span></span>            |
| <span data-ttu-id="14e68-119">Pyöristys 10,00</span><span class="sxs-lookup"><span data-stu-id="14e68-119">Rounding 10.00</span></span>  | <span data-ttu-id="14e68-120">2 440,00</span><span class="sxs-lookup"><span data-stu-id="14e68-120">2,440.00</span></span>            |
| <span data-ttu-id="14e68-121">Pyöristys 100,00</span><span class="sxs-lookup"><span data-stu-id="14e68-121">Rounding 100.00</span></span> | <span data-ttu-id="14e68-122">2 400,00</span><span class="sxs-lookup"><span data-stu-id="14e68-122">2,400.00</span></span>            |





