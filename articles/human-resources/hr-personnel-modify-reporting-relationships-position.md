---
title: Muokkaa toimen raportointisuhteita
description: Tässä menettelyssä näytetään, miten työntekijän raportointisuhde muutetaan.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3285222b11905999f0eadb846ac785342c16aa38
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008912"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="6e4e9-103">Muokkaa toimen raportointisuhteita</span><span class="sxs-lookup"><span data-stu-id="6e4e9-103">Modify reporting relationships for a position</span></span>



<span data-ttu-id="6e4e9-104">Tässä menettelyssä näytetään, miten työntekijän raportointisuhde muutetaan.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="6e4e9-105">Asiakirjoja voi reitittää työnkulussa raportointisuhteen avulla.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="6e4e9-106">Menettelyssä näytetään myös, miten työntekijä määritetään lisähierarkioihin.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="6e4e9-107">Työntekijä voi esimerkiksi kuulua projektiryhmään ja hänellä voi olla epävirallinen raportointisuhde projektivastaavaan.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="6e4e9-108">Toimelle voidaan määrittää lisäraportointisuhteita erilaisten projekti- tai matriisiskenaarioiden tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="6e4e9-109">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6e4e9-110">Valitse Henkilöstöhallinto > Toimet > Toimet.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="6e4e9-111">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6e4e9-112">Voit esimerkiksi suodattaa Toimi-kenttää arvolla 000091.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="6e4e9-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6e4e9-114">Laajenna Raportoi toimelle -osa.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="6e4e9-115">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="6e4e9-116">Anna tai valitse Raportoi:-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="6e4e9-117">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-117">Click Create.</span></span>
8. <span data-ttu-id="6e4e9-118">Laajenna Suhteet-osa.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="6e4e9-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-119">Click Add.</span></span>
10. <span data-ttu-id="6e4e9-120">Valitse valintaruutu ruudukossa vasemmalta.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="6e4e9-121">Anna tai valitse Hierarkian nimi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="6e4e9-122">Esimerkki: projekti</span><span class="sxs-lookup"><span data-stu-id="6e4e9-122">Example: Project</span></span>  
12. <span data-ttu-id="6e4e9-123">Anna tai valitse Raportoi toimelle -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="6e4e9-124">Esimerkki: 000437</span><span class="sxs-lookup"><span data-stu-id="6e4e9-124">Example:  000437</span></span>
13. <span data-ttu-id="6e4e9-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-125">Click Save.</span></span>

