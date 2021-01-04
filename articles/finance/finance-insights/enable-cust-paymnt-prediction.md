---
title: Asiakkaan maksuennusteiden käyttöönotto (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten Asiakkaan maksuennusteet -toiminto otetaan käyttöön ja määritetään Finance Insightsissa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644990"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="93c0a-103">Asiakkaan maksuennusteiden käyttöönotto (esiversio)</span><span class="sxs-lookup"><span data-stu-id="93c0a-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="93c0a-104">Tässä ohjeaiheessa kerrotaan, miten Asiakkaan maksuennusteet -toiminto otetaan käyttöön ja määritetään Finance Insightsissa.</span><span class="sxs-lookup"><span data-stu-id="93c0a-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="93c0a-105">Toiminto otetaan käyttöön **Toimintojen hallinta** -työtilassa ja määritysasetukset syötetään **Financial Insights -parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="93c0a-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="93c0a-106">Tämä ohjeaihe sisältää tietoja, joiden avulla voit käyttää toimintoa tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="93c0a-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="93c0a-107">Ennen kuin suoritat seuraavat vaiheet, varmista, että olet suorittanut ennalta suoritettavat vaiheet [Määritykset Finance Insightsia varten](configure-for-fin-insites.md) -ohjeaiheesta.</span><span class="sxs-lookup"><span data-stu-id="93c0a-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="93c0a-108">Muodosta yhteys ympäristön Azure SQL:n ensisijaiseen esiintymään Microsoft Dynamics Lifecycle Services (LCS) -ratkaisun ympäristösivun tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="93c0a-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="93c0a-109">Suorita seuraava Transact-SQL (T-SQL) -komento, jos haluat ottaa käyttöön eristysympäristön väliversiotestaukset.</span><span class="sxs-lookup"><span data-stu-id="93c0a-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="93c0a-110">(Sinun on ehkä otettava käyttöön IP-osoitteen käyttö LCS:ssä ennen etäyhteyden muodostamista Application Object Serveriin \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="93c0a-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="93c0a-111">Jos Microsoft Dynamics 365 Finance -käyttöönotto on Service Fabric -käyttöönotto, voit ohittaa tämän vaiheen.</span><span class="sxs-lookup"><span data-stu-id="93c0a-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="93c0a-112">Finance Insightsin ryhmä on todennäköisesti jo ottanyt sen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="93c0a-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="93c0a-113">Jos et näe ominaisuutta **Toimintojen hallinta** -työtilassa tai jos sen käyttöönotossa on ongelmia, ota yhteyttä käyttämällä osoitetta <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="93c0a-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="93c0a-114">Ota käyttöön Asiakasmaksun tiedot -toiminto:</span><span class="sxs-lookup"><span data-stu-id="93c0a-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="93c0a-115">Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="93c0a-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="93c0a-116">Etsi toiminto, jonka nimi on **Asiakasmaksujen tiedot (esiversio)**.</span><span class="sxs-lookup"><span data-stu-id="93c0a-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="93c0a-117">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="93c0a-117">Select **Enable now**.</span></span>

    <span data-ttu-id="93c0a-118">Asiakasmaksujen tiedot -toiminto on nyt käytössä ja valmis määritettäväksi.</span><span class="sxs-lookup"><span data-stu-id="93c0a-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="93c0a-119">Määritä Asiakasmaksun tiedot -toiminto:</span><span class="sxs-lookup"><span data-stu-id="93c0a-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="93c0a-120">Siirry kohtaan **Luotonvalvonta \> Asetukset \> Finance Insights \> Finance Insights -parametrit**.</span><span class="sxs-lookup"><span data-stu-id="93c0a-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="93c0a-121">[![Financial Insights -parametrit -sivu ennen toiminnon määrittämistä](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="93c0a-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="93c0a-122">Valitse **Financial Insights -parametrit** -sivun **Asiakasmaksun tiedot** -välilehdessä **Ennustemallissa käytettyjen tietokenttien tarkasteleminen** -linkki ja avaa **Ennustemallin tietokentät** -sivu.</span><span class="sxs-lookup"><span data-stu-id="93c0a-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="93c0a-123">Siellä voit tarkastella oletusluetteloa kentistä, joita käytetään asiakkaan maksuennusteiden tekoälyennustemallissa.</span><span class="sxs-lookup"><span data-stu-id="93c0a-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="93c0a-124">Jos haluat käyttää kenttien oletusluetteloa ja luoda ennustemallin, sulje **Ennustemallin tietokentät** -sivu ja määritä sitten **Financial Insights -parametrit** -sivu ja **Ota toiminto käyttöön** -vaihtoehdon arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="93c0a-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="93c0a-125">Määrtä erittäin paljon myöhässä -tapahtumakausi, jotta voit määrittää, mitä **Erittäin paljon myöhässä** -ennustesäilö tarkoittaa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="93c0a-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="93c0a-126">Järjestelmä ennustaa avoimen laskun maksun todennäköisyyden kolmen säilön avulla: **Ajoissa**, **Myöhässä** ja **Erittäin paljon myöhässä**.</span><span class="sxs-lookup"><span data-stu-id="93c0a-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="93c0a-127">**Ajoissa** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi ajoissa tai ennen tapahtuman eräpäivää.</span><span class="sxs-lookup"><span data-stu-id="93c0a-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="93c0a-128">**Myöhässä** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi tapahtuman eräpäivän jälkeen, mutta ennen Erittäin paljon myöhässä -tapahtumakautta.</span><span class="sxs-lookup"><span data-stu-id="93c0a-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="93c0a-129">**Erittäin paljon myöhässä** – Tämä säilö sisältää maksut, jotka on ennustettu maksettavaksi Erittäin paljon myöhässä -tapahtumakauden alun jälkeen.</span><span class="sxs-lookup"><span data-stu-id="93c0a-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="93c0a-130">Jos muutat Erittäin paljon myöhässä -tapahtumakautta ja valitset **Muuta myöhäistä rajaa** -arvoa asiakasmaksujen tekoälyennustemallin luomisen jälkeen, olemassa oleva ennustemalli poistetaan ja uusi luodaan.</span><span class="sxs-lookup"><span data-stu-id="93c0a-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="93c0a-131">Uusi ennustemalli siirtää tapahtumat Erittäin paljon myöhässä -kauteen määritettyjen asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="93c0a-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="93c0a-132">Kun Erittäin paljon myöhässä -tapahtumakausi on määritetty, valitse **Luo ennustemalli** ja luo ennustemalli.</span><span class="sxs-lookup"><span data-stu-id="93c0a-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="93c0a-133">**Ennustemalli**-osassa **Financial Insights -parametrit** -sivulla näkyy ennustemallin tila.</span><span class="sxs-lookup"><span data-stu-id="93c0a-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="93c0a-134">Kun ennustemallia luodaan, voit käynnistää prosessin uudelleen valitsemalla **Nollaa mallin luominen**.</span><span class="sxs-lookup"><span data-stu-id="93c0a-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="93c0a-135">Toiminto on nyt määritetty ja valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="93c0a-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="93c0a-136">Kun toiminto on otettu käyttöön ja määritetty ja ennustemalli luotu ja toiminnassa, **Ennustemalli**-osa **Financial Insights -parametrit** -sivulla näyttää mallin tarkkuuden seuraavan kuvan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="93c0a-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="93c0a-137">[![Financial Insights -parametrit -sivun ennustemallin tarkkuus](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="93c0a-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="93c0a-138">Julkaisun tiedot</span><span class="sxs-lookup"><span data-stu-id="93c0a-138">Release details</span></span>

<span data-ttu-id="93c0a-139">Finance Insightsin julkinen esiversio on saatavilla koekäyttöönotoissa Yhdysvalloissa, Euroopassa ja Yhdistyneessä kuningaskunnassa.</span><span class="sxs-lookup"><span data-stu-id="93c0a-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="93c0a-140">Microsoft lisää tukea jatkuvasti myös muilla alueilla.</span><span class="sxs-lookup"><span data-stu-id="93c0a-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="93c0a-141">Julkisen esiversion ominaisuudet voidaan ottaa käyttöön vain Taso 2 -eristysympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="93c0a-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="93c0a-142">Eristysympäristössä luotuja määrityksiä ja tekoälymalleja ei voi siirtää tuotantoympäristöön.</span><span class="sxs-lookup"><span data-stu-id="93c0a-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="93c0a-143">Lisätietoja on kohdassa [Microsoft Dynamics 365 -esiversioiden lisäkäyttöehdot](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="93c0a-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="93c0a-144">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="93c0a-144">Privacy notice</span></span>

<span data-ttu-id="93c0a-145">Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.</span><span class="sxs-lookup"><span data-stu-id="93c0a-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
