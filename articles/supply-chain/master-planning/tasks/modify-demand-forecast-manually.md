---
title: Muuta ennustetta manuaalisesti
description: Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca6b881bc094b68d1bbf8c7c20b65418e42b28e3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835864"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="80115-103">Muuta ennustetta manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="80115-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80115-104">Tässä menettelyssä kerrotaan, miten nimikkeen ennustetta muokataan.</span><span class="sxs-lookup"><span data-stu-id="80115-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="80115-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="80115-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="80115-106">Tämä tallenne on tarkoitettu tuotannon suunnittelijalle.</span><span class="sxs-lookup"><span data-stu-id="80115-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="80115-107">Nimikkeen ennusteen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="80115-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="80115-108">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="80115-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="80115-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="80115-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="80115-110">Valitse nimike, jonka ennustetta haluat muokata.</span><span class="sxs-lookup"><span data-stu-id="80115-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="80115-111">Valitse esimerkiksi nimike D0001.</span><span class="sxs-lookup"><span data-stu-id="80115-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="80115-112">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="80115-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="80115-113">Valitse Kysynnän ennuste.</span><span class="sxs-lookup"><span data-stu-id="80115-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="80115-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="80115-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="80115-115">Jos ennusterivejä ei ole, luo uusi rivi</span><span class="sxs-lookup"><span data-stu-id="80115-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="80115-116">valitsemalla sovelluspalkista Uusi.</span><span class="sxs-lookup"><span data-stu-id="80115-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="80115-117">Syötä numero Myyntimäärä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="80115-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="80115-118">Tämä luku kertoo nimikkeen ennustetun määrän.</span><span class="sxs-lookup"><span data-stu-id="80115-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="80115-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="80115-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="80115-120">Ennusteen muokkaaminen Excelissä</span><span class="sxs-lookup"><span data-stu-id="80115-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="80115-121">Valitse Avaa Microsoft Officessa.</span><span class="sxs-lookup"><span data-stu-id="80115-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="80115-122">Valitse Muokkaa kysynnän ennustetta Excelissä.</span><span class="sxs-lookup"><span data-stu-id="80115-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="80115-123">Excelissä voit lisätä, poistaa ja muokata kysynnän ennusterivejä.</span><span class="sxs-lookup"><span data-stu-id="80115-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="80115-124">Jos et näe tietoja Excelissä, kirjaudu Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin niin, että Pidä minut kirjautuneena -asetus on käytössä. Sinun on myös luotettava tietoyhteyssovellukseen.</span><span class="sxs-lookup"><span data-stu-id="80115-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

