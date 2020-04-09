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
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140829"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="9665c-103">Vähittäismyyntilaskelmiin vaikuttavien parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9665c-103">Configure parameters that affect retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9665c-104">Tässä aiheessa esitellään Commercen parametrit konfiguraatiot, jotka vaikuttavat laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="9665c-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="9665c-105">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="9665c-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="9665c-106">Siirry siirtymisruudussa kohtaan **Moduulit >Retail ja Commerce > Pääkonttorin asetukset > Parametrit > Commercen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="9665c-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="9665c-107">Valitse **Kirjaus**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="9665c-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="9665c-108">Valitse **Kyllä**, jos haluat kirjata erityisesti kausialennussummat.</span><span class="sxs-lookup"><span data-stu-id="9665c-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="9665c-109">Valitse **Vakio**, kun haluat käyttää oletustilejä. Valitse **Kausittainen**, jos haluat määrittää kunkin kausialennuksen käyttämän tili.</span><span class="sxs-lookup"><span data-stu-id="9665c-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="9665c-110">Valitse **Yhteenveto**, jos varastorivit yhdistetään aina, kun se on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="9665c-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="9665c-111">Valitse **Kyllä**, jos laskut ja maksut selvitetään automaattisesti laskelman kirjausprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="9665c-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="9665c-112">Valitse **Kyllä**, jos kassakaappiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="9665c-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="9665c-113">Valitse **Kyllä**, jos pankkiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="9665c-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="9665c-114">Valitse **Kyllä**, jos laskelman kirjauksen yhdistäminen otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="9665c-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="9665c-115">Valitse **Kyllä**, kun tilaukset luodaan ja käsitellään rinnakkain, kun laskelmat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="9665c-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="9665c-116">Syötä kussakin erätyötehtävässä käsiteltävien tilausten enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="9665c-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="9665c-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9665c-117">Select **Save**.</span></span>

