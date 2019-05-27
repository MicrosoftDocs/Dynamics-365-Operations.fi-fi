---
title: Sisällytä fyysinen arvo
description: Nimikemalliryhmät -sivun Varastomalli-pikavälilehden Sisällytä fyysinen arvo -valintaruudun avulla määritetään, otetaanko fyysisesti päivitetyt tapahtumat huomioon nimikkeen keskimääräisen käyttökustannushinnan laskennassa.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96d5e2a658a027d66663868329cf4eedcb1d46f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551971"
---
# <a name="include-physical-value"></a><span data-ttu-id="a1cff-103">Sisällytä fyysinen arvo</span><span class="sxs-lookup"><span data-stu-id="a1cff-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1cff-104">Nimikemalliryhmät -sivun Varastomalli-pikavälilehden Sisällytä fyysinen arvo -valintaruudun avulla määritetään, otetaanko fyysisesti päivitetyt tapahtumat huomioon nimikkeen keskimääräisen käyttökustannushinnan laskennassa.</span><span class="sxs-lookup"><span data-stu-id="a1cff-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="a1cff-105">**Sisällytä fyysinen arvo** -valintaruudulla on seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="a1cff-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="a1cff-106">Arvo</span><span class="sxs-lookup"><span data-stu-id="a1cff-106">Value</span></span>    | <span data-ttu-id="a1cff-107">Tulos</span><span class="sxs-lookup"><span data-stu-id="a1cff-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1cff-108">Valittu</span><span class="sxs-lookup"><span data-stu-id="a1cff-108">Selected</span></span> | <span data-ttu-id="a1cff-109">Keskimääräisen kustannushinnan laskennassa käytetään sekä fyysisesti että rahoituksellisesti päivitettyjä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a1cff-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="a1cff-110">Selvitetyt</span><span class="sxs-lookup"><span data-stu-id="a1cff-110">Cleared</span></span>  | <span data-ttu-id="a1cff-111">Keskimääräisen kustannushinnan laskennassa käytetään vain rahoituksellisesti päivitettyjä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a1cff-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="a1cff-112">Valintaruudulla on hieman erilaisia vaikutuksia käytettävän varastomallin mukaan.</span><span class="sxs-lookup"><span data-stu-id="a1cff-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="a1cff-113">Jos valitset **Sisällytä fyysinen arvo** -valintaruudun, kun käytät FIFO-, LIFO- tai LIFO-päivämäärävarastomallia, varaston sulkeminen oikaisee myös fyysisesti päivitetyt tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a1cff-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="a1cff-114">Jos et valitse **Sisällytä fyysinen arvo** -valintaruutua käyttäessäsi näitä varastomalleja, varaston sulkeminen selvittää vain kirjanpidollisesti päivitetyt tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a1cff-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="a1cff-115">Kun käytät painotettua keskiarvoa tai painotetun keskiarvon päivämäärän varastomallia, varaston sulkeminen selvittää vain rahoituksellisesti päivitetyt tapahtumat riippumatta siitä, onko **Sisällytä fyysinen arvo** -valintaruutu valittu.</span><span class="sxs-lookup"><span data-stu-id="a1cff-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="a1cff-116">**Esimerkki 1** Olet valinnut **Sisällytä fyysinen arvo** -valintaruudun ja saat seuraavat ostotilaukset:</span><span class="sxs-lookup"><span data-stu-id="a1cff-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="a1cff-117">Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on pakkausluettelopäivitetty</span><span class="sxs-lookup"><span data-stu-id="a1cff-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="a1cff-118">Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskupäivitetty</span><span class="sxs-lookup"><span data-stu-id="a1cff-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="a1cff-119">Tässä tilanteessa keskimääräinen käyttökustannushinta on 11,20 Yhdysvaltain dollaria (USD), koska kustannushinnan laskennassa käytetään sekä fyysisesti että rahoituksellisesti päivitettyjä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a1cff-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="a1cff-120">**Esimerkki 2** Et ole valinnut **Sisällytä fyysinen arvo** -valintaruutua ja nimikeasetusten kustannushinta on 10,00 Yhdysvaltain dollaria (USD).</span><span class="sxs-lookup"><span data-stu-id="a1cff-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="a1cff-121">Saat ostotilauksen, jonka määrä on 20 ja kustannushinta 12,00 USD, ja se on pakkausluettelopäivitetty.</span><span class="sxs-lookup"><span data-stu-id="a1cff-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="a1cff-122">Kun myyntitilaus kirjataan, kirjattu kustannussumman on 10,00 Yhdysvaltain dollaria (USD), koska fyysisesti kirjatut tapahtumat eivät ole mukana keskimääräisessä käyttökustannushinnassa.</span><span class="sxs-lookup"><span data-stu-id="a1cff-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="a1cff-123">**Huomautus:** Jos puolestaan olet valinnut nimikkeen **Sisällytä fyysinen arvo** -valintaruudun ja myyntitilaus kirjataan, kirjattu kustannussumma on 12,00 Yhdysvaltain dollaria.</span><span class="sxs-lookup"><span data-stu-id="a1cff-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>



