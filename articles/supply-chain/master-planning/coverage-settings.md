---
title: Kattavuusasetukset
description: Tässä ohjeaiheessa on tietoja kattavuusasetuksista, joita pääajoitus käyttää nimiketarpeiden laskennassa.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1134f734f1025151a56b2a72266a6baa5763ba4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427319"
---
# <a name="coverage-settings"></a><span data-ttu-id="77aa2-103">Kattavuusasetukset</span><span class="sxs-lookup"><span data-stu-id="77aa2-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77aa2-104">Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="77aa2-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="77aa2-105">Voit määrittää kattavuusasetukset useilla eri tavoilla:</span><span class="sxs-lookup"><span data-stu-id="77aa2-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="77aa2-106">Määritä kattavuusryhmän kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="77aa2-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="77aa2-107">Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="77aa2-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="77aa2-108">Luodaksesi kattavuusryhmän, valitse **Pääsuunnittelu &gt; Asetukset &gt; Kattavuus &gt; Kattavuusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="77aa2-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="77aa2-109">Voit linkittää kattavuusryhmän tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="77aa2-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="77aa2-110">Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="77aa2-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="77aa2-111">Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehden **Kattavuusryhmä**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="77aa2-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="77aa2-112">Oletusarvoisesti, jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä yleistä kattavuusryhmää.</span><span class="sxs-lookup"><span data-stu-id="77aa2-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="77aa2-113">Määritä tuotteen kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="77aa2-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="77aa2-114">Voit luoda tietyn tuotteen kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="77aa2-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="77aa2-115">Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="77aa2-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="77aa2-116">Valitse tuote ja napsauta toimintoruudussa **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu.</span><span class="sxs-lookup"><span data-stu-id="77aa2-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="77aa2-117">Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="77aa2-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="77aa2-118">**Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.</span><span class="sxs-lookup"><span data-stu-id="77aa2-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="77aa2-119">Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="77aa2-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="77aa2-120">Ohjattu toiminto opastaa vaiheittain ensisijaisen nimikkeen kattavuusparametrien määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="77aa2-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="77aa2-121">Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla toimintoruudusta **Ohjattu toiminto**.</span><span class="sxs-lookup"><span data-stu-id="77aa2-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="77aa2-122">Määritä dimensioryhmän kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="77aa2-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="77aa2-123">Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="77aa2-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="77aa2-124">Napsauta **Vapautetun tuotteen tiedot** -sivulla **Yleiset**-pikavälilehden **Hallinta**-osassa **Varastodimensioryhmä**-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="77aa2-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="77aa2-125">Valitse **Varastodimensioryhmät** -sivulta **Kattavuussuunnitelma dimension mukaan** -valintaruutu, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="77aa2-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="77aa2-126">**Kattavuussuunnitelma dimension mukaan** -kentän on oltava valittuna kaikissa tuotedimensioissa, kuten konfiguraatiossa, värissä, koossa ja tyylissä.</span><span class="sxs-lookup"><span data-stu-id="77aa2-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="77aa2-127">Kattavuuskoodit</span><span class="sxs-lookup"><span data-stu-id="77aa2-127">Coverage codes</span></span>

<span data-ttu-id="77aa2-128">Pääsuunnittelu voidaan määrittää käyttämään erilaisia täydennysmenetelmiä.</span><span class="sxs-lookup"><span data-stu-id="77aa2-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="77aa2-129">Täydennysmenetelmät tai eräkoon muuttamismenetelmät ovat tekniikoita, joiden avulla järjestelmä voi määrittää ostettujen tai tuotettujen nimikkeiden eräkoon.</span><span class="sxs-lookup"><span data-stu-id="77aa2-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="77aa2-130">Kullekin täydennysmenetelmälle määritetään jokin seuraavista kattavuuskoodeista:</span><span class="sxs-lookup"><span data-stu-id="77aa2-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="77aa2-131">**Manuaalinen** – Eräkoon muuttamismenetelmä, jossa järjestelmä ei ehdota nimikkeelle osto-, siirto- tai tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="77aa2-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="77aa2-132">Nimikkeen suunnittelija vastaa nimikkeen täydentämiseen tarvittavien tilausten luomisesta.</span><span class="sxs-lookup"><span data-stu-id="77aa2-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="77aa2-133">**Tarpeen mukaan** – Eräkoon muuttamismenetelmä, jossa järjestelmä nimikkeelle tarpeen mukaan suunnitellun osto-, siirto- tai tuotantotilauksen.</span><span class="sxs-lookup"><span data-stu-id="77aa2-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="77aa2-134">Tätä menetelmää käytetään yleensä kalliille nimikkeille, joilla on ajoittaista kysyntää.</span><span class="sxs-lookup"><span data-stu-id="77aa2-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="77aa2-135">**Kausikohtainen** – Eräkoon muuttamismenetelmä, joka yhdistää kausikohtaisen kysynnän nimikkeen yhteen tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="77aa2-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="77aa2-136">Tilaus suunnitellaan kauden ensimmäiselle päivälle, ja sen määrä täyttää määritetyn kauden nettotarpeet.</span><span class="sxs-lookup"><span data-stu-id="77aa2-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="77aa2-137">Kausi alkaa nimikkeen ensimmäisestä kysynnästä ja kattaa määritetyn ajanjakson.</span><span class="sxs-lookup"><span data-stu-id="77aa2-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="77aa2-138">Seuraava kausi alkaa nimikkeen seuraavista tarpeista.</span><span class="sxs-lookup"><span data-stu-id="77aa2-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="77aa2-139">**Min./Maks.** – Eräkoon muuttamismenetelmä, joka sisältää varaston täydennyksen tietylle tasolle, kun ennustettu käytettävissä oleva määrä alittaa raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="77aa2-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="77aa2-140">Täydennysmäärä on enimmäistason ja ennustetun käytettävissä olevan tason välinen erotus.</span><span class="sxs-lookup"><span data-stu-id="77aa2-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="77aa2-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="77aa2-141">Additional resources</span></span>

[<span data-ttu-id="77aa2-142">Pääsuunnitelmien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="77aa2-142">Master plans overview</span></span>](master-plans.md)
