---
title: "Lisää osoite huoltotilaukseen"
description: "Tässä ohjeaiheessa kuvataan asiakkaan osoitteen lisääminen huoltotilaukseen."
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="7d158-103">Lisää osoite huoltotilaukseen</span><span class="sxs-lookup"><span data-stu-id="7d158-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7d158-104">Tässä ohjeaiheessa kuvataan asiakkaan osoitteen lisääminen huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="7d158-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="7d158-105">Kun luot huoltotilauksen, osoitetiedot siirretään siitä projektista, johon huoltotilaus liittyy.</span><span class="sxs-lookup"><span data-stu-id="7d158-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="7d158-106">Voit kuitenkin valita vaihtoehtoisen sijainnin osoitteista, jotka on jo määritetty Microsoft Dynamics AX:ssä asiakkaille, toimittajille, sivustoille, varastoille, huoltotilauksille ja projekteille.</span><span class="sxs-lookup"><span data-stu-id="7d158-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="7d158-107">Voit myös luoda uuden osoitteen.</span><span class="sxs-lookup"><span data-stu-id="7d158-107">You can also create a new address.</span></span> <span data-ttu-id="7d158-108">Oletusarvon mukaan uusi osoite siirretään projektiin.</span><span class="sxs-lookup"><span data-stu-id="7d158-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="7d158-109">Voit määrittää, että uutta osoitetta käytetään vain tässä palveluesiintymässä.</span><span class="sxs-lookup"><span data-stu-id="7d158-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="7d158-110">Jos teet niin, uutta osoitetta ei siirretä projektiin.</span><span class="sxs-lookup"><span data-stu-id="7d158-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="7d158-111">Luo asiakkaan osoite palvelutilaukselle</span><span class="sxs-lookup"><span data-stu-id="7d158-111">Create a customer address for a service order</span></span>

<span data-ttu-id="7d158-112">Voit lisätä osoitteen huoltotilaukseen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7d158-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="7d158-113">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="7d158-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="7d158-114">Avaa huoltotilaus, jolle haluat luoda osoitteen.</span><span class="sxs-lookup"><span data-stu-id="7d158-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="7d158-115">Napsauta **Toimintoruudussa** **Muokkaa** ja napsauta sitten **Otsikkonäkymä**.</span><span class="sxs-lookup"><span data-stu-id="7d158-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="7d158-116">Valitse **Osoite**-pikavälilehdessä **Lisää osoite**.</span><span class="sxs-lookup"><span data-stu-id="7d158-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="7d158-117">Valitse **Uusi osoite** -lomakkeessa yksilöivä nimi osoitteelle ja täytä muut kentät.</span><span class="sxs-lookup"><span data-stu-id="7d158-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="7d158-118">Jos annat saman nimen olemassa olevana osoitteena, tiedot, jotka kirjoitat muihin kenttiin, korvaavat aiemmat osoitetiedot.</span><span class="sxs-lookup"><span data-stu-id="7d158-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="7d158-119">Valitse **OK** kopioidaksesi huoltotilaukseen uuden osoitteen.</span><span class="sxs-lookup"><span data-stu-id="7d158-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="7d158-120">Vaihtoehtoisen osoitteen määrittäminen huoltotilaukseen</span><span class="sxs-lookup"><span data-stu-id="7d158-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="7d158-121">Voit lisätä vaihtoehtoisen osoitteen huoltotilaukseen seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7d158-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="7d158-122">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="7d158-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="7d158-123">Avaa huoltotilaus, jolle haluat kirjoittaa vaihtoehtoisen osoitteen.</span><span class="sxs-lookup"><span data-stu-id="7d158-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="7d158-124">Napsauta **Toimintoruudussa** **Muokkaa** ja napsauta sitten **Otsikkonäkymä**.</span><span class="sxs-lookup"><span data-stu-id="7d158-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="7d158-125">Valitse **Osoite**-pikavälilehdessä **Muu osoite**.</span><span class="sxs-lookup"><span data-stu-id="7d158-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="7d158-126">Valitse **Osoitteen valinta** -lomakkeessa **Tietuetyyppi** -kentässä**Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="7d158-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="7d158-127">Valitse osoite ja napsauta sitten **OK** kopioidaksesi sen huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="7d158-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  



