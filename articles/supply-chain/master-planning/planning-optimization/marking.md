---
title: Varastomerkintä suunnittelun optimoinnissa
description: Tässä aiheessa on tietoja vahvistettujen tilausten varaston merkintävaihtoehdoista suunnittelun optimointia käytettäessä.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 236e1955dd80564e748aab1c595b017cb78e9418
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983488"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="64d25-103">Varastomerkintä suunnittelun optimoinnissa</span><span class="sxs-lookup"><span data-stu-id="64d25-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64d25-104">Tässä aiheessa on tietoja vahvistettujen tilausten varaston merkintävaihtoehdoista suunnittelun optimointia käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="64d25-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="64d25-105">*Merkintää* käytetään linkittämään kysyntä ja tarjonta.</span><span class="sxs-lookup"><span data-stu-id="64d25-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="64d25-106">Se muistuttaa *tarvekohdistusta*, joka ilmaisee, miten pääsuunnittelun odotetaan kattavan kysynnän.</span><span class="sxs-lookup"><span data-stu-id="64d25-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="64d25-107">Suunnittelun kannalta suurin ero on siinä, että merkintä on pysyvämpää kuin tarvekohdistus.</span><span class="sxs-lookup"><span data-stu-id="64d25-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="64d25-108">Merkintä otettiin käyttöön tukemaan kustannuslaskennan FIFO- ja LIFO-erityisskenaarioita.</span><span class="sxs-lookup"><span data-stu-id="64d25-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="64d25-109">Sitä käytetään nyt kuitenkin myös joissakin muissa kuin kustannuslaskentaskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="64d25-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="64d25-110">Tarjonnan ja kysynnän välinen merkintä on valinnainen ja lähes pysyvä.</span><span class="sxs-lookup"><span data-stu-id="64d25-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="64d25-111">Käyttäjä voi poistaa merkinnän manuaalisesti tai se voidaan poistaa suorittamalla myyntitilauksen rivin hajotus, jossa **Poista merkintä** -vaihtoehto on valittu.</span><span class="sxs-lookup"><span data-stu-id="64d25-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="64d25-112">Tarvekohdistusta ohjataan pääsuunnittelulla kattavuuden aikana, ja sen avulla linkitetään kysyntä tarvittavaan tarjontaan.</span><span class="sxs-lookup"><span data-stu-id="64d25-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="64d25-113">Tarvekohdistus voidaan päivittää kullekin suunnitteluajolle, jolla optimoidaan kysynnän kattamiseen tarvittava tarjonta.</span><span class="sxs-lookup"><span data-stu-id="64d25-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="64d25-114">Kun pääsuunnittelu päivittää tarvekohdistustiedot, se noudattaa mahdollista aiemmin luotua merkintää.</span><span class="sxs-lookup"><span data-stu-id="64d25-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="64d25-115">Tarvekohdistus alkaa sisällyttämällä liittyvä merkintä, käytettävissä olevan varaston varaukset ja tilauksessa olevan varaston varaukset seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="64d25-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="64d25-116">Kysynnän ja tarjonnan välinen merkintä</span><span class="sxs-lookup"><span data-stu-id="64d25-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="64d25-117">Käytettävissä olevan varaston varaukset</span><span class="sxs-lookup"><span data-stu-id="64d25-117">On-hand reservations</span></span>
1. <span data-ttu-id="64d25-118">Tilauksessa olevan varaston varaukset</span><span class="sxs-lookup"><span data-stu-id="64d25-118">On-order reservations</span></span>

<span data-ttu-id="64d25-119">Kun vahvistat suunnitellun tilauksen, **Vahvistus**-valintaikkunan **Päivitä merkintä** -kentässä voi määrittää vahvistuksen aikana luotujen tilausten merkintävaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="64d25-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="64d25-120">Valitse jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="64d25-120">Select one of the following values:</span></span>

- <span data-ttu-id="64d25-121">**Ei** – varastomerkintää ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="64d25-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="64d25-122">**Vakio** – varastomerkintä päivitetään tarvekohdistuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="64d25-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="64d25-123">Tarvetilaus (kysyntä) merkitään täyttötilauksen (tarjonta) mukaan.</span><span class="sxs-lookup"><span data-stu-id="64d25-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="64d25-124">Jos täyttötilaukseen jää jäljelle jokin määrä, sitä ei merkitä ja viitetiedot jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="64d25-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="64d25-125">Jos esimerkiksi 100 kappaleen myyntitilaus tarvekohdistetaan 150 kappaleen ostotilaukseen, viitetiedot määritetään vain myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="64d25-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="64d25-126">**Laajennettu** – sekä tarvetilaus (kysyntä) että täyttötilaus (tarjonta) merkitään riippumatta siitä, jääkö täyttötilaukseen jäljelle jokin määrä.</span><span class="sxs-lookup"><span data-stu-id="64d25-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="64d25-127">Jos esimerkiksi 100 kappaleen myyntitilaus tarvekohdistetaan 150 kappaleen ostotilaukseen, viitetiedot määritetään sekä myyntitilaukseen tai ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="64d25-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>
