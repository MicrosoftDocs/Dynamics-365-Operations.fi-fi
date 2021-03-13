---
title: Huoltotilauksen alkamisajan ja keston tarkasteleminen
description: Voit tarkistaa, milloin huoltotilauksen työt aloitettiin ja milloin huoltotilaus on valmis.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7e3277a61bd776c665d598583165e0dbd856e8c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010369"
---
# <a name="view-the-start-time-and-duration-of-a-service-order"></a><span data-ttu-id="86e14-103">Huoltotilauksen alkamisajan ja keston tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="86e14-103">View the start time and duration of a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="86e14-104">Voit tarkistaa, milloin huoltotilauksen työt aloitettiin ja milloin huoltotilaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="86e14-104">You can view when the work on the service order was started and when the service order is going to be completed.</span></span>

<span data-ttu-id="86e14-105">Voit myös tarkistaa, milloin huoltotilauksen ajanseuranta aloitettiin ja lopetettiin.</span><span class="sxs-lookup"><span data-stu-id="86e14-105">You can also view when the time recording for a service order was started and stopped.</span></span> <span data-ttu-id="86e14-106">Kun huoltotilaus pysäytetään, huoltotilauksen valmistumisajankohtaa lykätään.</span><span class="sxs-lookup"><span data-stu-id="86e14-106">When a service order is stopped, the time at which the service order must be completed is postponed.</span></span>

## <a name="view-the-start-time-for-a-service-order"></a><span data-ttu-id="86e14-107">Huoltotilauksen alkamisajan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="86e14-107">View the start time for a service order</span></span>

1.  <span data-ttu-id="86e14-108">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="86e14-108">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="86e14-109">Valitse tilaus ja kaksoisnapsauta sitä tietolomakkeen avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="86e14-109">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="86e14-110">Tarkasta huoltotilauksen työn alkamisaika **Yleiset**-välilehden **Alkamisaika**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="86e14-110">On the **General** tab, view the time that the work was started for a service order in the **Start time** field.</span></span>

## <a name="view-the-time-remaining-to-complete-a-service-order"></a><span data-ttu-id="86e14-111">Huoltotilauksen valmistumisen keston näyttäminen</span><span class="sxs-lookup"><span data-stu-id="86e14-111">View the time remaining to complete a service order</span></span>

1.  <span data-ttu-id="86e14-112">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="86e14-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="86e14-113">Valitse tilaus ja kaksoisnapsauta sitä tietolomakkeen avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="86e14-113">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="86e14-114">Tarkista huoltotilauksen valmistumista edeltävä aika **Yleiset**-välilehden **Viimeinen valmistumisaika**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="86e14-114">On the **General** tab, view the time remaining to complete a service order in the **Latest completion time** field.</span></span>

## <a name="view-the-start-time-and-stop-time-recording-entries-for-a-service-order"></a><span data-ttu-id="86e14-115">Huoltotilauksen ajanseurannan alkamis- ja päättymisaikojen näyttäminen</span><span class="sxs-lookup"><span data-stu-id="86e14-115">View the start time and stop time recording entries for a service order</span></span>

1.  <span data-ttu-id="86e14-116">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="86e14-116">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="86e14-117">Valitse tilaus ja kaksoisnapsauta sitä tietolomakkeen avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="86e14-117">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="86e14-118">Napsauta **Toimintoruudun** **Resursointi**-välilehteä \> **Ajanseuranta** avataksesi **SLA-ajanseuranta**-lomakkeen ja tarkastellaksesi huoltotilauksen ajanseurannan merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="86e14-118">On the **Action Pane**, click the **Dispatch** tab \> **Time recording** to open the **SLA time recording** form and view the time recording entries for the service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="86e14-119">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="86e14-119">See also</span></span>

<span data-ttu-id="86e14-120">[Palvelutilaukset (lomake)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="86e14-120">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  


