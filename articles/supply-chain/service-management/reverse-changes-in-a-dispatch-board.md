---
title: Muutosten peruuttaminen resursointitaulussa
description: Tässä ohjeaiheessa kuvataan, kuinka resursointitaululle tehdyt tallentamattomat muutokset peruutetaan.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMADispatchBoard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc55c1ab0a9ad7af3b55e49079185062fd119cc7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546153"
---
# <a name="reverse-changes-in-a-dispatch-board"></a><span data-ttu-id="1896f-103">Muutosten peruuttaminen resursointitaulussa</span><span class="sxs-lookup"><span data-stu-id="1896f-103">Reverse changes in a dispatch board</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1896f-104">Tässä ohjeaiheessa kuvataan, kuinka resursointitaululle tehdyt tallentamattomat muutokset peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="1896f-104">This topic describes how to reverse unsaved modifications that you make in a dispatch board.</span></span> <span data-ttu-id="1896f-105">Esimerkiksi määrität työntekijän palvelutehtävään, tallennat tiedot ja päätät myöhemmin määrittää toisen työntekijän palvelutehtävään.</span><span class="sxs-lookup"><span data-stu-id="1896f-105">For example, you assign a worker to a service activity, save the information, and then later decide to assign a different worker to the service activity.</span></span> <span data-ttu-id="1896f-106">Muokkaat työntekijää resursointitaulussa ja havaitset ennen muutoksen tallentamista, että juuri määritetty työntekijä ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="1896f-106">You modify the worker in the dispatch board, and then, before saving the change, learn that the worker just assigned is not available.</span></span> <span data-ttu-id="1896f-107">Voit palauttaa tallentamattomat muutokset siten, että alkuperäinen työntekijä liitetään uudelleen huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1896f-107">You can reverse the unsaved modification so that the original worker is reassigned to the service order.</span></span>

<span data-ttu-id="1896f-108">Seuraavien vaiheiden avulla voit perua tallentamattomat muutokset resursointitaulussa:</span><span class="sxs-lookup"><span data-stu-id="1896f-108">Use the following steps to reverse unsaved changes in a dispatch board:</span></span>

1.  <span data-ttu-id="1896f-109">Valitse **Huollon hallinta** \> **Kausittainen** \> **Resursointitaulu**.</span><span class="sxs-lookup"><span data-stu-id="1896f-109">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>

2.  <span data-ttu-id="1896f-110">**Resursointitaulu**-lomakkeessa kirjoita tarpeelliset tiedot kenttiin ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1896f-110">In the **Dispatch board** form, enter relevant information in the fields, and then click **OK**.</span></span> 

3.  <span data-ttu-id="1896f-111">Voit palauttaa viimeisimmän tallentamattoman muutoksen napsauttamalla **Kumoa**.</span><span class="sxs-lookup"><span data-stu-id="1896f-111">To reverse the most recent change that is not saved, click **Undo**.</span></span>

4.  <span data-ttu-id="1896f-112">Jos haluat peruuttaa joukon tallentamattomia muutoksia, jatka **Kumoa**-painikkeen napsauttamista, kunnes haluamasi muutokset on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="1896f-112">To reverse a series of changes that are not saved, continue clicking **Undo** until each change that you want to discard is reversed.</span></span>

## <a name="see-also"></a><span data-ttu-id="1896f-113">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="1896f-113">See also</span></span>

[<span data-ttu-id="1896f-114">Resursointitaulu</span><span class="sxs-lookup"><span data-stu-id="1896f-114">Dispatch board</span></span>](dispatch-board.md)

[<span data-ttu-id="1896f-115">Huoltotehtävät</span><span class="sxs-lookup"><span data-stu-id="1896f-115">Service activities</span></span>](service-activities.md)

 


