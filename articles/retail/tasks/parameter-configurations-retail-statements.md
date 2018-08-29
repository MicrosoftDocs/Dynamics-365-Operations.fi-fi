--- 
title: "Määritä Retail-parametrit, jotka vaikuttavat vähittäismyyntilaskelmiin"
description: "Tässä menettelyssä esitellään vähittäismyynnin parametrit konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ff12587d8332801131d5b0cac84e0db38f8f6142
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="eddfd-103">Määritä Retail-parametrit, jotka vaikuttavat vähittäismyyntilaskelmiin</span><span class="sxs-lookup"><span data-stu-id="eddfd-103">Configure Retail parameters that affect retail statements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="eddfd-104">Tässä menettelyssä esitellään vähittäismyynnin parametrit konfiguraatiot, jotka vaikuttavat vähittäismyynnin laskelmien luomiseen ja kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="eddfd-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="eddfd-105">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="eddfd-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="eddfd-106">Valitse Vähittäismyynti ja kauppa > Pääkonttorin asetukset > Parametrit > Vähittäismyyntiparametrit.</span><span class="sxs-lookup"><span data-stu-id="eddfd-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="eddfd-107">Valitse Kirjaus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="eddfd-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="eddfd-108">Valitse Kyllä, jos haluat kirjata erityisesti kausialennussummat.</span><span class="sxs-lookup"><span data-stu-id="eddfd-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="eddfd-109">Valitse Vakio, kun haluat käyttää oletustilejä. Valitse Kausittainen, jos haluat määrittää kunkin kausialennuksen käyttämän tili.</span><span class="sxs-lookup"><span data-stu-id="eddfd-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="eddfd-110">Valitse Yhteenveto, jos varastorivit yhdistetään aina, kun se on mahdollista.</span><span class="sxs-lookup"><span data-stu-id="eddfd-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="eddfd-111">Valitse Kyllä, jos laskut ja maksut selvitetään automaattisesti laskelman kirjausprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="eddfd-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="eddfd-112">Valitse Kyllä, jos kassakaappiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="eddfd-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="eddfd-113">Valitse Kyllä, jos pankkiin toimitukset yhdistetään.</span><span class="sxs-lookup"><span data-stu-id="eddfd-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="eddfd-114">Valitse Kyllä, jos laskelman kirjauksen yhdistäminen otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="eddfd-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="eddfd-115">Valitse Kyllä, kun tilaukset luodaan ja käsitellään rinnakkain, kun laskelmat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="eddfd-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="eddfd-116">Syötä kussakin erätyötehtävässä käsiteltävien tilausten enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="eddfd-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="eddfd-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="eddfd-117">Click Save.</span></span>


