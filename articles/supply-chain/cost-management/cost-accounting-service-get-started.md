---
title: Kustannuslaskentapalvelun käytön aloittaminen (yksityinen esiversio)
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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: bbf2df112657342245aca2bd02e06cee7e51ea82
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251047"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="3de7c-103">Kustannuslaskentapalvelun käytön aloittaminen (yksityinen esiversio)</span><span class="sxs-lookup"><span data-stu-id="3de7c-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="3de7c-104">Tässä ohjeaiheessa kuvatut toiminnot ovat saatavilla käyttöön yksityisen ennakkoversion osana.</span><span class="sxs-lookup"><span data-stu-id="3de7c-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="3de7c-105">Tämän ohjeaiheen sisältö ja sen kuvaamien toimintojen muutokset saattavat muuttua.</span><span class="sxs-lookup"><span data-stu-id="3de7c-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="3de7c-106">Lisätietoja ennakkojulkaisusta on kohdassa [Yhden version palvelupäivitysten usein kysytyt kysymykset](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="3de7c-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="3de7c-107">Kustannuslaskentapalvelun avulla voit suorittaa useita varastokirjanpitoja määrittämissäsi kustannuslaskentarekistereissä.</span><span class="sxs-lookup"><span data-stu-id="3de7c-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="3de7c-108">Kukin kustannuslaskentatapahtuma liitetään *käytäntöön*.</span><span class="sxs-lookup"><span data-stu-id="3de7c-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="3de7c-109">Yleissopimus on kokoelma seuraavantyyppisiä kirjanpitokäytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="3de7c-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="3de7c-110">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="3de7c-110">Cost object</span></span>
- <span data-ttu-id="3de7c-111">Syötteen mittaperuste</span><span class="sxs-lookup"><span data-stu-id="3de7c-111">Input measurement basis</span></span>
- <span data-ttu-id="3de7c-112">Kustannusvirran oletus</span><span class="sxs-lookup"><span data-stu-id="3de7c-112">Cost flow assumption</span></span>
- <span data-ttu-id="3de7c-113">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="3de7c-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="3de7c-114">Vaikka olet ottanut kustannuslaskentapalvelun käyttöön, voit silti tehdä varastokirjanpidon Microsoft Dynamics 365 Supply Chain Management -ohjelmassa tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="3de7c-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="3de7c-115">Kustannuslaskentapalvelu on apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="3de7c-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="3de7c-116">Jos haluat käyttää sen toimintoja, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesistä (LCS).</span><span class="sxs-lookup"><span data-stu-id="3de7c-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3de7c-117">Tämän vuoksi voit valita, että se arvioidaan testiympäristössä, ennen kuin otat sen käyttöön tuotantoympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="3de7c-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="3de7c-118">Kustannuslaskentapalvelu ei tällä hetkellä tue kaikkia Dynamics 365 Supply Chain Managementin sisäänrakennettuja kustannustenhallintatoimintoja.</span><span class="sxs-lookup"><span data-stu-id="3de7c-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3de7c-119">Tämän vuoksi on tärkeää arvioida, vastaako tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="3de7c-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="3de7c-120">Kustannuslaskentapalvelun hankkiminen (yksityinen esiversio)</span><span class="sxs-lookup"><span data-stu-id="3de7c-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3de7c-121">Kustannuslaskentapalvelun käyttäminen edellyttää, että käytössä on LCS-yhteensopiva korkean käytettävyyden ympäristö (ei OneBox-ympäristö) ja että käytössä on Dynamics 365 Supply Chain Managementin versio 10.0.11 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="3de7c-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="3de7c-122">Kustannuslaskentapalvelun yksityiseen esiversioon kirjaudutaan lähettämällä LCS-ympäristön tunnus sähköpostitse [kustannuslaskentapalveluun (yksityinen esikatselu)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="3de7c-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="3de7c-123">Kun sinut hyväksytään ohjelmaan, saat seurantasähköpostin, jossa on kustannuslaskentapalvelun beeta-avain.</span><span class="sxs-lookup"><span data-stu-id="3de7c-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="3de7c-124">Kun olet saanut beeta-avaimen, voit jatkaa [lisäosan asentamiseen](#install).</span><span class="sxs-lookup"><span data-stu-id="3de7c-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="3de7c-125">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="3de7c-125">Licensing</span></span>

<span data-ttu-id="3de7c-126">Kustannuslaskentapalvelu on lisensoitu yhdessä Supply Chain Managementin käytettävissä olevien varastokirjanpidon vakiotoimintojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="3de7c-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="3de7c-127">Sinun ei tarvitse ostaa lisäkäyttöoikeutta, jotta voisit käyttää kustannuslaskentapalvelua.</span><span class="sxs-lookup"><span data-stu-id="3de7c-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="3de7c-128">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="3de7c-128">Install the add-in</span></span>

<span data-ttu-id="3de7c-129">Jos haluat käyttää kustannuslaskentapalvelua, asenna kustannuslaskentapalvelun apuohjelma Supply Chain Managementia varten seuraavassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="3de7c-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="3de7c-130">[Kirjaudu](#sign-up) kustannuslaskentapalveluun (yksityinen esiversio).</span><span class="sxs-lookup"><span data-stu-id="3de7c-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="3de7c-131">Kirjaudu sisään LCS:ään.</span><span class="sxs-lookup"><span data-stu-id="3de7c-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="3de7c-132">Mene kohtaan **Toimintojen hallinnan esiversio**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="3de7c-133">Valitse plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="3de7c-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="3de7c-134">Syötä **Koodi**-kenttään kustannuslaskentapalvelun apuohjelman beeta-avain.</span><span class="sxs-lookup"><span data-stu-id="3de7c-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="3de7c-135">(Sinun olisi pitänyt vastaanottaa avaimesi sähköpostilla.)</span><span class="sxs-lookup"><span data-stu-id="3de7c-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="3de7c-136">Valitse **Poista esto**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="3de7c-137">Avaa LCS-ympäristö, johon haluat lisätä palvelun.</span><span class="sxs-lookup"><span data-stu-id="3de7c-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="3de7c-138">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="3de7c-139">Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="3de7c-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="3de7c-140">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="3de7c-141">Valitse **Kustannuslaskentapalvelu**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="3de7c-142">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="3de7c-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="3de7c-143">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-143">Select **Install**.</span></span>

1. <span data-ttu-id="3de7c-144">**Ympäristön apuohjelmat** -pikavälilehdessä näkyy, että kustannuslaskentapalvelua asennetaan.</span><span class="sxs-lookup"><span data-stu-id="3de7c-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="3de7c-145">Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta **Asennetaan** tilaan **Asennettu**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="3de7c-146">(Sivu on ehkä päivitettävä, jotta näet tämän muutoksen.) Tässä vaiheessa kustannuslaskentapalvelu on valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="3de7c-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="3de7c-147">Määritä integraatio</span><span class="sxs-lookup"><span data-stu-id="3de7c-147">Set up the integration</span></span>

<span data-ttu-id="3de7c-148">Voit määrittää kustannuslaskentapalvelun ja Dynamics 365 Supply Chain Managementin integroinnin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="3de7c-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="3de7c-149">Siirry kohtaan **Järjestelmänhallinta > Ominaisuuksien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="3de7c-150">Valitse **Tarkista päivitysten saatavuus**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="3de7c-151">Avaa **Kaikki**-välilehti ja etsi toiminto, jonka nimi on *Kustannuslaskentapalvelu*.</span><span class="sxs-lookup"><span data-stu-id="3de7c-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="3de7c-152">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="3de7c-153">Siirry kohtaan **Kustannusten hallinta > Kustannuslaskentapalvelu > Asetukset > Kustannuslaskentapalvelun parametrit > Integrointien parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3de7c-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="3de7c-154">Syötä **Sovellustunnus**-kenttään seuraava koodi:</span><span class="sxs-lookup"><span data-stu-id="3de7c-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="3de7c-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="3de7c-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="3de7c-156">Kirjoita **Tietopalvelun päätepiste** -kenttään seuraava URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="3de7c-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="3de7c-157">Kirjoita **Kustannuslaskentapalvelun päätepiste** -kenttään seuraava URL-osoite:</span><span class="sxs-lookup"><span data-stu-id="3de7c-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="3de7c-158">Kustannuslaskentapalvelu on nyt valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="3de7c-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="3de7c-159">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="3de7c-159">Related resources</span></span>

[<span data-ttu-id="3de7c-160">Kustannuslaskentapalvelun aloitussivu</span><span class="sxs-lookup"><span data-stu-id="3de7c-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]