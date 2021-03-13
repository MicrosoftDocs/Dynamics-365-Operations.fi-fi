---
title: Sähköisen laskutuksen lisäosien hallintakomponentit
description: Tässä ohjeaiheessa on tietoja sähköisen laskutuksen lisäosan hallintaan liittyvistä komponenteista.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104375"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="a0472-103">Sähköisen laskutuksen lisäosien hallintakomponentit</span><span class="sxs-lookup"><span data-stu-id="a0472-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a0472-104">Tässä ohjeaiheessa on tietoja sähköisen laskutuksen lisäosan hallintaan liittyvistä komponenteista.</span><span class="sxs-lookup"><span data-stu-id="a0472-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0472-105">Se sisältää myös tietoja sähköisen laskutuksen lisäpalvelun konfiguroinnista.</span><span class="sxs-lookup"><span data-stu-id="a0472-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="a0472-106">Azure</span><span class="sxs-lookup"><span data-stu-id="a0472-106">Azure</span></span>

<span data-ttu-id="a0472-107">Microsoft Azuren avulla voit luoda avainsäilön ja tallennustilin salaisia koodeja.</span><span class="sxs-lookup"><span data-stu-id="a0472-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="a0472-108">Käytä sen jälkeen sen salaisia koodeja sähköisen laskutuksen lisäosan konfiguroinnissa.</span><span class="sxs-lookup"><span data-stu-id="a0472-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="a0472-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a0472-109">Lifecycle Services</span></span>

<span data-ttu-id="a0472-110">Ota Microsoft DynamicsLifecycle Servicesin (LCS) avulla käyttöön lisäosa LCS-käyttöönottoprojektin mikropalveluille.</span><span class="sxs-lookup"><span data-stu-id="a0472-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="a0472-111">Valitse LCS:ssä **Esiversio-ominaisuuden hallinta** -ruutu ja ota sitten **sähköisen laskutuksen palvelu** käyttöön.</span><span class="sxs-lookup"><span data-stu-id="a0472-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="a0472-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="a0472-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="a0472-113">Dynamics 365 Regulatory Configuration Services (RCS) on liittymä, jota käytetään sähköisen laskutuksen lisäosan määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="a0472-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0472-114">Resursseja, kuten ympäristöjä ja sähköistä laskutusta, luodaan, ylläpidetään ja ylläpidetään RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="a0472-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="a0472-115">Kun resurssit ovat valmiita, ne julkaistaan sähköisen laskutuksen lisäpalvelussa.</span><span class="sxs-lookup"><span data-stu-id="a0472-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="a0472-116">Lisätietoja RCS:stä: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="a0472-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="a0472-117">Sähköisen laskutuksen lisäosan integrointi</span><span class="sxs-lookup"><span data-stu-id="a0472-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="a0472-118">Ennen kuin sähköisten laskujen konfiguroinnissa voi käyttää RCS:ää, RCS on määritettävä sallimaan tietoliikenne sähköisen laskutuksen lisäosan kanssa.</span><span class="sxs-lookup"><span data-stu-id="a0472-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0472-119">Tämä konfigurointi tehdään **Sähköisen raportoinnin parametrit** -sivun **Sähköisen laskutuksen lisäosa** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="a0472-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="a0472-120">Palvelun päätepiste</span><span class="sxs-lookup"><span data-stu-id="a0472-120">Service endpoint</span></span>

<span data-ttu-id="a0472-121">Sähköisen laskutuksen lisäosan päätepisteen URL-osoite voi vaihdella Azure-konesalin maantieteellisen sijainnin mukaan.</span><span class="sxs-lookup"><span data-stu-id="a0472-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="a0472-122">Seuraavassa taulukossa luetellaan käytettävyys alueittain:</span><span class="sxs-lookup"><span data-stu-id="a0472-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="a0472-123">Azure-konesalin alue</span><span class="sxs-lookup"><span data-stu-id="a0472-123">Azure datacenter geography</span></span> | <span data-ttu-id="a0472-124">Palvelun päätepisteen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="a0472-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a0472-125">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="a0472-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="a0472-126">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="a0472-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="a0472-127">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="a0472-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="a0472-128">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="a0472-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="a0472-129">Sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="a0472-129">Application ID</span></span>

<span data-ttu-id="a0472-130">Sovellustunnus on sähköisen laskutuksen lisäosasovelluksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="a0472-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="a0472-131">Tässä tapauksessa arvo on kiinteä: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="a0472-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="a0472-132">LCS-ympäristön tunnus</span><span class="sxs-lookup"><span data-stu-id="a0472-132">LCS environment ID</span></span>

<span data-ttu-id="a0472-133">LCS-ympäristötunnus on organisaation LCS-ylläpitosopimuksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="a0472-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="a0472-134">Palveluympäristöt</span><span class="sxs-lookup"><span data-stu-id="a0472-134">Service environments</span></span>

<span data-ttu-id="a0472-135">Palveluympäristöt ovat loogisia osioita, jotka luodaan sähköisen laskutuksen lisäosan sähköisten laskutusominaisuuksien suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="a0472-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0472-136">Suojauksen salasanat ja digitaaliset varmenteet sekä hallinto (eli käyttöoikeudet) on määritettävä palveluympäristön tasolla.</span><span class="sxs-lookup"><span data-stu-id="a0472-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="a0472-137">Asiakkaat voivat luoda niin monta palveluympäristöä kuin haluavat.</span><span class="sxs-lookup"><span data-stu-id="a0472-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="a0472-138">Kaikki asiakkaan luomat palveluympäristöt ovat toisistaan riippumattomia.</span><span class="sxs-lookup"><span data-stu-id="a0472-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="a0472-139">Palveluympäristöt on luotava ja ylläpidettävä RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="a0472-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="a0472-140">Kun palveluympäristöt ovat valmiita, ne pitää julkaista sähköisen laskutuksen lisäosassa.</span><span class="sxs-lookup"><span data-stu-id="a0472-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="a0472-141">Palveluympäristön tila</span><span class="sxs-lookup"><span data-stu-id="a0472-141">Service environment status</span></span>

<span data-ttu-id="a0472-142">Palveluympäristöjä voidaan hallita tilan kautta.</span><span class="sxs-lookup"><span data-stu-id="a0472-142">Service environments can be managed through status.</span></span> <span data-ttu-id="a0472-143">Mahdolliset vaihtoehdot ovat:</span><span class="sxs-lookup"><span data-stu-id="a0472-143">The possible options are:</span></span>

- <span data-ttu-id="a0472-144">**Ei julkaistu** – Ympäristö on luotu, mutta sitä ei ole vielä julkaistu.</span><span class="sxs-lookup"><span data-stu-id="a0472-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="a0472-145">**Julkaistu** – Ympäristö on julkaistu sähköisen laskutuksen lisäosassa.</span><span class="sxs-lookup"><span data-stu-id="a0472-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="a0472-146">**Muutettu** – Julkaistun ympäristön määritteitä on muutettu, mutta muutoksia ei ole vielä julkaistu.</span><span class="sxs-lookup"><span data-stu-id="a0472-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="a0472-147">Asiakkaan salaiset koodit</span><span class="sxs-lookup"><span data-stu-id="a0472-147">Customer secrets</span></span>

<span data-ttu-id="a0472-148">Sähköisen laskutuksen lisäosapalvelu vastaa kaikkien liiketoimintatietojen tallentamisesta yrityksen omistamiin Azure-resursseihin.</span><span class="sxs-lookup"><span data-stu-id="a0472-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="a0472-149">Sen varmistamiseksi, että palvelu toimii oikein ja että kaikki sähköisen laskutuksen lisäosaa varten tarvittavat ja sen luomat liiketoimintatiedot ovat vain lisäosan käytettävissä, on luotava kaksi keskeistä Azure-resurssia:</span><span class="sxs-lookup"><span data-stu-id="a0472-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="a0472-150">Azure-tallennustili (Blob-tallennus) sähköisten laskujen tallentamista varten</span><span class="sxs-lookup"><span data-stu-id="a0472-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="a0472-151">Azure-avainsäilö, johon tallennetaan tallennustilin tallennusvarmenteet ja Uniform Resource Identifier (URI)</span><span class="sxs-lookup"><span data-stu-id="a0472-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="a0472-152">Erillinen avainsäilö ja asiakkaan tallennustili on määritettävä nimenomaisesti käytettäväksi sähköisen laskutuksen lisäosan kanssa.</span><span class="sxs-lookup"><span data-stu-id="a0472-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="a0472-153">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="a0472-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="a0472-154">Käyttäjät</span><span class="sxs-lookup"><span data-stu-id="a0472-154">Users</span></span>

<span data-ttu-id="a0472-155">Jokaisessa palveluympäristössä on oltava luettelo käyttäjistä, jotka voivat muodostaa yhteyden Dynamics 365 Financesta tai Dynamics 365 Supply Chain Managementista sähköisen laskutuksen lisäosaan.</span><span class="sxs-lookup"><span data-stu-id="a0472-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="a0472-156">Julkaisu</span><span class="sxs-lookup"><span data-stu-id="a0472-156">Publication</span></span>

<span data-ttu-id="a0472-157">Palveluympäristöt pitää julkaista sähköisen laskutuksen lisäosassa, enne kuin niitä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="a0472-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="a0472-158">Finance ja Supply Chain Management voivat käyttää vain julkaisuja ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="a0472-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="a0472-159">Lisäksi palveluympäristö on julkaistava, ennen kuin sen määritteiden päivitykset tulevat voimaan sähköisessä laskutuspalvelussa.</span><span class="sxs-lookup"><span data-stu-id="a0472-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="a0472-160">Sovellukset, joista on muodostettu yhteys</span><span class="sxs-lookup"><span data-stu-id="a0472-160">Connected applications</span></span>

<span data-ttu-id="a0472-161">Liitetyt sovellukset ovat ne Finance- ja Supply Chain Management -esiintymät, joihin haluat ehkä ottaa yhteyttä RCS:n kautta.</span><span class="sxs-lookup"><span data-stu-id="a0472-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="a0472-162">Sovelluksen URL-osoitteen ja vuokraajan lisäksi liitetty sovellus sisältää tunnistetiedot, joiden avulla RCS voi muodostaa yhteyden ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="a0472-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="a0472-163">Toisiinsa liitettyjen sovellusten avulla voit konfiguroida osan sähköistä laskutustoimintoa Financessa ja Supply Chain Managementissa, jotta koko sähköinen laskutustoiminto toimisi.</span><span class="sxs-lookup"><span data-stu-id="a0472-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="a0472-164">Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a0472-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="a0472-165">Sähköisen laskutuksen lisäosan integrointi</span><span class="sxs-lookup"><span data-stu-id="a0472-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="a0472-166">Ennen kuin Financea ja Supply Chain Managementia voidaan käyttää sähköisten laskujen lähettämiseen sähköisen laskutuksen lisäosan kautta, lisäosa on määritettävä niin, että se sallii viestinnän palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="a0472-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="a0472-167">Sähköisen laskutuksen lisäosan integrointiominaisuus</span><span class="sxs-lookup"><span data-stu-id="a0472-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="a0472-168">Financen ja Supply Chain Managementin ja sähköisen laskutuksen lisäosan välisen viestinnän mahdollistamiseksi **Sähköisen laskutuksen lisäosan integrointi** -ominaisuus on otettava käyttöön **Ominaisuuden hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="a0472-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="a0472-169">Palvelun päätepiste</span><span class="sxs-lookup"><span data-stu-id="a0472-169">Service endpoint</span></span>

<span data-ttu-id="a0472-170">Palvelun päätepiste on URL-osoite, jossa sähköisen laskutuksen lisäosa sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="a0472-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="a0472-171">Ennen kuin sähköisiä laskuja voidaan lähettää palvelun päätepiste pitää määrittää Financessa ja Supply Chain Managementissa niin, että se sallii viestinnän palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="a0472-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="a0472-172">Voit määrittää palvelun päätepisteen siirtymällä kohtaan **Organisaation hallinto \> Määritys \> Sähköisen asiakirjan parametri** ja kirjoita **Lähetyspalvelut**-välilehden **Sähköisen laskutuksen lisäosan URL-osoite** -kenttään URL-osoite, kuten on kuvattu osan **Palvelun päätepiste** -osan taulukossa.</span><span class="sxs-lookup"><span data-stu-id="a0472-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="a0472-173">Ympäristöt</span><span class="sxs-lookup"><span data-stu-id="a0472-173">Environments</span></span>

<span data-ttu-id="a0472-174">Financeen ja Supply Chain Managementiin syötetty ympäristönimi viittaa RCS:ssä luotavaan ja sähköiseen laskutukseen lisäosaan julkaistavaan ympäristön nimeen.</span><span class="sxs-lookup"><span data-stu-id="a0472-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="a0472-175">Ympäristö on konfiguroitava **Sähköisen tiedoston parametri** -sivun **Lähetyspalvelut**-välilehdessä, jotta kaikki sähköisten laskujen lähetyspyynnöt sisältävät ympäristön, jossa sähköisen laskutuksen lisäosa voi määrittää, mikä sähköisen laskutuksen toiminto käsittelee pyynnön.</span><span class="sxs-lookup"><span data-stu-id="a0472-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0472-176">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a0472-176">Additional resources</span></span>

- [<span data-ttu-id="a0472-177">Konfiguroi sähköiset laskut RCS:ssä</span><span class="sxs-lookup"><span data-stu-id="a0472-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="a0472-178">Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="a0472-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
