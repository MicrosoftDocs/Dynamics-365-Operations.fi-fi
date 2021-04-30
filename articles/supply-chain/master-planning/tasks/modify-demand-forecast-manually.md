---
title: Kysynnän ennusteen manuaalinen muokkaaminen
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889021"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="7cf21-103">Kysynnän ennusteen manuaalinen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7cf21-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7cf21-104">Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan.</span><span class="sxs-lookup"><span data-stu-id="7cf21-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="7cf21-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="7cf21-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7cf21-106">Tämä menettely on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="7cf21-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="7cf21-107">Valitun nimikkeen ennusteen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7cf21-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="7cf21-108">Valitun nimikkeen ennusteen muokkaaminen:</span><span class="sxs-lookup"><span data-stu-id="7cf21-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="7cf21-109">Mene **Moduulit \> Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="7cf21-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7cf21-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7cf21-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="7cf21-111">Valitse nimike, jonka ennustetta haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="7cf21-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="7cf21-112">Avaa toimintoruudun **Suunnitelma**-välilehti ja valitse **Kysyntäennuste**.</span><span class="sxs-lookup"><span data-stu-id="7cf21-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="7cf21-113">Valitse luettelosta rivi.</span><span class="sxs-lookup"><span data-stu-id="7cf21-113">In the list, select a row.</span></span> <span data-ttu-id="7cf21-114">Jos ennusterivejä ei ole, luo uusi rivi valitsemalla toimintoruudusta **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7cf21-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="7cf21-115">Syötä positiivinen luku **Myyntimäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7cf21-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="7cf21-116">Tämä luku kertoo nimikkeen ennustetun määrän.</span><span class="sxs-lookup"><span data-stu-id="7cf21-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="7cf21-117">Näyttöön tulee virheilmoitus, jos olet syöttänyt negatiivisen luvun.</span><span class="sxs-lookup"><span data-stu-id="7cf21-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="7cf21-118">Täytä muiden kenttien tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="7cf21-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="7cf21-119">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7cf21-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="7cf21-120">Yhden tai useamman nimikkeen ennusteen muokkaaminen Microsoft Excelissä</span><span class="sxs-lookup"><span data-stu-id="7cf21-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="7cf21-121">Yhden tai useamman nimikkeen ennusteen muokkaaminen Microsoft Excelissä:</span><span class="sxs-lookup"><span data-stu-id="7cf21-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="7cf21-122">Tee jompikumpi seuraavista toimista:</span><span class="sxs-lookup"><span data-stu-id="7cf21-122">Do one of the following:</span></span>
    - <span data-ttu-id="7cf21-123">Avaa **Tarveennuste**-sivu nimikkeelle (ei merkitystä mikä niistä) edellisen osan ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7cf21-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="7cf21-124">Siirry kohtaan **Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteen syöttö \> Kysynnän ennusteen rivit**.</span><span class="sxs-lookup"><span data-stu-id="7cf21-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="7cf21-125">Valitse toimintoruudussa **Avaa Microsoft Officessa \> Kysynnän ennusteen syöttö**.</span><span class="sxs-lookup"><span data-stu-id="7cf21-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="7cf21-126">Valitse ladatun tiedoston sijainti, tallenna ja avaa sitten ladattu tiedosto Excelissä.</span><span class="sxs-lookup"><span data-stu-id="7cf21-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="7cf21-127">Jos näyttöön tulee varoitus, valitse **Ota muokkaus käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="7cf21-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="7cf21-128">Kirjaudu Excelissä Supply Chain Managementiin Microsoft Dynamicsin tehtäväruudun avulla.</span><span class="sxs-lookup"><span data-stu-id="7cf21-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="7cf21-129">Kirjaudu sisään **Pysy sisäänkirjautuneena** -vaihtoehdolla, ja sinun on luotettava tietoyhteyssovellukseen.</span><span class="sxs-lookup"><span data-stu-id="7cf21-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="7cf21-130">Excel-taulukko näyttää nyt kaikki yrityksesi nykyiset tarve-ennusterivit.</span><span class="sxs-lookup"><span data-stu-id="7cf21-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="7cf21-131">Lisää, poista ja muokkaa kysynnän ennusterivejä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7cf21-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="7cf21-132">Valitse Microsoft Dynamics -tehtäväruudussa **Julkaise**, jos haluat ladata muutokset takaisin Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="7cf21-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
