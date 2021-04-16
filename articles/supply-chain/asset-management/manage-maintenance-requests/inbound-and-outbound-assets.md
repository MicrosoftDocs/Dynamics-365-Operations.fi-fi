---
title: Saapuvat ja lähtevät resurssit
description: Tässä ohjeaiheessa kerrotaan, miten saapuvat ja lähtevät resurssit rekisteröidään resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a2bac914330058400a7e4d7d355bd4a00a4522f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816793"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="63766-103">Saapuvat ja lähtevät resurssit</span><span class="sxs-lookup"><span data-stu-id="63766-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="63766-104">Jos yrityksesi tekee korjauksia tai kunnossapitotyötä muista sijainneista tai asiakkaista saatuihin resursseihin, resurssien hallinta voi seurata sekä saapuvia resursseja, jotka ovat matkalla yritykseen, että lähteviä resursseja, jotka palautetaan.</span><span class="sxs-lookup"><span data-stu-id="63766-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="63766-105">Jos haluat käyttää saapuvia ja lähteviä elinkaaritiloja hallitsemaan resursseja, jotka tulevat sisään ja palautetaan, sinun täytyy määrittää huoltopyynnön elinkaaritilat ja elinkaariallit tukemaan näitä toimintoja.</span><span class="sxs-lookup"><span data-stu-id="63766-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="63766-106">Lisätietoja on kohdassa [Ylläpitopyynnöt](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="63766-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="63766-107">Resurssien hallinnan asetukset määrittävät, voiko saapuvia ja lähteviä resursseja käsitellä.</span><span class="sxs-lookup"><span data-stu-id="63766-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="63766-108">Rekisteröi resurssit saapuviksi</span><span class="sxs-lookup"><span data-stu-id="63766-108">Register assets as inbound</span></span>

1. <span data-ttu-id="63766-109">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="63766-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="63766-110">Valitse ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="63766-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="63766-111">Valitse **Päivitä ylläpitopyynnön tila**.</span><span class="sxs-lookup"><span data-stu-id="63766-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="63766-112">Valitse **Saapuva** (tai muu elinkaaren tila, jonka olet luonut saapuville resursseille) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="63766-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Rekisteröi resurssit saapuviksi](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="63766-114">Rekisteröi saapuvat resurssit vastaanotetuiksi</span><span class="sxs-lookup"><span data-stu-id="63766-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="63766-115">Valitse **Resurssien halllinta** \> **Yhteiset** \> **Saapuva/lähtevä** \> **Saapuvat resurssit**.</span><span class="sxs-lookup"><span data-stu-id="63766-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="63766-116">Valitse resurssi tai ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="63766-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="63766-117">Valitse **Vastaanota resurssit**.</span><span class="sxs-lookup"><span data-stu-id="63766-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="63766-118">Määritä päivämäärä ja kellonaika **Vastaanotettu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63766-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="63766-119">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="63766-119">Then select **OK**.</span></span> <span data-ttu-id="63766-120">Tietue poistetaan **Saapuvat resurssit** -luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="63766-120">The record is removed from the **Inbound assets** list page.</span></span>

![Rekisteröi saapuvat resurssit vastaanotetuiksi](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="63766-122">Rekisteröi resurssit lähteviksi</span><span class="sxs-lookup"><span data-stu-id="63766-122">Register assets as outbound</span></span>

<span data-ttu-id="63766-123">Kun huolto- tai korjaustyö on suoritettu, voit rekisteröidä resurssin palautetuksi.</span><span class="sxs-lookup"><span data-stu-id="63766-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="63766-124">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="63766-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="63766-125">Valitse ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="63766-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="63766-126">Valitse **Päivitä ylläpitopyynnön tila**.</span><span class="sxs-lookup"><span data-stu-id="63766-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="63766-127">Valitse **Lähtevä** (tai muu elinkaaren tila, jonka olet luonut lähteville resursseille) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="63766-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="63766-128">Rekisteröi lähtevät resurssit toimitetuiksi</span><span class="sxs-lookup"><span data-stu-id="63766-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="63766-129">Valitse **Resurssien halllinta** \> **Yhteiset** \> **Saapuva/lähtevä** \> **Lähtevät resurssit**.</span><span class="sxs-lookup"><span data-stu-id="63766-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="63766-130">Valitse resurssi tai ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="63766-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="63766-131">Valitse **Toimita resurssit**.</span><span class="sxs-lookup"><span data-stu-id="63766-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="63766-132">Määritä päivämäärä ja kellonaika **Toimitettu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="63766-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="63766-133">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="63766-133">Then select **OK**.</span></span> <span data-ttu-id="63766-134">Tietue poistetaan **Lähtevät resurssit** -luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="63766-134">The record is removed from the **Outbound assets** list page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]