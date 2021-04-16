---
title: Online-tilausten verot on laskettu väärin
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.
author: Reza-Assadi
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
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801408"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="64cee-103">Online-tilausten verot on laskettu väärin</span><span class="sxs-lookup"><span data-stu-id="64cee-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64cee-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun online-tilausten verot on laskettu väärin tai kun myyntirivin veroryhmää ei ole määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="64cee-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="64cee-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="64cee-105">Description</span></span>

<span data-ttu-id="64cee-106">Kun sähköinen kaupankäyntitilaus on tehty, verot lasketaan väärin tai myyntirivin veroryhmä on määritetty väärin.</span><span class="sxs-lookup"><span data-stu-id="64cee-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="64cee-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="64cee-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="64cee-108">Vähittäismyymälän arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="64cee-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="64cee-109">Voit konfiguroida vähittäismyymälän arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="64cee-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="64cee-110">Valitse **Retail ja Commerce \> Kanavat \> Kaikki myymälät**.</span><span class="sxs-lookup"><span data-stu-id="64cee-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="64cee-111">Valitse myymälä, jolle arvonlisävero konfiguroitaan.</span><span class="sxs-lookup"><span data-stu-id="64cee-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="64cee-112">Määritä myymälän arvonlisäverotiedot **Yleiset**-pikavälilehden **Arvonlisävero**-osassa.</span><span class="sxs-lookup"><span data-stu-id="64cee-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="64cee-113">Jos tuote noudetaan myymälästä, veroryhmä tulee noutoa varten valitusta myymälästä.</span><span class="sxs-lookup"><span data-stu-id="64cee-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="64cee-114">Lisätietoja on kohdassa [Muiden myymälän veroasetusten määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="64cee-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="64cee-115">Asiakkaan osoitteen arvonlisäveron konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="64cee-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="64cee-116">Voit konfiguroida asiakkaan osoitteen arvonlisäveron Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="64cee-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="64cee-117">Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="64cee-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="64cee-118">Valitse asiakas, jolle arvonlisäverot määritetään.</span><span class="sxs-lookup"><span data-stu-id="64cee-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="64cee-119">Valitse **Osoitteet**-pikavälilehdestä osoite, jolle haluat määrittää arvonlisäverot, valitse **Lisää vaihtoehtoja** ja valitse sitten **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="64cee-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="64cee-120">Valitse **Yleiset**-pikavälilehdessä **Veroryhmä**.</span><span class="sxs-lookup"><span data-stu-id="64cee-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="64cee-121">Valitse sopiva arvo **Arvonlisävero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="64cee-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="64cee-122">Lähetykselle, johon liittyy asiakkaan osoitteen arvonlisäveroa, rivin toimitusosoite määrittää rivin veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="64cee-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="64cee-123">Jos asiakkaalle toimitetaan olemassa olevaan osoitteeseen, jonka veroryhmä on jo konfiguroitu, käytetään aiemmin luotua veroryhmää.</span><span class="sxs-lookup"><span data-stu-id="64cee-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="64cee-124">Osoitteilla ei oletusarvoisesti ole veroryhmää, kun ne luodaan.</span><span class="sxs-lookup"><span data-stu-id="64cee-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="64cee-125">Yleisten arvonlisäveroryhmien konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="64cee-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="64cee-126">Voit konfiguroida yleiset arvonlisäveroryhmät Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="64cee-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="64cee-127">Siirry kohtaan **Vero \> Välilliset verot \> Arvonlisävero \> Arvonlisäveroryhmä**.</span><span class="sxs-lookup"><span data-stu-id="64cee-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="64cee-128">Valitse määritettävä veroryhmä vasemmasta siirtymisruudusta.</span><span class="sxs-lookup"><span data-stu-id="64cee-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="64cee-129">Määritä arvonlisäveroryhmän verot **Vähittäismyyntikohteeseen perustuva vero** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="64cee-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="64cee-130">Jos lähetykseen ei liity arvonlisäveroa asiakkaan osoitteeseen, rivin toimitusosoite sekä veroryhmälle määritetyt kohteeseen perustuvat verot määrittävät veroryhmän.</span><span class="sxs-lookup"><span data-stu-id="64cee-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="64cee-131">Lisätietoja on kohdassa [Määränpäähän perustuvien verojen määrittäminen online-myymälöille](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="64cee-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64cee-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="64cee-132">Additional resources</span></span>

[<span data-ttu-id="64cee-133">Arvonlisäveron laskeminen online-tilauksille</span><span class="sxs-lookup"><span data-stu-id="64cee-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
