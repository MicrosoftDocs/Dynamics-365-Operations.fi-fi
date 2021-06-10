---
title: Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan
description: Etuuspäällikkö voi liittää työntekijöitä kiinteisiin kompensaatiosuunnitelmiin peruspalkan hallintaa varten.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5f0862c86234495c89b2a6ad947cc78e687de37
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054233"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="4bc16-103">Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="4bc16-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4bc16-104">Etuuspäällikkö voi liittää työntekijöitä kiinteisiin kompensaatiosuunnitelmiin peruspalkan hallintaa varten.</span><span class="sxs-lookup"><span data-stu-id="4bc16-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="4bc16-105">Tässä menettelyssä oletetaan, että kiinteä suunnitelma on luotu ja se on aktiivinen, ja että suunnitelmalle on määritetty oikeutussäännöt.</span><span class="sxs-lookup"><span data-stu-id="4bc16-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="4bc16-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="4bc16-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4bc16-107">Aloita menettely valitsemalla Henkilöstöhallinto > Työntekijät > Työntekijät > Kompensaatio > Kiinteä suunnitelma</span><span class="sxs-lookup"><span data-stu-id="4bc16-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="4bc16-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4bc16-108">Click New.</span></span>
2. <span data-ttu-id="4bc16-109">Valitse Toiminto-kentässä kiinteän kompensaation toiminnoksi Palkkaa / palkkaa uudelleen -tyyppi. Se kuvaa työntekijän kompensaation muutosta.</span><span class="sxs-lookup"><span data-stu-id="4bc16-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="4bc16-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4bc16-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4bc16-111">Avaa haku napsauttamalla Toimi-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4bc16-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4bc16-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4bc16-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4bc16-113">Näkyvillä oleva taso on toimen työn kompensaatiotaso.</span><span class="sxs-lookup"><span data-stu-id="4bc16-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="4bc16-114">Työlle on määritettävä taso, ennen kuin kompensaatio voidaan liittää työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="4bc16-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="4bc16-115">Valitse Suunnitelma-kentässä työntekijöille kiinteä kompensaatiosuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="4bc16-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="4bc16-116">Suunnitelman haku suodatetaan näyttämään vain suunnitelmat, joihin työntekijä on oikeutettu oikeutussääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4bc16-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="4bc16-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="4bc16-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4bc16-118">Kompensaation voimassaolopäivämäärien ja vanhenemispäivämäärien oletusarvot saadaan työntekijän toimen määrityksen aloitus- ja päättymispäivämääristä.</span><span class="sxs-lookup"><span data-stu-id="4bc16-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="4bc16-119">Päivämääriä voi muuttaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="4bc16-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="4bc16-120">Jos Kiinteä kompensaatiosuunnitelma on vaihesuunnitelma, valitse vaihe, joka sisältää työntekijän oikean palkkion.</span><span class="sxs-lookup"><span data-stu-id="4bc16-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="4bc16-121">Jos Kiinteä kompensaatiosuunnitelma on palkkaluokan tai kompensaatioluokan suunnitelma, työntekijälle oikea palkkio.</span><span class="sxs-lookup"><span data-stu-id="4bc16-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="4bc16-122">Palkkio vahvistetaan suunnitelman toleranssiasetusten ja työn kompensaatiotason vähimmäis- ja enimmäisviitepisteiden avulla.</span><span class="sxs-lookup"><span data-stu-id="4bc16-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="4bc16-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4bc16-123">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]