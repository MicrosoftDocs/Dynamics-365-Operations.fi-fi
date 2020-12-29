---
title: Luo ostotilaus kertatoimittajalle
description: Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427469"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="f2a10-103">Luo ostotilaus kertatoimittajalle</span><span class="sxs-lookup"><span data-stu-id="f2a10-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2a10-104">Tässä menettelyssä näytetään, miten ostotilaus luodaan kertatoimittajalle.</span><span class="sxs-lookup"><span data-stu-id="f2a10-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="f2a10-105">Toimittaja luodaan automaattisesti ostotilauksen yhteydessä, sen sijaan, että toimittajatili pitäisi luoda manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f2a10-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="f2a10-106">Ostotilaukset luo yleensä ostoedustaja.</span><span class="sxs-lookup"><span data-stu-id="f2a10-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="f2a10-107">Tämän oppaan esimerkissä käytetään esittely-yritys USMF:n tietoja.</span><span class="sxs-lookup"><span data-stu-id="f2a10-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="f2a10-108">Luomisen edellytys on, että kertatoimittajan tili on määritetty Ostoreskontran parametrit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f2a10-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="f2a10-109">Luo ostotilaus kertatoimittajalle</span><span class="sxs-lookup"><span data-stu-id="f2a10-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="f2a10-110">Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="f2a10-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f2a10-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2a10-111">Click New.</span></span>
3. <span data-ttu-id="f2a10-112">Valitse Kertatoimittaja-kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="f2a10-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="f2a10-113">Ostotilaukselle luodaan ja määritetään automaattisesti toimittajatili.</span><span class="sxs-lookup"><span data-stu-id="f2a10-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="f2a10-114">Toimittajatili luodaan Ostoreskontran parametrit -sivun Yleiset-välilehdellä määritetyn mallin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f2a10-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="f2a10-115">Kirjoita Nimi-kenttään toimittajan yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="f2a10-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="f2a10-116">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f2a10-116">Click OK.</span></span>
    * <span data-ttu-id="f2a10-117">Ostotilauksen nyt viedä loppuun ja käsitellä kuin minkä tahansa tilauksen.</span><span class="sxs-lookup"><span data-stu-id="f2a10-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="f2a10-118">Tämän suorittamisessa ei ole mitään erityisominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f2a10-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="f2a10-119">Laskulla tulee ilmi erääntyvä tapahtuma toimittajan tilille, joka on luotu tilausta luotaessa, jonka jälkeen maksu käsitellään.</span><span class="sxs-lookup"><span data-stu-id="f2a10-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

