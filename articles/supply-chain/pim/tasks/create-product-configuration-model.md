---
title: Luo tuotemääritysmalli
description: Tässä menettelyssä käsitellään tuotemallien luomista sekä perustietojen, kuten määritteiden ja alikomponenttien antamista.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921362"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="61bd4-103">Luo tuotemääritysmalli</span><span class="sxs-lookup"><span data-stu-id="61bd4-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61bd4-104">Tässä menettelyssä käsitellään tuotemallien luomista sekä perustietojen, kuten määritteiden ja alikomponenttien antamista.</span><span class="sxs-lookup"><span data-stu-id="61bd4-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="61bd4-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="61bd4-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="61bd4-106">Tuotemallin luominen</span><span class="sxs-lookup"><span data-stu-id="61bd4-106">Create a product model</span></span>

1. <span data-ttu-id="61bd4-107">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="61bd4-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-108">Select **New**.</span></span>
1. <span data-ttu-id="61bd4-109">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="61bd4-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="61bd4-110">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="61bd4-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="61bd4-111">Valitse **Solver-strategia**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="61bd4-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="61bd4-112">Selvitysstrategia määrittää, miten poissulkevan tuotekonfiguraation mallin rajoitukset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="61bd4-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="61bd4-113">Tämä valinta voi vaikuttaa tuotekonfiguraatiomallin suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="61bd4-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="61bd4-114">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="61bd4-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="61bd4-115">Juurikomponentti vastaa tuotekonfiguraatiomallia, mutta sitä voi käyttää myös muissa tuotemalleissa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="61bd4-116">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-116">Select **OK**.</span></span>
1. <span data-ttu-id="61bd4-117">Valitse vaihtoehto **Käytä konfigurointeja** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="61bd4-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="61bd4-118">Jos konfiguraation parametrin uudellenkäyttöasetukseksi on valittu Kyllä, järjestelmä etsii identtisiä konfiguraatioita jokaisen konfigurointi-istunnon jälkeen ja käyttää niitä uudelleen, jos tarkka vastine löytyy.</span><span class="sxs-lookup"><span data-stu-id="61bd4-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="61bd4-119">Lisää määritteet</span><span class="sxs-lookup"><span data-stu-id="61bd4-119">Add attributes</span></span>

1. <span data-ttu-id="61bd4-120">Laajenna **Määritteet**-osa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="61bd4-121">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-121">Select **Add**.</span></span>
3. <span data-ttu-id="61bd4-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="61bd4-123">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="61bd4-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="61bd4-124">Kirjoita arvo **Selvityksen nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="61bd4-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="61bd4-125">Tuotekonfiguroinnin rajoiteselvitys käyttää selvitysnimeä.</span><span class="sxs-lookup"><span data-stu-id="61bd4-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="61bd4-126">Siinä ei saa olla välilyöntejä tai erikoismerkkejä. Alaviivaa (_) saa kuitenkin käyttää.</span><span class="sxs-lookup"><span data-stu-id="61bd4-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="61bd4-127">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="61bd4-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="61bd4-128">Konfiguraation käyttäjä näkee kuvaustekstin, joten se auttaa valitsemaan oikean määritteen arvon.</span><span class="sxs-lookup"><span data-stu-id="61bd4-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="61bd4-129">Anna tai valitse arvo **Määritteen tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="61bd4-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="61bd4-130">Määritteen tyyppi määrittää, mitä arvoja määritteessä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="61bd4-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="61bd4-131">Valitse **Sisällytä uudelleenkäyttöön** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="61bd4-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="61bd4-132">Tämä vaihtoehto on käytettävissä vain, kun Käytä konfigurointeja -asetus on valittu.</span><span class="sxs-lookup"><span data-stu-id="61bd4-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="61bd4-133">Sisällytetyn määritteen uudelleenkäytön valintaruutu tarkoittaa, että määritettä harkitaan, kun järjestelmää etsii tarkkaa vastinetta.</span><span class="sxs-lookup"><span data-stu-id="61bd4-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="61bd4-134">Lisää alikomponentit</span><span class="sxs-lookup"><span data-stu-id="61bd4-134">Add subcomponents</span></span>

1. <span data-ttu-id="61bd4-135">Laajenna **Alikomponentit**-osa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="61bd4-136">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-136">Select **Add**.</span></span>
3. <span data-ttu-id="61bd4-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="61bd4-138">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="61bd4-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="61bd4-139">Kirjoita arvo **Selvityksen nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="61bd4-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="61bd4-140">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="61bd4-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="61bd4-141">Anna tai valitse arvo **Komponentti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="61bd4-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="61bd4-142">JokaisenKunkin alikomponentin on viitattava komponentin määritykseen.</span><span class="sxs-lookup"><span data-stu-id="61bd4-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="61bd4-143">Tämä rakenne tukee komponenttien uudelleenkäyttöä ja varmistaa, että määritettyä komponenttia voidaan käyttää useissa tuotemalleissa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="61bd4-144">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-144">Select **Save**.</span></span>
9. <span data-ttu-id="61bd4-145">Valitse **Tuoterakennerivin tiedot**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="61bd4-146">Tuoterakennerivin tiedot -lomakkeen avulla käyttäjä voi valita alikomponentin pakolliset osat.</span><span class="sxs-lookup"><span data-stu-id="61bd4-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="61bd4-147">Jokaiselle komponentille annetaan kiinteä arvo tai se yhdistetään määritteeseen.</span><span class="sxs-lookup"><span data-stu-id="61bd4-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="61bd4-148">Yhdistettäessä määritteeseen tuoterakennerivin ominaisuus saa eri arvon valitun konfiguraation mukaan.</span><span class="sxs-lookup"><span data-stu-id="61bd4-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="61bd4-149">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="61bd4-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="61bd4-150">Jokain alikomponentin vastaa määritettävää päätuotetta, jossa on poissulkevan konfiguraation tekniikkaa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="61bd4-151">Viittaus tehdään nimiketunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="61bd4-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="61bd4-152">Valitse **Määritä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="61bd4-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="61bd4-153">Valitse **Laskenta**-kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="61bd4-154">Laskenta-asetuksen määrittäminen varmistaa, että tuote sisällytetään tuotteen kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="61bd4-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="61bd4-155">Valitse **Määritys**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="61bd4-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="61bd4-156">Valitse **Määritä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="61bd4-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="61bd4-157">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="61bd4-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="61bd4-158">Määräkentän määrittää, kuinka paljon tätä tuotetta kulutetaan määritetyssä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="61bd4-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="61bd4-159">Valitse **Määritä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="61bd4-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="61bd4-160">Lisää **Per sarja** -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="61bd4-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="61bd4-161">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="61bd4-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]