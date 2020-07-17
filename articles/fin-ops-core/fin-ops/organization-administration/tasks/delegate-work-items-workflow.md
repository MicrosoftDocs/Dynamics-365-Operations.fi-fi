---
title: Työnkulun työnimikkeiden delegointi
description: Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515761"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="ccc05-103">Työnkulun työnimikkeiden delegointi</span><span class="sxs-lookup"><span data-stu-id="ccc05-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="ccc05-104">Työnimikkeen delegointi manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="ccc05-104">Manually delegate a work item</span></span>

<span data-ttu-id="ccc05-105">Yksittäinen työnimike voidaan delegoida valitsemalla **delegoida**-asetus **työnkulku**-valikosta, lisäämällä kommentin ja syöttämällä käyttäjän, jolle työ delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="ccc05-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="ccc05-106">Määrittää työnimikkeen käyttäjälle, jotta käyttäjä voi suorittaa sen loppuun.</span><span class="sxs-lookup"><span data-stu-id="ccc05-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="ccc05-107">Delegoi manuaalisesti useita työnimikkeitä</span><span class="sxs-lookup"><span data-stu-id="ccc05-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="ccc05-108">Useita työnimikkeitä voidaan delegoida yhteen **Minulle määritetyt työnimikkeet** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="ccc05-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="ccc05-109">Seuraavat työnkulutyypit soveltuvat joukkodelegointiin: ostosopimuksen hyväksynnän työnkulku, ostotilauksen työnkulku, ostoehdotuksen arvostelu ja toimittajan laskun työnkulku.</span><span class="sxs-lookup"><span data-stu-id="ccc05-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="ccc05-110">**Delegoi useita työnimikkeitä** -ominaisuus on oletuksena pois käytöstä, ja sen voi ottaa käyttöön kohdassa **Työtilat > Ominaisuuksien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="ccc05-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="ccc05-111">Ota yhteyttä järjestelmänvalvojaasi, jos haluat apua tämän toiminnon käyttöön ottamisessa.</span><span class="sxs-lookup"><span data-stu-id="ccc05-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="ccc05-112">Siirry kohtaan **Yleinen > Yleinen > Työnimikkeet > Minulle määritetyt työnimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="ccc05-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="ccc05-113">Valitse delegoitavat työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="ccc05-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="ccc05-114">Valitse **Delegoi työnimikkeet** -valikko.</span><span class="sxs-lookup"><span data-stu-id="ccc05-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="ccc05-115">Valitse **Käyttäjä**-kentässä käyttäjä, jolle työnimikkeet delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="ccc05-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="ccc05-116">Selitä **Kommentti**-kentässä, miksi delegoit työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="ccc05-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="ccc05-117">Viimeistele työnimikkeen delegointi napsauttamalla **Delegoi työnimikkeet** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="ccc05-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="ccc05-118">Delegoi työnimikkeet automaattisesti</span><span class="sxs-lookup"><span data-stu-id="ccc05-118">Automatically delegate work items</span></span>

<span data-ttu-id="ccc05-119">Jos aiot olla poissa toimistosta tai et muuten ole käytettävissä tiettynä aikana, voit siirtää uusia työnimikkeitä automaattisesti muille käyttäjille käyttämällä **Käyttäjäasetukset**-sivua.</span><span class="sxs-lookup"><span data-stu-id="ccc05-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="ccc05-120">Automaattisen delegoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ccc05-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="ccc05-121">Valitse **Yhteiset > Asetukset > Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="ccc05-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="ccc05-122">Valitse **Työnkulku**-väli lehti. Varmista, että Delegointi-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="ccc05-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="ccc05-123">Luo delegointisäännöt määrittämään, milloin tietyt työnimiketyypit delegoidaan. Tällä tavoin voit määrittää järjestelmän delegoimaan työnimikkeesi automaattisesti muille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="ccc05-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="ccc05-124">Luo delegointisääntö seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="ccc05-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="ccc05-125">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ccc05-125">Click **Add**.</span></span>
4. <span data-ttu-id="ccc05-126">Valitse **Vaikutusalue**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ccc05-126">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="ccc05-127">Kaikki – delegoi kaikki sinulle määritetyt työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="ccc05-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="ccc05-128">Moduuli – Delegoi vain tiettyyn työnkulkutyyppiin liittyvät työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="ccc05-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="ccc05-129">Jos valitset tämän vaihtoehdon, työnkulkutyyppi on valittava Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ccc05-129">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="ccc05-130">Työnkulku – Delegoi vain tiettyyn työnkulkuun liittyvät työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="ccc05-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="ccc05-131">Jos valitset tämän vaihtoehdon, työnkulku on valittava Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ccc05-131">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="ccc05-132">Valitse **Delegoi**-kentässä käyttäjä, jolle työnimikkeet delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="ccc05-132">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="ccc05-133">Määritä Alkamispäivämäärä ja -kellonaika- ja Päättymispäivämäärä ja -kellonaika -kenttien avulla, milloin haluat delegoida työnimikkeet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ccc05-133">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="ccc05-134">Anna päivämäärä ja kellonaika **Aloituspäivämäärä ja -kellonaika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="ccc05-134">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="ccc05-135">Anna päivämäärä ja kellonaika **Päättymispäivämäärä ja -kellonaika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="ccc05-135">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="ccc05-136">Aktivoi tämä delegointisääntö valitsemalla **Käytössä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="ccc05-136">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="ccc05-137">Jos **Moduuli** on valittu vaikutusalueeksi, moduuli on valittava myös Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ccc05-137">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="ccc05-138">Jos **Työnkulku** on valittu vaikutusalueeksi, tietty työnkulku on valittava delegoitavaksi myös Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ccc05-138">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="ccc05-139">Selitä **Kommentti**-kentässä, miksi delegoit työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="ccc05-139">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>

