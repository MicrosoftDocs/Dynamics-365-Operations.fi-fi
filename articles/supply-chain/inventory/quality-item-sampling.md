---
title: Laadunhallinnan nimikeotanta
description: Tässä aiheessa käsitellään nimikeotannan määrittämistä.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956632"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="6d44d-103">Laadunhallinnan nimikeotanta</span><span class="sxs-lookup"><span data-stu-id="6d44d-103">Quality management item sampling</span></span>

<span data-ttu-id="6d44d-104">Nimikeotantaa käytetään laatuliitoksen osana.</span><span class="sxs-lookup"><span data-stu-id="6d44d-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="6d44d-105">Se määrittää nykyisen fyysisen varaston määrän, joka on tarkastettava.</span><span class="sxs-lookup"><span data-stu-id="6d44d-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="6d44d-106">Otanta voi perustua kiinteisiin määriin, prosenttiosuuteen tai täyteen rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="6d44d-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="6d44d-107">Nimikeotannan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6d44d-107">Set up item sampling</span></span>

<span data-ttu-id="6d44d-108">Voit määrittää nimikeotannan noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="6d44d-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="6d44d-109">Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Nimikeotanta**.</span><span class="sxs-lookup"><span data-stu-id="6d44d-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="6d44d-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6d44d-110">Select **New**.</span></span>
1. <span data-ttu-id="6d44d-111">Kirjoita arvo **Nimikeotanta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6d44d-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="6d44d-112">Anna arvo **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="6d44d-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="6d44d-113">Kirjoita numero **Arvo**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6d44d-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="6d44d-114">Tämä arvo liittyy määrän määrityksen arvoon, joka valitaan viereisessä kentässä.</span><span class="sxs-lookup"><span data-stu-id="6d44d-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="6d44d-115">Valitse **Prosessi**-osassa **Täysi esto** -valintaruutu, jos koko erä tai tilausrivin määrä estetään, jos testi epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="6d44d-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="6d44d-116">Jos tämän valintaruudun valinta poistetaan, vain laatutilauksen nimikkeet estetään, jos testi epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="6d44d-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="6d44d-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6d44d-117">Select **Save**.</span></span>
1. <span data-ttu-id="6d44d-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6d44d-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="6d44d-119">*Varastoprosessien laadunhallinta* -toiminto tarjoaa lisää nimikkeen otantatoimintoja.</span><span class="sxs-lookup"><span data-stu-id="6d44d-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="6d44d-120">Se lisää käsitteen *Nimikkeen otanta-alueesta* ja mahdollisuuden määrittää täyden rekisterikilven määrä määritykseksi.</span><span class="sxs-lookup"><span data-stu-id="6d44d-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="6d44d-121">Jos olet ottanut tämän toiminnon käyttöön, lisätietoja on kohdassa [Varastoprosessien laadunhallinta](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="6d44d-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
