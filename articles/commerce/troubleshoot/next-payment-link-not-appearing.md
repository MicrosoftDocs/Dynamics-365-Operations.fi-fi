---
title: Tallenna seuraavaa maksua varten -vaihtoehto ei tule näkyviin
description: Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa siinä, kun Tallenna seuraavaa maksua varten -valintaruutu ei näy sähköisen kaupankäynnin sivuston kassasivun Maksutapa-kohdassa.
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018431"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="83c7f-103">Tallenna seuraavaa maksua varten -vaihtoehto ei tule näkyviin</span><span class="sxs-lookup"><span data-stu-id="83c7f-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83c7f-104">Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa siinä, kun **Tallenna seuraavaa maksua varten** -valintaruutu ei näy sähköisen kaupankäynnin sivuston kassasivun **Maksutapa**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="83c7f-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="83c7f-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="83c7f-105">Description</span></span>

<span data-ttu-id="83c7f-106">**Tallenna seuraavaa maksua varten** -valintaruutu ei näy sähköisen kaupankäynnin sivuston kassasivun **Maksutapa**-osassa.</span><span class="sxs-lookup"><span data-stu-id="83c7f-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="83c7f-107">Seuraavassa kuvassa on esimerkki kassasivusta, joka sisältää **Tallenna seuraavaa maksua varten** -valintaruudun.</span><span class="sxs-lookup"><span data-stu-id="83c7f-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Tallenna seuraavaa maksua varten -valintaruutu maksumoduulissa](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="83c7f-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="83c7f-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="83c7f-110">Tarkista, että Dynamics 365 Payment Connector Adyenia varten on määritetty oikein Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="83c7f-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="83c7f-111">Voit tarkistaa, että Dynamics 365 Payment Connector Adyenia varten on määritetty oikein Commerce headquarters -sovelluksessa, toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="83c7f-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="83c7f-112">Valitse **Retail ja Commerce \> Kanavat \> Verkkokaupat**.</span><span class="sxs-lookup"><span data-stu-id="83c7f-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="83c7f-113">Valitse verkkokauppa.</span><span class="sxs-lookup"><span data-stu-id="83c7f-113">Select the online store.</span></span>
1. <span data-ttu-id="83c7f-114">Varmista **Maksutilit**-pikavälilehdessä, että **Salli maksutietojen tallentaminen verkkokaupassa** -kentän arvoksi on määritetty **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="83c7f-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Salli maksutietojen tallentaminen verkkokaupassa -kenttä Commerce headquartersissa](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="83c7f-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="83c7f-116">Additional resources</span></span>

[<span data-ttu-id="83c7f-117">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="83c7f-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="83c7f-118">Online-maksuvälineiden tallentaminen Adyen-yhdistimen avulla</span><span class="sxs-lookup"><span data-stu-id="83c7f-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
