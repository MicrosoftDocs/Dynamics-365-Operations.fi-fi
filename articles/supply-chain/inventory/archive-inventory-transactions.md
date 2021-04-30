---
title: Varastotapahtumien arkistointi
description: Tässä aiheessa kuvataan, miten voit arkistoida varastotapahtumien tietoja järjestelmän suorituskyvyn parantamiseksi.
author: sherry-zheng
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
ms.openlocfilehash: b740da1a8a349f4a1a80b41bf717c388fd3db0c0
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881829"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="a8fb5-103">Varastotapahtumien arkistointi</span><span class="sxs-lookup"><span data-stu-id="a8fb5-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a8fb5-104">Ajan mittaan varastotapahtumien taulukko (`InventTrans`) kasvaa ja kuluttaa enemmän tietokannan tilaa.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="a8fb5-105">Tästä syystä taulukolle tehdyt kyselyt hidastuvat ajan myötä.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="a8fb5-106">Tässä aiheessa kuvataan, kuinka voit käyttää *Varastotapahtumien arkisto* -ominaisuutta varastotapahtumien tietojen arkistoimiseksi ja järjestelmän suorituskyvyn parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="a8fb5-107">Vain kirjanpidollisesti päivityt varastotapahtumat voidaan arkistoida valitulta suljetulta kirjanpitokaudelta.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="a8fb5-108">Jotta kirjanpidollisesti päivitetyt lähtevät varastotapahtumat voidaan arkistoida, niiden varasto-oton tilan täytyy olla *Myyty*, ja saapuvien maksutapahtumien vastaanoton tilan täytyy olla *Ostettu*.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="a8fb5-109">Kun arkistoit varastotapahtumia, kaikki niihin liittyvät tapahtumat siirretään `InventTransArchive`-taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="a8fb5-110">Varasto-ottotapahtumat ja varaston vastaanottotapahtumat arkistoidaan erikseen nimikkeen tunnuksen (`itemId`) ja varastodimension tunnuksen (`inventDimId`) yhdistelmän perusteella, ja ne asetetaan varasto-ottotapahtumien ja vastaanottotapahtumien yhteenvetoihin.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="a8fb5-111">Jos `itemId`- ja `inventDimId`-yhdistelmä sisältää vain yhden vastaanotto- tai varasto-ottotapahtuman, tapahtumaa ei arkistoida.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="a8fb5-112">Toiminnon ottaminen käyttöön järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="a8fb5-112">Turn on the feature in your system</span></span>

<span data-ttu-id="a8fb5-113">Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Varastotapahtumien arkisto* -ominaisuus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span> <span data-ttu-id="a8fb5-114">Huomaa, että tätä toimintoa ei voi poistaa käytöstä, kun se on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-114">Note that this feature cannot be disabled once it has been enabled.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="a8fb5-115">Ennen varastotapahtumien arkistointia huomioitavat asiat</span><span class="sxs-lookup"><span data-stu-id="a8fb5-115">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="a8fb5-116">Huomioi seuraavat liiketoimintaskenaariot ennen varastotapahtumien arkistoimista, koska arkistointi vaikuttaa niihin:</span><span class="sxs-lookup"><span data-stu-id="a8fb5-116">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="a8fb5-117">Kun tarkastat varastotapahtumia niihin liittyvistä asiakirjoista, kuten ostotilausriveiltä, ne näkyvät arkistoituina.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-117">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="a8fb5-118">Jos haluat tarkastaa arkistoidut tapahtumat, sinun täytyy valita **Varastonhallinta \> Kausittaiset tehtävät \> Puhdista \> Varastotapahtumien arkisto**.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-118">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="a8fb5-119">Varaston sulkemista ei voi peruuttaa arkistoiduilta kausilta.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-119">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="a8fb5-120">Ennen kuin voit peruuttaa varaston sulkemisen, sinun täytyy peruuttaa varastotapahtumien arkistointi asiaankuuluvalta kaudelta.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-120">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="a8fb5-121">Standardikustannusten muunnosta ei voi suorittaa arkistoiduille kausille.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-121">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="a8fb5-122">Ennen kuin voit suorittaa standardikustannusten muunnoksen, sinun täytyy peruuttaa varastotapahtumien arkistointi asiaankuuluvalta kaudelta.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-122">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="a8fb5-123">Varastotapahtumien arkistointi vaikuttaa varastotapahtumista saatuihin varastoraportteihin.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-123">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="a8fb5-124">Nämä raportit sisältävät varaston erääntymisraportin ja varaston arvon raportit.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-124">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="a8fb5-125">Arkistointi saattaa vaikuttaa varastoennusteisiin, jos ne suoritetaan arkistoitujen kausien aikahorisontin aikana.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-125">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a8fb5-126">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="a8fb5-126">Prerequisites</span></span>

<span data-ttu-id="a8fb5-127">Varastotapahtumia voidaan arkistoida vain kausina, jotka täyttävät seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="a8fb5-127">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="a8fb5-128">Kirjanpitokauden on oltava suljettu.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-128">The ledger period must be closed.</span></span>
- <span data-ttu-id="a8fb5-129">Varaston sulkeminen on suoritettava arkiston päättymispäivänä tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-129">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="a8fb5-130">Kauden on oltava vähintään vuosi ennen arkiston alkamispäivää.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-130">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="a8fb5-131">Varaston uudelleenlaskentoja ei sallita.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-131">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="a8fb5-132">Varastotapahtumien arkistointi</span><span class="sxs-lookup"><span data-stu-id="a8fb5-132">Archive inventory transactions</span></span>

<span data-ttu-id="a8fb5-133">Arkistoi varastotapahtumia noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-133">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="a8fb5-134">Avaa **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Puhdista** \> **Varastotapahtumien arkisto**.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-134">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="a8fb5-135">**Varastotapahtumien arkisto** -sivu avautuu ja näyttää arkistoitujen prosessitietueiden luettelon.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-135">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="a8fb5-136">![Varastotapahtumien arkisto -sivu](media/archive-inventory-empty.png "Varastotapahtumien arkisto -sivu")</span><span class="sxs-lookup"><span data-stu-id="a8fb5-136">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="a8fb5-137">Valitse toimintoruudusta **Varastotapahtumien arkisto** luodaksesi varastotapahtumien arkiston.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-137">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="a8fb5-138">Määritä **Varastotapahtumien arkisto** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="a8fb5-138">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="a8fb5-139">**Suljetun kirjanpitokauden alkamispäivä** – Valitse aikaisin tapahtumapäivä, joka sisällytetään arkistoon.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-139">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="a8fb5-140">**Suljetun kirjanpitokauden päättymispäivä** – Valitse myöhäisin tapahtumapäivä, joka sisällytetään arkistoon.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-140">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="a8fb5-141">![Varastotapahtumien arkisto -valintaikkuna](media/archive-inventory-dates.png "Varastotapahtumien arkisto -valintaikkuna")</span><span class="sxs-lookup"><span data-stu-id="a8fb5-141">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="a8fb5-142">Voit valita vain kausia, jotka täyttävät [edellytykset](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="a8fb5-142">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="a8fb5-143">Määritä eräkäsittelyn tiedot tarpeen mukaan **Suorita taustalla** -pikavälilehdestä.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-143">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="a8fb5-144">Noudata erätöiden tavallisia ohjeita Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-144">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="a8fb5-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-145">Select **OK**.</span></span>
1. <span data-ttu-id="a8fb5-146">Näet viestin, joka pyytää sinua vahvistamaan, että haluat jatkaa.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-146">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="a8fb5-147">Lue viesti huolellisesti ja valitse **Kyllä**, jos haluat jatkaa.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-147">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="a8fb5-148">Näet viestin, jonka mukaan varastotapahtumien arkistointityösi on lisätty eräjonoon.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-148">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="a8fb5-149">Työ aloittaa nyt varastotapahtumien arkistoinnin valitulta kaudelta.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-149">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="a8fb5-150">Näytä arkistoidut varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="a8fb5-150">View archived inventory transactions</span></span>

<span data-ttu-id="a8fb5-151">**Varastotapahtumien arkisto** -sivu näyttää koko arkistointihistoriasi.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-151">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="a8fb5-152">Ruudukon jokaisella rivillä näytetään tietoja, kuten arkiston luontipäivä, arkiston luonut käyttäjä ja arkiston tila.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-152">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="a8fb5-153">![Arkistointihistoria Varastotapahtumien arkisto -sivulla](media/archive-inventory-full.png "Arkistointihistoria Varastotapahtumien arkisto -sivulla")</span><span class="sxs-lookup"><span data-stu-id="a8fb5-153">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="a8fb5-154">Valitse sivun ylälaidan avattavasta luettelosta jokin seuraavista arvoista suodattaaksesi ruudukossa näytettäviä arkistoja:</span><span class="sxs-lookup"><span data-stu-id="a8fb5-154">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="a8fb5-155">**Aktiiviset** – Näytä vain aktiiviset arkistot, älä peruutettuja arkistoja.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-155">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="a8fb5-156">**Kaikki** – Näytä kaikki arkistot, sekä aktiiviset että peruutetut.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-156">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="a8fb5-157">Jokainen ruudukossa näytetty artikkeli sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="a8fb5-157">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="a8fb5-158">**Aktiivinen** – Valintamerkki osoittaa, että arkisto on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-158">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="a8fb5-159">**Päivämäärästä** – Vanhimman arkistoon sisällytettävissä olevan tapahtuman päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-159">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="a8fb5-160">**Päivämäärään** – Uusimman arkistoon sisällytettävissä olevan tapahtuman päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-160">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="a8fb5-161">**Ajoittaja** – Arkiston luonut käyttäjätili.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-161">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="a8fb5-162">**Suoritettu** – Arkiston luontipäivä.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-162">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="a8fb5-163">**Peruuta** – Valintamerkki osoittaa, että arkisto on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-163">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="a8fb5-164">**Pysäytä tämänhetkinen päivitys** – Valintamerkki osoittaa, että arkisto on käynnissä, mutta se on keskeytetty.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-164">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="a8fb5-165">**Tila** – Arkiston käsittelytila.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-165">**State** – The processing status of the archive.</span></span> <span data-ttu-id="a8fb5-166">Mahdolliset arvot ovat *Odottaa*, *Käynnissä* ja *Valmis*.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-166">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="a8fb5-167">Ruudukon yllä oleva työkalurivi sisältää seuraavat painikkeet, joita voit käyttää valitun arkiston työstämiseen:</span><span class="sxs-lookup"><span data-stu-id="a8fb5-167">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="a8fb5-168">**Arkistoidut tapahtumat** – Katso valitun arkiston kaikki tiedot.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-168">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="a8fb5-169">**Arkistoidut tapahtumat** -sivu näyttää arkiston kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-169">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="a8fb5-170">![Arkistoidut tapahtumat -sivu](media/archive-inventory-transactions.png "Arkistoidut tapahtumat -sivu")</span><span class="sxs-lookup"><span data-stu-id="a8fb5-170">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="a8fb5-171">Jos haluat lisätietoja tietystä **Arkistoidut tapahtumat** -sivulla olevasta tapahtumasta, valitse se ruudukosta ja valitse sitten toimintoruudusta **Arkistoidun tapahtuman tiedot**.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-171">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="a8fb5-172">**Arkistoidun tapahtumat tiedot** -sivulla näytetään esimerkiksi kirjanpidon kirjaus, asiaan liittyvät alareskontran viitteet ja taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-172">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="a8fb5-173">**Keskeytä arkistointi** – Keskeytä valittu arkisto, jota käsitellään tällä hetkellä.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-173">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="a8fb5-174">Keskeytys astuu voimaan vasta, kun arkistointitehtävä on luotu.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-174">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="a8fb5-175">Tästä syystä ennen keskeytyksen alkamista voi olla lyhyt viive.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-175">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="a8fb5-176">Jos arkisto on keskeytetty, sen **Pysäytä tämänhetkinen päivitys** -kenttään ilmestyy valintamerkki.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-176">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="a8fb5-177">**Jatka arkistointia** – Jatka valitun keskeytetyn arkiston käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-177">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="a8fb5-178">**Peruuta** – Peruuta valittu arkisto.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-178">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="a8fb5-179">Voit peruuttaa arkiston vain, jos sen **Tila**-kentän arvo on *Valmis*.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-179">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="a8fb5-180">Jos arkisto on peruutettu, sen **Peruuta**-kenttään ilmestyy valintamerkki.</span><span class="sxs-lookup"><span data-stu-id="a8fb5-180">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
