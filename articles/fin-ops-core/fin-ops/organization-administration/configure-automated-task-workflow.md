---
title: Automaattisten tehtävien määrittäminen työnkulkuun
description: Tässä ohjeaiheessa kerrotaan, miten automaattisen tehtävän ominaisuudet määritetään.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c02b4ff61b5b1f1e69d7fc0d537fe5ce535a430
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190232"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="c8bfc-103">Automaattisten tehtävien määrittäminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="c8bfc-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8bfc-104">Tässä ohjeaiheessa kerrotaan, miten automaattisen tehtävän ominaisuudet määritetään.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="c8bfc-105">Automaattinen tehtävä konfiguroidaan työnkulkueditorissa napsauttamalla tehtävää hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c8bfc-106">Sitten voit määrittää seuraavien ohjeiden avulla automaattisen tehtävän ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="c8bfc-107">Tehtävän nimeäminen</span><span class="sxs-lookup"><span data-stu-id="c8bfc-107">Name the task</span></span>

<span data-ttu-id="c8bfc-108">Kirjoita näiden ohjeiden avulla nimi automaattiselle tehtävälle.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="c8bfc-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c8bfc-110">Kirjoita tehtävän yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c8bfc-111">Määritä, milloin ilmoitukset lähetetään</span><span class="sxs-lookup"><span data-stu-id="c8bfc-111">Specify when notifications are sent</span></span>

<span data-ttu-id="c8bfc-112">Voit lähettää käyttäjille ilmoituksia, kun automaattinen tehtävä on suoritettu tai peruutettu.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="c8bfc-113">Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="c8bfc-114">Valitse vasemmasta ruudusta **Ilmoitukset**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="c8bfc-115">Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:</span><span class="sxs-lookup"><span data-stu-id="c8bfc-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="c8bfc-116">**Suoritus** – Ilmoitus lähetetään, kun tehtävä on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="c8bfc-117">**Peruutettu** – Ilmoitus lähetetään, kun tehtävä on peruutettu.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="c8bfc-118">Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="c8bfc-119">Kirjoita **Ilmoitusteksti**-välilehden tekstiruutuun ilmoituksen leipäteksti.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="c8bfc-120">Voit mukauttaa ilmoitusta lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="c8bfc-121">Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="c8bfc-122">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c8bfc-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="c8bfc-123">Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c8bfc-124">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c8bfc-125">Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c8bfc-126">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-126">Click **Insert**.</span></span>

6. <span data-ttu-id="c8bfc-127">Ilmoitusten käännökset voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="c8bfc-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="c8bfc-128">Napsauta **Käännökset**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="c8bfc-129">Valitse esiin tulevalla sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="c8bfc-130">Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="c8bfc-131">Kirjota tekstisi **Käännetty teksti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c8bfc-132">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 5 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="c8bfc-133">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-133">Click **Close**.</span></span>

7. <span data-ttu-id="c8bfc-134">Valitse **Vastaanottaja**-välilehdellä käyttäjät, joille ilmoitukset lähetetään.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="c8bfc-135">Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 8.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c8bfc-136">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="c8bfc-136">Option</span></span></th>
    <th><span data-ttu-id="c8bfc-137">Ilmoituksen vastaanottajat</span><span class="sxs-lookup"><span data-stu-id="c8bfc-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="c8bfc-138">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="c8bfc-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c8bfc-139">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="c8bfc-139">Participant</span></span></td>
    <td><span data-ttu-id="c8bfc-140">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="c8bfc-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c8bfc-141">Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c8bfc-142">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c8bfc-143">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="c8bfc-143">Workflow user</span></span></td>
    <td><span data-ttu-id="c8bfc-144">Nykyiseen työnkulkuun osallistuvat käyttäjät</span><span class="sxs-lookup"><span data-stu-id="c8bfc-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="c8bfc-145">Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c8bfc-146">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="c8bfc-146">User</span></span></td>
    <td><span data-ttu-id="c8bfc-147">Tietyt käyttäjät</span><span class="sxs-lookup"><span data-stu-id="c8bfc-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c8bfc-148">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c8bfc-149"><strong>Käytettävissä olevat käyttäjät</strong> -luettelo sisältää kaikki käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="c8bfc-150">Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="c8bfc-151">Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="c8bfc-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>