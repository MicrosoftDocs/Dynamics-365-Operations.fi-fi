--- 
title: "Työnkulun työnimikkeiden delegointi"
description: "Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille."
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: abd59b96a2e5dceb2492c2db2c617485b332fbd3
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/13/2018

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="1c661-103">Työnkulun työnimikkeiden delegointi</span><span class="sxs-lookup"><span data-stu-id="1c661-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c661-104">Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="1c661-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="1c661-105">Tämä menettely auttaa määrittämään järjestelmän siten, että työnimikkeesi delegoidaan automaattisesti toiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="1c661-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="1c661-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="1c661-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="1c661-107">Automaattisen delegoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1c661-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="1c661-108">Valitse Yleinen > Asetukset > Käyttäjän asetukset.</span><span class="sxs-lookup"><span data-stu-id="1c661-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="1c661-109">Valitse Työnkulku-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1c661-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="1c661-110">Varmista, että Delegointi-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="1c661-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="1c661-111">Luo delegointisäännöt määrittämään, milloin tietyt työnimiketyypit delegoidaan. Tällä tavoin voit määrittää järjestelmän delegoimaan työnimikkeesi automaattisesti muille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="1c661-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="1c661-112">Luo delegointisääntö seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="1c661-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="1c661-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="1c661-113">Click Add.</span></span>
4. <span data-ttu-id="1c661-114">Valitse Vaikutusalue-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="1c661-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="1c661-115">Kaikki – delegoi kaikki sinulle määritetyt työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="1c661-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="1c661-116">Moduuli – Delegoi vain tiettyyn työnkulkutyyppiin liittyvät työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="1c661-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="1c661-117">Jos valitset tämän vaihtoehdon, työnkulkutyyppi on valittava Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c661-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="1c661-118">Työnkulku – Delegoi vain tiettyyn työnkulkuun liittyvät työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="1c661-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="1c661-119">Jos valitset tämän vaihtoehdon, työnkulku on valittava Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c661-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="1c661-120">Valitse Delegoi-kentässä käyttäjä, jolle työnimikkeet delegoidaan.</span><span class="sxs-lookup"><span data-stu-id="1c661-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="1c661-121">Määritä Alkamispäivämäärä ja -kellonaika- ja Päättymispäivämäärä ja -kellonaika -kenttien avulla, milloin haluat delegoida työnimikkeet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="1c661-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="1c661-122">Anna päivämäärä ja kellonaika Aloituspäivämäärä ja -kellonaika -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c661-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="1c661-123">Anna päivämäärä ja kellonaika Päättymispäivämäärä ja -kellonaika -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c661-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="1c661-124">Aktivoi tämä delegointisääntö valitsemalla Käytössä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1c661-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="1c661-125">Jos Moduuli on valittu vaikutusalueeksi, moduuli on valittava myös Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c661-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="1c661-126">Jos Työnkulku on valittu vaikutusalueeksi, tietty työnkulku on valittava delegoitavaksi myös Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1c661-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="1c661-127">Selitä Kommentti-kentässä, miksi delegoit työnimikkeet.</span><span class="sxs-lookup"><span data-stu-id="1c661-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


