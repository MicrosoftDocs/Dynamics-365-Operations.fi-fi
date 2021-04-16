---
title: Kustannustason dimensiot
description: Koska kustannustasodimensio on yksi kustannuslaskennan perustekijöistä, sitä käytetään luokittelemaan ja jäljittämään kustannusvirran suuntaa.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 067d7035cdb9c8f4bcb2bdac9cf0a33cd4e01079
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811434"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="4cbb1-103">Kustannustason dimensiot</span><span class="sxs-lookup"><span data-stu-id="4cbb1-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cbb1-104">Koska kustannustasodimensio on yksi kustannuslaskennan perustekijöistä, sitä käytetään luokittelemaan ja jäljittämään kustannusvirran suuntaa.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="4cbb1-105">Kustannustaso vastaa kustannusten kannalta merkittävää nimikettä tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="4cbb1-106">Periaatteessa se voi olla minkä tahansa tyyppinen liiketoiminnan alatason elementti, johon kustannusvirta suuntautuu.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="4cbb1-107">Kustannustaso käsitteenä vaihtelee kirjanpitotilistä kaikkiin kustannusten kannalta merkittäviin resursseihin.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="4cbb1-108">Tällä hetkellä kustannuslaskenta tukee kirjanpitotilejä.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="4cbb1-109">Kaksi kustannustasotyyppiä</span><span class="sxs-lookup"><span data-stu-id="4cbb1-109">Two types of cost elements</span></span>
<span data-ttu-id="4cbb1-110">Kustannustasoja on kahdenlaisia: ensisijaiset ja toissijaiset kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="4cbb1-111">Seuraavassa taulukossa esitetään kahden kustannustasotyypin erot:</span><span class="sxs-lookup"><span data-stu-id="4cbb1-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cbb1-112"><strong>Ensisijaiset kustannustasot</strong></span><span class="sxs-lookup"><span data-stu-id="4cbb1-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="4cbb1-113"><strong>Toissijaiset kustannustasot</strong></span><span class="sxs-lookup"><span data-stu-id="4cbb1-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cbb1-114">Ensisijaiset kustannustasot edustavat kustannusvirtaa kirjanpidosta kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="4cbb1-115">Kustannustasorakenne vastaa kirjanpidon tuloksen tilirakennetta, jossa kustannustaso voi vastata päätiliä.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="4cbb1-116">Liiketoiminnan tarpeiden mukaisesti kaikkia päätilejä ei välttämättä voida merkitä kustannustasoiksi.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="4cbb1-117">Esimerkkejä ensisijaisista kustannustasoista:</span><span class="sxs-lookup"><span data-stu-id="4cbb1-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="4cbb1-118">Myytyjen tuotteiden kustannukset (COG)</span><span class="sxs-lookup"><span data-stu-id="4cbb1-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="4cbb1-119">Epäsuorat materiaalikustannukset</span><span class="sxs-lookup"><span data-stu-id="4cbb1-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="4cbb1-120">Henkilökunnan kustannukset</span><span class="sxs-lookup"><span data-stu-id="4cbb1-120">Personnel costs</span></span></li>
<li><span data-ttu-id="4cbb1-121">Energiakustannukset</span><span class="sxs-lookup"><span data-stu-id="4cbb1-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="4cbb1-122">Toissijaiset kustannustasot edustavat sisäistä kustannusvirtaa, koska nämä kustannukset luodaan ja niitä käytetään ainoastaan kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="4cbb1-123">Niitä käytetään varmistamaan, että kustannuslähde voidaan jäljittää.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="4cbb1-124">Näitä kustannustasoja käytetään kustannusten kohdistuksiin ja yleiskustannuslaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="4cbb1-125">Esimerkkejä toissijaisista kustannustasoista:</span><span class="sxs-lookup"><span data-stu-id="4cbb1-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="4cbb1-126">Tuotantokustannukset</span><span class="sxs-lookup"><span data-stu-id="4cbb1-126">Production costs</span></span></li>
<li><span data-ttu-id="4cbb1-127">Tuotannon, materiaalien ja markkinoinnin yleiskustannukset</span><span class="sxs-lookup"><span data-stu-id="4cbb1-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="4cbb1-128">Kustannustason dimensiot ja kustannustason dimension jäsenet</span><span class="sxs-lookup"><span data-stu-id="4cbb1-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="4cbb1-129">Kustannustasoja kutsutaan *kustannustasodimensioiksi* .</span><span class="sxs-lookup"><span data-stu-id="4cbb1-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="4cbb1-130">Yksittäisiä dimensioarvoja kutsutaan *kustannusluokkien dimensiojäseniksi*.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="4cbb1-131">Esimerkki: US tilikartan rakennetta (COA) käytetään lakisääteinen raportoinnin perustana.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="4cbb1-132">Tätä tilikarttaa käytetään kustannustason dimensiona.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="4cbb1-133">Tilit, jotka ovat ensisijaisia kustannustasoja, esitetään kustannustason dimensiojäseninä kustannuslaskennassa.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="4cbb1-134">Seuraavassa kuvankaappauksessa on esimerkki päätileistä kustannustasodimensioina ja toteutuneista päätileistä kustannustasodimension jäseninä.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="4cbb1-135">[![Näyttökuva päätileistä kustannustason dimensiona](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="4cbb1-135">[![Screenshot of Main Accounts as cost element dimension](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="4cbb1-136">Kustannustason dimension jäsenten tuominen tietoyhdistimillä</span><span class="sxs-lookup"><span data-stu-id="4cbb1-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="4cbb1-137">Voit helpottaa kustannustason dimension jäsenten asetusta kustannuslaskennassa käyttämällä valmiita tai mukautettuja tietoyhdistimiä, joilla haetaan ensisijaiset kustannustasot yhdestä tai useammasta lähdejärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="4cbb1-138">Toteutuksessa huomioitavaa</span><span class="sxs-lookup"><span data-stu-id="4cbb1-138">Implementation considerations</span></span>
<span data-ttu-id="4cbb1-139">Koska kustannustasot vastaavat alimman tason kustannustietoja, varmista, että kaikki kustannustasot, joita tarvitaan johdon raportointiin, sisältyvät käyttämääsi kustannustasorakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="4cbb1-140">Riittävän kustannustasomäärän saaminen kustannusseurantaa varten voi olla haastavaa.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="4cbb1-141">Jos kustannustasoja on tuhansia, yksittäisen kustannustason tarkastaminen voi olla vaikeaa.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="4cbb1-142">Vaihtoehtoisesti voit ryhmitellä kustannustasot ja hallita kustannusseurantaa yhdistetyllä tasolla.</span><span class="sxs-lookup"><span data-stu-id="4cbb1-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]