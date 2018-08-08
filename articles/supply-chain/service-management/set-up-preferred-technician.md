---
title: "Ensisijaisen teknikon määrittäminen"
description: "Voit valita minkä tahansa työntekijän ensisijaiseksi teknikoksi huoltosopimukseen tai huoltotilaukseen."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable, SMADispatchBoard
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
ms.openlocfilehash: e904db7312563b8b7dc584c9fa4d40b947db4db5
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---


# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="3ce74-103">Ensisijaisen teknikon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3ce74-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3ce74-104">Voit valita minkä tahansa työntekijän ensisijaiseksi teknikoksi huoltosopimukseen tai huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="3ce74-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="3ce74-105">On kuitenkin hyvä ajatus lisätä työntekijä asianmukaiseen resursointiryhmään siten, että työntekijä on mukana **Resursointitaulussa**.</span><span class="sxs-lookup"><span data-stu-id="3ce74-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="3ce74-106">Työntekijän määrittäminen resursointiryhmään</span><span class="sxs-lookup"><span data-stu-id="3ce74-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="3ce74-107">Valitse **Henkilöstöhallinto** \> **Yleinen** \> **Työntekijät** \> **Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="3ce74-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="3ce74-108">Kaksoisnapsauta työntekijää avataksesi työntekijän tiedot -sivun.</span><span class="sxs-lookup"><span data-stu-id="3ce74-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="3ce74-109">Valitse **toimintoruudussa** **Asetukset** \>**Resursointiryhmä** avataksesi **Resursoi työntekijöitä** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="3ce74-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="3ce74-110">Valitse **Resursointiryhmä**-kentässä työntekijään liitettävä ryhmä.</span><span class="sxs-lookup"><span data-stu-id="3ce74-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="3ce74-111">Ensisijaisen teknikon määrittäminen huoltosopimukseen</span><span class="sxs-lookup"><span data-stu-id="3ce74-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="3ce74-112">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="3ce74-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="3ce74-113">Avaa tietolomake kaksoisnapsauttamalla huoltosopimusta.</span><span class="sxs-lookup"><span data-stu-id="3ce74-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="3ce74-114">Valitse **Yleinen**-välilehdellä **Ensisijainen teknikko** -kenttä ja valitse sitten sopivan resursointiryhmän jäsen huoltosopimuksen ensisijaiseksi teknikoksi.</span><span class="sxs-lookup"><span data-stu-id="3ce74-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="3ce74-115">Ensisijaisen teknikon määrittäminen huoltotilaukseen</span><span class="sxs-lookup"><span data-stu-id="3ce74-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="3ce74-116">Valitse **Huollon hallinta** \> **Kausittainen** \> **Resursointitaulu**.</span><span class="sxs-lookup"><span data-stu-id="3ce74-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="3ce74-117">Määritä <STRONG>Resursointitaulu</STRONG>-lomakkeessa tarkasteltavien resursointitehtävien päivämääräväli.</span><span class="sxs-lookup"><span data-stu-id="3ce74-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="3ce74-118">Voit myös määrittää, haluatko näyttää suljettuja tehtäviä ja haluatko rajoittaa resursointitehtävien käytön ryhmille, joihin kuulut tai joille on annettu valintaoikeudet.</span><span class="sxs-lookup"><span data-stu-id="3ce74-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="3ce74-119">Avaa <STRONG>Resursointitaulu</STRONG> valitsemalla <STRONG>OK</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3ce74-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="3ce74-120">Valitse muokattavan huoltotoiminnan rivi.</span><span class="sxs-lookup"><span data-stu-id="3ce74-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="3ce74-121">Valitse **Liittyvä**-välilehti ja määritä **Työntekijä**-luettelosta asianmukaisen resursointiryhmän jäsen huoltokäynnin ensisijaiseksi teknikoksi.</span><span class="sxs-lookup"><span data-stu-id="3ce74-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ce74-122">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3ce74-122">See also</span></span>

[<span data-ttu-id="3ce74-123">Huoltosopimukset</span><span class="sxs-lookup"><span data-stu-id="3ce74-123">Service agreements</span></span>](service-agreements.md)

[<span data-ttu-id="3ce74-124">Huoltotilausten luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="3ce74-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="3ce74-125">[Palvelusopimukset (lomake)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="3ce74-125">[Service agreements (form)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span></span>
  



