---
title: Jäljityksen käyttö hajotuksessa
description: Tässä artikkelissa kerrotaan, miten jäljitystä käytetään tilauksen hajotuksen tuloksen takana olevien syiden tutkimisessa.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f2821eb6a17d2caaacf399f8d519e4caf3ecd04
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813658"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="88454-103">Jäljityksen käyttö hajotuksessa</span><span class="sxs-lookup"><span data-stu-id="88454-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88454-104">Tässä artikkelissa kerrotaan, miten jäljitystä käytetään tilauksen hajotuksen tuloksen takana olevien syiden tutkimisessa.</span><span class="sxs-lookup"><span data-stu-id="88454-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="88454-105">Kun otat jäljityksen käyttöön, voit tarkastella tietoja tietyn tilauksen hajotustulokseen vaikuttaneista tekijöistä.</span><span class="sxs-lookup"><span data-stu-id="88454-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="88454-106">Seuraavat esimerkit osoittavat, miten jäljitystietoja voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="88454-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="88454-107">Näytä suunniteltujen tilausten välisten toimintojen suhteet, jotta voit optimoida toimitusketjun ja varastovaraukset.</span><span class="sxs-lookup"><span data-stu-id="88454-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="88454-108">Näytä suhteet jo hyväksyttyihin tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="88454-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="88454-109">Voit kohdistaa automaattiseen johdettujen vaatimusten vahvistamiseen ja priorisoida sitten tilaukset tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="88454-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="88454-110">Simuloimalla suunnittelutulokset voit selvittää, ovatko suunnitteluparametreilla optimaalisia.</span><span class="sxs-lookup"><span data-stu-id="88454-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="88454-111">Tunnista, miten tiedot, kuten tilauksen tuotantopäivät, määrätä ja prioriteetit, määritettiin.</span><span class="sxs-lookup"><span data-stu-id="88454-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="88454-112">Voit tarkastella tietoja tulevasta ja valitun tilauksen toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="88454-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="88454-113">Jäljitystiedot ovat saatavilla **Hajotus**-sivun **Selitys**-välilehden yläruudussa.</span><span class="sxs-lookup"><span data-stu-id="88454-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="88454-114">Jäljitys tapahtuu, kun tilaus hajotetaan.</span><span class="sxs-lookup"><span data-stu-id="88454-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="88454-115">Aloita tilauksen jäljitys valitsemalla ensin **Päivitys** ja sitten **Ota jäljitys käyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="88454-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="88454-116">Voit hakea lokista tietoja **Etsi teksti** -kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="88454-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="88454-117">Hakutulokset näkyvät korostettuina puurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="88454-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="88454-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="88454-118">Additional resources</span></span>
--------

[<span data-ttu-id="88454-119">Pääsuunnitelmien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="88454-119">Master plans overview</span></span>](master-plans.md)



