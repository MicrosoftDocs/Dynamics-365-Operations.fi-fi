--- 
title: "Vähittäismyynnin laskelmien parametrin konfiguraatiot"
description: "Tässä menettelyssä esitellään vähittäismyynnin parametrit konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 61540297a2ebbbc76657734140b8add009db67ca
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="d7bfb-103">Vähittäismyynnin laskelmien parametrin konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="d7bfb-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d7bfb-104">Tässä menettelyssä esitellään vähittäismyynnin parametrit konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="d7bfb-105">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d7bfb-106">Valitse Vähittäismyynti ja kauppa > Pääkonttorin asetukset > Parametrit > Vähittäismyyntiparametrit.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="d7bfb-107">Valitse Kirjaus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="d7bfb-108">Valitse Kyllä, jos haluat kirjata erityisesti kausialennussummat.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="d7bfb-109">Valitse Vakio, kun haluat käyttää oletustilejä. Valitse Kausittainen, jos haluat määrittää kunkin kausialennuksen käyttämän tili.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="d7bfb-110">Valitse Yhteenveto, jos varastorivit yhdistetään aina, kun se on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="d7bfb-111">Valitse Kyllä, jos laskut ja maksut selvitetään automaattisesti laskelman kirjausprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="d7bfb-112">Valitse Kyllä, jos kassakaappiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="d7bfb-113">Valitse Kyllä, jos pankkiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="d7bfb-114">Valitse Kyllä, jos laskelman kirjauksen yhdistäminen otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="d7bfb-115">Valitse Kyllä, kun tilaukset luodaan ja käsitellään rinnakkain, kun laskelmat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="d7bfb-116">Syötä kussakin erätyötehtävässä käsiteltävien tilausten enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="d7bfb-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-117">Click Save.</span></span>


