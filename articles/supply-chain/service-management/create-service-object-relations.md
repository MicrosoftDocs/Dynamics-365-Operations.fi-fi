---
title: Huoltokohteen suhteiden luominen
description: Tässä ohjeaiheessa kuvataan, kuinka huoltosopimukselle ja huoltotilaukselle voidaan luoda huoltokohteiden suhteita.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab5de850ef40c26e447b96d8f42ccf83fb490818
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202764"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="6f9ff-103">Huoltokohteen suhteiden luominen</span><span class="sxs-lookup"><span data-stu-id="6f9ff-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6f9ff-104">Tässä ohjeaiheessa kuvataan, kuinka huoltosopimukselle ja huoltotilaukselle voidaan luoda huoltokohteiden suhteita.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="6f9ff-105">Kun luot huolto-objektin suhteen, liität huoltokohteen huoltosopimukseen tai huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="6f9ff-106">Asiakkaan pyytäessä huoltoa nimikkeelle, joka on huoltokohde, voit valita huoltokohteen huoltokohteen suhdeluettelosta.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="6f9ff-107">Luo huoltokohteen suhde huoltosopimukselle</span><span class="sxs-lookup"><span data-stu-id="6f9ff-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="6f9ff-108">Luo uusi huoltokohteen suhde huoltosopimukselle seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="6f9ff-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="6f9ff-109">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="6f9ff-110">Valitse **Huoltosopimukset**-luettelosta aiemmin luotu huoltosopimus tai valitse **Uusi** luodaksesi uuden huoltosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="6f9ff-111">Napsauta **Huoltosopimukset**-lomakkeen **toimintoruudussa** **Huoltosopimus**-välilehden **Suhteet**-ryhmässä **Huoltokohteet**</span><span class="sxs-lookup"><span data-stu-id="6f9ff-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="6f9ff-112">Valitse **Huoltokohteet**-lomakkeesta **Uusi** ja valitse sitten huoltokohde tälle palvelusopimukselle.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="6f9ff-113">Voit määrittää mallituoterakenteen (BOM) huoltosopimukseen napsauttamalla **Toiminnot** ja valitsemalla sitten **Liitä mallituoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="6f9ff-114">Valitse malli **Valitse mallituoterakenne**-lomakkeen **Mallituoterakenne**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="6f9ff-115">Luo huoltokohteen suhde huoltotilaukselle</span><span class="sxs-lookup"><span data-stu-id="6f9ff-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="6f9ff-116">Luo uusi huoltokohteen suhde huoltotilaukselle seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="6f9ff-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="6f9ff-117">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="6f9ff-118">**Huoltotilaukset**-luettelosta valitse nykyinen huoltotilaus tai luo uusi huoltotilaus.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="6f9ff-119">Napsauta **Huoltotilaukset**-lomakkeen **toimintoruudussa** **Huoltotilaus**-välilehden **Suhteet**-ryhmässä **Huoltokohteet**</span><span class="sxs-lookup"><span data-stu-id="6f9ff-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="6f9ff-120">Valitse **Huoltokohteet**-lomakkeesta **Uusi** ja valitse sitten huoltokohde tälle huoltotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="6f9ff-121">Voit määrittää mallituoterakenteen (BOM) huoltosopimukseen napsauttamalla **Toiminnot** ja valitsemalla sitten **Liitä mallituoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="6f9ff-122">Valitse malli **Valitse mallituoterakenne**-lomakkeen **Mallituoterakenne**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="6f9ff-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="6f9ff-123">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="6f9ff-123">See also</span></span>

[<span data-ttu-id="6f9ff-124">Huoltokohteiden yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6f9ff-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="6f9ff-125">Huoltokohteen suhteet</span><span class="sxs-lookup"><span data-stu-id="6f9ff-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="6f9ff-126">Mallituoterakenteet</span><span class="sxs-lookup"><span data-stu-id="6f9ff-126">Template BOMs</span></span>](template-boms.md)

  


