---
title: Arvonlisäveron laskeminen online-tilauksille
description: Tässä ohjeaiheessa on yhteenveto eri online-tilaustyyppien arvonlisäveroryhmän valinnasta Dynamics 365 Commercessa.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 56621bb9658b71551c7312aa47812903914bc888
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031786"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="f714e-103">Arvonlisäveron laskeminen online-tilauksille</span><span class="sxs-lookup"><span data-stu-id="f714e-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f714e-104">Tässä ohjeaiheessa on yhteenveto eri online-tilaustyyppien arvonlisäveroryhmän valinnasta.</span><span class="sxs-lookup"><span data-stu-id="f714e-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="f714e-105">Sähköisen kaupankäynnin kanava voi tarvita tuen online-tilausten vaihtoehdoille, kuten toimittamiselle tai noudolle.</span><span class="sxs-lookup"><span data-stu-id="f714e-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="f714e-106">Arvonlisäveron sovellettavuus perustuu online-käyttäjien valitsemaan vaihtoehtoon.</span><span class="sxs-lookup"><span data-stu-id="f714e-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="f714e-107">Kun sivuston asiakas haluaa ostaa nimikkeen verkosta ja saada sen toimitetuksi osoitteeseen, arvonlisävero määräytyy asiakkaan toimitusosoitteen veroryhmän asetuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f714e-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="f714e-108">Kun asiakas päättää noutaa ostetun nimikkeen myymälästä, arvonlisävero määräytyy noutomyymälän veroryhmän asetuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f714e-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="f714e-109">Asiakkaan osoitteeseen toimitetut tilaukset</span><span class="sxs-lookup"><span data-stu-id="f714e-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="f714e-110">Yleensä asiakkaan osoitteisiin toimitettavien online-tilausten verot määräytyvät määränpään mukaan.</span><span class="sxs-lookup"><span data-stu-id="f714e-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="f714e-111">Jokaisella arvonlisäveroryhmällä on vähittäismyynnin määränpäähän perustuva verokonfiguraatio, jossa yrityksesi voi määrittää määränpään tiedot, kuten läänin/alueen, osavaltion, läänin ja kaupungin hierarkkisessa muodossa.</span><span class="sxs-lookup"><span data-stu-id="f714e-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="f714e-112">Kun online-tilaus tehdään, Commercen veromoduuli käyttää jokaisen tilauksen rivinimikkeen toimitusosoitetta ja etsii arvonlisäveroryhmät, joilla on vastaavat kohteeseen perustuvat verokriteerit.</span><span class="sxs-lookup"><span data-stu-id="f714e-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="f714e-113">Esimerkiksi online-tilauksessa, jonka rivinimikkeen toimitusosoite on San Francisco, Kalifornia, veromoduuli etsii arvonlisävero ryhmän ja arvonlisäverokoodin Kaliforniasta ja laskee sitten kunkin rivinimikkeen veron sen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f714e-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="f714e-114">Asiakaspohjaiset veroryhmät</span><span class="sxs-lookup"><span data-stu-id="f714e-114">Customer-based tax groups</span></span>

<span data-ttu-id="f714e-115">Commerce-pääkonttorisovelluksessa on kaksi paikkaa, joissa asiakkaan veroryhmät on konfiguroitu:</span><span class="sxs-lookup"><span data-stu-id="f714e-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="f714e-116">**Asiakkaan profiili**</span><span class="sxs-lookup"><span data-stu-id="f714e-116">**Customer's profile**</span></span>
- <span data-ttu-id="f714e-117">**Asiakkaan toimitusosoite**</span><span class="sxs-lookup"><span data-stu-id="f714e-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="f714e-118">Jos asiakkaan profiilissa on määritetty veroryhmä</span><span class="sxs-lookup"><span data-stu-id="f714e-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="f714e-119">Asiakkaan profiilitietueeseen pääkonttorisovelluksessa voi olla määritetty arvonlisäveroryhmä, mutta online-tilauksissa veromoduuli ei käytä asiakkaan profiiliin konfiguroituja arvonlisäveroryhmiä.</span><span class="sxs-lookup"><span data-stu-id="f714e-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="f714e-120">Jos asiakkaan toimitusosoitteessa on määritetty veroryhmä</span><span class="sxs-lookup"><span data-stu-id="f714e-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="f714e-121">Jos asiakkaan toimitusosoitteen tietueessa on määritetty veroryhmä ja online-tilaus (tai rivinimike) toimitetaan asiakkaan toimitusosoitteeseen, veromoduuli käyttää asiakkaan osoitetietueeseen konfiguroituja veroryhmiä verolaskelmissa.</span><span class="sxs-lookup"><span data-stu-id="f714e-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="f714e-122">Veroryhmän määrittäminen asiakkaan toimitusosoitteen tietueessa</span><span class="sxs-lookup"><span data-stu-id="f714e-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="f714e-123">Voit määrittää asiakkaan toimitusosoitetietueen veroryhmän Commerce-pääkonttorisovelluksessa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f714e-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f714e-124">Siirry kohtaan **Kaikki asiakkaat** ja valitse haluamasi asiakas.</span><span class="sxs-lookup"><span data-stu-id="f714e-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="f714e-125">Valitse **Osoitteet**-pikavälilehdessä haluamasi osoite ja valitse sitten **Lisää vaihtoehtoja \> Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="f714e-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="f714e-126">Määritä arvonlisäveron arvo **Osoitteiden hallinta**-sivun **Yleiset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="f714e-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="f714e-127">Veroryhmä määritetään tilausrivin toimitusosoitteen avulla, ja kohteeseen perustuvat verot määritetään itse veroryhmässä.</span><span class="sxs-lookup"><span data-stu-id="f714e-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="f714e-128">Lisätietoja on kohdassa [Määränpäähän perustuvien verojen määrittäminen online-myymälöille](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="f714e-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="f714e-129">Tilauksen nouto myymälästä</span><span class="sxs-lookup"><span data-stu-id="f714e-129">Order pickup in store</span></span>

<span data-ttu-id="f714e-130">Jos tilausrivit on määritetty noudettaviksi myymälästä tai tien vierestä, valitun noutomyymälän veroryhmä otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f714e-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="f714e-131">Lisätietoja tietyn myymälän veroryhmän konfiguroinnista on kohdassa [Muiden veroasetusten määrittäminen myymälöille](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="f714e-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="f714e-132">Kun tilausrivi noudetaan myymälästä, veromoduuli ohittaa asiakkaan osoitteen veroasetukset (jos se on määritetty) ja noutomyymälän verokonfiguraatio otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f714e-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f714e-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f714e-133">Additional resources</span></span>

[<span data-ttu-id="f714e-134">Arvonlisäveron yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f714e-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f714e-135">Arvonlisäveron laskentatavat Alkuperä-kentässä</span><span class="sxs-lookup"><span data-stu-id="f714e-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f714e-136">Arvonlisäveron määrittäminen ja ohitukset</span><span class="sxs-lookup"><span data-stu-id="f714e-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f714e-137">Arvonlisäverokoodien koko summan ja välin laskentavaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="f714e-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f714e-138">Verovapauden laskenta</span><span class="sxs-lookup"><span data-stu-id="f714e-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 

