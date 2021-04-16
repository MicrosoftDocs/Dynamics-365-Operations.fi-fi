---
title: Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä
description: Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa silloin, kun Maksutapa-osaa ei ladata, ja näyttöön tulee virhesanoma.
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
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801768"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="65200-103">Luottokortin merkintäsivulla näkyy virhe uloskuittauksen yhteydessä</span><span class="sxs-lookup"><span data-stu-id="65200-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65200-104">Tässä aiheessa on vianmääritysohjeita, jotka voivat auttaa silloin, kun **Maksutapa**-osaa ei ladata, ja näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="65200-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="65200-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="65200-105">Description</span></span>

<span data-ttu-id="65200-106">Kun avaat online-myymälän kassasivun,**Maksutapa**-osaa ei ladata, ja näyttöön tulee seuraava virhesanoma: "Jokin meni vikaan.</span><span class="sxs-lookup"><span data-stu-id="65200-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="65200-107">Yritä myöhemmin uudelleen."</span><span class="sxs-lookup"><span data-stu-id="65200-107">Please try again later."</span></span>

![Maksumoduulin virhe](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="65200-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="65200-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="65200-110">Odota Commerce Scale Unit -välimuistin vanhentumista</span><span class="sxs-lookup"><span data-stu-id="65200-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="65200-111">Verkkokaupan kassasivun maksupalvelun asetukset tallennetaan välimuistiin Commerce Scale Unitissa, ja niiden näkyminen sähköisen kaupan sivustossa voi kestää 15 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="65200-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="65200-112">Nämä maksupalvelun asetukset sisältävät muutoksia myyjätilin tunnukseen, pilvipalvelun API-avaimeen ja erilaisiin maksutapaan liittyviin konfigurointiasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="65200-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65200-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="65200-113">Additional resources</span></span>

[<span data-ttu-id="65200-114">Online-kanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="65200-114">Set up an online channel</span></span>](../channel-setup-online.md)
