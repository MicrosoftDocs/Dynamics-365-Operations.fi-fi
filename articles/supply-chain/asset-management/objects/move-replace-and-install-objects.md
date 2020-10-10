---
title: Resurssien siirtäminen, korvaaminen ja asentaminen
description: Tässä ohjeaiheessa kerrotaan, miten resursseja siirretään, korvataan ja asennetaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889550"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="1b950-103">Resurssien siirtäminen, korvaaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="1b950-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1b950-104">Tässä ohjeaiheessa kerrotaan, miten resursseja siirretään, korvataan ja asennetaan resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="1b950-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="1b950-105">Voit luoda yksittäisiä resursseja, joilla ei ole suhteita muihin resursseihin, tai voit luoda resurssirakenteen, joka sisältää pääresurssin (ylätason resurssi) ja siihen liittyvät aliresurssit.</span><span class="sxs-lookup"><span data-stu-id="1b950-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="1b950-106">Resurssien hallinnassa on kolme lähestymistapaa, joilla resurssin sijaintia siirretään ja muutetaan:</span><span class="sxs-lookup"><span data-stu-id="1b950-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="1b950-107">**Siirrä** – Siirrä resurssi joko toiseen resurssirakenteeseen tai toiseen sijaintiin samassa resurssirakenteessa.</span><span class="sxs-lookup"><span data-stu-id="1b950-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="1b950-108">**Korvaa** – Poista resurssi resurssirakenteesta tilapäisesti, jotta se voidaan korjata tai kunnostaa, ja lisätä sitten kunnostettu resurssi takaisin resurssirakenteeseen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="1b950-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="1b950-109">Vaihtoehtoisesti voit korvata käytetyn resurssin pysyvästi uudella resurssilla.</span><span class="sxs-lookup"><span data-stu-id="1b950-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="1b950-110">**Asenna** – Asenna pääresurssi ja kaikki siihen liittyvät aliresurssit toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="1b950-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="1b950-111">Siirrettävä, korvattava tai asennettava resurssi saattaa liittyä toiseen toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="1b950-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="1b950-112">Tässä tapauksessa resurssi voi käyttää toiminnallisen sijainnin taloushallinnon dimensioita.</span><span class="sxs-lookup"><span data-stu-id="1b950-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="1b950-113">**Toiminnallisen sijainnin tyypit** -sivulla voit määrittää taloushallinnon dimensioiden käsittelyn toiminnallisissa sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="1b950-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="1b950-114">Siirrä resurssi</span><span class="sxs-lookup"><span data-stu-id="1b950-114">Move asset</span></span>

<span data-ttu-id="1b950-115">Käytä **Siirrä resurssi** -toimintoa siirtääksesi resurssin joko toiseen resurssirakenteeseen tai toiseen sijaintiin samassa resurssirakenteessa.</span><span class="sxs-lookup"><span data-stu-id="1b950-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="1b950-116">Voit myös siirtää resurssin pois resurssirakenteesta niin, että siitä tulee itsenäinen resurssi, jolla ei ole rakennesuhteita.</span><span class="sxs-lookup"><span data-stu-id="1b950-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="1b950-117">Älä käytä tätä toimintoa, jos resursseja korjataan tai vaihdetaan väliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="1b950-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="1b950-118">Käytä sen sijaan **Korvaa resurssi** -toimintoa, joka on kuvattu myöhemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="1b950-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="1b950-119">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**.</span><span class="sxs-lookup"><span data-stu-id="1b950-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="1b950-120">Valitse luettelosta siirrettävä resurssi.</span><span class="sxs-lookup"><span data-stu-id="1b950-120">In the list, select the asset to move.</span></span> <span data-ttu-id="1b950-121">Jos resurssilla on aliresursseja, siirrät myös kyseiset resurssit.</span><span class="sxs-lookup"><span data-stu-id="1b950-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="1b950-122">Valitse **Siirrä resurssi**.</span><span class="sxs-lookup"><span data-stu-id="1b950-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="1b950-123">Jos haluat siirtää resurssin siten, että siitä tulee osa resurssirakennetta, valitse uusi pääresurssi **Pääresurssi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1b950-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="1b950-124">Jos siirrät alatason resurssin ja haluat tehdä siitä erillisen resurssin, jolla ei ole rakennesuhteita, jätä **Pääresurssi**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="1b950-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="1b950-125">**Voimassa**-kenttään valitaan oletusarvoisesti nykyinen päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="1b950-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="1b950-126">Voit kuitenkin valita eri päivämäärän ja ajan, josta lähtien resurssin siirto on voimassa.</span><span class="sxs-lookup"><span data-stu-id="1b950-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="1b950-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b950-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="1b950-128">Korvaa resurssi</span><span class="sxs-lookup"><span data-stu-id="1b950-128">Replace asset</span></span>

<span data-ttu-id="1b950-129">Käytä **Korvaa resurssi** -toimintoa resurssin korjausten, kunnostuksen tai kuluneen resurssin pysyvän korvaamisen uudella resurssilla yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="1b950-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="1b950-130">Tätä funktiota käytetään korvaamaan resurssirakenteen alieliresurssit.</span><span class="sxs-lookup"><span data-stu-id="1b950-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="1b950-131">Pääresursseille (eli resursseille, joilla ei tällä hetkellä ole pääresurssia) tämä korvaus tehdään toiminnallisessa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="1b950-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="1b950-132">Lisätietoja toiminnallisen sijainnin pääresurssien korvaamisesta on kohdassa [Resurssien asentaminen toiminnallisiin sijainteihin](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="1b950-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1b950-133">Jos korjausosasto liittyy tuotanto-osastoosi, voit luoda toiminnallisia sijainteja, kuten **Korjaus**, **Hävikki** ja **Varastointi**, jotta voidaan käsitellä resurssien korjausta ja korvaamista.</span><span class="sxs-lookup"><span data-stu-id="1b950-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="1b950-134">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**.</span><span class="sxs-lookup"><span data-stu-id="1b950-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="1b950-135">Valitse luettelosta korvattava aliresurssi.</span><span class="sxs-lookup"><span data-stu-id="1b950-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="1b950-136">Jos resurssilla on aliresursseja, korvaat myös kyseiset resurssit.</span><span class="sxs-lookup"><span data-stu-id="1b950-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="1b950-137">Valitse **Korvaa resurssi**.</span><span class="sxs-lookup"><span data-stu-id="1b950-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="1b950-138">**Rakenne on muuttunut** -kentässä näkyy viimeisin päivämäärä ja aika, jolloin valittu resurssi ja siihen liittyvät aliresurssit siirrettiin resurssirakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="1b950-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="1b950-139">Valitse **Valittu resurssi** -osan **Toiminnallinen kohdesijainti** -kentässä toiminnallinen sijainti, johon resurssi siirretään.</span><span class="sxs-lookup"><span data-stu-id="1b950-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="1b950-140">Valitse esimerkiksi sijainniksi **Korjaus** tai **Hävikki**.</span><span class="sxs-lookup"><span data-stu-id="1b950-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="1b950-141">**Pääresurssi**-osan **Voimassa**-kentässä näkyy viimeisin päivämäärä ja aika, jolloin pääresurssi ja siihen liittyvät aliresurssit on asennettu tai siirretty nykyiseen toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="1b950-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="1b950-142">Valitse **Uusi resurssi** -osion **Resurssi**-kentässä resurssi, joka lisätään väliaikaisena tai pysyvänä korvaavana resurssina valitulle resurssille.</span><span class="sxs-lookup"><span data-stu-id="1b950-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="1b950-143">Tämä resurssi saattaa tällä hetkellä sijaita toisessa toiminnallisessa sijainnissa, kuten **Varastointi**.</span><span class="sxs-lookup"><span data-stu-id="1b950-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="1b950-144">**Voimassa lähtien** -osan **Voimassa**-kenttään valitaan oletusarvoisesti nykyinen päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="1b950-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="1b950-145">Voit kuitenkin valita eri päivämäärän ja ajan, josta lähtien resurssin korvaaminen on voimassa.</span><span class="sxs-lookup"><span data-stu-id="1b950-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="1b950-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b950-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="1b950-147">Asenna resurssi</span><span class="sxs-lookup"><span data-stu-id="1b950-147">Install asset</span></span>

<span data-ttu-id="1b950-148">Käytä **Asenna resurssi** -toimintoa resurssirakenteen asentamiseen toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="1b950-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="1b950-149">Valitse aina pääresurssi.</span><span class="sxs-lookup"><span data-stu-id="1b950-149">Always select a parent asset.</span></span> <span data-ttu-id="1b950-150">Pääresurssi ja siihen liittyvät aliresurssit siirretään valittuun toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="1b950-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="1b950-151">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**.</span><span class="sxs-lookup"><span data-stu-id="1b950-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="1b950-152">Valitse luettelosta pääresurssi, joka asennetaan toiseen toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="1b950-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="1b950-153">Valitse **Asenna resurssi**.</span><span class="sxs-lookup"><span data-stu-id="1b950-153">Select **Install asset**.</span></span>

    <span data-ttu-id="1b950-154">**Määritteet**-osassa näkyvät resurssimääritteet, jotka on määritetty pääresurssille.</span><span class="sxs-lookup"><span data-stu-id="1b950-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="1b950-155">Valitse uusi sijainti **Toiminnallinen sijainti** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1b950-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="1b950-156">**Voimassa**-kenttään valitaan oletusarvoisesti nykyinen päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="1b950-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="1b950-157">Voit kuitenkin valita eri päivämäärän ja ajan, josta lähtien resurssin asentaminen resurssirakenteeseen on voimassa.</span><span class="sxs-lookup"><span data-stu-id="1b950-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="1b950-158">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b950-158">Select **OK**.</span></span>
