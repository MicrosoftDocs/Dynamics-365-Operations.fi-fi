---
title: Työnkulun työnimikkeiden delegointi
description: Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189956"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="dad49-103">Työnkulun työnimikkeiden delegointi</span><span class="sxs-lookup"><span data-stu-id="dad49-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="dad49-104">Työnimikkeen delegointi manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="dad49-104">Manually delegate a work item</span></span>

<span data-ttu-id="dad49-105">Yksittäinen työnimike voidaan delegoida valitsemalla **delegoida**-asetus **työnkulku**-valikosta, lisäämällä kommentin ja syöttämällä käyttäjän, jolle työ delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="dad49-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="dad49-106">Määrittää työnimikkeen käyttäjälle, jotta käyttäjä voi suorittaa sen loppuun.</span><span class="sxs-lookup"><span data-stu-id="dad49-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="dad49-107">Delegoi työnimikkeet automaattisesti</span><span class="sxs-lookup"><span data-stu-id="dad49-107">Automatically delegate work items</span></span>

<span data-ttu-id="dad49-108">Jos aiot olla poissa toimistosta tai et muuten ole käytettävissä tiettynä aikana, voit siirtää uusia työnimikkeitä automaattisesti muille käyttäjille käyttämällä **Käyttäjäasetukset**-sivua.</span><span class="sxs-lookup"><span data-stu-id="dad49-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="dad49-109">Automaattisen delegoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dad49-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="dad49-110">Valitse **Yhteiset > Asetukset > Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="dad49-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="dad49-111">Valitse **Työnkulku**-väli lehti. Varmista, että Delegointi-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="dad49-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="dad49-112">Luo delegointisäännöt määrittämään, milloin tietyt työnimiketyypit delegoidaan. Tällä tavoin voit määrittää järjestelmän delegoimaan työnimikkeesi automaattisesti muille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="dad49-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="dad49-113">Luo delegointisääntö seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="dad49-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="dad49-114">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="dad49-114">Click **Add**.</span></span>
4. <span data-ttu-id="dad49-115">Valitse **Vaikutusalue**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="dad49-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="dad49-116">Kaikki – delegoi kaikki sinulle määritetyt työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="dad49-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="dad49-117">Moduuli – Delegoi vain tiettyyn työnkulkutyyppiin liittyvät työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="dad49-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="dad49-118">Jos valitset tämän vaihtoehdon, työnkulkutyyppi on valittava Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dad49-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="dad49-119">Työnkulku – Delegoi vain tiettyyn työnkulkuun liittyvät työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="dad49-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="dad49-120">Jos valitset tämän vaihtoehdon, työnkulku on valittava Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dad49-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="dad49-121">Valitse **Delegoi**-kentässä käyttäjä, jolle työnimikkeet delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="dad49-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="dad49-122">Määritä Alkamispäivämäärä ja -kellonaika- ja Päättymispäivämäärä ja -kellonaika -kenttien avulla, milloin haluat delegoida työnimikkeet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="dad49-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="dad49-123">Anna päivämäärä ja kellonaika **Aloituspäivämäärä ja -kellonaika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="dad49-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="dad49-124">Anna päivämäärä ja kellonaika **Päättymispäivämäärä ja -kellonaika** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="dad49-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="dad49-125">Aktivoi tämä delegointisääntö valitsemalla **Käytössä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="dad49-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="dad49-126">Jos **Moduuli** on valittu vaikutusalueeksi, moduuli on valittava myös Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dad49-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="dad49-127">Jos **Työnkulku** on valittu vaikutusalueeksi, tietty työnkulku on valittava delegoitavaksi myös Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dad49-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="dad49-128">Selitä **Kommentti**-kentässä, miksi delegoit työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="dad49-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

