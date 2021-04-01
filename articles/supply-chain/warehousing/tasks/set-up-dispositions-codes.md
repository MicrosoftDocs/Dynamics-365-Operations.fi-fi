---
title: Määritä käsittelykoodit
description: Menettely koskee sellaista palautustilauksen vastaanottoprosessin käsittelykoodin määritystä, jota voidaan käyttää mobiililaitteella.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8eeba07aafbcbc327aa5e28a10d10c16b0e0f43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236539"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="739e2-103">Määritä käsittelykoodit</span><span class="sxs-lookup"><span data-stu-id="739e2-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="739e2-104">Menettely koskee sellaista palautustilauksen vastaanottoprosessin käsittelykoodin määritystä, jota voidaan käyttää mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="739e2-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="739e2-105">Käsittelykoodit ovat sääntökokoelma, joita voidaan käyttää nimikkeitä vastaanotettaessa.</span><span class="sxs-lookup"><span data-stu-id="739e2-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="739e2-106">Kun esimerkiksi työn käyttäjä vastaanottaa vioittuneita nimikkeitä mobiililaitteella, käyttäjän on skannattava vioittuneiden nimikkeiden käsittelykoodi.</span><span class="sxs-lookup"><span data-stu-id="739e2-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="739e2-107">Vastaanotettujen tavaroiden, työmallin ja sijaintidirektiivin varastotila voidaan määrittää skannatusta käsittelykoodista.</span><span class="sxs-lookup"><span data-stu-id="739e2-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="739e2-108">Käsittelykoodin käyttö ei ole pakollista ostotilausten vastaanottoprosessissa eikä tuotantotilauksen valmiiksi ilmoittamisprosessissa.</span><span class="sxs-lookup"><span data-stu-id="739e2-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="739e2-109">Käsittelykoodin käyttö on pakolista myyntitilauksen palautuksen vastaanottoprosessissa, jos nimikkeet on rekisteröity mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="739e2-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="739e2-110">Tämän oppaan luomisessa käytetty demotietojen yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="739e2-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="739e2-111">Tämä menettely on tarkoitettu varastopäällikölle.</span><span class="sxs-lookup"><span data-stu-id="739e2-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="739e2-112">Valitse Varastonhallinta > Asetukset > Mobiililaite > Käsittelykoodit.</span><span class="sxs-lookup"><span data-stu-id="739e2-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="739e2-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="739e2-113">Click New.</span></span>
    * <span data-ttu-id="739e2-114">Luo asiakaspalautuksille uusi käsittelykoodi.</span><span class="sxs-lookup"><span data-stu-id="739e2-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="739e2-115">Kirjoita arvo Käsittelykoodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="739e2-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="739e2-116">Valitse Varaston tila -kentässä varastotila, jossa on varastoesto.</span><span class="sxs-lookup"><span data-stu-id="739e2-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="739e2-117">Jos USMF on käytössä, valitse Esto.</span><span class="sxs-lookup"><span data-stu-id="739e2-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="739e2-118">Voit lisätä varaston tilan käsittelykoodiin. Se ohittaa tilausriveillä olevan oletustilan.</span><span class="sxs-lookup"><span data-stu-id="739e2-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="739e2-119">Kirjoita Työmalli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="739e2-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="739e2-120">Valinnainen: Valitse palautustilaukseen liitetty työmallikoodi.</span><span class="sxs-lookup"><span data-stu-id="739e2-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="739e2-121">Jos arvoa ei ole annettu, työmalli selvitetään käyttämällä järjestelmään määritettyjä vakiosääntöjä.</span><span class="sxs-lookup"><span data-stu-id="739e2-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="739e2-122">Työmallin valitseminen rajoittaa prosesseja, joiden kanssa käsittelykoodia voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="739e2-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="739e2-123">Jos esimerkiksi käsittelykoodissa on työmalli, joka työtilaustyyppi on ostotilaus, sillä ei voi rekisteröidä asiakkaiden palauttamia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="739e2-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="739e2-124">Kirjoita arvo Palauta käsittelykoodi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="739e2-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="739e2-125">Palautuksen käsittelykoodi määrittää rekisteröityjen nimikkeiden jäljellä olevat palautustilausprosessit.</span><span class="sxs-lookup"><span data-stu-id="739e2-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="739e2-126">Tässä esimerkissä asiakkaan pitäisi saada hyvityslasku.</span><span class="sxs-lookup"><span data-stu-id="739e2-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="739e2-127">Lisää palautuksen käsittelykoodi, joka sisältää hyvitystoiminnon.</span><span class="sxs-lookup"><span data-stu-id="739e2-127">Add a returns disposition code that contains an action Credit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]