---
title: "Tuotemääritysmallien laskelmat – usein kysytyt kysymykset"
description: "Tässä ohjeaiheessa kuvataan laskutoimitukset tuotekonfiguraatiomalleille ja laskentojen käyttäminen yhdessä rajoitteiden kanssa."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: daae96502f705f05076cb351aa1baefc37957803
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---

# <a name="calculations-for-product-configuration-models-faq"></a><span data-ttu-id="51783-103">Tuotemääritysmallien laskelmat – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="51783-103">Calculations for product configuration models FAQ</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="51783-104">Tässä ohjeaiheessa kuvataan laskutoimitukset tuotekonfiguraatiomalleille ja laskentojen käyttäminen yhdessä rajoitteiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="51783-104">This topic describes calculations for product configuration models and explains how to use calculations together with constraints.</span></span>

<span data-ttu-id="51783-105">Laskutoimituksia on mahdollista käyttää aritmeettisiin tai loogisiin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="51783-105">Calculations can be used for arithmetic or logical operations.</span></span> <span data-ttu-id="51783-106">Ne täydentävät lausekkeiden rajoituksia tuotemääritysmalleissa.</span><span class="sxs-lookup"><span data-stu-id="51783-106">They complement expression constraints in product configuration models.</span></span> <span data-ttu-id="51783-107">Voit määrittää laskutoimituksia **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla ja luoda laskutoimituksille lausekkeita lauseke-editorilla.</span><span class="sxs-lookup"><span data-stu-id="51783-107">You can define calculations on the **Constraint-based product configuration model details** page and then build expressions for the calculations in the expression editor.</span></span> <span data-ttu-id="51783-108">Lisätietoja on kohdassa Laskelmien luominen.</span><span class="sxs-lookup"><span data-stu-id="51783-108">For more information, see Create calculations.</span></span>

## <a name="what-is-a-calculation"></a><span data-ttu-id="51783-109">Mikä on laskelma?</span><span class="sxs-lookup"><span data-stu-id="51783-109">What is a calculation?</span></span>
<span data-ttu-id="51783-110">Laskutoimitus on elementti, jota voit käyttää tuotteen kokoonpanomallissa.</span><span class="sxs-lookup"><span data-stu-id="51783-110">A calculation is an element that you can use in a product configuration model.</span></span> <span data-ttu-id="51783-111">Laskelmat täydentävät rajoituksia mahdollistamalla arvojen laskemisen käyttämällä desimaalilukuja tuotetta määrittäessäsi.</span><span class="sxs-lookup"><span data-stu-id="51783-111">Calculations complement constraints by letting you use decimal numbers to calculate values when you configure a product.</span></span> <span data-ttu-id="51783-112">Lisäksi laskelmilla on suurempi määrä operaattoreita käytettävissä kuin rajoituksilla.</span><span class="sxs-lookup"><span data-stu-id="51783-112">Additionally, calculations have a larger set of available operators than constraints have.</span></span>  

<span data-ttu-id="51783-113">Vastaavasti kuin rajoitus, laskenta liitetään tiettyyn tuotekonfiguraatiomallin komponenttiin, eikä sitä voi käyttää uudelleen tai jakaa toisen komponentin kanssa.</span><span class="sxs-lookup"><span data-stu-id="51783-113">Like a constraint, a calculation is associated with a specific component in a product configuration model, and can’t be reused by or shared with another component.</span></span> <span data-ttu-id="51783-114">Tärkeä ero laskelmien ja rajoitusten välillä on, että laskelmat ovat pakottavia (yksisuuntaisia), kun taas rajoitukset ovat määrittäviä (kaksisuuntaisia).</span><span class="sxs-lookup"><span data-stu-id="51783-114">One important difference between calculations and constraints is that calculations are imperative (unidirectional), whereas constraints are declarative (bi-directional).</span></span> <span data-ttu-id="51783-115">Katso lisätietoja rajoituksista kohdasta [Lausekerajoitukset ja taulukkorajoitukset](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="51783-115">For more information about constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span>  

<span data-ttu-id="51783-116">Laskenta koostuu kohdemääritteestä ja laskentakaavasta.</span><span class="sxs-lookup"><span data-stu-id="51783-116">A calculation consists of a target attribute and a calculation expression.</span></span>

## <a name="what-is-a-target-attribute"></a><span data-ttu-id="51783-117">Mikä on kohdemäärite?</span><span class="sxs-lookup"><span data-stu-id="51783-117">What is a target attribute?</span></span>
<span data-ttu-id="51783-118">Kohdemäärite on määrite, joka saa laskennan tuloksen lausekkeesta.</span><span class="sxs-lookup"><span data-stu-id="51783-118">A target attribute is an attribute that receives the result of the calculation expression.</span></span>  

<span data-ttu-id="51783-119">Seuraavassa lausekkeessa kohdemäärite on tablecloth-mitta:</span><span class="sxs-lookup"><span data-stu-id="51783-119">In the following expression, the target attribute is a tablecloth measurement:</span></span>  

<span data-ttu-id="51783-120">**Lauseke:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span><span class="sxs-lookup"><span data-stu-id="51783-120">**Expression:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span></span>  

<span data-ttu-id="51783-121">**DecimalAttribute1** on taulukon pituus ja **decimalAttribute2** on pöytäliinan pituus.</span><span class="sxs-lookup"><span data-stu-id="51783-121">**DecimalAttribute1** is the table length, and **decimalAttribute2** is the tablecloth length.</span></span> <span data-ttu-id="51783-122">Tämä lauseke palauttaa kohdemääritteeseen arvon **Tosi**, jos **decimalAttribute2** on suurempi tai yhtä suuri kuin **decimalAttribute1**.</span><span class="sxs-lookup"><span data-stu-id="51783-122">The expression returns the value **True** to the target attribute if **decimalAttribute2** is greater than or equal to **decimalAttribute1**.</span></span> <span data-ttu-id="51783-123">Muussa tapauksessa lauseke palauttaa arvon **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="51783-123">Otherwise, the expression returns **False**.</span></span> <span data-ttu-id="51783-124">Siten pöytäliinan mitta on hyväksyttävä, jos pöytäliinan pituus vastaa pöydän pituutta tai ylittää sen.</span><span class="sxs-lookup"><span data-stu-id="51783-124">Therefore, the tablecloth measurement is acceptable if the tablecloth length is the same as or exceeds the length of the table.</span></span>

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a><span data-ttu-id="51783-125">Mitä määritetyyppejä voidaan asettaa kohdemääritteiksi?</span><span class="sxs-lookup"><span data-stu-id="51783-125">What attribute types can be set to target attributes?</span></span>
<span data-ttu-id="51783-126">Kaikki tuotekonfiguroinnin tukemat määritetyypit voidaan asettaa kohdemääritteiksi lukuun ottamatta tekstiä, jolla ei ole kiinteää luetteloa.</span><span class="sxs-lookup"><span data-stu-id="51783-126">All attribute types that the product configurator supports can be set to target attributes, except text without a fixed list.</span></span>

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a><span data-ttu-id="51783-127">Voiko kohdemääritteen arvo rajoittaa syöttömääritteiden arvoja laskennassa?</span><span class="sxs-lookup"><span data-stu-id="51783-127">Can the value of a target attribute restrict the values of the input attributes in a calculation?</span></span>
<span data-ttu-id="51783-128">Ei, kohdemääritteen arvo ei voi rajoittaa syöttömääritteiden arvoja laskennassa, koska laskelmat ovat yksisuuntaisia.</span><span class="sxs-lookup"><span data-stu-id="51783-128">No, the value of a target attribute can’t restrict the values of the input attributes, because calculations are unidirectional.</span></span> <span data-ttu-id="51783-129">Kohdemääritteen arvo on siis asetettu syöttömääritteiden arvojen muutosten perusteella, mutta muutos kohteen arvossa ei vaikuta syöttömääritteisiin.</span><span class="sxs-lookup"><span data-stu-id="51783-129">Therefore, the value of the target attribute is set based on changes in the value of the input attributes, but a change in the value of the target doesn’t affect the value of the input attributes.</span></span> <span data-ttu-id="51783-130">Toiminta tältä osin eroaa rajoitteista.</span><span class="sxs-lookup"><span data-stu-id="51783-130">This behavior differs from the behavior for constraints.</span></span> <span data-ttu-id="51783-131">Rajoitukset toimivat kaksisuuntaisesti.</span><span class="sxs-lookup"><span data-stu-id="51783-131">Constraints occur in both directions.</span></span>

### <a name="example"></a><span data-ttu-id="51783-132">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="51783-132">Example</span></span>

<span data-ttu-id="51783-133">Seuraavassa lausekkeessa laskennan kohde on virtajohdon pituus ja syöttöarvo on väri:</span><span class="sxs-lookup"><span data-stu-id="51783-133">In the following expression, the target for the calculation is the length of a power cord, and the input value is a color:</span></span>  

<span data-ttu-id="51783-134">**Lauseke:** \[If Color == "Green", 1.5, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="51783-134">**Expression:** \[If Color == "Green", 1.5, 1.0\]</span></span>  

<span data-ttu-id="51783-135">Nimikettä määrittäessäsi laskenta luo **1,5**-kertaisen pituuden virtajohdon, jos määrität värimääreeksi **Green**.</span><span class="sxs-lookup"><span data-stu-id="51783-135">When you configure the item, the length of the power cord is set to **1.5** if you specify **Green** as the value of color attribute.</span></span> <span data-ttu-id="51783-136">Jos määrität muita värejä, pituudeksi asetetaan **1,0**.</span><span class="sxs-lookup"><span data-stu-id="51783-136">If you specify any other color, the length is set to **1.0**.</span></span> <span data-ttu-id="51783-137">Koska laskelmat ovat kuitenkin yksisuuntaisia, laskenta ei määritä väriarvomääritettä **vihreäksi** määrittäessäsi pituudeksi **1,5**.</span><span class="sxs-lookup"><span data-stu-id="51783-137">However, because calculations are unidirectional, the calculation doesn't set the value of the color attribute to **Green** if you specify a length of **1.5**.</span></span>

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a><span data-ttu-id="51783-138">Mitä tapahtuu, jos laskelmalla on kokonaislukutyyppinen kohdemäärite, mutta laskenta tuottaa desimaaliluvun?</span><span class="sxs-lookup"><span data-stu-id="51783-138">What happens if a calculation has a target attribute of the integer type but a calculation generates a decimal number?</span></span>
<span data-ttu-id="51783-139">Jos kohdemääritteen tietotyyppi on kokonaisluku, mutta laskenta tuottaa desimaaliluvun, palautetaan ainoastaan tuloksen kokonaislukuosa.</span><span class="sxs-lookup"><span data-stu-id="51783-139">If a target attribute is of the integer type, but a calculation generates a decimal number, only the integer part of the calculated result is returned.</span></span> <span data-ttu-id="51783-140">Desimaaliosa poistetaan, eikä tulosta pyöristetä.</span><span class="sxs-lookup"><span data-stu-id="51783-140">The decimal part is removed, and the result isn't rounded.</span></span> <span data-ttu-id="51783-141">Esimerkiksi tulos 12,70 näytetään arvona 12.</span><span class="sxs-lookup"><span data-stu-id="51783-141">For example, a result of 12.70 is shown as 12.</span></span>

## <a name="when-do-calculations-occur"></a><span data-ttu-id="51783-142">Milloin laskelmia esiintyy?</span><span class="sxs-lookup"><span data-stu-id="51783-142">When do calculations occur?</span></span>
<span data-ttu-id="51783-143">Laskelmat tehdään, kun kaikille syöttöattribuuteille on annettu arvo.</span><span class="sxs-lookup"><span data-stu-id="51783-143">Calculations occur when a value has been provided for all input attributes.</span></span>

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a><span data-ttu-id="51783-144">Voit korvata arvon, joka lasketaan kohteen määritteeseen?</span><span class="sxs-lookup"><span data-stu-id="51783-144">Can I overwrite the value that is calculated for the target attribute?</span></span>
<span data-ttu-id="51783-145">Voit korvata arvon, joka lasketaan kohteen määritteelle, ellei kohteen määritteen arvo ole piilotettu tai vain luku-muotoinen.</span><span class="sxs-lookup"><span data-stu-id="51783-145">You can overwrite the value that is calculated for the target attribute, unless the target attribute is set as hidden or read-only.</span></span>

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a><span data-ttu-id="51783-146">Kohdemääritteen määrittäminen piilotetuksi tai vain luettavaksi?</span><span class="sxs-lookup"><span data-stu-id="51783-146">How do I set a target attribute as hidden or read-only?</span></span>
<span data-ttu-id="51783-147">Aseta määrite piilotetuksi tai vain luku -tilaan noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="51783-147">To set an attribute as hidden or read-only, follow these steps.</span></span>

1.  <span data-ttu-id="51783-148">Napsauta **Tuotetietojen hallinta** &gt; **Yleinen** &gt; **Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="51783-148">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="51783-149">Valitse tuotemallin konfiguraatio ja napsauta toimintoruudulta **Muokkaa**-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="51783-149">Select a product configuration model, and then, on the Action Pane, click **Edit**.</span></span>
3.  <span data-ttu-id="51783-150">Valitse kohdemääritteenä käytettävä määrite **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="51783-150">On the **Constraint-based product configuration model details** page, select the attribute to use as a target attribute.</span></span>
4.  <span data-ttu-id="51783-151">Valitse **Määritteet** -pikavälilehdeltä **Piilotettu** tai **Vain luku-**.</span><span class="sxs-lookup"><span data-stu-id="51783-151">On the **Attributes** FastTab, select **Hidden** or **Read-only**.</span></span>

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a><span data-ttu-id="51783-152">Voiko laskenta korvata asettamani arvot?</span><span class="sxs-lookup"><span data-stu-id="51783-152">Can a calculation overwrite the values that I set?</span></span>
<span data-ttu-id="51783-153">Ei.</span><span class="sxs-lookup"><span data-stu-id="51783-153">No.</span></span> <span data-ttu-id="51783-154">Tuotteen konfiguroinnin yhteydessä asettamasi arvot ovat käytettävät arvot.</span><span class="sxs-lookup"><span data-stu-id="51783-154">The values that you set when you configure a product are the values that are used.</span></span> <span data-ttu-id="51783-155">Laskelma, joka suoritetaan, kun laskelman muuttuvat syötearvot eivät pysty korvaamaan tietylle määritteelle annettuja arvoja.</span><span class="sxs-lookup"><span data-stu-id="51783-155">The calculation that occurs when the input values in a calculation are changed can’t overwrite the values that you provide for a specific attribute.</span></span>

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a><span data-ttu-id="51783-156">Mitä tapahtuu, jos poistan laskelmasta syöttöarvon?</span><span class="sxs-lookup"><span data-stu-id="51783-156">What happens if I remove an input value in a calculation?</span></span>
<span data-ttu-id="51783-157">Jos poistat syötetyn arvon laskennassa, kohteen määritteen arvo poistetaan.</span><span class="sxs-lookup"><span data-stu-id="51783-157">If you remove an input value in a calculation, the value of the target attribute is also removed.</span></span>

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a><span data-ttu-id="51783-158">Miksi näyttöön tulee virhesanoma, jonka mukaan mallissa on ristiriita?</span><span class="sxs-lookup"><span data-stu-id="51783-158">Why do I receive an error message that says that my model is in contradiction?</span></span>
<span data-ttu-id="51783-159">Tämä sanoma tulee näkyviin, kun laskelma sisältää virheen tai vähintään yhdessä rajoituksessa on ristiriita.</span><span class="sxs-lookup"><span data-stu-id="51783-159">This message is shown when a calculation includes an error, or when a contradiction exists in one or more constraints.</span></span> <span data-ttu-id="51783-160">Katso lisätietoja ristiriidoista kohdasta [Lausekerajoitukset ja taulukkorajoitukset](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="51783-160">For more information about contradictions in constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span> <span data-ttu-id="51783-161">Tässä esitellään muutama tilanne, joissa laskelmavirheitä voi tapahtua:</span><span class="sxs-lookup"><span data-stu-id="51783-161">Here are some situations where errors can occur in calculations:</span></span>

-   <span data-ttu-id="51783-162">Arvo jaetaan nollalla.</span><span class="sxs-lookup"><span data-stu-id="51783-162">A value is divided by 0 (zero).</span></span>
-   <span data-ttu-id="51783-163">Seuraavien kahden elementin välillä on ristiriita:</span><span class="sxs-lookup"><span data-stu-id="51783-163">A conflict exists between the following two elements:</span></span>
    -   <span data-ttu-id="51783-164">Määritteen käytettävissä olevat arvot, joita rajoitetaan rajoitteella</span><span class="sxs-lookup"><span data-stu-id="51783-164">The values that are available for an attribute and are limited by a constraint</span></span>
    -   <span data-ttu-id="51783-165">Arvo, joka luodaan laskutoimituksessa</span><span class="sxs-lookup"><span data-stu-id="51783-165">A value that is generated by a calculation</span></span>
-   <span data-ttu-id="51783-166">Laskelman palauttamat arvot ovat määritteen toimialueen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="51783-166">The values that are returned by the calculation are outside the domain of the attribute.</span></span> <span data-ttu-id="51783-167">Esimerkki on kokonaisluku \[1..10\], joka lasketaan nollaan.</span><span class="sxs-lookup"><span data-stu-id="51783-167">An example is an integer from \[1..10\] that is calculated to 0.</span></span>

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a><span data-ttu-id="51783-168">Miksi näyttöön tulee virhesanoma, vaikka tuotemallini on vahvistettu onnistuneesti?</span><span class="sxs-lookup"><span data-stu-id="51783-168">Why do I receive an error message even though I successfully validated my product model?</span></span>
<span data-ttu-id="51783-169">Oikeellisuustarkistukseen ei sisällytetä laskentaa.</span><span class="sxs-lookup"><span data-stu-id="51783-169">Calculations aren't included in the validation.</span></span> <span data-ttu-id="51783-170">Sinun on testattava tuotemääritysmalli laskelmien virheiden löytämiseksi.</span><span class="sxs-lookup"><span data-stu-id="51783-170">You must test the product configuration model to find errors in calculations.</span></span> <span data-ttu-id="51783-171">Seuraavat vaiheet kuvaavat tuotekonfiguraatiomallin testaamisen.</span><span class="sxs-lookup"><span data-stu-id="51783-171">To test a product configuration model, follow these steps.</span></span>

1.  <span data-ttu-id="51783-172">Napsauta **Tuotetietojen hallinta** &gt; **Yleinen** &gt; **Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="51783-172">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="51783-173">Valitse tuotemallin konfiguraatio ja napsauta toimintoruudun **Suorita**-ryhmästä **Testi**-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="51783-173">Select a product configuration model, and then, on the Action Pane, in the **Run** group, click **Test**.</span></span>





