---
title: "Manuaalisten päätösten konfiguroiminen työnkulkuun"
description: "Tässä ohjeaiheessa kerrotaan, miten manuaalisen päätöksen eri ominaisuudet määritetään."
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
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: e942942aac5e9973ebd0a4e3f3a134b0c667ff5b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="4c2ee-103">Manuaalisten päätösten konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="4c2ee-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c2ee-104">Tässä ohjeaiheessa kerrotaan, miten manuaalisen päätöksen eri ominaisuudet määritetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="4c2ee-105">Manuaalinen päätös konfiguroidaan työnkulkueditorissa napsauttamalla päätöstä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="4c2ee-106">Sitten voit määrittää seuraavien ohjeiden avulla manuaalisen päätöksen ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="4c2ee-107">Päätöksen nimi</span><span class="sxs-lookup"><span data-stu-id="4c2ee-107">Name the decision</span></span>
<span data-ttu-id="4c2ee-108">Kirjoita näiden ohjeiden avulla nimi manuaaliselle päätökselle.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-108">Follow these steps to enter a name for the manual decision.</span></span>

1.  <span data-ttu-id="4c2ee-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="4c2ee-110">Kirjoita manuaalisen päätöksen yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="4c2ee-111">Aiherivin ja ohjeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4c2ee-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="4c2ee-112">Sinun on luotava aiherivi ja ohjeet käyttäjille, jotka on määritetty manuaaliseen päätökseen.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="4c2ee-113">Esimerkiksi jos olet konfiguroimassa ostoehdotukselle päätöstä, sille määritetty käyttäjä näkee aiherivin ja ohjeet **Ostoehdotukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="4c2ee-114">Aiherivi näytetään sivulla olevalla viestirivillä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="4c2ee-115">Käyttäjä voi sitten avata ohjeet napsauttamalla viestirivin kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="4c2ee-116">Seuraavia ohjeita noudattamalla voit määrittää aiherivin ja ohjeet.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="4c2ee-117">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="4c2ee-118">Kirjoita aiherivi **Ohjeet**-välilehden **Työnimikkeen aihe** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="4c2ee-119">Voit mukauttaa aiheriviä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="4c2ee-120">Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="4c2ee-121">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="4c2ee-122">Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="4c2ee-123">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="4c2ee-124">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="4c2ee-125">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="4c2ee-126">Aiherivin käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="4c2ee-127">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="4c2ee-128">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="4c2ee-129">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="4c2ee-130">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="4c2ee-131">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 3 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="4c2ee-132">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-132">Click **Close**.</span></span>

5.  <span data-ttu-id="4c2ee-133">Kirjoita ohjeet **Työnimikkeen ohjeet** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="4c2ee-134">Voit mukauttaa ohjeita lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="4c2ee-135">Kun käyttäjät tarkastelevat ohjeita, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="4c2ee-136">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="4c2ee-137">Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="4c2ee-138">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="4c2ee-139">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="4c2ee-140">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="4c2ee-141">Ohjeiden käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="4c2ee-142">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="4c2ee-143">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="4c2ee-144">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="4c2ee-145">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="4c2ee-146">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 6 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="4c2ee-147">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="4c2ee-148">Määritä päätöksen mahdolliset tulokset</span><span class="sxs-lookup"><span data-stu-id="4c2ee-148">Specify the possible outcomes of a decision</span></span>
<span data-ttu-id="4c2ee-149">Kun asiakirja määritetään päätöksentekijälle, siihen sisältyy yleensä kysymys, johon päätöksentekijän on vastattava.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="4c2ee-150">Kysymyksen vastaus on yleensä **Kyllä** tai **Ei** tai **Tosi** tai **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="4c2ee-151">Noudata seuraavia ohjeita määrittääksesi manuaalisen päätöksen mahdolliset tulokset.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1.  <span data-ttu-id="4c2ee-152">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-152">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="4c2ee-153">Valitse **Tulokset**-välilehden **Tulos 1** -kenttään tuloksen nimi tai vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3.  <span data-ttu-id="4c2ee-154">Tulosten käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-154">To add translations of the outcome, follow these steps:</span></span>
    1.  <span data-ttu-id="4c2ee-155">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-155">Click **Translations**.</span></span>
    2.  <span data-ttu-id="4c2ee-156">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-156">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="4c2ee-157">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="4c2ee-158">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-158">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="4c2ee-159">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-159">Click **Close**.</span></span>

4.  <span data-ttu-id="4c2ee-160">Valitse **Tulos 2** -kenttään tuloksen nimi tai vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5.  <span data-ttu-id="4c2ee-161">Tulosten käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-161">To add translations of the outcome, follow these steps:</span></span>
    1.  <span data-ttu-id="4c2ee-162">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-162">Click **Translations**.</span></span>
    2.  <span data-ttu-id="4c2ee-163">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-163">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="4c2ee-164">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="4c2ee-165">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-165">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="4c2ee-166">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="4c2ee-167">Määritä, milloin ilmoitukset lähetetään</span><span class="sxs-lookup"><span data-stu-id="4c2ee-167">Specify when notifications are sent</span></span>
<span data-ttu-id="4c2ee-168">Voit lähettää käyttäjille ilmoituksia, kun päätös on tehty, delegoitu tai eskaloitu.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="4c2ee-169">Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="4c2ee-170">Valitse vasemmasta ruudusta **Ilmoitukset**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-170">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="4c2ee-171">Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-171">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="4c2ee-172">**\[Vaihtoehto 1\]** – Määritetty käyttäjä on valinnut **\[vaihtoehdon 1\]**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    -   <span data-ttu-id="4c2ee-173">**\[Vaihtoehto 2\]** – Määritetty käyttäjä on valinnut **\[vaihtoehdon 2\]**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    -   <span data-ttu-id="4c2ee-174">**Delegoi** – Määritetty käyttäjä on delegoinut päätöksen toiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    -   <span data-ttu-id="4c2ee-175">**Eskaloi** – Määritetty käyttäjä ei ole tehnyt päätöstä määräajassa.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3.  <span data-ttu-id="4c2ee-176">Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-176">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="4c2ee-177">Kirjoita **Ilmoitusteksti**-välilehden tekstiruutuun ilmoituksen leipäteksti.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="4c2ee-178">Voit mukauttaa ilmoitusta lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="4c2ee-179">Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="4c2ee-180">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-180">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="4c2ee-181">Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-181">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="4c2ee-182">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-182">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="4c2ee-183">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-183">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="4c2ee-184">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-184">Click **Insert**.</span></span>

6.  <span data-ttu-id="4c2ee-185">Ilmoitusten käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-185">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="4c2ee-186">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-186">Click **Translations**.</span></span>
    2.  <span data-ttu-id="4c2ee-187">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-187">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="4c2ee-188">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="4c2ee-189">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-189">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="4c2ee-190">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 5 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="4c2ee-191">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-191">Click **Close**.</span></span>

7.  <span data-ttu-id="4c2ee-192">Valitse **Vastaanottaja**-välilehdellä käyttäjät, joille ilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="4c2ee-193">Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 8.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="4c2ee-194">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4c2ee-194">Option</span></span></th>
    <th><span data-ttu-id="4c2ee-195">Ilmoituksen vastaanottajat</span><span class="sxs-lookup"><span data-stu-id="4c2ee-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="4c2ee-196">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="4c2ee-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="4c2ee-197">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="4c2ee-197">Participant</span></span></td>
    <td><span data-ttu-id="4c2ee-198">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="4c2ee-198">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4c2ee-199">Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="4c2ee-200">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="4c2ee-201">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="4c2ee-201">Workflow user</span></span></td>
    <td><span data-ttu-id="4c2ee-202">Nykyisen työnkulun käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-202">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="4c2ee-203">Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="4c2ee-204">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="4c2ee-204">User</span></span></td>
    <td><span data-ttu-id="4c2ee-205">Tietyt Microsoft Dynamics 365 for Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4c2ee-206">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="4c2ee-207"><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="4c2ee-208">Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="4c2ee-209">Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="4c2ee-210">Määritä päätös</span><span class="sxs-lookup"><span data-stu-id="4c2ee-210">Assign a decision</span></span>
<span data-ttu-id="4c2ee-211">Seuraavia ohjeita noudattamalla voit määrittää käyttäjät, joille manuaalinen päätös määritetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1.  <span data-ttu-id="4c2ee-212">Valitse vasemmasta ruudusta **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-212">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="4c2ee-213">Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 3.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="4c2ee-214">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4c2ee-214">Option</span></span></th>
    <th><span data-ttu-id="4c2ee-215">Käyttäjät, joille päätös on määritetty</span><span class="sxs-lookup"><span data-stu-id="4c2ee-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="4c2ee-216">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="4c2ee-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="4c2ee-217">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="4c2ee-217">Participant</span></span></td>
    <td><span data-ttu-id="4c2ee-218">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="4c2ee-218">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4c2ee-219">Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle päätös määritetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="4c2ee-220">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle päätös määritetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="4c2ee-221">Hierarkia</span><span class="sxs-lookup"><span data-stu-id="4c2ee-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="4c2ee-222">Tietyssä organisaatiohierarkiassa olevat käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-222">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4c2ee-223">Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle päätös määritetään.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="4c2ee-224">Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="4c2ee-225">Nämä nimet edustavat käyttäjiä, joille päätöksen voi määrittää.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="4c2ee-226">Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="4c2ee-227">Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="4c2ee-228">Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="4c2ee-229">Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="4c2ee-230">Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille päätös määritetään:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="4c2ee-231"><strong>Määritä kaikille noudetuille työntekijöille</strong> – Päätös määritetään joukon kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="4c2ee-232"><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Päätös määritetään vain joukon viimeiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="4c2ee-233"><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Päätöstä ei liitetä niille joukon käyttäjille, jotka täyttävät määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="4c2ee-234">Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="4c2ee-235">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="4c2ee-235">Workflow user</span></span></td>
    <td><span data-ttu-id="4c2ee-236">Nykyisen työnkulun käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-236">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="4c2ee-237">Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="4c2ee-238">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="4c2ee-238">User</span></span></td>
    <td><span data-ttu-id="4c2ee-239">Tietyt Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-239">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4c2ee-240">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="4c2ee-241"><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="4c2ee-242">Valitse käyttäjät, joille päätös liitetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="4c2ee-243">Jono</span><span class="sxs-lookup"><span data-stu-id="4c2ee-243">Queue</span></span></td>
    <td><span data-ttu-id="4c2ee-244">Työnimikejono</span><span class="sxs-lookup"><span data-stu-id="4c2ee-244">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="4c2ee-245">Valittuasi <strong>jonon</strong>, napsauta <strong>Jonoperustainen</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="4c2ee-246">Voit määrittää päätöksen tiettyyn jonoon seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="4c2ee-247">Valitse <strong>Jonon tyyppi</strong> -luettelosta <strong>Työnimikejonot</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="4c2ee-248">Valitse jono <strong>Jonon nimi</strong> -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="4c2ee-249">Noudata seuraavia ohjeita, jos haluat, että tietty ehto päättää, mihin jonoon päätös määritetään:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="4c2ee-250">Valitse <strong>Jonon tyyppi</strong> -luettelosta <strong>Ehdolliset työnimikejonot</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="4c2ee-251">Valitse <strong>Ehdollinen jono</strong> <strong>Jonon nimi</strong> -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="4c2ee-252">
    <strong>Huomautus:</strong> tätä vaihtoehtoa käytetään vain muutamissa työnkuluissa, kuten Palvelupyynnön hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-252">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="4c2ee-253">Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on tehdä päätös.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="4c2ee-254">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-254">Select one of the following options:</span></span>
    -   <span data-ttu-id="4c2ee-255">**Tunnit** – Määritä käyttäjän päätöksentekoaika tunteina.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="4c2ee-256">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="4c2ee-257">**Päivät** – Määritä käyttäjän päätöksentekoaika päivinä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="4c2ee-258">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="4c2ee-259">**Viikot** – Määritä käyttäjän päätöksentekoaika viikkoina.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    -   <span data-ttu-id="4c2ee-260">**Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee tehdä päätös.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="4c2ee-261">Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös kuukauden kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="4c2ee-262">**Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee tehdä päätös.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="4c2ee-263">Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös joulukuun kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="4c2ee-264">Jos käyttäjä ei tee päätöstä aikarajan puitteissa, päätös on erääntynyt.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="4c2ee-265">Erääntyneet päätökset eskaloidaan, sivun **Eskalointi**-alueessa valitsemiesi asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="4c2ee-266">Erääntyneen päätöksen toimenpiteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4c2ee-266">Specify what happens when a decision is overdue</span></span>
<span data-ttu-id="4c2ee-267">Jos käyttäjä ei tee päätöstä aikarajan puitteissa, päätös on erääntynyt.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="4c2ee-268">Erääntyneen päätöksen voi eskaloida tai määrittää automaattisesti toisen käyttäjän tehtäväksi.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="4c2ee-269">Seuraa näitä ohjeita, jos haluat eskaloida erääntyneet päätökset.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="4c2ee-270">Valitse vasemmasta ruudusta **Eskalointi**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="4c2ee-271">Luo eskalointipolku valitsemalla **Käytä eskalointipolkua** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="4c2ee-272">Järjestelmä määrittää päätöksen automaattisesti eskalointipolussa luetelluille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="4c2ee-273">Seuraava taulukko on esimerkki eskalointipolusta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-273">For example, the following table represents an escalation path.</span></span>

   | <span data-ttu-id="4c2ee-274">Järjestys</span><span class="sxs-lookup"><span data-stu-id="4c2ee-274">Sequence</span></span> | <span data-ttu-id="4c2ee-275">Eskalointipolku</span><span class="sxs-lookup"><span data-stu-id="4c2ee-275">Escalation path</span></span>            |
   |----------|----------------------------|
   | <span data-ttu-id="4c2ee-276">1</span><span class="sxs-lookup"><span data-stu-id="4c2ee-276">1</span></span>        | <span data-ttu-id="4c2ee-277">Määritä rooliin: Donna</span><span class="sxs-lookup"><span data-stu-id="4c2ee-277">Assign to: Donna</span></span>           |
   | <span data-ttu-id="4c2ee-278">2</span><span class="sxs-lookup"><span data-stu-id="4c2ee-278">2</span></span>        | <span data-ttu-id="4c2ee-279">Määritä rooliin: Erin</span><span class="sxs-lookup"><span data-stu-id="4c2ee-279">Assign to: Erin</span></span>            |
   | <span data-ttu-id="4c2ee-280">3</span><span class="sxs-lookup"><span data-stu-id="4c2ee-280">3</span></span>        | <span data-ttu-id="4c2ee-281">Lopullinen toiminto: \[Vaihtoehto 1\]</span><span class="sxs-lookup"><span data-stu-id="4c2ee-281">Final action: \[Choice 1\]</span></span> |

   <span data-ttu-id="4c2ee-282">Tässä esimerkissä järjestelmä määrittää erääntyneen päätöksen Donnalle.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="4c2ee-283">Jos Donna ei tee päätöstä ajoissa, päätöksenteko määritetään Erinille.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="4c2ee-284">Jos Erin ei tee päätöstä ajoissa, järjestelmä valitsee **\[vaihtoehdon 1\]**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>
3. <span data-ttu-id="4c2ee-285">Voit lisätä käyttäjän eskalointipolkuun valitsemalla **Lisää eskalaatio**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="4c2ee-286">Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 4.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th><span data-ttu-id="4c2ee-287">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="4c2ee-287">Option</span></span></th>
   <th><span data-ttu-id="4c2ee-288">Käyttäjät, joille päätös eskaloidaan</span><span class="sxs-lookup"><span data-stu-id="4c2ee-288">Users that the decision is escalated to</span></span></th>
   <th><span data-ttu-id="4c2ee-289">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="4c2ee-289">Additional steps</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td><span data-ttu-id="4c2ee-290">Hierarkia</span><span class="sxs-lookup"><span data-stu-id="4c2ee-290">Hierarchy</span></span></td>
   <td><span data-ttu-id="4c2ee-291">Tietyssä organisaatiohierarkiassa olevat käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-291">Users in a specific organizational hierarchy</span></span></td>
   <td><ol>
   <li><span data-ttu-id="4c2ee-292">Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle päätös eskaloidaan.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
   <li><span data-ttu-id="4c2ee-293">Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="4c2ee-294">Nämä nimet edustavat käyttäjiä, joille päätöksen voi eskaloida.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="4c2ee-295">Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
   <li><span data-ttu-id="4c2ee-296">Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
   <li><span data-ttu-id="4c2ee-297">Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="4c2ee-298">Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
   </ol></li>
   <li><span data-ttu-id="4c2ee-299">Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille päätös eskaloidaan:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
   <li><span data-ttu-id="4c2ee-300"><strong>Määritä kaikille noudetuille työntekijöille</strong> – Päätös eskaloidaan joukon kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
   <li><span data-ttu-id="4c2ee-301"><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Päätös eskaloidaan vain joukon viimeiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
   <li><span data-ttu-id="4c2ee-302"><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Päätöstä ei eskaloida niille joukon käyttäjille, jotka täyttävät määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="4c2ee-303">Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
   </ul></li>
   </ol></td>
   </tr>
   <tr class="even">
   <td><span data-ttu-id="4c2ee-304">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="4c2ee-304">Workflow user</span></span></td>
   <td><span data-ttu-id="4c2ee-305">Nykyisen työnkulun käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-305">Users in the current workflow</span></span></td>
   <td><ul>
   <li><span data-ttu-id="4c2ee-306">Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td><span data-ttu-id="4c2ee-307">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="4c2ee-307">User</span></span></td>
   <td><span data-ttu-id="4c2ee-308">Tietyt Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="4c2ee-308">Specific Finance and Operations users</span></span></td>
   <td><ol>
   <li><span data-ttu-id="4c2ee-309">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
   <li><span data-ttu-id="4c2ee-310"><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="4c2ee-311">Valitse käyttäjät, joille päätös eskaloidaan ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
   </ol></td>
   </tr>
   </tbody>
   </table>

4. <span data-ttu-id="4c2ee-312">Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on tehdä päätös.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="4c2ee-313">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-313">Select one of the following options:</span></span>
   -   <span data-ttu-id="4c2ee-314">**Tunnit** – Määritä käyttäjän päätöksentekoaika tunteina.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="4c2ee-315">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
   -   <span data-ttu-id="4c2ee-316">**Päivät** – Määritä käyttäjän päätöksentekoaika päivinä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="4c2ee-317">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
   -   <span data-ttu-id="4c2ee-318">**Viikot** – Määritä käyttäjän päätöksentekoaika viikkoina.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
   -   <span data-ttu-id="4c2ee-319">**Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee tehdä päätös.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="4c2ee-320">Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös kuukauden kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
   -   <span data-ttu-id="4c2ee-321">**Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee tehdä päätös.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="4c2ee-322">Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös joulukuun kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="4c2ee-323">Toista vaiheet 3 ja 4 jokaiselle käyttäjälle, joka lisätään eskalointipolkuun.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="4c2ee-324">Käyttäjien järjestystä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="4c2ee-325">Jos eskalointipolun käyttäjät eivät tee päätöstä ajoissa, järjestelmä tekee päätöksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="4c2ee-326">Voit määrittää vaihtoehdon, jonka järjestelmän valitsee valitsemalla **Toiminto**-rivin ja sitten valitsemalla **Lopetustoiminto**-välilehdellä vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="4c2ee-327">Aikarajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4c2ee-327">Set a time limit</span></span>
<span data-ttu-id="4c2ee-328">Noudata seuraavia ohjeita, jos päätös on tehtävä tietyn ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-328">Follow these steps if the decision must be made in a specific time.</span></span> <span data-ttu-id="4c2ee-329">**Huomautus:** näiden ohjeiden mukaan valitsemasi asetukset korvaavat asetukset, jotka olet valinnut kunkin hyväksyntävaiheen **Liitos**- ja **Eskalointi**-alueissa.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="4c2ee-330">Napsauta vasemmassa ruudussa **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="4c2ee-331">Merkitse **Aseta aikaraja työnkulun elementille** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="4c2ee-332">Valitse **Kesto**-kenttään, aika, johon mennessä päätös on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="4c2ee-333">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="4c2ee-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="4c2ee-334">**Tunnit** – Anna tuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="4c2ee-335">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="4c2ee-336">**Päivät** – Anna päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="4c2ee-337">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="4c2ee-338">**Viikot** – Anna viikkojen määrä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-338">**Weeks** – Enter the number of weeks.</span></span>
    -   <span data-ttu-id="4c2ee-339">**Kuukaudet** – Valitse päivä ja viikko, johon mennessä päätös on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="4c2ee-340">Voit esimerkiksi määrittää, että päätös on tehtävä kuukauden kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="4c2ee-341">**Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä päätös on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="4c2ee-342">Voit esimerkiksi määrittää, että päätös on tehtävä joulukuun kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="4c2ee-343">Jos aikaraja ylittyy, järjestelmä tekee päätöksen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="4c2ee-344">Valitse **Toiminto**-luettelosta vaihtoehto, jonka haluat järjestelmän valitsevan.</span><span class="sxs-lookup"><span data-stu-id="4c2ee-344">In the **Action** list, select the option that the system should select.</span></span>





