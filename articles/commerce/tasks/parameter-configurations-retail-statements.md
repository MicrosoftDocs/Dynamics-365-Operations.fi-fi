---
title: Vähittäismyyntilaskelmiin vaikuttavien parametrien määrittäminen
description: Tässä aiheessa esitellään Commercen parametrit konfiguraatiot, jotka vaikuttavat laskelmien luomiseen ja kirjaamiseen.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022377"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="8d688-103">Vähittäismyyntilaskelmiin vaikuttavien parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8d688-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8d688-104">Tässä aiheessa esitellään Commercen parametrit konfiguraatiot, jotka vaikuttavat laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="8d688-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="8d688-105">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="8d688-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="8d688-106">Siirry siirtymisruudussa kohtaan **Moduulit >Retail ja Commerce > Pääkonttorin asetukset > Parametrit > Commercen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8d688-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="8d688-107">Valitse **Kirjaus**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8d688-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="8d688-108">Valitse **Kyllä**, jos haluat kirjata erityisesti kausialennussummat.</span><span class="sxs-lookup"><span data-stu-id="8d688-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="8d688-109">Valitse **Vakio**, kun haluat käyttää oletustilejä. Valitse **Kausittainen**, jos haluat määrittää kunkin kausialennuksen käyttämän tili.</span><span class="sxs-lookup"><span data-stu-id="8d688-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="8d688-110">Valitse **Yhteenveto**, jos varastorivit yhdistetään aina, kun se on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="8d688-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="8d688-111">Valitse **Kyllä**, jos laskut ja maksut selvitetään automaattisesti laskelman kirjausprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="8d688-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="8d688-112">Valitse **Kyllä**, jos kassakaappiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="8d688-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="8d688-113">Valitse **Kyllä**, jos pankkiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="8d688-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="8d688-114">Valitse **Kyllä**, jos laskelman kirjauksen yhdistäminen otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8d688-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="8d688-115">Valitse **Kyllä**, kun tilaukset luodaan ja käsitellään rinnakkain, kun laskelmat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="8d688-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="8d688-116">Syötä kussakin erätyötehtävässä käsiteltävien tilausten enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="8d688-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="8d688-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8d688-117">Select **Save**.</span></span>

