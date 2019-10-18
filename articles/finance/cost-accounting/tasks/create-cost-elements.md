---
title: Luo kustannustasot
description: Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187794"
---
# <a name="create-cost-elements"></a><span data-ttu-id="55151-103">Luo kustannustasot</span><span class="sxs-lookup"><span data-stu-id="55151-103">Create cost elements</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55151-104">Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja.</span><span class="sxs-lookup"><span data-stu-id="55151-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="55151-105">Tässä menettelyssä kuvataan, miten kustannuselementtejä luodaan tuomalla päätilejä tietoyhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="55151-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="55151-106">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="55151-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="55151-107">Tätä toimintaohje koskee Kustannuslaskennan toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="55151-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="55151-108">Luo uudet kustannustasot</span><span class="sxs-lookup"><span data-stu-id="55151-108">Create new cost elements</span></span>
1. <span data-ttu-id="55151-109">Valitse Kustannuslaskenta > Dimensiot > Kustannuselementin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="55151-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="55151-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="55151-110">Click New.</span></span>
3. <span data-ttu-id="55151-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55151-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="55151-112">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="55151-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="55151-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55151-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="55151-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="55151-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="55151-115">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="55151-115">Configure the data connector</span></span>
1. <span data-ttu-id="55151-116">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="55151-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="55151-117">Anna tai valitse arvo Tilikartta-kentässä.</span><span class="sxs-lookup"><span data-stu-id="55151-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="55151-118">Valitse Jaettu käyttämään jaettua tilikarttaa.</span><span class="sxs-lookup"><span data-stu-id="55151-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="55151-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="55151-119">Click New.</span></span>
4. <span data-ttu-id="55151-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="55151-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="55151-121">Voit suodattaa tilit vastaamaan ehtojasi.</span><span class="sxs-lookup"><span data-stu-id="55151-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="55151-122">Anna tai valitse arvo Päätililtä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="55151-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="55151-123">Syötä tai valitse arvo Päätilille-kentässä.</span><span class="sxs-lookup"><span data-stu-id="55151-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="55151-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="55151-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="55151-125">Tuo päätilit</span><span class="sxs-lookup"><span data-stu-id="55151-125">Import main accounts</span></span>
1. <span data-ttu-id="55151-126">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="55151-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="55151-127">Päätilit tuodaan kustannuslaskentaan käytettäväksi kustannuselementteinä.</span><span class="sxs-lookup"><span data-stu-id="55151-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="55151-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="55151-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="55151-129">Näytä tuodut tilit kustannuselementteinä</span><span class="sxs-lookup"><span data-stu-id="55151-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="55151-130">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="55151-130">Click View dimension members.</span></span>
    * <span data-ttu-id="55151-131">Näytä tuodut kirjanpitotilit yrityksesi kustannuselementteinä joihin kustannukset voivat virrata.</span><span class="sxs-lookup"><span data-stu-id="55151-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  
