---
title: Mobiililaitteen valikkovaihtoehdon määrittäminen tuottamaan keräilyrivin yhteenvedon
description: Tässä ohjeaiheessa selitetään, miten voit määrittää, milloin kaikkien työrivien luettelo näytetään varastotyöntekijöille, jotka käsittelevät varastotyötä mobiililaitteilla. Tämä ominaisuus voi olla hyödyllinen varastotyöntekijöille, jotka tarvitsevat usein yhteenvedon työtilauksen keräilyriveistä, jotta he voivat optimoida keräilyjärjestyksen.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: a52a789044ca66c6771224a6cf0be8749bc99e5a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2020
ms.locfileid: "3837309"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="53f0e-104">Mobiililaitteen valikkovaihtoehdon määrittäminen tuottamaan keräilyrivin yhteenvedon</span><span class="sxs-lookup"><span data-stu-id="53f0e-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="53f0e-105">Tässä ohjeaiheessa selitetään, miten määritetään keräilyrivien mobiililaitteille tarkoitettuun yhteenvetoon liittyvät valikkovaihtoehdot, joita käytetään keräilytyön käsittelyssä.</span><span class="sxs-lookup"><span data-stu-id="53f0e-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="53f0e-106">Keräilyrivin yhteenvedon avulla varastotyöntekijät pystyvät tarkastelemaan ja valitsemaan töitä luettelosta, joka sisältää kaikki heidän kulloiseenkin tehtäväänsä liittyvät työrivit.</span><span class="sxs-lookup"><span data-stu-id="53f0e-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="53f0e-107">Tämä ominaisuus voi auttaa työntekijöitä optimoimaan keräilyjärjestyksensä.</span><span class="sxs-lookup"><span data-stu-id="53f0e-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="53f0e-108">Toiminto sisältää vaihtoehtoja vakiomuotoisen **Ohitus**-painikkeen korvaamiseksi. Tällä painikkeella työntekijät voivat käydä rivit läpi yksi kerrallaan kiinteässä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="53f0e-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="53f0e-109">(Painikkeen käyttäminen on kuitenkin edelleen mahdollista.)</span><span class="sxs-lookup"><span data-stu-id="53f0e-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="53f0e-110">Järjestelmänvalvojat voivat määrittää kunkin valikkovaihtoehdon erikseen ja hallita miten, milloin ja missä varastosovellus esittää keräilyrivin yhteenvedon.</span><span class="sxs-lookup"><span data-stu-id="53f0e-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="53f0e-111">Työn keräilyriviyhteenveto-toiminnon käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="53f0e-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="53f0e-112">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="53f0e-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="53f0e-113">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="53f0e-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="53f0e-114">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="53f0e-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="53f0e-115">**Moduuli:** _Varastonhallinta_</span><span class="sxs-lookup"><span data-stu-id="53f0e-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="53f0e-116">**Toiminnon nimi:** _Työn keräilyrivin yhteenveto_</span><span class="sxs-lookup"><span data-stu-id="53f0e-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="53f0e-117">Valikkovaihtoehtojen määrittäminen näyttämään luettelon kaikista työriveistä</span><span class="sxs-lookup"><span data-stu-id="53f0e-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="53f0e-118">Määritä mobiililaitteen valikkovaihtoehto tuottamaan keräilyrivin yhteenveto seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="53f0e-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="53f0e-119">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="53f0e-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="53f0e-120">Valitse tai luo keräilytyöhön liittyvä valikkovaihtoehto ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="53f0e-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="53f0e-121">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="53f0e-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="53f0e-122">**Käytä aiemmin luotua työtä:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="53f0e-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="53f0e-123">**Ohjaaja:** *Käyttäjän ohjaama* tai *Järjestelmän ohjaama*</span><span class="sxs-lookup"><span data-stu-id="53f0e-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="53f0e-124">Lisätietoja valikkovaihtoehtojen luomisesta ja **Mobiililaitteen valikkovaihtoehdot** -sivulla käytettävissä olevien eri asetusten käyttämisestä: [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="53f0e-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="53f0e-125">Määritä toiminto **Yleiset**-pikavalikossa määrittämällä **Näytä työriviluettelo** -kentän arvoksi jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="53f0e-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="53f0e-126">**Näytä vain pyydettäessä** – Työntekijät voivat avata keräilyriviluettelon valitsemalla **Siirry kohteeseen** -painikkeen varastosovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53f0e-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="53f0e-127">**Näytä jokaisen keräilyn alussa** – Työntekijät näkevät luettelon aina, kun he aloittavat keräilyrivin tai saavat sen valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="53f0e-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="53f0e-128">He voivat myös tarkastella luetteloa uudelleen valitsemalla **Siirry kohteeseen** -painikkeen varastosovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53f0e-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="53f0e-129">**Näytä vain ensimmäisen keräilyn alussa** – Työtekijät näkevät luettelon aina, kun he aloittavat uuden keräystyön, mutta eivät jokaisen rivin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="53f0e-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="53f0e-130">He voivat myös tarkastella luetteloa uudelleen valitsemalla **Siirry kohteeseen** -painikkeen varastosovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="53f0e-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="53f0e-131">**Älä näytä koskaan** – Vakiomuotoinen **Ohita**-painike näkyy varastosovelluksessa ja työriviluettelon näyttö on kytketty pois.</span><span class="sxs-lookup"><span data-stu-id="53f0e-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="53f0e-132">**Ohita**-painikkeen avulla työntekijät käyvät rivit läpi yksi kerrallaan kiinteässä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="53f0e-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="53f0e-133">He voivat myös selata luetteloa niin monta kertaa kuin on tarpeen, kunnes kaikki rivit on käsitelty.</span><span class="sxs-lookup"><span data-stu-id="53f0e-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="53f0e-134">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="53f0e-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="53f0e-135">Jos määrität **Näytä työriviluettelo**-kentän arvoksi minkä tahansa muun kuin *Älä näytä koskaan*, toimintoruudun **Kenttäluettelo**-painike muuttuu käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="53f0e-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="53f0e-136">Valitse toimintoruudussa **Kenttäluettelo**.</span><span class="sxs-lookup"><span data-stu-id="53f0e-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="53f0e-137">Määritä **Kenttäluettelo**-sivulla tiedot, jotka varastosovellus näyttää kunkin luettelon rivin osalta.</span><span class="sxs-lookup"><span data-stu-id="53f0e-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="53f0e-138">**Ensisijainen ohjausobjekti** -kentän arvona on aina *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="53f0e-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="53f0e-139">Siksi jokainen luettelon rivi alkaa rivinumerolla.</span><span class="sxs-lookup"><span data-stu-id="53f0e-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="53f0e-140">Käytä jäljellä olevia **Näyttökenttä**-kenttiä lisätäksesi jopa seitsemän lisänäyttökenttää tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="53f0e-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="53f0e-141">Valitse jokaisessa **Näyttökenttä**-kentässä työrivikentän nimi.</span><span class="sxs-lookup"><span data-stu-id="53f0e-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="53f0e-142">Kukin rivi näyttä tällöin arvon kyseiselle kentälle.</span><span class="sxs-lookup"><span data-stu-id="53f0e-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="53f0e-143">Arvot näytetään tässä valitussa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="53f0e-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="53f0e-144">Voit jättää osan **Näyttökenttä**-kentistä tyhjiksi, jos et tarvitse kaikkia seitsemää arvoa.</span><span class="sxs-lookup"><span data-stu-id="53f0e-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="53f0e-145">Valitse toimintoruudussa **Tallenna** ja sulje sitten **Kenttäluettelo**-sivu.</span><span class="sxs-lookup"><span data-stu-id="53f0e-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>
