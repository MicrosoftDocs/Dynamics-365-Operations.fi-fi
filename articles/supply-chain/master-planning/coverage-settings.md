---
title: Kattavuusasetukset
description: Tässä ohjeaiheessa on tietoja kattavuusasetuksista, joita pääajoitus käyttää nimiketarpeiden laskennassa.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538891"
---
# <a name="coverage-settings"></a><span data-ttu-id="dde55-103">Kattavuusasetukset</span><span class="sxs-lookup"><span data-stu-id="dde55-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dde55-104">Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="dde55-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="dde55-105">Voit määrittää kattavuusasetukset useilla eri tavoilla:</span><span class="sxs-lookup"><span data-stu-id="dde55-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="dde55-106">Määritä kattavuusryhmän kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="dde55-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="dde55-107">Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="dde55-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="dde55-108">Luodaksesi kattavuusryhmän, valitse **Pääsuunnittelu &gt; Asetukset &gt; Kattavuus &gt; Kattavuusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="dde55-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="dde55-109">Voit linkittää kattavuusryhmän tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="dde55-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="dde55-110">Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="dde55-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="dde55-111">Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehden **Kattavuusryhmä**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="dde55-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="dde55-112">Oletusarvoisesti, jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä yleistä kattavuusryhmää.</span><span class="sxs-lookup"><span data-stu-id="dde55-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="dde55-113">Määritä tuotteen kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="dde55-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="dde55-114">Voit luoda tietyn tuotteen kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="dde55-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="dde55-115">Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="dde55-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="dde55-116">Valitse tuote ja napsauta toimintoruudussa **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu.</span><span class="sxs-lookup"><span data-stu-id="dde55-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="dde55-117">Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="dde55-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="dde55-118">**Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.</span><span class="sxs-lookup"><span data-stu-id="dde55-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="dde55-119">Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="dde55-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="dde55-120">Ohjattu toiminto opastaa vaiheittain ensisijaisen nimikkeen kattavuusparametrien määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="dde55-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="dde55-121">Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla toimintoruudusta **Ohjattu toiminto**.</span><span class="sxs-lookup"><span data-stu-id="dde55-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="dde55-122">Määritä dimensioryhmän kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="dde55-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="dde55-123">Mene **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="dde55-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="dde55-124">Napsauta **Vapautetun tuotteen tiedot** -sivulla **Yleiset**-pikavälilehden **Hallinta**-osassa **Varastodimensioryhmä**-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="dde55-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="dde55-125">Valitse **Varastodimensioryhmät** -sivulta **Kattavuussuunnitelma dimension mukaan** -valintaruutu, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="dde55-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="dde55-126">**Kattavuussuunnitelma dimension mukaan** -kentän on oltava valittuna kaikissa tuotedimensioissa, kuten konfiguraatiossa, värissä, koossa ja tyylissä.</span><span class="sxs-lookup"><span data-stu-id="dde55-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dde55-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="dde55-127">Additional resources</span></span>

[<span data-ttu-id="dde55-128">Pääsuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="dde55-128">Master plans</span></span>](master-plans.md)
