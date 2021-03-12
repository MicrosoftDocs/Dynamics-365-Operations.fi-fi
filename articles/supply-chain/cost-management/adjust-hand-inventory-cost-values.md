---
title: Käytettävissä olevan varaston kustannusarvojen oikaiseminen
description: Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a702a083d60bdb289712027fbaee5c0a72e60cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963835"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="2d67e-103">Käytettävissä olevan varaston kustannusarvojen oikaiseminen</span><span class="sxs-lookup"><span data-stu-id="2d67e-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d67e-104">Käytettävissä olevan varaston oikaisu -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="2d67e-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="2d67e-105">**Käytettävissä olevan varaston oikaisu** -sivulla voit oikaista käytettävissä olevan varaston määrien kustannusarvoa varaston sulkemisprosessin suorituksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="2d67e-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="2d67e-106">**Huomautus:** **Käytettävissä olevan varaston oikaisu** -sivu avataan **Päätös ja oikaisu** -sivulla valitsemalla valmiin varaston sulkemisprosessin tietue ja valitsemalla sitten **Oikaisu** &gt; **Varastosaldo**.</span><span class="sxs-lookup"><span data-stu-id="2d67e-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="2d67e-107">**Esimerkki:** Helmikuussa suoritetaan seuraavat tapahtumat:</span><span class="sxs-lookup"><span data-stu-id="2d67e-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="2d67e-108">1. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 2, kustannus 10,00 €</span><span class="sxs-lookup"><span data-stu-id="2d67e-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="2d67e-109">5. helmikuuta: varaston rahoituksellinen vastaanotto, määrä 1, kustannus 13,00 €</span><span class="sxs-lookup"><span data-stu-id="2d67e-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="2d67e-110">19. helmikuuta: rahoituksellinen varasto-otto, määrä 1, juokseva keskimääräinen kustannus 11,00 €.</span><span class="sxs-lookup"><span data-stu-id="2d67e-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="2d67e-111">Tämä nimike on määritetty FIFO-varastomallilla ja varaston sulkeminen suoritettiin 28.2.</span><span class="sxs-lookup"><span data-stu-id="2d67e-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="2d67e-112">Rahoituksellinen tapahtumaotto 11,00 $ täsmäytetään vasten rahoituksellista vastaanottoa, jonka päivämäärä on 1.2. Tehdään oikaisu, jonka arvo on 1,00 $.</span><span class="sxs-lookup"><span data-stu-id="2d67e-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="2d67e-113">Tämän jälkeen seuraavat varaston vastaanotot sisältävät avoimia varastomääriä:</span><span class="sxs-lookup"><span data-stu-id="2d67e-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="2d67e-114">1. helmikuuta: Määrä 1 ja kustannus 10,00 €</span><span class="sxs-lookup"><span data-stu-id="2d67e-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="2d67e-115">5. helmikuuta: Määrä 1 ja kustannus 13,00 €</span><span class="sxs-lookup"><span data-stu-id="2d67e-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="2d67e-116">Voit määrittää näiden kahden nimikkeen kustannukseksi 15,00 Yhdysvaltain dollaria oikaisemalla avoimen käytettävissä olevan varaston edellisestä varaston sulkemisesta lähtien.</span><span class="sxs-lookup"><span data-stu-id="2d67e-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="2d67e-117">**Huomautus:** Käytettävissä olevan varaston oikaisutapahtuman kirjauspäivämäärä on edellinen varaston sulkemispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="2d67e-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="2d67e-118">Tätä päivämäärää ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="2d67e-118">This date can't be modified.</span></span>
