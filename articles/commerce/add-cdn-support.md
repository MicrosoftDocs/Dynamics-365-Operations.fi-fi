---
title: Sisältöverkon (CDN) tuen lisääminen
description: Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582716"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="3c740-103">Sisällön toimitusverkoston (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="3c740-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c740-104">Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="3c740-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="3c740-105">Kun määrität Dynamics 365 Commerce -sovelluksessa sähköisen kaupankäynnin ympäristöä, voit määrittää sen käyttämään CDN-palvelua.</span><span class="sxs-lookup"><span data-stu-id="3c740-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="3c740-106">Mukautettu toimialue voi olla käytössä sähköisen kaupankäynnin ympäristön valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="3c740-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="3c740-107">Vaihtoehtoisesti voit käyttää palvelupyyntöä määrittämiseen valmisteluprosessin päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="3c740-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="3c740-108">Sähköisen kaupankäynnin ympäristön valmisteluprosessi luo isäntänimen, joka liittyy ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="3c740-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="3c740-109">Tällä isäntänimellä on seuraava muoto, jossa \<*e-commerce-tenant-name*\> on ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="3c740-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="3c740-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="3c740-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="3c740-111">Isäntänimi tai päätepiste, joka luodaan valmisteluprosessin aikana, tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="3c740-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="3c740-112">Se ei tue SSL-varmennetta mukautetuissa toimialueissa.</span><span class="sxs-lookup"><span data-stu-id="3c740-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="3c740-113">Tämän vuoksi SSL on päätettävä CDN:n mukautetuissa toimialueissa ja ohjattava liikenne CDN:stä isäntänimelle tai päätepisteelle, jonka Commerce on luonut.</span><span class="sxs-lookup"><span data-stu-id="3c740-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="3c740-114">Lisäksi Commerce-sovelluksen *tilastot* (JavaScript- tai Cascading Style Sheets \[CSS\] -tiedostot) saadaan Commercen luomasta päätepisteestä (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="3c740-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="3c740-115">Tilastot voidaan tallentaa välimuistiin vain, jos Commercen luoma isäntänimi tai päätepiste sijoitetaan CDN:n jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3c740-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="3c740-116">Määritä SSL</span><span class="sxs-lookup"><span data-stu-id="3c740-116">Set up SSL</span></span>

<span data-ttu-id="3c740-117">Jos haluat varmistaa, että SSL on määritetty ja että tilastot tallennetaan välimuistiin, määritä CDN niin, että se liittyy isäntänimeen, jonka Commerce on luonut ympäristöä varten.</span><span class="sxs-lookup"><span data-stu-id="3c740-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="3c740-118">Myös seuraava muoto on tallennettava välimuistiin tilastoja varten:</span><span class="sxs-lookup"><span data-stu-id="3c740-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="3c740-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="3c740-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="3c740-120">Kun Commerce-ympäristö on valmisteltu annetun mukautetun toimialueen avulla tai kun ympäristön mukautettu toimialue on annettu palvelupyynnön avulla, osoita mukautettu toimialue isäntänimelle tai päätepisteelle, jonka Commerce on luonut.</span><span class="sxs-lookup"><span data-stu-id="3c740-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="3c740-121">Kuten aiemmin mainittiin, luotu isäntänimi tai päätepiste tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="3c740-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="3c740-122">Se ei tue SSL-varmennetta mukautetuissa toimialueissa.</span><span class="sxs-lookup"><span data-stu-id="3c740-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="3c740-123">CDN-palvelut</span><span class="sxs-lookup"><span data-stu-id="3c740-123">CDN services</span></span>

<span data-ttu-id="3c740-124">Commerce-ympäristössä voi käyttää mitä tahansa CDN-palvelua.</span><span class="sxs-lookup"><span data-stu-id="3c740-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="3c740-125">Seuraavassa on kaksi esimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="3c740-125">Here are two examples:</span></span>

- <span data-ttu-id="3c740-126">**Microsoft Azure Front Door Service** – Azuren CDN-ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="3c740-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="3c740-127">Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Azure Front Door Service -dokumentaatio](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="3c740-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="3c740-128">**Akamai Dynamic Site Accelerator** – Lisätietoja on kohdassa [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="3c740-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="3c740-129">CDN-asetukset</span><span class="sxs-lookup"><span data-stu-id="3c740-129">CDN setup</span></span>

<span data-ttu-id="3c740-130">CDN-määritysprosessi koostuu seuraavista yleisistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="3c740-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="3c740-131">Lisää edustaisäntä.</span><span class="sxs-lookup"><span data-stu-id="3c740-131">Add a front-end host.</span></span>
1. <span data-ttu-id="3c740-132">Määritä taustapooli.</span><span class="sxs-lookup"><span data-stu-id="3c740-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="3c740-133">Määritä reitityksen ja välimuistiin tallennuksen säännöt.</span><span class="sxs-lookup"><span data-stu-id="3c740-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="3c740-134">Lisää edustaisäntä</span><span class="sxs-lookup"><span data-stu-id="3c740-134">Add a front-end host</span></span>

<span data-ttu-id="3c740-135">Mitä tahansa CDN-palvelua voi käyttää. Tämän ohjeaiheen esimerkissä käytetään Azure Front Door Service -palvelua.</span><span class="sxs-lookup"><span data-stu-id="3c740-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="3c740-136">Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Pika-aloitus: Luo Front Door erittäin käytettävissä olevalle yleiselle verkkosovellukselle](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="3c740-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="3c740-137">Azure Front Door Service -palvelun taustapooli</span><span class="sxs-lookup"><span data-stu-id="3c740-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="3c740-138">Voit määrittää Azure Front Door Service -palvelun taustapoolin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3c740-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="3c740-139">Lisää **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** taustapooliin mukautettuna isäntänä, jolla on tyhjä taustan isännän otsikko.</span><span class="sxs-lookup"><span data-stu-id="3c740-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="3c740-140">Jätä **Kuormituksen tasaus** -kohtaan oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="3c740-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="3c740-141">Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa sekä annettu taustan isäntänimi.</span><span class="sxs-lookup"><span data-stu-id="3c740-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Taustapooli-valintaikkunan lisääminen](./media/CDN_BackendPool.png)

<span data-ttu-id="3c740-143">Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa sekä kuormituksen tasauksen oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="3c740-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Taustapooli-valintaikkunan lisääminen, jatkuu](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="3c740-145">Sääntöjen määrittäminen Azure Front Door Service -palvelussa</span><span class="sxs-lookup"><span data-stu-id="3c740-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="3c740-146">Määritä reitityssääntö Azure Front Door Service -palvelussa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3c740-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="3c740-147">Lisää reitityssääntö.</span><span class="sxs-lookup"><span data-stu-id="3c740-147">Add a routing rule.</span></span>
1. <span data-ttu-id="3c740-148">Kirjoita **Nimi**-kenttään **oletus**.</span><span class="sxs-lookup"><span data-stu-id="3c740-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="3c740-149">Valitse **Hyväksytty protokolla** -kentässä **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="3c740-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="3c740-150">Syötä **Edustaisännät**-kenttään **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="3c740-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="3c740-151">Syötä ylempään **Kohdistettavat mallit** -kenttään **/\***.</span><span class="sxs-lookup"><span data-stu-id="3c740-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="3c740-152">Määritä **Reitin tiedot** -kohdan **Reitin tyyppi** -vaihtoehdon arvoksi **Välitä edelleen**.</span><span class="sxs-lookup"><span data-stu-id="3c740-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="3c740-153">Valitse **Taustapooli**-kentässä **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="3c740-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="3c740-154">Valitse **Välitysprotokolla**-kenttäryhmässä **Pyynnön vastaavuus** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="3c740-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="3c740-155">Määritä **URL-osoitteen uudelleenkirjoitus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="3c740-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="3c740-156">Määritä **Välimuistiin tallennus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="3c740-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="3c740-157">Määritä välimuistiin tallennuksen sääntö Azure Front Door Service -palvelussa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3c740-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="3c740-158">Lisää välimuistiin tallennuksen sääntö.</span><span class="sxs-lookup"><span data-stu-id="3c740-158">Add a caching rule.</span></span>
1. <span data-ttu-id="3c740-159">Kirjoita **Nimi**-kenttään **tilastot**.</span><span class="sxs-lookup"><span data-stu-id="3c740-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="3c740-160">Valitse **Hyväksytty protokolla** -kentässä **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="3c740-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="3c740-161">Syötä **Edustaisännät**-kenttään **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="3c740-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="3c740-162">Syötä ylempään **Kohdistettavat mallit** -kenttään **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="3c740-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="3c740-163">Määritä **Reitin tiedot** -kohdan **Reitin tyyppi** -vaihtoehdon arvoksi **Välitä edelleen**.</span><span class="sxs-lookup"><span data-stu-id="3c740-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="3c740-164">Valitse **Taustapooli**-kentässä **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="3c740-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="3c740-165">Valitse **Välitysprotokolla**-kenttäryhmässä **Pyynnön vastaavuus** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="3c740-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="3c740-166">Määritä **URL-osoitteen uudelleenkirjoitus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="3c740-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="3c740-167">Määritä **Välimuistiin tallennus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="3c740-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="3c740-168">Valitse **Kyselymerkkijonon välimuistiin tallennuksen toiminta** -kentässä **Tallenna jokainen yksilöllinen URL-osoite välimuistiin**.</span><span class="sxs-lookup"><span data-stu-id="3c740-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="3c740-169">Valitse **Dynaaminen pakkaus** -kenttäryhmässä **Käytössä**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="3c740-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="3c740-170">Seuraavassa kuvassa näkyy **Lisää sääntö** -valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="3c740-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Lisää sääntö -valintaikkuna](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="3c740-172">Jos käytettävä toimialue on jo aktiivinen ja julkaistu, luo tukipalvelupyyntö **Tuki**-ruudussa [Microsoft Dynamics Lifecycle Services -sovelluksessa](https://lcs.dynamics.com/). Näin saat apua seuraavissa vaiheissa.</span><span class="sxs-lookup"><span data-stu-id="3c740-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="3c740-173">Lisätietoja on kohdassa [Tuen pyytäminen Finance and Operations -sovelluksia tai Lifecycle Services (LCS) -sovellusta varten](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="3c740-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="3c740-174">Jos toimialueesi on uusi, eikä se ole aiemmin määritetty julkaistu toimialue, voit lisätä mukautetun toimialueen määritykseen Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="3c740-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="3c740-175">Tämän jälkeen verkkoliikenne voi ohjata sivuston Azure Front Door -ilmentymän kautta.</span><span class="sxs-lookup"><span data-stu-id="3c740-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="3c740-176">Jos haluat lisätä mukautetun toimialueen (esimerkiksi `www.fabrikam.com`), määritä toimialueelle kanoninen nimi (CNAME).</span><span class="sxs-lookup"><span data-stu-id="3c740-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="3c740-177">Seuraavassa kuvassa näkyy **CNAME-määritys**-valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="3c740-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME-määritys-valintaikkuna](./media/CNAME_Configuration.png)

<span data-ttu-id="3c740-179">Voit käyttää Azure Front Door Service -palvelua varmenteen hallinnassa tai voit käyttää omaa varmennetta mukautetussa toimialueessa.</span><span class="sxs-lookup"><span data-stu-id="3c740-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="3c740-180">Seuraavassa kuvassa näkyy **Mukautetun toimialueen HTTPS**-valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="3c740-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Mukautetun toimialueen HTTPS -valintaikkuna](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="3c740-182">Lisätietoja mukautetun toimialueen lisäämisestä Azure Front Door -palveluun on kohdassa [Mukautetun toimialueen lisääminen Front Door -palveluun](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="3c740-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="3c740-183">CDN:n tulisi nyt olla määritetty niin, että sitä voi käyttää Commerce-sivuston kanssa.</span><span class="sxs-lookup"><span data-stu-id="3c740-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c740-184">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3c740-184">Additional resources</span></span>

[<span data-ttu-id="3c740-185">Sisällön toimitusverkoston käyttöönottoasetukset</span><span class="sxs-lookup"><span data-stu-id="3c740-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
