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
ms.openlocfilehash: b87b411ed24f89a674ec3fb7ac44d3ab1d8a720a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819983"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="a7688-103">Luo tuotemääritysmalli</span><span class="sxs-lookup"><span data-stu-id="a7688-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7688-104">Tässä menettelyssä käsitellään tuotemallien luomista sekä perustietojen, kuten määritteiden ja alikomponenttien antamista.</span><span class="sxs-lookup"><span data-stu-id="a7688-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="a7688-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a7688-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="a7688-106">Tuotemallin luominen</span><span class="sxs-lookup"><span data-stu-id="a7688-106">Create a product model</span></span>
1. <span data-ttu-id="a7688-107">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="a7688-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a7688-108">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="a7688-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="a7688-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a7688-109">Click New.</span></span>
4. <span data-ttu-id="a7688-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a7688-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a7688-112">Valitse Solver-strategia-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="a7688-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="a7688-113">Selvitysstrategia määrittää, miten poissulkevan tuotekonfiguraation mallin rajoitukset käsitellään.</span><span class="sxs-lookup"><span data-stu-id="a7688-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="a7688-114">Tämä valinta voi vaikuttaa tuotekonfiguraatiomallin suorituskykyyn.</span><span class="sxs-lookup"><span data-stu-id="a7688-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="a7688-115">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a7688-116">Juurikomponentti vastaa tuotekonfiguraatiomallia, mutta sitä voi käyttää myös muissa tuotemalleissa.</span><span class="sxs-lookup"><span data-stu-id="a7688-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="a7688-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a7688-117">Click OK.</span></span>
9. <span data-ttu-id="a7688-118">Valitse vaihtoehto Käytä konfigurointeja -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a7688-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="a7688-119">Jos konfiguraation parametrin uudellenkäyttöasetukseksi on valittu Kyllä, järjestelmä etsii identtisiä konfiguraatioita jokaisen konfigurointi-istunnon jälkeen ja käyttää niitä uudelleen, jos tarkka vastine löytyy.</span><span class="sxs-lookup"><span data-stu-id="a7688-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="a7688-120">Lisää määritteet</span><span class="sxs-lookup"><span data-stu-id="a7688-120">Add attributes</span></span>
1. <span data-ttu-id="a7688-121">Laajenna Määritteet-osa.</span><span class="sxs-lookup"><span data-stu-id="a7688-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="a7688-122">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a7688-122">Click Add.</span></span>
3. <span data-ttu-id="a7688-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a7688-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a7688-124">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a7688-125">Kirjoita arvo Selvityksen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="a7688-126">Tuotekonfiguroinnin rajoiteselvitys käyttää selvitysnimeä.</span><span class="sxs-lookup"><span data-stu-id="a7688-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="a7688-127">Siinä ei saa olla välilyöntejä tai erikoismerkkejä. Alaviivaa (_) saa kuitenkin käyttää.</span><span class="sxs-lookup"><span data-stu-id="a7688-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="a7688-128">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a7688-129">Konfiguraation käyttäjä näkee kuvaustekstin, joten se auttaa valitsemaan oikean määritteen arvon.</span><span class="sxs-lookup"><span data-stu-id="a7688-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="a7688-130">Anna tai valitse arvo Määritteen tyyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a7688-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="a7688-131">Määritteen tyyppi määrittää, mitä arvoja määritteessä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="a7688-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="a7688-132">Valitse Sisällytä uudelleenkäyttöön -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a7688-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="a7688-133">Tämä vaihtoehto on käytettävissä vain, kun Käytä konfigurointeja -asetus on valittu.</span><span class="sxs-lookup"><span data-stu-id="a7688-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="a7688-134">Sisällytetyn määritteen uudelleenkäytön valintaruutu tarkoittaa, että määritettä harkitaan, kun järjestelmää etsii tarkkaa vastinetta.</span><span class="sxs-lookup"><span data-stu-id="a7688-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="a7688-135">Lisää alikomponentit</span><span class="sxs-lookup"><span data-stu-id="a7688-135">Add subcomponents</span></span>
1. <span data-ttu-id="a7688-136">Laajenna Alikomponentit-osa.</span><span class="sxs-lookup"><span data-stu-id="a7688-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="a7688-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a7688-137">Click Add.</span></span>
3. <span data-ttu-id="a7688-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a7688-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a7688-139">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a7688-140">Kirjoita arvo Selvityksen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="a7688-141">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="a7688-142">Anna tai valitse arvo Komponentti-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a7688-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="a7688-143">JokaisenKunkin alikomponentin on viitattava komponentin määritykseen.</span><span class="sxs-lookup"><span data-stu-id="a7688-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="a7688-144">Tämä rakenne tukee komponenttien uudelleenkäyttöä ja varmistaa, että määritettyä komponenttia voidaan käyttää useissa tuotemalleissa.</span><span class="sxs-lookup"><span data-stu-id="a7688-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="a7688-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a7688-145">Click Save.</span></span>
9. <span data-ttu-id="a7688-146">Valitse Tuoterakennerivin tiedot.</span><span class="sxs-lookup"><span data-stu-id="a7688-146">Click BOM line details.</span></span>
    * <span data-ttu-id="a7688-147">Tuoterakennerivin tiedot -lomakkeen avulla käyttäjä voi valita alikomponentin pakolliset osat.</span><span class="sxs-lookup"><span data-stu-id="a7688-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="a7688-148">Jokaiselle komponentille annetaan kiinteä arvo tai se yhdistetään määritteeseen.</span><span class="sxs-lookup"><span data-stu-id="a7688-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="a7688-149">Yhdistettäessä määritteeseen tuoterakennerivin ominaisuus saa eri arvon valitun konfiguraation mukaan.</span><span class="sxs-lookup"><span data-stu-id="a7688-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="a7688-150">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a7688-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a7688-151">Jokain alikomponentin vastaa määritettävää päätuotetta, jossa on poissulkevan konfiguraation tekniikkaa.</span><span class="sxs-lookup"><span data-stu-id="a7688-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="a7688-152">Viittaus tehdään nimiketunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="a7688-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="a7688-153">Valitse Määritä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a7688-153">Select the Set check box.</span></span>
12. <span data-ttu-id="a7688-154">Valitse Laskenta-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a7688-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="a7688-155">Laskenta-asetuksen määrittäminen varmistaa, että tuote sisällytetään tuotteen kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="a7688-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="a7688-156">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a7688-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="a7688-157">Valitse Määritä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a7688-157">Select the Set check box.</span></span>
15. <span data-ttu-id="a7688-158">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a7688-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a7688-159">Määräkentän määrittää, kuinka paljon tätä tuotetta kulutetaan määritetyssä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="a7688-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="a7688-160">Valitse Määritä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a7688-160">Select the Set check box.</span></span>
17. <span data-ttu-id="a7688-161">Lisää Per sarja -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a7688-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="a7688-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a7688-162">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]