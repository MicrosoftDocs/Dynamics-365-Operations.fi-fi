---
title: Analyysiraportit eivät päivity
description: Tässä ohjeaiheessa kerrotaan, mitä pitää tehdä, jos asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtiloissa.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304175"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="cc9ba-103">Analyysiraportit eivät päivity</span><span class="sxs-lookup"><span data-stu-id="cc9ba-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc9ba-104">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="cc9ba-104">**Issue**</span></span>

<span data-ttu-id="cc9ba-105">Asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtilojen **Analytiikka**-välilehdillä.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="cc9ba-106">**Syy**</span><span class="sxs-lookup"><span data-stu-id="cc9ba-106">**Cause**</span></span>

<span data-ttu-id="cc9ba-107">Microsoft Power BI -raportit päivittyvät oletusarvoisesti neljän tunnin välein Ota mitta käyttöön -erätyön aikataulun mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="cc9ba-108">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="cc9ba-108">**Resolution**</span></span>

<span data-ttu-id="cc9ba-109">Ajoitus voi siis selittää tämän ongelman.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="cc9ba-110">Päivitä analytiikkatyötilat aloittamalla erätyö seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="cc9ba-111">Avaa **Erätyöt**-sivut valitsemalla **Järjestelmänvalvoja \> Linkit \> Erätyöt \> Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="cc9ba-112">Vaihtoehtoisesti voit käyttää hakutoimintoa ja hakusanaa **Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="cc9ba-113">Etsi **Ota mitta käyttöön** -työ luettelosta.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="cc9ba-114">Valitse sivun yläosassa **Muokkaa** ja määritä ajoitetuksi aloituspäiväksi ja -ajaksi arvo, joka päivittää analytiikkaan lähellä kuluvaa ajankohtaa.</span><span class="sxs-lookup"><span data-stu-id="cc9ba-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Erätyöt](media/batch-jobs.png)
