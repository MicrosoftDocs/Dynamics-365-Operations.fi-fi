---
title: Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi
description: Voit antaa työntekijöille oikeuden ostaa ja myydä lomaa Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 89563204cf1423ddce47d7bacace8f14edf87005
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115993"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="a9306-103">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="a9306-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="a9306-104">Voit antaa työntekijöille oikeuden ostaa ja myydä lomia luomalla lomien osto- ja myyntikäytännön.</span><span class="sxs-lookup"><span data-stu-id="a9306-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="a9306-105">Voit määrittää nämä käytännöt käyttämään hyväksyntätyökulkua, määrittää enimmäismäärät ja -hinnat sekä määrittää osto- ja myyntihinnat.</span><span class="sxs-lookup"><span data-stu-id="a9306-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="a9306-106">Anna työntekijöille mahdollisuus ostaa ja myydä lomaa</span><span class="sxs-lookup"><span data-stu-id="a9306-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="a9306-107">Valitse **Loma- ja poissaoloparametrit** -sivun **Työntekijät voivat ostaa lomaa**- ja **Salli työntekijöiden myydä lomaa** -vaihtoehdoissa **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a9306-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="a9306-108">Loman rahaksi tai lomapalkan vapaaksi vaihtamiskäytäntöjen luominen</span><span class="sxs-lookup"><span data-stu-id="a9306-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="a9306-109">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a9306-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="a9306-110">Valitse **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi -käytäntö**.</span><span class="sxs-lookup"><span data-stu-id="a9306-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="a9306-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a9306-111">Select **New**.</span></span>

4. <span data-ttu-id="a9306-112">Kirjoita **Osta ja myy lomaa** -käytännön mukaisen käytännön **Nimi** ja **Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="a9306-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="a9306-113">Valitse **Käytäntötyyppi**.</span><span class="sxs-lookup"><span data-stu-id="a9306-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="a9306-114">Käytettävissä olevat käytäntötyypit ovat **Määrä** ja **Tuntia viikossa**.</span><span class="sxs-lookup"><span data-stu-id="a9306-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="a9306-115">Valitse **Määrä**, jos haluat syöttää **Kiinteän määrän** maksimi määriin, joita työntekijät voivat ostaa ja myydä.</span><span class="sxs-lookup"><span data-stu-id="a9306-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="a9306-116">Jos valitset **Tunteja viikossa** -käytännön, enimmäismäärä määritetään käyttämällä työntekijän määritettyä työaikaa työaikakalenterissa.</span><span class="sxs-lookup"><span data-stu-id="a9306-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="a9306-117">Valitse käytännön **Alkamispäivämäärä** ja **Päättymispäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="a9306-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="a9306-118">Osto- tai myyntipyynnöt ovat käytettävissä vain tämän aikajakson aikana.</span><span class="sxs-lookup"><span data-stu-id="a9306-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="a9306-119">Valitse käytännön **Työnkulkutunnus**.</span><span class="sxs-lookup"><span data-stu-id="a9306-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="a9306-120">Kaikki osto-ja myyntipyynnöt arvioidaan ja hyväksytään tämän työnkulun avulla.</span><span class="sxs-lookup"><span data-stu-id="a9306-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="a9306-121">Valitse **Ostokäytäntö**-kohdasta **Koko ajan vastaavuus** (FTE), jos haluat määrittää enimmäisarvon työntekijän toimessa määritetyn FTE-arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="a9306-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="a9306-122">Jos käytäntötyyppi on **Määrä**, määritä **Enimmäismäärä**.</span><span class="sxs-lookup"><span data-stu-id="a9306-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="a9306-123">Valitse **Lisää**, kun haluat lisätä lomatyypit työntekijöille, jotka ostavat lomaa.</span><span class="sxs-lookup"><span data-stu-id="a9306-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="a9306-124">Voit lisätä käytäntöön useita lomatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="a9306-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="a9306-125">Syötä lomatyypin **palvelukuukaudet**, jotta eri kuukaudet voivat määrittää työntekijän ostaman enimmäishinnan.</span><span class="sxs-lookup"><span data-stu-id="a9306-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="a9306-126">Kirjoita lomatyypin **enimmäismäärä**.</span><span class="sxs-lookup"><span data-stu-id="a9306-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="a9306-127">Kirjoita **taksa**, jolla työntekijä ostaa loman.</span><span class="sxs-lookup"><span data-stu-id="a9306-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="a9306-128">Vaihtoehtoisesti voit antaa **ansaintakoodin**, jota käytetään loman ostamiseen.</span><span class="sxs-lookup"><span data-stu-id="a9306-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="a9306-129">Voit myös määrittää, käytetäänkö FTE-tyyppiä, kun haluat määrittää lomatyypin enimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="a9306-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="a9306-130">Luo ostokäytäntö **Ostokäytäntö**-kohdan vaiheiden 8–14 mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a9306-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="a9306-131">Loman osto- ja myyntikäytännön lisääminen loma- ja poissaolosuunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="a9306-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="a9306-132">Valitse **loma ja poissaolo** -sivulla loma- ja poissaolosuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="a9306-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="a9306-133">Valitse **Säännöt**-kohdasta **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="a9306-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9306-134">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a9306-134">See also</span></span>

[<span data-ttu-id="a9306-135">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="a9306-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="a9306-136">Loma- ja poissaolotyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a9306-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="a9306-137">Jaksota loma- ja poissaolosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="a9306-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="a9306-138">Osta ja myy lomaa</span><span class="sxs-lookup"><span data-stu-id="a9306-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

