---
title: Kompensaatiorakenteen kehittäminen
description: Tässä artikkelissa kerrotaan kiinteän kompensaatiosuunnitelman luomisesta ja siitä, miten työntekijät voivat rekisteröityä suunnitelmaan oikeutussääntöjen avulla.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: de715b7fda2f1548f2f443b9e0f6d09f5b881d61
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2020
ms.locfileid: "3034260"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="2bbac-103">Kompensaatiorakenteen kehittäminen</span><span class="sxs-lookup"><span data-stu-id="2bbac-103">Develop a compensation structure</span></span>

<span data-ttu-id="2bbac-104">Tässä artikkelissa kerrotaan kiinteän kompensaatiosuunnitelman luomisesta ja siitä, miten työntekijät voivat rekisteröityä suunnitelmaan oikeutussääntöjen avulla.</span><span class="sxs-lookup"><span data-stu-id="2bbac-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="2bbac-105">Tässä artikkelissa käytetään USMF-esittelytietoja. Artikkeli on tarkoitettu kompensaatio- ja etuuspäälliköille.</span><span class="sxs-lookup"><span data-stu-id="2bbac-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="2bbac-106">Luo kiinteä kompensaatiosuunnitelma</span><span class="sxs-lookup"><span data-stu-id="2bbac-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="2bbac-107">Valitse **Kompensaation hallinta**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="2bbac-108">Valitse **Kiinteät kompensaatiosuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="2bbac-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-109">Select **New**.</span></span>

4. <span data-ttu-id="2bbac-110">Anna **Suunnitelma**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2bbac-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="2bbac-111">Anna arvo **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2bbac-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="2bbac-112">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2bbac-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="2bbac-113">Määritä **Tyyppi**-kentässä, onko kiinteä kompensaatiosuunnitelma **kompensaatioluokka**-, **palkkaluokka**- vai **vaihesuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="2bbac-114">**Suositus sallitaan** -valintaruutu toimii minkä tahansa käsittelytapahtumassa tähän suunnitelmaan lisätyn toiminnon oletusarvona.</span><span class="sxs-lookup"><span data-stu-id="2bbac-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="2bbac-115">Jos suositukset ovat käytössä, voit korvata lasketun ohjeellisen summan kompensaation käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2bbac-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="2bbac-116">**Alueen ulkopuolisuuden toleranssi** -kentän avulla voit määrittää, miten annetun tason määritetyn kompensaatiorakenteen alueen ulkopuolella olevia kompensaatiosummia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="2bbac-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="2bbac-117">Kun määrität **Alueen ulkopuolisuuden toleranssi** -kentän arvoksi **Ei mitään**, voit käyttää mitä tahansa kompensaatiosummaa.</span><span class="sxs-lookup"><span data-stu-id="2bbac-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="2bbac-118">**Alustava toleranssi** varoittaa käyttäjää, jos kompensaatiosumma on pienempi kuin vähimmäisviitepisteen summa tai suurempi kuin tason enimmäissumma.</span><span class="sxs-lookup"><span data-stu-id="2bbac-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="2bbac-119">Käyttäjät voivat ohittaa varoituksen ja jatkaa.</span><span class="sxs-lookup"><span data-stu-id="2bbac-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="2bbac-120">**Kiinteä toleranssi** luo virheen, jos työntekijän kompensaatio on tason vähimmäis- ja enimmäisviitepisteen ulkopuolella. Se muokkaa työntekijän kompensaatiota automaattisesti niin, että se kuuluu alueeseen.</span><span class="sxs-lookup"><span data-stu-id="2bbac-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="2bbac-121">**Työhönottosääntö**-kenttä laskee työntekijän kompensaation tapahtuman käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="2bbac-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="2bbac-122">**Työhönottosääntö**, joka on **Prosentti**,  laskee nousun, joka jaetaan sille ajalle, jonka työntekijä on työskennellyt syklissä.</span><span class="sxs-lookup"><span data-stu-id="2bbac-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="2bbac-123">Kirjoita arvo **Valuutta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2bbac-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="2bbac-124">Syötä tai valitse arvo **Palkkion muunnos** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2bbac-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="2bbac-125">Laajenna **Palkka-alueen käyttöastematriisi** -osa.</span><span class="sxs-lookup"><span data-stu-id="2bbac-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="2bbac-126">Vaihtoehtoisesti voit lisätä alueen käyttöasteen tietueita, jos haluat työntekijöiden saavuttavan alueen keskipisteen nopeammin ja maksimin hitaammin.</span><span class="sxs-lookup"><span data-stu-id="2bbac-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="2bbac-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-127">Select **Save**.</span></span> <span data-ttu-id="2bbac-128">**Määritä kompensaatio** -painike tulee käyttöön. Tämän jälkeen voit jatkaa suunnitelman kompensaatiorakenteen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="2bbac-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="2bbac-129">Valitse **Määritä kompensaatio**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-129">Select **Set up compensation**.</span></span> <span data-ttu-id="2bbac-130">Voit luoda kompensaatiorakenteen jollakin seuraavista kolmesta tavasta:</span><span class="sxs-lookup"><span data-stu-id="2bbac-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="2bbac-131">Luo kokonaan uusi rakenne valitsemalla viitepisteet ja lisäämällä tasot, joiden avulla oma rakenne luodaan.</span><span class="sxs-lookup"><span data-stu-id="2bbac-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="2bbac-132">Kopioi aiemmin luodun suunnitelman kompensaatiorakenne aloituskohdaksi ja muokkaa uusi suunnitelma sen avulla.</span><span class="sxs-lookup"><span data-stu-id="2bbac-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="2bbac-133">Valitse aiemmin luotu kompensaatioruudukko.</span><span class="sxs-lookup"><span data-stu-id="2bbac-133">Select an existing compensation grid.</span></span> <span data-ttu-id="2bbac-134">Jos toinen suunnitelma jo käyttää kompensaatioruudukkoa, ruudukkoon tehdyt muutokset vaikuttavat myös tähän suunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="2bbac-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="2bbac-135">Valitse **Luo aiemmin luodusta kompensaatiomatriisista uusi matriisi**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="2bbac-136">Anna arvo **Kopioi ruudukosta** -kenttään tai valitse siihen arvo.</span><span class="sxs-lookup"><span data-stu-id="2bbac-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="2bbac-137">Vaihtoehtoisesti voit muuttaa valitun ruudukon kopioksi luotavan uuden kompensaatioruudukon nimen.</span><span class="sxs-lookup"><span data-stu-id="2bbac-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="2bbac-138">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-138">Select **OK**.</span></span>

19. <span data-ttu-id="2bbac-139">Valitse **Joukkomuutos**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-139">Select **Mass change**.</span></span> <span data-ttu-id="2bbac-140">**Joukkomuutostoiminnon** avulla voit ylläpitää kompensaatiomatriisin summia kohdistamalla prosentin tai kiinteän summan lisäyksen vähintään yhteen tasoon tai viitepisteeseen.</span><span class="sxs-lookup"><span data-stu-id="2bbac-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="2bbac-141">Anna **Oikaisusumma**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2bbac-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="2bbac-142">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2bbac-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="2bbac-143">Valitse **Käytä ruudukossa**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="2bbac-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2bbac-144">Close the page.</span></span> <span data-ttu-id="2bbac-145">Kun kompensaatiorakenne on luotu, voit valita kiinteän kompensaatiosuunnitelman tarkistuspisteinä käytettävät viitepisteet.</span><span class="sxs-lookup"><span data-stu-id="2bbac-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="2bbac-146">Tarkistuspistettä käytetään laskettaessa työntekijän kompensaatioastetta.</span><span class="sxs-lookup"><span data-stu-id="2bbac-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="2bbac-147">Anna arvo **Tarkistuspiste**-kenttään tai valitse siinä arvo.</span><span class="sxs-lookup"><span data-stu-id="2bbac-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="2bbac-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2bbac-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="2bbac-149">Oikeutussäännön luominen kiinteälle kompensaatiosuunnitelmalle</span><span class="sxs-lookup"><span data-stu-id="2bbac-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="2bbac-150">Uutta kiinteää kompensaatiosuunnitelmaa ei voi liittää työntekijään, ennen kuin suunnitelmalle on määritetty oikeutussäännöt.</span><span class="sxs-lookup"><span data-stu-id="2bbac-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="2bbac-151">Valitse **Oikeutussäännöt**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="2bbac-152">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2bbac-152">Select **New**.</span></span>

3. <span data-ttu-id="2bbac-153">Anna arvo **Oikeutus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2bbac-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="2bbac-154">Anna arvo **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2bbac-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="2bbac-155">Syötä päivämäärä **Voimaantulopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2bbac-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="2bbac-156">Oikeutussääntöjä käytetään sekä kiinteissä että muuttuvissa kompensaatiosuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="2bbac-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="2bbac-157">Valitse **Tyyppi**-kentässä suunnitelman tyyppi.</span><span class="sxs-lookup"><span data-stu-id="2bbac-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="2bbac-158">Anna tai valitse **Suunnitelma**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="2bbac-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="2bbac-159">Valitse ehdot, jotka työntekijän on täytettävä, ennen kuin hän on oikeutettu kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="2bbac-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="2bbac-160">Ehtoja voivat olla seuraavat:</span><span class="sxs-lookup"><span data-stu-id="2bbac-160">Criteria can include:</span></span>

    - <span data-ttu-id="2bbac-161">**Osasto**</span><span class="sxs-lookup"><span data-stu-id="2bbac-161">**Department**</span></span>
    - <span data-ttu-id="2bbac-162">**Ammattijärjestö**</span><span class="sxs-lookup"><span data-stu-id="2bbac-162">**Labor union**</span></span>
    - <span data-ttu-id="2bbac-163">**Sijainti** (**kompensaation alue**)</span><span class="sxs-lookup"><span data-stu-id="2bbac-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="2bbac-164">**Työ**</span><span class="sxs-lookup"><span data-stu-id="2bbac-164">**Job**</span></span>
    - <span data-ttu-id="2bbac-165">**Toiminto**</span><span class="sxs-lookup"><span data-stu-id="2bbac-165">**Function**</span></span>
    - <span data-ttu-id="2bbac-166">**Työlaji**</span><span class="sxs-lookup"><span data-stu-id="2bbac-166">**Job type**</span></span>
    - <span data-ttu-id="2bbac-167">**Kompensaatiotaso**</span><span class="sxs-lookup"><span data-stu-id="2bbac-167">**Compensation level**</span></span>
    
    <span data-ttu-id="2bbac-168">Työntekijän on täytettävä kaikki määritetyt ehdot, jotta hän on oikeutettu kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="2bbac-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="2bbac-169">Jos et määritä ehtoja, kaikki työntekijät ovat oikeutettuja kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="2bbac-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="2bbac-170">Jos työntekijä ei täytä oikeutussäännön määrittämiä ehtoja tai jos kompensaatiosuunnitelmalle ei ole määritetty oikeutussääntöä, kompensaatiosuunnitelma ei ole valittavissa, kun työntekijälle luodaan kiinteää kompensaatiotietuetta.</span><span class="sxs-lookup"><span data-stu-id="2bbac-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="2bbac-171">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2bbac-171">Close the page.</span></span>

8. <span data-ttu-id="2bbac-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2bbac-172">Close the page.</span></span>
