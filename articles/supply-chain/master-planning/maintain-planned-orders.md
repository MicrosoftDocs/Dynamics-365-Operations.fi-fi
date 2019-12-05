---
title: Ylläpidä suunniteltuja tilauksia
description: Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja. Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813773"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="b6e67-104">Ylläpidä suunniteltuja tilauksia</span><span class="sxs-lookup"><span data-stu-id="b6e67-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6e67-105">Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="b6e67-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="b6e67-106">Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.</span><span class="sxs-lookup"><span data-stu-id="b6e67-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="b6e67-107">Voit hallita suunniteltuja tilauksia **Pääsuunnittelu**-työtilassa, **Suunniteltu tilaus** -luettelossa tai **Suunnitellut tuotantotilaukset**-, **Suunnitellut ostotilaukset**- ja **Suunniteltu siirto** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b6e67-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="b6e67-108">Suunnitellun tilauksen tila</span><span class="sxs-lookup"><span data-stu-id="b6e67-108">Planned order status</span></span>
<span data-ttu-id="b6e67-109">Voit seurata edistymistä **Tila**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b6e67-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="b6e67-110">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b6e67-110">The following values are used:</span></span>

-   <span data-ttu-id="b6e67-111">Kun pääsuunnittelu luo suunniteltuja tilauksia, suunniteltujen tilausten tilana on **Käsittelemätön**.</span><span class="sxs-lookup"><span data-stu-id="b6e67-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="b6e67-112">Jos et halua vahvistaa suunniteltua tilausta, voit asettaa sen tilaksi **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="b6e67-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="b6e67-113">Jos haluat vahvistaa suunnitellun tilauksen, voit muuttaa tilaksi **Hyväksytty**.</span><span class="sxs-lookup"><span data-stu-id="b6e67-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="b6e67-114">Pääsuunnittelu noudattaa suunniteltuja tilauksia, joiden tila on **Hyväksytty**, joten niitä ei muokata tai poisteta myöhemmän pääsuunnitteluajon aikana.</span><span class="sxs-lookup"><span data-stu-id="b6e67-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="b6e67-115">Suunniteltujen tilausten vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="b6e67-115">Firming planned orders</span></span> 
<span data-ttu-id="b6e67-116">Vahvistettaessa suunniteltuja tilauksia luodaan todelliset tilaukset.</span><span class="sxs-lookup"><span data-stu-id="b6e67-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="b6e67-117">Nämä tunnetaan myös nimellä *vapautetut* tai *avoimet* tilaukset.</span><span class="sxs-lookup"><span data-stu-id="b6e67-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="b6e67-118">Kun suunniteltu tilaus on vahvistettu, se siirtyy kyseisen moduulin tilausosaan.</span><span class="sxs-lookup"><span data-stu-id="b6e67-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="b6e67-119">Voit valita kaksi vahvistusvaihtoehtoa **Suunnitellut tila ukset** -sivulta:</span><span class="sxs-lookup"><span data-stu-id="b6e67-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="b6e67-120">**Vahvista** – tämä vahvistaa yhden tai useita valittuja suunniteltuja tilauksia.</span><span class="sxs-lookup"><span data-stu-id="b6e67-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="b6e67-121">**Vahvista kaikki** – tämä vahvistaa suodattimen kaikki suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="b6e67-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="b6e67-122">Käyttämällä **Vahvista kaikki** -toimintoa sinun ei tarvitse valita suunniteltua tilausta, kaikki suodattimen sisällä olevat suunnitellut tilaukset vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="b6e67-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="b6e67-123">Tämä vaihtoehto voi olla hyödyllinen, jos olet vahvistamassa suunniteltujen tilausten suurta määrää.</span><span class="sxs-lookup"><span data-stu-id="b6e67-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="b6e67-124">Voit **vahvistushistoriassa** jäljittää suunnitellun tilauksen, joka on vahvistettu kohdassa **Suunnitellut tilaukset -lomake > Näytä > Vahvistushistoria**.</span><span class="sxs-lookup"><span data-stu-id="b6e67-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="b6e67-125">Rinnakkaisvahvistus</span><span class="sxs-lookup"><span data-stu-id="b6e67-125">Parallelize firming</span></span>
<span data-ttu-id="b6e67-126">Jos aiot vahvistaa useita tilauksia samalla kertaa, suorituksen rinnakkaisuus voi parantaa ajoaikaa tai suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="b6e67-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="b6e67-127">Tämä vaihtoehto on käytettävissä vahvistettaessa useita suunniteltuja tilauksia joko **Vahvista**- tai **Vahvista kaikki** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="b6e67-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="b6e67-128">Seuraavat parametrit ovat käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="b6e67-128">The following parameters are available:</span></span>

-   <span data-ttu-id="b6e67-129">**Rinnakkainen vahvistus** – jos **Kyllä**, vahvistusprosessista tehdään rinnakkainen hyödyntämällä **Säikeiden määrä** -kohdassa määritettyä säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="b6e67-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="b6e67-130">**Säikeiden määrä** – määrittää vahvistusprosessin rinnakkaisten säikeiden määrän.</span><span class="sxs-lookup"><span data-stu-id="b6e67-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="b6e67-131">Parametri näkyy vain, kun **Rinnakkainen vahvistus** -arvoksi on määritetty **Kyllä.**</span><span class="sxs-lookup"><span data-stu-id="b6e67-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="b6e67-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b6e67-132">Additional resources</span></span>
--------

[<span data-ttu-id="b6e67-133">Pääsuunnitelmien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b6e67-133">Master plans overview</span></span>](master-plans.md)



