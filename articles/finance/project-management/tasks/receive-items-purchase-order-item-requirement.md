---
title: Ostotilauksen nimikkeiden vastaanottaminen nimiketarpeen perusteella
description: Tässä aiheessa kerrotaan, miten ostotilauksen nimikkeet vastaanotetaan nimiketarpeesta.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f288a47f952a30d98a4a5b96409dc53f880d41d
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139051"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="d1882-103">Ostotilauksen nimikkeiden vastaanottaminen nimiketarpeen perusteella</span><span class="sxs-lookup"><span data-stu-id="d1882-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1882-104">Tässä aiheessa kerrotaan, miten ostotilauksen nimikkeet vastaanotetaan nimiketarpeesta.</span><span class="sxs-lookup"><span data-stu-id="d1882-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="d1882-105">Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="d1882-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="d1882-106">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="d1882-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d1882-107">Siirry siirtymisruudussa kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Projektit > Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="d1882-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="d1882-108">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="d1882-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="d1882-109">Valitse toimintoruudussa **Suunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="d1882-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="d1882-110">Valitse **Nimiketarpeet**.</span><span class="sxs-lookup"><span data-stu-id="d1882-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="d1882-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d1882-111">Select **New**.</span></span>
6. <span data-ttu-id="d1882-112">Syötä tai valitse arvo uuden rivin **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d1882-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="d1882-113">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="d1882-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="d1882-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d1882-114">Select **Save**.</span></span>
9. <span data-ttu-id="d1882-115">Valitse toimintoruudussa **Hallinta**.</span><span class="sxs-lookup"><span data-stu-id="d1882-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="d1882-116">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="d1882-116">Select **Functions**.</span></span>
11. <span data-ttu-id="d1882-117">Valitse **Luo ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="d1882-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="d1882-118">Valitse **Sisällytä kaikki** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="d1882-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="d1882-119">Anna tai valitse arvo **Toimittajatili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d1882-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="d1882-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1882-120">Select **OK**.</span></span>
15. <span data-ttu-id="d1882-121">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d1882-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="d1882-122">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="d1882-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="d1882-123">Valitse toimintoruudussa **Osto**.</span><span class="sxs-lookup"><span data-stu-id="d1882-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="d1882-124">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="d1882-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="d1882-125">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="d1882-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="d1882-126">Valitse **Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="d1882-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="d1882-127">Kirjoita arvo **Tuotteen vastaanotto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="d1882-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="d1882-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1882-128">Select **OK**.</span></span>

