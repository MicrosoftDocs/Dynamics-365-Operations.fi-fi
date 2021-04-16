---
title: Synkronointi tarvittaessa Supply Chain Managementin hinnoittelumoduulin kanssa
description: Tässä ohjeaiheessa kuvataan, kuinka hinnoittelumoduulia käytetään Microsoft Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesista.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750761"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="6f9f8-103">Synkronointi tarvittaessa Supply Chain Managementin hinnoittelumoduulin kanssa</span><span class="sxs-lookup"><span data-stu-id="6f9f8-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6f9f8-104">Microsoft Dynamics 365 Supply Chain Management sisältää hinnoittelumoduulin, joka käsittelee kauppasopimukset, hinnastot, kanta-asiakasohjelmat, kampanjat ja alennukset.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="6f9f8-105">Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="6f9f8-106">Kun käytät kaksoiskirjoittamista, voit käyttää joko staattista hinnoittelua tai hinnoittelumoduulia Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesin tarjous- ja tilaussivuilla.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="6f9f8-107">Hinnoittelumoduulin käyttäminen Salesin Supply Chain Managementista</span><span class="sxs-lookup"><span data-stu-id="6f9f8-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="6f9f8-108">Siirry Salesissa kohtaan **Myynti \> Tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="6f9f8-109">Valitse **Uusi** luodaksesi uuden tilauksen tai valitse olemassa oleva tilaus **Omat tilaukset** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="6f9f8-110">Uuden tilausrivin lisääminen.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-110">Add a new order line.</span></span>
4. <span data-ttu-id="6f9f8-111">Jos luot uuden tilauksen, valitse toimintoruudusta **Hintatilaus**.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="6f9f8-112">Jos päivität olemassa olevan tilauksen, valitse toimintoruudusta **Laske uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="6f9f8-113">Seuraavat sarakkeet täytetään automaattisesti:</span><span class="sxs-lookup"><span data-stu-id="6f9f8-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="6f9f8-114">Tietojen määrä</span><span class="sxs-lookup"><span data-stu-id="6f9f8-114">Detail Amount</span></span>
    + <span data-ttu-id="6f9f8-115">Alennusprosentti</span><span class="sxs-lookup"><span data-stu-id="6f9f8-115">Discount %</span></span>
    + <span data-ttu-id="6f9f8-116">Alennus</span><span class="sxs-lookup"><span data-stu-id="6f9f8-116">Discount</span></span>
    + <span data-ttu-id="6f9f8-117">Rahdin ennakkosumma</span><span class="sxs-lookup"><span data-stu-id="6f9f8-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="6f9f8-118">Rahdin summa</span><span class="sxs-lookup"><span data-stu-id="6f9f8-118">Freight Amount</span></span>
    + <span data-ttu-id="6f9f8-119">Vero yhteensä</span><span class="sxs-lookup"><span data-stu-id="6f9f8-119">Total Tax</span></span>
    + <span data-ttu-id="6f9f8-120">Loppusumma</span><span class="sxs-lookup"><span data-stu-id="6f9f8-120">Total Amount</span></span>
    
5. <span data-ttu-id="6f9f8-121">Sen varmistamiseksi, että järjestelmä ottaa huomioon kauppa- ja myyntisopimukset hinnan laskennassa:</span><span class="sxs-lookup"><span data-stu-id="6f9f8-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="6f9f8-122">Siirry Supply Chain Management -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="6f9f8-123">Siirry kohtaan **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="6f9f8-124">Valitse sivunavigointipalkista **Hinnat**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="6f9f8-125">Poista **kauppasopimuksen arviointi** -pikavälilehdestä **manuaalinen syöttö** -valinta.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="6f9f8-126">Näin se toimii</span><span class="sxs-lookup"><span data-stu-id="6f9f8-126">How it works</span></span>

<span data-ttu-id="6f9f8-127">Kun valitset **Hintatilauksen** Salesissa, **Yhteensä**-toiminto **Myyntitilaus \>Näkymä** -välilehden Supply Chain Managementissa on nimeltään liittyvä myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="6f9f8-128">Myynnin tilauksen kokonaissumman arvoja käytetään Supply Chain Managementin vastaavien sarakkeiden täyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="6f9f8-129">Kun myyntitilauksen kokonaissumma lasketaan Supply Chain Managementissa, laskelma laskee asiakkaan ja myyntitilauksessa lueteltujen tuotteiden olemassa olevat kauppasopimukset ja myyntisopimukset.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="6f9f8-130">Näitä tietoja käytetään summien laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="6f9f8-131">Kun **Hintatilaus** valitaan, Sales vastaa automaattisesti kaikkia Supply Chain Managementin asetuksia.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="6f9f8-132">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="6f9f8-132">Limitations</span></span>

<span data-ttu-id="6f9f8-133">Kun Salesin sarakkeet on täytetty, seuraavat rajoitukset ovat voimassa:</span><span class="sxs-lookup"><span data-stu-id="6f9f8-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="6f9f8-134">Supply Chain Managementin kuluja ja kulujen kohdistuksia ei replikoida Salesiin.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="6f9f8-135">Hinnoittelu ei ota huomioon erikoisvähittäismyyntihinnoittelua, joka on määritetty **Vähittäismyyntikanava**-sarakkeessa myyntitilausrivisivulla Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="6f9f8-136">Supply Chain Managementin **Myynninedistämispalkkioiden hallinta** -osassa määritettyjä alennuksia ei oteta huomioon.</span><span class="sxs-lookup"><span data-stu-id="6f9f8-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]