---
title: Ylläpidä suunniteltuja tilauksia
description: Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja. Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 039fce86ac9649989df1eaa6179c79dd98b8ae3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967060"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="9e1c3-104">Ylläpidä suunniteltuja tilauksia</span><span class="sxs-lookup"><span data-stu-id="9e1c3-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e1c3-105">Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="9e1c3-106">Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="9e1c3-107">Voit hallita suunniteltuja tilauksia **Pääsuunnittelu**-työtilassa, **Suunniteltu tilaus** -luettelossa tai **Suunnitellut tuotantotilaukset**-, **Suunnitellut ostotilaukset**- ja **Suunniteltu siirto** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="9e1c3-108">Suunnitellun tilauksen tila</span><span class="sxs-lookup"><span data-stu-id="9e1c3-108">Planned order status</span></span>
<span data-ttu-id="9e1c3-109">Voit seurata edistymistä **Tila**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="9e1c3-110">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="9e1c3-110">The following values are used:</span></span>

-   <span data-ttu-id="9e1c3-111">Kun pääsuunnittelu luo suunniteltuja tilauksia, suunniteltujen tilausten tilana on **Käsittelemätön**.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="9e1c3-112">Jos et halua vahvistaa suunniteltua tilausta, voit asettaa sen tilaksi **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="9e1c3-113">Jos haluat vahvistaa suunnitellun tilauksen, voit muuttaa tilaksi **Hyväksytty**.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="9e1c3-114">Pääsuunnittelu noudattaa suunniteltuja tilauksia, joiden tila on **Hyväksytty**, joten niitä ei muokata tai poisteta myöhemmän pääsuunnitteluajon aikana.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="9e1c3-115">Tämän saavuttamiseksi suunnittelulogiikka kopioi **hyväksytyt** suunnitellut tilaukset vanhasta suunnitelmaversiosta uuteen suunnitelmaversioon pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="9e1c3-116">Suunniteltujen tilausten vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="9e1c3-116">Firming planned orders</span></span> 
<span data-ttu-id="9e1c3-117">Vahvistettaessa suunniteltuja tilauksia luodaan todelliset tilaukset.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="9e1c3-118">Nämä tunnetaan myös nimellä *vapautetut* tai *avoimet* tilaukset.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="9e1c3-119">Kun suunniteltu tilaus on vahvistettu, se siirtyy kyseisen moduulin tilausosaan.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="9e1c3-120">Voit valita kaksi vahvistusvaihtoehtoa **Suunnitellut tila ukset** -sivulta:</span><span class="sxs-lookup"><span data-stu-id="9e1c3-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="9e1c3-121">**Vahvista** – tämä vahvistaa yhden tai useita valittuja suunniteltuja tilauksia.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="9e1c3-122">**Vahvista kaikki** – tämä vahvistaa suodattimen kaikki suunnitellut tilaukset.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="9e1c3-123">Käyttämällä **Vahvista kaikki** -toimintoa sinun ei tarvitse valita suunniteltua tilausta, kaikki suodattimen sisällä olevat suunnitellut tilaukset vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="9e1c3-124">Tämä vaihtoehto voi olla hyödyllinen, jos olet vahvistamassa suunniteltujen tilausten suurta määrää.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="9e1c3-125">Voit **vahvistushistoriassa** jäljittää suunnitellun tilauksen, joka on vahvistettu kohdassa **Suunnitellut tilaukset -lomake > Näytä > Vahvistushistoria**.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="9e1c3-126">Rinnakkaisvahvistus</span><span class="sxs-lookup"><span data-stu-id="9e1c3-126">Parallelize firming</span></span>
<span data-ttu-id="9e1c3-127">Jos aiot vahvistaa useita tilauksia samalla kertaa, suorituksen rinnakkaisuus voi parantaa ajoaikaa tai suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="9e1c3-128">Tämä vaihtoehto on käytettävissä vahvistettaessa useita suunniteltuja tilauksia joko **Vahvista**- tai **Vahvista kaikki** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="9e1c3-129">Seuraavat parametrit ovat käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="9e1c3-129">The following parameters are available:</span></span>

-   <span data-ttu-id="9e1c3-130">**Rinnakkainen vahvistus** – jos **Kyllä**, vahvistusprosessista tehdään rinnakkainen hyödyntämällä **Säikeiden määrä** -kohdassa määritettyä säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="9e1c3-131">**Säikeiden määrä** – määrittää vahvistusprosessin rinnakkaisten säikeiden määrän.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="9e1c3-132">Parametri näkyy vain, kun **Rinnakkainen vahvistus** -arvoksi on määritetty **Kyllä.**</span><span class="sxs-lookup"><span data-stu-id="9e1c3-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="9e1c3-133">**Yhdenmukaista vahvistus** -vaihtoehto näkyy vain, kun vahvistumiseen on valittu useampi kuin yksi suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="9e1c3-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9e1c3-134">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9e1c3-134">Additional resources</span></span>
--------

[<span data-ttu-id="9e1c3-135">Pääsuunnitelmien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9e1c3-135">Master plans overview</span></span>](master-plans.md)



