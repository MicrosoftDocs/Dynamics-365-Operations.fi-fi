---
title: Asiakirjojen tulostuksen yleiskatsaus
description: Voit tulostaa asiakirjat joko paikallisessa tulostimessa tai verkkotulostimessa. Tässä artikkelissa yhteenveto asiakirjojen tulostamisesta.
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c349e50826aa577ce6a3b8a68676d549f7fed1b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564402"
---
# <a name="document-printing-overview"></a><span data-ttu-id="52c80-104">Asiakirjojen tulostuksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="52c80-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52c80-105">Voit tulostaa asiakirjat joko paikallisessa tulostimessa tai verkkotulostimessa.</span><span class="sxs-lookup"><span data-stu-id="52c80-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="52c80-106">Tässä artikkelissa yhteenveto asiakirjojen tulostamisesta.</span><span class="sxs-lookup"><span data-stu-id="52c80-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="52c80-107">Tulostamisen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="52c80-107">Printing overview</span></span>

<span data-ttu-id="52c80-108">Sovelluksessa on integroituja huolto- ja asiakasohjelmasovelluksia, joilla on helppo luoda, tallentaa ja jakaa liiketoimintoja tukevia asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="52c80-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="52c80-109">Voit tulostaa asiakirjat joko paikallisessa tulostimessa tai verkkotulostimessa.</span><span class="sxs-lookup"><span data-stu-id="52c80-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="52c80-110">Voit lisäksi viedä sivuja ja raportteja suodaan asiakasohjelmista esimerkiksi PDF- tai Microsoft Office -tiedostoina.</span><span class="sxs-lookup"><span data-stu-id="52c80-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="52c80-111">Ja koska työkuorma jaetaan, voi tulostaa liiketoiminta-asiakirjoja suoraan mobiililaitteesta verkkoresurssien avulla.</span><span class="sxs-lookup"><span data-stu-id="52c80-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="52c80-112">Vaikka tulostusvaatimukset voivat vaihdella, kaikilla toimialoilla liiketoiminta-asiakirjat on yleensä tulostettava sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="52c80-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="52c80-113">Asiakirjojen tulostaminen verkkolaitteilla isännöidyistä sovelluksista tuo mukanaan aivan omanlaisensa haasteet.</span><span class="sxs-lookup"><span data-stu-id="52c80-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="52c80-114">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="52c80-114">Here are some examples:</span></span>

- <span data-ttu-id="52c80-115">Tulostimen ohjaimet eivät ehkä ole käytettävissä käyttäjän laitteessa.</span><span class="sxs-lookup"><span data-stu-id="52c80-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="52c80-116">Käyttäjän laitetta ei ole ehkä liitetty yritysverkkoon.</span><span class="sxs-lookup"><span data-stu-id="52c80-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="52c80-117">Kun järjestelmänvalvojat käyttävät tarkoitukseen varattua isäntään ja toimivat seuraavien helppojen ohjeiden mukaisesti, he voivat määrittää käyttöönotot siten, että käyttäjät voivat tulostaa suoraan verkkolaitteiden yrityssovelluksista.</span><span class="sxs-lookup"><span data-stu-id="52c80-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="52c80-118">Sovelluksen tulostusskenaariot</span><span class="sxs-lookup"><span data-stu-id="52c80-118">Application printing scenarios</span></span> 

<span data-ttu-id="52c80-119">Seuraavassa taulukossa kuvataan kolme ensisijaista tulostusskenaariota.</span><span class="sxs-lookup"><span data-stu-id="52c80-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="52c80-120">Skenaario</span><span class="sxs-lookup"><span data-stu-id="52c80-120">Scenario</span></span>                        | <span data-ttu-id="52c80-121">Tavoite</span><span class="sxs-lookup"><span data-stu-id="52c80-121">Goal</span></span>                                                      | <span data-ttu-id="52c80-122">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="52c80-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="52c80-123">1. Näkyvissä olevan tulostaminen</span><span class="sxs-lookup"><span data-stu-id="52c80-123">1. Printing what you see</span></span>        | <span data-ttu-id="52c80-124">Tulosta selaimessa näkyvä sisältö.</span><span class="sxs-lookup"><span data-stu-id="52c80-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="52c80-125">Selaimeen muodostetaan verkkosivun tulostettava versio.</span><span class="sxs-lookup"><span data-stu-id="52c80-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="52c80-126">2. Vuorovaikutteinen tulostus</span><span class="sxs-lookup"><span data-stu-id="52c80-126">2. Interactive printing</span></span>         | <span data-ttu-id="52c80-127">Tulosta tietty asiakirja paikallisesti liitetyssä laitteessa.</span><span class="sxs-lookup"><span data-stu-id="52c80-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="52c80-128">Voit viedä raportin PDF-version ja ladata sen selaimeen.</span><span class="sxs-lookup"><span data-stu-id="52c80-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="52c80-129">3. Tulosta verkkolaitteessa</span><span class="sxs-lookup"><span data-stu-id="52c80-129">3. Printing on a network device</span></span> | <span data-ttu-id="52c80-130">Lähetä tietty asiakirja toimialueen tulostimeen.</span><span class="sxs-lookup"><span data-stu-id="52c80-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="52c80-131">Tietty asiakirja lähetetään asiakkaan toimialueella isännöidyssä tulostimessa toimivaan asiakassovellukseen.</span><span class="sxs-lookup"><span data-stu-id="52c80-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="52c80-132">Koska ratkaisu vaihtelee skenaarion mukaan, sovelluksiin sisältyy palveluja ja työkaluja, joiden avulla käyttäjät saavuttavat tavoitteensa:</span><span class="sxs-lookup"><span data-stu-id="52c80-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="52c80-133">Selain tukee **skenaariota 1** hahmontamalla HTML5-asiakasohjelman.</span><span class="sxs-lookup"><span data-stu-id="52c80-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="52c80-134">**Skenaario 2** käyttää asiakassovellusta ja Microsoft 365 -palveluja.</span><span class="sxs-lookup"><span data-stu-id="52c80-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="52c80-135">**Skenaario 3** edellyttää asiakassovellusten ja Microsoft Azuressa isännöityjen palvelujen tukea.</span><span class="sxs-lookup"><span data-stu-id="52c80-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="52c80-136">Azure-tilauksessa käyttöönotetun ympäristön lisäksi Finance and Operations -sovellukset antavat asiakkaille integroidun, ensikäden Azure-sovelluksen, joka helpottaa asiakirjojen tulostusta toimialueella isännöidyissä laitteissa.</span><span class="sxs-lookup"><span data-stu-id="52c80-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="52c80-137">Palvelujen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="52c80-137">Service overview</span></span>
<span data-ttu-id="52c80-138">Verkkoon liitetyssä laitteessa tulostusta odottavat isännöityjen sovellusten tuottamat asiakirjat tallennetaan Azure Blob -säilöön.</span><span class="sxs-lookup"><span data-stu-id="52c80-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="52c80-139">[Verkkotulostuksen käyttöönotto asentamalla asiakirjan reititysagentti](install-document-routing-agent.md) muodostaa turvallisen kanavan Azure-palveluihin Azure-todennuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="52c80-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="52c80-140">**Suoritusjärjestys**</span><span class="sxs-lookup"><span data-stu-id="52c80-140">**Execution sequence**</span></span>

1. <span data-ttu-id="52c80-141">Microsoft SQL Server Reporting Services (SSRS) luo raportin, joka tallennetaan Azure Blob -säilöön.</span><span class="sxs-lookup"><span data-stu-id="52c80-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="52c80-142">Liitetyt tulostinasetukset tallennetaan yhdessä asiakirjan kanssa.</span><span class="sxs-lookup"><span data-stu-id="52c80-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="52c80-143">Asiakirjareitityksen agentti kyselee aktiivisia töitä Azuren palveluväylän jonosta.</span><span class="sxs-lookup"><span data-stu-id="52c80-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="52c80-144">Asiakirjareitityksen agentti lataa asiakirjan, joka viedään taustatulostukseen verkkotulostimeen.</span><span class="sxs-lookup"><span data-stu-id="52c80-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="52c80-145">Asiakasohjelmaan perustuvan ratkaisun ansiosta asiakkaat voivat hallita tulostustarpeidensa laajuutta.</span><span class="sxs-lookup"><span data-stu-id="52c80-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="52c80-146">Paljon tulostavat asiakkaat voivat asentaa useita asiakirjareitityksen agentteja, mikä mahdollistaa entistä useamman samanaikaisen tulostoiminnan suorittamisen.</span><span class="sxs-lookup"><span data-stu-id="52c80-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="52c80-147">Toisille asiakkaalle puolestaan riittää vain muutama asiakirjareitityksen agentti oletettujen tulostustarpeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="52c80-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="52c80-148">Verkkotulostuksen palveluosat</span><span class="sxs-lookup"><span data-stu-id="52c80-148">Service components for network printing</span></span>

<span data-ttu-id="52c80-149">Seuraavassa kaaviossa on verkkotulostusta tukevat perusosat.</span><span class="sxs-lookup"><span data-stu-id="52c80-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="52c80-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="52c80-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="52c80-151">Huomaa, että yhteen tulostimeen voidaan rekisteröidä useita asiakirjan reititysagentteja.</span><span class="sxs-lookup"><span data-stu-id="52c80-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="52c80-152">Isännöity palvelu ratkaisee tulostinasetukset käyttämällä verkkopolkua, joka tunnistaa yksilöllisesti jokaisen verkkotulostimen.</span><span class="sxs-lookup"><span data-stu-id="52c80-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="52c80-153">Tämän vuoksi myös sellainen tulostin, johon on rekisteröity useita asiakasohjelmia, näkyy yhtenä valintana sovellusten käytettävissä olevien tulostimien luettelossa.</span><span class="sxs-lookup"><span data-stu-id="52c80-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]