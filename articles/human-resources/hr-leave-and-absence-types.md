---
title: Määritä loman ja poissaolon tyypit
description: Määritä Dynamics 365 Human Resourcesissa lomatyypit, joita työntekijät voivat valita.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198047"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="9ebf0-103">Määritä loman ja poissaolon tyypit</span><span class="sxs-lookup"><span data-stu-id="9ebf0-103">Configure leave and absence types</span></span>

<span data-ttu-id="9ebf0-104">Lomatyypit Dynamics 365 Human Resourcesissa määrittävät erilaiset poissaolotyypit, joita työntekijät voivat ilmoittaa.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="9ebf0-105">Voit räätälöidä lomatyyppejä organisaatiosi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="9ebf0-106">Esimerkkejä lomatyypeistä:</span><span class="sxs-lookup"><span data-stu-id="9ebf0-106">Examples of leave types include:</span></span>

- <span data-ttu-id="9ebf0-107">Palkallinen vapaa (PTO)</span><span class="sxs-lookup"><span data-stu-id="9ebf0-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="9ebf0-108">Palkaton vapaa</span><span class="sxs-lookup"><span data-stu-id="9ebf0-108">Unpaid leave</span></span>
- <span data-ttu-id="9ebf0-109">Palkallinen vapaa</span><span class="sxs-lookup"><span data-stu-id="9ebf0-109">Paid vacation</span></span>
- <span data-ttu-id="9ebf0-110">Sairausloma</span><span class="sxs-lookup"><span data-stu-id="9ebf0-110">Sick leave</span></span>
- <span data-ttu-id="9ebf0-111">Sairausloma</span><span class="sxs-lookup"><span data-stu-id="9ebf0-111">Medical leave</span></span>
- <span data-ttu-id="9ebf0-112">Perheloma</span><span class="sxs-lookup"><span data-stu-id="9ebf0-112">Family leave</span></span>
- <span data-ttu-id="9ebf0-113">Lyhytaikainen vamma</span><span class="sxs-lookup"><span data-stu-id="9ebf0-113">Short-term disability</span></span>
- <span data-ttu-id="9ebf0-114">Suruvapaa</span><span class="sxs-lookup"><span data-stu-id="9ebf0-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="9ebf0-115">Lomatyypin lisääminen</span><span class="sxs-lookup"><span data-stu-id="9ebf0-115">Add a leave type</span></span>

1. <span data-ttu-id="9ebf0-116">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9ebf0-117">Valitse **Asetukset**-kohdasta **Loma- ja poissaolotyypit**.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="9ebf0-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-118">Select **New**.</span></span>

4. <span data-ttu-id="9ebf0-119">Kirjoita lomatyypin nimi **Tyyppi**-kohtaan, valitse työnkulku **Työnkulun tunnus** -kohdasta ja kirjoita kuvaus **Kuvaus**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="9ebf0-120">Valitse **Yleinen**-kohdasta **Ei mitään**, **Ajoitettu** tai **Ennakoimaton** **Luokan** avattavasta luettelosta.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="9ebf0-121">Valitse ansaitsemiskoodi avattavasta **Ansaitsemiskoodi**-valikosta.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="9ebf0-122">Valitse **Vaadittu syykoodi** -kohdassa, haluatko vaatia syykoodin.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="9ebf0-123">Jos haluat vaatia syykoodeja, ne on ehkä lisättävä.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="9ebf0-124">Valitse **Syykoodit**-kohdasta **Lisää**, valitse syykoodi ja valitse sitten sen vieressä oleva **Käytössä** valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="9ebf0-125">Valitse **Rajoita käyttöoikeuksia valittuihin rooleihin** -kohdassa, haluatko rajoittaa käyttöä.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="9ebf0-126">Valitse sitten käyttöoikeusroolit **Tämän lomatyypin käyttöoikeusroolit** -kohdasta.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="9ebf0-127">Käyttöoikeusroolit määritetään työnkulussa, jonka valitsit **Työnkulun tunnus** -kohdasta aiemmin tässä toimintosarjassa.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="9ebf0-128">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="9ebf0-129">Lomatyypin sääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9ebf0-129">Configure leave type rules</span></span>

1. <span data-ttu-id="9ebf0-130">Määritä lomatyypin pyöristysasetukset.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="9ebf0-131">Vaihtoehtoja ovat **Ei mitään**, **Ylös**, **Alas** ja **Lähin**.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="9ebf0-132">Voit myös määrittää lomatyypin pyöristystarkkuuden.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="9ebf0-133">Määritä lomatyypin **Lomakorjaukset**.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="9ebf0-134">Kun valitset tämän vaihtoehdon, henkilöstöhallinto käyttää työpäivään kuuluvien lomien määrää määrittääkseen, miten lomatyypille voidaan jaksottaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="9ebf0-135">Jos esimerkiksi joulupäivä osuu maanantaihin, henkilöstöhallinto vähentää yhden päivän lomatyypistä jaksotusten käsittelyn yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="9ebf0-136">Voit määrittää lomat työaikakalenteriin.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="9ebf0-137">Lisätietoja on ohjeaiheessa [Työaikakalenterin luominen](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="9ebf0-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="9ebf0-138">Esikatseluominaisuuksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9ebf0-138">Configure preview features</span></span>

<span data-ttu-id="9ebf0-139">Jos olet ottanut käyttöön loman ja poissaolon esikatseluominaisuudet, sinun on määritettävä myös niiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="9ebf0-140">Valitse lomatyyppi, johon siirrettävät saldot siirretään.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="9ebf0-141">Voit myös luoda uuden lomatyypin siirtokirjauksen.</span><span class="sxs-lookup"><span data-stu-id="9ebf0-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="9ebf0-142">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="9ebf0-142">See also</span></span>

- [<span data-ttu-id="9ebf0-143">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="9ebf0-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="9ebf0-144">Loma- ja poissaolosuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="9ebf0-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="9ebf0-145">Työaikakalenterin luominen</span><span class="sxs-lookup"><span data-stu-id="9ebf0-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
