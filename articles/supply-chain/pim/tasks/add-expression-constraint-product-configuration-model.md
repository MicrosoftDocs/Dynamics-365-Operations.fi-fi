---
title: Lisää rajoituslauseke tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256156"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="84b7b-103">Lisää rajoituslauseke tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="84b7b-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84b7b-104">Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="84b7b-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="84b7b-105">Se näyttää, miten voit määrätä, että kulmasuojausta on käytettävä kaiuttimessa, jos käyttäjä on valinnut metallin etusäleikköön.</span><span class="sxs-lookup"><span data-stu-id="84b7b-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="84b7b-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="84b7b-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="84b7b-107">Luo lausekerajoitus</span><span class="sxs-lookup"><span data-stu-id="84b7b-107">Create an expression constraint</span></span>
1. <span data-ttu-id="84b7b-108">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="84b7b-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="84b7b-109">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="84b7b-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="84b7b-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="84b7b-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="84b7b-111">Tässä esimerkissä käytetään Korkealaatuinen kaiutin -mallia.</span><span class="sxs-lookup"><span data-stu-id="84b7b-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="84b7b-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="84b7b-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="84b7b-113">Laajenna Rajoitukset-osa.</span><span class="sxs-lookup"><span data-stu-id="84b7b-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="84b7b-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="84b7b-114">Click Add.</span></span>
7. <span data-ttu-id="84b7b-115">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="84b7b-115">Click Create.</span></span>
8. <span data-ttu-id="84b7b-116">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="84b7b-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="84b7b-117">Anna lauseke</span><span class="sxs-lookup"><span data-stu-id="84b7b-117">Enter expression</span></span>
1. <span data-ttu-id="84b7b-118">Valitse Muokkaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="84b7b-118">Click Edit expression.</span></span>
    * <span data-ttu-id="84b7b-119">Jos vapautat käyttöliittymän tehtävätallenteen tässä vaiheessa, voit muodostaa rajoituslausekkeen IntelliSensen ja symboliluettelon avulla.</span><span class="sxs-lookup"><span data-stu-id="84b7b-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="84b7b-120">Lisää ConstraintBody-kenttään Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="84b7b-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="84b7b-121">Tämän lausekkeen logiikka ilmaisee, että jos etusäleikkö on metallia, sitten kulmasuojausvaihtoehto on valittava.</span><span class="sxs-lookup"><span data-stu-id="84b7b-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="84b7b-122">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="84b7b-122">Click Validate.</span></span>
    * <span data-ttu-id="84b7b-123">Vahvistustoiminto suoritetaan rajoitelausekkeessa, jossa se tarkistaa syntaksivirheet.</span><span class="sxs-lookup"><span data-stu-id="84b7b-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="84b7b-124">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="84b7b-124">Click Close.</span></span>
5. <span data-ttu-id="84b7b-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="84b7b-125">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]