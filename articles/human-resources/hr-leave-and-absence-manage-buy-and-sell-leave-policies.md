---
title: Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi
description: Voit antaa työntekijöille oikeuden ostaa ja myydä lomaa Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429010"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="69dd2-103">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="69dd2-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="69dd2-104">Voit antaa työntekijöille oikeuden ostaa lomaa luomalla ostolomakäytännön.</span><span class="sxs-lookup"><span data-stu-id="69dd2-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="69dd2-105">Anna työntekijöille mahdollisuus ostaa ja myydä lomaa</span><span class="sxs-lookup"><span data-stu-id="69dd2-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="69dd2-106">Valitse **Loma- ja poissaoloparametrit** -sivulla **Kyllä**, jotta **Työntekijät voivat ostaa loman**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="69dd2-107">Luo loman ostokäytäntö</span><span class="sxs-lookup"><span data-stu-id="69dd2-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="69dd2-108">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="69dd2-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="69dd2-109">Valitse **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi -käytäntö**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="69dd2-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-110">Select **New**.</span></span>

4. <span data-ttu-id="69dd2-111">Kirjoita **Osta ja myy lomaa** -käytännön mukaisen käytännön **Nimi** ja **Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="69dd2-112">Valitse **Käytäntötyyppi**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="69dd2-113">Käytettävissä olevat käytäntötyypit ovat **Määrä** ja **Tuntia viikossa**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="69dd2-114">Valitse **Määrä**, jos haluat syöttää **Kiinteän määrän** maksimi määriin, joita työntekijät voivat ostaa ja myydä.</span><span class="sxs-lookup"><span data-stu-id="69dd2-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="69dd2-115">Jos valitset **Tunteja viikossa** -käytännön, enimmäismäärä määritetään käyttämällä työntekijän määritettyä työaikaa työaikakalenterissa.</span><span class="sxs-lookup"><span data-stu-id="69dd2-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="69dd2-116">Valitse käytännön **Alkamispäivämäärä** ja **Päättymispäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="69dd2-117">Osto- tai myyntipyynnöt ovat käytettävissä vain tämän aikajakson aikana.</span><span class="sxs-lookup"><span data-stu-id="69dd2-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="69dd2-118">Valitse **Ostokäytäntö**-kohdasta **Koko ajan vastaavuus** (FTE), jos haluat määrittää enimmäisarvon työntekijän toimessa määritetyn FTE-arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="69dd2-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="69dd2-119">Jos käytäntötyyppi on **Määrä**, määritä **Enimmäismäärä**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="69dd2-120">Valitse **Lisää**, kun haluat lisätä lomatyypit työntekijöille, jotka ostavat lomaa.</span><span class="sxs-lookup"><span data-stu-id="69dd2-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="69dd2-121">Voit lisätä käytäntöön useita lomatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="69dd2-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="69dd2-122">Syötä lomatyypin **palvelukuukaudet**, jotta eri kuukaudet voivat määrittää työntekijän ostaman enimmäishinnan.</span><span class="sxs-lookup"><span data-stu-id="69dd2-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="69dd2-123">Kirjoita lomatyypin **enimmäismäärä**.</span><span class="sxs-lookup"><span data-stu-id="69dd2-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="69dd2-124">Kirjoita **taksa**, jolla työntekijä ostaa loman.</span><span class="sxs-lookup"><span data-stu-id="69dd2-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="69dd2-125">Vaihtoehtoisesti voit antaa **ansaintakoodin**, jota käytetään loman ostamiseen.</span><span class="sxs-lookup"><span data-stu-id="69dd2-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="69dd2-126">Voit myös määrittää, käytetäänkö FTE-tyyppiä, kun haluat määrittää lomatyypin enimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="69dd2-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="69dd2-127">Loman osto- ja myyntikäytännön lisääminen loma- ja poissaolosuunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="69dd2-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="69dd2-128">Valitse **loma ja poissaolo** -sivulla loma- ja poissaolosuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="69dd2-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="69dd2-129">Valitse **Säännöt**-kohdasta **Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi** -käytäntö.</span><span class="sxs-lookup"><span data-stu-id="69dd2-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="69dd2-130">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="69dd2-130">See also</span></span>

[<span data-ttu-id="69dd2-131">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="69dd2-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="69dd2-132">Loma- ja poissaolotyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69dd2-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="69dd2-133">Jaksota loma- ja poissaolosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="69dd2-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="69dd2-134">Osta ja myy lomaa</span><span class="sxs-lookup"><span data-stu-id="69dd2-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

