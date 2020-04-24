---
title: Jäljityksen käyttö hajotuksessa
description: Tässä artikkelissa kerrotaan, miten jäljitystä käytetään tilauksen hajotuksen tuloksen takana olevien syiden tutkimisessa.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 046d4f5270869542d33023b9b9c927e89f5ad40b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209510"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="11032-103">Jäljityksen käyttö hajotuksessa</span><span class="sxs-lookup"><span data-stu-id="11032-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11032-104">Tässä artikkelissa kerrotaan, miten jäljitystä käytetään tilauksen hajotuksen tuloksen takana olevien syiden tutkimisessa.</span><span class="sxs-lookup"><span data-stu-id="11032-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="11032-105">Kun otat jäljityksen käyttöön, voit tarkastella tietoja tietyn tilauksen hajotustulokseen vaikuttaneista tekijöistä.</span><span class="sxs-lookup"><span data-stu-id="11032-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="11032-106">Seuraavat esimerkit osoittavat, miten jäljitystietoja voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="11032-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="11032-107">Näytä suunniteltujen tilausten välisten toimintojen suhteet, jotta voit optimoida toimitusketjun ja varastovaraukset.</span><span class="sxs-lookup"><span data-stu-id="11032-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="11032-108">Näytä suhteet jo hyväksyttyihin tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="11032-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="11032-109">Voit kohdistaa automaattiseen johdettujen vaatimusten vahvistamiseen ja priorisoida sitten tilaukset tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="11032-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="11032-110">Simuloimalla suunnittelutulokset voit selvittää, ovatko suunnitteluparametreilla optimaalisia.</span><span class="sxs-lookup"><span data-stu-id="11032-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="11032-111">Tunnista, miten tiedot, kuten tilauksen tuotantopäivät, määrätä ja prioriteetit, määritettiin.</span><span class="sxs-lookup"><span data-stu-id="11032-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="11032-112">Voit tarkastella tietoja tulevasta ja valitun tilauksen toiminnoista.</span><span class="sxs-lookup"><span data-stu-id="11032-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="11032-113">Jäljitystiedot ovat saatavilla **Hajotus**-sivun **Selitys**-välilehden yläruudussa.</span><span class="sxs-lookup"><span data-stu-id="11032-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="11032-114">Jäljitys tapahtuu, kun tilaus hajotetaan.</span><span class="sxs-lookup"><span data-stu-id="11032-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="11032-115">Aloita tilauksen jäljitys valitsemalla ensin **Päivitys** ja sitten **Ota jäljitys käyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="11032-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="11032-116">Voit hakea lokista tietoja **Etsi teksti** -kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="11032-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="11032-117">Hakutulokset näkyvät korostettuina puurakenteessa.</span><span class="sxs-lookup"><span data-stu-id="11032-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="11032-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="11032-118">Additional resources</span></span>
--------

[<span data-ttu-id="11032-119">Pääsuunnitelmien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="11032-119">Master plans overview</span></span>](master-plans.md)



