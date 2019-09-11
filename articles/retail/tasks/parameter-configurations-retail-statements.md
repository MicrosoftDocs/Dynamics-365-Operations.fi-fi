---
title: Vähittäismyyntilaskelmiin vaikuttavien vähittäismyynnin parametrien määrittäminen
description: Tässä aiheessa esitellään vähittäismyynnin parametrit konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.
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
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867268"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="74dd8-103">Vähittäismyyntilaskelmiin vaikuttavien vähittäismyynnin parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="74dd8-103">Configure Retail parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="74dd8-104">Tässä aiheessa esitellään vähittäismyynnin parametrit konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="74dd8-104">This topic demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="74dd8-105">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="74dd8-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="74dd8-106">Siirry siirtymisruudussa kohtaan **Moduulit >Vähittäismyynti ja kauppa > Pääkonttorin asetukset > Parametrit > Vähittäismyyntiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="74dd8-106">In the navigation pane, go to **Modules > Retail and commerce > Headquarters setup  > Parameters > Retail parameters**.</span></span>
2. <span data-ttu-id="74dd8-107">Valitse **Kirjaus**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="74dd8-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="74dd8-108">Valitse **Kyllä**, jos haluat kirjata erityisesti kausialennussummat.</span><span class="sxs-lookup"><span data-stu-id="74dd8-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="74dd8-109">Valitse **Vakio**, kun haluat käyttää oletustilejä. Valitse **Kausittainen**, jos haluat määrittää kunkin kausialennuksen käyttämän tili.</span><span class="sxs-lookup"><span data-stu-id="74dd8-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="74dd8-110">Valitse **Yhteenveto**, jos varastorivit yhdistetään aina, kun se on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="74dd8-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="74dd8-111">Valitse **Kyllä**, jos laskut ja maksut selvitetään automaattisesti laskelman kirjausprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="74dd8-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="74dd8-112">Valitse **Kyllä**, jos kassakaappiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="74dd8-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="74dd8-113">Valitse **Kyllä**, jos pankkiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="74dd8-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="74dd8-114">Valitse **Kyllä**, jos laskelman kirjauksen yhdistäminen otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="74dd8-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="74dd8-115">Valitse **Kyllä**, kun tilaukset luodaan ja käsitellään rinnakkain, kun laskelmat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="74dd8-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="74dd8-116">Syötä kussakin erätyötehtävässä käsiteltävien tilausten enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="74dd8-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="74dd8-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="74dd8-117">Select **Save**.</span></span>

