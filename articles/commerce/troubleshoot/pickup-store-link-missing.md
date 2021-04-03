---
title: Nouda tämä -vaihtoehtoa ei ole näkyvissä ostoskori- tai tuotetietosivuilla
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, että myymälästä noudon vaihtoehto ei näy ostoskorisivulla tai tuotteen tietosivuilla.
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
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585300"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="8e15c-103">Nouda tämä -vaihtoehtoa ei ole näkyvissä ostoskori- tai tuotetietosivuilla</span><span class="sxs-lookup"><span data-stu-id="8e15c-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e15c-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa siinä, että myymälästä noudon vaihtoehto ei näy ostoskorisivulla tai tuotteen tietosivuilla.</span><span class="sxs-lookup"><span data-stu-id="8e15c-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="8e15c-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8e15c-105">Description</span></span>

<span data-ttu-id="8e15c-106">**Nouda tämä** -vaihtoehtoa ei ole näkyvissä ostoskorisivulla tai tuotetietosivuilla.</span><span class="sxs-lookup"><span data-stu-id="8e15c-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="8e15c-107">Seuraavassa kuvassa on esimerkki sivusta, joka sisältää **Nouda tämä** -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="8e15c-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Nouda tämä -painike](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="8e15c-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8e15c-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="8e15c-110">Ota BOPIS-laajennus käyttöön Commerce sivustonmuodostimessa</span><span class="sxs-lookup"><span data-stu-id="8e15c-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="8e15c-111">Ota "Osta verkosta, nouda myymälästä" (BOPIS) -laajennus käyttöön Commerce sivustonmuodostimessa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="8e15c-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8e15c-112">Valitse sivusto.</span><span class="sxs-lookup"><span data-stu-id="8e15c-112">Select your site.</span></span>
1. <span data-ttu-id="8e15c-113">Valitse **Sivuston asetukset** ja valitse sitten **Laajennukset**.</span><span class="sxs-lookup"><span data-stu-id="8e15c-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="8e15c-114">Varmista, että **Poista BOPIS** -valinta on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="8e15c-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="8e15c-115">Toimitustapojen konfiguroiminen Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="8e15c-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="8e15c-116">Voit määrittää toimitustavat Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8e15c-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8e15c-117">Siirry kohtaan **Hankinta \> Asetukset \> Toimitustavat**.</span><span class="sxs-lookup"><span data-stu-id="8e15c-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="8e15c-118">Varmista, että **Asiakkaan nouto** -toimitustapa on luotu ja että siihen on liitetty tuotteet ja osoitteet.</span><span class="sxs-lookup"><span data-stu-id="8e15c-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="8e15c-119">Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8e15c-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="8e15c-120">Valitse vasemmassa siirtymisruudussa **Asiakastilaukset**.</span><span class="sxs-lookup"><span data-stu-id="8e15c-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="8e15c-121">Varmista, että **Noutotoimitustapa** on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="8e15c-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="8e15c-122">Asiakastilausmaksujen konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="8e15c-122">Configure customer orders payments</span></span>

<span data-ttu-id="8e15c-123">Voit konfiguroida asiakastilausten maksut Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8e15c-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8e15c-124">Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8e15c-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="8e15c-125">Valitse vasemmassa siirtymisruudussa **Asiakastilaukset**.</span><span class="sxs-lookup"><span data-stu-id="8e15c-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="8e15c-126">Varmista **Maksut**-pikavälilehdellä, että **Maksuehdot**- ja **Maksutapa**-kentät on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="8e15c-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e15c-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8e15c-127">Additional resources</span></span>

[<span data-ttu-id="8e15c-128">Määritä BOPIS</span><span class="sxs-lookup"><span data-stu-id="8e15c-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="8e15c-129">Useiden noutotoimitustapojen ottaminen käyttöön asiakastilauksille</span><span class="sxs-lookup"><span data-stu-id="8e15c-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="8e15c-130">Monikanavaisten Commerce-tilausten maksut</span><span class="sxs-lookup"><span data-stu-id="8e15c-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="8e15c-131">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="8e15c-131">Store selector module</span></span>](../store-selector.md)
