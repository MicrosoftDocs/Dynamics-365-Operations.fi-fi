---
title: Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan
description: Etuuspäällikkö voi rekisteröidä työntekijät muuttuvan kompensaation suunnitelmiin, kun työntekijöille lasketaan käteis- ja muut kuin käteispalkkiot.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f10164b4002d3cb83a2332e913adcb25506ffdd2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468224"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="b01aa-103">Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="b01aa-103">Enroll an employee in a variable compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b01aa-104">Etuuspäällikkö voi rekisteröidä työntekijät muuttuvan kompensaation suunnitelmiin, kun työntekijöille lasketaan käteis- ja muut kuin käteispalkkiot.</span><span class="sxs-lookup"><span data-stu-id="b01aa-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="b01aa-105">Tässä menettelyssä oletetaan, että muuttuva kompensaatiosuunnitelma on luotu niin, että Ota rekisteröinti käyttöön -kentän arvoksi on määritetty Kyllä ja muuttuvan kompensaatiosuunnitelman oikeutussäännöt on luotu.</span><span class="sxs-lookup"><span data-stu-id="b01aa-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="b01aa-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b01aa-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b01aa-107">Aloita menettely siirtymällä kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät > Kompensaatio > Muuttuvan suunnitelman rekisteröityminen.</span><span class="sxs-lookup"><span data-stu-id="b01aa-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="b01aa-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b01aa-108">Click New.</span></span>
2. <span data-ttu-id="b01aa-109">Avaa haku valitsemalla Suunnitelma-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b01aa-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b01aa-110">Suunnitelman haku suodatetaan näyttämään vain muuttuvat kompensaatiosuunnitelmat, joihin työntekijä on oikeutettu oikeutussääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="b01aa-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="b01aa-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b01aa-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b01aa-112">Ota käyttöön Yleinen-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="b01aa-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="b01aa-113">Syötä päivämäärä Voimaantulopäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b01aa-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="b01aa-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b01aa-114">Click Save.</span></span>
7. <span data-ttu-id="b01aa-115">Ota käyttöön Ohitukset-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="b01aa-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="b01aa-116">Vaihtoehtoisesti työhönottosäännön päivämäärä voi korvata työntekijän työhönottopäivämäärän, kun valitulle muuttuvalle suunnitelmalle määritetty työhönottosääntö on Prosentti.</span><span class="sxs-lookup"><span data-stu-id="b01aa-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="b01aa-117">Jos muuttuva suunnitelma on perussuunnitelman prosentti, työntekijän palkkioprosentti voidaan ohittaa.</span><span class="sxs-lookup"><span data-stu-id="b01aa-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="b01aa-118">Jos muuttuva kompensaatiosuunnitelma on yksiköiden määrän suunnitelma, työntekijän yksiköiden määrä voidaan ohittaa.</span><span class="sxs-lookup"><span data-stu-id="b01aa-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="b01aa-119">Jos työntekijälle tulee antaa kiinteä palkkiosumma, summa voidaan määrittää tässä.</span><span class="sxs-lookup"><span data-stu-id="b01aa-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="b01aa-120">Ota käyttöön Organisaation ohitukset -osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="b01aa-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="b01aa-121">Jos työntekijän suoritustaso on otettava huomioon, eri osastojen tai muun kuin työntekijän toimelle liitetyn osaston suoritustaso voidaan ohittaa.</span><span class="sxs-lookup"><span data-stu-id="b01aa-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="b01aa-122">Prosentti-sarakkeen summan on oltava 100.</span><span class="sxs-lookup"><span data-stu-id="b01aa-122">The Percent column should total 100.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]