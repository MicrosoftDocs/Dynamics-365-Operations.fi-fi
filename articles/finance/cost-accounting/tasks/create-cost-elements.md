---
title: Luo kustannustasot
description: Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c4c1e2aee7ba98c1cca378286afb643eaca1600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810075"
---
# <a name="create-cost-elements"></a><span data-ttu-id="64b24-103">Luo kustannustasot</span><span class="sxs-lookup"><span data-stu-id="64b24-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64b24-104">Kustannuselementtien luomiseen Kustannuslaskennassa on useita keinoja.</span><span class="sxs-lookup"><span data-stu-id="64b24-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="64b24-105">Tässä menettelyssä kuvataan, miten kustannuselementtejä luodaan tuomalla päätilejä tietoyhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="64b24-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="64b24-106">Tämän menettelyn luomisessa käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="64b24-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="64b24-107">Tätä toimintaohje koskee Kustannuslaskennan toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="64b24-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="64b24-108">Luo uudet kustannustasot</span><span class="sxs-lookup"><span data-stu-id="64b24-108">Create new cost elements</span></span>
1. <span data-ttu-id="64b24-109">Valitse Kustannuslaskenta > Dimensiot > Kustannuselementin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="64b24-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="64b24-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="64b24-110">Click New.</span></span>
3. <span data-ttu-id="64b24-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="64b24-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="64b24-112">Syötä tai valitse arvo Dimension jäsenten tietoyhdistin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="64b24-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="64b24-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="64b24-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="64b24-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="64b24-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="64b24-115">Määritä tietoyhdistin</span><span class="sxs-lookup"><span data-stu-id="64b24-115">Configure the data connector</span></span>
1. <span data-ttu-id="64b24-116">Valitse Määritä dimension jäsenen lähde.</span><span class="sxs-lookup"><span data-stu-id="64b24-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="64b24-117">Anna tai valitse arvo Tilikartta-kentässä.</span><span class="sxs-lookup"><span data-stu-id="64b24-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="64b24-118">Valitse Jaettu käyttämään jaettua tilikarttaa.</span><span class="sxs-lookup"><span data-stu-id="64b24-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="64b24-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="64b24-119">Click New.</span></span>
4. <span data-ttu-id="64b24-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="64b24-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="64b24-121">Voit suodattaa tilit vastaamaan ehtojasi.</span><span class="sxs-lookup"><span data-stu-id="64b24-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="64b24-122">Anna tai valitse arvo Päätililtä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="64b24-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="64b24-123">Syötä tai valitse arvo Päätilille-kentässä.</span><span class="sxs-lookup"><span data-stu-id="64b24-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="64b24-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="64b24-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="64b24-125">Tuo päätilit</span><span class="sxs-lookup"><span data-stu-id="64b24-125">Import main accounts</span></span>
1. <span data-ttu-id="64b24-126">Valitse Tuo dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="64b24-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="64b24-127">Päätilit tuodaan kustannuslaskentaan käytettäväksi kustannuselementteinä.</span><span class="sxs-lookup"><span data-stu-id="64b24-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="64b24-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="64b24-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="64b24-129">Näytä tuodut tilit kustannuselementteinä</span><span class="sxs-lookup"><span data-stu-id="64b24-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="64b24-130">Valitse Näytä dimension jäsenet.</span><span class="sxs-lookup"><span data-stu-id="64b24-130">Click View dimension members.</span></span>
    * <span data-ttu-id="64b24-131">Näytä tuodut kirjanpitotilit yrityksesi kustannuselementteinä joihin kustannukset voivat virrata.</span><span class="sxs-lookup"><span data-stu-id="64b24-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]