---
title: Maksut selvitetään automaattisesti, ennen kuin tilaukset laskutetaan tai lähetetään
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585303"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="1770c-103">Maksut selvitetään automaattisesti, ennen kuin tilaukset laskutetaan tai lähetetään</span><span class="sxs-lookup"><span data-stu-id="1770c-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1770c-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.</span><span class="sxs-lookup"><span data-stu-id="1770c-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="1770c-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1770c-105">Description</span></span>

<span data-ttu-id="1770c-106">Maksu selvitetään Adyen-portaalissa heti tilauksen tekemisen jälkeen, vaikka myyntitilausta ei ole laskutettu eikä lähetetty.</span><span class="sxs-lookup"><span data-stu-id="1770c-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="1770c-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="1770c-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="1770c-108">Sähköisen kaupankäynnin maksujen manuaalisen sieppauksen konfiguroiminen Adyen-portaalissa</span><span class="sxs-lookup"><span data-stu-id="1770c-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="1770c-109">Voit konfiguroida sähköisen kaupankäynnin maksujen manuaalisen sieppauksen Adyen-portaalissa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1770c-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="1770c-110">Kirjaudu Adyen-portaaliin.</span><span class="sxs-lookup"><span data-stu-id="1770c-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="1770c-111">Valitse oikeasta yläkulmasta sähköisen kaupankäynnin kanavan myyjätilisi.</span><span class="sxs-lookup"><span data-stu-id="1770c-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="1770c-112">Valitse yläreunan siirtymispalkissa **Tili** ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="1770c-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="1770c-113">Valitse **Siepausviive**-kentästä **manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="1770c-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Siepausviive-asetus Adyen-portaalissa](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="1770c-115">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1770c-115">Additional resources</span></span>

[<span data-ttu-id="1770c-116">Adyen-maksun sieppaus</span><span class="sxs-lookup"><span data-stu-id="1770c-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="1770c-117">Dynamics 365 -maksuyhdistin Adyenia varten</span><span class="sxs-lookup"><span data-stu-id="1770c-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="1770c-118">Dynamics 365:n Adyen-maksuyhdistimen määritys</span><span class="sxs-lookup"><span data-stu-id="1770c-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)