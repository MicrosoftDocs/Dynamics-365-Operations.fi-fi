---
title: Määritä loman ja poissaolon tyypit
description: Määritä Dynamics 365 Human Resourcesissa lomatyypit, joita työntekijät voivat valita.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e6ca7d04b86232ba48474fcbe288a18995661ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418301"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="34877-103">Määritä loman ja poissaolon tyypit</span><span class="sxs-lookup"><span data-stu-id="34877-103">Configure leave and absence types</span></span>

<span data-ttu-id="34877-104">Lomatyypit Dynamics 365 Human Resourcesissa määrittävät erilaiset poissaolotyypit, joita työntekijät voivat ilmoittaa.</span><span class="sxs-lookup"><span data-stu-id="34877-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="34877-105">Voit räätälöidä lomatyyppejä organisaatiosi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="34877-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="34877-106">Esimerkkejä lomatyypeistä:</span><span class="sxs-lookup"><span data-stu-id="34877-106">Examples of leave types include:</span></span>

- <span data-ttu-id="34877-107">Palkallinen vapaa (PTO)</span><span class="sxs-lookup"><span data-stu-id="34877-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="34877-108">Palkaton vapaa</span><span class="sxs-lookup"><span data-stu-id="34877-108">Unpaid leave</span></span>
- <span data-ttu-id="34877-109">Palkallinen vapaa</span><span class="sxs-lookup"><span data-stu-id="34877-109">Paid vacation</span></span>
- <span data-ttu-id="34877-110">Sairausloma</span><span class="sxs-lookup"><span data-stu-id="34877-110">Sick leave</span></span>
- <span data-ttu-id="34877-111">Sairausloma</span><span class="sxs-lookup"><span data-stu-id="34877-111">Medical leave</span></span>
- <span data-ttu-id="34877-112">Perheloma</span><span class="sxs-lookup"><span data-stu-id="34877-112">Family leave</span></span>
- <span data-ttu-id="34877-113">Lyhytaikainen vamma</span><span class="sxs-lookup"><span data-stu-id="34877-113">Short-term disability</span></span>
- <span data-ttu-id="34877-114">Suruvapaa</span><span class="sxs-lookup"><span data-stu-id="34877-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="34877-115">Lomatyypin lisääminen</span><span class="sxs-lookup"><span data-stu-id="34877-115">Add a leave type</span></span>

1. <span data-ttu-id="34877-116">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="34877-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="34877-117">Valitse **Asetukset**-kohdasta **Loma- ja poissaolotyypit**.</span><span class="sxs-lookup"><span data-stu-id="34877-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="34877-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="34877-118">Select **New**.</span></span>

4. <span data-ttu-id="34877-119">Kirjoita lomatyypin nimi **Tyyppi**-kohtaan, valitse työnkulku **Työnkulun tunnus** -kohdasta ja kirjoita kuvaus **Kuvaus**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="34877-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="34877-120">Valitse **Yleinen**-kohdasta **Ei mitään**, **Ajoitettu** tai **Ennakoimaton** **Luokan** avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="34877-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="34877-121">Valitse ansaitsemiskoodi avattavasta **Ansaitsemiskoodi**-valikosta.</span><span class="sxs-lookup"><span data-stu-id="34877-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="34877-122">Valitse **Vaadittu syykoodi** -kohdassa, haluatko vaatia syykoodin.</span><span class="sxs-lookup"><span data-stu-id="34877-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="34877-123">Jos haluat vaatia syykoodeja, ne on ehkä lisättävä.</span><span class="sxs-lookup"><span data-stu-id="34877-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="34877-124">Valitse **Syykoodit**-kohdasta **Lisää**, valitse syykoodi ja valitse sitten sen vieressä oleva **Käytössä** valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="34877-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="34877-125">Valitse **Rajoita käyttöoikeuksia valittuihin rooleihin** -kohdassa, haluatko rajoittaa käyttöä.</span><span class="sxs-lookup"><span data-stu-id="34877-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="34877-126">Valitse sitten käyttöoikeusroolit **Tämän lomatyypin käyttöoikeusroolit** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="34877-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="34877-127">Käyttöoikeusroolit määritetään työnkulussa, jonka valitsit **Työnkulun tunnus** -kohdasta aiemmin tässä toimintosarjassa.</span><span class="sxs-lookup"><span data-stu-id="34877-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="34877-128">Valitse **Kalenterin väri** -kohdassa, mikä väri näytetään tämän lomatyypin loma- ja poissaolokalentereissa.</span><span class="sxs-lookup"><span data-stu-id="34877-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="34877-129">Valitse **Keskeytyssuhteet**-kohdassa haluatko, että tämä lomatyyppi keskeyttää toisen lomatyypin tai tulee toisen lomatyypin keskeyttämäksi.</span><span class="sxs-lookup"><span data-stu-id="34877-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="34877-130">Kun poissaoloa koskeva poissaolopyyntö jätetään, keskeytetyn loman tyypiksi luodaan automaattisesti loman keskeytys.</span><span class="sxs-lookup"><span data-stu-id="34877-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="34877-131">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="34877-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="34877-132">Lomatyypin sääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="34877-132">Configure leave type rules</span></span>

1. <span data-ttu-id="34877-133">Määritä lomatyypin pyöristysasetukset.</span><span class="sxs-lookup"><span data-stu-id="34877-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="34877-134">Vaihtoehtoja ovat **Ei mitään**, **Ylös**, **Alas** ja **Lähin**.</span><span class="sxs-lookup"><span data-stu-id="34877-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="34877-135">Voit myös määrittää lomatyypin pyöristystarkkuuden.</span><span class="sxs-lookup"><span data-stu-id="34877-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="34877-136">Määritä lomatyypin **Lomakorjaukset**.</span><span class="sxs-lookup"><span data-stu-id="34877-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="34877-137">Kun valitset tämän vaihtoehdon, henkilöstöhallinto käyttää työpäivään kuuluvien lomien määrää määrittääkseen, miten lomatyypille voidaan jaksottaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="34877-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="34877-138">Jos esimerkiksi joulupäivä osuu maanantaihin, henkilöstöhallinto vähentää yhden päivän lomatyypistä jaksotusten käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="34877-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="34877-139">Voit määrittää lomat työaikakalenteriin.</span><span class="sxs-lookup"><span data-stu-id="34877-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="34877-140">Lisätietoja on ohjeaiheessa [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="34877-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="34877-141">Määritä vapaan tyypiksi **Siirretty lomatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="34877-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="34877-142">Kun valitset tämän vaihtoehdon, kaikki siirrettävät saldot siirretään määritettyyn lomatyyppiin.</span><span class="sxs-lookup"><span data-stu-id="34877-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="34877-143">Siirretyn lomatyypin on sisällyttävä myös loma- ja poissaolosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="34877-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="34877-144">Määritä lomatyypin **vanhenemissäännöt**.</span><span class="sxs-lookup"><span data-stu-id="34877-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="34877-145">Kun määrität tämän asetuksen, voit valita päivien tai kuukausien yksikön ja määrittää vanhenemisajan.</span><span class="sxs-lookup"><span data-stu-id="34877-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="34877-146">Voit myös määrittää vanhentumissäännön voimaantulopäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="34877-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="34877-147">Kaikki voimassaolon päättymishetkellä jäljellä olevat saldot vähennetään lomatyypistä, ja ne näkyvät lomasaldoissa.</span><span class="sxs-lookup"><span data-stu-id="34877-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="34877-148">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="34877-148">See also</span></span>

- [<span data-ttu-id="34877-149">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="34877-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="34877-150">Loma- ja poissaolosuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="34877-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="34877-151">Työaikakalenterin luominen</span><span class="sxs-lookup"><span data-stu-id="34877-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="34877-152">Loman keskeyttäminen</span><span class="sxs-lookup"><span data-stu-id="34877-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

