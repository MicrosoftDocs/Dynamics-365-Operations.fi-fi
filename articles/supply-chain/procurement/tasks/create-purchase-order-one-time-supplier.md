---
title: Luo ostotilaus kertatoimittajalle
description: Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26c62aa72a7919c780bb709b185b48c97066c538
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836309"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="70462-103">Luo ostotilaus kertatoimittajalle</span><span class="sxs-lookup"><span data-stu-id="70462-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70462-104">Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle.</span><span class="sxs-lookup"><span data-stu-id="70462-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="70462-105">Toimittaja luodaan automaattisesti ostotilauksen yhteydessä, sen sijaan, että toimittajatili pitäisi luoda manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="70462-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="70462-106">Ostotilaukset luo yleensä ostoedustaja.</span><span class="sxs-lookup"><span data-stu-id="70462-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="70462-107">Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja.</span><span class="sxs-lookup"><span data-stu-id="70462-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="70462-108">Luomisen edellytys on, että kertatoimittajan tili on määritetty Ostoreskontran parametrit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="70462-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="70462-109">Luo ostotilaus kertatoimittajalle</span><span class="sxs-lookup"><span data-stu-id="70462-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="70462-110">Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="70462-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="70462-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="70462-111">Click New.</span></span>
3. <span data-ttu-id="70462-112">Valitse Kertatoimittaja-kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="70462-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="70462-113">Ostotilaukselle luodaan ja määritetään automaattisesti toimittajatili.</span><span class="sxs-lookup"><span data-stu-id="70462-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="70462-114">Toimittajatili luodaan Ostoreskontran parametrit -sivun Yleiset-välilehdellä määritetyn mallin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="70462-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="70462-115">Kirjoita Nimi-kenttään toimittajan yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="70462-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="70462-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="70462-116">Click OK.</span></span>
    * <span data-ttu-id="70462-117">Ostotilauksen nyt viedä loppuun ja käsitellä kuin minkä tahansa tilauksen.</span><span class="sxs-lookup"><span data-stu-id="70462-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="70462-118">Tämän suorittamisessa ei ole mitään erityisominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="70462-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="70462-119">Laskulla tulee ilmi erääntyvä tapahtuma toimittajan tilille, joka on luotu tilausta luotaessa, jonka jälkeen maksu käsitellään.</span><span class="sxs-lookup"><span data-stu-id="70462-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="70462-120">Kun tämä on tehty, toimittajan tilin voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="70462-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="70462-121">Tämän suorittaa yleensä ostoreskontraosaston työntekijä.</span><span class="sxs-lookup"><span data-stu-id="70462-121">This is typically done by the accounts payable department.</span></span>  

