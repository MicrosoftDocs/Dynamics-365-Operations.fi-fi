---
title: Varastotapahtumien arkistointi
description: Tässä aiheessa kuvataan, miten voit arkistoida varastotapahtumien tietoja järjestelmän suorituskyvyn parantamiseksi.
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556417"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="a15f9-103">Varastotapahtumien arkistointi</span><span class="sxs-lookup"><span data-stu-id="a15f9-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a15f9-104">Ajan mittaan varastotapahtumien taulukko (`InventTrans`) kasvaa ja kuluttaa enemmän tietokannan tilaa.</span><span class="sxs-lookup"><span data-stu-id="a15f9-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="a15f9-105">Tästä syystä taulukolle tehdyt kyselyt hidastuvat ajan myötä.</span><span class="sxs-lookup"><span data-stu-id="a15f9-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="a15f9-106">Tässä aiheessa kuvataan, kuinka voit käyttää *Varastotapahtumien arkisto* -ominaisuutta varastotapahtumien tietojen arkistoimiseksi ja järjestelmän suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="a15f9-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="a15f9-107">Vain kirjanpidollisesti päivityt varastotapahtumat voidaan arkistoida valitulta suljetulta kirjanpitokaudelta.</span><span class="sxs-lookup"><span data-stu-id="a15f9-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="a15f9-108">Jotta kirjanpidollisesti päivitetyt lähtevät varastotapahtumat voidaan arkistoida, niiden varasto-oton tilan täytyy olla *Myyty*, ja saapuvien maksutapahtumien vastaanoton tilan täytyy olla *Ostettu*.</span><span class="sxs-lookup"><span data-stu-id="a15f9-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="a15f9-109">Kun arkistoit varastotapahtumia, kaikki niihin liittyvät tapahtumat siirretään `InventTransArchive`-taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="a15f9-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="a15f9-110">Varasto-ottotapahtumat ja varaston vastaanottotapahtumat arkistoidaan erikseen nimikkeen tunnuksen (`itemId`) ja varastodimension tunnuksen (`inventDimId`) yhdistelmän perusteella, ja ne asetetaan varasto-ottotapahtumien ja vastaanottotapahtumien yhteenvetoihin.</span><span class="sxs-lookup"><span data-stu-id="a15f9-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="a15f9-111">Jos `itemId`- ja `inventDimId`-yhdistelmä sisältää vain yhden vastaanotto- tai varasto-ottotapahtuman, tapahtumaa ei arkistoida.</span><span class="sxs-lookup"><span data-stu-id="a15f9-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="a15f9-112">Toiminnon ottaminen käyttöön järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="a15f9-112">Turn on the feature in your system</span></span>

<span data-ttu-id="a15f9-113">Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Varastotapahtumien arkisto* -ominaisuus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a15f9-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="a15f9-114">Ennen varastotapahtumien arkistointia huomioitavat asiat</span><span class="sxs-lookup"><span data-stu-id="a15f9-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="a15f9-115">Huomioi seuraavat liiketoimintaskenaariot ennen varastotapahtumien arkistoimista, koska arkistointi vaikuttaa niihin:</span><span class="sxs-lookup"><span data-stu-id="a15f9-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="a15f9-116">Kun tarkastat varastotapahtumia niihin liittyvistä asiakirjoista, kuten ostotilausriveiltä, ne näkyvät arkistoituina.</span><span class="sxs-lookup"><span data-stu-id="a15f9-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="a15f9-117">Jos haluat tarkastaa arkistoidut tapahtumat, sinun täytyy valita **Varastonhallinta \> Kausittaiset tehtävät \> Puhdista \> Varastotapahtumien arkisto**.</span><span class="sxs-lookup"><span data-stu-id="a15f9-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="a15f9-118">Varaston sulkemista ei voi peruuttaa arkistoiduilta kausilta.</span><span class="sxs-lookup"><span data-stu-id="a15f9-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="a15f9-119">Ennen kuin voit peruuttaa varaston sulkemisen, sinun täytyy peruuttaa varastotapahtumien arkistointi asiaankuuluvalta kaudelta.</span><span class="sxs-lookup"><span data-stu-id="a15f9-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="a15f9-120">Standardikustannusten muunnosta ei voi suorittaa arkistoiduille kausille.</span><span class="sxs-lookup"><span data-stu-id="a15f9-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="a15f9-121">Ennen kuin voit suorittaa standardikustannusten muunnoksen, sinun täytyy peruuttaa varastotapahtumien arkistointi asiaankuuluvalta kaudelta.</span><span class="sxs-lookup"><span data-stu-id="a15f9-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="a15f9-122">Varastotapahtumien arkistointi vaikuttaa varastotapahtumista saatuihin varastoraportteihin.</span><span class="sxs-lookup"><span data-stu-id="a15f9-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="a15f9-123">Nämä raportit sisältävät varaston erääntymisraportin ja varaston arvon raportit.</span><span class="sxs-lookup"><span data-stu-id="a15f9-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="a15f9-124">Arkistointi saattaa vaikuttaa varastoennusteisiin, jos ne suoritetaan arkistoitujen kausien aikahorisontin aikana.</span><span class="sxs-lookup"><span data-stu-id="a15f9-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a15f9-125">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="a15f9-125">Prerequisites</span></span>

<span data-ttu-id="a15f9-126">Varastotapahtumia voidaan arkistoida vain kausina, jotka täyttävät seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="a15f9-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="a15f9-127">Kirjanpitokauden on oltava suljettu.</span><span class="sxs-lookup"><span data-stu-id="a15f9-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="a15f9-128">Varaston sulkeminen on suoritettava arkiston päättymispäivänä tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a15f9-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="a15f9-129">Kauden on oltava vähintään vuosi ennen arkiston alkamispäivää.</span><span class="sxs-lookup"><span data-stu-id="a15f9-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="a15f9-130">Varaston uudelleenlaskentoja ei sallita.</span><span class="sxs-lookup"><span data-stu-id="a15f9-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="a15f9-131">Varastotapahtumien arkistointi</span><span class="sxs-lookup"><span data-stu-id="a15f9-131">Archive inventory transactions</span></span>

<span data-ttu-id="a15f9-132">Arkistoi varastotapahtumia noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="a15f9-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="a15f9-133">Avaa **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Puhdista** \> **Varastotapahtumien arkisto**.</span><span class="sxs-lookup"><span data-stu-id="a15f9-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="a15f9-134">**Varastotapahtumien arkisto** -sivu avautuu ja näyttää arkistoitujen prosessitietueiden luettelon.</span><span class="sxs-lookup"><span data-stu-id="a15f9-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="a15f9-135">![Varastotapahtumien arkisto -sivu](media/archive-inventory-empty.png "Varastotapahtumien arkisto -sivu")</span><span class="sxs-lookup"><span data-stu-id="a15f9-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="a15f9-136">Valitse toimintoruudusta **Varastotapahtumien arkisto** luodaksesi varastotapahtumien arkiston.</span><span class="sxs-lookup"><span data-stu-id="a15f9-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="a15f9-137">Määritä **Varastotapahtumien arkisto** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="a15f9-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="a15f9-138">**Suljetun kirjanpitokauden alkamispäivä** – Valitse aikaisin tapahtumapäivä, joka sisällytetään arkistoon.</span><span class="sxs-lookup"><span data-stu-id="a15f9-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="a15f9-139">**Suljetun kirjanpitokauden päättymispäivä** – Valitse myöhäisin tapahtumapäivä, joka sisällytetään arkistoon.</span><span class="sxs-lookup"><span data-stu-id="a15f9-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="a15f9-140">![Varastotapahtumien arkisto -valintaikkuna](media/archive-inventory-dates.png "Varastotapahtumien arkisto -valintaikkuna")</span><span class="sxs-lookup"><span data-stu-id="a15f9-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="a15f9-141">Voit valita vain kausia, jotka täyttävät [edellytykset](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="a15f9-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="a15f9-142">Määritä eräkäsittelyn tiedot tarpeen mukaan **Suorita taustalla** -pikavälilehdestä.</span><span class="sxs-lookup"><span data-stu-id="a15f9-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="a15f9-143">Noudata erätöiden tavallisia ohjeita Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="a15f9-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="a15f9-144">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a15f9-144">Select **OK**.</span></span>
1. <span data-ttu-id="a15f9-145">Näet viestin, joka pyytää sinua vahvistamaan, että haluat jatkaa.</span><span class="sxs-lookup"><span data-stu-id="a15f9-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="a15f9-146">Lue viesti huolellisesti ja valitse **Kyllä**, jos haluat jatkaa.</span><span class="sxs-lookup"><span data-stu-id="a15f9-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="a15f9-147">Näet viestin, jonka mukaan varastotapahtumien arkistointityösi on lisätty eräjonoon.</span><span class="sxs-lookup"><span data-stu-id="a15f9-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="a15f9-148">Työ aloittaa nyt varastotapahtumien arkistoinnin valitulta kaudelta.</span><span class="sxs-lookup"><span data-stu-id="a15f9-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="a15f9-149">Näytä arkistoidut varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="a15f9-149">View archived inventory transactions</span></span>

<span data-ttu-id="a15f9-150">**Varastotapahtumien arkisto** -sivu näyttää koko arkistointihistoriasi.</span><span class="sxs-lookup"><span data-stu-id="a15f9-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="a15f9-151">Ruudukon jokaisella rivillä näytetään tietoja, kuten arkiston luontipäivä, arkiston luonut käyttäjä ja arkiston tila.</span><span class="sxs-lookup"><span data-stu-id="a15f9-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="a15f9-152">![Arkistointihistoria Varastotapahtumien arkisto -sivulla](media/archive-inventory-full.png "Arkistointihistoria Varastotapahtumien arkisto -sivulla")</span><span class="sxs-lookup"><span data-stu-id="a15f9-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="a15f9-153">Valitse sivun ylälaidan avattavasta luettelosta jokin seuraavista arvoista suodattaaksesi ruudukossa näytettäviä arkistoja:</span><span class="sxs-lookup"><span data-stu-id="a15f9-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="a15f9-154">**Aktiiviset** – Näytä vain aktiiviset arkistot, älä peruutettuja arkistoja.</span><span class="sxs-lookup"><span data-stu-id="a15f9-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="a15f9-155">**Kaikki** – Näytä kaikki arkistot, sekä aktiiviset että peruutetut.</span><span class="sxs-lookup"><span data-stu-id="a15f9-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="a15f9-156">Jokainen ruudukossa näytetty artikkeli sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="a15f9-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="a15f9-157">**Aktiivinen** – Valintamerkki osoittaa, että arkisto on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="a15f9-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="a15f9-158">**Päivämäärästä** – Vanhimman arkistoon sisällytettävissä olevan tapahtuman päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a15f9-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="a15f9-159">**Päivämäärään** – Uusimman arkistoon sisällytettävissä olevan tapahtuman päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a15f9-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="a15f9-160">**Ajoittaja** – Arkiston luonut käyttäjätili.</span><span class="sxs-lookup"><span data-stu-id="a15f9-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="a15f9-161">**Suoritettu** – Arkiston luontipäivä.</span><span class="sxs-lookup"><span data-stu-id="a15f9-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="a15f9-162">**Peruuta** – Valintamerkki osoittaa, että arkisto on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="a15f9-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="a15f9-163">**Pysäytä tämänhetkinen päivitys** – Valintamerkki osoittaa, että arkisto on käynnissä, mutta se on keskeytetty.</span><span class="sxs-lookup"><span data-stu-id="a15f9-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="a15f9-164">**Tila** – Arkiston käsittelytila.</span><span class="sxs-lookup"><span data-stu-id="a15f9-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="a15f9-165">Mahdolliset arvot ovat *Odottaa*, *Käynnissä* ja *Valmis*.</span><span class="sxs-lookup"><span data-stu-id="a15f9-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="a15f9-166">Ruudukon yllä oleva työkalurivi sisältää seuraavat painikkeet, joita voit käyttää valitun arkiston työstämiseen:</span><span class="sxs-lookup"><span data-stu-id="a15f9-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="a15f9-167">**Arkistoidut tapahtumat** – Katso valitun arkiston kaikki tiedot.</span><span class="sxs-lookup"><span data-stu-id="a15f9-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="a15f9-168">**Arkistoidut tapahtumat** -sivu näyttää arkiston kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a15f9-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="a15f9-169">![Arkistoidut tapahtumat -sivu](media/archive-inventory-transactions.png "Arkistoidut tapahtumat -sivu")</span><span class="sxs-lookup"><span data-stu-id="a15f9-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="a15f9-170">Jos haluat lisätietoja tietystä **Arkistoidut tapahtumat** -sivulla olevasta tapahtumasta, valitse se ruudukosta ja valitse sitten toimintoruudusta **Arkistoidun tapahtuman tiedot**.</span><span class="sxs-lookup"><span data-stu-id="a15f9-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="a15f9-171">**Arkistoidun tapahtumat tiedot** -sivulla näytetään esimerkiksi kirjanpidon kirjaus, asiaan liittyvät alareskontran viitteet ja taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="a15f9-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="a15f9-172">**Keskeytä arkistointi** – Keskeytä valittu arkisto, jota käsitellään tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="a15f9-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="a15f9-173">Keskeytys astuu voimaan vasta, kun arkistointitehtävä on luotu.</span><span class="sxs-lookup"><span data-stu-id="a15f9-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="a15f9-174">Tästä syystä ennen keskeytyksen alkamista voi olla lyhyt viive.</span><span class="sxs-lookup"><span data-stu-id="a15f9-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="a15f9-175">Jos arkisto on keskeytetty, sen **Pysäytä tämänhetkinen päivitys** -kenttään ilmestyy valintamerkki.</span><span class="sxs-lookup"><span data-stu-id="a15f9-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="a15f9-176">**Jatka arkistointia** – Jatka valitun keskeytetyn arkiston käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="a15f9-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="a15f9-177">**Peruuta** – Peruuta valittu arkisto.</span><span class="sxs-lookup"><span data-stu-id="a15f9-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="a15f9-178">Voit peruuttaa arkiston vain, jos sen **Tila**-kentän arvo on *Valmis*.</span><span class="sxs-lookup"><span data-stu-id="a15f9-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="a15f9-179">Jos arkisto on peruutettu, sen **Peruuta**-kenttään ilmestyy valintamerkki.</span><span class="sxs-lookup"><span data-stu-id="a15f9-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
