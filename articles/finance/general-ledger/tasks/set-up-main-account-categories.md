---
title: Määritä päätilien luokat
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää päätilien luokat Dynamics 365 Financeissa.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442694"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="1a5a2-103">Määritä päätilien luokat</span><span class="sxs-lookup"><span data-stu-id="1a5a2-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a5a2-104">Tässä ohjeaiheessa kuvataan, kuinka voit määrittää päätilien luokat.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="1a5a2-105">Päätilin luokkia käytetään raportoinnin oletusraporteissa ja Power BI:ssa.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="1a5a2-106">Oletusarvoisesti luodut päätilin luokille voidaan määrittää uusi nimi mutta niitä ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="1a5a2-107">Tililuokkia voidaan luoda lisää raportointia ja analysointia varten.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="1a5a2-108">Tässä aiheessa käytetään USMF-esittely-yritystä.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="1a5a2-109">Luo päätilin luokka</span><span class="sxs-lookup"><span data-stu-id="1a5a2-109">Create a main account category</span></span>
1. <span data-ttu-id="1a5a2-110">Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Tilit > Päätililuokat**.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="1a5a2-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-111">Select **New**.</span></span>
3. <span data-ttu-id="1a5a2-112">Anna **Päätililuokka**-kentässä yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="1a5a2-113">Kirjoita päätilin luokan kuvaus **Kuvaus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="1a5a2-114">Valitse **Päätilin tyyppi** -kentässä luokkaan linkitettävä päätilin tyyppi.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="1a5a2-115">Linkitä päätilit tililuokkiin</span><span class="sxs-lookup"><span data-stu-id="1a5a2-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="1a5a2-116">Valitse **Linkitä päätilit**.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="1a5a2-117">Valitse luettelosta päätilit, jotka liitetään päätililuokkaan, merkitsemällä **Linkitetty**-sarakkeen valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="1a5a2-118">Päätilien määrittäminen päätilin luokkaan koostaa tilien saldot, kun kyseistä luokkaa käytetään raportointiin ja analysointiin.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="1a5a2-119">Valitse päätilit valitsemalla **Linkitetty**-vaihtoehto tai poistamalla sen valinta.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="1a5a2-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-120">Select **OK**.</span></span>
5. <span data-ttu-id="1a5a2-121">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="1a5a2-121">Select **Yes**.</span></span>
