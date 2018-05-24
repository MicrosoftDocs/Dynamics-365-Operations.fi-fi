---
title: Peruuta huoltotilaukset
description: "Voit peruuttaa huoltotilauksen tai huoltotilausrivin suoraan huoltotilauksesta tai peruuttaa useita huoltotilauksia suorittamalla kausittaisen työn."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8e5ad119c28bba18b75bb5ed7854e94a4e734d55
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="aa14e-103">Peruuta huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="aa14e-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="aa14e-104">Voit peruuttaa huoltotilauksen tai huoltotilausrivin suoraan huoltotilauksesta tai peruuttaa useita huoltotilauksia suorittamalla kausittaisen työn.</span><span class="sxs-lookup"><span data-stu-id="aa14e-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="aa14e-105">Huoltotilauksia ei voi peruuttaa, jos huoltotilauksen tila ei salli peruuttamista, jos huoltotilauksella on nimiketarpeita tai jos huoltotilaus on jo kirjattu.</span><span class="sxs-lookup"><span data-stu-id="aa14e-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="aa14e-106">Huoltotilauksen peruuttaminen Huoltotilaukset-lomakkeessa</span><span class="sxs-lookup"><span data-stu-id="aa14e-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="aa14e-107">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aa14e-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="aa14e-108">Valitse huoltotilaus ja valitse sitten **Peruuta tilaus** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="aa14e-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="aa14e-109">Huoltotilausrivin peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="aa14e-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="aa14e-110">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aa14e-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="aa14e-111">Kaksoisnapsauta huoltotilausta, joka sisältää peruutettavan rivin.</span><span class="sxs-lookup"><span data-stu-id="aa14e-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="aa14e-112">Valitse huoltotilausrivi, jonka haluat peruuttaa ja valitse sitten **Peruuta tilausrivi**, niin rivin tilaksi muuttuu **Peruutettu**.</span><span class="sxs-lookup"><span data-stu-id="aa14e-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="aa14e-113">Voit kumota huoltotilausrivin peruutuksen ja muuttaa tilan takaisin <STRONG>Luotu</STRONG>-tilaan valitsemalla <STRONG>Kumoa peruutus</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="aa14e-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="aa14e-114">Useiden huoltotilausten peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="aa14e-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="aa14e-115">Valitse **Huoltohallinta** \> **Kausittainen** \> **Huoltotilaukset** \> **Peuuta huoltotilaukset**</span><span class="sxs-lookup"><span data-stu-id="aa14e-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="aa14e-116">Napsauta **Valitse**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="aa14e-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="aa14e-117">Valitse peruutettavat huoltotilaukset **Kysely**-lomakkeen **Ehdot**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="aa14e-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="aa14e-118">Sulje **Kysely**-lomake valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa14e-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="aa14e-119">Valitse **Näytä infoloki** -valintaruutu, jos haluat luoda infolokin, jossa näkyvät peruutetut huoltotilaukset.</span><span class="sxs-lookup"><span data-stu-id="aa14e-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="aa14e-120">Valitse **Kumoa peruutus** -valintaruutu, jos haluat peruuttaa huoltotilauksen **Peruutettu**-tilan.</span><span class="sxs-lookup"><span data-stu-id="aa14e-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="aa14e-121">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa14e-121">Click **OK**.</span></span>

<span data-ttu-id="aa14e-122">Valitut huoltotilaukset on joko peruutettu tai niiden **Peruutettu**-tila on palautettu tilaksi **Käsittelyssä**.</span><span class="sxs-lookup"><span data-stu-id="aa14e-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="aa14e-123">Jos valitset <STRONG>Kumoa peruutus</STRONG> -valintaruudun, tilassa <STRONG>Peruutettu</STRONG> olevat huoltotilaukset palautetaan, eikä <STRONG>Käsittelyssä</STRONG>-tilassa olevia huoltotilauksia peruuteta.</span><span class="sxs-lookup"><span data-stu-id="aa14e-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



