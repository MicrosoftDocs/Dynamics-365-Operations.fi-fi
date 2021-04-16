---
title: Sisältöverkon (CDN) tuen lisääminen
description: Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a56f675b1fb43160625101a067c74e9fcf4f714a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797836"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="9b195-103">Sisällön toimitusverkoston (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="9b195-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9b195-104">Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="9b195-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="9b195-105">Kun määrität Dynamics 365 Commerce -sovelluksessa sähköisen kaupankäynnin ympäristöä, voit määrittää sen käyttämään CDN-palvelua.</span><span class="sxs-lookup"><span data-stu-id="9b195-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="9b195-106">Mukautettu toimialue voi olla käytössä sähköisen kaupankäynnin ympäristön valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="9b195-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="9b195-107">Vaihtoehtoisesti voit käyttää palvelupyyntöä määrittämiseen valmisteluprosessin päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="9b195-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="9b195-108">Sähköisen kaupankäynnin ympäristön valmisteluprosessi luo isäntänimen, joka liittyy ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="9b195-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="9b195-109">Tällä isäntänimellä on seuraava muoto, jossa \<*e-commerce-tenant-name*\> on ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="9b195-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="9b195-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="9b195-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="9b195-111">Isäntänimi tai päätepiste, joka luodaan valmisteluprosessin aikana, tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9b195-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9b195-112">Se ei tue SSL-varmennetta mukautetuissa toimialueissa.</span><span class="sxs-lookup"><span data-stu-id="9b195-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="9b195-113">Tämän vuoksi SSL on päätettävä CDN:n mukautetuissa toimialueissa ja ohjattava liikenne CDN:stä isäntänimelle tai päätepisteelle, jonka Commerce on luonut.</span><span class="sxs-lookup"><span data-stu-id="9b195-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="9b195-114">Lisäksi Commerce-sovelluksen *tilastot* (JavaScript- tai Cascading Style Sheets \[CSS\] -tiedostot) saadaan Commercen luomasta päätepisteestä (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9b195-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="9b195-115">Tilastot voidaan tallentaa välimuistiin vain, jos Commercen luoma isäntänimi tai päätepiste sijoitetaan CDN:n jälkeen.</span><span class="sxs-lookup"><span data-stu-id="9b195-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="9b195-116">Määritä SSL</span><span class="sxs-lookup"><span data-stu-id="9b195-116">Set up SSL</span></span>

<span data-ttu-id="9b195-117">Kun Commerce-ympäristö on valmisteltu annetun mukautetun toimialueen avulla tai kun ympäristön mukautettu toimialue on annettu palvelupyynnön avulla, DNS-muutokset pitää suunnitella Commerce-perehdytystiimin kanssa.</span><span class="sxs-lookup"><span data-stu-id="9b195-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="9b195-118">Kuten aiemmin mainittiin, luotu isäntänimi tai päätepiste tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9b195-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9b195-119">Se ei tue SSL-varmennetta mukautetuissa toimialueissa.</span><span class="sxs-lookup"><span data-stu-id="9b195-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="9b195-120">CDN-palvelut</span><span class="sxs-lookup"><span data-stu-id="9b195-120">CDN services</span></span>

<span data-ttu-id="9b195-121">Commerce-ympäristössä voi käyttää mitä tahansa CDN-palvelua.</span><span class="sxs-lookup"><span data-stu-id="9b195-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="9b195-122">Seuraavassa on kaksi esimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="9b195-122">Here are two examples:</span></span>

- <span data-ttu-id="9b195-123">**Microsoft Azure Front Door Service** – Azuren CDN-ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="9b195-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="9b195-124">Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Azure Front Door Service -dokumentaatio](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="9b195-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="9b195-125">**Akamai Dynamic Site Accelerator** – Lisätietoja on kohdassa [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="9b195-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="9b195-126">CDN-asetukset</span><span class="sxs-lookup"><span data-stu-id="9b195-126">CDN setup</span></span>

<span data-ttu-id="9b195-127">CDN-määritysprosessi koostuu seuraavista yleisistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="9b195-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="9b195-128">Lisää edustaisäntä.</span><span class="sxs-lookup"><span data-stu-id="9b195-128">Add a front-end host.</span></span>
1. <span data-ttu-id="9b195-129">Määritä taustapooli.</span><span class="sxs-lookup"><span data-stu-id="9b195-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="9b195-130">Määritä reitityssäännöt.</span><span class="sxs-lookup"><span data-stu-id="9b195-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="9b195-131">Lisää edustaisäntä</span><span class="sxs-lookup"><span data-stu-id="9b195-131">Add a front-end host</span></span>

<span data-ttu-id="9b195-132">Mitä tahansa CDN-palvelua voi käyttää. Tämän ohjeaiheen esimerkissä käytetään Azure Front Door Service -palvelua.</span><span class="sxs-lookup"><span data-stu-id="9b195-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="9b195-133">Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Pika-aloitus: Luo Front Door erittäin käytettävissä olevalle yleiselle verkkosovellukselle](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="9b195-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="9b195-134">Azure Front Door Service -palvelun taustapooli</span><span class="sxs-lookup"><span data-stu-id="9b195-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="9b195-135">Voit määrittää Azure Front Door Service -palvelun taustapoolin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9b195-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9b195-136">Lisää **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** taustapooliin mukautettuna isäntäkoneena, jolla on taustakoneen otsikko, joka on sama kuin **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="9b195-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="9b195-137">Jätä **Kuormituksen tasaus** -kohtaan oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="9b195-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="9b195-138">Poista taustapoolin kunnon tarkistukset käytöstä.</span><span class="sxs-lookup"><span data-stu-id="9b195-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="9b195-139">Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa sekä annettu taustan isäntänimi.</span><span class="sxs-lookup"><span data-stu-id="9b195-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Taustapooli-valintaikkunan lisääminen](./media/CDN_BackendPool.png)

<span data-ttu-id="9b195-141">Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa sekä kuormituksen tasauksen oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="9b195-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Taustapooli-valintaikkunan lisääminen, jatkuu](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="9b195-143">Varmista, että poistat **Kuntotutukimukset**, kun määrität omaa Azure Front Door -palvelua Commercelle.</span><span class="sxs-lookup"><span data-stu-id="9b195-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="9b195-144">Sääntöjen määrittäminen Azure Front Door Service -palvelussa</span><span class="sxs-lookup"><span data-stu-id="9b195-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="9b195-145">Määritä reitityssääntö Azure Front Door Service -palvelussa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9b195-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9b195-146">Lisää reitityssääntö.</span><span class="sxs-lookup"><span data-stu-id="9b195-146">Add a routing rule.</span></span>
1. <span data-ttu-id="9b195-147">Kirjoita **Nimi**-kenttään **oletus**.</span><span class="sxs-lookup"><span data-stu-id="9b195-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="9b195-148">Valitse **Hyväksytty protokolla** -kentässä **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="9b195-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="9b195-149">Syötä **Edustaisännät**-kenttään **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="9b195-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="9b195-150">Syötä ylempään **Kohdistettavat mallit** -kenttään **/\***.</span><span class="sxs-lookup"><span data-stu-id="9b195-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="9b195-151">Määritä **Reitin tiedot** -kohdan **Reitin tyyppi** -vaihtoehdon arvoksi **Välitä edelleen**.</span><span class="sxs-lookup"><span data-stu-id="9b195-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="9b195-152">Valitse **Taustapooli**-kentässä **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="9b195-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="9b195-153">Valitse **Välitysprotokolla**-kenttäryhmässä **Pyynnön vastaavuus** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="9b195-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="9b195-154">Määritä **URL-osoitteen uudelleenkirjoitus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="9b195-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="9b195-155">Määritä **Välimuistiin tallennus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="9b195-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="9b195-156">Jos käytettävä toimialue on jo aktiivinen ja julkaistu, luo tukipalvelupyyntö **Tuki**-ruudussa [Microsoft Dynamics Lifecycle Services -sovelluksessa](https://lcs.dynamics.com/). Näin saat apua seuraavissa vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="9b195-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="9b195-157">Lisätietoja on kohdassa [Tuen pyytäminen Finance and Operations -sovelluksia tai Lifecycle Services (LCS) -sovellusta varten](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="9b195-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="9b195-158">Jos toimialueesi on uusi, eikä se ole aiemmin määritetty julkaistu toimialue, voit lisätä mukautetun toimialueen määritykseen Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="9b195-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="9b195-159">Tämän jälkeen verkkoliikenne voi ohjata sivuston Azure Front Door -ilmentymän kautta.</span><span class="sxs-lookup"><span data-stu-id="9b195-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="9b195-160">Jos haluat lisätä mukautetun toimialueen (esimerkiksi `www.fabrikam.com`), määritä toimialueelle kanoninen nimi (CNAME).</span><span class="sxs-lookup"><span data-stu-id="9b195-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="9b195-161">Seuraavassa kuvassa näkyy **CNAME-määritys**-valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="9b195-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME-määritys-valintaikkuna](./media/CNAME_Configuration.png)

<span data-ttu-id="9b195-163">Voit käyttää Azure Front Door Service -palvelua varmenteen hallinnassa tai voit käyttää omaa varmennetta mukautetussa toimialueessa.</span><span class="sxs-lookup"><span data-stu-id="9b195-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="9b195-164">Seuraavassa kuvassa näkyy **Mukautetun toimialueen HTTPS**-valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="9b195-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Mukautetun toimialueen HTTPS -valintaikkuna](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="9b195-166">Lisätietoja mukautetun toimialueen lisäämisestä Azure Front Door -palveluun on kohdassa [Mukautetun toimialueen lisääminen Front Door -palveluun](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="9b195-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="9b195-167">CDN:n tulisi nyt olla määritetty niin, että sitä voi käyttää Commerce-sivuston kanssa.</span><span class="sxs-lookup"><span data-stu-id="9b195-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b195-168">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9b195-168">Additional resources</span></span>

[<span data-ttu-id="9b195-169">Sisällön toimitusverkoston käyttöönottoasetukset</span><span class="sxs-lookup"><span data-stu-id="9b195-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
