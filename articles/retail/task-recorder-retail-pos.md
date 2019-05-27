---
title: Retail Modern POS:n (MPOS) ja pilvimyyntipisteen tehtävien tallennustoiminto sekä ohje
description: Tässä ohjeaiheessa kuvataan, miten tehtävien tallennustoimintoa käytetään Retail Modern POS:ssa ja pilvimyyntipisteessä.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a74a1275f08e3dba60a1002a102e143eb37fcd9a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548551"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="adb30-103">Retail Modern POS:n (MPOS) ja pilvimyyntipisteen tehtävien tallennustoiminto sekä ohje</span><span class="sxs-lookup"><span data-stu-id="adb30-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="adb30-104">Tässä ohjeaiheessa kuvataan, miten tehtävien tallennustoimintoa käytetään Retail Modern POS:ssa ja pilvimyyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="adb30-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="adb30-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="adb30-105">Overview</span></span>

<span data-ttu-id="adb30-106">Tehtävien tallennustoiminto Retail Modern POS -sovelluksessa on uusi ratkaisu, jonka reagointikyky on suuri.</span><span class="sxs-lookup"><span data-stu-id="adb30-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="adb30-107">Se sisältää joustavan ohjelmointirajapinnan (API:n), joka mahdollistaa laajennettavuuden ja jonka avulla integrointi liiketoimintaprosessien tallenteiden kuluttajien kanssa on saumatonta.</span><span class="sxs-lookup"><span data-stu-id="adb30-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="adb30-108">Lisäksi tehtävän tallennus Microsoft Dynamics Lifecycle Servicesin liiketoimintaprosessin mallintajan (BPM) ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) avulla on nostettu eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="adb30-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="adb30-109">Tämän vuoksi käyttäjät voivat jatkaa monipuolisten liiketoimintaprosessien kaavioiden tekemistä tallenteista ja analysoida ja suunnitella sovelluksia.</span><span class="sxs-lookup"><span data-stu-id="adb30-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="adb30-110">Arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="adb30-110">Architecture</span></span>

<span data-ttu-id="adb30-111">Tehtävien tallennustoiminto voi tallentaa käyttäjän toiminnot asiakasohjelmassa erittäin tarkasti.</span><span class="sxs-lookup"><span data-stu-id="adb30-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="adb30-112">Kukin ohjausobjekti mitataan, ja tehtävien tallennustoiminnolle ilmoitetaan käyttäjän toiminnon suorituksesta.</span><span class="sxs-lookup"><span data-stu-id="adb30-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="adb30-113">Ohjausobjekti ilmoittaa tehtävien tallennustoiminnolle, että tapahtuma on suoritettu, ja välittää reaaliaikaisesti kaikki vastaavaa käyttäjän toimintoa koskevat asianmukaiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="adb30-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="adb30-114">Näistä tiedoista tehtävien tallennustoiminto voi tallentaa käyttäjän toiminnon tyypin (kuten painikkeen valinta, arvon syöttö tai siirtyminen) ja käyttäjän toimintoon liittyvät tiedot (kuten syöttötietojen arvon ja tyypin, lomakkeen kontekstin tai tietueen kontekstin).</span><span class="sxs-lookup"><span data-stu-id="adb30-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="adb30-115">Tehtävien tallennustoiminto säilyttää niin paljon tietoja, että niiden avulla voidaan varmistaa tallenteen toisto juuri niin kuin käyttäjä toiminnon suorittanut tallennuksen hetkellä.</span><span class="sxs-lookup"><span data-stu-id="adb30-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="adb30-116">(Toistotoimintoa ei ole vielä otettu käyttöön Retail Modern POS -sovelluksessa ja pilvimyyntipisteessä.)</span><span class="sxs-lookup"><span data-stu-id="adb30-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="adb30-117">Peruskonfigurointi</span><span class="sxs-lookup"><span data-stu-id="adb30-117">Basic configuration</span></span>

<span data-ttu-id="adb30-118">Voit ottaa tehtävätallenteen käyttöön myyntipisteessä seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="adb30-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="adb30-119">Valitse **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="adb30-119">Click **Retail** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="adb30-120">Valitse kassakone, jolle haluat ottaa tehtävätallenteen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="adb30-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="adb30-121">Valitse **Kassakone**-välilehden **Yleinen**-pikavälilehden **Ota tehtävän tallennus käyttöön** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="adb30-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="adb30-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="adb30-122">Click **Save**.</span></span>
5. <span data-ttu-id="adb30-123">Siirry kohtaan **Vähittäismyynti** &gt; **Vähittäismyynnin IT** &gt; **Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="adb30-123">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="adb30-124">Valitse **Kassakoneet (1090)** -työ ja valitse sitten **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="adb30-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="adb30-125">Tallenteen luominen</span><span class="sxs-lookup"><span data-stu-id="adb30-125">Create a recording</span></span>

<span data-ttu-id="adb30-126">Näiden ohjeiden avulla voit luoda uuden tallenteen tehtävien tallennustoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="adb30-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="adb30-127">Käynnistä Retail Modern POS tai pilvimyyntipiste ja kirjaudu sisään.</span><span class="sxs-lookup"><span data-stu-id="adb30-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="adb30-128">Valitse **Asetukset**-sivun **Tehtävien tallennustoiminto** -osassa **Avaa tehtävien tallennustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="adb30-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="adb30-129">**Tehtävien tallennustoiminto** -ruutu avautuu.</span><span class="sxs-lookup"><span data-stu-id="adb30-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="adb30-130">Valitse oikeassa yläkulmassa oleva **Sulje**-painike (**X**), kun haluat sulkea **Tehtävien tallennustoiminto** -ruudun ennen uuden tallenteen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="adb30-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="adb30-131">Voit avata ruudun uudelleen toistamalla vaiheen 2.</span><span class="sxs-lookup"><span data-stu-id="adb30-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="adb30-132">[![Tehtävien tallennustoiminto -ruutu](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="adb30-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="adb30-133">Kirjoita tallenteen nimi ja kuvaus ja valitse sitten **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="adb30-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="adb30-134">Tallennusistunto alkaa heti, kun valitset **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="adb30-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="adb30-135">Jos valitset oikeassa yläkulmassa olevan **Sulje**-painikkeen (**X**) tallennuksen ollessa käynnissä, **Tehtävien tallennustoiminto** -ruutu suljetaan, mutta tallennusistuntoa ei päätetä.</span><span class="sxs-lookup"><span data-stu-id="adb30-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="adb30-136">Voit avata Tehtävien tallennustoiminto -ruudun uudelleen valitsemalla näytön yläosassa olevan **Ohje**-painikkeen (kysymysmerkki).</span><span class="sxs-lookup"><span data-stu-id="adb30-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="adb30-137">[![Kysymysmerkki](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="adb30-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="adb30-138">Kun valitset **Aloita**, tehtävien tallennustoiminto siirtyy tallennustilaan.</span><span class="sxs-lookup"><span data-stu-id="adb30-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="adb30-139">**Tehtävien tallennustoiminto** -ruutu näyttää tallennusprosessiin liittyvät tiedot ja ohjausobjektit.</span><span class="sxs-lookup"><span data-stu-id="adb30-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="adb30-140">Suorita toimintoja, joita haluat suorittaa Retail Modern POS:n tai pilvimyyntipisteen käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="adb30-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="adb30-141">Kun lopetat tallennusistunnon, valitse **Lopeta**.</span><span class="sxs-lookup"><span data-stu-id="adb30-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="adb30-142">Latausvalinnat</span><span class="sxs-lookup"><span data-stu-id="adb30-142">Download options</span></span>

<span data-ttu-id="adb30-143">Tallennusistunnon loputtua näkyvissä on useita vaihtoehtoja, joiden avulla tallenteen voi ladata.</span><span class="sxs-lookup"><span data-stu-id="adb30-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="adb30-144">[![Latausvalinnat](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="adb30-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="adb30-145">Tallenna tälle tietokoneelle</span><span class="sxs-lookup"><span data-stu-id="adb30-145">Save to this PC</span></span>

<span data-ttu-id="adb30-146">Tallennepaketin avulla voi toistaa tehtäväoppaan, ylläpitää tallennetta ja muokata tallenteen huomautuksia.</span><span class="sxs-lookup"><span data-stu-id="adb30-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="adb30-147">(Tätä toimintoa ei ole vielä otettu käyttöön Retail Modern POS:ssa ja pilvimyyntipisteessä.)</span><span class="sxs-lookup"><span data-stu-id="adb30-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="adb30-148">Vie Word-tiedostona</span><span class="sxs-lookup"><span data-stu-id="adb30-148">Export as Word document</span></span>

<span data-ttu-id="adb30-149">Tallenteen voi tallentaa Microsoft Word -asiakirjana.</span><span class="sxs-lookup"><span data-stu-id="adb30-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="adb30-150">Asiakirja sisältää tallennetut vaiheet ja näyttökuvat.</span><span class="sxs-lookup"><span data-stu-id="adb30-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="adb30-151">Tallenna kehittäjien tallenteena</span><span class="sxs-lookup"><span data-stu-id="adb30-151">Save as developer recording</span></span>

<span data-ttu-id="adb30-152">Kehittäjät voivat käyttää käsittelemätöntä tallennetiedostoa moniin tarkoituksiin, esimerkiksi testikoodin muodostamiseen.</span><span class="sxs-lookup"><span data-stu-id="adb30-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="adb30-153">(Tätä toimintoa ei ole vielä otettu käyttöön.)</span><span class="sxs-lookup"><span data-stu-id="adb30-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="adb30-154">Tallennuksen säätimet</span><span class="sxs-lookup"><span data-stu-id="adb30-154">Recording controls</span></span>

<span data-ttu-id="adb30-155">[![Tallennuksen säätimet](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="adb30-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="adb30-156">P&ysäytä</span><span class="sxs-lookup"><span data-stu-id="adb30-156">Stop</span></span>

<span data-ttu-id="adb30-157">Valitse **Lopeta**, kun haluat lopettaa tallennusistunnon.</span><span class="sxs-lookup"><span data-stu-id="adb30-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="adb30-158">Huomaa, että lopettamisen jälkeen et voi käynnistää istuntoa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="adb30-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="adb30-159">Tämän vuoksi kannattaa varmistaa, että tallenne on valmis, ennen kuin se lopetetaan.</span><span class="sxs-lookup"><span data-stu-id="adb30-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="adb30-160">Keskeytä</span><span class="sxs-lookup"><span data-stu-id="adb30-160">Pause</span></span>

<span data-ttu-id="adb30-161">Valitse **Keskeytä**, kun haluat pysäyttää tallennusistunnon väliaikaisesti ja jatkaa toimintoa.</span><span class="sxs-lookup"><span data-stu-id="adb30-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="adb30-162">**Keskeytä**-painikkeen valinnan jälkeen suoritettuja vaiheita ei tallenneta.</span><span class="sxs-lookup"><span data-stu-id="adb30-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="adb30-163">Jatka</span><span class="sxs-lookup"><span data-stu-id="adb30-163">Continue</span></span>

<span data-ttu-id="adb30-164">Voit jatkaa tallennusistuntoa keskeytyksen jälkeen, kun valitset **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="adb30-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="adb30-165">Tallenna näyttökuvia</span><span class="sxs-lookup"><span data-stu-id="adb30-165">Capture screenshots</span></span>

<span data-ttu-id="adb30-166">Tehtävien tallennustoiminto voi tallentaa Retail Modern POS -käyttöliittymän näyttökuvia liiketoimintaprosessin tallennuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="adb30-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="adb30-167">Voit ottaa näyttökuvatoiminnon käyttöön määrittämällä **Tallenna näyttökuvia** -asetukseksi **Kyllä** ja tekemällä tallenteen.</span><span class="sxs-lookup"><span data-stu-id="adb30-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="adb30-168">Kun tallenne on valmis, valitse **Pysäytä** ja lataa Word-asiakirja.</span><span class="sxs-lookup"><span data-stu-id="adb30-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="adb30-169">Asiakirja sisältää vaiheet ja liittyvät näyttökuvat.</span><span class="sxs-lookup"><span data-stu-id="adb30-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="adb30-170">Näyttökuvien tallennustoimintoa ei tueta pilvimyyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="adb30-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="adb30-171">Tehtävän aloittaminen ja lopettaminen</span><span class="sxs-lookup"><span data-stu-id="adb30-171">Start task and End task</span></span>

<span data-ttu-id="adb30-172">Voit määrittää ryhmiteltyjen vaiheiden joukon aloituksen ja lopetuksen **Aloita tehtävä**- ja **Lopeta** **tehtävä** -painikkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="adb30-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="adb30-173">Lisää Aloita tehtävä -vaihe valitsemalla **Aloita tehtävä**. Suorita sitten vaiheet, jotka lisätään ryhmään.</span><span class="sxs-lookup"><span data-stu-id="adb30-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="adb30-174">Kun ryhmän vaiheet on suoritettu, valitse **Lopeta tehtävä**.</span><span class="sxs-lookup"><span data-stu-id="adb30-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="adb30-175">Tehtävien avulla menettelyiden järjestäminen on helpompaa.</span><span class="sxs-lookup"><span data-stu-id="adb30-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="adb30-176">Tehtävät voivat olla sisäkkäisiä muiden tehtävien kanssa.</span><span class="sxs-lookup"><span data-stu-id="adb30-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="adb30-177">Näin myös pitkien ja monimutkaisten liiketoimintaprosessien järjestäminen onnistuu paremmin.</span><span class="sxs-lookup"><span data-stu-id="adb30-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="adb30-178">Huomautusten lisääminen</span><span class="sxs-lookup"><span data-stu-id="adb30-178">Adding annotations</span></span>

<span data-ttu-id="adb30-179">Huomautus on lisäteksti, joka lisätään vaiheeseen tallennuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="adb30-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="adb30-180">Huomautusten avulla voidaan esimerkiksi antaa käyttäjille lisätietoja tai ohjeita.</span><span class="sxs-lookup"><span data-stu-id="adb30-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="adb30-181">Huomautuksia voi lisätä vaiheen edelle ja sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="adb30-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="adb30-182">Huomautuksia voi lisätä mihin tahansa vaiheeseen **Muokkaa**-painikkeen avulla (kynäsymboli), joka löytyy vaiheen oikealta puolelta.</span><span class="sxs-lookup"><span data-stu-id="adb30-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="adb30-183">[![Vaiheen Muokkaa-painike](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="adb30-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="adb30-184">Tekstit ja muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="adb30-184">Texts and notes</span></span>

<span data-ttu-id="adb30-185">**Tekstit**- ja **Muistiinpanot**-kenttien avulla voi lisätä tekstiä, jotka liitetään tehtäväoppaan vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="adb30-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="adb30-186">[![Teksti- ja Muistiinpanot-kenttä](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="adb30-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="adb30-187">Teksti</span><span class="sxs-lookup"><span data-stu-id="adb30-187">Text</span></span>

<span data-ttu-id="adb30-188">**Teksti**-kenttään syötetty kenttä näkyy tehtäväoppaan vaiheen tekstin *yläpuolella*.</span><span class="sxs-lookup"><span data-stu-id="adb30-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="adb30-189">Tämä sijainti on sopiva tekstille, joka on tarkoitettu käyttäjän luettavaksi ennen vaiheen suoritusta.</span><span class="sxs-lookup"><span data-stu-id="adb30-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="adb30-190">Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="adb30-190">Notes</span></span>

<span data-ttu-id="adb30-191">**Muistiinpanot**-kenttään syötetty kenttä näkyy tehtäväoppaan vaiheen tekstin *alapuolella*.</span><span class="sxs-lookup"><span data-stu-id="adb30-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="adb30-192">Käyttäjän on laajennettava vaiheen teksti ponnahdusikkunassa, jotta sen voi lukea.</span><span class="sxs-lookup"><span data-stu-id="adb30-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="adb30-193">Tämä sijainti on sopiva valinnaisesti luettavalle materiaalille tai muille tiedoille, jotka voivat olla hyödyllisiä, mutta joita ei vaadita toiminnon suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="adb30-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="adb30-194">Retail Modern POS:n ja pilvimyyntipisteen ohje</span><span class="sxs-lookup"><span data-stu-id="adb30-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="adb30-195">Voit näyttää omat mukautetut tehtävätallenteet Retail Modern POS:n ja pilvimyyntipisteen ohjeruudussa niin, että niitä voidaan tarkastella tekstinä, kun tallennat tehtävätallenteet ensin omaan BPM-kirjastoon ja päivität sitten ohjejärjestelmän parametrit niin, että ne osoittavat BPM-kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="adb30-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="adb30-196">Lisätietoja on kohdassa [Yhteyden muodostaminen ohjejärjestelmään.](../fin-and-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="adb30-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="adb30-197">Retail Modern POS:n ja pilvimyyntipisteen ohje tekee haut LCS-palvelusta reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="adb30-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="adb30-198">Se tekee haun kaikista BPM-kirjastoista, jotka on valittu Microsoft Dynamics 365 for Retailin ohjejärjestelmän parametreissa, ja näyttää hakua vastaavat tulokset.</span><span class="sxs-lookup"><span data-stu-id="adb30-198">It searches across all the BPM libraries that are selected in the Microsoft Dynamics 365 for Retail Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="adb30-199">Voit käyttää **Ohje**-valikkoa valitsemalla näytön yläosassa olevan **Ohje**-painikkeen (kysymysmerkki) kirjoittamalla hakuruutuun prosessin nimen ja painamalla hakupainiketta.</span><span class="sxs-lookup"><span data-stu-id="adb30-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="adb30-200">[![Ohje-painike](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="adb30-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="adb30-201">Kun valitset hakutuloksista tehtäväoppaan, voit tarkastella vaiheita ohjeaiheena tai viedä ne Word-asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="adb30-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="adb30-202">Retail Modern POS:n ja pilvimyyntipisteen ohje ei anna tehtäväohjeita sen mukaan, mikä lomake tai tehtävä on käsiteltävänä.</span><span class="sxs-lookup"><span data-stu-id="adb30-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="adb30-203">Kirjoita hakukenttään prosessin nimi ja valitse sitten on **Haku**.</span><span class="sxs-lookup"><span data-stu-id="adb30-203">You have to type the process name in the search box and then click **Search**.</span></span>
