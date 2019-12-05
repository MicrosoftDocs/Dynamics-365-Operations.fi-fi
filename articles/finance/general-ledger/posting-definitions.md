---
title: Kirjausmääritykset
description: Tässä artikkelissa on tietoja määritysten kirjaamisesta ja niiden määrittämisestä ja linkittämisestä. Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot.
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22a7b0acae02738e4f14905edb13fac1da0d0213
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770594"
---
# <a name="posting-definitions"></a><span data-ttu-id="8744f-104">Kirjausmääritykset</span><span class="sxs-lookup"><span data-stu-id="8744f-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8744f-105">Tässä artikkelissa on tietoja määritysten kirjaamisesta ja niiden määrittämisestä ja linkittämisestä.</span><span class="sxs-lookup"><span data-stu-id="8744f-105">This article provides information about posting definitions, and how to define and link them.</span></span>
<span data-ttu-id="8744f-106">Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="8744f-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="8744f-107">Voit tarkastella tuettuja asiakirjoja ja kirjaustyyppejä **Tapahtuman kirjausmääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8744f-107">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="8744f-108">Voit aloittaa kirjausmääritysten käyttämisen valitsemalla **Kirjanpitoparametrit**-sivun **Käytä kirjausmäärityksiä** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="8744f-108">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="8744f-109">Alkuperäisten merkintöjen ja muiden kuin tuettujen kirjaustyyppien ja asiakirjojen kirjausprofiilit on määritettävä myös kirjausmääritysten käyttämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8744f-109">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="8744f-110">Kirjausmääritysten avulla otetaan käyttöön ostotilausten varauskirjanpito ja ostoehdotuksien alustavan varauksen kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="8744f-110">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="8744f-111">Kirjausmääritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8744f-111">Defining posting definitions</span></span>
<span data-ttu-id="8744f-112">Määritä **Kirjausmääritykset**-sivulla vastaavuusehto ja merkinnät, jotka luodaan vastaavuuden löytymisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8744f-112">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="8744f-113">Alkuperäisten merkintöjen vastaavuusehdot arvioidaan kirjanpidollisina jakoina.</span><span class="sxs-lookup"><span data-stu-id="8744f-113">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="8744f-114">**Kirjausmääritykset**-sivulla voi myös liittää prioriteettinumerot merkintäriveihin rivien arviointijärjestyksen hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="8744f-114">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="8744f-115">Alimman prioriteettinumeron omaavat rivit arvioidaan ensin.</span><span class="sxs-lookup"><span data-stu-id="8744f-115">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="8744f-116">Ensin arvioidaan siis rivit, joiden prioriteetti on 1, sen jälkeen rivit, joiden prioriteetti on 2 jne.</span><span class="sxs-lookup"><span data-stu-id="8744f-116">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="8744f-117">Kun vastaavuus löytyy, muut vastaavuusehdot ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="8744f-117">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="8744f-118">Lisäksi vain alkuperäistä tapahtumaa vastaavassa ryhmässä olevat ehdot luovat merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="8744f-118">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="8744f-119">Voit tarkistaa kirjausmääritykset ohjatun **kirjausmäärityksen testauksen** avulla.</span><span class="sxs-lookup"><span data-stu-id="8744f-119">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="8744f-120">Kun kirjausmäärityksen alkuperäinen mallimerkintä on määritetty, luodut merkinnät tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="8744f-120">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="8744f-121">Voit käyttää kirjausmäärityksen versioita yhdessä voimaantulopäivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="8744f-121">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="8744f-122">Voit esimerkiksi luoda kirjausmäärityksestä tulevan version, joka kirjataan uuden tilikauden eri kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="8744f-122">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="8744f-123">Liitä kirjausmääritykset tapahtumatyyppeihin **Tapahtuman kirjausmääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8744f-123">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="8744f-124">Kirjausmääritysten linkittäminen</span><span class="sxs-lookup"><span data-stu-id="8744f-124">Linking posting definitions</span></span>
<span data-ttu-id="8744f-125">Voit linkittää kirjausmäärityksen toiseen kirjausmääritysten luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8744f-125">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="8744f-126">Linkitetyn määrityksen ehdot otetaan huomioon nykyisen kirjausmäärityksen ehtojen lisäksi.</span><span class="sxs-lookup"><span data-stu-id="8744f-126">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="8744f-127">Tämä toiminto säästää aikaa, koska nykyisen kirjausmäärityksen **Kirjausmerkinnät**-sivun **Merkinnät**-pikavälilehden ehtoja ei tarvitse syöttää uudelleen, jos kyseiset rivit on jo syötetty toisessa määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="8744f-127">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="8744f-128">Lisää kaavioihin tai tauluihin linkit, joita saatat käyttää.</span><span class="sxs-lookup"><span data-stu-id="8744f-128">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="8744f-129">Voit välttää ristiriidat nykyisen kirjausmäärityksen kanssa varmistamalla, että kaikkien linkittämiesi kirjausmääritysten rivit ovat yksilöiviä.</span><span class="sxs-lookup"><span data-stu-id="8744f-129">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="8744f-130">Seuraavat rajoitukset ovat voimassa, kun luot kirjausmääritysten linkkejä:</span><span class="sxs-lookup"><span data-stu-id="8744f-130">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="8744f-131">Annettu kirjausmääritys voi olla linkki toiseen kirjausmääritykseen tai toinen kirjausmääritys on voitu linkittää siihen. Molempia ei voi tehdä.</span><span class="sxs-lookup"><span data-stu-id="8744f-131">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="8744f-132">Kirjausmäärityksestä voi kuitenkin olla linkki useisiin kirjausmäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="8744f-132">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="8744f-133">Voit määrittää linkkejä vain saman moduulin kirjausmäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="8744f-133">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="8744f-134">Voit liittää kirjausmäärityksen mihin tahansa tapahtumatyyppiin, mutta tapahtumatyypin on kuuluttava samaan moduuliin kuin kirjausmääritys.</span><span class="sxs-lookup"><span data-stu-id="8744f-134">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="8744f-135">**Tapahtuman kirjausmääritykset** -sivulla näet tapahtumatyypin moduulin.</span><span class="sxs-lookup"><span data-stu-id="8744f-135">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="8744f-136">Lisätietoja on kohdassa [Määritysesimerkkien kirjaaminen](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="8744f-136">For more information, see [Posting definition examples](example-posting-definitions.md).</span></span> 


