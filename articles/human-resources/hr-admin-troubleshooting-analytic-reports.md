---
title: Analyysiraporttien vianmääritys
description: Tässä artikkelissa kerrotaan, mitä pitää tehdä, jos asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtiloissa.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112376"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="2b3c2-103">Analyysiraporttien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="2b3c2-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="2b3c2-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="2b3c2-104">**Issue**</span></span>

<span data-ttu-id="2b3c2-105">Asiakkaan tietoihin tekemät muutokset eivät näy asiakkaan työtilojen **Analytiikka**-välilehdillä.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="2b3c2-106">**Syy**</span><span class="sxs-lookup"><span data-stu-id="2b3c2-106">**Cause**</span></span>

<span data-ttu-id="2b3c2-107">Microsoft Power BI -raportit päivittyvät oletusarvoisesti neljän tunnin välein Ota mitta käyttöön -erätyön aikataulun mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="2b3c2-108">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="2b3c2-108">**Resolution**</span></span>

<span data-ttu-id="2b3c2-109">Ajoitus voi siis selittää tämän ongelman.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="2b3c2-110">Päivitä analytiikkatyötilat aloittamalla erätyö seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="2b3c2-111">Avaa **Erätyöt**-sivut valitsemalla **Järjestelmänvalvoja \> Linkit \> Erätyöt \> Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="2b3c2-112">Vaihtoehtoisesti voit käyttää hakutoimintoa ja hakusanaa **Erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="2b3c2-113">Etsi **Ota mitta käyttöön** -työ luettelosta.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="2b3c2-114">Valitse sivun yläosassa **Muokkaa** ja määritä ajoitetuksi aloituspäiväksi ja -ajaksi arvo, joka päivittää analytiikkaan lähellä kuluvaa ajankohtaa.</span><span class="sxs-lookup"><span data-stu-id="2b3c2-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Erätyöt](media/batch-jobs.png)
