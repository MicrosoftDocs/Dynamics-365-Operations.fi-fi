---
title: "Varaston vanhojen erien näyttämisen määrittäminen mobiililaitteessa"
description: "Tässä ohjeaiheessa kerrotaan, miten mobiililaite määritetään näyttämään luettelon sijainneista, joissa on työrivin nykyistä sijaintia vanhempia eriä."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 946266e73d59bdf383f1f91cdf70dd58f01b995c
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="20864-103">Varaston vanhojen erien näyttämisen määrittäminen mobiililaitteessa</span><span class="sxs-lookup"><span data-stu-id="20864-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20864-104">**Näytä varaston vanhat erät** -määrityksellä saadaan näkyviin luettelo sijainnista, joissa on vanhempia eriä kuin työrivin nykyinen sijainti.</span><span class="sxs-lookup"><span data-stu-id="20864-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="20864-105">Näkyvässä sijaintiluettelossa on tietoja sijainnin vanhoista eristä, erien erääntymispäivä ja kunkin erän fyysinen varasto.</span><span class="sxs-lookup"><span data-stu-id="20864-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="20864-106">Voit valita keräilyn uudesta sijainnista tai jatkaa keräilyä nykyisestä sijainnista.</span><span class="sxs-lookup"><span data-stu-id="20864-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="20864-107">Kerää uudesta sijainnista – Jos valitse keräilyn uudesta sijainnista, nykyinen työrivi päivitetään käyttämään uutta sijaintia ja työ jatkuu entiseen tapaan uudessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="20864-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="20864-108">Uusi sijainti kelpaa, kun sen käytettävissä oleva määrä kattaa koko työrivin.</span><span class="sxs-lookup"><span data-stu-id="20864-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="20864-109">Jos vaadittu määrä ei ole käytettävissä, työriviä ei päivitetään ja luettelo on näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="20864-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="20864-110">Jatka keräilyä nykyisestä sijainnista – Jos jatkat työrivin nykyisessä sijainnissa, työrivin määrien keräilyä jatketaan alkuperäisestä sijainnista.</span><span class="sxs-lookup"><span data-stu-id="20864-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="20864-111">Käyttö</span><span class="sxs-lookup"><span data-stu-id="20864-111">Where it applies</span></span>
<span data-ttu-id="20864-112">Näytä varaston vanhat erät määritetään mobiililaitteen valikkovaihtoehdoissa ja se vaikuttaa erän alempien nimikkeiden keräilyyn.</span><span class="sxs-lookup"><span data-stu-id="20864-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="20864-113">Varaston vanhojen erien näyttämisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="20864-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="20864-114">**Näytä varaston vanhat erät** -määritys on valittavissa mobiililaitteen valikossa, kun **Valitse vanhin erä** -asetukseksi on määritetty **Varoitus**.</span><span class="sxs-lookup"><span data-stu-id="20864-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="20864-115">Valitse ensin **Varastonhallinta** > **Asetukset** > **Mobiililaite** > **Mobiililaitteen valikkovaihtoehdot**, valitse sitten **Käytä nykyistä työtä** -arvoksi **Kyllä** ja valitse lopuksi **Varoitus** **Valitse vanhin erä** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="20864-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 


