---
title: Kustannuslaskenta-analyysin Power BI -sisällön suojauksen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan. Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d371d35352348b1cfe1dd2a5ba25e1b2b20d7d71
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769898"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="1d83a-104">Kustannuslaskenta-analyysin Power BI -sisällön suojauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1d83a-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d83a-105">Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan.</span><span class="sxs-lookup"><span data-stu-id="1d83a-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="1d83a-106">Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="1d83a-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="1d83a-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="1d83a-107">Overview</span></span>

<span data-ttu-id="1d83a-108">**Kustannuslaskennan analyysin** Microsoft Power BI -sisältö rajoittaa käyttäjien käyttöoikeuksia Power BI:n rivitason tietoturvan avulla.</span><span class="sxs-lookup"><span data-stu-id="1d83a-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="1d83a-109">Suojaus perustuu käyttöoikeustason organisaatiohierarkiaan, joka on määritetty Kustannuslaskennan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="1d83a-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="1d83a-110">Lisätietoja **kustannuslaskennan analyysin** Power BI -sisällöstä on kohdassa [Kustannuslaskennan analyysin Power BI -sisältö](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="1d83a-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="1d83a-111">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="1d83a-111">Setup</span></span>
<span data-ttu-id="1d83a-112">Power BI -sisällön omistajan on tehtävä seuraavat toimet täyttääkseen käyttöoikeustason tietoturvan Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="1d83a-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="1d83a-113">Käyttäjä, joka julkaisee **kustannuslaskennan analyysin** Power BI -sisällön on automaattisesti omistaja.</span><span class="sxs-lookup"><span data-stu-id="1d83a-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="1d83a-114">Vain omistaja voi määrittää Power BI:n tietoturvan.</span><span class="sxs-lookup"><span data-stu-id="1d83a-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="1d83a-115">Ennen kuin omistaja lisää käyttäjiä PowerBI.com-sivustossa, vain omistaja voi nähdä **kustannuslaskennan analyysin** Power BI -sisällön tiedot.</span><span class="sxs-lookup"><span data-stu-id="1d83a-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="1d83a-116">Julkaise määritystiedosto Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="1d83a-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="1d83a-117">Kirjaudu PowerBI.com -sivustoon.</span><span class="sxs-lookup"><span data-stu-id="1d83a-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="1d83a-118">Paikanna **kustannuslaskennan analyysin** Power BI -sisällön tietojoukko.</span><span class="sxs-lookup"><span data-stu-id="1d83a-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="1d83a-119">Avaa Suojaus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1d83a-119">Open the security page.</span></span>

    ![Suojaus-välilehden avaaminen](./media/CA-picture-1.png)

5. <span data-ttu-id="1d83a-121">**Kustannusobjektin vastuuhenkilö** -rooli on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="1d83a-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="1d83a-122">Lisätä muut kustannuslaskennan käyttöoikeustason organisaatiohierarkian jäsenet.</span><span class="sxs-lookup"><span data-stu-id="1d83a-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Jäsenten lisääminen](./media/CA-picture-2.png)

<span data-ttu-id="1d83a-124">Käyttäjät, joille lisätään **Kustannusobjektin vastuuhenkilö** -rooli näkevät vain ne tiedot, joihin heillä on käyttöoikeus sen mukaan, miten kustannuslaskennan käyttöoikeustason organisaatiohierarkia on määritetty.</span><span class="sxs-lookup"><span data-stu-id="1d83a-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="1d83a-125">Rivitason suojaus koskee ruutuja ja raportteja, jotka on upotettu Power BI:stä.</span><span class="sxs-lookup"><span data-stu-id="1d83a-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="1d83a-126">Suojauksen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="1d83a-126">Updating security</span></span>
<span data-ttu-id="1d83a-127">Jos kustannuslaskennan käyttöoikeustason suojaukseen tehdään päivityksiä ja haluat, että Power BI käyttää näitä päivityksiä, sinun on päivitettävä **kustannuslaskennan analyysin** Power BI -sisällön yksikkösäilö.</span><span class="sxs-lookup"><span data-stu-id="1d83a-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="1d83a-128">Kun yksikkösäilön päivitys on valmis, sinun täytyy päivittää PowerBI.com-sivuston tiedot.</span><span class="sxs-lookup"><span data-stu-id="1d83a-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="1d83a-129">Lisätietoja yksikkösäilön päivittämisestä on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="1d83a-129">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="1d83a-130">**Kustannuslaskennan analyysin** Power BI -sisällön omistajan on suoritettava yksikkösäilön päivitys myös, jos uusille käyttäjille annetaan käyttöoikeus organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="1d83a-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="1d83a-131">Omistajan on lisäksi lisättävä uusille käyttäjille **Kustannusobjektini vastuuhenkilö** -rooli PowerBI.com-sivustossa, jotta rivitason tietoturva koskee heitä.</span><span class="sxs-lookup"><span data-stu-id="1d83a-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="1d83a-132">Suojauksen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="1d83a-132">Disabling security</span></span>
<span data-ttu-id="1d83a-133">Oletetaan, että organisaatiosi haluaa rajoittaa tietojen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="1d83a-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="1d83a-134">Jos jostain syystä suojausparametrit on poistettu käytöstä, kun suoritat kustannuslaskennan, omistajan on lisättävä käyttäjille Power BI:ssä **Kustannuslaskija**-rooli.</span><span class="sxs-lookup"><span data-stu-id="1d83a-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="1d83a-135">Jos muutat suojauksen Käytössä-tilasta käytöstä poistetuksi, käyttäjien poistaminen **Kustannusobjektin vastuuhenkilö** -roolista voi olla tarpeen.</span><span class="sxs-lookup"><span data-stu-id="1d83a-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="1d83a-136">Ja päinvastoin, jos otat suojauksen uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1d83a-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="1d83a-137">Käyttäjät voivat kuulua molempiin rooleihin.</span><span class="sxs-lookup"><span data-stu-id="1d83a-137">Users can belong to both roles.</span></span> <span data-ttu-id="1d83a-138">Yhteinen käyttö on molempien roolien liitto.</span><span class="sxs-lookup"><span data-stu-id="1d83a-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="1d83a-139">Kun kyseessä on **kustannuslaskennan analyysin** Power BI -sisältö, käyttäjillä, joilla on yhteinen käyttöoikeus, on rajoittamaton käyttöoikeus tietoihin.</span><span class="sxs-lookup"><span data-stu-id="1d83a-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="1d83a-140">Jos tavoitteesi on rajoittaa käyttöoikeuksia, käyttäjät on määritettävä ainoastaan **Kustannusobjektin vastuuhenkilö** -rooliin.</span><span class="sxs-lookup"><span data-stu-id="1d83a-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="1d83a-141">Nämä rivitason suojauspäivitykset tulevat voimaan heti.</span><span class="sxs-lookup"><span data-stu-id="1d83a-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="1d83a-142">Käyttäjien, joita muutokset koskevat, tulisi päivittää selaimen sisältö.</span><span class="sxs-lookup"><span data-stu-id="1d83a-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d83a-143">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1d83a-143">Additional resources</span></span>
<span data-ttu-id="1d83a-144">Lisätietoja Power BI:n rivitason suojauksesta on kohdassa [Mallin tietoturvan hallinta Power BI:ssä](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="1d83a-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
