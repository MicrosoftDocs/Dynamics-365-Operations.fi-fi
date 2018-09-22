---
title: "Kustannuslaskennan Power BI -sisällön suojauksen määrittäminen"
description: "Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan. Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: d1cd378a58d4a4fe4388238f97e84a8e2b07937b
ms.contentlocale: fi-fi
ms.lasthandoff: 08/13/2018

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="63b79-104">Kustannuslaskennan Power BI -sisällön suojauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="63b79-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63b79-105">Tässä ohjeaiheessa kerrotaan, miten Kustannuslaskennan käyttöoikeustason tietoturva täytetään Microsoft Power BI:n rivitason tietoturvaan.</span><span class="sxs-lookup"><span data-stu-id="63b79-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="63b79-106">Tämä toiminto takaa, että käyttäjät näkevät vain Power BI -tietoja, joihin heillä on käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="63b79-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="63b79-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="63b79-107">Overview</span></span>

<span data-ttu-id="63b79-108">Microsoft Power BI:n **Kustannuslaskennan analyysi** -sisältö rajoittaa käyttäjien käyttöoikeuksia Power BI:n rivitason tietoturvan avulla.</span><span class="sxs-lookup"><span data-stu-id="63b79-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="63b79-109">Suojaus perustuu käyttöoikeustason organisaatiohierarkiaan, joka on määritetty Kustannuslaskennan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="63b79-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="63b79-110">Lisätietoja Power BI:n **kustannuslaskennan analyysi** -sisällöstä löydät kohdasta [Power BI:n kustannuslaskennan analyysi -sisältö](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="63b79-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="63b79-111">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="63b79-111">Setup</span></span>
<span data-ttu-id="63b79-112">Power BI -sisällön omistajan on tehtävä seuraavat toimet täyttääkseen käyttöoikeustason tietoturva Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="63b79-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="63b79-113">Käyttäjä, joka julkaisee **kustannuslaskennan analyysin** Power BI -sisällön on automaattisesti omistaja.</span><span class="sxs-lookup"><span data-stu-id="63b79-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="63b79-114">Vain omistaja voi Power BI:n tietoturvan.</span><span class="sxs-lookup"><span data-stu-id="63b79-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="63b79-115">Lisäksi, kunnes omistaja lisää käyttäjiä PowerBI.com-sivustossa, vain omistaja voi nähdä Power BI:n **kustannuslaskennan analyysi** -sisällön tiedot.</span><span class="sxs-lookup"><span data-stu-id="63b79-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="63b79-116">Julkaise määritystiedoston Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="63b79-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="63b79-117">Kirjaudu PowerBI.com -sivustoon.</span><span class="sxs-lookup"><span data-stu-id="63b79-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="63b79-118">Paikanna **Kustannuslaskennan analyysin** Power BI -sisällön tietojoukko.</span><span class="sxs-lookup"><span data-stu-id="63b79-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="63b79-119">Avaa Suojaus-välilehti.</span><span class="sxs-lookup"><span data-stu-id="63b79-119">Open the security page.</span></span>

    ![Suojaus-välilehden avaaminen](./media/CA-picture-1.png)

5. <span data-ttu-id="63b79-121">**Kustannusobjektin vastuuhenkilö** -rooli on jo luotu.</span><span class="sxs-lookup"><span data-stu-id="63b79-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="63b79-122">Lisätä muut kustannuslaskennan käyttöoikeustason organisaatiohierarkian jäsenet.</span><span class="sxs-lookup"><span data-stu-id="63b79-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Jäsenten lisääminen](./media/CA-picture-2.png)

<span data-ttu-id="63b79-124">Käyttäjät, joille lisätään **Kustannusobjektin vastuuhenkilö** -rooli näkevät vain ne tiedot, joihin heillä on käyttöoikeus sen mukaan, miten kustannuslaskennan käyttöoikeustason organisaatiohierarkia on määritetty.</span><span class="sxs-lookup"><span data-stu-id="63b79-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="63b79-125">Rivitason suojaus koskee ruutuja ja raportteja, jotka on upotettu Microsoft Dynamics 365 for Finance and Operationsiin Power BI:stä.</span><span class="sxs-lookup"><span data-stu-id="63b79-125">Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="63b79-126">Suojauksen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="63b79-126">Updating security</span></span>
<span data-ttu-id="63b79-127">Jos kustannuslaskennan käyttöoikeustason suojaukseen tehdään päivityksiä ja haluat, että Power BI käyttää näitä päivityksiä, sinun on päivitettävä **kustannuslaskennan analyysin** Power BI -sisällön yksikkösäilö.</span><span class="sxs-lookup"><span data-stu-id="63b79-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="63b79-128">Kun Finance and Operationsin yksikkösäilön päivitys on valmis, päivitä PowerBI.com-sivuston tiedot.</span><span class="sxs-lookup"><span data-stu-id="63b79-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="63b79-129">Lisätietoja yksikkösäilön päivittämisestä on kohdassa [Yksikkösäilön päivittäminen](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="63b79-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="63b79-130">**Kkustannuslaskennan analyysin** Power BI -sisällön omistajan on suoritettava yksikkösäilön päivitys myös, jos uusille käyttäjille annetaan käyttöoikeus organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="63b79-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="63b79-131">Omistajan on lisäksi lisättävä uusille käyttäjille **Kustannusobjektini vastuuhenkilö** -rooli PowerBI.com-sivustossa, jotta rivitason tietoturva koskee heitä.</span><span class="sxs-lookup"><span data-stu-id="63b79-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="63b79-132">Suojauksen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="63b79-132">Disabling security</span></span>
<span data-ttu-id="63b79-133">Oletetaan, että organisaatiosi haluaa rajoittaa tietojen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="63b79-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="63b79-134">Jos jostain syystä suojausparametrit on poistettu käytöstä, kun suoritat kustannuslaskennan, omistajan on lisättävä käyttäjille Power BI:ssä **Kustannuslaskija** -rooli.</span><span class="sxs-lookup"><span data-stu-id="63b79-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="63b79-135">Jos muutat suojauksen Käytössä-tilasta käytöstä poistetuksi, käyttäjien poistaminen **Kustannusobjektin vastuuhenkilö** -roolista voi olla tarpeen.</span><span class="sxs-lookup"><span data-stu-id="63b79-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="63b79-136">Ja päinvastoin, jos otat suojauksen uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="63b79-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="63b79-137">Käyttäjät voivat kuulua molempiin rooleihin.</span><span class="sxs-lookup"><span data-stu-id="63b79-137">Users can belong to both roles.</span></span> <span data-ttu-id="63b79-138">Yhteinen käyttö on molempien roolien liitto.</span><span class="sxs-lookup"><span data-stu-id="63b79-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="63b79-139">Kun kyseessä on **kustannuslaskennan analyysin** Power BI -sisältö, käyttäjillä, joilla on yhteinen käyttöoikeus, on rajoittamaton käyttöoikeus tietoihin.</span><span class="sxs-lookup"><span data-stu-id="63b79-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="63b79-140">Jos tavoitteesi on rajoittaa käyttöoikeuksia, käyttäjät on määritettävä ainoastaan **Kustannusobjektin vastuuhenkilö** -rooliin.</span><span class="sxs-lookup"><span data-stu-id="63b79-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="63b79-141">Nämä rivitason suojauspäivitykset tulevat voimaan heti.</span><span class="sxs-lookup"><span data-stu-id="63b79-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="63b79-142">Käyttäjien, joita muutokset koskevat, tulisi päivittää selaimen sisältö.</span><span class="sxs-lookup"><span data-stu-id="63b79-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63b79-143">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="63b79-143">Additional resources</span></span>
<span data-ttu-id="63b79-144">Katso lisätietoja Power BI:n rivitason suojauksesta kohdasta [Mallin tietoturvan hallinta Power BI:ssä](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="63b79-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>

