---
title: Tuotekonfiguraatiomallin laskelmat
description: Tässä aiheessa kuvataan, miten tuotekonfiguraatiomallissa määritteiden laskelmat
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829615"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="a5975-103">Tuotekonfiguraatiomallin laskelmat</span><span class="sxs-lookup"><span data-stu-id="a5975-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5975-104">Tässä aiheessa kuvataan, miten tuotekonfiguraatiomallissa määritteiden laskelmat.</span><span class="sxs-lookup"><span data-stu-id="a5975-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a5975-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="a5975-105">Prerequisites</span></span>

<span data-ttu-id="a5975-106">Laskentaa käytetään tuotteen kokoonpanomallissa laskettaessa tuotteelle kokoonpanoarvoja.</span><span class="sxs-lookup"><span data-stu-id="a5975-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="a5975-107">Ennen kuin laskelmien määritys aloitetaan, liittyvä tuotekonfiguraatiomalli on oltava olemassa.</span><span class="sxs-lookup"><span data-stu-id="a5975-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="a5975-108">Yhteenveto konfigurointimallien määritysprosessista ja niihin liittyvistä tehtävistä on kohdassa [Tuotekonfiguraatiomallin määrittäminen](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="a5975-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="a5975-109">Luo laskenta</span><span class="sxs-lookup"><span data-stu-id="a5975-109">Create a calculation</span></span>

<span data-ttu-id="a5975-110">Laskenta koostuu kaavasta ja kohdemääritteestä.</span><span class="sxs-lookup"><span data-stu-id="a5975-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="a5975-111">Lisätietoja: [Tuotekonfiguraatiomallin laskelmat – usein kysytyt kysymykset](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="a5975-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="a5975-112">Voit luoda laskelman aiemmin luotua tuotemallia varten noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="a5975-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="a5975-113">Siirry kohtaan **Tuotetietojen hallinta \> Yleinen \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="a5975-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="a5975-114">Avaa tuotekonfiguraation malli ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="a5975-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="a5975-115">Lisää laskelma valitsemalla **Laskelmat** -pikavälilehdessä **Lisää** ja määritä sitten seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="a5975-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="a5975-116">**Nimi** – Anna laskelman nimi.</span><span class="sxs-lookup"><span data-stu-id="a5975-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="a5975-117">**Kuvaus** – anna laskelman kuvaus.</span><span class="sxs-lookup"><span data-stu-id="a5975-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="a5975-118">**Kohdemäärite** – Valitse määrite, jota varten laskenta tehdään.</span><span class="sxs-lookup"><span data-stu-id="a5975-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="a5975-119">Valitse **Muokkaa lauseketta**.</span><span class="sxs-lookup"><span data-stu-id="a5975-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="a5975-120">Lisää lausekkeeseen pakolliset määritteet, operaattorit ja arvot **Syötä laskenta** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="a5975-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="a5975-121">Lisätietoja näiden elementtien käsittelystä on kohdassa [Tuotteen määritysmallien lausekerajoitukset ja taulukkorajoitukset](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="a5975-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="a5975-122">Kun lauseke on valmis, valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5975-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="a5975-123">Esimerkkejä laskutoimituksista</span><span class="sxs-lookup"><span data-stu-id="a5975-123">Calculation examples</span></span>

<span data-ttu-id="a5975-124">Tässä osassa on muutamia esimerkkejä, jotka osoittavat, kuinka laskelmat toimivat.</span><span class="sxs-lookup"><span data-stu-id="a5975-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="a5975-125">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="a5975-125">Example 1</span></span>

<span data-ttu-id="a5975-126">Kohdemääritteen tyyppi on Boolean ja laskenta käyttää seuraavaa ehtolauseketta:</span><span class="sxs-lookup"><span data-stu-id="a5975-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="a5975-127">Tämä lauseke palauttaa kohdemääritteeseen *Tosi*, jos `decimalAttribute2` on suurempi tai yhtä suuri kuin `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="a5975-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="a5975-128">Muussa tapauksessa se palauttaa totuusarvon *Epätosi*.</span><span class="sxs-lookup"><span data-stu-id="a5975-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="a5975-129">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="a5975-129">Example 2</span></span>

<span data-ttu-id="a5975-130">Tässä esimerkissä kohdemääritteenä käytetään tekstimääritettä `textFixedList`.</span><span class="sxs-lookup"><span data-stu-id="a5975-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="a5975-131">Tämä määrite sisältää seuraavan kiinteän luettelon.</span><span class="sxs-lookup"><span data-stu-id="a5975-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="a5975-132">Arvo</span><span class="sxs-lookup"><span data-stu-id="a5975-132">Value</span></span> | <span data-ttu-id="a5975-133">Selvityksen arvo</span><span class="sxs-lookup"><span data-stu-id="a5975-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="a5975-134">A</span><span class="sxs-lookup"><span data-stu-id="a5975-134">A</span></span> | <span data-ttu-id="a5975-135">1a</span><span class="sxs-lookup"><span data-stu-id="a5975-135">1a</span></span> |
| <span data-ttu-id="a5975-136">D</span><span class="sxs-lookup"><span data-stu-id="a5975-136">B</span></span> | <span data-ttu-id="a5975-137">2b</span><span class="sxs-lookup"><span data-stu-id="a5975-137">2b</span></span> |
| <span data-ttu-id="a5975-138">K</span><span class="sxs-lookup"><span data-stu-id="a5975-138">C</span></span> | <span data-ttu-id="a5975-139">2c</span><span class="sxs-lookup"><span data-stu-id="a5975-139">2c</span></span> |

<span data-ttu-id="a5975-140">Seuraavassa näyttökuvassa näkyy, miltä tämän määritteen asetukset voivat näyttää järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="a5975-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="a5975-141">![Määritteen tyypin asetukset esimerkissä 2](media/model-calculations-example2.png "Määritteen tyypin asetukset esimerkissä 2")</span><span class="sxs-lookup"><span data-stu-id="a5975-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="a5975-142">Määritettä käytetään seuraavassa ehtolausekkeessa:</span><span class="sxs-lookup"><span data-stu-id="a5975-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="a5975-143">Jos `integerAttribute` on pienempi kuin 150, tämä lauseke palauttaa kiinteän luettelon ensimmäisen tietueen tekstin arvon *A*. Muussa tapauksessa se palauttaa kiinteän luettelon kolmannen tietueen tekstiarvon *C*.</span><span class="sxs-lookup"><span data-stu-id="a5975-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="a5975-144">Kiinteä luettelo vastaa nollaan perustuvaa valintalista (enum), ja sen arvoja voidaan käyttää sopivalla kokonaislukuarvolla.</span><span class="sxs-lookup"><span data-stu-id="a5975-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="a5975-145">Siksi ensimmäisen kiinteän luettelon arvo (*A*) vastaa arvoa numeroa *0*, toinen arvo (*B*) vastaa numeroa *1* ja kolmas arvo (*C*) vastaa numeroa *2*.</span><span class="sxs-lookup"><span data-stu-id="a5975-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="a5975-146">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="a5975-146">Example 3</span></span>

<span data-ttu-id="a5975-147">Tässä esimerkissä `textFixedList`-kohdemääritettä edellisestä esimerkistä.</span><span class="sxs-lookup"><span data-stu-id="a5975-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="a5975-148">Se käyttää myös toista `textAttribute`-tekstimääritettä, joka sisältää seuraavan kiinteän luettelon.</span><span class="sxs-lookup"><span data-stu-id="a5975-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="a5975-149">Arvo</span><span class="sxs-lookup"><span data-stu-id="a5975-149">Value</span></span> | <span data-ttu-id="a5975-150">Selvityksen arvo</span><span class="sxs-lookup"><span data-stu-id="a5975-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="a5975-151">AA</span><span class="sxs-lookup"><span data-stu-id="a5975-151">AA</span></span> | <span data-ttu-id="a5975-152">1aa</span><span class="sxs-lookup"><span data-stu-id="a5975-152">1aa</span></span> |
| <span data-ttu-id="a5975-153">BB</span><span class="sxs-lookup"><span data-stu-id="a5975-153">BB</span></span> | <span data-ttu-id="a5975-154">2bb</span><span class="sxs-lookup"><span data-stu-id="a5975-154">2bb</span></span> |

<span data-ttu-id="a5975-155">Seuraavassa näyttökuvassa näkyy, miltä tämän määritteen asetukset voivat näyttää järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="a5975-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="a5975-156">![Määritteen tyypin asetukset esimerkissä 3](media/model-calculations-example3.png "Määritteen tyypin asetukset esimerkissä 3")</span><span class="sxs-lookup"><span data-stu-id="a5975-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="a5975-157">Määritteen `textFixedList` arvo lasketaan seuraavan ehtolausekkeen avulla:</span><span class="sxs-lookup"><span data-stu-id="a5975-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="a5975-158">Jos `textAttribute`-palautusarvo on yhtä kuin *1aa*, tämä lauseke palauttaa kiinteän `textFixedList`-luettelon ensimmäisen tietueen tekstin arvon *A*. Muussa tapauksessa se palauttaa kiinteän `textFixedList`-luettelon kolmannen tietueen tekstiarvon *C*.</span><span class="sxs-lookup"><span data-stu-id="a5975-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="a5975-159">Ehdollisen laskelman on käytettävä määritteen palautusarvoa.</span><span class="sxs-lookup"><span data-stu-id="a5975-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="a5975-160">Laskelmissa voidaan käyttää vain kiinteän luettelon tekstimääritteitä.</span><span class="sxs-lookup"><span data-stu-id="a5975-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5975-161">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a5975-161">See also</span></span>

- [<span data-ttu-id="a5975-162">Tuotemääritysmallien laskelmat – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="a5975-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="a5975-163">Lisää rajoituslauseke tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="a5975-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="a5975-164">Tuotekonfiguraatiomallien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a5975-164">Product configuration models overview</span></span>](product-configuration-models.md)
