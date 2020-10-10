---
title: Luo ostotilauksiin perustuvia resursseja
description: Tässä ohjeaiheessa kerrotaan, kuinka voit luoda luettelon resursseista, joita voidaan käyttää perustana luotaessa resursseja resurssien hallinnan kunnossapitotöille.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889022"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="2f2de-103">Luo ostotilauksiin perustuvia resursseja</span><span class="sxs-lookup"><span data-stu-id="2f2de-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2f2de-104">Tässä ohjeaiheessa kerrotaan, kuinka voit luoda luettelon resursseista, joita voidaan käyttää perustana luotaessa resursseja resurssien hallinnan kunnossapitotöille.</span><span class="sxs-lookup"><span data-stu-id="2f2de-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="2f2de-105">Resurssien perusteella voit tarkastella luetteloa ostotilausriveistä, jotka on luotu kyseisiin nimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="2f2de-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="2f2de-106">Tämän toiminnon tarkoituksena on helposti luoda resurssi resurssien hallinnassa ostotilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="2f2de-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="2f2de-107">Ensin määritetään nimikkeet, joita käytetään resurssien luomiseen ostotilauksesta kohdassa **Resurssinimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="2f2de-108">Kun olet luonut ostotilausrivin, voit luoda resurssit **Odottavat resurssit** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="2f2de-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="2f2de-109">On mahdollista päättää, missä ostotilauksen vaiheessa resurssi on luotava.</span><span class="sxs-lookup"><span data-stu-id="2f2de-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="2f2de-110">Valitse resurssinimikkeet</span><span class="sxs-lookup"><span data-stu-id="2f2de-110">Select asset items</span></span>

1. <span data-ttu-id="2f2de-111">Valitse **resurssien hallinta** > **Asetukset** > **resurssit** > **nimikkeet**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="2f2de-112">Luo uusi resurssinimike napsauttamalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="2f2de-113">Valitse **Nimiketunnus**-kentässä nimike.</span><span class="sxs-lookup"><span data-stu-id="2f2de-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="2f2de-114">Kun poistut kyseisestä kentästä, nimikkeen nimi lisätään automaattisesti **Tuotteen nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f2de-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="2f2de-115">Valitse **Yleiset**-pikavälilehdessä nimikkeen resurssityyppi.</span><span class="sxs-lookup"><span data-stu-id="2f2de-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="2f2de-116">Valitse nimikkeelle resurssin valmistaja ja malli.</span><span class="sxs-lookup"><span data-stu-id="2f2de-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="2f2de-117">Tallenna nimike.</span><span class="sxs-lookup"><span data-stu-id="2f2de-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="2f2de-118">Resurssien luominen odottavista resursseista</span><span class="sxs-lookup"><span data-stu-id="2f2de-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="2f2de-119">Valitse **resurssien hallinta** > **yhteiset** > **resurssit** > **odottavat resurssit**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="2f2de-120">Näet päivitetyn luettelon ostotilauksista, jotka perustuvat **resurssinimikkeet** -kohdassa valittuihin nimikkeisiin.</span><span class="sxs-lookup"><span data-stu-id="2f2de-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="2f2de-121">Voit suodattaa ostotilausten tiloja ja valita, missä elinkaaren tilassa resurssi luodaan.</span><span class="sxs-lookup"><span data-stu-id="2f2de-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="2f2de-122">Haluat ehkä esimerkiksi luoda resursseja vain, kun tuotteen vastaanotto on kirjattu ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="2f2de-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="2f2de-123">Valitse ostotilausrivin **Viitenumero**-linkki, jos haluat tarkastella nimikkeen yksityiskohtaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="2f2de-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="2f2de-124">Jos haluat muokata, mitkä dimensiot näkyvät **varastodimensiot**-pikavälilehdessä, napsauta **Näytä dimensiot** -painiketta ja tee valintasi.</span><span class="sxs-lookup"><span data-stu-id="2f2de-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="2f2de-125">Jos haluat luoda resurssin ostotilausrivin perusteella, valitse luettelo sivulla kyseisen rivin **Merkitse**-sarakkeen valintaruutu ja valitse sitten **Luo resurssit.**</span><span class="sxs-lookup"><span data-stu-id="2f2de-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="2f2de-126">Näyttöön tulee sanoma, jossa ilmoitetaan resurssin tunnus.</span><span class="sxs-lookup"><span data-stu-id="2f2de-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="2f2de-127">Valitse resurssi **Kaikki resurssit** -luettelosta ja valitse **Muokkaa** lisätäksesi lisätietoja resurssiin.</span><span class="sxs-lookup"><span data-stu-id="2f2de-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="2f2de-128">Jos haluat poistaa rivin **Odottavat resurssit** -kohdassa, koska et halua luoda resurssia, valitse kyseisen rivin **Merkitse**-sarakkeen valintaruutu ja valitse **Hylkää odottavat resurssit**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="2f2de-129">Näyttöön tulee sanoma, jossa ilmoitetaan resurssin tunnus.</span><span class="sxs-lookup"><span data-stu-id="2f2de-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="2f2de-130">Et poista ostotilausta tai myyntitilausta, vaan vain sen tietueen, josta olet voinut luoda resurssin **resurssien hallinnassa**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="2f2de-131">Kaikki tuotedimensiot (koko, väri, konfiguraatio jne.) siirretään automaattisesti resurssin määritteisiin.</span><span class="sxs-lookup"><span data-stu-id="2f2de-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="2f2de-132">Seurantadimensiot (sarjanumerot) tallennetaan suoraan resurssiin, kun resurssi luodaan.</span><span class="sxs-lookup"><span data-stu-id="2f2de-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="2f2de-133">Odottavien resurssien etsiminen</span><span class="sxs-lookup"><span data-stu-id="2f2de-133">Find pending assets</span></span>

<span data-ttu-id="2f2de-134">Voit tarkistaa odottavat resurssit suorittamalla **Odottavien resurssien määrä** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="2f2de-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="2f2de-135">Tätä toimintoa voidaan käyttää esimerkiksi ilmoituksen vastaanottamiseen aina, kun odottava resurssi on valmis luotavaksi resurssina.</span><span class="sxs-lookup"><span data-stu-id="2f2de-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="2f2de-136">Valitse **resurssien hallinta** > **Kausittainen** > **resurssit** > **Odottavien resurssien määrä**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="2f2de-137">Suorita työ valitsemalla **OK**ja luettelo päivittyy kohdassa **Odottavat resurssit**.</span><span class="sxs-lookup"><span data-stu-id="2f2de-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="2f2de-138">Voit määrittää tämän työn suoritettavaksi erätyönä, esimerkiksi kerran päivässä.</span><span class="sxs-lookup"><span data-stu-id="2f2de-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="2f2de-139">**Varoitus:** jos tietoja muutetaan ostotilauksessa *sen jälkeen*, resurssi on luotu nimikkeeseen perustuen, kyseiset muutokset eivät vaikuta resurssiin.</span><span class="sxs-lookup"><span data-stu-id="2f2de-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
