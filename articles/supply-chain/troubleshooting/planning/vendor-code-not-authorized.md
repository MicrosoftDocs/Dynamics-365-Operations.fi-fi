---
title: Toimittajan koodia ei ole valtuutettu tietylle tuotteelle ja päivämäärälle
description: Kun yrität vahvistaa suunnitellun tilauksen tai lisätä rivin ostotilaukseen, näyttöön tulee virhesanoma, jossa todetaan, että toimittajan koodi ei ole valtuutettu tuotteen ja päivämäärän osalta.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294068"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="49c5f-103">Toimittajan koodia ei ole valtuutettu tietylle tuotteelle ja päivämäärälle</span><span class="sxs-lookup"><span data-stu-id="49c5f-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="49c5f-104">Virhekoodi: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="49c5f-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="49c5f-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="49c5f-105">Symptoms</span></span>

<span data-ttu-id="49c5f-106">Kun yrität vahvistaa suunnitellun tilauksen tai lisätä rivin ostotilaukseen, näyttöön tulee seuraava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="49c5f-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="49c5f-107">Toimittajan koodia %1 ei ole valtuutettu kohteelle %2 kohteessa %3.</span><span class="sxs-lookup"><span data-stu-id="49c5f-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="49c5f-108">Syy</span><span class="sxs-lookup"><span data-stu-id="49c5f-108">Cause</span></span>

<span data-ttu-id="49c5f-109">Virhe ilmenee, koska hyväksytyn **toimittajan tarkistusmenetelmän** kentän arvoksi on määritetty *Vain varoitus* tai *Ei sallittu* määritetylle tuotteelle eikä toimittajalla ole tällä hetkellä oikeutta toimittaa tätä tuotetta.</span><span class="sxs-lookup"><span data-stu-id="49c5f-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="49c5f-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="49c5f-110">Resolution</span></span>

<span data-ttu-id="49c5f-111">Voit korjata tämän ongelman poistamalla toimittajan valintaruudun käytöstä tai hyväksymällä toimittajan.</span><span class="sxs-lookup"><span data-stu-id="49c5f-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="49c5f-112">Jos haluat poistaa tuotteen toimittajan tarkistuksen käytöstä, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="49c5f-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="49c5f-113">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="49c5f-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="49c5f-114">Avaa asiaankuuluva tuote.</span><span class="sxs-lookup"><span data-stu-id="49c5f-114">Open the relevant product.</span></span>
1. <span data-ttu-id="49c5f-115">Määritä **Osto**-pikavälilehdessä **Hyväksytyn toimittajan tarkistusmenetelmä** -kentän arvoksi jokin muu kuin *Vain varoitus* tai *Ei sallittu*.</span><span class="sxs-lookup"><span data-stu-id="49c5f-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="49c5f-116">Jos haluat hyväksyä tuotteen toimittajan, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="49c5f-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="49c5f-117">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="49c5f-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="49c5f-118">Avaa asiaankuuluva nimike.</span><span class="sxs-lookup"><span data-stu-id="49c5f-118">Open the relevant item.</span></span>
1. <span data-ttu-id="49c5f-119">Valitse Toimintoruudussa **Osto**-välilehdellä **Hyväksytty toimittaja** -ryhmässä **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="49c5f-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="49c5f-120">Lisää rivi ruudukkoon **Hyväksytty toimittaja** -luettelosivulla ja määritä sitten sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="49c5f-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="49c5f-121">**Toimittaja** – Valitse toimittaja, joka hyväksytään nykyiselle tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="49c5f-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="49c5f-122">**Voimaantulopäivä** – Valitse ensimmäinen päivä, jona toimittaja on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="49c5f-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="49c5f-123">**Erääntymispäivä** – Valitse viimeinen päivä, jona toimittaja on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="49c5f-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="49c5f-124">Lisätietoja on kohdassa [Toimittajien hyväksyminen tiettyihin tuotteisiin](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="49c5f-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
