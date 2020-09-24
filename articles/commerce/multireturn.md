---
title: Nimikkeiden palauttaminen useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä aiheessa kuvataan Dynamics 365 Commercen toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760247"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="c8ba8-103">Nimikkeiden palauttaminen useista eri asiakkaan ostotilauksista ja laskuista</span><span class="sxs-lookup"><span data-stu-id="c8ba8-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="c8ba8-104">Tässä artikkelissa kuvataan kaksi ominaisuutta, jotka optimoivat asiakastilausten palautukset useista laskuista.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="c8ba8-105">Salli palautukset useista tietojen tallennuksista</span><span class="sxs-lookup"><span data-stu-id="c8ba8-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="c8ba8-106">Tämän ominaisuuden avulla samasta asiakastilauksesta voi tehdä useita linkitettyjä palautuksia.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="c8ba8-107">Siirry **Ominaisuuksien hallinta** -työtilaan ja tee haku hakusanoilla **Salli palautukset useista tietojen tallennuksista**.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="c8ba8-108">Valitse **Ota käyttöön palautukset useista tilauksista** ja valitse sitten **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="c8ba8-109">Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille</span><span class="sxs-lookup"><span data-stu-id="c8ba8-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="c8ba8-110">Tämä ominaisuus varmistaa, että kun tilaus palautetaan käyttäen useaa laskua, verot täsmäävät alun perin veloitetun verosumman kanssa.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="c8ba8-111">Siirry **Ominaisuuksien hallinta** -työtilaan ja tee haku hakusanoilla **Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille**.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="c8ba8-112">Valitse **Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille** ja valitse sitten **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="c8ba8-113">Palautusten käsittely</span><span class="sxs-lookup"><span data-stu-id="c8ba8-113">Process returns</span></span>

<span data-ttu-id="c8ba8-114">Kun nämä ominaisuudet on otettu käyttöön ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="c8ba8-115">Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="c8ba8-116">Kassanhoitaja voi tällöin valita palautettavat tuotteet.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="c8ba8-117">Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="c8ba8-118">Jos tilaus palautetaan kokonaan, asiakkaalle palautettujen verojen summa on sama kuin alun perin veloitettu verosumma.</span><span class="sxs-lookup"><span data-stu-id="c8ba8-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

