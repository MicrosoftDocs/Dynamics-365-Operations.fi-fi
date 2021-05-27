---
title: Online-tilausten verot on laskettu väärin
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021100"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="60fa3-103">Online-tilausten verot on laskettu väärin</span><span class="sxs-lookup"><span data-stu-id="60fa3-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60fa3-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="60fa3-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="60fa3-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="60fa3-105">Description</span></span>

<span data-ttu-id="60fa3-106">Kun sähköinen kaupankäyntitilaus on tehty, verot lasketaan väärin tai myyntirivin veroryhmä on määritetty väärin.</span><span class="sxs-lookup"><span data-stu-id="60fa3-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="60fa3-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="60fa3-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="60fa3-108">Vähittäismyymälän arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="60fa3-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="60fa3-109">Voit konfiguroida vähittäismyymälän arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="60fa3-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="60fa3-110">Valitse **Retail ja Commerce \> Kanavat \> Kaikki myymälät**.</span><span class="sxs-lookup"><span data-stu-id="60fa3-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="60fa3-111">Valitse myymälä, jolle arvonlisävero konfiguroitaan.</span><span class="sxs-lookup"><span data-stu-id="60fa3-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="60fa3-112">Määritä myymälän arvonlisäverotiedot **Yleiset**-pikavälilehden **Arvonlisävero**-osassa.</span><span class="sxs-lookup"><span data-stu-id="60fa3-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="60fa3-113">Jos tuote noudetaan myymälästä, veroryhmä tulee noutoa varten valitusta myymälästä.</span><span class="sxs-lookup"><span data-stu-id="60fa3-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="60fa3-114">Lisätietoja on kohdassa [Muiden myymälän veroasetusten määrittäminen](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="60fa3-114">For more information, see [Set other tax options for stores](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="60fa3-115">Asiakkaan osoitteen arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="60fa3-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="60fa3-116">Voit konfiguroida asiakkaan osoitteen arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="60fa3-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="60fa3-117">Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="60fa3-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="60fa3-118">Valitse asiakas, jolle arvonlisäverot määritetään.</span><span class="sxs-lookup"><span data-stu-id="60fa3-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="60fa3-119">Valitse **Osoitteet**-pikavälilehdestä osoite, jolle haluat määrittää arvonlisäverot, valitse **Lisää vaihtoehtoja** ja valitse sitten **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="60fa3-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="60fa3-120">Valitse **Yleiset**-pikavälilehdessä **Veroryhmä**.</span><span class="sxs-lookup"><span data-stu-id="60fa3-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="60fa3-121">Valitse sopiva arvo **Arvonlisävero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="60fa3-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="60fa3-122">Lähetykselle, johon liittyy asiakkaan osoitteen arvonlisäveroa, rivin toimitusosoite määrittää rivin veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="60fa3-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="60fa3-123">Jos asiakkaalle toimitetaan olemassa olevaan osoitteeseen, jonka veroryhmä on jo konfiguroitu, käytetään aiemmin luotua veroryhmää.</span><span class="sxs-lookup"><span data-stu-id="60fa3-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="60fa3-124">Osoitteilla ei oletusarvoisesti ole veroryhmää, kun ne luodaan.</span><span class="sxs-lookup"><span data-stu-id="60fa3-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="60fa3-125">Yleisten arvonlisäveroryhmien konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="60fa3-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="60fa3-126">Voit konfiguroida yleiset arvonlisäveroryhmät Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="60fa3-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="60fa3-127">Siirry kohtaan **Vero \> Välilliset verot \> Arvonlisävero \> Arvonlisäveroryhmä**.</span><span class="sxs-lookup"><span data-stu-id="60fa3-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="60fa3-128">Valitse määritettävä veroryhmä vasemmasta siirtymisruudusta.</span><span class="sxs-lookup"><span data-stu-id="60fa3-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="60fa3-129">Määritä arvonlisäveroryhmän verot **Vähittäismyyntikohteeseen perustuva vero** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="60fa3-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="60fa3-130">Jos lähetykseen ei liity arvonlisäveroa asiakkaan osoitteeseen, rivin toimitusosoite sekä veroryhmälle määritetyt kohteeseen perustuvat verot määrittävät veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="60fa3-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="60fa3-131">Lisätietoja on kohdassa [Määränpäähän perustuvien verojen määrittäminen online-myymälöille](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="60fa3-131">For more information, see [Set up taxes for online stores based on destination](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60fa3-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="60fa3-132">Additional resources</span></span>

[<span data-ttu-id="60fa3-133">Arvonlisäveron laskeminen online-tilauksille</span><span class="sxs-lookup"><span data-stu-id="60fa3-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)