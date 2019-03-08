---
title: Kirjausmääritykset
description: Tässä artikkelissa on tietoja määritysten kirjaamisesta ja niiden määrittämisestä ja linkittämisestä. Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e9d1e593f58e8fc9e12ddac7664b6e67ecda6a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "359770"
---
# <a name="posting-definitions"></a><span data-ttu-id="2b176-104">Kirjausmääritykset</span><span class="sxs-lookup"><span data-stu-id="2b176-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b176-105">Tässä artikkelissa on tietoja määritysten kirjaamisesta ja niiden määrittämisestä ja linkittämisestä.</span><span class="sxs-lookup"><span data-stu-id="2b176-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="2b176-106">Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="2b176-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="2b176-107">Voit käyttää tuetuissa kirjaustyypeissä ja asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="2b176-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="2b176-108">Voit tarkastella tuettuja asiakirjoja ja kirjaustyyppejä **Tapahtuman kirjausmääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2b176-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="2b176-109">Voit aloittaa kirjausmääritysten käyttämisen valitsemalla **Kirjanpitoparametrit**-sivun **Käytä kirjausmäärityksiä** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="2b176-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="2b176-110">Alkuperäisten merkintöjen ja muiden kuin tuettujen kirjaustyyppien ja asiakirjojen kirjausprofiilit on määritettävä myös kirjausmääritysten käyttämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2b176-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="2b176-111">Kirjausmääritysten avulla otetaan käyttöön ostotilausten varauskirjanpito ja ostoehdotuksien alustavan varauksen kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="2b176-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="2b176-112">Kirjausmääritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2b176-112">Defining posting definitions</span></span>
<span data-ttu-id="2b176-113">Määritä **Kirjausmääritykset**-sivulla vastaavuusehto ja merkinnät, jotka luodaan vastaavuuden löytymisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2b176-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="2b176-114">Alkuperäisten merkintöjen vastaavuusehdot arvioidaan kirjanpidollisina jakoina.</span><span class="sxs-lookup"><span data-stu-id="2b176-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="2b176-115">**Kirjausmääritykset**-sivulla voi myös liittää prioriteettinumerot merkintäriveihin rivien arviointijärjestyksen hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="2b176-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="2b176-116">Alimman prioriteettinumeron omaavat rivit arvioidaan ensin.</span><span class="sxs-lookup"><span data-stu-id="2b176-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="2b176-117">Ensin arvioidaan siis rivit, joiden prioriteetti on 1, sen jälkeen rivit, joiden prioriteetti on 2 jne.</span><span class="sxs-lookup"><span data-stu-id="2b176-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="2b176-118">Kun vastaavuus löytyy, muut vastaavuusehdot ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="2b176-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="2b176-119">Lisäksi vain alkuperäistä tapahtumaa vastaavassa ryhmässä olevat ehdot luovat merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="2b176-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="2b176-120">Voit tarkistaa kirjausmääritykset ohjatun **kirjausmäärityksen testauksen** avulla.</span><span class="sxs-lookup"><span data-stu-id="2b176-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="2b176-121">Kun kirjausmäärityksen alkuperäinen mallimerkintä on määritetty, luodut merkinnät tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="2b176-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="2b176-122">Voit käyttää kirjausmäärityksen versioita yhdessä voimaantulopäivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="2b176-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="2b176-123">Voit esimerkiksi luoda kirjausmäärityksestä tulevan version, joka kirjataan uuden tilikauden eri kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="2b176-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="2b176-124">Liitä kirjausmääritykset tapahtumatyyppeihin **Tapahtuman kirjausmääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2b176-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="2b176-125">Kirjausmääritysten linkittäminen</span><span class="sxs-lookup"><span data-stu-id="2b176-125">Linking posting definitions</span></span>
<span data-ttu-id="2b176-126">Voit linkittää kirjausmäärityksen toiseen kirjausmääritysten luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2b176-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="2b176-127">Linkitetyn määrityksen ehdot otetaan huomioon nykyisen kirjausmäärityksen ehtojen lisäksi.</span><span class="sxs-lookup"><span data-stu-id="2b176-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="2b176-128">Tämä toiminto säästää aikaa, koska nykyisen kirjausmäärityksen **Kirjausmerkinnät**-sivun **Merkinnät**-pikavälilehden ehtoja ei tarvitse syöttää uudelleen, jos kyseiset rivit on jo syötetty toisessa määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2b176-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="2b176-129">Lisää kaavioihin tai tauluihin linkit, joita saatat käyttää.</span><span class="sxs-lookup"><span data-stu-id="2b176-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="2b176-130">Voit välttää ristiriidat nykyisen kirjausmäärityksen kanssa varmistamalla, että kaikkien linkittämiesi kirjausmääritysten rivit ovat yksilöiviä.</span><span class="sxs-lookup"><span data-stu-id="2b176-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="2b176-131">Seuraavat rajoitukset ovat voimassa, kun luot kirjausmääritysten linkkejä:</span><span class="sxs-lookup"><span data-stu-id="2b176-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="2b176-132">Annettu kirjausmääritys voi olla linkki toiseen kirjausmääritykseen tai toinen kirjausmääritys on voitu linkittää siihen. Molempia ei voi tehdä.</span><span class="sxs-lookup"><span data-stu-id="2b176-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="2b176-133">Kirjausmäärityksestä voi kuitenkin olla linkki useisiin kirjausmäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="2b176-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="2b176-134">Voit määrittää linkkejä vain saman moduulin kirjausmäärityksiin.</span><span class="sxs-lookup"><span data-stu-id="2b176-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="2b176-135">Voit liittää kirjausmäärityksen mihin tahansa tapahtumatyyppiin, mutta tapahtumatyypin on kuuluttava samaan moduuliin kuin kirjausmääritys.</span><span class="sxs-lookup"><span data-stu-id="2b176-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="2b176-136">**Tapahtuman kirjausmääritykset** -sivulla näet tapahtumatyypin moduulin.</span><span class="sxs-lookup"><span data-stu-id="2b176-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="2b176-137">Lisätietoja on kohdassa [Määritysesimerkkien kirjaaminen](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="2b176-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 


