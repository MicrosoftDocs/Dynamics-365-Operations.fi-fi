---
title: Lisää tuotevariantteja ostotilauksiin käyttämällä muuttuvia painotuksia
description: Tässä menettelyssä kerrotaan, miten kunkin tuotevariantin ostotilausrivit täytetään automaattisesti variantin painojen avulla.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446260a09bd5177877637ac8a288ad584dfa2b2b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568693"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="f6c91-103">Lisää tuotevariantteja ostotilauksiin käyttämällä muuttuvia painotuksia</span><span class="sxs-lookup"><span data-stu-id="f6c91-103">Add variant products to purchase orders using variant weights</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6c91-104">Tässä menettelyssä kerrotaan, miten kunkin tuotevariantin ostotilausrivit täytetään automaattisesti variantin painojen avulla.</span><span class="sxs-lookup"><span data-stu-id="f6c91-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="f6c91-105">Kun ostettavan tuotteen määrä on valittu, kaikille tuotevarianteille luodaan ostotilausrivit. Ne sisältävät ehdotetut määrät tuotevariantille määritettyjen painojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="f6c91-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="f6c91-106">Tämä menettely ei sisällä tuotedimensioiden ja tuotevarianttien painoarvojen määrityksen vaiheita.</span><span class="sxs-lookup"><span data-stu-id="f6c91-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="f6c91-107">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="f6c91-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f6c91-108">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="f6c91-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f6c91-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f6c91-109">Click New.</span></span>
3. <span data-ttu-id="f6c91-110">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f6c91-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f6c91-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f6c91-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f6c91-112">Ota käyttöön Yleinen-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="f6c91-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="f6c91-113">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="f6c91-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f6c91-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f6c91-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f6c91-115">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f6c91-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f6c91-116">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f6c91-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f6c91-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f6c91-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f6c91-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f6c91-118">Click OK.</span></span>
12. <span data-ttu-id="f6c91-119">Ota käyttöön Rivitiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="f6c91-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="f6c91-120">Valitse Variantit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f6c91-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="f6c91-121">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="f6c91-121">Click Add line.</span></span>
15. <span data-ttu-id="f6c91-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f6c91-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="f6c91-123">Kirjoita Nimiketunnus-kenttään 0140.</span><span class="sxs-lookup"><span data-stu-id="f6c91-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="f6c91-124">Valitse määräksi 1000.</span><span class="sxs-lookup"><span data-stu-id="f6c91-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="f6c91-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f6c91-125">Click Save.</span></span>

