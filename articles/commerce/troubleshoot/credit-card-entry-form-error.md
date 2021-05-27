---
title: Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä
description: Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa silloin, kun Maksutapa-osaa ei ladata, ja näyttöön tulee virhesanoma.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018503"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="f8a7a-103">Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä</span><span class="sxs-lookup"><span data-stu-id="f8a7a-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8a7a-104">Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa silloin, kun **Maksutapa**-osaa ei ladata, ja näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="f8a7a-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="f8a7a-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="f8a7a-105">Description</span></span>

<span data-ttu-id="f8a7a-106">Kun avaat online-myymälän kassasivun,**Maksutapa**-osaa ei ladata, ja näyttöön tulee seuraava virhesanoma: "Jokin meni vikaan.</span><span class="sxs-lookup"><span data-stu-id="f8a7a-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="f8a7a-107">Yritä myöhemmin uudelleen."</span><span class="sxs-lookup"><span data-stu-id="f8a7a-107">Please try again later."</span></span>

![Maksumoduulin virhe](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="f8a7a-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f8a7a-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="f8a7a-110">Odota Commerce Scale Unit -välimuistin vanhentumista</span><span class="sxs-lookup"><span data-stu-id="f8a7a-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="f8a7a-111">Verkkokaupan kassasivun maksupalvelun asetukset tallennetaan välimuistiin Commerce Scale Unitissa, ja niiden näkyminen sähköisen kaupan sivustossa voi kestää 15 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="f8a7a-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="f8a7a-112">Nämä maksupalvelun asetukset sisältävät muutoksia myyjätilin tunnukseen, pilvipalvelun API-avaimeen ja erilaisiin maksutapaan liittyviin konfigurointiasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="f8a7a-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8a7a-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f8a7a-113">Additional resources</span></span>

[<span data-ttu-id="f8a7a-114">Online-kanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8a7a-114">Set up an online channel</span></span>](../channel-setup-online.md)
