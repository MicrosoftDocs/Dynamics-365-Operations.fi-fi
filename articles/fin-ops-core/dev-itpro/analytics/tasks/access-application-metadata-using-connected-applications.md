---
title: Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla
description: Tämän aiheen vaiheissa selitetään, miten Regulatory Configuration Service (RCS) -käyttäjät voivat suunnitella uuden sähköisen raportoinnin eli ER-mallin yhdistämisen käyttämällä Finance and Operationsin metatietoja.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 751ac21dc056373e1cd89a5149bf38789134e0cc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682138"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="2a09d-103">Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla</span><span class="sxs-lookup"><span data-stu-id="2a09d-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a09d-104">Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava Regulatory Configuration Service (RCS) -käyttäjä voi suunnitella uuden sähköisen raportoinnin ER-mallin yhdistämisen Finance and Operationsin metatietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="2a09d-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="2a09d-105">Sovelluksen metatietoja käytetään verkossa RCS:n yhdistetyllä sovelluksella.</span><span class="sxs-lookup"><span data-stu-id="2a09d-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="2a09d-106">ER-näytemallin yhdistäminen määritetään käyttämään ulkomaankauppatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="2a09d-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="2a09d-107">Näitä vaiheita varten on ensin suoritettava RCS:ssä ohjeaiheessa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2a09d-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="2a09d-108">Jos olet suorittanut aiheen [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](access-application-metadata-er-configuration.md) vaiheet, siirry [Esimerkki sähköisestä raportoinnista -sivulle](https://go.microsoft.com/fwlink/?linkid=862266) ja tallenna seuraavat ER-konfiguraatiot: Ulkomaankaupan metatiedot.xml, Ulkomaankauppamalli.xml ja Ulkomaankaupan yhdistäminen.xml ja suorita sitten toimenpiteen vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2a09d-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2a09d-109">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="2a09d-109">Prerequisites</span></span>
1. <span data-ttu-id="2a09d-110">Valitse **Kaikki työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="2a09d-111">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="2a09d-112">Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2a09d-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="2a09d-113">Tarvittavien ER-konfiguraatioiden hankkiminen</span><span class="sxs-lookup"><span data-stu-id="2a09d-113">Get required ER configurations</span></span>
1. <span data-ttu-id="2a09d-114">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="2a09d-115">Jos olet jo suorittanut toimenpiteen [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](access-application-metadata-er-configuration.md) vaiheet, sinulla on jo tarvittavat nykyisen RCS-esiintymän ER-määritykset (ulkomaankaupan metatietojen, mallin ja yhdistämisen määritykset).</span><span class="sxs-lookup"><span data-stu-id="2a09d-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="2a09d-116">Voit ohittaa tämän alitehtävän kaikki jäljellä olevat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2a09d-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="2a09d-117">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="2a09d-118">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="2a09d-119">Valitse ensin **Selaa** ja sitten **Ulkomaankaupan metatiedot.xml** -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="2a09d-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="2a09d-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-120">Click **OK**.</span></span> 
7. <span data-ttu-id="2a09d-121">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="2a09d-122">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="2a09d-123">Valitse ensin **Selaa** ja sitten **Ulkomaankauppamalli.xml**-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="2a09d-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="2a09d-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-124">Click **OK**.</span></span> 
11. <span data-ttu-id="2a09d-125">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="2a09d-126">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="2a09d-127">Valitse ensin **Selaa** ja sitten **Ulkomaankaupan yhdistäminen.xml** -tiedosto.</span><span class="sxs-lookup"><span data-stu-id="2a09d-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="2a09d-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="2a09d-129">Yhdistetyn sovelluksen rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="2a09d-129">Register a connected application</span></span>
1. <span data-ttu-id="2a09d-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09d-130">Close the page.</span></span> 
2. <span data-ttu-id="2a09d-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09d-131">Close the page.</span></span> 
3. <span data-ttu-id="2a09d-132">Valitse **Kaikki työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="2a09d-133">Valitse **Yhdistetyt sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="2a09d-134">Varmista, että määritetty sovellus on Azure-pohjainen ja että nykyinen RCS-käyttäjä voi käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="2a09d-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="2a09d-135">Nykyisellä RCS-käyttäjällä on lisäksi oltava valitun sovelluksen käyttöoikeus ja hänen on oltava rekisteröitynyt sovelluksen käyttäjäksi roolilla, jolla voi käyttää sovelluksen metatietoja.</span><span class="sxs-lookup"><span data-stu-id="2a09d-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="2a09d-136">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-136">Click **New**.</span></span> 
7. <span data-ttu-id="2a09d-137">Kirjoita **Nimi**-kenttään MyConnectedApp.</span><span class="sxs-lookup"><span data-stu-id="2a09d-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="2a09d-138">Kirjoita **Sovellus**-kenttään https:// mycompany.operations.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="2a09d-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="2a09d-139">Kirjoita **Vuokraaja**-kenttään mycompany.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="2a09d-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="2a09d-140">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-140">Click **Save**.</span></span> 
11. <span data-ttu-id="2a09d-141">Voit tarkistaa yhteyden määritettyyn sovellukseen valitsemalla **Yhdistä etäsovellukseen** -sivulla **Muodosta yhteys etäsovellukseen napsauttamalla tätä** -linkki.</span><span class="sxs-lookup"><span data-stu-id="2a09d-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="2a09d-142">Valitse **Tarkista yhteys**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="2a09d-143">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-143">Click **Close**.</span></span> 
14. <span data-ttu-id="2a09d-144">Kun yhteyden tarkistus onnistuu, nykyisen ruudukon määritetyn sovelluksen version ja vuokraajan tiedot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="2a09d-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="2a09d-145">Aiemmin määritetyn mallin yhdistämismäärityksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="2a09d-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="2a09d-146">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09d-146">Close the page.</span></span> 
2. <span data-ttu-id="2a09d-147">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="2a09d-148">Laajenna puussa **Ulkomaankauppamalli**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="2a09d-149">Valitse puussa **Ulkomaankauppamalli\Ulkomaankaupan yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="2a09d-150">Laajenna **Edellytykset**-osa.</span><span class="sxs-lookup"><span data-stu-id="2a09d-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a09d-151">Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen.</span><span class="sxs-lookup"><span data-stu-id="2a09d-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="2a09d-152">Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="2a09d-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="2a09d-153">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="2a09d-154">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="2a09d-155">Valitse puussa **Dynamics 365 for Operations\Taulukon tietueet**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="2a09d-156">Valitse **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="2a09d-157">Anna tai valitse **Taulu**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="2a09d-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a09d-158">Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen.</span><span class="sxs-lookup"><span data-stu-id="2a09d-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="2a09d-159">Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="2a09d-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="2a09d-160">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="2a09d-161">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09d-161">Close the page.</span></span> 
13. <span data-ttu-id="2a09d-162">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09d-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="2a09d-163">Yhdistetyn sovelluksen määrittäminen mallin yhdistämiseen</span><span class="sxs-lookup"><span data-stu-id="2a09d-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="2a09d-164">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="2a09d-165">Valitse **MyConnectedApp**-sovellus.</span><span class="sxs-lookup"><span data-stu-id="2a09d-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a09d-166">Tällä hetkellä yhdistämismääritys viittaa valitun yhdistetyn sovelluksen metatietoihin.</span><span class="sxs-lookup"><span data-stu-id="2a09d-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="2a09d-167">Kun sama yhdistämismääritys viittaa samanaikaisesti metatietojen määritykseen ja yhdistettyyn sovellukseen, yhdistetyn sovelluksen metatietoja käytetään.</span><span class="sxs-lookup"><span data-stu-id="2a09d-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="2a09d-168">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="2a09d-169">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="2a09d-170">Valitse puussa **Dynamics 365 for Operations\Taulukon tietueet**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="2a09d-171">Valitse **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="2a09d-172">Anna tai valitse **Taulu**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="2a09d-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a09d-173">Valittavana on nyt enemmän kuin kaksi sovellustaulukkoa, sillä tämä yhdistämismääritys käyttää siihen määritetyn yhdistetyn sovelluksen kaikkia metatietoja.</span><span class="sxs-lookup"><span data-stu-id="2a09d-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="2a09d-174">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="2a09d-175">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="2a09d-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a09d-176">Tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä tähän yhdistämismääritykseen määritetyn yhdistetyn sovelluksen metatietoja.</span><span class="sxs-lookup"><span data-stu-id="2a09d-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="2a09d-177">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09d-177">Close the page.</span></span> 
11. <span data-ttu-id="2a09d-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2a09d-178">Close the page.</span></span> 

<span data-ttu-id="2a09d-179">Kun tämä malli on arvioitava käyttämällä toisen version sovelluksen metatietoja, rekisteröi toinen yhdistetty sovellus, määritä se tähän mallin yhdistämismääritykseen ja vahvista se käyttämällä uusia metatietoja.</span><span class="sxs-lookup"><span data-stu-id="2a09d-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
