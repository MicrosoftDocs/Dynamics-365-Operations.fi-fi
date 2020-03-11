---
title: Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä aiheessa kuvataan Dynamics 365 Commercen toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004455"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="913af-103">Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista</span><span class="sxs-lookup"><span data-stu-id="913af-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="913af-104">Palautuksia voidaan tehdä useista eri asiakkaan ostotilauksista ja laskuista.</span><span class="sxs-lookup"><span data-stu-id="913af-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="913af-105">Määritä Commerce tukemaan palautuksia useista asiakkaan ostotilauksista ja laskuista.</span><span class="sxs-lookup"><span data-stu-id="913af-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="913af-106">Siirry kohtaan **Kaupan parametrit \> Asiakastilaukset**.</span><span class="sxs-lookup"><span data-stu-id="913af-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="913af-107">Ota käyttöön **Mahdollista palautukset useille ostotilauksille** -parametri.</span><span class="sxs-lookup"><span data-stu-id="913af-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="913af-108">Palautusten käsittely</span><span class="sxs-lookup"><span data-stu-id="913af-108">Process returns</span></span>

<span data-ttu-id="913af-109">Sen jälkeen, kun parametri on käytössä ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.</span><span class="sxs-lookup"><span data-stu-id="913af-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="913af-110">Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta.</span><span class="sxs-lookup"><span data-stu-id="913af-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="913af-111">Kassanhoitaja voi tällöin valita palautettavat tuotteet.</span><span class="sxs-lookup"><span data-stu-id="913af-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="913af-112">Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.</span><span class="sxs-lookup"><span data-stu-id="913af-112">A single return order will be created for all the selected products.</span></span>