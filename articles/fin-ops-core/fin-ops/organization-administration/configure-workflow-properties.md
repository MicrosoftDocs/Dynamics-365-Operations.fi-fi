---
title: Työnkulkuominaisuuksien asetusten määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten työnkulun eri ominaisuudet määritetään.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d55665df9efdc87f8a7c42a132bad11b4c4426e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747780"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="f56b4-103">Työnkulkuominaisuuksien asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f56b4-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f56b4-104">Tässä ohjeaiheessa kerrotaan, miten työnkulun eri ominaisuudet määritetään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="f56b4-105">Konfiguroidaksesi työnkulun ominaisuudet, avaa työnkulku työnkulkueditorissa.</span><span class="sxs-lookup"><span data-stu-id="f56b4-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="f56b4-106">Napsauta Työnkulkueditorin alustaa ja valitse sitten **ominaisuudet** avataksesi **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="f56b4-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="f56b4-107">Seuraavien ohjeiden avulla voit sitten määrittää työnkulun eri ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="f56b4-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="f56b4-108">Työnkulun nimeäminen</span><span class="sxs-lookup"><span data-stu-id="f56b4-108">Name the workflow</span></span>

<span data-ttu-id="f56b4-109">Kirjoita näiden ohjeiden avulla nimi työnkululle.</span><span class="sxs-lookup"><span data-stu-id="f56b4-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="f56b4-110">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56b4-111">Kirjoita **Nimi**-kenttään työnkulun yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="f56b4-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="f56b4-112">Oletetaan esimerkiksi, että olet luomassa ostoehdotustyönkulut jokaiselle maalle/alueelle, jossa toimit. Ostoehdotustyönkulut voi nimetä esimerkiksi seuraavasti: **Tanskan ostoehdotukset** tai **Espanjan ostoehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="f56b4-113">Työnkulun omistajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f56b4-113">Specify the workflow owner</span></span>

<span data-ttu-id="f56b4-114">Työnkulun omistaja on vastuussa työnkulun hallinnasta ja ylläpidosta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="f56b4-115">Määritä työnkulun omistaja seuraavia ohjeita noudattamalla.</span><span class="sxs-lookup"><span data-stu-id="f56b4-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="f56b4-116">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56b4-117">Valitse **Omistaja**-luettelosta tämän työnkulun hallinnasta vastaava henkilö.</span><span class="sxs-lookup"><span data-stu-id="f56b4-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="f56b4-118">Valitse sähköpostimalli.</span><span class="sxs-lookup"><span data-stu-id="f56b4-118">Select an email template</span></span>

<span data-ttu-id="f56b4-119">Valitse näiden ohjeiden avulla sähköpostimalli, jota käytetään työnkulkua koskevien ilmoitusviestin luomiseen.</span><span class="sxs-lookup"><span data-stu-id="f56b4-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="f56b4-120">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56b4-121">Valitse malli **Työnkulkuilmoitusten sähköpostimallit** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="f56b4-122">Käyttäjien ohjeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f56b4-122">Enter instructions for users</span></span>

<span data-ttu-id="f56b4-123">Voit antaa ohjeita käyttäjille, jotka lähettävät asiakirjoja käsiteltäviksi ja hyväksyttäviksi.</span><span class="sxs-lookup"><span data-stu-id="f56b4-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="f56b4-124">Näistä käyttäjistä käytetään myös nimitystä *aloittaja*.</span><span class="sxs-lookup"><span data-stu-id="f56b4-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="f56b4-125">Oletetaan, että olet luomassa ostoehdotuksen työnkulkua, jolle kirjoitat ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f56b4-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="f56b4-126">Ohjeet ovat sitten niiden henkilöiden tarkasteltavissa, jotka luovat ostoehdotuksia **Ostoehdotukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f56b4-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="f56b4-127">Aloittaja voi avata ohjeet näyttöön napsauttamalla työnkulun sanomapalkissa olevaa kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="f56b4-128">Määritä käyttäjien ohjeet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f56b4-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="f56b4-129">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="f56b4-130">Kirjoita ohjeet **Lähetysohjeet**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="f56b4-131">Voit mukauttaa ohjeita lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="f56b4-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="f56b4-132">Kun käyttäjät tarkastelevat ohjeita, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="f56b4-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="f56b4-133">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f56b4-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="f56b4-134">Napsauta **Lähetysohjeet**-kenttää määrittääksesi, mihin haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="f56b4-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f56b4-135">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f56b4-136">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="f56b4-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f56b4-137">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-137">Click **Insert**.</span></span>

4. <span data-ttu-id="f56b4-138">Ohjeiden käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f56b4-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="f56b4-139">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="f56b4-140">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="f56b4-141">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="f56b4-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="f56b4-142">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f56b4-143">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="f56b4-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="f56b4-144">Ohjeet paikkamerkkien asettamisesta ovat vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="f56b4-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="f56b4-145">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-145">Click **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="f56b4-146">Paikkamerkkejä ei voi lisätä kopioimalla ja liittämällä, koska kohdetietoja ei ole liitetty oikein.</span><span class="sxs-lookup"><span data-stu-id="f56b4-146">Placeholders cannot be added using copy and paste because the target information is not pasted in correctly.</span></span> <span data-ttu-id="f56b4-147">Lisää paikkamerkit käyttöliittymän avulla.</span><span class="sxs-lookup"><span data-stu-id="f56b4-147">Use the interface to add placeholders.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="f56b4-148">Määritä, milloin tätä työnkulkua käytetään aktivointiehtojen avulla</span><span class="sxs-lookup"><span data-stu-id="f56b4-148">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="f56b4-149">Voit luoda useita samaan työnkulkutyyppiin perustuvia työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="f56b4-149">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="f56b4-150">Jos käytössä on useita samaan tyyppiin perustuvia työnkulkuja, määritä aktivointiehtojen avulla, milloin kutakin työnkulkua käytetään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-150">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="f56b4-151">Jos aktivointiehdot eivät täyty, käytetään oletusarvoista työnkulkua.</span><span class="sxs-lookup"><span data-stu-id="f56b4-151">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="f56b4-152">Vastaavasti jos työnkulkutyypille on määritetty vain yksi työnkulun määritys, tätä työnkulun määritystä käytetään aktivointiolosuhteista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-152">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="f56b4-153">Voit esimerkiksi luoda ostoehdotustyönkulun kullekin maalle/alueelle, jossa toimit, kuten Tanskan ostoehdotukset ja Espanjan ostoehdotukset seuraavin ehdoin:</span><span class="sxs-lookup"><span data-stu-id="f56b4-153">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="f56b4-154">Tanskan ostoehdotukset -työnkulkua käytetään, kun maa/alue on DK.</span><span class="sxs-lookup"><span data-stu-id="f56b4-154">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="f56b4-155">Espanjan ostoehdotukset -työnkulkua käytetään, kun maa/alue on ES.</span><span class="sxs-lookup"><span data-stu-id="f56b4-155">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="f56b4-156">Määritä seuraavien ohjeiden avulla, milloin konfiguroitavaa työnkulkua tulee käyttää.</span><span class="sxs-lookup"><span data-stu-id="f56b4-156">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="f56b4-157">Valitse vasemmasta ruudusta **Aktivointi**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-157">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="f56b4-158">Merkitse **Määritä tämän työnkulun suorittamisen ehdot** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f56b4-158">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="f56b4-159">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-159">Click **Add condition**.</span></span>
4. <span data-ttu-id="f56b4-160">Määritä ehto.</span><span class="sxs-lookup"><span data-stu-id="f56b4-160">Enter a condition.</span></span>
5. <span data-ttu-id="f56b4-161">Kirjoita kaikki muut tarvittavat ehdot.</span><span class="sxs-lookup"><span data-stu-id="f56b4-161">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="f56b4-162">Suorittamalla työnkulun joillakin kohdetietueilla voit varmistaa, että ehto sisällyttää ja jättää tietueita pois oikein.</span><span class="sxs-lookup"><span data-stu-id="f56b4-162">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="f56b4-163">Määritä, milloin ilmoitukset lähetetään</span><span class="sxs-lookup"><span data-stu-id="f56b4-163">Specify when notifications are sent</span></span>

<span data-ttu-id="f56b4-164">Kun asiakirja lähetetään käsiteltäväksi, järjestelmä luo työnkulkuinstanssin.</span><span class="sxs-lookup"><span data-stu-id="f56b4-164">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="f56b4-165">Voit lähettää käyttäjille ilmoituksen, kun (tähän työnkulkuun perustuva) työnkulkuinstanssi aloitetaan tai päätetään tai kun työnkulku on valmis tai se pysäytetään virheen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="f56b4-165">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="f56b4-166">Seuraavia ohjeita noudattamalla voit määrittää, milloin ilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-166">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="f56b4-167">Valitse vasemmasta ruudusta **Ilmoitukset**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-167">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="f56b4-168">Merkitse kunkin tapahtuman valintaruutu, jonka tulisi käynnistää ilmoitusten lähettäminen:</span><span class="sxs-lookup"><span data-stu-id="f56b4-168">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="f56b4-169">**Aloitettu** – Ilmoitukset lähetetään, kun työnkulkuinstanssi aloitetaan.</span><span class="sxs-lookup"><span data-stu-id="f56b4-169">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="f56b4-170">**Pysäytettiin** – Ilmoitukset lähetetään, kun työnkulkuinstanssi pysäytetään virheen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="f56b4-170">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="f56b4-171">**Valmis** – Ilmoitukset lähetetään, kun työnkulkuinstanssi valmistuu.</span><span class="sxs-lookup"><span data-stu-id="f56b4-171">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="f56b4-172">**Peruuttamaton** – Ilmoitukset lähetetään, kun työnkulkuinstanssi pysäytetään peruuttamattoman virheen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="f56b4-172">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="f56b4-173">**Lopetettu** – Ilmoitukset lähetetään, kun työnkulkuinstanssi lopetetaan.</span><span class="sxs-lookup"><span data-stu-id="f56b4-173">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="f56b4-174">Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="f56b4-174">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="f56b4-175">Kirjoita **Ilmoitusteksti**-välilehdellä ilmoituksen leipäteksti.</span><span class="sxs-lookup"><span data-stu-id="f56b4-175">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="f56b4-176">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="f56b4-176">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="f56b4-177">Kun käyttäjät tarkastelevat tekstiä, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="f56b4-177">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="f56b4-178">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f56b4-178">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="f56b4-179">Napsauta kentän kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="f56b4-179">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="f56b4-180">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-180">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="f56b4-181">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="f56b4-181">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="f56b4-182">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-182">Click **Insert**.</span></span>
    5. <span data-ttu-id="f56b4-183">Tavallinen sisällytettävä **Ilmoitusteksti**-paikkamerkki on Viimeiset muistiinpanot: %Workflow.Last note%, joka näyttää kaikki kommentit edellisestä vaiheesta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-183">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="f56b4-184">Tekstien käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="f56b4-184">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="f56b4-185">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-185">Click **Translations**.</span></span>
    2. <span data-ttu-id="f56b4-186">Napsauta esiin tulevalla sivulla **Lisää**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f56b4-186">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="f56b4-187">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="f56b4-187">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="f56b4-188">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-188">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="f56b4-189">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="f56b4-189">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="f56b4-190">Ohjeet paikkamerkkien asettamisesta ovat vaiheessa 5.</span><span class="sxs-lookup"><span data-stu-id="f56b4-190">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="f56b4-191">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-191">Click **Close**.</span></span>

7. <span data-ttu-id="f56b4-192">Käytä **Vastaanottaja**-välilehden seuraavia asetuksia määrittääksesi henkilöt, joille ilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-192">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="f56b4-193">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="f56b4-193">Option</span></span></th>
    <th><span data-ttu-id="f56b4-194">Ilmoitukset lähetetään näille käyttäjille</span><span class="sxs-lookup"><span data-stu-id="f56b4-194">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="f56b4-195">Noudata seuraavia ohjeita lähettääksesi ilmoituksia</span><span class="sxs-lookup"><span data-stu-id="f56b4-195">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="f56b4-196">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="f56b4-196">Participant</span></span></td>
    <td><span data-ttu-id="f56b4-197">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="f56b4-197">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f56b4-198">Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Osallistuja</strong>-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="f56b4-198">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="f56b4-199">Valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-199">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="f56b4-200">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-200">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f56b4-201">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="f56b4-201">Workflow user</span></span></td>
    <td><span data-ttu-id="f56b4-202">Käyttäjät, jotka osallistuvat työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="f56b4-202">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f56b4-203">Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Työnkulun käyttäjä</strong>-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="f56b4-203">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="f56b4-204">Valitse <strong>Työnkulun käyttäjä</strong> -välilehden <strong>Työnkulun käyttäjä</strong> -luettelosta tämän työnkulun osallistuja.</span><span class="sxs-lookup"><span data-stu-id="f56b4-204">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="f56b4-205">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="f56b4-205">User</span></span></td>
    <td><span data-ttu-id="f56b4-206">Tietyt käyttäjät</span><span class="sxs-lookup"><span data-stu-id="f56b4-206">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="f56b4-207">Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Käyttäjä</strong>-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="f56b4-207">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="f56b4-208"><strong>Käyttäjä</strong>-välilehden <strong>Käytettävissä olevat käyttäjät</strong> -luettelo sisältää kaikki käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="f56b4-208">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="f56b4-209">Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="f56b4-209">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="f56b4-210">Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="f56b4-210">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="f56b4-211">Kirjoita kommentit työnkulkuun tekemistäsi muutoksista</span><span class="sxs-lookup"><span data-stu-id="f56b4-211">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="f56b4-212">Noudata seuraavia ohjeita, kun haluat määrittää työnkulkuun tehtyjen muutosten kommentteja.</span><span class="sxs-lookup"><span data-stu-id="f56b4-212">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="f56b4-213">Valitse vasemmasta ruudusta **Huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="f56b4-213">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="f56b4-214">Kirjoita kommenttisi **Anna kommentteja työnkulusta** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f56b4-214">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="f56b4-215">Tarkista kommenttisi.</span><span class="sxs-lookup"><span data-stu-id="f56b4-215">Review your comments.</span></span> <span data-ttu-id="f56b4-216">Kommentteja ei voi muokata lisäämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f56b4-216">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="f56b4-217">Valitse **Lisää** lisätäksesi kommenttisi **Kommenttihistoria**-alueelle.</span><span class="sxs-lookup"><span data-stu-id="f56b4-217">Click **Add** to add your comments to the **Comment history** area.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]