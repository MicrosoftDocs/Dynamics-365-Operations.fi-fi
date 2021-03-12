---
title: Varastosovelluksen tapahtumat
description: Tässä ohjeaiheessa käsitellään varastosovelluksen tapahtumasanomien käsittelyssä erätyön osana käytettyä varastosovelluksen tapahtumien käsittelyä.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 66a5ca8a679563b59ca23992f7e0b4ee6fab470b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993800"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="ffaf9-103">Varastosovelluksen tapahtumakäsittely</span><span class="sxs-lookup"><span data-stu-id="ffaf9-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffaf9-104">Supply Chain Managementissa suoritettavat erätyöt voivat käyttää tapahtumien käsittelyjonon varastosovelluksen määrittämiä tietoja, jotta ilmoitettuihin tapahtumiin voidaan reagoida tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="ffaf9-105">Tämä toiminto lisää liittyvät tapahtumat jonoon vastauksena sovellusta käyttävien työtekijöiden tekemiin tietyn tyyppisiin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="ffaf9-106">Esimerkiksi käytettäessä **Luo ja käsittele siirtotilauksia varastosovelluksessa** -toimintoa siirtotilauksen otsikko ja rivit luodaan ja päivitetään taustalla, kun järjestelmä suorittaa **Käsittele varastosovelluksen tapahtumia** -erätyön.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="ffaf9-107">Käsittele varastosovelluksen tapahtumia -toiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="ffaf9-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="ffaf9-108">Ennen kuin käytät tätä toimintoa, se on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="ffaf9-109">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sivua ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="ffaf9-110">Käsittele varastosovelluksen tapahtumia -toiminnossa on seuraavat osat:</span><span class="sxs-lookup"><span data-stu-id="ffaf9-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="ffaf9-111">**Moduuli** - Varastonhallinta</span><span class="sxs-lookup"><span data-stu-id="ffaf9-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="ffaf9-112">**Toiminnon nimi** – Käsittele varastosovelluksen tapahtumia</span><span class="sxs-lookup"><span data-stu-id="ffaf9-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="ffaf9-113">Erätyön määrittäminen käsittelemään varastosovelluksen tapahtumia</span><span class="sxs-lookup"><span data-stu-id="ffaf9-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="ffaf9-114">Käsittele varastosovelluksen tapahtumat</span><span class="sxs-lookup"><span data-stu-id="ffaf9-114">Process warehouse app events</span></span>

<span data-ttu-id="ffaf9-115">Määritä aikataulutettu erätyö käsittelemään siirtotilausten luonti-ja rivipäivitysten varastosovelluksen tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="ffaf9-116">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Käsittele varastosovelluksen tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="ffaf9-117">Käsittele varastosovelluksen tapahtumat -valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="ffaf9-118">Laajenna **Suorita taustalla** -pikavälilehti ja määritä **Erän käsittely** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="ffaf9-119">Valitse **Suorita taustalla** -pikavälilehdessä **Toistuminen**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="ffaf9-120">**Määritä toistuminen** -valintaikkuna aukeaa.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="ffaf9-121">Määritä yritykselle ajon aikataulu tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="ffaf9-122">Palaa **Käsittele varastosovelluksen tapahtumat** -valintaikkunaan valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="ffaf9-123">Lisää erätyö eräajoon valitsemalla **OK** **Käsittele varastosovelluksen tapahtumat** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="ffaf9-124">Varastosovelluksen tapahtumakyselyt</span><span class="sxs-lookup"><span data-stu-id="ffaf9-124">Query warehouse app events</span></span>

<span data-ttu-id="ffaf9-125">Voit näyttää varastosovelluksen luoman tapahtumajonon ja tapahtumasanomat valitsemalla **Varastonhallinta \> Kyselyt ja raportit \> Mobiililaitteen lokit \> Varastosovelluksen tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="ffaf9-126">Tapahtuman vakiojonoprosessi</span><span class="sxs-lookup"><span data-stu-id="ffaf9-126">The standard event queue process</span></span>

<span data-ttu-id="ffaf9-127">Varastosovellusten tapahtumajonoa käytetään yleensä seuraavaksi käsitellyn työnkulun kanssa:</span><span class="sxs-lookup"><span data-stu-id="ffaf9-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="ffaf9-128">Tapahtuma lisätään jonoon tapahtumasanoman avulla.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="ffaf9-129">Uuden sanoman tapahtuman tila on aluksi **Odottaa**, jolloin **Käsittele varastosovelluksen tapahtumat** -erätyö ei poimi ja käsittele tätä sanomaa.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="ffaf9-130">Heti kun sanoman tilaksi päivitetään **Asetettu jonoon**, **Käsittele varastosovelluksen tapahtumat** -erätyö poimii ja käsittelee tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="ffaf9-131">Erätyö päivittää tapahtuman tilaksi joko **Valmis** tai **Epäonnistui** sen mukaan, oliko pyydetty prosessi mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="ffaf9-132">Kun kaikkien liittyvien tapahtumasanomien tila on **Valmis**, tapahtuma poistetaan jonosta.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="ffaf9-133">Yksityiskohtainen esimerkki on kohdassa [Siirtotilauksen luonti varastosovellusprosessissa](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="ffaf9-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="ffaf9-134">Tapahtumavirheiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="ffaf9-134">Handle event errors</span></span>

<span data-ttu-id="ffaf9-135">Varastotapahtuman käsittelyn osana pyydetty sanomatehtävä ei ehkä vastaanota prosesseja erätyöstä.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="ffaf9-136">Siinä tapauksessa tapahtumasanoman tilaksi muuttuu **Epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="ffaf9-137">**Eräloki**-tietojen avulla saadaan tietoja, miksi jokin toiminto on tehtävä ongelman korjaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="ffaf9-138">Yksityiskohtainen esimerkki on kohdassa [Siirtotilauksen luonti varastosovelluksessa](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="ffaf9-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="ffaf9-139">Epäonnistuneen varastosovelluksen tapahtumasanoman nollaaminen:</span><span class="sxs-lookup"><span data-stu-id="ffaf9-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="ffaf9-140">Valitse **Varastonhallinta \> Kyselyt ja raportit \> Mobiililaitteen loki \> Varastosovelluksen tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="ffaf9-141">Etsi ja valitse **Varastosovelluksen tapahtumasanomat** -pikavälilehdessä liittyvä tapahtuma, jonka **Tapahtuman tila** -sarakkeessa näkyy **Epäonnistui**.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="ffaf9-142">Valitse **Palauta** **Varastosovelluksen tapahtumasanomat** -työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="ffaf9-143">Jatka työskentelyä, kunnes kaikki liittyvät sanomat on palautettu.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="ffaf9-144">Voit poistaa **Epäonnistui**-tapahtumasanoman myös käyttämällä **Varastosovelluksen tapahtumasanomat** -työkalurivin **Poista**-vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="ffaf9-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
