---
title: Ostojen ja hankintojen työnkulkujen vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita voi esiintyä ostojen ja hankintojen työnkuluissa.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cdedc45b8f057310801f134104156a732fb58d86
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018534"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="ad2a6-103">Ostojen ja hankintojen työnkulkujen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="ad2a6-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="ad2a6-104">Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita voi esiintyä ostojen ja hankintojen työnkuluissa.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="ad2a6-105">Virhe lähetettäessä ostotilausta uudelleen työnkulkuun muutoksen jälkeen: "Muutokset ostotilaukseen X ovat sallittuja vain Luonnos-tilassa, kun muutoksenhallinta on käytössä"</span><span class="sxs-lookup"><span data-stu-id="ad2a6-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="ad2a6-106">Tämä ongelma ilmenee vain, jos ostotilaus oli tilassa *Vahvistettu* , ennen kuin muutoksia pyydettiin.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="ad2a6-107">Jos pyydät muutoksia ostotilauksen ollessa tilassa *Hyväksytty* , työnkulku voidaan käsitellä onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="ad2a6-108">Virheen kuvaus</span><span class="sxs-lookup"><span data-stu-id="ad2a6-108">Error description</span></span>

<span data-ttu-id="ad2a6-109">Työnkulussa tapahtuu seuraava virhe, kun ostotilaus lähetetään uudelleen muutoksen jälkeen:</span><span class="sxs-lookup"><span data-stu-id="ad2a6-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="ad2a6-110">Pysäytetty (virhe): X ++ -poikkeus: Ostotilaukseen PO0000569 tehtävät muutokset ovat sallittuja Luonnos-tilassa, vain, kun muutoksenhallinta aktivoidaan seuraavissa kohdissa:</span><span class="sxs-lookup"><span data-stu-id="ad2a6-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="ad2a6-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="ad2a6-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="ad2a6-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="ad2a6-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="ad2a6-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="ad2a6-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="ad2a6-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="ad2a6-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad2a6-115">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ad2a6-115">Issue resolution</span></span>

<span data-ttu-id="ad2a6-116">Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="ad2a6-117">Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="ad2a6-118">Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="ad2a6-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="ad2a6-119">Ongelma korjataan [tämän Microsoft Knowledge Base (KB) -artikkelin](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) avulla.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="ad2a6-120">Vähintään yksi kirjanpidollinen jako on joko yli- tai alijaettu.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="ad2a6-121">Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="ad2a6-122">Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="ad2a6-123">Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="ad2a6-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="ad2a6-124">Jos jäännösmäärä peruutetaan ostotilauksessa, jossa muutoksenhallinta on otettu käyttöön, ostotilaus siirtyy tilaan Vahvistettu.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad2a6-125">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ad2a6-125">Issue description</span></span>

<span data-ttu-id="ad2a6-126">Kun kyseessä on ostotilaus, johon sovelletaan muutoksenhallintaa ja ainoana muutoksena on jäännösmäärän peruuttaminen vähintään yhdellä rivillä, ostotilaus siirtyy suoraan *Vahvistettu* -tilaan, kun se hyväksytään, eikä kirjauskansiota luoda.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad2a6-127">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ad2a6-127">Issue resolution</span></span>

<span data-ttu-id="ad2a6-128">Jäännösmäärän peruuttaminen ei vaikuta vahvistuskirjauskansion sisältöön.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="ad2a6-129">Tätä toimintoa pitäisi käyttää, kun rivi on vastaanotettu osittain ja jäännösmäärän laatu on peruutettava prosessivaiheessa, joka seuraa toimittajan antamaa vahvistusta ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="ad2a6-130">Jos tämän pitäisi näkyä ostotilausvahvistuksessa, määrää pitäisi muokata ostotilausrivillä, jotta vahvistusta vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="ad2a6-131">Jos rivillä ei taas ole vastaanotettu mitään, määrän voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="ad2a6-132">Tällöin vaaditaan uusi vahvistus.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="ad2a6-133">Peruutetut ostotilaukset näkyvät ostotilausten valmistelutyötilan luonnosluettelossa.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad2a6-134">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="ad2a6-134">Issue description</span></span>

<span data-ttu-id="ad2a6-135">Kun olet peruuttanut *Vahvistettu* -tilassa olleita ostotilauksia, peruutetut ostotilaukset näkyvät edelleen ostotilausluonnosten luettelossa **Ostotilausten valmistelu** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad2a6-136">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ad2a6-136">Issue resolution</span></span>

<span data-ttu-id="ad2a6-137">Tämä ongelma ilmenee vain sellaisten ostotilausten osalta, joihin sovelletaan muutoksenhallintaa.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="ad2a6-138">Se johtuu siitä, että peruutus tulkitaan muutokseksi, joka on hyväksyttävä.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="ad2a6-139">Järjestelmä voi suorittaa hyväksynnän automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="ad2a6-140">siksi prosessina on peruutetun ostotilauksen lähettäminen hyväksymisen työnkulkuun, jotta se voi siirtyä *Hyväksytty* -tilaan.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="ad2a6-141">Tässä vaiheessa ostotilaus ei enää näy **Ostotilausten valmistelu** -työtilan ostotilausluonnosten luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ad2a6-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

