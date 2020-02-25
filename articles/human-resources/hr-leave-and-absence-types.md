---
title: Määritä loman ja poissaolon tyypit
description: Määritä Dynamics 365 Human Resourcesissa lomatyypit, joita työntekijät voivat valita.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008922"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="56756-103">Määritä loman ja poissaolon tyypit</span><span class="sxs-lookup"><span data-stu-id="56756-103">Configure leave and absence types</span></span>

<span data-ttu-id="56756-104">Lomatyypit Dynamics 365 Human Resourcesissa määrittävät erilaiset poissaolotyypit, joita työntekijät voivat ilmoittaa.</span><span class="sxs-lookup"><span data-stu-id="56756-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="56756-105">Voit räätälöidä lomatyyppejä organisaatiosi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="56756-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="56756-106">Esimerkkejä lomatyypeistä:</span><span class="sxs-lookup"><span data-stu-id="56756-106">Examples of leave types include:</span></span>

- <span data-ttu-id="56756-107">Palkallinen vapaa (PTO)</span><span class="sxs-lookup"><span data-stu-id="56756-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="56756-108">Palkaton vapaa</span><span class="sxs-lookup"><span data-stu-id="56756-108">Unpaid leave</span></span>
- <span data-ttu-id="56756-109">Palkallinen vapaa</span><span class="sxs-lookup"><span data-stu-id="56756-109">Paid vacation</span></span>
- <span data-ttu-id="56756-110">Sairausloma</span><span class="sxs-lookup"><span data-stu-id="56756-110">Sick leave</span></span>
- <span data-ttu-id="56756-111">Sairausloma</span><span class="sxs-lookup"><span data-stu-id="56756-111">Medical leave</span></span>
- <span data-ttu-id="56756-112">Perheloma</span><span class="sxs-lookup"><span data-stu-id="56756-112">Family leave</span></span>
- <span data-ttu-id="56756-113">Lyhytaikainen vamma</span><span class="sxs-lookup"><span data-stu-id="56756-113">Short-term disability</span></span>
- <span data-ttu-id="56756-114">Suruvapaa</span><span class="sxs-lookup"><span data-stu-id="56756-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="56756-115">Lomatyypin lisääminen</span><span class="sxs-lookup"><span data-stu-id="56756-115">Add a leave type</span></span>

1. <span data-ttu-id="56756-116">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="56756-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="56756-117">Valitse **Asetukset**-kohdasta **Loma- ja poissaolotyypit**.</span><span class="sxs-lookup"><span data-stu-id="56756-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="56756-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="56756-118">Select **New**.</span></span>

4. <span data-ttu-id="56756-119">Kirjoita lomatyypin nimi **Tyyppi**-kohtaan, valitse työnkulku **Työnkulun tunnus** -kohdasta ja kirjoita kuvaus **Kuvaus**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="56756-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="56756-120">Valitse **Yleinen**-kohdasta **Ei mitään**, **Ajoitettu** tai **Ennakoimaton** **Luokan** avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="56756-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="56756-121">Valitse ansaitsemiskoodi avattavasta **Ansaitsemiskoodi**-valikosta.</span><span class="sxs-lookup"><span data-stu-id="56756-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="56756-122">Valitse **Vaadittu syykoodi** -kohdassa, haluatko vaatia syykoodin.</span><span class="sxs-lookup"><span data-stu-id="56756-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="56756-123">Jos haluat vaatia syykoodeja, ne on ehkä lisättävä.</span><span class="sxs-lookup"><span data-stu-id="56756-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="56756-124">Valitse **Syykoodit**-kohdasta **Lisää**, valitse syykoodi ja valitse sitten sen vieressä oleva **Käytössä** valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="56756-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="56756-125">Valitse **Rajoita käyttöoikeuksia valittuihin rooleihin** -kohdassa, haluatko rajoittaa käyttöä.</span><span class="sxs-lookup"><span data-stu-id="56756-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="56756-126">Valitse sitten käyttöoikeusroolit **Tämän lomatyypin käyttöoikeusroolit** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="56756-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="56756-127">Käyttöoikeusroolit määritetään työnkulussa, jonka valitsit **Työnkulun tunnus** -kohdasta aiemmin tässä toimintosarjassa.</span><span class="sxs-lookup"><span data-stu-id="56756-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="56756-128">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="56756-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="56756-129">Esikatseluominaisuuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="56756-129">Configure preview features</span></span>

<span data-ttu-id="56756-130">Jos olet ottanut käyttöön loman ja poissaolon esikatseluominaisuudet, sinun on määritettävä myös niiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="56756-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="56756-131">Määritä lomatyypin pyöristysasetukset.</span><span class="sxs-lookup"><span data-stu-id="56756-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="56756-132">Vaihtoehtoja ovat **Ei mitään**, **Ylös**, **Alas** ja **Lähin**.</span><span class="sxs-lookup"><span data-stu-id="56756-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="56756-133">Voit myös määrittää lomatyypin pyöristystarkkuuden.</span><span class="sxs-lookup"><span data-stu-id="56756-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="56756-134">Määritä lomatyypin **Lomakorjaukset**.</span><span class="sxs-lookup"><span data-stu-id="56756-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="56756-135">Kun valitset tämän vaihtoehdon, henkilöstöhallinto käyttää työpäivään kuuluvien lomien määrää määrittääkseen, miten lomatyypille voidaan jaksottaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="56756-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="56756-136">Jos esimerkiksi joulupäivä osuu maanantaihin, henkilöstöhallinto vähentää yhden päivän lomatyypistä jaksotusten käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="56756-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="56756-137">Voit määrittää lomat työaikakalenteriin.</span><span class="sxs-lookup"><span data-stu-id="56756-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="56756-138">Lisätietoja on ohjeaiheessa [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="56756-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="56756-139">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="56756-139">See also</span></span>

- [<span data-ttu-id="56756-140">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="56756-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="56756-141">Loma- ja poissaolosuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="56756-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="56756-142">Työaikakalenterin luominen</span><span class="sxs-lookup"><span data-stu-id="56756-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)