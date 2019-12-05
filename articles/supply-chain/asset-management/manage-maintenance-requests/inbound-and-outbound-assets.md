---
title: Saapuvat ja lähtevät resurssit
description: Tässä ohjeaiheessa kerrotaan, miten saapuvat ja lähtevät resurssit rekisteröidään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53100a897dc71758b8920672fea1e684817cb4b7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812280"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="38f91-103">Saapuvat ja lähtevät resurssit</span><span class="sxs-lookup"><span data-stu-id="38f91-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="38f91-104">Jos yrityksesi tekee korjauksia tai kunnossapitotyötä muista sijainneista tai asiakkaista saatuihin resursseihin, resurssien hallinta voi seurata sekä saapuvia resursseja, jotka ovat matkalla yritykseen, että lähteviä resursseja, jotka palautetaan.</span><span class="sxs-lookup"><span data-stu-id="38f91-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="38f91-105">Jos haluat käyttää saapuvia ja lähteviä elinkaaritiloja hallitsemaan resursseja, jotka tulevat sisään ja palautetaan, sinun täytyy määrittää huoltopyynnön elinkaaritilat ja elinkaariallit tukemaan näitä toimintoja.</span><span class="sxs-lookup"><span data-stu-id="38f91-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="38f91-106">Lisätietoja on kohdassa [Ylläpitopyynnöt](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="38f91-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="38f91-107">Resurssien hallinnan asetukset määrittävät, voiko saapuvia ja lähteviä resursseja käsitellä.</span><span class="sxs-lookup"><span data-stu-id="38f91-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="38f91-108">Rekisteröi resurssit saapuviksi</span><span class="sxs-lookup"><span data-stu-id="38f91-108">Register assets as inbound</span></span>

1. <span data-ttu-id="38f91-109">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="38f91-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="38f91-110">Valitse ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="38f91-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="38f91-111">Valitse **Päivitä ylläpitopyynnön tila**.</span><span class="sxs-lookup"><span data-stu-id="38f91-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="38f91-112">Valitse **Saapuva** (tai muu elinkaaren tila, jonka olet luonut saapuville resursseille) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38f91-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Rekisteröi resurssit saapuviksi](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="38f91-114">Rekisteröi saapuvat resurssit vastaanotetuiksi</span><span class="sxs-lookup"><span data-stu-id="38f91-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="38f91-115">Valitse **Resurssien halllinta** \> **Yhteiset** \> **Saapuva/lähtevä** \> **Saapuvat resurssit**.</span><span class="sxs-lookup"><span data-stu-id="38f91-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="38f91-116">Valitse resurssi tai ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="38f91-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="38f91-117">Valitse **Vastaanota resurssit**.</span><span class="sxs-lookup"><span data-stu-id="38f91-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="38f91-118">Määritä päivämäärä ja kellonaika **Vastaanotettu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="38f91-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="38f91-119">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38f91-119">Then select **OK**.</span></span> <span data-ttu-id="38f91-120">Tietue poistetaan **Saapuvat resurssit** -luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="38f91-120">The record is removed from the **Inbound assets** list page.</span></span>

![Rekisteröi saapuvat resurssit vastaanotetuiksi](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="38f91-122">Rekisteröi resurssit lähteviksi</span><span class="sxs-lookup"><span data-stu-id="38f91-122">Register assets as outbound</span></span>

<span data-ttu-id="38f91-123">Kun huolto- tai korjaustyö on suoritettu, voit rekisteröidä resurssin palautetuksi.</span><span class="sxs-lookup"><span data-stu-id="38f91-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="38f91-124">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="38f91-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="38f91-125">Valitse ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="38f91-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="38f91-126">Valitse **Päivitä ylläpitopyynnön tila**.</span><span class="sxs-lookup"><span data-stu-id="38f91-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="38f91-127">Valitse **Lähtevä** (tai muu elinkaaren tila, jonka olet luonut lähteville resursseille) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38f91-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="38f91-128">Rekisteröi lähtevät resurssit toimitetuiksi</span><span class="sxs-lookup"><span data-stu-id="38f91-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="38f91-129">Valitse **Resurssien halllinta** \> **Yhteiset** \> **Saapuva/lähtevä** \> **Lähtevät resurssit**.</span><span class="sxs-lookup"><span data-stu-id="38f91-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="38f91-130">Valitse resurssi tai ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="38f91-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="38f91-131">Valitse **Toimita resurssit**.</span><span class="sxs-lookup"><span data-stu-id="38f91-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="38f91-132">Määritä päivämäärä ja kellonaika **Toimitettu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="38f91-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="38f91-133">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="38f91-133">Then select **OK**.</span></span> <span data-ttu-id="38f91-134">Tietue poistetaan **Lähtevät resurssit** -luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="38f91-134">The record is removed from the **Outbound assets** list page.</span></span>
