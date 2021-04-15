---
title: Kustannuslaskenta-analyysin Power BI -sisällön suojauksen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 32093f4e47fe3d9ca691b70e15adfc3199e65beb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754261"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="a558f-103">Kustannuslaskenta-analyysin Power BI -sisällön suojauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a558f-103">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a558f-104">Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan.</span><span class="sxs-lookup"><span data-stu-id="a558f-104">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="a558f-105">Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="a558f-105">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="a558f-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="a558f-106">Overview</span></span>

<span data-ttu-id="a558f-107">**Kustannuslaskennan analyysin** Microsoft Power BI -sisältö rajoittaa käyttäjien käyttöoikeuksia Power BI:n rivitason tietoturvan avulla.</span><span class="sxs-lookup"><span data-stu-id="a558f-107">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="a558f-108">Suojaus perustuu käyttöoikeustason organisaatiohierarkiaan, joka on määritetty Kustannuslaskennan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="a558f-108">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="a558f-109">Lisätietoja **kustannuslaskennan analyysin** Power BI -sisällöstä on kohdassa [Kustannuslaskennan analyysin Power BI -sisältö](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="a558f-109">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="a558f-110">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="a558f-110">Setup</span></span>
<span data-ttu-id="a558f-111">Power BI -sisällön omistajan on tehtävä seuraavat toimet täyttääkseen käyttöoikeustason tietoturvan Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="a558f-111">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="a558f-112">Käyttäjä, joka julkaisee **kustannuslaskennan analyysin** Power BI -sisällön on automaattisesti omistaja.</span><span class="sxs-lookup"><span data-stu-id="a558f-112">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="a558f-113">Vain omistaja voi määrittää Power BI:n tietoturvan.</span><span class="sxs-lookup"><span data-stu-id="a558f-113">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="a558f-114">Ennen kuin omistaja lisää käyttäjiä PowerBI.com-sivustossa, vain omistaja voi nähdä **kustannuslaskennan analyysin** Power BI -sisällön tiedot.</span><span class="sxs-lookup"><span data-stu-id="a558f-114">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="a558f-115">Julkaise määritystiedosto Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="a558f-115">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="a558f-116">Kirjaudu PowerBI.com -sivustoon.</span><span class="sxs-lookup"><span data-stu-id="a558f-116">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="a558f-117">Paikanna **kustannuslaskennan analyysin** Power BI -sisällön tietojoukko.</span><span class="sxs-lookup"><span data-stu-id="a558f-117">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="a558f-118">Avaa Suojaus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a558f-118">Open the security page.</span></span>

    ![Suojaus-välilehden avaaminen](./media/CA-picture-1.png)

5. <span data-ttu-id="a558f-120">**Kustannusobjektin vastuuhenkilö** -rooli on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="a558f-120">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="a558f-121">Lisätä muut kustannuslaskennan käyttöoikeustason organisaatiohierarkian jäsenet.</span><span class="sxs-lookup"><span data-stu-id="a558f-121">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Jäsenten lisääminen](./media/CA-picture-2.png)

<span data-ttu-id="a558f-123">Käyttäjät, joille lisätään **Kustannusobjektin vastuuhenkilö** -rooli näkevät vain ne tiedot, joihin heillä on käyttöoikeus sen mukaan, miten kustannuslaskennan käyttöoikeustason organisaatiohierarkia on määritetty.</span><span class="sxs-lookup"><span data-stu-id="a558f-123">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="a558f-124">Rivitason suojaus koskee ruutuja ja raportteja, jotka on upotettu Power BI:stä.</span><span class="sxs-lookup"><span data-stu-id="a558f-124">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="a558f-125">Suojauksen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="a558f-125">Updating security</span></span>
<span data-ttu-id="a558f-126">Jos kustannuslaskennan käyttöoikeustason suojaukseen tehdään päivityksiä ja haluat, että Power BI käyttää näitä päivityksiä, sinun on päivitettävä **kustannuslaskennan analyysin** Power BI -sisällön yksikkösäilö.</span><span class="sxs-lookup"><span data-stu-id="a558f-126">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="a558f-127">Kun yksikkösäilön päivitys on valmis, sinun täytyy päivittää PowerBI.com-sivuston tiedot.</span><span class="sxs-lookup"><span data-stu-id="a558f-127">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="a558f-128">Lisätietoja yksikkösäilön päivittämisestä on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="a558f-128">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="a558f-129">**Kustannuslaskennan analyysin** Power BI -sisällön omistajan on suoritettava yksikkösäilön päivitys myös, jos uusille käyttäjille annetaan käyttöoikeus organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="a558f-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="a558f-130">Omistajan on lisäksi lisättävä uusille käyttäjille **Kustannusobjektini vastuuhenkilö** -rooli PowerBI.com-sivustossa, jotta rivitason tietoturva koskee heitä.</span><span class="sxs-lookup"><span data-stu-id="a558f-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="a558f-131">Suojauksen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="a558f-131">Disabling security</span></span>
<span data-ttu-id="a558f-132">Oletetaan, että organisaatiosi haluaa rajoittaa tietojen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="a558f-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="a558f-133">Jos jostain syystä suojausparametrit on poistettu käytöstä, kun suoritat kustannuslaskennan, omistajan on lisättävä käyttäjille Power BI:ssä **Kustannuslaskija**-rooli.</span><span class="sxs-lookup"><span data-stu-id="a558f-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="a558f-134">Jos muutat suojauksen Käytössä-tilasta käytöstä poistetuksi, käyttäjien poistaminen **Kustannusobjektin vastuuhenkilö** -roolista voi olla tarpeen.</span><span class="sxs-lookup"><span data-stu-id="a558f-134">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="a558f-135">Ja päinvastoin, jos otat suojauksen uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a558f-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="a558f-136">Käyttäjät voivat kuulua molempiin rooleihin.</span><span class="sxs-lookup"><span data-stu-id="a558f-136">Users can belong to both roles.</span></span> <span data-ttu-id="a558f-137">Yhteinen käyttö on molempien roolien liitto.</span><span class="sxs-lookup"><span data-stu-id="a558f-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="a558f-138">Kun kyseessä on **kustannuslaskennan analyysin** Power BI -sisältö, käyttäjillä, joilla on yhteinen käyttöoikeus, on rajoittamaton käyttöoikeus tietoihin.</span><span class="sxs-lookup"><span data-stu-id="a558f-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="a558f-139">Jos tavoitteesi on rajoittaa käyttöoikeuksia, käyttäjät on määritettävä ainoastaan **Kustannusobjektin vastuuhenkilö** -rooliin.</span><span class="sxs-lookup"><span data-stu-id="a558f-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="a558f-140">Nämä rivitason suojauspäivitykset tulevat voimaan heti.</span><span class="sxs-lookup"><span data-stu-id="a558f-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="a558f-141">Käyttäjien, joita muutokset koskevat, tulisi päivittää selaimen sisältö.</span><span class="sxs-lookup"><span data-stu-id="a558f-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a558f-142">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a558f-142">Additional resources</span></span>
<span data-ttu-id="a558f-143">Lisätietoja Power BI:n rivitason suojauksesta on kohdassa [Mallin tietoturvan hallinta Power BI:ssä](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="a558f-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]