---
title: Resurssin kriittisyystyypit
description: Aiheessa selitetään resurssin kriittisyystyypit resurssien hallinnassa.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb2da2d58b7f98fad80d0ea63bf4445ec4d08163
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808349"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="1a237-103">Resurssin kriittisyystyypit</span><span class="sxs-lookup"><span data-stu-id="1a237-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1a237-104">Aiheessa selitetään resurssin kriittisyystyypit resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="1a237-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="1a237-105">Resurssin kriittisyys liittyy resursseihin ja ne siirretään työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="1a237-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="1a237-106">Sitä ei voi muuttaa työtilauksessa.</span><span class="sxs-lookup"><span data-stu-id="1a237-106">It can't be changed on a work order.</span></span> <span data-ttu-id="1a237-107">Resurssin kriittisyyttä käytetään laskettaessa työtilauksen kriittisyyttä työtilausten ajoituksessa.</span><span class="sxs-lookup"><span data-stu-id="1a237-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="1a237-108">Toisin sanoen sen avulla lasketaan, missä määrin resurssin kunnossapitotyö vaikuttaa yrityksen tuotantoaikatauluun ja tuottavuuteen.</span><span class="sxs-lookup"><span data-stu-id="1a237-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="1a237-109">Lisätietoja asetuksista, jotka liittyvät työtilausten ajoituksen luokituspisteiden laskentaan, on kohdassa [Resurssien hallinnan parametrit.](../setup-for-objects/enterprise-asset-management-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="1a237-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="1a237-110">Voit määrittää kriittisyyden määrittämällä ensin kriittisyystyypit, joita käytetään resurssin asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="1a237-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="1a237-111">Sen jälkeen määritetään resurssin kriittisyydet.</span><span class="sxs-lookup"><span data-stu-id="1a237-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="1a237-112">Määritä kriittisyystyypit</span><span class="sxs-lookup"><span data-stu-id="1a237-112">Set up criticality types</span></span>

1. <span data-ttu-id="1a237-113">Valitse **Resurssien hallinta** \> **Asetukset** \> **resurssit** \> **Kriittisyystyypit**.</span><span class="sxs-lookup"><span data-stu-id="1a237-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="1a237-114">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1a237-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="1a237-115">Kirjoita **Kriittisyys**-kenttään numero, joka ilmaisee kriittisyyden.</span><span class="sxs-lookup"><span data-stu-id="1a237-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="1a237-116">Kirjoita **Nimi**-kenttään kriittisyystyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="1a237-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="1a237-117">Syötä **Kerroin**-kenttään kerroin.</span><span class="sxs-lookup"><span data-stu-id="1a237-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="1a237-118">Tätä kerrointa käytetään työtilausten ajoittamisen laskennassa, kun määritetään käytettävä kriittisyystietue.</span><span class="sxs-lookup"><span data-stu-id="1a237-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="1a237-119">(Tietuetta, jonka kerroin on korkein, käytetään aina.) Tämä asetus on merkityksellinen, jos, kuten seuraavasta kuvasta näkyy, luodaan kriittisyysrivejä, joilla on sama kriittisyysarvo.</span><span class="sxs-lookup"><span data-stu-id="1a237-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Kriittisyyden tyyppisivu](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="1a237-121">Määritetä resurssin kriittisyydet.</span><span class="sxs-lookup"><span data-stu-id="1a237-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="1a237-122">Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssin kriittisyydet**.</span><span class="sxs-lookup"><span data-stu-id="1a237-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="1a237-123">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1a237-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="1a237-124">Tee tarvittavat valinnat seuraavista kentistä sen mukaan, miten yksityiskohtaista resurssin kriittisyyttä tarvitaan: **Toiminnallinen sijainti**, **resurssityyppi**, **Valmistaja**, **malli**, **resurssi**, **Työtyypin luokka**, **Työtyyppi**, **Työtyypin variantti** ja **Työtarve**.</span><span class="sxs-lookup"><span data-stu-id="1a237-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a237-125">Kun resurssin kriittisyys on valittuna, resurssien hallinta käy läpi kaikki resurssin kriittisyystietueet ja tarkistaa mahdollisen osuvuuden.</span><span class="sxs-lookup"><span data-stu-id="1a237-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="1a237-126">Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin.</span><span class="sxs-lookup"><span data-stu-id="1a237-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="1a237-127">Toisin sanoen resurssien hallinta tarkistaa ensin **Työtarve**-kentän.</span><span class="sxs-lookup"><span data-stu-id="1a237-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="1a237-128">Jos vastaavuutta ei löydy, se tarkistaa **Työtyypin variantti** -kentän.</span><span class="sxs-lookup"><span data-stu-id="1a237-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="1a237-129">Jos vastaavuutta ei löydy, se tarkistaa **Työtyyppi**-kentän jne.</span><span class="sxs-lookup"><span data-stu-id="1a237-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="1a237-130">Kuten näet sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, omaisuuden hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan.</span><span class="sxs-lookup"><span data-stu-id="1a237-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="1a237-131">Jos vastaavuutta ei löydy, käytetään oletustietuetta, jolla ei ole valintoja.</span><span class="sxs-lookup"><span data-stu-id="1a237-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="1a237-132">Valitse **Kriittisyys**-kentästä jokin edellisessä menettelyssä luomasi kriittisyyden arvo.</span><span class="sxs-lookup"><span data-stu-id="1a237-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="1a237-133">Huomautuksia kriittisyysasetuksista</span><span class="sxs-lookup"><span data-stu-id="1a237-133">Notes about criticality setup</span></span>

- <span data-ttu-id="1a237-134">Jos muutat resurssin kriittisyyttä tässä määrityksessäjälkeen, kun olet jo käyttänyt sitä työtilauksessa, työtilauksen kriittisyyttä ei päivitetä vastaavasti.</span><span class="sxs-lookup"><span data-stu-id="1a237-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="1a237-135">Työtilauksen kriittisyys lasketaan uudelleen aina, kun työtilausivi lisätään työtilaukseen tai poistetaan siitä.</span><span class="sxs-lookup"><span data-stu-id="1a237-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="1a237-136">Jos työtilaus sisältää useita työtilaustöitä, suurin kriittisyys, joka määräytyy **Kriittisyystyypit**-sivun **kerroin**-kentän mukaan, on aina käytössä työtilauksessa.</span><span class="sxs-lookup"><span data-stu-id="1a237-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="1a237-137">Yleensä resurssin kriittisyys voi muuttua kauden aikana.</span><span class="sxs-lookup"><span data-stu-id="1a237-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="1a237-138">Kriittisyyteen voidaan vaikuttaa ostamalla uusia laitteita, kunnostustöitä, ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="1a237-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="1a237-139">Harkitse resurssien kriittisyyden uudelleenarviointia säännöllisin väliajoin (esimerkiksi kerran vuodessa tai joka toinen vuosi) varmistaaksesi, että kriittisyysmääritykset vastaavat nykyisiä tuotannon asetuksia.</span><span class="sxs-lookup"><span data-stu-id="1a237-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]