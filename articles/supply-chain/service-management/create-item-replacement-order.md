---
title: Nimikkeen korvaavan tilauksen luominen
description: Nimikkeen korvaavat tilaukset luodaan yleensä tuotteen palautuksen ja tarkistuksen jälkeen.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0006ea9ec64cd95a709ec91509cb3a9828df160
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996648"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="1ed34-103">Nimikkeen korvaavan tilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="1ed34-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1ed34-104">Nimikkeen korvaavat tilaukset luodaan yleensä tuotteen palautuksen ja tarkistuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="1ed34-105">Jos nimike kuitenkin on korvattava ennen sen palauttamista tai alkuperäistä nimikettä ei palauteta, voit luoda nimikkeen korvaavan tilauksen heti palautustilauksen luonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="1ed34-106">Korvaavan tilauksen luominen palautetun nimikkeen vastaanoton jälkeen</span><span class="sxs-lookup"><span data-stu-id="1ed34-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="1ed34-107">Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**.</span><span class="sxs-lookup"><span data-stu-id="1ed34-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="1ed34-108">Luo uusi palautustilaus tai valitse palautettu tilaus luettelosta avataksesi **Palautustilaus - palautusnumero: %1, %2** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="1ed34-109">Valitse **Palautusrivi**, ja valitse sitten **Korvaava nimike**.</span><span class="sxs-lookup"><span data-stu-id="1ed34-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="1ed34-110">Valitse nimike, jolla palautettu nimike korvataan.</span><span class="sxs-lookup"><span data-stu-id="1ed34-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="1ed34-111">Kirjoita nimikkeen tiedot ja valitse sitten **Käytä**.</span><span class="sxs-lookup"><span data-stu-id="1ed34-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="1ed34-112">Voit luoda palautustilauksen pakkausluettelon napsauttamalla **Pakkausluettelo**.</span><span class="sxs-lookup"><span data-stu-id="1ed34-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="1ed34-113">Valitsemallesi korvaavalle nimikkeelle luodaan myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="1ed34-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="1ed34-114">Kun myyntitilaus on luotu korvaavalle nimikkeelle, järjestelmän myyntisopimuksista haetaan automaattisesti sopivaa myyntisopimusta ja jos tämä löytyy, sitä sovelletaan myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="1ed34-115">Korvaavan tilauksen luonti ennen palautetun nimikkeen vastaanottamista</span><span class="sxs-lookup"><span data-stu-id="1ed34-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="1ed34-116">Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**.</span><span class="sxs-lookup"><span data-stu-id="1ed34-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="1ed34-117">Luo uusi palautustilaus tai valitse palautustilaus luettelosta avataksesi **Palautustilaus - palautusnumero: %1, %2** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="1ed34-118">Valitse **Etsi myyntitilaus** , jos haluat merkitä palautetun nimikkeen myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="1ed34-119">Täytä **Etsi myyntitilaus** -lomake ja valitse **OK** sulkeaksesi lomakkeen ja palataksesi takaisin **Palautustilaus - palautusnumero: %1, %2** -lomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="1ed34-120">Palautetun nimikkeen myyntitilausrivi kopioidaan palautustilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="1ed34-121">Napsauta **Korvaava tilaus** avataksesi **Luo myyntitilaus** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="1ed34-122">Valitse **Kopioi palautustilauksen rivit** -valintaruutu siirtääksesi **Palautustilaus - palautusnumero: %1, %2** -lomakkeessa valitsemasi palautustilauksen tiedot tähän myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="1ed34-123">Kirjoita tai muokkaa tiedot tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1ed34-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="1ed34-124">Jos tunnistit myyntitilauksen vaiheessa 3 ja jos palautetun nimikkeen myyntitilausrivi on yhdistetty myyntisopimukseen, nimikkeen korvaavan tilauksen soveltuvan myyntisopimuksen tunniste näkyy automaattisesti **Myyntisopimuksen tunnus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1ed34-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="1ed34-125">Napsauta **OK** sulkeaksesi **Luo myyntitilaus** -lomakkeen ja avataksesi **Myyntitilaus**-lomakkeen, jossa voit jatkaa uuden myyntitilauksen tietojen kirjoittamista.</span><span class="sxs-lookup"><span data-stu-id="1ed34-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="1ed34-126">Kaikki sovellettavat palautustilauksen rivit kopioidaan uuteen myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1ed34-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="1ed34-127">Jos myyntisopimuksen tunniste näytetään **Myyntitilauksen tunnus** -kentässä, tällöin myyntisopimus on yhdistetty myyntitilauksen otsikkoon nimikkeen korvaavalle tilaukselle.</span><span class="sxs-lookup"><span data-stu-id="1ed34-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="1ed34-128">Jos myyntisopimuksessa on soveltuva sitoumus, jota ei ole vielä täytetty, ja myyntitilaus on luotu ennen myyntisopimuksen vanhenemista, myyntisopimusrivin ja myyntitilausrivin välille luodaan yhteys.</span><span class="sxs-lookup"><span data-stu-id="1ed34-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="1ed34-129">Siksi myyntisopimuksen tiedot, kuten hinta, kopioidaan uudelle myyntitilausriville.</span><span class="sxs-lookup"><span data-stu-id="1ed34-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


