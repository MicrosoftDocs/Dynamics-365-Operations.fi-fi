---
title: Huoltotilauksen nimiketarpeet
description: Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dc7c721af4b25e1586e546392518648110a3fb6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "327501"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="6f00b-103">Huoltotilauksen nimiketarpeet</span><span class="sxs-lookup"><span data-stu-id="6f00b-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6f00b-104">Voit luoda huoltotilauksen seurataksesi ja hallitaksesi palveluita, joita tarjoat asiakkaillesi.</span><span class="sxs-lookup"><span data-stu-id="6f00b-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="6f00b-105">Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="6f00b-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="6f00b-106">Nimiketarve voidaan kuluttaa suoraan varastosta tai se voi käynnistää nimikkeen tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="6f00b-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="6f00b-107">Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="6f00b-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="6f00b-108">Palvelutilausten nimikevaatimukset käsitellään projektin kautta.</span><span class="sxs-lookup"><span data-stu-id="6f00b-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="6f00b-109">Jos huoltotilaukselle luodaan nimiketarve, huoltotilauksen pitää olla liitetty projektiin.</span><span class="sxs-lookup"><span data-stu-id="6f00b-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="6f00b-110">Nimiketarvetta voi katsella heti, kun se on luotu huoltotilaukseen, yksittäisen huoltotilauksen **Projekti**-kohdassa tai **Myyntitilaus**-lomakkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="6f00b-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="6f00b-111">Nimiketarpeen tarkasteleminen huoltotilauksesta</span><span class="sxs-lookup"><span data-stu-id="6f00b-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="6f00b-112">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6f00b-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6f00b-113">Valitse **Lähetys**, ja valitse sitten **Nimiketarve** avataksesi **Nimiketarpeet**-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="6f00b-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="6f00b-114">Valitse **Projekti** -välilehti ja tarkasta **Huoltotilaus**-kentästä nimiketarpeen palvelutilaukset.</span><span class="sxs-lookup"><span data-stu-id="6f00b-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="6f00b-115">Nimiketarpeita sisältävien huoltotilausten poistaminen</span><span class="sxs-lookup"><span data-stu-id="6f00b-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="6f00b-116">Jos huoltotilaukselle luodaan nimiketarve, et voi poistaa huoltotilausta.</span><span class="sxs-lookup"><span data-stu-id="6f00b-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="6f00b-117">Sinun on poistettava nimiketarve ennen kuin voit poistaa huoltotilauksen.</span><span class="sxs-lookup"><span data-stu-id="6f00b-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="6f00b-118">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6f00b-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6f00b-119">Valitse **Lähetys**, ja valitse sitten **Nimiketarve** avataksesi **Nimiketarpeet**-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="6f00b-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="6f00b-120">Tässä lomakkeessa näkyvät kaikki huoltotilaukseen luodut nimiketarpeet.</span><span class="sxs-lookup"><span data-stu-id="6f00b-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="6f00b-121">Valitse poistettava nimiketarve ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="6f00b-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="6f00b-122">–TAI–</span><span class="sxs-lookup"><span data-stu-id="6f00b-122">–or–</span></span>

1.  <span data-ttu-id="6f00b-123">Valitse **Projektinhallinta ja kirjanpito** \> **Yleinen** \> **Projektit** \> **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="6f00b-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="6f00b-124">Avaa projekti, joka sisältää palvelutilauksen, jossa nimiketarve on luotu.</span><span class="sxs-lookup"><span data-stu-id="6f00b-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="6f00b-125">Valitse **Projektit**-lomakkeen oikeassa ruudussa **Nimiketarpeet**.</span><span class="sxs-lookup"><span data-stu-id="6f00b-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="6f00b-126">**Nimiketarpeet**-lomake avautuu, ja siinä näkyvät valittuun projektiin liittyvät nimiketarpeet.</span><span class="sxs-lookup"><span data-stu-id="6f00b-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="6f00b-127">Valitse poistettava nimiketarve ja valitse sitten **Poista**.</span><span class="sxs-lookup"><span data-stu-id="6f00b-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f00b-128">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="6f00b-128">See also</span></span>

<span data-ttu-id="6f00b-129">[Nimiketarpeet (lomake)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="6f00b-129">[Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span></span>

