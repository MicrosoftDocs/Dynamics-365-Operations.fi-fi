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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab158a9f96054f7478a331b6165c01432311eb7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213374"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="55fa2-103">Lisää rajoituslauseke tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="55fa2-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55fa2-104">Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="55fa2-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="55fa2-105">Se näyttää, miten voit määrätä, että kulmasuojausta on käytettävä kaiuttimessa, jos käyttäjä on valinnut metallin etusäleikköön.</span><span class="sxs-lookup"><span data-stu-id="55fa2-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="55fa2-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="55fa2-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="55fa2-107">Luo lausekerajoitus</span><span class="sxs-lookup"><span data-stu-id="55fa2-107">Create an expression constraint</span></span>
1. <span data-ttu-id="55fa2-108">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="55fa2-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="55fa2-109">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="55fa2-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="55fa2-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="55fa2-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="55fa2-111">Tässä esimerkissä käytetään Korkealaatuinen kaiutin -mallia.</span><span class="sxs-lookup"><span data-stu-id="55fa2-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="55fa2-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="55fa2-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="55fa2-113">Laajenna Rajoitukset-osa.</span><span class="sxs-lookup"><span data-stu-id="55fa2-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="55fa2-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="55fa2-114">Click Add.</span></span>
7. <span data-ttu-id="55fa2-115">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="55fa2-115">Click Create.</span></span>
8. <span data-ttu-id="55fa2-116">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55fa2-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="55fa2-117">Anna lauseke</span><span class="sxs-lookup"><span data-stu-id="55fa2-117">Enter expression</span></span>
1. <span data-ttu-id="55fa2-118">Valitse Muokkaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="55fa2-118">Click Edit expression.</span></span>
    * <span data-ttu-id="55fa2-119">Jos vapautat käyttöliittymän tehtävätallenteen tässä vaiheessa, voit muodostaa rajoituslausekkeen IntelliSensen ja symboliluettelon avulla.</span><span class="sxs-lookup"><span data-stu-id="55fa2-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="55fa2-120">Lisää ConstraintBody-kenttään Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="55fa2-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="55fa2-121">Tämän lausekkeen logiikka ilmaisee, että jos etusäleikkö on metallia, sitten kulmasuojausvaihtoehto on valittava.</span><span class="sxs-lookup"><span data-stu-id="55fa2-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="55fa2-122">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="55fa2-122">Click Validate.</span></span>
    * <span data-ttu-id="55fa2-123">Vahvistustoiminto suoritetaan rajoitelausekkeessa, jossa se tarkistaa syntaksivirheet.</span><span class="sxs-lookup"><span data-stu-id="55fa2-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="55fa2-124">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="55fa2-124">Click Close.</span></span>
5. <span data-ttu-id="55fa2-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="55fa2-125">Click OK.</span></span>

