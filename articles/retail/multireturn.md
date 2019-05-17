---
title: Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä aiheessa kuvataan ohjelman Microsoft Dynamics 365 for Retail toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
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
ms.openlocfilehash: d410fde2cd127f8d644e6a385937b6bc98d74576
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517055"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="ad257-103">Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista</span><span class="sxs-lookup"><span data-stu-id="ad257-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="ad257-104">Dynamics 365 for Finance and Operations -ohjelman versiossa 10.0 palautuksia voidaan tehdä useista ostotilauksista ja laskuista, kun versiota 10.0 edeltävissä ohjelmaversioissa palautuksia voitiin käsitellä ainoastaan yksi lasku kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="ad257-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="ad257-105">Konfiguroi Retail tukemaan palautuksia useista asiakkaan ostotilauksista ja laskuista.</span><span class="sxs-lookup"><span data-stu-id="ad257-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="ad257-106">Siirry **Retail parametrit \> Asiakastilaukset**.</span><span class="sxs-lookup"><span data-stu-id="ad257-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="ad257-107">Ota käyttöön **Mahdollista palautukset useille ostotilauksille** -parametri.</span><span class="sxs-lookup"><span data-stu-id="ad257-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="ad257-108">Palautusten käsittely</span><span class="sxs-lookup"><span data-stu-id="ad257-108">Process returns</span></span>

<span data-ttu-id="ad257-109">Sen jälkeen, kun parametri on käytössä ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.</span><span class="sxs-lookup"><span data-stu-id="ad257-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="ad257-110">Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta.</span><span class="sxs-lookup"><span data-stu-id="ad257-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="ad257-111">Kassanhoitaja voi tällöin valita palautettavat tuotteet.</span><span class="sxs-lookup"><span data-stu-id="ad257-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="ad257-112">Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.</span><span class="sxs-lookup"><span data-stu-id="ad257-112">A single return order will be created for all the selected products.</span></span>
