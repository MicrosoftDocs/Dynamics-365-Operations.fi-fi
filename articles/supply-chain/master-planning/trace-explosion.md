---
title: "Jäljityksen käyttö hajotuksessa"
description: "Tässä artikkelissa kerrotaan, miten jäljitystä käytetään tilauksen hajotuksen tuloksen takana olevien syiden tutkimisessa."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3628e3f2d24bb41e83f544b20db4aff0e8e6deb7
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="use-tracing-for-explosion"></a><span data-ttu-id="fd1d1-103">Jäljityksen käyttö hajotuksessa</span><span class="sxs-lookup"><span data-stu-id="fd1d1-103">Use tracing for explosion</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fd1d1-104">Tässä artikkelissa kerrotaan, miten jäljitystä käytetään tilauksen hajotuksen tuloksen takana olevien syiden tutkimisessa.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="fd1d1-105">Kun otat jäljityksen käyttöön, voit tarkastella tietoja tietyn tilauksen hajotustulokseen vaikuttaneista tekijöistä.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="fd1d1-106">Seuraavat esimerkit osoittavat, miten jäljitystietoja voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="fd1d1-107">Näytä suunniteltujen tilausten välisten toimintojen suhteet, jotta voit optimoida toimitusketjun ja varastovaraukset.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="fd1d1-108">Näytä suhteet jo hyväksyttyihin tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="fd1d1-109">Voit kohdistaa automaattiseen johdettujen vaatimusten vahvistamiseen ja priorisoida sitten tilaukset tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="fd1d1-110">Simuloimalla suunnittelutulokset voit selvittää, ovatko suunnitteluparametreilla optimaalisia.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="fd1d1-111">Tunnista, miten tiedot, kuten tilauksen tuotantopäivät, määrätä ja prioriteetit, määritettiin.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="fd1d1-112">Voit tarkastella tietoja tulevasta ja valitun tilauksen toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="fd1d1-113">Jäljitystiedot ovat saatavilla **Hajotus**-sivun **Selitys**-välilehden yläruudussa.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="fd1d1-114">Jäljitys tapahtuu, kun tilaus hajotetaan.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="fd1d1-115">Aloita tilauksen jäljitys valitsemalla ensin **Päivitys** ja sitten **Ota jäljitys käyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="fd1d1-116">Voit hakea lokista tietoja **Etsi teksti** -kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="fd1d1-117">Hakutulokset näkyvät korostettuina puurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="fd1d1-117">Search results are highlighted in the tree.</span></span>

<a name="see-also"></a><span data-ttu-id="fd1d1-118">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="fd1d1-118">See also</span></span>
--------

[<span data-ttu-id="fd1d1-119">Pääsuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="fd1d1-119">Master plans</span></span>](master-plans.md)




