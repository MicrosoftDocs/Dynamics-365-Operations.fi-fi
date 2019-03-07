---
title: Työntekijöille lainattujen kohteiden hallinta
description: Lainakohteet ovat tietueita, joiden avulla esimiehet voivat seurata yrityksen työntekijöille lainaamia fyysisiä kohteita.
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 6c22e85360c3e6e40e0338960866b96d66a0ba50
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304151"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="bc30e-103">Työntekijöille lainattujen kohteiden hallinta</span><span class="sxs-lookup"><span data-stu-id="bc30e-103">Manage items that are lent to workers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bc30e-104">Lainakohteet ovat tietueita, joiden avulla esimiehet voivat seurata yrityksen työntekijöille lainaamia fyysisiä kohteita.</span><span class="sxs-lookup"><span data-stu-id="bc30e-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="bc30e-105">Seuraavissa kohdissa on esimerkkejä kohteista, joita yritys voi lainata työntekijöille:</span><span class="sxs-lookup"><span data-stu-id="bc30e-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="bc30e-106">matkapuhelimia</span><span class="sxs-lookup"><span data-stu-id="bc30e-106">Mobile telephones</span></span>
-   <span data-ttu-id="bc30e-107">autopuhelimia</span><span class="sxs-lookup"><span data-stu-id="bc30e-107">Automobiles</span></span>
-   <span data-ttu-id="bc30e-108">tietokoneet.</span><span class="sxs-lookup"><span data-stu-id="bc30e-108">Computer equipment</span></span>

<span data-ttu-id="bc30e-109">Jokaisella fyysisellä kohteella on oltava vastaava lainakohde.</span><span class="sxs-lookup"><span data-stu-id="bc30e-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="bc30e-110">Jokaisessa lainan kohdetietueessa tulisi kuvailla, mitä lainataan, kuka vastaa lainasta sekä aika (päivinä), jonka kohde voi olla työntekijällä lainassa.</span><span class="sxs-lookup"><span data-stu-id="bc30e-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="bc30e-111">Voit luoda samalla useita lainakohteita, kuten avaimia, kulkukortteja tai työpukuja.</span><span class="sxs-lookup"><span data-stu-id="bc30e-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="bc30e-112">Kun kohde lainataan, kirjataan sen lainauspäivämäärä ja suunniteltu palautuspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="bc30e-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="bc30e-113">Kun kohde palautetaan, kirjataan todellinen palautuspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="bc30e-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="bc30e-114">Työntekijät voivat heille lainattujen kohteiden tietueita Työntekijän itsepalvelu -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="bc30e-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="bc30e-115">He voivat myös muokata aiemmin luotuja tietueita tai kirjata uusia lainakohteita, jos he saavat uusia fyysisiä kohteita.</span><span class="sxs-lookup"><span data-stu-id="bc30e-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="bc30e-116">Työnkulku voidaan määrittää reitittämään uusien ja aiemmin luotujen lainakohteiden muutokset hyväksyntäprosessin vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="bc30e-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="bc30e-117">Esimiehet voivat tarkastella suorille alaisille lainattuja kohteita.</span><span class="sxs-lookup"><span data-stu-id="bc30e-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="bc30e-118">Heille voidaan myös myöntää oikeus lisätä uusia lainakohteita työntekijöiden puolesta.</span><span class="sxs-lookup"><span data-stu-id="bc30e-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="bc30e-119"> Kadonneiden tai hävinneiden lainakohteiden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="bc30e-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="bc30e-120">Jos kohde vahingoittuu tai häviää, sille kirjataan fiktiivinen palautustietue.</span><span class="sxs-lookup"><span data-stu-id="bc30e-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="bc30e-121">Sen jälkeen kohde joko poistetaan tai jätetään yleiskatsaukseen ja muutetaan kuvausta sitten, ettei kohde ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bc30e-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="bc30e-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bc30e-122">Additional resources</span></span>
--------

[<span data-ttu-id="bc30e-123">Henkilöstö</span><span class="sxs-lookup"><span data-stu-id="bc30e-123">Human resources</span></span>](index.md)



