---
title: Kustannusobjektien luominen
description: Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operations, Enterprise Editionin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "322671"
---
# <a name="create-cost-objects"></a><span data-ttu-id="cd330-103">Kustannusobjektien luominen</span><span class="sxs-lookup"><span data-stu-id="cd330-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd330-104">Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operations, Enterprise Editionin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.</span><span class="sxs-lookup"><span data-stu-id="cd330-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="cd330-105">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="cd330-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="cd330-106">Tätä toimintaohje koskee Kustannuslaskennan toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="cd330-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="cd330-107">Luo uudet kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="cd330-107">Create new cost objects</span></span>
1. <span data-ttu-id="cd330-108">Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="cd330-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="cd330-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="cd330-109">Click New.</span></span>
3. <span data-ttu-id="cd330-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cd330-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cd330-111">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cd330-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="cd330-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cd330-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="cd330-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="cd330-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="cd330-114">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="cd330-114">Configure the data connector</span></span>
1. <span data-ttu-id="cd330-115">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="cd330-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="cd330-116">Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="cd330-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="cd330-117">Valitse Dimension nimi -kentässä Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="cd330-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="cd330-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cd330-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="cd330-119">Tuo kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="cd330-119">Import cost centers</span></span>
1. <span data-ttu-id="cd330-120">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="cd330-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="cd330-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cd330-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="cd330-122">Näytä tuodut kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="cd330-122">View the imported cost centers</span></span>
1. <span data-ttu-id="cd330-123">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="cd330-123">Click View dimension members.</span></span>

