---
title: 'Opas: Kysynnän ennusteen manuaalinen muokkaaminen'
description: Tässä ohjeaiheessa kerrotaan, miten nimikkeen ennustetta muokataan
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224007"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="28b41-103">Opas: Kysynnän ennusteen manuaalinen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="28b41-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28b41-104">Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan.</span><span class="sxs-lookup"><span data-stu-id="28b41-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="28b41-105">Tämä menettely on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="28b41-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="28b41-106">Valitun nimikkeen ennusteen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="28b41-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="28b41-107">Valitun nimikkeen ennusteen muokkaaminen:</span><span class="sxs-lookup"><span data-stu-id="28b41-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="28b41-108">Mene **Moduulit \> Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="28b41-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="28b41-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="28b41-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="28b41-110">Valitse nimike, jonka ennustetta haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="28b41-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="28b41-111">Avaa toimintoruudun **Suunnitelma**-välilehti ja valitse **Kysyntäennuste**.</span><span class="sxs-lookup"><span data-stu-id="28b41-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="28b41-112">Valitse luettelosta rivi.</span><span class="sxs-lookup"><span data-stu-id="28b41-112">In the list, select a row.</span></span> <span data-ttu-id="28b41-113">Jos ennusterivejä ei ole, luo uusi rivi valitsemalla toimintoruudusta **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="28b41-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="28b41-114">Syötä positiivinen luku **Myyntimäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="28b41-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="28b41-115">Tämä luku kertoo nimikkeen ennustetun määrän.</span><span class="sxs-lookup"><span data-stu-id="28b41-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="28b41-116">Näyttöön tulee virheilmoitus, jos olet syöttänyt negatiivisen luvun.</span><span class="sxs-lookup"><span data-stu-id="28b41-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="28b41-117">Täytä muiden kenttien tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="28b41-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="28b41-118">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="28b41-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="28b41-119">Yhden tai useamman nimikkeen ennusteen muokkaaminen Microsoft Excelissä</span><span class="sxs-lookup"><span data-stu-id="28b41-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="28b41-120">Yhden tai useamman nimikkeen ennusteen muokkaaminen Microsoft Excelissä:</span><span class="sxs-lookup"><span data-stu-id="28b41-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="28b41-121">Tee jompikumpi seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="28b41-121">Do one of the following:</span></span>
    - <span data-ttu-id="28b41-122">Avaa **Tarveennuste**-sivu nimikkeelle (ei merkitystä mikä niistä) edellisen osan ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="28b41-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="28b41-123">Siirry kohtaan **Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteen syöttö \> Kysynnän ennusteen rivit**.</span><span class="sxs-lookup"><span data-stu-id="28b41-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="28b41-124">Valitse toimintoruudussa **Avaa Microsoft Officessa \> Kysynnän ennusteen syöttö**.</span><span class="sxs-lookup"><span data-stu-id="28b41-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="28b41-125">Valitse ladatun tiedoston sijainti, tallenna ja avaa sitten ladattu tiedosto Excelissä.</span><span class="sxs-lookup"><span data-stu-id="28b41-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="28b41-126">Jos näyttöön tulee varoitus, valitse **Ota muokkaus käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="28b41-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="28b41-127">Kirjaudu Excelissä Supply Chain Managementiin Microsoft Dynamicsin tehtäväruudun avulla.</span><span class="sxs-lookup"><span data-stu-id="28b41-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="28b41-128">Kirjaudu sisään **Pysy sisäänkirjautuneena** -vaihtoehdolla, ja sinun on luotettava tietoyhteyssovellukseen.</span><span class="sxs-lookup"><span data-stu-id="28b41-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="28b41-129">Excel-taulukko näyttää nyt kaikki yrityksesi nykyiset tarve-ennusterivit.</span><span class="sxs-lookup"><span data-stu-id="28b41-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="28b41-130">Lisää, poista ja muokkaa kysynnän ennusterivejä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="28b41-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="28b41-131">Valitse Microsoft Dynamics -tehtäväruudussa **Julkaise**, jos haluat ladata muutokset takaisin Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="28b41-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
