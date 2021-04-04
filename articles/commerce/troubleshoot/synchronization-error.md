---
title: Oletusmaksupalveluun liittyvä tilauksen synkronointivirhe
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa korjaamaan online-tilauksen synkronoinnin yhteydessä mahdollisesti tapahtuvat virheet.
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585297"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="a5773-103">Oletusmaksupalveluun liittyvä tilauksen synkronointivirhe</span><span class="sxs-lookup"><span data-stu-id="a5773-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5773-104">Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa korjaamaan online-tilauksen synkronoinnin yhteydessä mahdollisesti tapahtuvat virheet.</span><span class="sxs-lookup"><span data-stu-id="a5773-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="a5773-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="a5773-105">Description</span></span>

<span data-ttu-id="a5773-106">Kun synkronoit online-tilauksen, näyttöön tulee seuraava virhesanoma: "Luottokorttitapahtumien käsittelemiseksi on oltava oletusmaksupalvelu."</span><span class="sxs-lookup"><span data-stu-id="a5773-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Puuttuva oletusmaksupalvelu -virhe](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="a5773-108">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="a5773-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="a5773-109">Commerce headquarters -oletusmaksupalvelun vahvistus tai asetus</span><span class="sxs-lookup"><span data-stu-id="a5773-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="a5773-110">Voit vahvistaa tai määrittää Commerce headquarters -oletusmaksupalvelun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a5773-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a5773-111">Siirry kohtaan **Myyntireskontra \> Maksujen asetukset \> Maksupalvelut**.</span><span class="sxs-lookup"><span data-stu-id="a5773-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="a5773-112">Varmista, että **Uusien luottokorttien oletuskäsittelijä** -asetukseksi on määritetty **Kyllä** yhdelle maksupalvelulle.</span><span class="sxs-lookup"><span data-stu-id="a5773-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5773-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a5773-113">Additional resources</span></span>

[<span data-ttu-id="a5773-114">Luottokorttien määrittäminen, varmennus ja tietojen tarkistus</span><span class="sxs-lookup"><span data-stu-id="a5773-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
