---
title: Konsernin sisäiset kulut
description: Organisaation yhdessä yrityksessä työskentelevä työntekijä voi tehdä työtä saman organisaation toiselle yritykselle. Tässä tilanteessa työntekijän kulut voidaan määrittää työn vastaanottaneelle yritykselle konsernin sisäisten kulujen toiminnolla.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390881"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c42d5-104">Konsernin sisäiset kulut</span><span class="sxs-lookup"><span data-stu-id="c42d5-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c42d5-105">Organisaation yhdessä yrityksessä työskentelevä työntekijä voi tehdä työtä saman organisaation toiselle yritykselle.</span><span class="sxs-lookup"><span data-stu-id="c42d5-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c42d5-106">Tässä tilanteessa työntekijän kulut voidaan määrittää työn vastaanottaneelle yritykselle konsernin sisäisten kulujen toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="c42d5-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="c42d5-107">Yritystä, joka työllistää työntekijän, kutsutaan lainaajayritykseksi.</span><span class="sxs-lookup"><span data-stu-id="c42d5-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c42d5-108">Yritystä, jolle työntekijä aiheuttaa kuluja, kutsutaan lainaavaksi yritykseksi.</span><span class="sxs-lookup"><span data-stu-id="c42d5-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c42d5-109">Ennen kuin työntekijä voi luoda ja lähettää kuluja töistä, jotka on suoritettu toiselle yritykselle, valitse lainaavan yrityksen **Kulujenhallinnan parametrit** -sivulla **Salli konsernin sisäiset kulurivit** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="c42d5-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c42d5-110">Konsernin sisäisten kulujen verojen kirjaus</span><span class="sxs-lookup"><span data-stu-id="c42d5-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c42d5-111">Jos haluat käyttää kuluraportissa lainaajayritykseen (lähteeseen) liitettyjä veroryhmiä lainaavan yrityksen (kohteen) sijaan, se on määritettävä kirjanpidon arvonlisäveroasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="c42d5-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="c42d5-112">Kun kirjanpidon **Konsernin sisäisen verokirjauksen yritys** -parametrin arvoksi on määritetty **Lähde** ja **Käytä arvonlisäveron verotussäännöt** -arvona on **Ei**, lainaajayrityksen veroyhdistelmää käytetään.</span><span class="sxs-lookup"><span data-stu-id="c42d5-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="c42d5-113">Kun saman parametrin asetuksena on **Kohde**, lainaavan yrityksen veroyhdistelmää käytetään.</span><span class="sxs-lookup"><span data-stu-id="c42d5-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c42d5-114">Kun yhdysvaltalaisen yrityksen parametrin asetuksena on **Lähde**, myös **Saatava arvonlisävero** -kenttä on määritettävä uudella **Kirjanpidon kirjausryhmät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c42d5-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c42d5-115">Kirjanpitomoduuli käyttää tämän kentän tietoja veroihin liittyvässä kirjanpitomerkinnässä.</span><span class="sxs-lookup"><span data-stu-id="c42d5-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="c42d5-116">Toiminta on yhdenmukainen riippumatta siitä, onko kulurivit projektin yhteydessä tai ilman sitä.</span><span class="sxs-lookup"><span data-stu-id="c42d5-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
