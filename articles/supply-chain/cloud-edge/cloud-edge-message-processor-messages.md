---
title: Sanoman käsittelijän sanomat
description: Tässä ohjeaiheessa on tietoja sanoman käsittelijän sanomaominaisuudesta scale unitin kuormitusta varten.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021052"
---
# <a name="message-processor-messages"></a><span data-ttu-id="cc2ff-103">Sanoman käsittelijän sanomat</span><span class="sxs-lookup"><span data-stu-id="cc2ff-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cc2ff-104">Sanoman käsittelijän sanomia käytetään, kun suoritetaan pilvi- ja reunapalvelujen scale uniteja [valmistuksen kuormituksille](cloud-edge-workload-manufacturing.md) ja [varaston hallinnan kuormituksille](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="cc2ff-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="cc2ff-105">Keskuksen ja yksiköiden käyttöönottoympäristöjen välillä vaihdetaan paljon tietoja, jotta ne voidaan pitää synkronoituina, mutta *sanoman käsittelijä* käsittelee vain muutamia näistä tietojen vaihdoista.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="cc2ff-106">Voit tarkastella sanoman käsittelijän käsittelemiä sanomia valitsemalla **Järjestelmänvalvonta > Sanoman käsittelijä > Sanoman käsittelijän sanomat**.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="cc2ff-107">Sanomaruudukon sarakkeet ja suodattimet</span><span class="sxs-lookup"><span data-stu-id="cc2ff-107">Message grid columns and filters</span></span>

<span data-ttu-id="cc2ff-108">**Sanoman käsittelijän sanomat** -sivun yläosan kenttien avulla voit etsiä haluamiasi sanomia.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="cc2ff-109">Useimmat näistä suodattimista vastaavat sanomaruudukon sarakeotsikoita.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="cc2ff-110">Käytettävissä ovat seuraavat suodattimet ja sarakeotsikot:</span><span class="sxs-lookup"><span data-stu-id="cc2ff-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="cc2ff-111">**Sanomatyyppi** – Määrittää sanoman tyypin.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="cc2ff-112">**Sanomajono** – Määrittää sen jonon nimen, jossa sanoma käsitellään.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="cc2ff-113">Käytettävissä ovat seuraavat jonot:</span><span class="sxs-lookup"><span data-stu-id="cc2ff-113">The following queues are provided:</span></span>
  - <span data-ttu-id="cc2ff-114">*Skaalausyksiköstä keskukseen*</span><span class="sxs-lookup"><span data-stu-id="cc2ff-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="cc2ff-115">*Varastonohjausasteikon yksikkö*</span><span class="sxs-lookup"><span data-stu-id="cc2ff-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="cc2ff-116">*Tuotannonohjausasteikon yksikkö*</span><span class="sxs-lookup"><span data-stu-id="cc2ff-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="cc2ff-117">**Sanoman tila** – Määrittää sanoman tilan.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="cc2ff-118">Käytössä ovat seuraavat tilat:</span><span class="sxs-lookup"><span data-stu-id="cc2ff-118">The following states exists:</span></span>
  - <span data-ttu-id="cc2ff-119">*Jonossa* – Sanoma on valmis sanoman käsittelijän käsiteltäväksi.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="cc2ff-120">*Käsitelty* – Sanoman käsittely sanoman käsittelijän toimesta onnistui.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="cc2ff-121">*Peruutettu* – Sanoma käsiteltiin, mutta käsittely epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="cc2ff-122">**Sanoman sisältö** – Tämän suodattimen avulla voit tehdä tekstihakuja sanoman sisällöstä.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="cc2ff-123">(Sanoman sisältöä ei näytetä ruudukossa.) Suodatin käsittelee useimmat erikoissymbolit (kuten ”-”) välilyönteinä ja käsittelee kaikkia välilyöntimerkkejä TAI-totuusarvo-operaattoreina.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="cc2ff-124">T=Tämä tarkoittaa esimerkiksi sitä, että jos haet tiettyä `journalid`-arvoa, joka on sama kuin "USMF-123456", järjestelmä etsii kaikki sanomat, joissa on "USMF" tai "123456", joka on todennäköisesti pitkä luettelo.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="cc2ff-125">Siksi olisi parempi syöttää vain "123456" siksi, että se palauttaa yksityiskohtaisia tuloksia.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="cc2ff-126">Sanoman tyypin esimerkki: Varasto-oikaisun taloudellisen päivityksen pyytäminen</span><span class="sxs-lookup"><span data-stu-id="cc2ff-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="cc2ff-127">Esimerkiksi **Sanoman tyyppi** *Varasto-oikaisun taloudellisen päivityksen pyytäminen* -kohdan avulla luodaan ja kirjataan keskukseen kirjauskansio, kun työntekijä [rekisteröi varaston oikaisun](cloud-edge-warehouse-inventory-adjustment.md) varastosovellusta käyttämällä scale unitin varastonhallinnan kuormitusta varten.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="cc2ff-128">Koska tämä prosessi on peräisin yksiköstä, **Sanomajono**-kenttä näyttää arvon *Scale unitista keskukseen*.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="cc2ff-129">Tälle sanomatyypille scale unitin kuormitus kirjaa sanoman osana varastosovelluksen varasto-oikaisutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="cc2ff-130">Tämän jälkeen sanomatiedot siirretään keskukseen samassa prosessissa, kuin mitä käytetään [Commerce Data Exchange -arkkitehtuurissa](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="cc2ff-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="cc2ff-131">Sanoma päivitetään niin, että siinä näkyy **Sanoman tilana** *Jonossa*.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="cc2ff-132">Sanoman käsittelijä yrittää käsitellä sanomaa ja päivittää **Sanoman tilaksi** *Käsitelty*, jos käsittely onnistui, tai *Peruutettu*, jos epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="cc2ff-133">Sanomalokin, sanomasisällön ja tietojen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="cc2ff-133">View the message log, message content, and details</span></span>

<span data-ttu-id="cc2ff-134">Voit etsiä yksityiskohtaisia tietoja sanomasta valitsemalla sen ruudukosta ja avaamalla sitten **Loki**- tai **Sanoman sisältö** -välilehdet sanomaruudukosta, jossa näkyy kukin käsittelytapahtuma.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="cc2ff-135">**Sanoman sisältö** riippuu **Sanoman tyypistä**, minkä takia sen tekstipituus vaihtelee.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="cc2ff-136">Yleensä sanoman sisältö alkaa **{** ja päättyy **}** ja välissä on kenttien nimet, kuten `journalId` ja sen jälkeen **:** sekä arvo, kuten *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="cc2ff-137">**Loki**-välilehden työkalurivi sisältää seuraavat painikkeet:</span><span class="sxs-lookup"><span data-stu-id="cc2ff-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="cc2ff-138">**Loki** – Näyttää käsittelytulokset.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="cc2ff-139">Tämä auttaa erityisesti ymmärtämään syitä, joiden vuoksi sanomien käsittely epäonnistui ja **Käsittelyn tulos** on *Epäonnistui*.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="cc2ff-140">**Myyntirakenne** – Useita sanomankäsittelytoimintoja voi suorittaa saman eräprosessin osana.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="cc2ff-141">Valitsemalla tämän painikkeen voit tarkastella näitä yksityiskohtaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="cc2ff-142">Voit esimerkiksi nähdä, onko olemassa riippuvuuksia, jotka edellyttävät, että järjestelmä käsittelee tietyt sanomat tietyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="cc2ff-143">Sanoman käsittelijän erätyö</span><span class="sxs-lookup"><span data-stu-id="cc2ff-143">Message processor batch job</span></span>

<span data-ttu-id="cc2ff-144">Pilvi- ja reunapalveluita suoritettaessa *Sanoman käsittelijä* -erätyö käynnistyy automaattisesti, kun uusi sanoma luodaan käsittelyä varten, joten tätä työtä ei tarvitse ajoittaa manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="cc2ff-145">Voit tarvittaessa käyttää erätyötä valitsemalla **Järjestelmänvalvonta > Sanoman käsittelijä > Sanoman käsittelijä**.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="cc2ff-146">Sanoman käsitteleminen manuaalisesti tai sen peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="cc2ff-146">Manually process or cancel a message</span></span>

<span data-ttu-id="cc2ff-147">Voit tarvittaessa käsitellä tai peruuttaa sanoman manuaalisesti sen nykyisen tilan mukaan.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="cc2ff-148">Voit tehdä tämän valitsemalla sanoman ruudukossa ja valitsemalla sitten toimintoruudusta **Käsittele** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="cc2ff-149">Liiketapahtumien määrittäminen hälytyksien toimitusta varten käsittelytulosten epäonnistumisen vuoksi</span><span class="sxs-lookup"><span data-stu-id="cc2ff-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="cc2ff-150">Se lisäksi, että voit suodattaa **Sanoman tila** -arvon *Peruutettu* epäonnistui-sanomien kyselemiseksi, voi määrittää [Liiketoimintatapahtumat](../../fin-ops-core/dev-itpro/business-events/home-page.md) keskuksessa ja saada ilmoituksen epäonnistuneista käsittelytuloksista.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="cc2ff-151">Voit tehdä tämän aktivoimalla yritystapahtuman nimeltä *Sanoman käsittelijän sanoma käsitelty* **Liiketoimintatapahtumien luettelo** -sivulla (**Järjestelmänvalvonta > Asetukset > Liiketoimintatapahtumat > Liiketoimintatapahtumien luettelo**).</span><span class="sxs-lookup"><span data-stu-id="cc2ff-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="cc2ff-152">Osana aktivointiprosessia sinua ohjataan määrittämään, koskeeko tapahtuma vain yhtä vai kaikkia yrityksiä sekä antamaan **Päätepisteen nimi**, on määritettävä ensin.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="cc2ff-153">Jos **Kun liiketoimintatapahtuma ilmenee** -kohdan arvona on *Microsoft Power Automate* (eikä esimerkiksi *HTTPS*), **Päätepisteen nimi** luodaan automaattisesti Supply Chain Managementissa *Microsoft Power Automate* -määrityksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="cc2ff-154">Microsoft Power Automate -esimerkki</span><span class="sxs-lookup"><span data-stu-id="cc2ff-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="cc2ff-155">Tässä esimerkissä **Kun liiketoimintatapahtuma ilmenee** -arvon käyttö *Microsoft Power Automate* n kanssa lähettää InfoLog-sanomia ja hyperlinkkejä sisältäviä sähköpostiviestejä **Sanoman käsittelijän sanomat** -sivun avaamiseksi tietylle epäonnistuneelle sivulle keskuksen käyttöönotossa.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="cc2ff-156">Tarvittaessa voit lisätä logiikkaa, jonka avulla ilmoitukset lähetetään rinnakkain eri kanavien avulla ja ohjata vastaanottajia tapahtumatietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="cc2ff-157">Kohdassa [Power Automate](https://preview.flow.microsoft.com) luo uusi automaattinen pilvityönkulku työnkulun käynnistimelle **Kun liiketoimintatapahtuma ilmenee - Fin & Ops App (Dynamics 365)** ja sen jälkeen **Jäsennä JSON**- ja **Lähetä sähköpostiviesti** -vaiheet seuraavassa kuvassa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automaten automaattinen pilvityönkulku":::

1. <span data-ttu-id="cc2ff-159">**Kun liiketoimintatapahtuma ilmenee** -vaiheessa voit etsiä tai syöttää keskuksen **Esiintymä**-kohdan, sitten **Luokka** ja sitten **Liiketoimintatapahtuma** *Sanoman käsittelijän sanoma käsitelty* seuraavassa kuvassa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Kun liiketoimintatapahtuma ilmenee -vaihe":::

1. <span data-ttu-id="cc2ff-161">**Jäsennä JSON** -vaiheessa anna **Rakenne**, joka määrittää laajennetut kentät.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="cc2ff-162">Voit käyttää *Lataa rakenne*-vaihtoehtoa **Liiketoimintatapahtumien luettelo** -sivulla Supply Chain Managementissa tai aloittaa liittämällä esimerkkirakenteen tekstin.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="cc2ff-163">Tämä esimerkkiteksti annetaan seuraavan kuvan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Jäsennä JSON -vaihe":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="cc2ff-165">Voit valita **Lähetä sähköpostiviesti** -kohdasta yksittäiset kentät tai aloittaa liittämällä sähköpostin perustekstiesimerkin **Perusteksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="cc2ff-166">Tämä esimerkki annetaan seuraavan kuvan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate Lähetä sähköpostiviesti -vaihe":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="cc2ff-168">Kun tallennat liiketoimintatapahtuman, se aktivoidaan automaattisesti ja sitä voidaan käyttää osana Supply Chain Managementia.</span><span class="sxs-lookup"><span data-stu-id="cc2ff-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
