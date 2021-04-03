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
ms.openlocfilehash: 15247587f04813121473f24d4c3c849ec1ba7bb8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259527"
---
# <a name="view-the-start-time-and-duration-of-a-service-order"></a><span data-ttu-id="25bfd-103">Huoltotilauksen alkamisajan ja keston tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="25bfd-103">View the start time and duration of a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="25bfd-104">Voit tarkistaa, milloin huoltotilauksen työt aloitettiin ja milloin huoltotilaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="25bfd-104">You can view when the work on the service order was started and when the service order is going to be completed.</span></span>

<span data-ttu-id="25bfd-105">Voit myös tarkistaa, milloin huoltotilauksen ajanseuranta aloitettiin ja lopetettiin.</span><span class="sxs-lookup"><span data-stu-id="25bfd-105">You can also view when the time recording for a service order was started and stopped.</span></span> <span data-ttu-id="25bfd-106">Kun huoltotilaus pysäytetään, huoltotilauksen valmistumisajankohtaa lykätään.</span><span class="sxs-lookup"><span data-stu-id="25bfd-106">When a service order is stopped, the time at which the service order must be completed is postponed.</span></span>

## <a name="view-the-start-time-for-a-service-order"></a><span data-ttu-id="25bfd-107">Huoltotilauksen alkamisajan näyttäminen</span><span class="sxs-lookup"><span data-stu-id="25bfd-107">View the start time for a service order</span></span>

1.  <span data-ttu-id="25bfd-108">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="25bfd-108">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="25bfd-109">Valitse tilaus ja kaksoisnapsauta sitä tietolomakkeen avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="25bfd-109">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="25bfd-110">Tarkasta huoltotilauksen työn alkamisaika **Yleiset**-välilehden **Alkamisaika**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="25bfd-110">On the **General** tab, view the time that the work was started for a service order in the **Start time** field.</span></span>

## <a name="view-the-time-remaining-to-complete-a-service-order"></a><span data-ttu-id="25bfd-111">Huoltotilauksen valmistumisen keston näyttäminen</span><span class="sxs-lookup"><span data-stu-id="25bfd-111">View the time remaining to complete a service order</span></span>

1.  <span data-ttu-id="25bfd-112">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="25bfd-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="25bfd-113">Valitse tilaus ja kaksoisnapsauta sitä tietolomakkeen avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="25bfd-113">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="25bfd-114">Tarkista huoltotilauksen valmistumista edeltävä aika **Yleiset**-välilehden **Viimeinen valmistumisaika**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="25bfd-114">On the **General** tab, view the time remaining to complete a service order in the **Latest completion time** field.</span></span>

## <a name="view-the-start-time-and-stop-time-recording-entries-for-a-service-order"></a><span data-ttu-id="25bfd-115">Huoltotilauksen ajanseurannan alkamis- ja päättymisaikojen näyttäminen</span><span class="sxs-lookup"><span data-stu-id="25bfd-115">View the start time and stop time recording entries for a service order</span></span>

1.  <span data-ttu-id="25bfd-116">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="25bfd-116">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="25bfd-117">Valitse tilaus ja kaksoisnapsauta sitä tietolomakkeen avaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="25bfd-117">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="25bfd-118">Napsauta **Toimintoruudun** **Resursointi**-välilehteä \> **Ajanseuranta** avataksesi **SLA-ajanseuranta**-lomakkeen ja tarkastellaksesi huoltotilauksen ajanseurannan merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="25bfd-118">On the **Action Pane**, click the **Dispatch** tab \> **Time recording** to open the **SLA time recording** form and view the time recording entries for the service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="25bfd-119">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="25bfd-119">See also</span></span>

<span data-ttu-id="25bfd-120">[Palvelutilaukset (lomake)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="25bfd-120">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]