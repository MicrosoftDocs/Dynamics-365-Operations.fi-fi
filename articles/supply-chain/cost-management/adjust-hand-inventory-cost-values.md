---
title: "Käytettävissä olevan varaston kustannusarvojen oikaiseminen"
description: "Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 78a97e1ff893ecfb864052b79e56ad48efa5191c
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="f2960-103">Käytettävissä olevan varaston kustannusarvojen oikaiseminen</span><span class="sxs-lookup"><span data-stu-id="f2960-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2960-104">Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f2960-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="f2960-105">**Käytettävissä olevan varaston oikaisu** -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f2960-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="f2960-106">**Huomautus**: Voit avata **Päätös ja oikaisu** -sivun **Käytettävissä olevan varaston oikaisu** -sivulla tietueen valmiiden varaston sulkemisprosessien tietueen ja siirtyä sitten kohtaan **Oikaisu** &gt; **Varastosaldo**.</span><span class="sxs-lookup"><span data-stu-id="f2960-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="f2960-107">**Esimerkki:** Helmikuussa suoritetaan seuraavat tapahtumat:</span><span class="sxs-lookup"><span data-stu-id="f2960-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="f2960-108">1. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 2, kustannus 10,00 €</span><span class="sxs-lookup"><span data-stu-id="f2960-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="f2960-109">5. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 1, kustannus 13,00 €</span><span class="sxs-lookup"><span data-stu-id="f2960-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="f2960-110">19. helmikuuta: rahoituksellinen varasto-otto, määrä 1, juokseva keskimääräinen kustannus 11,00 €.</span><span class="sxs-lookup"><span data-stu-id="f2960-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="f2960-111">Tämä nimike on määritetty FIFO-varastomallilla ja varaston sulkeminen suoritettiin 28.2.</span><span class="sxs-lookup"><span data-stu-id="f2960-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="f2960-112">Rahoituksellinen tapahtumaotto 11,00 $ täsmäytetään vasten rahoituksellista vastaanottoa, jonka päivämäärä on 1.2. Tehdään oikaisu, jonka arvo on 1,00 $.</span><span class="sxs-lookup"><span data-stu-id="f2960-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="f2960-113">Tämän jälkeen seuraavat varaston vastaanotot sisältävät avoimia varastomääriä:</span><span class="sxs-lookup"><span data-stu-id="f2960-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="f2960-114">1. helmikuuta: Määrä 1 ja kustannus 10,00 €</span><span class="sxs-lookup"><span data-stu-id="f2960-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="f2960-115">5. helmikuuta: Määrä 1 ja kustannus 13,00 €</span><span class="sxs-lookup"><span data-stu-id="f2960-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="f2960-116">Voit määrittää näiden kahden nimikkeen kustannukseksi 15,00 Yhdysvaltain dollaria oikaisemalla avoimen käytettävissä olevan varaston edellisestä varaston sulkemisesta lähtien.</span><span class="sxs-lookup"><span data-stu-id="f2960-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="f2960-117">**Huomautus:** Käytettävissä olevan varaston oikaisutapahtuman kirjauspäivämäärä on edellinen varaston sulkemispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="f2960-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="f2960-118">Tätä päivämäärää ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="f2960-118">This date can't be modified.</span></span>

