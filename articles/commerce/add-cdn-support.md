---
title: Sisältöverkon (CDN) tuen lisääminen
description: Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001619"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="5dabe-103">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="5dabe-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5dabe-104">Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="5dabe-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="5dabe-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5dabe-105">Overview</span></span>

<span data-ttu-id="5dabe-106">Kun määrität Dynamics 365 Commerce -sovelluksessa sähköisen kaupankäynnin ympäristön, voit määrittää sen käyttämään CDN-palvelua.</span><span class="sxs-lookup"><span data-stu-id="5dabe-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="5dabe-107">Mukautettu toimialue voi olla käytössä sähköisen kaupankäynnin ympäristön valmisteluprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="5dabe-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="5dabe-108">Vaihtoehtoisesti voit käyttää palvelupyyntöä määrittämiseen valmisteluprosessin päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="5dabe-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="5dabe-109">Sähköisen kaupankäynnin ympäristön valmisteluprosessi luo isäntänimen, joka liittyy ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="5dabe-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="5dabe-110">Tällä isäntänimellä on seuraava muoto, jossa *e-commerce-tenant-name* on ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="5dabe-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="5dabe-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="5dabe-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="5dabe-112">Isäntänimi tai päätepiste, joka luodaan valmisteluprosessin aikana, tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="5dabe-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="5dabe-113">Se ei tue SSL-varmennetta mukautetuissa toimialueissa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="5dabe-114">Tämän vuoksi SSL on päätettävä CDN:n mukautetuissa toimialueissa ja ohjattava liikenne CDN:stä isäntänimelle tai päätepisteelle, jonka Commerce on luonut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="5dabe-115">Lisäksi Commerce-sovelluksen *tilastot* (JavaScript- tai Cascading Style Sheets \[CSS\] -tiedostot) saadaan Commercen luomasta päätepisteestä (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="5dabe-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="5dabe-116">Tilastot voidaan tallentaa välimuistiin vain, jos Commercen luoma isäntänimi tai päätepiste sijoitetaan CDN:n jälkeen.</span><span class="sxs-lookup"><span data-stu-id="5dabe-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="5dabe-117">Määritä SSL</span><span class="sxs-lookup"><span data-stu-id="5dabe-117">Set up SSL</span></span>

<span data-ttu-id="5dabe-118">Jos haluat varmistaa, että SSL on määritetty ja että tilastot tallennetaan välimuistiin, määritä CDN niin, että se liittyy isäntänimeen, jonka Commerce on luonut ympäristöä varten.</span><span class="sxs-lookup"><span data-stu-id="5dabe-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="5dabe-119">Myös seuraava muoto on tallennettava välimuistiin tilastoja varten:</span><span class="sxs-lookup"><span data-stu-id="5dabe-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="5dabe-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="5dabe-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="5dabe-121">Kun Commerce-ympäristö on valmisteltu annetun mukautetun toimialueen avulla tai kun ympäristön mukautettu toimialue on annettu palvelupyynnön avulla, osoita mukautettu toimialue isäntänimelle tai päätepisteelle, jonka Commerce on luonut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="5dabe-122">Kuten aiemmin mainittiin, luotu isäntänimi tai päätepiste tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="5dabe-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="5dabe-123">Se ei tue SSL-varmennetta mukautetuissa toimialueissa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="5dabe-124">CDN-palvelut</span><span class="sxs-lookup"><span data-stu-id="5dabe-124">CDN services</span></span>

<span data-ttu-id="5dabe-125">Commerce-ympäristössä voi käyttää mitä tahansa CDN-palvelua.</span><span class="sxs-lookup"><span data-stu-id="5dabe-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="5dabe-126">Seuraavassa on kaksi esimerkkiä:</span><span class="sxs-lookup"><span data-stu-id="5dabe-126">Here are two examples:</span></span>

- <span data-ttu-id="5dabe-127">**Microsoft Azure Front Door Service** – Azuren CDN-ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="5dabe-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="5dabe-128">Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Azure Front Door Service -dokumentaatio](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="5dabe-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="5dabe-129">**Akamai Dynamic Site Accelerator** – Lisätietoja on kohdassa [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="5dabe-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="5dabe-130">CDN-asetukset</span><span class="sxs-lookup"><span data-stu-id="5dabe-130">CDN setup</span></span>

<span data-ttu-id="5dabe-131">CDN-määritysprosessi koostuu seuraavista yleisistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="5dabe-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="5dabe-132">Lisää edustaisäntä.</span><span class="sxs-lookup"><span data-stu-id="5dabe-132">Add a front-end host.</span></span>
1. <span data-ttu-id="5dabe-133">Määritä taustapooli.</span><span class="sxs-lookup"><span data-stu-id="5dabe-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="5dabe-134">Määritä reitityksen ja välimuistiin tallennuksen säännöt.</span><span class="sxs-lookup"><span data-stu-id="5dabe-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="5dabe-135">Lisää edustaisäntä</span><span class="sxs-lookup"><span data-stu-id="5dabe-135">Add a front-end host</span></span>

<span data-ttu-id="5dabe-136">Mitä tahansa CDN-palvelua voi käyttää. Tämän ohjeaiheen esimerkissä käytetään Azure Front Door Service -palvelua.</span><span class="sxs-lookup"><span data-stu-id="5dabe-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="5dabe-137">Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Pika-aloitus: Luo Front Door erittäin käytettävissä olevalle yleiselle verkkosovellukselle](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="5dabe-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="5dabe-138">Azure Front Door Service -palvelun taustapooli</span><span class="sxs-lookup"><span data-stu-id="5dabe-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="5dabe-139">Voit määrittää Azure Front Door Service -palvelun taustapoolin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5dabe-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="5dabe-140">Lisää **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** taustapooliin mukautettuna isäntänä, jolla on tyhjä taustan isännän otsikko.</span><span class="sxs-lookup"><span data-stu-id="5dabe-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="5dabe-141">Syötä **Kuntotutkimukset**-kohdan **Polku**-kenttään **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="5dabe-142">Kirjoita **Aikavälit (sekunteina)** -kenttään **255**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="5dabe-143">Jätä **Kuormituksen tasaus** -kohtaan oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="5dabe-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="5dabe-144">Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Taustapooli-valintaikkunan lisääminen](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="5dabe-146">Sääntöjen määrittäminen Azure Front Door Service -palvelussa</span><span class="sxs-lookup"><span data-stu-id="5dabe-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="5dabe-147">Määritä reitityssääntö Azure Front Door Service -palvelussa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5dabe-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="5dabe-148">Lisää reitityssääntö.</span><span class="sxs-lookup"><span data-stu-id="5dabe-148">Add a routing rule.</span></span>
1. <span data-ttu-id="5dabe-149">Kirjoita **Nimi**-kenttään **oletus**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="5dabe-150">Valitse **Hyväksytty protokolla** -kentässä **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="5dabe-151">Syötä **Edustaisännät**-kenttään **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="5dabe-152">Syötä ylempään **Kohdistettavat mallit** -kenttään **/\***.</span><span class="sxs-lookup"><span data-stu-id="5dabe-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="5dabe-153">Määritä **Reitin tiedot** -kohdan **Reitin tyyppi** -vaihtoehdon arvoksi **Välitä edelleen**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="5dabe-154">Valitse **Taustapooli**-kentässä **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="5dabe-155">Valitse **Välitysprotokolla**-kenttäryhmässä **Pyynnön vastaavuus** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="5dabe-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="5dabe-156">Määritä **URL-osoitteen uudelleenkirjoitus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="5dabe-157">Määritä **Välimuistiin tallennus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="5dabe-158">Määritä välimuistiin tallennuksen sääntö Azure Front Door Service -palvelussa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5dabe-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="5dabe-159">Lisää välimuistiin tallennuksen sääntö.</span><span class="sxs-lookup"><span data-stu-id="5dabe-159">Add a caching rule.</span></span>
1. <span data-ttu-id="5dabe-160">Kirjoita **Nimi**-kenttään **tilastot**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="5dabe-161">Valitse **Hyväksytty protokolla** -kentässä **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="5dabe-162">Syötä **Edustaisännät**-kenttään **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="5dabe-163">Syötä ylempään **Kohdistettavat mallit** -kenttään **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="5dabe-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="5dabe-164">Määritä **Reitin tiedot** -kohdan **Reitin tyyppi** -vaihtoehdon arvoksi **Välitä edelleen**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="5dabe-165">Valitse **Taustapooli**-kentässä **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="5dabe-166">Valitse **Välitysprotokolla**-kenttäryhmässä **Pyynnön vastaavuus** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="5dabe-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="5dabe-167">Määritä **URL-osoitteen uudelleenkirjoitus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="5dabe-168">Määritä **Välimuistiin tallennus** -vaihtoehdon arvoksi **Poistettu käytöstä**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="5dabe-169">Valitse **Kyselymerkkijonon välimuistiin tallennuksen toiminta** -kentässä **Tallenna jokainen yksilöllinen URL-osoite välimuistiin**.</span><span class="sxs-lookup"><span data-stu-id="5dabe-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="5dabe-170">Valitse **Dynaaminen pakkaus** -kenttäryhmässä **Käytössä**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="5dabe-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="5dabe-171">Seuraavassa kuvassa näkyy **Lisää sääntö** -valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Lisää sääntö -valintaikkuna](./media/CDN_CachingRule.png)

<span data-ttu-id="5dabe-173">Kun tämä ensimmäinen määritys on otettu käyttöön, lisää mukautettu toimialue Azure Front Door Service -palvelun määritykseen.</span><span class="sxs-lookup"><span data-stu-id="5dabe-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="5dabe-174">Jos haluat lisätä mukautetun toimialueen (esimerkiksi `www.fabrikam.com`), määritä toimialueelle kanoninen nimi (CNAME).</span><span class="sxs-lookup"><span data-stu-id="5dabe-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="5dabe-175">Seuraavassa kuvassa näkyy **CNAME-määritys**-valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME-määritys-valintaikkuna](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="5dabe-177">Jos käyttämäsi toimialue on jo aktiivinen ja julkaistu, ota yhteyttä tukeen, jotta tämä toimialue otetaan käyttöön Azure Front Door Service -palvelun kanssa testin määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="5dabe-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="5dabe-178">Voit käyttää Azure Front Door Service -palvelua varmenteen hallinnassa tai voit käyttää omaa varmennetta mukautetussa toimialueessa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="5dabe-179">Seuraavassa kuvassa näkyy **Mukautetun toimialueen HTTPS**-valintaikkuna Azure Front Door Service -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Mukautetun toimialueen HTTPS -valintaikkuna](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="5dabe-181">CDN:n tulisi nyt olla määritetty niin, että sitä voi käyttää Commerce-sivuston kanssa.</span><span class="sxs-lookup"><span data-stu-id="5dabe-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5dabe-182">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5dabe-182">Additional resources</span></span>

[<span data-ttu-id="5dabe-183">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5dabe-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5dabe-184">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="5dabe-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="5dabe-185">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="5dabe-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5dabe-186">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="5dabe-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5dabe-187">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="5dabe-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="5dabe-188">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="5dabe-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5dabe-189">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="5dabe-189">Enable location-based store detection</span></span>](enable-store-detection.md)
