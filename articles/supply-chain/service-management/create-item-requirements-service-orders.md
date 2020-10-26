---
title: Nimiketarpeiden luominen huoltotilauksiin
description: Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18484b637723cef43cad288c08ddfe53cddf9e03
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978480"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="3dbbc-103">Nimiketarpeiden luominen huoltotilauksiin</span><span class="sxs-lookup"><span data-stu-id="3dbbc-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3dbbc-104">Voit luoda huoltotilauksen seurataksesi ja hallitaksesi palveluita, joita tarjoat asiakkaillesi.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="3dbbc-105">Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="3dbbc-106">Nimiketarve voidaan kuluttaa suoraan varastosta tai se voi käynnistää nimikkeen tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="3dbbc-107">Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="3dbbc-108">Palvelutilausten nimikevaatimukset käsitellään projektin kautta.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="3dbbc-109">Jos huoltotilaukselle luodaan nimiketarve, projektille pitää olla määritettynä huoltotilaus.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="3dbbc-110">Kun olet luonut huoltotilaukselle nimiketarpeen, voit tarkastella sitä valitun projektin **Projektit**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="3dbbc-111">Luo nimiketarve huoltotilaukselle</span><span class="sxs-lookup"><span data-stu-id="3dbbc-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="3dbbc-112">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="3dbbc-113">Valitse huoltotilaus, jolle haluat luoda nimiketarpeen.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="3dbbc-114">Napsauta **toimintoruudun** **Lähetys**-välilehdellä **Nimiketarve**.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="3dbbc-115">Kirjoita **Nimiketarve**-lomakkeeseen tarvittavat nimikkeen tiedot.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="3dbbc-116">Lisätietoja kentistä on kohdassa [Nimiketarpeet (lomake)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="3dbbc-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="3dbbc-117">Luo nimiketarve huoltosopimukselle</span><span class="sxs-lookup"><span data-stu-id="3dbbc-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="3dbbc-118">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="3dbbc-119">Valitse huoltosopimus, jolle haluat luoda nimiketarpeen.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="3dbbc-120">Luo uusi rivi napsauttamalla **Rivit**-pikavälilehdellä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="3dbbc-121">Valitse **Tapahtumalaji**-kentästä **Nimike**.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="3dbbc-122">Valitse **Nimikeasetukset**-kentässä **Nimiketarve**.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="3dbbc-123">Valitse **Nimikenumero**-kentästä nimike, joka on tarpeen huoltosopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="3dbbc-124">**Rivin tiedot** -pikavälilehdessä **Nimikedimensiot**-välilehdellä **Toimipaikka**-kentässä valitse nimikkeen varastotoimipaikkaa.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="3dbbc-125">Luodaksesi huoltotilauksen sopimusriviltä, mene **Rivit**-pikavälilehdelle, napsauta **Luo huoltotilauksia**, ja syötä sitten tarvittava tieto **Luo huoltotilauksia** -lomakkeella.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="3dbbc-126">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3dbbc-126">See also</span></span>

<span data-ttu-id="3dbbc-127">[Automaattisesti luodut huoltotilaukset](create-service-orders-automatically.md)</span><span class="sxs-lookup"><span data-stu-id="3dbbc-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


