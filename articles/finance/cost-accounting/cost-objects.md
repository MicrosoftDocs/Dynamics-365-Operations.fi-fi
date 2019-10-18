---
title: Kustannusobjektin dimensiot
description: Käytä kustannusten analysointiin kustannuselementin dimensioita määrittämään kustannusvirran kohde. Kustannusobjektin dimensioita käytetään määrittämään, mihin kustannukset tulee liittää. Tässä aiheessa on tietoja kustannusobjektin dimensioista.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 90d9176a2ca37b581ef82306cc1ceef515ceb624
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187886"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="cc2f1-105">Kustannusobjektin dimensiot</span><span class="sxs-lookup"><span data-stu-id="cc2f1-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc2f1-106">Käytä kustannusten analysointiin kustannuselementin dimensioita määrittämään kustannusvirran kohde.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="cc2f1-107">Kustannusobjektin dimensioita käytetään määrittämään, mihin kustannukset tulee liittää.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="cc2f1-108">Tässä aiheessa on tietoja kustannusobjektin dimensioista.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="cc2f1-109">Kustannusobjektit ovat mitä tahansa objektityyppejä, joita arvioidaan, mitataan suoraan tai joihin kohdistetaan kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="cc2f1-110">Tyypillisiä kustannusobjekteja ovat tuotteet, projektit, resurssit, osastot, kustannuspaikat ja maantieteelliset alueet.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="cc2f1-111">Yritysjohto käyttää kustannusobjekteja kustannusten määrittämiseen ja kannattavuusanalyysin tekemiseen.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="cc2f1-112">Kustannusobjektin dimensiot ja kustannusobjektin dimension jäsenet</span><span class="sxs-lookup"><span data-stu-id="cc2f1-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="cc2f1-113">Kustannusobjekteja kutsutaan *kustannusobjektin dimensioiksi*.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="cc2f1-114">Kun olet päättänyt, mihin yksikköön kustannusobjektin dimensio viittaa, on annettava yksittäisen dimension arvot tai tuotava ne toisista lähdejärjestelmistä kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="cc2f1-115">Yksittäisten dimensioiden arvoja kutsutaan *kustannusobjektin dimension jäseniksi*.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="cc2f1-116">Esimerkiksi haluat käyttää kustannusobjektin dimensiona taloushallinnon dimensiota, jonka nimi on kustannuspaikka.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="cc2f1-117">Voidaksesi nähdä, miten kustannukset siirtyvät yksittäisiin kustannuspaikkoihin, sinun on tuotava kustannusobjektin dimensiojäsenet.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="cc2f1-118">Tällöin kustannusobjektin dimensiojäsenet ovat todellisia kustannuspaikkoja, kuten myynti, tuotanto, hallinto, maantieteellinen sijainti.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="cc2f1-119">Seuraavassa kuvankaappauksessa on esimerkki kustannuspaikoista kustannusobjektin dimensioina ja todellisista kustannuspaikoista kustannusobjektidimension jäseninä.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="cc2f1-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="cc2f1-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="cc2f1-121">Kustannusobjektin dimension jäsenten tuominen tietoyhdistimillä</span><span class="sxs-lookup"><span data-stu-id="cc2f1-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="cc2f1-122">Voit helpottaa kustannusobjektin dimensiojäsenten tuontia käyttämällä tietoyhdistimiä, joiden avulla voidaan noutaa arvot yksiköistä, joita haluat käyttää kustannusobjektin dimensioina.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="cc2f1-123">Voit käyttää valmiita tietoyhdistimiä tai itse muokattuja tietoyhdistimiä.</span><span class="sxs-lookup"><span data-stu-id="cc2f1-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



