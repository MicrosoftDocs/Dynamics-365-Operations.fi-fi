--- 
title: Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa
description: "Näiden ohjeiden avulla voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 906f9611370e19ad4f063d15608d3564c5292c96
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="20523-103">Toimittajien maksujen luominen ja tuonti ISO20022-maksumuodossa</span><span class="sxs-lookup"><span data-stu-id="20523-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20523-104">Näiden ohjeiden avulla voit luoda maksurivit toimittajan maksukirjauskansioon sekä luoda toimittajan maksutiedostot ISO2022-pankkisiirtoesimerkin avulla.</span><span class="sxs-lookup"><span data-stu-id="20523-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="20523-105">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="20523-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="20523-106">Tämä on viides viidestä tehtävästä, joilla esitellään toimittajamaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="20523-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="20523-107">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="20523-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="20523-108">Maksurivien luominen</span><span class="sxs-lookup"><span data-stu-id="20523-108">Create payment lines</span></span>
1. <span data-ttu-id="20523-109">Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="20523-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="20523-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="20523-110">Click New.</span></span>
3. <span data-ttu-id="20523-111">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="20523-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="20523-112">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="20523-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="20523-113">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="20523-113">Click Lines.</span></span>
6. <span data-ttu-id="20523-114">Valitse Maksuehdotus.</span><span class="sxs-lookup"><span data-stu-id="20523-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="20523-115">Valitse Luo maksuehdotus.</span><span class="sxs-lookup"><span data-stu-id="20523-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="20523-116">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="20523-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="20523-117">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="20523-117">Click Filter.</span></span>
10. <span data-ttu-id="20523-118">Valitse luettelosta Toimittajat-taulukon ja Toimittajan tili -kentän rivi.</span><span class="sxs-lookup"><span data-stu-id="20523-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="20523-119">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="20523-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="20523-120">Voit käyttää kaikkia maksettavien toimittajatapahtumien valintaehtoja, tässä esimerkissä toimittajan tilinä käytetään arvoa DE-001.</span><span class="sxs-lookup"><span data-stu-id="20523-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="20523-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="20523-121">Click OK.</span></span>
13. <span data-ttu-id="20523-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="20523-122">Click OK.</span></span>
14. <span data-ttu-id="20523-123">Valitse Luo maksut.</span><span class="sxs-lookup"><span data-stu-id="20523-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="20523-124">ISO20022-maksutiedoston luominen</span><span class="sxs-lookup"><span data-stu-id="20523-124">Generate an ISO20022 payment file</span></span>


