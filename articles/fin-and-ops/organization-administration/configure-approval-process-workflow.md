---
title: "Hyväksyntäprosessin lisääminen työnkulkuun"
description: "Määritä hyväksyntäprosessin ominaisuudet seuraavan menettelyn avulla."
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
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7a7770abf84d8f3c77e348c6aedb785dcb8ea28b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="configure-an-approval-process-in-a-workflow"></a><span data-ttu-id="6e6dc-103">Hyväksyntäprosessin lisääminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="6e6dc-103">Configure an approval process in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e6dc-104">Määritä hyväksyntäprosessin ominaisuudet seuraavan menettelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="6e6dc-105">Hyväksyntäprosessi konfiguroidaan työnkulkueditorissa napsauttamalla hyväksyntäelementtiä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, mikä avaa **Ominaisuudet**-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="6e6dc-106">Hyväksyntäprosessin nimeäminen</span><span class="sxs-lookup"><span data-stu-id="6e6dc-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="6e6dc-107">Seuraavia ohjeita noudattamalla voit nimetä hyväksyntäprosessin.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="6e6dc-108">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6e6dc-109">Kirjoita hyväksyntäprosessin yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="6e6dc-110">Määritä, milloin järjestelmä käsittelee asiakirjaa automaattisesti</span><span class="sxs-lookup"><span data-stu-id="6e6dc-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="6e6dc-111">Voit määrittää järjestelmän siten, että se käsittelee automaattisesti asiakirjan, jos tietyt ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="6e6dc-112">Järjestelmä voi hyväksyä esimerkiksi kuluraportit, joiden kokonaissummat ovat alle 100 USD.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="6e6dc-113">Noudata seuraavia ohjeita määrittääksesi, milloin järjestelmä käsittelee asiakirjaa.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="6e6dc-114">Valitse vasemmasta ruudusta **Automaattiset toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="6e6dc-115">Merkitse **Ota käyttöön automaattiset toiminnot** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="6e6dc-116">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="6e6dc-117">Määritä ehto.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-117">Enter a condition.</span></span>
5.  <span data-ttu-id="6e6dc-118">Voit tarvittaessa määrittää useita ehtoja.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="6e6dc-119">Voit tarkistaa, onko ehdot määritetty oikein käymällä läpi seuraavat ohjeet:</span><span class="sxs-lookup"><span data-stu-id="6e6dc-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="6e6dc-120">Valitse **Testi**, jolloin **Testaa työnkulun ehto** -lomake tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="6e6dc-121">Valitse tietue lomakkeen **Tarkista ehto** -alueelta.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="6e6dc-122">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-122">Click **Test**.</span></span> <span data-ttu-id="6e6dc-123">Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="6e6dc-124">Palaa **Ominaisuudet**-lomakkeeseen valitsemalla **OK** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="6e6dc-125">Valitse **Automaattinen loppuunvientitoiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan asiakirjalle.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="6e6dc-126">Määritä, milloin ilmoitukset lähetetään</span><span class="sxs-lookup"><span data-stu-id="6e6dc-126">Specify when notifications are sent</span></span>
<span data-ttu-id="6e6dc-127">Voit lähettää käyttäjille ilmoituksia, kun asiakirja on hyväksytty, hylätty, delegoitu tai eskaloitu, tai kun muutosta on pyydetty.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="6e6dc-128">Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="6e6dc-129">Valitse vasemmasta ruudusta **Ilmoitukset**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="6e6dc-130">Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:</span><span class="sxs-lookup"><span data-stu-id="6e6dc-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="6e6dc-131">**Delegoi** : asiakirja on annettu toiselle käyttäjälle hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="6e6dc-132">**Eskaloi** : kun määritetty käyttäjä ei ole reagoinut asiakirjaan määritetyn ajanjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="6e6dc-133">**Hyväksy** : kun asiakirja on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="6e6dc-134">**Hylkää** : kun asiakirja on hyläytty.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="6e6dc-135">**Pyydä muutosta**: kun määritetty käyttäjä on pyytänyt muutosta lähetettyyn asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="6e6dc-136">Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="6e6dc-137">Valitse **Ilmoitusteksti**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="6e6dc-138">Kirjoita tekstiruutuun ilmoitusteksti.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="6e6dc-139">Voit mukauttaa tekstiä lisäämällä siihen paikkamerkkejä, jotka korvataan sopivilla tiedoilla, kun ne näytetään käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="6e6dc-140">Paikkamerkkejä voit lisätä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6e6dc-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="6e6dc-141">Napsauta tekstiruutua kohdassa, johon haluat lisätä paikkamerkin.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="6e6dc-142">Napsauta **Lisää paikkamerkki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="6e6dc-143">Valitse näyttöön tulevasta luettelosta lisättävä paikkamerkki.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="6e6dc-144">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="6e6dc-145">Ilmoitusten käännökset voit lisätä valitsemalla **Käännökset**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="6e6dc-146">Käy näyttöön tulevassa lomakkeessa läpi seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="6e6dc-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="6e6dc-147">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="6e6dc-148">Valitse näyttöön tulevasta luettelosta kieli, jolla kirjoitat tekstin.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="6e6dc-149">Kirjota tekstisi **Käännetty teksti** -tekstiruutuun.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="6e6dc-150">Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="6e6dc-151">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-151">Click **Close**.</span></span>

8.  <span data-ttu-id="6e6dc-152">Valitse **Vastaanottaja**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="6e6dc-153">Määritä, kenelle ilmoitukset lähetetään</span><span class="sxs-lookup"><span data-stu-id="6e6dc-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="6e6dc-154">Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 10.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6e6dc-155">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6e6dc-155">Option</span></span></th>
    <th><span data-ttu-id="6e6dc-156">Ilmoituksen vastaanottajat</span><span class="sxs-lookup"><span data-stu-id="6e6dc-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="6e6dc-157">Lisävaiheet</span><span class="sxs-lookup"><span data-stu-id="6e6dc-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="6e6dc-158"><strong>Osallistuja</strong></span><span class="sxs-lookup"><span data-stu-id="6e6dc-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="6e6dc-159">Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</span><span class="sxs-lookup"><span data-stu-id="6e6dc-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6e6dc-160">Valittuasi <strong>Osanottaja</strong> napsauta <strong>Rooliperustainen</strong>-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="6e6dc-161">Valitse <strong>Osallistujan tyyppi</strong>-luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="6e6dc-162">Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="6e6dc-163"><strong>Työnkulun käyttäjä</strong></span><span class="sxs-lookup"><span data-stu-id="6e6dc-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="6e6dc-164">Nykyiseen työnkulkuun osallistuvat käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6e6dc-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6e6dc-165">Valittuasi <strong>Työnkulun käyttäjä</strong> napsauta <strong>Työnkulun käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="6e6dc-166">Valitse <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="6e6dc-167"><strong>Käyttäjä</strong></span><span class="sxs-lookup"><span data-stu-id="6e6dc-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="6e6dc-168">Tietyt Microsoft Dynamics 365 for Finance and Operations -käyttäjät</span><span class="sxs-lookup"><span data-stu-id="6e6dc-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="6e6dc-169">Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="6e6dc-170"><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Microsoft Dynamics 365 for Finance and Operations -käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="6e6dc-171">Valitse käyttäjät, joille ilmoituksia lähetetään, ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="6e6dc-172">Toista vaiheet 3-9 kullekin tapahtumalle, jonka valitsit vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="6e6dc-173"> Lopullisen hyväksyjän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6e6dc-173">Specify a final approver</span></span>
<span data-ttu-id="6e6dc-174">Voit halutessasi määrittää lopullisen hyväksyjän skenaarioissa, joissa hyväksyjä on henkilö, joka lähetti asiakirjan hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="6e6dc-175">Määritä lopullinen hyväksyjä käymällä läpi seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="6e6dc-176">Napsauta vasemmassa ruudussa **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="6e6dc-177">Valitse **Käytä lopullista hyväksyjää** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="6e6dc-178">Valitse luettelosta käyttäjä, joka on lopullinen hyväksyjä.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="6e6dc-179">Aikarajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6e6dc-179">Set a time limit</span></span>
<span data-ttu-id="6e6dc-180">Noudata seuraavia ohjeita, jos hyväksyntäprosessi on suoritettava tietyn ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

| <span data-ttu-id="6e6dc-181">**Huomautus**</span><span class="sxs-lookup"><span data-stu-id="6e6dc-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6dc-182">Tässä vaiheessa valitsemasi asetukset korvaavat asetukset, jotka olet valinnut kunkin hyväksyntävaiheen **Määritys**- ja **Eskalointi**-kohdissa.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="6e6dc-183">Napsauta vasemmassa ruudussa **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="6e6dc-184">Valitse **Aseta aikaraja työnkulun****elementille** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="6e6dc-185">Merkitse **Kesto**-kenttään aika, johon mennessä hyväksyntäprosessi on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="6e6dc-186">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="6e6dc-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="6e6dc-187">**Tunti**: Määritä tuntimäärä, jonka kuluessa hyväksyntäprosessi on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="6e6dc-188">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6e6dc-189">**Päivä**: Määritä päivien lukumäärä, jonka kuluessa hyväksyntäprosessi on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="6e6dc-190">Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="6e6dc-191">**Viikko**: Määritä viikkomäärä, jonka kuluessa hyväksyntäprosessi on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="6e6dc-192">**Kuukausi** – Valitse päivä ja viikko, johon mennessä hyväksyntäprosessi on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="6e6dc-193">Voit esimerkiksi määrittää, että hyväksyntäprosessi on suoritettava kuukauden kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="6e6dc-194">**Vuosi** – Valitse päivä, viikko ja kuukausi, johon mennessä hyväksyntäprosessi on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="6e6dc-195">Voit esimerkiksi määrittää, että hyväksyntäprosessi on suoritettava joulukuun kolmannen viikon perjantaihin mennessä.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="6e6dc-196">Jos aikaraja ylittyy, järjestelmä käsittelee asiakirjan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="6e6dc-197">Valitse **Toiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="6e6dc-198">Määritä käyttäjän käytettävissä olevat toiminnot</span><span class="sxs-lookup"><span data-stu-id="6e6dc-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="6e6dc-199">Kun asiakirja on määritetty käyttäjälle hyväksymistä varten, käyttäjän pitää suorittaa asiakirjan toimenpide.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="6e6dc-200">Käy läpi seuraavat vaiheet määrittääksesi, mitä toimintoja käyttäjät voivat tehdä lähetetylle asiakirjalle.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="6e6dc-201">Napsauta vasemmassa ruudussa **Lisäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="6e6dc-202">Valitse **Hyväksy** -valintaruutu, jos haluat, että käyttäjä voi hyväksyä asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="6e6dc-203">Valitse **Hylkää** -valintaruutu, jos haluat, että käyttäjä voi hylätä asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="6e6dc-204">Valitse **Pyydä muutosta** -valintaruutu, jos haluat, että käyttäjä voi pyytää muutoksia asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="6e6dc-205">Valitse **Delegoi** -valintaruutu, jos haluat, että käyttäjä voi määrittää asiakirjan hyväksyttäväksi toiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="6e6dc-206">**Huomautus**: **Ota työluettelon toiminnot käyttöön yritysportaalissa** -valintaruutu on poistettu.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="6e6dc-207"> Hyväksyntävaiheiden konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="6e6dc-207">Configure the approval steps</span></span>
<span data-ttu-id="6e6dc-208">Hyväksyntäprosessi koostuu hyväksymisvaiheista.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="6e6dc-209">Lisää hyväksyntäprosessiin vaiheita ja määritä vaiheet tekemällä seuraava menettely.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="6e6dc-210">Kaksoisnapsauta hyväksyntäprosessia työnkulun editorissa.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="6e6dc-211">Työnkulun editori näyttää hyväksyntäprosessin vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="6e6dc-212">Hyväksyntävaihe lisätään vetämällä vaihe **Työnkulun elementit** -alueelta alustalle.</span><span class="sxs-lookup"><span data-stu-id="6e6dc-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="6e6dc-213">Lisätietoja hyväksyntävaiheen konfiguroimisesta on kohdassa [Hyväksyntävaiheen konfiguroiminen](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="6e6dc-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>






