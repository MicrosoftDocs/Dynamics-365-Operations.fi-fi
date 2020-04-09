---
title: Synkronointi Dynamics 365 Supply Chain Management -hinnoittelumoduulin kanssa tarvittaessa
description: Tässä ohjeaiheessa kuvataan, kuinka hinnoittelumoduulia käytetään Microsoft Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesista.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173174"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="0bf54-103">Synkronointi Dynamics 365 Supply Chain Management -hinnoittelumoduulin kanssa tarvittaessa</span><span class="sxs-lookup"><span data-stu-id="0bf54-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0bf54-104">Microsoft Dynamics 365 Supply Chain Management sisältää hinnoittelumoduulin, joka käsittelee kauppasopimukset, hinnastot, kanta-asiakasohjelmat, kampanjat ja alennukset.</span><span class="sxs-lookup"><span data-stu-id="0bf54-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="0bf54-105">Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="0bf54-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="0bf54-106">Kun käytät kaksoiskirjoittamista, voit käyttää joko staattista hinnoittelua tai hinnoittelumoduulia Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesin tarjous- ja tilaussivuilla.</span><span class="sxs-lookup"><span data-stu-id="0bf54-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="0bf54-107">Hinnoittelumoduulin käyttäminen Salesin Supply Chain Managementista</span><span class="sxs-lookup"><span data-stu-id="0bf54-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="0bf54-108">Siirry Salesissa kohtaan **Myynti \> Tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="0bf54-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="0bf54-109">Valitse **Uusi** luodaksesi uuden tilauksen tai valitse olemassa oleva tilaus **Omat tilaukset** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="0bf54-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="0bf54-110">Uuden tilausrivin lisääminen.</span><span class="sxs-lookup"><span data-stu-id="0bf54-110">Add a new order line.</span></span>
4. <span data-ttu-id="0bf54-111">Jos luot uuden tilauksen, valitse toimintoruudusta **Hintatilaus**.</span><span class="sxs-lookup"><span data-stu-id="0bf54-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="0bf54-112">Jos päivität olemassa olevan tilauksen, valitse toimintoruudusta **Laske uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="0bf54-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="0bf54-113">Seuraavat kentät täytetään automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="0bf54-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="0bf54-114">Tietojen määrä</span><span class="sxs-lookup"><span data-stu-id="0bf54-114">Detail Amount</span></span>
    + <span data-ttu-id="0bf54-115">Alennusprosentti</span><span class="sxs-lookup"><span data-stu-id="0bf54-115">Discount %</span></span>
    + <span data-ttu-id="0bf54-116">Alennus</span><span class="sxs-lookup"><span data-stu-id="0bf54-116">Discount</span></span>
    + <span data-ttu-id="0bf54-117">Rahdin ennakkosumma</span><span class="sxs-lookup"><span data-stu-id="0bf54-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="0bf54-118">Rahdin summa</span><span class="sxs-lookup"><span data-stu-id="0bf54-118">Freight Amount</span></span>
    + <span data-ttu-id="0bf54-119">Vero yhteensä</span><span class="sxs-lookup"><span data-stu-id="0bf54-119">Total Tax</span></span>
    + <span data-ttu-id="0bf54-120">Loppusumma</span><span class="sxs-lookup"><span data-stu-id="0bf54-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="0bf54-121">Näin se toimii</span><span class="sxs-lookup"><span data-stu-id="0bf54-121">How it works</span></span>

<span data-ttu-id="0bf54-122">Kun valitset **Hintatilauksen** Salesissa, **Yhteensä**-toiminto **Myyntitilaus \>Näkymä** -välilehden Supply Chain Managementissa on nimeltään liittyvä myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="0bf54-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="0bf54-123">Myynnin tilauksen kokonaissumman arvoja käytetään toimitusketjun hallinnan vastaavien kenttien täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="0bf54-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="0bf54-124">Kun myyntitilauksen kokonaissumma lasketaan Supply Chain Managementissa, laskelma laskee asiakkaan ja myyntitilauksessa lueteltujen tuotteiden olemassa olevat kauppasopimukset ja myyntisopimukset.</span><span class="sxs-lookup"><span data-stu-id="0bf54-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="0bf54-125">Näitä tietoja käytetään summien laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="0bf54-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="0bf54-126">Kun **Hintatilaus** valitaan, Sales vastaa automaattisesti kaikkia Supply Chain Managementin asetuksia.</span><span class="sxs-lookup"><span data-stu-id="0bf54-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="0bf54-127">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="0bf54-127">Limitations</span></span>

<span data-ttu-id="0bf54-128">Kun Salesin kentät on täytetty, seuraavat rajoitukset ovat voimassa:</span><span class="sxs-lookup"><span data-stu-id="0bf54-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="0bf54-129">Supply Chain Managementin kuluja ja kulujen kohdistuksia ei replikoida Salesiin.</span><span class="sxs-lookup"><span data-stu-id="0bf54-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="0bf54-130">Hinnoittelu ei ota huomioon erikoisvähittäismyyntihinnoittelua, joka on määritetty **Vähittäismyyntikanava**-kentässä myyntitilausrivisivulla Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="0bf54-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="0bf54-131">Supply Chain Managementin **Myynninedistämispalkkioiden hallinta** -osassa määritettyjä alennuksia ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="0bf54-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
