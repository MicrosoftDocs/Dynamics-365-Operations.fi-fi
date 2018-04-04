---
title: "Työnkulkuominaisuuksien asetusten määrittäminen"
description: "Tässä ohjeaiheessa kerrotaan, miten työnkulun eri ominaisuudet määritetään."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 7ea35d851613a19889392400e31cf8492d5dc799
ms.contentlocale: fi-fi
ms.lasthandoff: 03/23/2018

---

# <a name="configure-workflow-properties"></a><span data-ttu-id="85dcd-103">Työnkulkuominaisuuksien asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="85dcd-103">Configure workflow properties</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="85dcd-104">Tässä ohjeaiheessa kerrotaan, miten työnkulun eri ominaisuudet määritetään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="85dcd-105">Konfiguroidaksesi työnkulun ominaisuudet, avaa työnkulku työnkulkueditorissa.</span><span class="sxs-lookup"><span data-stu-id="85dcd-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="85dcd-106">Napsauta Työnkulkueditorin alustaa ja valitse sitten **ominaisuudet** avataksesi **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="85dcd-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="85dcd-107">Seuraavien ohjeiden avulla voit sitten määrittää työnkulun eri ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="85dcd-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="85dcd-108">Työnkulun nimeäminen</span><span class="sxs-lookup"><span data-stu-id="85dcd-108">Name the workflow</span></span>
<span data-ttu-id="85dcd-109">Kirjoita näiden ohjeiden avulla nimi työnkululle.</span><span class="sxs-lookup"><span data-stu-id="85dcd-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="85dcd-110">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="85dcd-111">Kirjoita **Nimi**-kenttään työnkulun yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="85dcd-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="85dcd-112">Oletetaan esimerkiksi, että olet luomassa ostoehdotustyönkulut jokaiselle maalle/alueelle, jossa toimit. Ostoehdotustyönkulut voi nimetä esimerkiksi seuraavasti: **Tanskan ostoehdotukset** tai **Espanjan ostoehdotukset**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="85dcd-113">Työnkulun omistajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="85dcd-113">Specify the workflow owner</span></span>
<span data-ttu-id="85dcd-114">Työnkulun omistaja on vastuussa työnkulun hallinnasta ja ylläpidosta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="85dcd-115">Määritä työnkulun omistaja seuraavia ohjeita noudattamalla.</span><span class="sxs-lookup"><span data-stu-id="85dcd-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="85dcd-116">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="85dcd-117">Valitse **Omistaja**-luettelosta tämän työnkulun hallinnasta vastaava henkilö.</span><span class="sxs-lookup"><span data-stu-id="85dcd-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="85dcd-118">Valitse sähköpostimalli.</span><span class="sxs-lookup"><span data-stu-id="85dcd-118">Select an email template</span></span>
<span data-ttu-id="85dcd-119">Valitse näiden ohjeiden avulla sähköpostimalli, jota käytetään työnkulkua koskevien ilmoitusviestin luomiseen.</span><span class="sxs-lookup"><span data-stu-id="85dcd-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="85dcd-120">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="85dcd-121">Valitse malli **Työnkulkuilmoitusten sähköpostimallit** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="85dcd-122">Käyttäjien ohjeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="85dcd-122">Enter instructions for users</span></span>
<span data-ttu-id="85dcd-123">Voit antaa ohjeita käyttäjille, jotka lähettävät asiakirjoja käsiteltäviksi ja hyväksyttäviksi.</span><span class="sxs-lookup"><span data-stu-id="85dcd-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="85dcd-124">Näistä käyttäjistä käytetään myös nimitystä *aloittaja*.</span><span class="sxs-lookup"><span data-stu-id="85dcd-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="85dcd-125">Oletetaan, että olet luomassa ostoehdotuksen työnkulkua, jolle kirjoitat ohjeita.</span><span class="sxs-lookup"><span data-stu-id="85dcd-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="85dcd-126">Ohjeet ovat sitten niiden henkilöiden tarkasteltavissa, jotka luovat ostoehdotuksia **Ostoehdotukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="85dcd-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="85dcd-127">Aloittaja voi avata ohjeet näyttöön napsauttamalla työnkulun sanomapalkissa olevaa kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="85dcd-128">Määritä käyttäjien ohjeet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="85dcd-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="85dcd-129">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="85dcd-130">Kirjoita ohjeet **Lähetysohjeet**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="85dcd-131">Voit mukauttaa ohjeita lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="85dcd-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="85dcd-132">Kun käyttäjät tarkastelevat ohjeita, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="85dcd-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="85dcd-133">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="85dcd-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="85dcd-134">Napsauta **Lähetysohjeet**-kenttää määrittääksesi, mihin haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="85dcd-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="85dcd-135">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="85dcd-136">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="85dcd-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="85dcd-137">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="85dcd-138">Ohjeiden käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="85dcd-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="85dcd-139">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="85dcd-140">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="85dcd-141">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="85dcd-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="85dcd-142">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="85dcd-143">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="85dcd-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="85dcd-144">Ohjeet paikkamerkkien asettamisesta ovat vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="85dcd-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="85dcd-145">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="85dcd-146">Määritä, milloin tätä työnkulkua käytetään</span><span class="sxs-lookup"><span data-stu-id="85dcd-146">Specify when this workflow is used</span></span>
<span data-ttu-id="85dcd-147">Voit luoda useita samaan tyyppiin perustuvia työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="85dcd-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="85dcd-148">Voit esimerkiksi luoda ostoehdotustyönkulun kullekin maalle/alueelle, jossa toimit, kuten Tanskan ostoehdotukset ja Espanjan ostoehdotukset.</span><span class="sxs-lookup"><span data-stu-id="85dcd-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="85dcd-149">Jos käytössä on useita samaan tyyppiin perustuvia työnkulkuja, määritä, milloin kutakin työnkulkua käytetään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="85dcd-150">Edellisessä esimerkissä määritetään seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="85dcd-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="85dcd-151">Tanskan ostoehdotukset -työnkulkua käytetään, kun maa/alue on DK.</span><span class="sxs-lookup"><span data-stu-id="85dcd-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="85dcd-152">Espanjan ostoehdotukset -työnkulkua käytetään, kun maa/alue on ES.</span><span class="sxs-lookup"><span data-stu-id="85dcd-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="85dcd-153">Määritä seuraavien ohjeiden avulla, milloin konfiguroitavaa työnkulkua tulee käyttää.</span><span class="sxs-lookup"><span data-stu-id="85dcd-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="85dcd-154">Valitse vasemmasta ruudusta **Aktivointi**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="85dcd-155">Merkitse **Määritä tämän työnkulun suorittamisen ehdot** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="85dcd-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="85dcd-156">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="85dcd-157">Määritä ehto.</span><span class="sxs-lookup"><span data-stu-id="85dcd-157">Enter a condition.</span></span>
5.  <span data-ttu-id="85dcd-158">Kirjoita kaikki muut tarvittavat ehdot.</span><span class="sxs-lookup"><span data-stu-id="85dcd-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="85dcd-159">Voit tarkistaa, onko ehdot määritetty oikein seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="85dcd-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="85dcd-160">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="85dcd-161">Valitse tietue **Testaa työnkulun ehto** -sivun **Tarkista ehto** -alueella.</span><span class="sxs-lookup"><span data-stu-id="85dcd-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="85dcd-162">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-162">Click **Test**.</span></span> <span data-ttu-id="85dcd-163">Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.</span><span class="sxs-lookup"><span data-stu-id="85dcd-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="85dcd-164">Jos esimerkiksi olet luomassa Espanjan ostoehdotusten työnkulkua, sivun **Tarkista ehto** -alueella näytetään luettelo ostoehdotuksista.</span><span class="sxs-lookup"><span data-stu-id="85dcd-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="85dcd-165">Kun valitset **Testi**, järjestelmä arvioi valitun ostoehdotuksen ja määrittää, onko maa/alue ES.</span><span class="sxs-lookup"><span data-stu-id="85dcd-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="85dcd-166">Palaa **Ominaisuudet**-sivulle valitsemalla **OK** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="85dcd-167">Määritä, milloin ilmoitukset lähetetään</span><span class="sxs-lookup"><span data-stu-id="85dcd-167">Specify when notifications are sent</span></span>
<span data-ttu-id="85dcd-168">Kun asiakirja lähetetään käsiteltäväksi, järjestelmä luo työnkulkuinstanssin.</span><span class="sxs-lookup"><span data-stu-id="85dcd-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="85dcd-169">Voit lähettää käyttäjille ilmoituksen, kun (tähän työnkulkuun perustuva) työnkulkuinstanssi aloitetaan tai päätetään tai kun työnkulku on valmis tai se pysäytetään virheen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="85dcd-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="85dcd-170">Seuraavia ohjeita noudattamalla voit määrittää, milloin ilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="85dcd-171">Valitse vasemmasta ruudusta **Ilmoitukset**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="85dcd-172">Merkitse kunkin tapahtuman valintaruutu, jonka tulisi käynnistää ilmoitusten lähettäminen:</span><span class="sxs-lookup"><span data-stu-id="85dcd-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="85dcd-173">**Aloitettu** – Ilmoitukset lähetetään, kun työnkulkuinstanssi aloitetaan.</span><span class="sxs-lookup"><span data-stu-id="85dcd-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="85dcd-174">**Pysäytettiin** – Ilmoitukset lähetetään, kun työnkulkuinstanssi pysäytetään virheen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="85dcd-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="85dcd-175">**Valmis** – Ilmoitukset lähetetään, kun työnkulkuinstanssi valmistuu.</span><span class="sxs-lookup"><span data-stu-id="85dcd-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="85dcd-176">**Peruuttamaton** – Ilmoitukset lähetetään, kun työnkulkuinstanssi pysäytetään peruuttamattoman virheen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="85dcd-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="85dcd-177">**Lopetettu** – Ilmoitukset lähetetään, kun työnkulkuinstanssi lopetetaan.</span><span class="sxs-lookup"><span data-stu-id="85dcd-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="85dcd-178">Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="85dcd-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="85dcd-179">Kirjoita **Ilmoitusteksti**-välilehdellä ilmoituksen leipäteksti.</span><span class="sxs-lookup"><span data-stu-id="85dcd-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="85dcd-180">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="85dcd-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="85dcd-181">Kun käyttäjät tarkastelevat tekstiä, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="85dcd-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="85dcd-182">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="85dcd-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="85dcd-183">Napsauta kentän kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="85dcd-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="85dcd-184">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="85dcd-185">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="85dcd-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="85dcd-186">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="85dcd-187">Tekstien käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="85dcd-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="85dcd-188">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="85dcd-189">Napsauta esiin tulevalla sivulla **Lisää**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="85dcd-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="85dcd-190">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="85dcd-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="85dcd-191">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="85dcd-192">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="85dcd-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="85dcd-193">Ohjeet paikkamerkkien asettamisesta ovat vaiheessa 5.</span><span class="sxs-lookup"><span data-stu-id="85dcd-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="85dcd-194">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-194">Click **Close**.</span></span>

7.  <span data-ttu-id="85dcd-195">Käytä **Vastaanottaja**-välilehden seuraavia asetuksia määrittääksesi henkilöt, joille ilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="85dcd-196">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="85dcd-196">Option</span></span></th>
    <th><span data-ttu-id="85dcd-197">Ilmoitukset lähetetään näille käyttäjille</span><span class="sxs-lookup"><span data-stu-id="85dcd-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="85dcd-198">Noudata seuraavia ohjeita lähettääksesi ilmoituksia</span><span class="sxs-lookup"><span data-stu-id="85dcd-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="85dcd-199">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="85dcd-199">Participant</span></span></td>
    <td><span data-ttu-id="85dcd-200">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="85dcd-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="85dcd-201">Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Osallistuja</strong>-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="85dcd-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="85dcd-202">Valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="85dcd-203">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="85dcd-204">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="85dcd-204">Workflow user</span></span></td>
    <td><span data-ttu-id="85dcd-205">Käyttäjät, jotka osallistuvat työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="85dcd-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="85dcd-206">Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Työnkulun käyttäjä</strong>-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="85dcd-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="85dcd-207">Valitse <strong>Työnkulun käyttäjä</strong> -välilehden <strong>Työnkulun käyttäjä</strong> -luettelosta tämän työnkulun osallistuja.</span><span class="sxs-lookup"><span data-stu-id="85dcd-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="85dcd-208">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="85dcd-208">User</span></span></td>
    <td><span data-ttu-id="85dcd-209">Tietyt Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="85dcd-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="85dcd-210">Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Käyttäjä</strong>-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="85dcd-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="85dcd-211"><strong>Käyttäjä</strong>-välilehden <strong>Käytettävissä olevat käyttäjät</strong> -luettelo sisältää kaikki Dynamics 365 for Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="85dcd-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="85dcd-212">Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="85dcd-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="85dcd-213">Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="85dcd-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="85dcd-214">Kirjoita kommentit työnkulkuun tekemistäsi muutoksista</span><span class="sxs-lookup"><span data-stu-id="85dcd-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="85dcd-215">Noudata seuraavia ohjeita, kun haluat määrittää työnkulkuun tehtyjen muutosten kommentteja.</span><span class="sxs-lookup"><span data-stu-id="85dcd-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="85dcd-216">Valitse vasemmasta ruudusta **Huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="85dcd-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="85dcd-217">Kirjoita kommenttisi **Anna kommentteja työnkulusta** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="85dcd-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="85dcd-218">Tarkista kommenttisi.</span><span class="sxs-lookup"><span data-stu-id="85dcd-218">Review your comments.</span></span> <span data-ttu-id="85dcd-219">Kommentteja ei voi muokata lisäämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="85dcd-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="85dcd-220">Valitse **Lisää** lisätäksesi kommenttisi **Kommenttihistoria**-alueelle.</span><span class="sxs-lookup"><span data-stu-id="85dcd-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





