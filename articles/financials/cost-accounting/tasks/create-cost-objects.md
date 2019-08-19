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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f63827977f080aa78fb385c60f757ad6b710005
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841246"
---
# <a name="create-cost-objects"></a><span data-ttu-id="c6ad5-103">Kustannusobjektien luominen</span><span class="sxs-lookup"><span data-stu-id="c6ad5-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6ad5-104">Tässä menettelyssä kuvataan, miten luot kustannusobjekteja tuomalla Dynamics 365 for Finance and Operations, Enterprise Editionin kustannuspaikkojen taloushallinnon dimension kustannushallintaan tietoyhdistimellä.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="c6ad5-105">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="c6ad5-106">Tätä toimintaohje koskee Kustannuslaskennan toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="c6ad5-107">Luo uudet kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="c6ad5-107">Create new cost objects</span></span>
1. <span data-ttu-id="c6ad5-108">Valitse Kustannuslaskenta > Dimensiot > Kustannusobjektin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="c6ad5-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-109">Click New.</span></span>
3. <span data-ttu-id="c6ad5-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c6ad5-111">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="c6ad5-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c6ad5-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="c6ad5-114">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="c6ad5-114">Configure the data connector</span></span>
1. <span data-ttu-id="c6ad5-115">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="c6ad5-116">Valitse CostCenter tuodaksesi CostCenter-dimension kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="c6ad5-117">Valitse Dimension nimi -kentässä Kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="c6ad5-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="c6ad5-119">Tuo kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="c6ad5-119">Import cost centers</span></span>
1. <span data-ttu-id="c6ad5-120">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="c6ad5-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="c6ad5-122">Näytä tuodut kustannuspaikat</span><span class="sxs-lookup"><span data-stu-id="c6ad5-122">View the imported cost centers</span></span>
1. <span data-ttu-id="c6ad5-123">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="c6ad5-123">Click View dimension members.</span></span>

