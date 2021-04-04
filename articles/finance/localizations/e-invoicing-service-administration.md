---
title: Sähköisen laskutuksen lisäosien hallintakomponentit
description: Tässä ohjeaiheessa on tietoja sähköisen laskutuksen lisäosan hallintaan liittyvistä komponenteista.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592571"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="c2d53-103">Sähköisen laskutuksen lisäosien hallintakomponentit</span><span class="sxs-lookup"><span data-stu-id="c2d53-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c2d53-104">Tässä ohjeaiheessa on tietoja sähköisen laskutuksen lisäosan hallintaan liittyvistä komponenteista.</span><span class="sxs-lookup"><span data-stu-id="c2d53-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="c2d53-105">Se sisältää myös tietoja sähköisen laskutuksen lisäpalvelun konfiguroinnista.</span><span class="sxs-lookup"><span data-stu-id="c2d53-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="c2d53-106">Azure</span><span class="sxs-lookup"><span data-stu-id="c2d53-106">Azure</span></span>

<span data-ttu-id="c2d53-107">Microsoft Azuren avulla voit luoda avainsäilön ja tallennustilin salaisia koodeja.</span><span class="sxs-lookup"><span data-stu-id="c2d53-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="c2d53-108">Käytä sen jälkeen sen salaisia koodeja sähköisen laskutuksen lisäosan konfiguroinnissa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="c2d53-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c2d53-109">Lifecycle Services</span></span>

<span data-ttu-id="c2d53-110">Ota Microsoft DynamicsLifecycle Servicesin (LCS) avulla käyttöön lisäosa LCS-käyttöönottoprojektin mikropalveluille.</span><span class="sxs-lookup"><span data-stu-id="c2d53-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="c2d53-111">Mikropalveluiden lisäosan asennus LCS:ssä edellyttää vähintään Tier 2 -virtuaalikoneen asentamista.</span><span class="sxs-lookup"><span data-stu-id="c2d53-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="c2d53-112">Lisätietoja ympäristöjen suunnittelusta on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="c2d53-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="c2d53-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="c2d53-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="c2d53-114">Dynamics 365 Regulatory Configuration Services (RCS) on liittymä, jota käytetään sähköisen laskutuksen lisäosan määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="c2d53-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="c2d53-115">Resursseja, kuten ympäristöjä ja sähköistä laskutusta, luodaan, ylläpidetään ja ylläpidetään RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="c2d53-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="c2d53-116">Kun resurssit ovat valmiita, ne julkaistaan sähköisen laskutuksen lisäpalvelussa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="c2d53-117">Lisätietoja RCS-rekisteröitymisistä on kohdassa [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="c2d53-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="c2d53-118">Lisätietoja RCS:stä: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="c2d53-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="c2d53-119">Sähköisen laskutuksen lisäosan integrointi</span><span class="sxs-lookup"><span data-stu-id="c2d53-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="c2d53-120">Ennen kuin sähköisten laskujen konfiguroinnissa voi käyttää RCS:ää, RCS on määritettävä sallimaan tietoliikenne sähköisen laskutuksen lisäosan kanssa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="c2d53-121">Tämä konfigurointi tehdään **Sähköisen raportoinnin parametrit** -sivun **Sähköisen laskutuksen lisäosa** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="c2d53-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="c2d53-122">Palvelun päätepiste</span><span class="sxs-lookup"><span data-stu-id="c2d53-122">Service endpoint</span></span>

<span data-ttu-id="c2d53-123">Sähköisen laskutuksen lisäosa on käytössä useilla Azure-palvelinkeskusten maantieteellisillä alueilla.</span><span class="sxs-lookup"><span data-stu-id="c2d53-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="c2d53-124">Seuraavassa taulukossa luetellaan käytettävyys alueittain.</span><span class="sxs-lookup"><span data-stu-id="c2d53-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="c2d53-125">Azure-konesalin alue</span><span class="sxs-lookup"><span data-stu-id="c2d53-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="c2d53-126">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="c2d53-126">East US</span></span>                    |
| <span data-ttu-id="c2d53-127">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="c2d53-127">West US</span></span>                    |
| <span data-ttu-id="c2d53-128">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="c2d53-128">North EU</span></span>                   |
| <span data-ttu-id="c2d53-129">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="c2d53-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="c2d53-130">Palveluympäristöt</span><span class="sxs-lookup"><span data-stu-id="c2d53-130">Service environments</span></span>

<span data-ttu-id="c2d53-131">Palveluympäristöt ovat loogisia osioita, jotka luodaan sähköisen laskutuksen lisäosan sähköisten laskutusominaisuuksien suorittamista varten.</span><span class="sxs-lookup"><span data-stu-id="c2d53-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="c2d53-132">Suojauksen salasanat ja digitaaliset varmenteet sekä hallinto (eli käyttöoikeudet) on määritettävä palveluympäristön tasolla.</span><span class="sxs-lookup"><span data-stu-id="c2d53-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="c2d53-133">Asiakkaat voivat luoda niin monta palveluympäristöä kuin haluavat.</span><span class="sxs-lookup"><span data-stu-id="c2d53-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="c2d53-134">Kaikki asiakkaan luomat palveluympäristöt ovat toisistaan riippumattomia.</span><span class="sxs-lookup"><span data-stu-id="c2d53-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="c2d53-135">Palveluympäristöt on luotava ja ylläpidettävä RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="c2d53-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="c2d53-136">Kun palveluympäristöt ovat valmiita, ne pitää julkaista sähköisen laskutuksen lisäosassa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="c2d53-137">Palveluympäristön tila</span><span class="sxs-lookup"><span data-stu-id="c2d53-137">Service environment status</span></span>

<span data-ttu-id="c2d53-138">Palveluympäristöjä voidaan hallita tilan kautta.</span><span class="sxs-lookup"><span data-stu-id="c2d53-138">Service environments can be managed through status.</span></span> <span data-ttu-id="c2d53-139">Mahdolliset vaihtoehdot ovat:</span><span class="sxs-lookup"><span data-stu-id="c2d53-139">The possible options are:</span></span>

- <span data-ttu-id="c2d53-140">**Ei julkaistu** – Ympäristö on luotu, mutta sitä ei ole vielä julkaistu.</span><span class="sxs-lookup"><span data-stu-id="c2d53-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="c2d53-141">**Julkaistu** – Ympäristö on julkaistu sähköisen laskutuksen lisäosassa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="c2d53-142">**Muutettu** – Julkaistun ympäristön määritteitä on muutettu, mutta muutoksia ei ole vielä julkaistu.</span><span class="sxs-lookup"><span data-stu-id="c2d53-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="c2d53-143">Asiakkaan salaiset koodit</span><span class="sxs-lookup"><span data-stu-id="c2d53-143">Customer secrets</span></span>

<span data-ttu-id="c2d53-144">Sähköisen laskutuksen lisäosapalvelu vastaa kaikkien liiketoimintatietojen tallentamisesta yrityksen omistamiin Azure-resursseihin.</span><span class="sxs-lookup"><span data-stu-id="c2d53-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="c2d53-145">Sen varmistamiseksi, että palvelu toimii oikein ja että kaikki sähköisen laskutuksen lisäosaa varten tarvittavat ja sen luomat liiketoimintatiedot ovat vain lisäosan käytettävissä, on luotava kaksi keskeistä Azure-resurssia:</span><span class="sxs-lookup"><span data-stu-id="c2d53-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="c2d53-146">Azure-tallennustili (Blob-tallennus) sähköisten laskujen tallentamista varten</span><span class="sxs-lookup"><span data-stu-id="c2d53-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="c2d53-147">Azure-avainsäilö, johon tallennetaan tallennustilin tallennusvarmenteet ja Uniform Resource Identifier (URI)</span><span class="sxs-lookup"><span data-stu-id="c2d53-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="c2d53-148">Erillinen avainsäilö ja asiakkaan tallennustili on määritettävä nimenomaisesti käytettäväksi sähköisen laskutuksen lisäosan kanssa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="c2d53-149">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="c2d53-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="c2d53-150">Käyttäjät</span><span class="sxs-lookup"><span data-stu-id="c2d53-150">Users</span></span>

<span data-ttu-id="c2d53-151">Jokaisessa palveluympäristössä on oltava luettelo käyttäjistä, jotka voivat muodostaa yhteyden Dynamics 365 Financesta tai Dynamics 365 Supply Chain Managementista sähköisen laskutuksen lisäosaan.</span><span class="sxs-lookup"><span data-stu-id="c2d53-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="c2d53-152">Julkaisu</span><span class="sxs-lookup"><span data-stu-id="c2d53-152">Publication</span></span>

<span data-ttu-id="c2d53-153">Palveluympäristöt pitää julkaista sähköisen laskutuksen lisäosassa, enne kuin niitä voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="c2d53-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="c2d53-154">Finance ja Supply Chain Management voivat käyttää vain julkaisuja ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="c2d53-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="c2d53-155">Lisäksi palveluympäristö on julkaistava, ennen kuin sen määritteiden päivitykset tulevat voimaan sähköisessä laskutuspalvelussa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="c2d53-156">Sovellukset, joista on muodostettu yhteys</span><span class="sxs-lookup"><span data-stu-id="c2d53-156">Connected applications</span></span>

<span data-ttu-id="c2d53-157">Liitetyt sovellukset ovat ne Finance- ja Supply Chain Management -esiintymät, joihin haluat ehkä ottaa yhteyttä RCS:n kautta.</span><span class="sxs-lookup"><span data-stu-id="c2d53-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="c2d53-158">Sovelluksen URL-osoitteen ja vuokraajan lisäksi liitetty sovellus sisältää tunnistetiedot, joiden avulla RCS voi muodostaa yhteyden ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="c2d53-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="c2d53-159">Toisiinsa liitettyjen sovellusten avulla voit konfiguroida osan sähköistä laskutustoimintoa Financessa ja Supply Chain Managementissa, jotta koko sähköinen laskutustoiminto toimisi.</span><span class="sxs-lookup"><span data-stu-id="c2d53-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="c2d53-160">Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c2d53-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="c2d53-161">Sähköisen laskutuksen lisäosan integrointi</span><span class="sxs-lookup"><span data-stu-id="c2d53-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="c2d53-162">Ennen kuin Financea ja Supply Chain Managementia voidaan käyttää sähköisten laskujen lähettämiseen sähköisen laskutuksen lisäosan kautta, lisäosa on määritettävä niin, että se sallii viestinnän palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="c2d53-163">Sähköisen laskutuksen lisäosan integrointiominaisuus</span><span class="sxs-lookup"><span data-stu-id="c2d53-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="c2d53-164">Financen ja Supply Chain Managementin ja sähköisen laskutuksen lisäosan välisen viestinnän mahdollistamiseksi **Sähköisen laskutuksen lisäosan integrointi** -ominaisuus on otettava käyttöön **Ominaisuuden hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="c2d53-165">Palvelun päätepiste</span><span class="sxs-lookup"><span data-stu-id="c2d53-165">Service endpoint</span></span>

<span data-ttu-id="c2d53-166">Palvelun päätepiste on URL-osoite, jossa sähköisen laskutuksen lisäosa sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="c2d53-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="c2d53-167">Ennen kuin sähköisiä laskuja voidaan lähettää palvelun päätepiste pitää määrittää Financessa ja Supply Chain Managementissa niin, että se sallii viestinnän palvelun kanssa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="c2d53-168">Voit määrittää palvelun päätepisteen siirtymällä kohtaan **Organisaation hallinto \> Määritys \> Sähköisen asiakirjan parametri** ja kirjoita **Lähetyspalvelut**-välilehden **Sähköisen laskutuksen lisäosan URL-osoite** -kenttään URL-osoite, kuten on kuvattu osan **Palvelun päätepiste** -osan taulukossa.</span><span class="sxs-lookup"><span data-stu-id="c2d53-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="c2d53-169">Ympäristöt</span><span class="sxs-lookup"><span data-stu-id="c2d53-169">Environments</span></span>

<span data-ttu-id="c2d53-170">Financeen ja Supply Chain Managementiin syötetty ympäristönimi viittaa RCS:ssä luotavaan ja sähköiseen laskutukseen lisäosaan julkaistavaan ympäristön nimeen.</span><span class="sxs-lookup"><span data-stu-id="c2d53-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="c2d53-171">Ympäristö on konfiguroitava **Sähköisen tiedoston parametri** -sivun **Lähetyspalvelut**-välilehdessä, jotta kaikki sähköisten laskujen lähetyspyynnöt sisältävät ympäristön, jossa sähköisen laskutuksen lisäosa voi määrittää, mikä sähköisen laskutuksen toiminto käsittelee pyynnön.</span><span class="sxs-lookup"><span data-stu-id="c2d53-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2d53-172">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c2d53-172">Additional resources</span></span>

- [<span data-ttu-id="c2d53-173">Konfiguroi sähköiset laskut RCS:ssä</span><span class="sxs-lookup"><span data-stu-id="c2d53-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="c2d53-174">Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="c2d53-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
