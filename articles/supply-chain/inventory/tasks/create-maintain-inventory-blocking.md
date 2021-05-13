---
title: Luo ja ylläpidä varastoesto
description: Tässä aiheessa kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muilta lähteviltä asiakirjoilta varastoeston avulla.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956155"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="9af16-103">Luo ja ylläpidä varastoesto</span><span class="sxs-lookup"><span data-stu-id="9af16-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9af16-104">Tässä aiheessa kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muilta lähteviltä asiakirjoilta varastoeston avulla.</span><span class="sxs-lookup"><span data-stu-id="9af16-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="9af16-105">Aloita tämän aiheen menettelyt vasta, kun käytettävissä on fyysistä käytettävissä olevaa varastoa omaava nimike.</span><span class="sxs-lookup"><span data-stu-id="9af16-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="9af16-106">Varastoesto</span><span class="sxs-lookup"><span data-stu-id="9af16-106">Block inventory</span></span>

<span data-ttu-id="9af16-107">Noudattamalla näitä ohjeita voit luoda varaston estotietueen varaston eston mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="9af16-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="9af16-108">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Varastoesto**.</span><span class="sxs-lookup"><span data-stu-id="9af16-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="9af16-109">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9af16-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9af16-110">Uuden estotietueen otsikossa määritä **Nimiketunnus**-kenttä estettävään nimikkeeseen ja kirjoita kuvaus.</span><span class="sxs-lookup"><span data-stu-id="9af16-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="9af16-111">Kirjoita **Yleiset**-pikavälilehden **Määrä**-kenttään estettävien nimikkeiden määrä.</span><span class="sxs-lookup"><span data-stu-id="9af16-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="9af16-112">Määritä **Varastodimensiot**-pikavälilehdessä paikka ja varasto, jossa estettävät nimikkeet sijaitsevat tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="9af16-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="9af16-113">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9af16-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="9af16-114">Varastoeston ehtojen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="9af16-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="9af16-115">Päivitä varaston estotietue noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="9af16-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="9af16-116">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Varastoesto**.</span><span class="sxs-lookup"><span data-stu-id="9af16-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="9af16-117">Valitse luetteloruudusta asianmukainen estotietue.</span><span class="sxs-lookup"><span data-stu-id="9af16-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="9af16-118">Muokkaa tietuetta tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="9af16-118">Edit the record as required.</span></span> <span data-ttu-id="9af16-119">Esimerkiksi ehkä haluat muuttaa **Odotettu päivämäärä** -kentän arvoa ja määrittää, milloin estetyn varaston odotetaan olevan varattavissa.</span><span class="sxs-lookup"><span data-stu-id="9af16-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="9af16-120">Jos **Oletetut vastaanotot** -asetus on valittuna, oletetussa tapahtumassa näkyy päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="9af16-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="9af16-121">(**Oletetut vastaanotot** -asetus on oletusarvon mukaan valittuna, kun estotietue luodaan manuaalisesti.)</span><span class="sxs-lookup"><span data-stu-id="9af16-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="9af16-122">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9af16-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="9af16-123">Poista varaston esto</span><span class="sxs-lookup"><span data-stu-id="9af16-123">Unblock inventory</span></span>

<span data-ttu-id="9af16-124">Noudattamalla näitä ohjeita voit poistaa varaston estotietueen varaston eston poiston mahdollistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="9af16-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="9af16-125">Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Varastoesto**.</span><span class="sxs-lookup"><span data-stu-id="9af16-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="9af16-126">Valitse luetteloruudusta asianmukainen estotietue.</span><span class="sxs-lookup"><span data-stu-id="9af16-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="9af16-127">Valitse toimintoruudussa **Poista**.</span><span class="sxs-lookup"><span data-stu-id="9af16-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="9af16-128">Järjestelmä pyytää vahvistamaan toiminnon.</span><span class="sxs-lookup"><span data-stu-id="9af16-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="9af16-129">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="9af16-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="9af16-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9af16-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
