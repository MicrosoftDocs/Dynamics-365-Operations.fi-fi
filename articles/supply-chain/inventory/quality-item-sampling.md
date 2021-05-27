---
title: Laadunhallinnan nimikeotanta
description: Tässä aiheessa käsitellään nimikeotannan määrittämistä.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022225"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="e7e81-103">Laadunhallinnan nimikeotanta</span><span class="sxs-lookup"><span data-stu-id="e7e81-103">Quality management item sampling</span></span>

<span data-ttu-id="e7e81-104">Nimikeotantaa käytetään laatuliitoksen osana.</span><span class="sxs-lookup"><span data-stu-id="e7e81-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="e7e81-105">Se määrittää nykyisen fyysisen varaston määrän, joka on tarkastettava.</span><span class="sxs-lookup"><span data-stu-id="e7e81-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="e7e81-106">Otanta voi perustua kiinteisiin määriin, prosenttiosuuteen tai täyteen rekisterikilpeen.</span><span class="sxs-lookup"><span data-stu-id="e7e81-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="e7e81-107">Nimikeotannan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e7e81-107">Set up item sampling</span></span>

<span data-ttu-id="e7e81-108">Voit määrittää nimikeotannan noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e7e81-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="e7e81-109">Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Nimikeotanta**.</span><span class="sxs-lookup"><span data-stu-id="e7e81-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="e7e81-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e7e81-110">Select **New**.</span></span>
1. <span data-ttu-id="e7e81-111">Kirjoita arvo **Nimikeotanta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e7e81-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="e7e81-112">Anna arvo **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7e81-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="e7e81-113">Kirjoita numero **Arvo**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e7e81-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="e7e81-114">Tämä arvo liittyy määrän määrityksen arvoon, joka valitaan viereisessä kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7e81-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="e7e81-115">Valitse **Prosessi**-osassa **Täysi esto** -valintaruutu, jos koko erä tai tilausrivin määrä estetään, jos testi epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="e7e81-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="e7e81-116">Jos tämän valintaruudun valinta poistetaan, vain laatutilauksen nimikkeet estetään, jos testi epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="e7e81-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="e7e81-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e7e81-117">Select **Save**.</span></span>
1. <span data-ttu-id="e7e81-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e7e81-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="e7e81-119">*Varastoprosessien laadunhallinta* -toiminto tarjoaa lisää nimikkeen otantatoimintoja.</span><span class="sxs-lookup"><span data-stu-id="e7e81-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="e7e81-120">Se lisää käsitteen *Nimikkeen otanta-alueesta* ja mahdollisuuden määrittää täyden rekisterikilven määrä määritykseksi.</span><span class="sxs-lookup"><span data-stu-id="e7e81-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="e7e81-121">Jos olet ottanut tämän toiminnon käyttöön, lisätietoja on kohdassa [Varastoprosessien laadunhallinta](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="e7e81-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
