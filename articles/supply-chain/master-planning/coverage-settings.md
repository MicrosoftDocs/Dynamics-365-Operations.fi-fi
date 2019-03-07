---
title: Kattavuusasetukset
description: Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa.
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
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "322556"
---
# <a name="coverage-settings"></a><span data-ttu-id="0c0a0-103">Kattavuusasetukset</span><span class="sxs-lookup"><span data-stu-id="0c0a0-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c0a0-104">Pääajoituksessa käytetään kattavuusasetuksia nimiketarpeiden laskemisessa.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="0c0a0-105">Voit määrittää kattavuusasetukset useilla eri tavoilla:</span><span class="sxs-lookup"><span data-stu-id="0c0a0-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="0c0a0-106">Määritä kattavuusryhmän kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="0c0a0-107">Voit luoda kattavuusryhmän, joka sisältää kaikkien kattavuusryhmään linkitettyjen tuotteiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="0c0a0-108">Luo kattavuusryhmä valitsemalla **Pääsuunnittelu &gt; Asetukset &gt; Kattavuus &gt; Kattavuusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="0c0a0-109">Voit linkittää kattavuusryhmän tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="0c0a0-110">Jos linkki koskee tiettyä toimipaikkaa, varastoa tai tuotedimensiota, käytä **Nimikkeen kattavuus** -sivun **Kattavuusryhmä**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="0c0a0-111">Jos linkki on yleinen tuotedimensioista riippumatta, käytä **Tuotteen tiedot** -sivulla **Suunnitelma**-pikavälilehdessä olevaa **Kattavuusryhmä**-kenttää.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="0c0a0-112">Jos tuotteeseen ei linkitetä kattavuusryhmää, pääsuunnittelu käyttää oletusarvoisesti **Pääsuunnittelun parametrit** -sivulla määritettyä **yleistä kattavuusryhmää**.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="0c0a0-113">Määritä tuotteen kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="0c0a0-114">Voit luoda tietyn tuotteen kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="0c0a0-115">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="0c0a0-116">Valitse tuote ja napsauta **toimintoruudussa** **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="0c0a0-117">Jos tuote on jo linkitetty kattavuusryhmään, voit ohittaa kattavuusryhmän asetukset **Ohita**-kentän avulla.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="0c0a0-118">**Nimikkeen kattavuus** -sivun kattavuusasetukset ovat ensisijaisia **Kattavuusryhmä**-sivun asetuksiin nähden.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="0c0a0-119">Määritä tuotteen kattavuusasetukset ohjatulla toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="0c0a0-120">Ohjattu toiminto auttaa määrittämään vaiheittain ensisijaisen nimikkeen kattavuusparametrit.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="0c0a0-121">Avaa **Ohjattu nimikekattavuustoiminto** napsauttamalla **Nimikkeen kattavuus** -sivulla **Ohjattu toiminto**.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="0c0a0-122">Määritä dimensioryhmän kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="0c0a0-123">Valitse **Tuotetietojen hallinta &gt; Yleinen &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="0c0a0-124">Napsauta **Vapautetun tuotteen tiedot** -sivulla **Yleiset**-välilehden **Hallinta**-ryhmässä **Varastodimensioryhmä**-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-124">On the **Released product detail** page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="0c0a0-125">Valitse **Varastodimensioryhmä** -sivulta **Kattavuussuunnitelma dimension mukaan** -kenttä, jotta voit luoda varastodimensioryhmän dimensiolle kattavuusasetukset.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="0c0a0-126">**Kattavuussuunnitelma dimension mukaan** -kentän on oltava valittuna kaikissa tuotedimensioissa, kuten konfiguraatiossa, värissä, koossa ja tyylissä.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="additional-resources"></a><span data-ttu-id="0c0a0-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0c0a0-127">Additional resources</span></span>
--------

[<span data-ttu-id="0c0a0-128">Pääsuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="0c0a0-128">Master plans</span></span>](master-plans.md)



