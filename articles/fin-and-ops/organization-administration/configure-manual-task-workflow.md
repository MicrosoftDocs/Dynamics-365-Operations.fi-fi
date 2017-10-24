---
title: "Manuaalisen tehtävän konfiguroiminen työnkulkuun"
description: "Tässä ohjeaiheessa kerrotaan, miten manuaalisen tehtävän ominaisuudet määritetään."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 98e25e1a132f0767b9c58334f177845c222c3863
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-manual-task-in-a-workflow"></a><span data-ttu-id="6f26f-103">Manuaalisen tehtävän konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="6f26f-103">Configure a manual task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6f26f-104">Tässä ohjeaiheessa kerrotaan, miten manuaalisen tehtävän ominaisuudet määritetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="6f26f-105">Manuaalinen tehtävä konfiguroidaan työnkulkueditorissa napsauttamalla tehtävää hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="6f26f-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="6f26f-106">Sitten voit määrittää seuraavien ohjeiden avulla manuaalisen tehtävän ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="6f26f-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="6f26f-107">Tehtävän nimeäminen</span><span class="sxs-lookup"><span data-stu-id="6f26f-107">Name the task</span></span>
<span data-ttu-id="6f26f-108">Kirjoita näiden ohjeiden avulla nimi manuaaliselle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="6f26f-108">Follow these steps to enter a name for the manual task.</span></span>

1.  <span data-ttu-id="6f26f-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6f26f-110">Kirjoita tehtävän yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="6f26f-111">Aiherivin ja ohjeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6f26f-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="6f26f-112">Sinun on luotava aiherivi ja ohjeet käyttäjille, jotka on määritetty tähän tehtävään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="6f26f-113">Esimerkiksi jos olet konfiguroimassa ostoehdotukselle tehtävää, sille määritetty käyttäjä näkee aiherivin ja ohjeet **Ostoehdotukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6f26f-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="6f26f-114">Aiherivi näytetään sivulla olevalla viestirivillä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="6f26f-115">Käyttäjä voi sitten avata ohjeet napsauttamalla viestirivin kuvaketta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="6f26f-116">Seuraavia ohjeita noudattamalla voit määrittää aiherivin ja ohjeet.</span><span class="sxs-lookup"><span data-stu-id="6f26f-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="6f26f-117">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6f26f-118">Kirjoita aiherivi **Työnimikkeen aihe** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="6f26f-119">Voit mukauttaa aiheriviä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="6f26f-120">Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="6f26f-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="6f26f-121">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6f26f-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6f26f-122">Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="6f26f-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6f26f-123">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6f26f-124">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="6f26f-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6f26f-125">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="6f26f-126">Aiherivin käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6f26f-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="6f26f-127">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6f26f-128">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6f26f-129">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="6f26f-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6f26f-130">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6f26f-131">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 3 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6f26f-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="6f26f-132">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-132">Click **Close**.</span></span>

5.  <span data-ttu-id="6f26f-133">Kirjoita ohjeet **Työnimikkeen ohjeet** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="6f26f-134">Voit mukauttaa ohjeita lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="6f26f-135">Kun käyttäjät tarkastelevat ohjeita, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="6f26f-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="6f26f-136">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6f26f-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6f26f-137">Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="6f26f-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6f26f-138">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6f26f-139">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="6f26f-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6f26f-140">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="6f26f-141">Ohjeiden käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6f26f-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="6f26f-142">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6f26f-143">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6f26f-144">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="6f26f-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6f26f-145">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6f26f-146">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 6 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6f26f-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="6f26f-147">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="6f26f-148">Tehtävän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6f26f-148">Assign the task</span></span>
<span data-ttu-id="6f26f-149">Seuraavia ohjeita noudattamalla voit määrittää käyttäjät, joille manuaalinen tehtävä määritetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1.  <span data-ttu-id="6f26f-150">Valitse vasemmasta ruudusta **Määritys**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="6f26f-151">Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 3.</span><span class="sxs-lookup"><span data-stu-id="6f26f-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6f26f-152">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6f26f-152">Option</span></span></th>
    <th><span data-ttu-id="6f26f-153">Käyttäjät, joille tehtävä on määritetty</span><span class="sxs-lookup"><span data-stu-id="6f26f-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="6f26f-154">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="6f26f-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6f26f-155">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="6f26f-155">Participant</span></span></td>
    <td><span data-ttu-id="6f26f-156">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="6f26f-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-157">Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle tehtävä määritetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="6f26f-158">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle tehtävä määritetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6f26f-159">Hierarkia</span><span class="sxs-lookup"><span data-stu-id="6f26f-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="6f26f-160">Tietyssä organisaatiohierarkiassa olevat käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-161">Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle tehtävä määritetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="6f26f-162">Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="6f26f-163">Nämä nimet edustavat käyttäjiä, joille tehtävän voi määrittää.</span><span class="sxs-lookup"><span data-stu-id="6f26f-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="6f26f-164">Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste:</span><span class="sxs-lookup"><span data-stu-id="6f26f-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="6f26f-165">Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="6f26f-166">Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f26f-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="6f26f-167">Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</span><span class="sxs-lookup"><span data-stu-id="6f26f-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="6f26f-168">Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille tehtävä määritetään:</span><span class="sxs-lookup"><span data-stu-id="6f26f-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="6f26f-169"><strong>Määritä kaikille noudetuille työntekijöille</strong> – Tehtävä määritetään joukon kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="6f26f-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="6f26f-170"><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Tehtävä määritetään vain joukon viimeiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="6f26f-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="6f26f-171"><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Tehtävää ei liitetä niille joukon käyttäjille, jotka täyttävät määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="6f26f-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="6f26f-172">Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f26f-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6f26f-173">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6f26f-173">Workflow user</span></span></td>
    <td><span data-ttu-id="6f26f-174">Nykyisen työnkulun käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6f26f-175">Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</span><span class="sxs-lookup"><span data-stu-id="6f26f-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6f26f-176">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6f26f-176">User</span></span></td>
    <td><span data-ttu-id="6f26f-177">Tietyt Microsoft Dynamics 365 for Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-178">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6f26f-179"><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="6f26f-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6f26f-180">Valitse käyttäjät, joille tehtävä liitetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="6f26f-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6f26f-181">Jono</span><span class="sxs-lookup"><span data-stu-id="6f26f-181">Queue</span></span></td>
    <td><span data-ttu-id="6f26f-182">Työnimikejono</span><span class="sxs-lookup"><span data-stu-id="6f26f-182">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-183">Valittuasi <strong>jonon</strong>, napsauta <strong>Jonoperustainen</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="6f26f-184">Voit määrittää tehtävän tiettyyn jonoon seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6f26f-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="6f26f-185">Valitse <strong>Jonon tyyppi</strong> -luettelosta <strong>Työnimikejonot</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f26f-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="6f26f-186">Valitse jono <strong>Jonon nimi</strong> -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="6f26f-187">Noudata seuraavia ohjeita, jos haluat, että tietty ehto päättää, mihin jonoon tehtävä määritetään:</span><span class="sxs-lookup"><span data-stu-id="6f26f-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="6f26f-188">Valitse <strong>Jonon tyyppi</strong> -luettelosta <strong>Ehdolliset työnimikejonot</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f26f-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="6f26f-189">Valitse <strong>Ehdollinen jono</strong> <strong>Jonon nimi</strong> -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="6f26f-190">
    <strong>Huomautus:</strong> tätä vaihtoehtoa käytetään vain muutamissa työnkuluissa, kuten Palvelupyynnön hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="6f26f-190">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="6f26f-191">Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on suorittaa tehtävä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6f26f-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="6f26f-192">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="6f26f-192">Select one of the following options:</span></span>
    -   <span data-ttu-id="6f26f-193">**Tunnit** – Määritä käyttäjän suoritusaika tunteina.</span><span class="sxs-lookup"><span data-stu-id="6f26f-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="6f26f-194">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6f26f-195">**Päivät** – Määritä käyttäjän suoritusaika päivinä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="6f26f-196">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6f26f-197">**Viikot** – Määritä käyttäjän suoritusaika viikkoina.</span><span class="sxs-lookup"><span data-stu-id="6f26f-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="6f26f-198">**Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6f26f-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="6f26f-199">Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä kuukauden kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6f26f-200">**Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6f26f-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="6f26f-201">Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä joulukuun kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="6f26f-202">Jos käyttäjä ei suorita tehtävää aikarajan puitteissa, tehtävä on erääntynyt.</span><span class="sxs-lookup"><span data-stu-id="6f26f-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="6f26f-203">Erääntyneet tehtävät voidaan eskaloida, sivun **Eskalointi**-alueessa valitsemiesi asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="6f26f-204">Erääntyneen tehtävän toimenpiteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6f26f-204">Specify what happens when the task is overdue</span></span>
<span data-ttu-id="6f26f-205">Jos käyttäjä ei suorita manuaalista tehtävää aikarajan puitteissa, tehtävä on erääntynyt.</span><span class="sxs-lookup"><span data-stu-id="6f26f-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="6f26f-206">Erääntyneen tehtävän voi eskaloida tai määrittää automaattisesti toisen käyttäjän hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="6f26f-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="6f26f-207">Seuraa näitä ohjeita, jos haluat eskaloida erääntyneet tehtävät.</span><span class="sxs-lookup"><span data-stu-id="6f26f-207">Follow these steps to escalate the task if it's overdue.</span></span>

1.  <span data-ttu-id="6f26f-208">Valitse vasemmasta ruudusta **Eskalointi**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-208">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="6f26f-209">Luo eskalointipolku valitsemalla **Käytä eskalointipolkua** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6f26f-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="6f26f-210">Järjestelmä määrittää tehtävän automaattisesti eskalointipolussa luetelluille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="6f26f-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="6f26f-211">Seuraava taulukko on esimerkki eskalointipolusta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="6f26f-212">Järjestys</span><span class="sxs-lookup"><span data-stu-id="6f26f-212">Sequence</span></span> | <span data-ttu-id="6f26f-213">Eskalointipolku</span><span class="sxs-lookup"><span data-stu-id="6f26f-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="6f26f-214">1</span><span class="sxs-lookup"><span data-stu-id="6f26f-214">1</span></span>        | <span data-ttu-id="6f26f-215">Määritä rooliin: Donna</span><span class="sxs-lookup"><span data-stu-id="6f26f-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="6f26f-216">2</span><span class="sxs-lookup"><span data-stu-id="6f26f-216">2</span></span>        | <span data-ttu-id="6f26f-217">Määritä rooliin: Erin</span><span class="sxs-lookup"><span data-stu-id="6f26f-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="6f26f-218">3</span><span class="sxs-lookup"><span data-stu-id="6f26f-218">3</span></span>        | <span data-ttu-id="6f26f-219">Viimeinen toimi: Hylkäys</span><span class="sxs-lookup"><span data-stu-id="6f26f-219">Final action: Reject</span></span> |

    <span data-ttu-id="6f26f-220">Tässä esimerkissä järjestelmä määrittää erääntyneen tehtävän Donnalle.</span><span class="sxs-lookup"><span data-stu-id="6f26f-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="6f26f-221">Jos Donna ei suorita tehtävää ajoissa, tehtävä määritetään Erinille.</span><span class="sxs-lookup"><span data-stu-id="6f26f-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="6f26f-222">Jos Erinkään ei suorita tehtävää määräajassa, järjestelmä hylkää käsittelyyn lähetetyn asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>
3.  <span data-ttu-id="6f26f-223">Voit lisätä käyttäjän eskalointipolkuun valitsemalla **Lisää eskalaatio**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="6f26f-224">Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 4.</span><span class="sxs-lookup"><span data-stu-id="6f26f-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6f26f-225">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6f26f-225">Option</span></span></th>
    <th><span data-ttu-id="6f26f-226">Käyttäjät, joille tehtävä eskaloidaan</span><span class="sxs-lookup"><span data-stu-id="6f26f-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="6f26f-227">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="6f26f-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6f26f-228">Hierarkia</span><span class="sxs-lookup"><span data-stu-id="6f26f-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="6f26f-229">Tietyssä organisaatiohierarkiassa olevat käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-229">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-230">Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle tehtävä eskaloidaan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="6f26f-231">Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="6f26f-232">Nämä nimet edustavat käyttäjiä, joille tehtävän voi eskaloida.</span><span class="sxs-lookup"><span data-stu-id="6f26f-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="6f26f-233">Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste:</span><span class="sxs-lookup"><span data-stu-id="6f26f-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="6f26f-234">Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="6f26f-235">Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f26f-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="6f26f-236">Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</span><span class="sxs-lookup"><span data-stu-id="6f26f-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="6f26f-237">Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille tehtävä eskaloidaan:</span><span class="sxs-lookup"><span data-stu-id="6f26f-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="6f26f-238"><strong>Määritä kaikille noudetuille työntekijöille</strong> – Tehtävä eskaloidaan joukon kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="6f26f-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="6f26f-239"><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Tehtävä eskaloidaan vain joukon viimeiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="6f26f-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="6f26f-240"><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Tehtävää ei eskaloida niille joukon käyttäjille, jotka täyttävät määritetyn ehdon.</span><span class="sxs-lookup"><span data-stu-id="6f26f-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="6f26f-241">Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f26f-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6f26f-242">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6f26f-242">Workflow user</span></span></td>
    <td><span data-ttu-id="6f26f-243">Nykyisen työnkulun käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-243">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6f26f-244">Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</span><span class="sxs-lookup"><span data-stu-id="6f26f-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6f26f-245">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6f26f-245">User</span></span></td>
    <td><span data-ttu-id="6f26f-246">Tietyt Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-246">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-247">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6f26f-248"><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="6f26f-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6f26f-249">Valitse käyttäjät, joille tehtävä eskaloidaan ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="6f26f-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="6f26f-250">Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on suorittaa tehtävä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6f26f-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="6f26f-251">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="6f26f-251">Select one of the following options:</span></span>
    -   <span data-ttu-id="6f26f-252">**Tunnit** – Määritä käyttäjän suoritusaika tunteina.</span><span class="sxs-lookup"><span data-stu-id="6f26f-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="6f26f-253">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6f26f-254">**Päivät** – Määritä käyttäjän suoritusaika päivinä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="6f26f-255">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6f26f-256">**Viikot** – Määritä käyttäjän suoritusaika viikkoina.</span><span class="sxs-lookup"><span data-stu-id="6f26f-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="6f26f-257">**Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6f26f-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="6f26f-258">Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä kuukauden kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6f26f-259">**Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="6f26f-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="6f26f-260">Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä joulukuun kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="6f26f-261">Toista vaiheet 3 ja 4 jokaiselle käyttäjälle, joka lisätään eskalointipolkuun.</span><span class="sxs-lookup"><span data-stu-id="6f26f-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="6f26f-262">Käyttäjien järjestystä voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="6f26f-262">You can change the order of the users.</span></span>
6.  <span data-ttu-id="6f26f-263">Jos eskalointipolun käyttäjät eivät suorita tehtävää ajoissa, järjestelmä suorittaa tehtävän toimenpiteen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6f26f-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="6f26f-264">Voit määrittää järjestelmän suorittaman toimenpiteen valitsemalla **Toimenpide**-rivin ja sitten valitsemalla **Lopetustoiminto**-välilehdellä toimenpiteen.</span><span class="sxs-lookup"><span data-stu-id="6f26f-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="6f26f-265">Määritä, milloin järjestelmä suorittaa tehtävän toimenpiteen automaattisesti</span><span class="sxs-lookup"><span data-stu-id="6f26f-265">Specify when the system automatically acts on the task</span></span>
<span data-ttu-id="6f26f-266">Voit määrittää järjestelmän tekemään jonkin tietyn toiminnon automaattisesti manuaaliselle tehtävälle, kun määritetyt ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="6f26f-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="6f26f-267">Tehtävä voi esimerkiksi edellyttää, että kuluraporttiosaston jäsen tarkastaa kuitit, jotka lähetetään kuluraportin liitteenä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="6f26f-268">Yrityksen käytäntöjen mukaan tämä tehtävä on suoritettava, jos kuluraportin kokonaissumma on yli 100 USD.</span><span class="sxs-lookup"><span data-stu-id="6f26f-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="6f26f-269">Tässä skenaariossa voit määrittää järjestelmän automaattisesti merkitsemään tehtävän tilaan **Valmis**, kun kokonaissumma on pienempi kuin 100.</span><span class="sxs-lookup"><span data-stu-id="6f26f-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="6f26f-270">Noudata seuraavia ohjeita määrittääksesi, milloin järjestelmä suorittaa manuaalisen tehtävän toimenpiteen.</span><span class="sxs-lookup"><span data-stu-id="6f26f-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1.  <span data-ttu-id="6f26f-271">Valitse vasemmasta ruudusta **Automaattiset toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-271">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="6f26f-272">Merkitse **Ota käyttöön automaattiset toiminnot** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6f26f-272">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="6f26f-273">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-273">Click **Add condition**.</span></span>
4.  <span data-ttu-id="6f26f-274">Määritä ehto.</span><span class="sxs-lookup"><span data-stu-id="6f26f-274">Enter a condition.</span></span>
5.  <span data-ttu-id="6f26f-275">Kirjoita kaikki muut tarvittavat ehdot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-275">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="6f26f-276">Voit tarkistaa, onko ehdot määritetty oikein seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="6f26f-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="6f26f-277">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-277">Click **Test**.</span></span>
    2.  <span data-ttu-id="6f26f-278">Valitse tietue **Testaa työnkulun ehto** -sivun **Tarkista ehto** -alueella.</span><span class="sxs-lookup"><span data-stu-id="6f26f-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="6f26f-279">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-279">Click **Test**.</span></span> <span data-ttu-id="6f26f-280">Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="6f26f-281">Palaa **Ominaisuudet**-sivulle valitsemalla **OK** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7.  <span data-ttu-id="6f26f-282">Valitse **Automaattinen loppuunvientitoiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="6f26f-283">Määritä, milloin ilmoitukset lähetetään</span><span class="sxs-lookup"><span data-stu-id="6f26f-283">Specify when notifications are sent</span></span>
<span data-ttu-id="6f26f-284">Voit lähettää käyttäjille ilmoituksia, kun manuaalinen tehtävä on suoritettu, delegoitu, eskaloitu tai hylätty, tai kun muutosta on pyydetty.</span><span class="sxs-lookup"><span data-stu-id="6f26f-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="6f26f-285">Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="6f26f-286">Valitse vasemmasta ruudusta **Ilmoitukset**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-286">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="6f26f-287">Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:</span><span class="sxs-lookup"><span data-stu-id="6f26f-287">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="6f26f-288">**Delegoi** – Tehtävä on määritetty toiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="6f26f-288">**Delegate** – The task has been assigned to another user.</span></span>
    -   <span data-ttu-id="6f26f-289">**Eskaloi** – Määritetty käyttäjä ei ole suorittanut tehtävää määräajassa.</span><span class="sxs-lookup"><span data-stu-id="6f26f-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    -   <span data-ttu-id="6f26f-290">**Valmis** – Määritetty käyttäjä on suorittanut tehtävän.</span><span class="sxs-lookup"><span data-stu-id="6f26f-290">**Complete** – The assigned user has completed the task.</span></span>
    -   <span data-ttu-id="6f26f-291">**Hylkää** – Määritetty käyttäjä on hylännyt lähetetyn asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    -   <span data-ttu-id="6f26f-292">**Pyydä muutosta** – Määritetty käyttäjä on pyytänyt muutosta lähetettyyn asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3.  <span data-ttu-id="6f26f-293">Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="6f26f-293">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="6f26f-294">Kirjoita **Ilmoitusteksti**-välilehden tekstiruutuun ilmoituksen leipäteksti.</span><span class="sxs-lookup"><span data-stu-id="6f26f-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="6f26f-295">Voit mukauttaa ilmoitusta lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="6f26f-296">Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="6f26f-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="6f26f-297">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6f26f-297">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="6f26f-298">Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="6f26f-298">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6f26f-299">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-299">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6f26f-300">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="6f26f-300">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6f26f-301">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-301">Click **Insert**.</span></span>

6.  <span data-ttu-id="6f26f-302">Ilmoitusten käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6f26f-302">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="6f26f-303">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="6f26f-303">Click **Translations**.</span></span>
    2.  <span data-ttu-id="6f26f-304">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-304">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="6f26f-305">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="6f26f-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="6f26f-306">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-306">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="6f26f-307">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 5 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6f26f-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="6f26f-308">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-308">Click **Close**.</span></span>

7.  <span data-ttu-id="6f26f-309">Valitse **Vastaanottaja**-välilehdellä käyttäjät, joille ilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="6f26f-310">Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 8.</span><span class="sxs-lookup"><span data-stu-id="6f26f-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6f26f-311">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6f26f-311">Option</span></span></th>
    <th><span data-ttu-id="6f26f-312">Ilmoituksen vastaanottajat</span><span class="sxs-lookup"><span data-stu-id="6f26f-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="6f26f-313">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="6f26f-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6f26f-314">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="6f26f-314">Participant</span></span></td>
    <td><span data-ttu-id="6f26f-315">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="6f26f-315">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-316">Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="6f26f-317">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6f26f-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6f26f-318">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6f26f-318">Workflow user</span></span></td>
    <td><span data-ttu-id="6f26f-319">Nykyisen työnkulun käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-319">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="6f26f-320">Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</span><span class="sxs-lookup"><span data-stu-id="6f26f-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6f26f-321">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6f26f-321">User</span></span></td>
    <td><span data-ttu-id="6f26f-322">Tietyt Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6f26f-322">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6f26f-323">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6f26f-324"><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="6f26f-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="6f26f-325">Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="6f26f-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="6f26f-326">Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="6f26f-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="6f26f-327">Aikarajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6f26f-327">Set a time limit</span></span>
<span data-ttu-id="6f26f-328">Noudata seuraavia ohjeita, jos manuaalinen tehtävä on suoritettava tietyn ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="6f26f-328">Follow these steps if the manual task must be completed in a specific time.</span></span> 

<span data-ttu-id="6f26f-329">**Huomautus:** näiden ohjeiden mukaan valitsemasi asetukset korvaavat asetukset, jotka olet valinnut kunkin hyväksyntävaiheen **Liitos**- ja **Eskalointi**-alueissa.</span><span class="sxs-lookup"><span data-stu-id="6f26f-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="6f26f-330">Napsauta vasemmassa ruudussa **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="6f26f-331">Merkitse **Aseta aikaraja työnkulun elementille** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6f26f-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="6f26f-332">Valitse **Kesto**-kenttään, aika, johon mennessä tehtävä on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6f26f-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="6f26f-333">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="6f26f-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="6f26f-334">**Tunnit** – Määritä tuntien määrä, jonka aikana tehtävän tulee olla valmis.</span><span class="sxs-lookup"><span data-stu-id="6f26f-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="6f26f-335">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6f26f-336">**Päivät** – Määritä päivien määrä, jonka aikana tehtävän tulee olla valmis.</span><span class="sxs-lookup"><span data-stu-id="6f26f-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="6f26f-337">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6f26f-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6f26f-338">**Viikot** – Määritä viikkojen määrä, jonka aikana tehtävän tulee olla valmis.</span><span class="sxs-lookup"><span data-stu-id="6f26f-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    -   <span data-ttu-id="6f26f-339">**Kuukaudet** – Valitse päivä ja viikko, johon mennessä tehtävä on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6f26f-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="6f26f-340">Voit esimerkiksi määrittää, että tehtävä on oltava valmis kuukauden kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6f26f-341">**Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä tehtävän tulee olla valmis.</span><span class="sxs-lookup"><span data-stu-id="6f26f-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="6f26f-342">Voit esimerkiksi määrittää, että tehtävän on oltava valmis joulukuun kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6f26f-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="6f26f-343">Jos aikaraja ylittyy, järjestelmä suorittaa automaattisesti tehtävälle toiminnon.</span><span class="sxs-lookup"><span data-stu-id="6f26f-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="6f26f-344">Valitse **Toiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="6f26f-345">Määritä käyttäjän käytettävissä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="6f26f-345">Specify which actions are available to the user</span></span>
<span data-ttu-id="6f26f-346">Kun manuaalinen tehtävä on määritetty käyttäjälle, käyttäjän pitää suorittaa tehtävälle toiminto.</span><span class="sxs-lookup"><span data-stu-id="6f26f-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="6f26f-347">Noudata seuraavia ohjeita määrittääksesi, mitä toimintoja käyttäjät voivat tehdä tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="6f26f-347">Follow these steps to specify which actions the user can take on the task.</span></span> <span data-ttu-id="6f26f-348">**Huomautus:** käytettävissä olevat toiminnot vaihtelevat sen mukaan, miten tehtävä on suunniteltu.</span><span class="sxs-lookup"><span data-stu-id="6f26f-348">**Note:** The actions that are available vary, depending on the design of the task.</span></span>

1.  <span data-ttu-id="6f26f-349">Napsauta vasemmassa ruudussa **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-349">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="6f26f-350">Valitse **Valmis**-valintaruutu, jos haluat, että käyttäjä voi merkitä tehtävän **valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="6f26f-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3.  <span data-ttu-id="6f26f-351">Valitse **Hylkää** -valintaruutu, jos haluat, että käyttäjä voi hylätä lähetetyn asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4.  <span data-ttu-id="6f26f-352">Valitse **Pyydä muutosta** -valintaruutu, jos haluat, että käyttäjä voi pyytää muutosta lähetettyyn asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6f26f-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5.  <span data-ttu-id="6f26f-353">Valitse **Delegoi**-valintaruutu, jos haluat, että käyttäjä voi määrittää tehtävän toiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="6f26f-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6.  <span data-ttu-id="6f26f-354">Valitse **Määritä uudelleen**-valintaruutu, jos haluat, että käyttäjä voi määrittää tehtävän uudelleen toiselle käyttäjälle työnimikejonossa.</span><span class="sxs-lookup"><span data-stu-id="6f26f-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7.  <span data-ttu-id="6f26f-355">Valitse **Vapauta**-valintaruutu, jos haluat, että käyttäjä voi vapauttaa tehtävän työnimikejonoon.</span><span class="sxs-lookup"><span data-stu-id="6f26f-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="6f26f-356">Toinen käyttäjä voi sitten suorittaa tehtävän.</span><span class="sxs-lookup"><span data-stu-id="6f26f-356">Another user can then complete the task.</span></span>





