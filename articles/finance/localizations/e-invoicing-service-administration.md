---
title: Sähköisen laskutuksen hallintakomponentit
description: Tässä ohjeaiheessa on tietoja sähköisen laskutuksen hallintaan liittyvistä komponenteista.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980920"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="72ed7-103">Sähköisen laskutuksen hallintakomponentit</span><span class="sxs-lookup"><span data-stu-id="72ed7-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="72ed7-104">Tässä ohjeaiheessa on tietoja sähköisen laskutuksen hallintaan liittyvistä komponenteista.</span><span class="sxs-lookup"><span data-stu-id="72ed7-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="72ed7-105">Se sisältää myös tietoja sähköisen laskutuksen palvelun konfiguroinnista.</span><span class="sxs-lookup"><span data-stu-id="72ed7-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="72ed7-106">Azure</span><span class="sxs-lookup"><span data-stu-id="72ed7-106">Azure</span></span>

<span data-ttu-id="72ed7-107">Microsoft Azuren avulla voit luoda Key Vaultin ja tallennustilin salaisia koodeja.</span><span class="sxs-lookup"><span data-stu-id="72ed7-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="72ed7-108">Käytä sen jälkeen sen salaisia koodeja sähköisen laskutuksen konfiguroinnissa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="72ed7-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="72ed7-109">Lifecycle Services</span></span>

<span data-ttu-id="72ed7-110">Ota Microsoft Dynamics Lifecycle Servicesin (LCS) avulla käyttöön mikropalvelut LCS-käyttöönottoprojektille.</span><span class="sxs-lookup"><span data-stu-id="72ed7-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="72ed7-111">Mikropalveluiden asennus LCS:ssä edellyttää vähintään Tier 2 -virtuaalikoneen asentamista.</span><span class="sxs-lookup"><span data-stu-id="72ed7-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="72ed7-112">Lisätietoja ympäristöjen suunnittelusta on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="72ed7-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="72ed7-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="72ed7-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="72ed7-114">Dynamics 365 Regulatory Configuration Services (RCS) on liittymä, jota käytetään sähköisen laskutuksen määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="72ed7-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="72ed7-115">Resursseja, kuten ympäristöjä ja sähköistä laskutusta, luodaan, ylläpidetään ja ylläpidetään RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="72ed7-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="72ed7-116">Kun resurssit ovat valmiita, ne julkaistaan sähköisen laskutuksen palvelussa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="72ed7-117">Lisätietoja RCS-rekisteröitymisistä on kohdassa [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="72ed7-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="72ed7-118">Lisätietoja RCS:stä: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="72ed7-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="72ed7-119">Sähköisen laskutuksen integrointi</span><span class="sxs-lookup"><span data-stu-id="72ed7-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="72ed7-120">Ennen kuin sähköisten laskujen konfiguroinnissa voi käyttää RCS:ää, RCS on määritettävä sallimaan tietoliikenne sähköisen laskutuksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="72ed7-121">Tämä konfigurointi tehdään **Sähköisen raportoinnin parametrit** -sivun **Sähköinen laskutus** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="72ed7-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="72ed7-122">Palvelun päätepiste</span><span class="sxs-lookup"><span data-stu-id="72ed7-122">Service endpoint</span></span>

<span data-ttu-id="72ed7-123">Sähköinen laskutus on käytössä useilla Azure-palvelinkeskusten maantieteellisillä alueilla.</span><span class="sxs-lookup"><span data-stu-id="72ed7-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="72ed7-124">Seuraavassa taulukossa luetellaan käytettävyys alueittain.</span><span class="sxs-lookup"><span data-stu-id="72ed7-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="72ed7-125">Azure-konesalin alue</span><span class="sxs-lookup"><span data-stu-id="72ed7-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="72ed7-126">Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="72ed7-126">United States</span></span>              |
| <span data-ttu-id="72ed7-127">Eurooppa</span><span class="sxs-lookup"><span data-stu-id="72ed7-127">Europe</span></span>                     |
| <span data-ttu-id="72ed7-128">Iso-Britannia</span><span class="sxs-lookup"><span data-stu-id="72ed7-128">United Kingdom</span></span>             |
| <span data-ttu-id="72ed7-129">Aasia</span><span class="sxs-lookup"><span data-stu-id="72ed7-129">Asia</span></span>                       |

### <a name="service-environments"></a><span data-ttu-id="72ed7-130">Palveluympäristöt</span><span class="sxs-lookup"><span data-stu-id="72ed7-130">Service environments</span></span>

<span data-ttu-id="72ed7-131">Palveluympäristöt ovat loogisia osioita, jotka luodaan sähköisen laskutuksen sähköisten laskutusominaisuuksien suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="72ed7-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="72ed7-132">Suojauksen salasanat ja digitaaliset varmenteet sekä hallinto (eli käyttöoikeudet) on määritettävä palveluympäristön tasolla.</span><span class="sxs-lookup"><span data-stu-id="72ed7-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="72ed7-133">Asiakkaat voivat luoda niin monta palveluympäristöä kuin haluavat.</span><span class="sxs-lookup"><span data-stu-id="72ed7-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="72ed7-134">Kaikki asiakkaan luomat palveluympäristöt ovat toisistaan riippumattomia.</span><span class="sxs-lookup"><span data-stu-id="72ed7-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="72ed7-135">Palveluympäristöt on luotava ja ylläpidettävä RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="72ed7-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="72ed7-136">Kun palveluympäristöt ovat valmiita, ne pitää julkaista sähköisessä laskutuksessa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="72ed7-137">Palveluympäristön tila</span><span class="sxs-lookup"><span data-stu-id="72ed7-137">Service environment status</span></span>

<span data-ttu-id="72ed7-138">Palveluympäristöjä voidaan hallita tilan kautta.</span><span class="sxs-lookup"><span data-stu-id="72ed7-138">Service environments can be managed through status.</span></span> <span data-ttu-id="72ed7-139">Mahdolliset vaihtoehdot ovat:</span><span class="sxs-lookup"><span data-stu-id="72ed7-139">The possible options are:</span></span>

- <span data-ttu-id="72ed7-140">**Ei julkaistu** – Ympäristö on luotu, mutta sitä ei ole vielä julkaistu.</span><span class="sxs-lookup"><span data-stu-id="72ed7-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="72ed7-141">**Julkaistu** – Ympäristö on julkaistu sähköisessä laskutuksessa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="72ed7-142">**Muutettu** – Julkaistun ympäristön määritteitä on muutettu, mutta muutoksia ei ole vielä julkaistu.</span><span class="sxs-lookup"><span data-stu-id="72ed7-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="72ed7-143">Asiakkaan salaiset koodit</span><span class="sxs-lookup"><span data-stu-id="72ed7-143">Customer secrets</span></span>

<span data-ttu-id="72ed7-144">Sähköinen laskutus vastaa kaikkien liiketoimintatietojen tallentamisesta yrityksen omistamiin Azure-resursseihin.</span><span class="sxs-lookup"><span data-stu-id="72ed7-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="72ed7-145">Sen varmistamiseksi, että palvelu toimii oikein ja että kaikki sähköistä laskutusta varten tarvittavat ja sen luomat liiketoimintatiedot ovat asianmukaisesti käytettävissä, on luotava kaksi keskeistä Azure-resurssia:</span><span class="sxs-lookup"><span data-stu-id="72ed7-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="72ed7-146">Azure-tallennustili (Blob-tallennus) sähköisten laskujen tallentamista varten</span><span class="sxs-lookup"><span data-stu-id="72ed7-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="72ed7-147">Azure Key Vault, johon tallennetaan tallennustilin tallennusvarmenteet ja Uniform Resource Identifier (URI)</span><span class="sxs-lookup"><span data-stu-id="72ed7-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="72ed7-148">Erillinen Key Vault ja asiakkaan tallennustili on määritettävä nimenomaisesti käytettäväksi sähköisen laskutuksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="72ed7-149">Lisätietoja: [Azure-tallennustilin ja Key Vaultin luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="72ed7-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="72ed7-150">Jos haluat seurata Key Vaultin kuntoa ja vastaanottaa hälytyksiä, voit määrittää Azure Monitorin Key Vaultille.</span><span class="sxs-lookup"><span data-stu-id="72ed7-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="72ed7-151">Ottamalla Key Vault -lokikirjauksen käyttöön voit valvoa, miten, koska ja kuka käyttää Key Vaulteja.</span><span class="sxs-lookup"><span data-stu-id="72ed7-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="72ed7-152">Lisätietoja on kohdassa [Azure Key Vaultin seuranta ja hälytykset](/azure/key-vault/general/alert) ja [Key Vault -lokikirjauksen käyttöönotto](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="72ed7-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="72ed7-153">Parhaana käytäntönä salaisia koodeja kannattaa vaihtaa säännöllisesti.</span><span class="sxs-lookup"><span data-stu-id="72ed7-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="72ed7-154">Lisätietoja on kohdassa [Salaisten koodien dokumentaatio](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="72ed7-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="72ed7-155">Käyttäjät</span><span class="sxs-lookup"><span data-stu-id="72ed7-155">Users</span></span>

<span data-ttu-id="72ed7-156">Jokaisessa palveluympäristössä on oltava luettelo käyttäjistä, jotka voivat muodostaa yhteyden Dynamics 365 Financesta tai Dynamics 365 Supply Chain Managementista sähköiseen laskutukseen.</span><span class="sxs-lookup"><span data-stu-id="72ed7-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="72ed7-157">Julkaisu</span><span class="sxs-lookup"><span data-stu-id="72ed7-157">Publication</span></span>

<span data-ttu-id="72ed7-158">Palveluympäristöt pitää julkaista sähköisessä laskutuksessa, ennen kuin niitä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="72ed7-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="72ed7-159">Finance ja Supply Chain Management voivat käyttää vain julkaisuja ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="72ed7-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="72ed7-160">Lisäksi palveluympäristö on julkaistava, ennen kuin sen määritteiden päivitykset tulevat voimaan sähköisessä laskutuspalvelussa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="72ed7-161">Sovellukset, joista on muodostettu yhteys</span><span class="sxs-lookup"><span data-stu-id="72ed7-161">Connected applications</span></span>

<span data-ttu-id="72ed7-162">Liitetyt sovellukset ovat ne Finance- ja Supply Chain Management -esiintymät, joihin haluat ehkä ottaa yhteyttä RCS:n kautta.</span><span class="sxs-lookup"><span data-stu-id="72ed7-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="72ed7-163">Sovelluksen URL-osoitteen ja vuokraajan lisäksi liitetty sovellus sisältää tunnistetiedot, joiden avulla RCS voi muodostaa yhteyden ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="72ed7-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="72ed7-164">Toisiinsa liitettyjen sovellusten avulla voit konfiguroida osan sähköistä laskutustoimintoa Financessa ja Supply Chain Managementissa, jotta koko sähköinen laskutustoiminto toimisi.</span><span class="sxs-lookup"><span data-stu-id="72ed7-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="72ed7-165">Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="72ed7-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="72ed7-166">Sähköisen laskutuksen integrointi</span><span class="sxs-lookup"><span data-stu-id="72ed7-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="72ed7-167">Ennen kuin Financea ja Supply Chain Managementia voidaan käyttää sähköisten laskujen lähettämiseen sähköisen laskutuksen kautta, laskutus on määritettävä niin, että se sallii viestinnän palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="72ed7-168">Sähköisen laskutuksen integrointiominaisuus</span><span class="sxs-lookup"><span data-stu-id="72ed7-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="72ed7-169">Financen ja Supply Chain Managementin ja sähköisen laskutuksen välisen viestinnän mahdollistamiseksi **Sähköisen laskutuksen integrointi** -ominaisuus on otettava käyttöön **Ominaisuuden hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="72ed7-170">Palvelun päätepiste</span><span class="sxs-lookup"><span data-stu-id="72ed7-170">Service endpoint</span></span>

<span data-ttu-id="72ed7-171">Palvelun päätepiste on URL-osoite, jossa sähköinen laskutus sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="72ed7-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="72ed7-172">Ennen kuin sähköisiä laskuja voidaan lähettää palvelun päätepiste pitää määrittää Financessa ja Supply Chain Managementissa niin, että se sallii viestinnän palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="72ed7-173">Voit määrittää palvelun päätepisteen siirtymällä kohtaan **Organisaation hallinto \> Määritys \> Sähköisen asiakirjan parametri** ja kirjoita **Lähetyspalvelut**-välilehden **Sähköisen laskutuksen URL-osoite** -kenttään URL-osoite, kuten on kuvattu osan **Palvelun päätepiste** -osan taulukossa.</span><span class="sxs-lookup"><span data-stu-id="72ed7-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="72ed7-174">Ympäristöt</span><span class="sxs-lookup"><span data-stu-id="72ed7-174">Environments</span></span>

<span data-ttu-id="72ed7-175">Financeen ja Supply Chain Managementiin syötetty ympäristönimi viittaa RCS:ssä luotavaan ja sähköiseen laskutukseen julkaistavaan ympäristön nimeen.</span><span class="sxs-lookup"><span data-stu-id="72ed7-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="72ed7-176">Ympäristö on konfiguroitava **Sähköisen tiedoston parametri** -sivun **Lähetyspalvelut**-välilehdessä, jotta kaikki sähköisten laskujen lähetyspyynnöt sisältävät ympäristön, jossa sähköinen laskutus voi määrittää, mikä sähköisen laskutuksen toiminto käsittelee pyynnön.</span><span class="sxs-lookup"><span data-stu-id="72ed7-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72ed7-177">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="72ed7-177">Additional resources</span></span>

- [<span data-ttu-id="72ed7-178">Konfiguroi sähköiset laskut RCS:ssä</span><span class="sxs-lookup"><span data-stu-id="72ed7-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="72ed7-179">Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="72ed7-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
