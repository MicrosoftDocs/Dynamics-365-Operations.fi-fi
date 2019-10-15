---
title: Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä aiheessa kuvataan Dynamics 365 Retailin toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017986"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="439f2-103">Nimikkeiden palauttaminen useista eri asiakkaan ostotilauksista ja laskuista</span><span class="sxs-lookup"><span data-stu-id="439f2-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="439f2-104">Palautuksia voidaan tehdä useista eri asiakkaan ostotilauksista ja laskuista.</span><span class="sxs-lookup"><span data-stu-id="439f2-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="439f2-105">Määritä Retail tukemaan palautuksia useista asiakkaan ostotilauksista ja laskuista.</span><span class="sxs-lookup"><span data-stu-id="439f2-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="439f2-106">Siirry kohtaan **Vähittäismyynnin parametrit \> Asiakastilaukset**.</span><span class="sxs-lookup"><span data-stu-id="439f2-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="439f2-107">Ota käyttöön **Mahdollista palautukset useille ostotilauksille** -parametri.</span><span class="sxs-lookup"><span data-stu-id="439f2-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="439f2-108">Palautusten käsittely</span><span class="sxs-lookup"><span data-stu-id="439f2-108">Process returns</span></span>

<span data-ttu-id="439f2-109">Sen jälkeen, kun parametri on käytössä ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.</span><span class="sxs-lookup"><span data-stu-id="439f2-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="439f2-110">Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta.</span><span class="sxs-lookup"><span data-stu-id="439f2-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="439f2-111">Kassanhoitaja voi tällöin valita palautettavat tuotteet.</span><span class="sxs-lookup"><span data-stu-id="439f2-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="439f2-112">Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.</span><span class="sxs-lookup"><span data-stu-id="439f2-112">A single return order will be created for all the selected products.</span></span>
