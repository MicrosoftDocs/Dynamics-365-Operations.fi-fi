---
title: Ylläpidä suunniteltuja tilauksia
description: Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja. Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
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
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "360460"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="27647-104">Ylläpidä suunniteltuja tilauksia</span><span class="sxs-lookup"><span data-stu-id="27647-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27647-105">Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="27647-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="27647-106">Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.</span><span class="sxs-lookup"><span data-stu-id="27647-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="27647-107">Voit hallita suunniteltuja tilauksia **Pääsuunnittelu**-työtilassa, **Suunniteltu tilaus** -luettelossa tai **Suunnitellut tuotantotilaukset**-, **Suunnitellut ostotilaukset**- ja **Suunniteltu siirto** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="27647-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="27647-108">Voit seurata edistymistä **Tila**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="27647-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="27647-109">Käytettävissä ovat seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="27647-109">The following values are used:</span></span>

-   <span data-ttu-id="27647-110">Kun pääsuunnittelu luo suunniteltuja tilauksia, suunniteltujen tilausten tilana on **Käsittelemätön**.</span><span class="sxs-lookup"><span data-stu-id="27647-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="27647-111">Jos et halua vahvistaa suunniteltua tilausta, voit asettaa sen tilaksi **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="27647-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="27647-112">Jos haluat vahvistaa suunnitellun tilauksen, voit asettaa sen tilaksi **Hyväksytty**.</span><span class="sxs-lookup"><span data-stu-id="27647-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="27647-113">Tämä tila ilmaisee, että hyväksyt suunnitellun tilauksen vahvistamisen mutta tilausta ei ole vielä vahvistettu.</span><span class="sxs-lookup"><span data-stu-id="27647-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="27647-114">**Huomautus:** Hyväksytty suunniteltu tilaus siirtyy nykyisessä tilassaan seuraavaan pääsuunnittelun laskentaan.</span><span class="sxs-lookup"><span data-stu-id="27647-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="27647-115">Voit vahvistaa suunnitellut tilaukset valitsemalla **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="27647-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="27647-116">Voit vahvistaa seuraavat suunnitellut tilaukset:</span><span class="sxs-lookup"><span data-stu-id="27647-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="27647-117">Valittuna oleva suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="27647-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="27647-118">Useita suunniteltuja tilauksia.</span><span class="sxs-lookup"><span data-stu-id="27647-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="27647-119">Suunnitellut tilaukset, jotka on luotu **Hajotus**-sivulla hajottamalla.</span><span class="sxs-lookup"><span data-stu-id="27647-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="27647-120">Napsauta **Suunnitellut tilaukset**, valitse suunniteltu tilaus ja napsauta sitten **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="27647-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="27647-121">Kun suunniteltu tilaus on vahvistettu, se siirtyy kyseisen moduulin tilausosaan.</span><span class="sxs-lookup"><span data-stu-id="27647-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="27647-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="27647-122">Additional resources</span></span>
--------

[<span data-ttu-id="27647-123">Pääsuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="27647-123">Master plans</span></span>](master-plans.md)



