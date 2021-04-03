---
title: Online-tilausten verot on laskettu väärin
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585299"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="d2237-103">Online-tilausten verot on laskettu väärin</span><span class="sxs-lookup"><span data-stu-id="d2237-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2237-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="d2237-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="d2237-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d2237-105">Description</span></span>

<span data-ttu-id="d2237-106">Kun sähköinen kaupankäyntitilaus on tehty, verot lasketaan väärin tai myyntirivin veroryhmä on määritetty väärin.</span><span class="sxs-lookup"><span data-stu-id="d2237-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="d2237-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="d2237-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="d2237-108">Vähittäismyymälän arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="d2237-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="d2237-109">Voit konfiguroida vähittäismyymälän arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d2237-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d2237-110">Valitse **Retail ja Commerce \> Kanavat \> Kaikki myymälät**.</span><span class="sxs-lookup"><span data-stu-id="d2237-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="d2237-111">Valitse myymälä, jolle arvonlisävero konfiguroitaan.</span><span class="sxs-lookup"><span data-stu-id="d2237-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="d2237-112">Määritä myymälän arvonlisäverotiedot **Yleiset**-pikavälilehden **Arvonlisävero**-osassa.</span><span class="sxs-lookup"><span data-stu-id="d2237-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="d2237-113">Jos tuote noudetaan myymälästä, veroryhmä tulee noutoa varten valitusta myymälästä.</span><span class="sxs-lookup"><span data-stu-id="d2237-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="d2237-114">Lisätietoja on kohdassa [Muiden myymälän veroasetusten määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="d2237-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="d2237-115">Asiakkaan osoitteen arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="d2237-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="d2237-116">Voit konfiguroida asiakkaan osoitteen arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d2237-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d2237-117">Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="d2237-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="d2237-118">Valitse asiakas, jolle arvonlisäverot määritetään.</span><span class="sxs-lookup"><span data-stu-id="d2237-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="d2237-119">Valitse **Osoitteet**-pikavälilehdestä osoite, jolle haluat määrittää arvonlisäverot, valitse **Lisää vaihtoehtoja** ja valitse sitten **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="d2237-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="d2237-120">Valitse **Yleiset**-pikavälilehdessä **Veroryhmä**.</span><span class="sxs-lookup"><span data-stu-id="d2237-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="d2237-121">Valitse sopiva arvo **Arvonlisävero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d2237-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="d2237-122">Lähetykselle, johon liittyy asiakkaan osoitteen arvonlisäveroa, rivin toimitusosoite määrittää rivin veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="d2237-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="d2237-123">Jos asiakkaalle toimitetaan olemassa olevaan osoitteeseen, jonka veroryhmä on jo konfiguroitu, käytetään aiemmin luotua veroryhmää.</span><span class="sxs-lookup"><span data-stu-id="d2237-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="d2237-124">Osoitteilla ei oletusarvoisesti ole veroryhmää, kun ne luodaan.</span><span class="sxs-lookup"><span data-stu-id="d2237-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="d2237-125">Yleisten arvonlisäveroryhmien konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="d2237-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="d2237-126">Voit konfiguroida yleiset arvonlisäveroryhmät Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="d2237-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d2237-127">Siirry kohtaan **Vero \> Välilliset verot \> Arvonlisävero \> Arvonlisäveroryhmä**.</span><span class="sxs-lookup"><span data-stu-id="d2237-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="d2237-128">Valitse määritettävä veroryhmä vasemmasta siirtymisruudusta.</span><span class="sxs-lookup"><span data-stu-id="d2237-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="d2237-129">Määritä arvonlisäveroryhmän verot **Vähittäismyyntikohteeseen perustuva vero** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d2237-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="d2237-130">Jos lähetykseen ei liity arvonlisäveroa asiakkaan osoitteeseen, rivin toimitusosoite sekä veroryhmälle määritetyt kohteeseen perustuvat verot määrittävät veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="d2237-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="d2237-131">Lisätietoja on kohdassa [Määränpäähän perustuvien verojen määrittäminen online-myymälöille](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="d2237-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2237-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d2237-132">Additional resources</span></span>

[<span data-ttu-id="d2237-133">Arvonlisäveron laskeminen online-tilauksille</span><span class="sxs-lookup"><span data-stu-id="d2237-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
