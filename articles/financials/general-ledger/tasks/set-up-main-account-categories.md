---
title: Määritä päätilien luokat
description: Päätilin luokkia käytetään raportoinnin oletusraporteissa ja Power BI:ssa.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46c7c86b93a3471ba10ec7ae6789f227bc9779c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "311447"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="b036f-103">Määritä päätilien luokat</span><span class="sxs-lookup"><span data-stu-id="b036f-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b036f-104">Päätilin luokkia käytetään raportoinnin oletusraporteissa ja Power BI:ssa.</span><span class="sxs-lookup"><span data-stu-id="b036f-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="b036f-105">Oletusarvoisesti luodut päätilin luokille voidaan määrittää uusi nimi mutta niitä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="b036f-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="b036f-106">Tililuokkia voidaan luoda lisää raportointia ja analysointia varten.</span><span class="sxs-lookup"><span data-stu-id="b036f-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="b036f-107">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="b036f-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="b036f-108">Luo päätilin luokka</span><span class="sxs-lookup"><span data-stu-id="b036f-108">Create a main account category</span></span>
1. <span data-ttu-id="b036f-109">Valitse Kirjanpito > Tilikartta > Tilit > Päätililuokat.</span><span class="sxs-lookup"><span data-stu-id="b036f-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="b036f-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b036f-110">Click New.</span></span>
3. <span data-ttu-id="b036f-111">Anna Päätililuokat-kentässä yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="b036f-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="b036f-112">Kirjoita päätilin luokan kuvaus Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b036f-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="b036f-113">Valitse Päätilin tyyppi -kentässä luokkaan linkitettävä päätilin tyyppi.</span><span class="sxs-lookup"><span data-stu-id="b036f-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="b036f-114">Linkitä päätilit tililuokkiin</span><span class="sxs-lookup"><span data-stu-id="b036f-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="b036f-115">Valitse Linkitä päätilit.</span><span class="sxs-lookup"><span data-stu-id="b036f-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="b036f-116">Valitse luettelossa päätilin luokkaan määritettävät päätilit.</span><span class="sxs-lookup"><span data-stu-id="b036f-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="b036f-117">Päätilien määrittäminen päätilin luokkaan koostaa tilien saldot, kun kyseistä luokkaa käytetään raportointiin ja analysointiin.</span><span class="sxs-lookup"><span data-stu-id="b036f-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="b036f-118">Valitse päätilit valitsemalla Linkitetty-vaihtoehto tai poistamalla sen valinta.</span><span class="sxs-lookup"><span data-stu-id="b036f-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="b036f-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b036f-119">Click OK.</span></span>
5. <span data-ttu-id="b036f-120">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b036f-120">Click Yes.</span></span>

