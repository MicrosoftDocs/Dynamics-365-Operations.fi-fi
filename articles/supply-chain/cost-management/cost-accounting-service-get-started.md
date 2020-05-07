---
title: Kustannuslaskentapalvelun käytön aloittaminen
description: Tässä ohjeaiheessa on kustannuslaskentapalvelun käyttöoikeustiedot ja asennusohjeet.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276912"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="78794-103">Kustannuslaskentapalvelun käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="78794-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="78794-104">Tässä ohjeaiheessa kuvatut toiminnot ovat saatavilla käyttöön yksityisen ennakkoversion osana.</span><span class="sxs-lookup"><span data-stu-id="78794-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="78794-105">Tämän ohjeaiheen sisältö ja sen kuvaamien toimintojen muutokset saattavat muuttua.</span><span class="sxs-lookup"><span data-stu-id="78794-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="78794-106">Lisätietoja ennakkojulkaisusta on kohdassa [Yhden version palvelupäivitysten usein kysytyt kysymykset](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="78794-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="78794-107">Kustannuslaskentapalvelun avulla voit suorittaa useita varastokirjanpitoja määrittämissäsi kustannuslaskentarekistereissä.</span><span class="sxs-lookup"><span data-stu-id="78794-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="78794-108">Kukin kustannuslaskentatapahtuma liitetään *käytäntöön*.</span><span class="sxs-lookup"><span data-stu-id="78794-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="78794-109">Yleissopimus on kokoelma seuraavantyyppisiä kirjanpitokäytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="78794-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="78794-110">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="78794-110">Cost object</span></span>
- <span data-ttu-id="78794-111">Syötteen mittaperuste</span><span class="sxs-lookup"><span data-stu-id="78794-111">Input measurement basis</span></span>
- <span data-ttu-id="78794-112">Kustannusvirran oletus</span><span class="sxs-lookup"><span data-stu-id="78794-112">Cost flow assumption</span></span>
- <span data-ttu-id="78794-113">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="78794-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="78794-114">Vaikka olet ottanut kustannuslaskentapalvelun käyttöön, voit silti tehdä varastokirjanpidon Microsoft Dynamics 365 Supply Chain Management -ohjelmassa tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="78794-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="78794-115">Kustannuslaskentapalvelu on apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="78794-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="78794-116">Jos haluat käyttää sen toimintoja, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesistä (LCS).</span><span class="sxs-lookup"><span data-stu-id="78794-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="78794-117">Tämän vuoksi voit valita, että se arvioidaan testiympäristössä, ennen kuin otat sen käyttöön tuotantoympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="78794-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="78794-118">Kustannuslaskentapalvelu ei tällä hetkellä tue kaikkia Dynamics 365 Supply Chain Managementin sisäänrakennettuja kustannustenhallintatoimintoja.</span><span class="sxs-lookup"><span data-stu-id="78794-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="78794-119">Tämän vuoksi on tärkeää arvioida, vastaako tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="78794-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="78794-120">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="78794-120">Licensing</span></span>

<span data-ttu-id="78794-121">Kustannuslaskentapalvelu on lisensoitu yhdessä Supply Chain Managementin käytettävissä olevien varastokirjanpidon vakiotoimintojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="78794-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="78794-122">Sinun ei tarvitse ostaa lisäkäyttöoikeutta, jotta voisit käyttää kustannuslaskentapalvelua.</span><span class="sxs-lookup"><span data-stu-id="78794-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="78794-123">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="78794-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78794-124">Kustannuslaskentapalvelun käyttäminen edellyttää, että käytössä on LCS-yhteensopiva korkean käytettävyyden ympäristö (ei OneBox-ympäristö) ja että käytössä on Dynamics 365 Supply Chain Managementin versio 10.0.11 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="78794-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="78794-125">Jos haluat käyttää kustannuslaskentapalvelua, asenna kustannuslaskentapalvelun apuohjelma Supply Chain Managementia varten seuraavassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="78794-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="78794-126">Kirjaudu sisään LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="78794-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="78794-127">Mene kohtaan **Toimintojen hallinnan esiversio**.</span><span class="sxs-lookup"><span data-stu-id="78794-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="78794-128">Valitse plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="78794-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="78794-129">Syötä **Koodi**-kenttään kustannuslaskentapalvelun apuohjelman beeta-avain.</span><span class="sxs-lookup"><span data-stu-id="78794-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="78794-130">(Sinun olisi pitänyt vastaanottaa avaimesi sähköpostilla.)</span><span class="sxs-lookup"><span data-stu-id="78794-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="78794-131">Valitse **Poista esto**.</span><span class="sxs-lookup"><span data-stu-id="78794-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="78794-132">Avaa LCS-ympäristö, johon haluat lisätä palvelun.</span><span class="sxs-lookup"><span data-stu-id="78794-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="78794-133">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="78794-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="78794-134">Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="78794-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="78794-135">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="78794-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="78794-136">Valitse **Kustannuslaskentapalvelu**.</span><span class="sxs-lookup"><span data-stu-id="78794-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="78794-137">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="78794-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="78794-138">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="78794-138">Select **Install**.</span></span>

1. <span data-ttu-id="78794-139">**Ympäristön apuohjelmat** -pikavälilehdessä näkyy, että kustannuslaskentapalvelua asennetaan.</span><span class="sxs-lookup"><span data-stu-id="78794-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="78794-140">Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta **Asennetaan** tilaan **Asennettu**.</span><span class="sxs-lookup"><span data-stu-id="78794-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="78794-141">(Sivu on ehkä päivitettävä, jotta näet tämän muutoksen.) Tässä vaiheessa kustannuslaskentapalvelu on valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="78794-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="78794-142">Määritä integraatio</span><span class="sxs-lookup"><span data-stu-id="78794-142">Set up the integration</span></span>

<span data-ttu-id="78794-143">Voit määrittää kustannuslaskentapalvelun ja Dynamics 365 Supply Chain Managementin integroinnin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="78794-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="78794-144">Siirry kohtaan **Järjestelmänhallinta > Ominaisuuksien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="78794-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="78794-145">Valitse **Tarkista päivitysten saatavuus**.</span><span class="sxs-lookup"><span data-stu-id="78794-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="78794-146">Avaa **Kaikki**-välilehti ja etsi toiminto, jonka nimi on *Kustannuslaskentapalvelu*.</span><span class="sxs-lookup"><span data-stu-id="78794-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="78794-147">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="78794-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="78794-148">Siirry kohtaan **Kustannusten hallinta > Kustannuslaskentapalvelu > Asetukset > Kustannuslaskentapalvelun parametrit > Integrointien parametrit**.</span><span class="sxs-lookup"><span data-stu-id="78794-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="78794-149">Syötä **Sovellustunnus**-kenttään seuraava koodi:</span><span class="sxs-lookup"><span data-stu-id="78794-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="78794-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="78794-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="78794-151">Kirjoita **Tietopalvelun päätepiste** -kenttään seuraava URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="78794-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="78794-152">Kirjoita **Kustannuslaskentapalvelun päätepiste** -kenttään seuraava URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="78794-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="78794-153">Kustannuslaskentapalvelu on nyt valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="78794-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="78794-154">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="78794-154">Related resources</span></span>

[<span data-ttu-id="78794-155">Kustannuslaskentapalvelun aloitussivu</span><span class="sxs-lookup"><span data-stu-id="78794-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
