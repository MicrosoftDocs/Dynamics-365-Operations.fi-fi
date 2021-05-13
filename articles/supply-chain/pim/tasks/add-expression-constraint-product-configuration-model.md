---
title: Lisää rajoituslauseke tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920878"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="93c54-103">Lisää rajoituslauseke tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="93c54-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93c54-104">Tässä menettelyssä käsitellään, miten uusi rajoituslauseke lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="93c54-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="93c54-105">Se näyttää, miten voit määrätä, että kulmasuojausta on käytettävä kaiuttimessa, jos käyttäjä on valinnut metallin etusäleikköön.</span><span class="sxs-lookup"><span data-stu-id="93c54-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="93c54-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="93c54-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="93c54-107">Luo lausekerajoitus</span><span class="sxs-lookup"><span data-stu-id="93c54-107">Create an expression constraint</span></span>

1. <span data-ttu-id="93c54-108">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="93c54-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="93c54-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="93c54-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="93c54-110">Tässä esimerkissä käytetään Korkealaatuinen kaiutin -mallia.</span><span class="sxs-lookup"><span data-stu-id="93c54-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="93c54-111">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="93c54-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="93c54-112">Laajenna **Rajoitukset**-osa.</span><span class="sxs-lookup"><span data-stu-id="93c54-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="93c54-113">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="93c54-113">Select **Add**.</span></span>
7. <span data-ttu-id="93c54-114">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="93c54-114">Select **Create**.</span></span>
8. <span data-ttu-id="93c54-115">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93c54-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="93c54-116">Anna lauseke</span><span class="sxs-lookup"><span data-stu-id="93c54-116">Enter expression</span></span>

1. <span data-ttu-id="93c54-117">Valitse **Muokkaa lauseketta**.</span><span class="sxs-lookup"><span data-stu-id="93c54-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="93c54-118">Jos vapautat käyttöliittymän tehtävätallenteen tässä vaiheessa, voit muodostaa rajoituslausekkeen IntelliSensen ja symboliluettelon avulla.</span><span class="sxs-lookup"><span data-stu-id="93c54-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="93c54-119">Lisää **ConstraintBody**-kenttään Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="93c54-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="93c54-120">Tämän lausekkeen logiikka ilmaisee, että jos etusäleikkö on metallia, sitten kulmasuojausvaihtoehto on valittava.</span><span class="sxs-lookup"><span data-stu-id="93c54-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="93c54-121">Valitse **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="93c54-121">Select **Validate**.</span></span>
    * <span data-ttu-id="93c54-122">Vahvistustoiminto suoritetaan rajoitelausekkeessa, jossa se tarkistaa syntaksivirheet.</span><span class="sxs-lookup"><span data-stu-id="93c54-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="93c54-123">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="93c54-123">Select **Close**.</span></span>
5. <span data-ttu-id="93c54-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="93c54-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]