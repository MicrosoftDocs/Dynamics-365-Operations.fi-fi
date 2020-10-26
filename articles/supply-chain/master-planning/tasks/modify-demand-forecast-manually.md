---
title: Muuta ennustetta manuaalisesti
description: Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan.
author: ShylaThompson
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 105cf50698889e81804155cdac3a8b484cbf87d7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987163"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="42cf9-103">Muuta ennustetta manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="42cf9-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42cf9-104">Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan.</span><span class="sxs-lookup"><span data-stu-id="42cf9-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="42cf9-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="42cf9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="42cf9-106">Tämä tallenne on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="42cf9-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="42cf9-107">Nimikkeen ennusteen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="42cf9-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="42cf9-108">Valitse **siirtymisruudussa** **Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="42cf9-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="42cf9-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="42cf9-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="42cf9-110">Valitse nimike, jonka ennustetta haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="42cf9-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="42cf9-111">Valitse esimerkiksi nimike D0001.</span><span class="sxs-lookup"><span data-stu-id="42cf9-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="42cf9-112">Valitse **toimintoruudussa** **Suunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="42cf9-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="42cf9-113">Valitse **Kysynnän ennuste**.</span><span class="sxs-lookup"><span data-stu-id="42cf9-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="42cf9-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="42cf9-114">In the list, mark the selected row.</span></span> <span data-ttu-id="42cf9-115">Jos ennusterivejä ei ole, luo uusi rivi valitsemalla sovelluspalkista Uusi.</span><span class="sxs-lookup"><span data-stu-id="42cf9-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="42cf9-116">Syötä numero **Myyntimäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="42cf9-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="42cf9-117">Tämä luku kertoo nimikkeen ennustetun määrän.</span><span class="sxs-lookup"><span data-stu-id="42cf9-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="42cf9-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="42cf9-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="42cf9-119">Ennusteen muokkaaminen Excelissä</span><span class="sxs-lookup"><span data-stu-id="42cf9-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="42cf9-120">Valitse **Avaa** Microsoft Officessa.</span><span class="sxs-lookup"><span data-stu-id="42cf9-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="42cf9-121">Valitse **Muokkaa kysynnän ennustetta** Excelissä.</span><span class="sxs-lookup"><span data-stu-id="42cf9-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="42cf9-122">Excelissä voit lisätä, poistaa ja muokata kysynnän ennusterivejä.</span><span class="sxs-lookup"><span data-stu-id="42cf9-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="42cf9-123">Jos et näe tietoja Excelissä, kirjaudu sisään niin, että Pidä minut kirjautuneena -asetus on käytössä. Sinun on myös luotettava tietoyhteyssovellukseen.</span><span class="sxs-lookup"><span data-stu-id="42cf9-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

