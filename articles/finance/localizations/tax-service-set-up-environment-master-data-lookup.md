---
title: Ympäristön määrittäminen päätietojen hakua varten
description: Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e4aa941c57e8c31793d6db8ae87140cd1bb1a82b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021341"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="03cf2-103">Ympäristön määrittäminen päätietojen hakua varten</span><span class="sxs-lookup"><span data-stu-id="03cf2-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03cf2-104">Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="03cf2-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="03cf2-105">Määritä power platformin integraatio Lifecycle Services (LCS) -palveluissa.</span><span class="sxs-lookup"><span data-stu-id="03cf2-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="03cf2-106">Lisätietoja on kohdassa [Microsoft Power Platform -apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="03cf2-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="03cf2-107">Määritä Dynamics 365 Finance ja Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="03cf2-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="03cf2-108">Lisätietoja on kohdassa [Ratkaisun saaminen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ja [todennus ja hyväksyntä](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="03cf2-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="03cf2-109">Määritä seuraavat yksiköt.</span><span class="sxs-lookup"><span data-stu-id="03cf2-109">Set up the following entities.</span></span> <span data-ttu-id="03cf2-110">Lisätietoja on kohdassa [Virtuaaliyksiköiden käyttöönotto](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="03cf2-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="03cf2-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="03cf2-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-112">CurrencyEntity</span></span>
      - <span data-ttu-id="03cf2-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="03cf2-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="03cf2-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="03cf2-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="03cf2-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="03cf2-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="03cf2-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="03cf2-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="03cf2-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="03cf2-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="03cf2-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="03cf2-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="03cf2-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="03cf2-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="03cf2-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="03cf2-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="03cf2-125">Määritä Dynamics 365 Regulatory Configuration Service (RCS) -palvelu.</span><span class="sxs-lookup"><span data-stu-id="03cf2-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="03cf2-126">Luo Microsoftille palvelupyyntö, jonka avulla voidaan ottaa käyttöön seuraavien ominaisuuksien lento:</span><span class="sxs-lookup"><span data-stu-id="03cf2-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="03cf2-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="03cf2-127">ERCdsFeature</span></span>
      - <span data-ttu-id="03cf2-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="03cf2-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="03cf2-129">Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="03cf2-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="03cf2-130">(Esiversio) Sähköisen raportoinnin Dataverse -tietolähteet tukevat</span><span class="sxs-lookup"><span data-stu-id="03cf2-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="03cf2-131">(Esiversio) Veropalvelun Dataverse-tietolähteiden tuki</span><span class="sxs-lookup"><span data-stu-id="03cf2-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="03cf2-132">(Esiversio) Globalisaatio-ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="03cf2-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="03cf2-133">Kirjaudu RCS-malliin vuokraajatiliä käyttäen.</span><span class="sxs-lookup"><span data-stu-id="03cf2-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="03cf2-134">Siirry kohtaan **sähköinen raportointi** > **Liittyvät sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="03cf2-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="03cf2-135">Lisää tietue valitsemalla **Uusi** ja lisää seuraavat kenttätiedot.</span><span class="sxs-lookup"><span data-stu-id="03cf2-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="03cf2-136">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="03cf2-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="03cf2-137">Valitse **Tyyppi**-kentässä **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="03cf2-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="03cf2-138">Kirjoita **Sovellus**-kenttään Dataverse-URL-osoitteesi.</span><span class="sxs-lookup"><span data-stu-id="03cf2-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="03cf2-139">Kirjoita **Vuokraaja**-kenttään vuokraajasi.</span><span class="sxs-lookup"><span data-stu-id="03cf2-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="03cf2-140">Kirjoita **Mukautetun URL-osoitteen** kenttään Dataverse-URL-osoite ja liitä siihen teksti "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="03cf2-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="03cf2-141">Valitse **Tarkista yhteys** ja viimeistele yhteysprosessi.</span><span class="sxs-lookup"><span data-stu-id="03cf2-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="03cf2-142">[![Tarkista yhteys -painike](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="03cf2-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="03cf2-143">Siirry kohtaan **sähköinen raportointi** > **Verokonfiguraatiot** ja tuo verokonfiguraatiot kohteesta [Vero-konfiguraatiot](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="03cf2-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="03cf2-144">[![Verokonfiguraatiot-sivu, Verotietomallipuu](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="03cf2-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="03cf2-145">Siirry **verotettavaan tiedostomallin määritykseen** tai **Dataverse-mallimääritykseen**, jos käytät Microsoft-konfiguraatiota, ja valitse **Yhteydessä oleva sovellus** -kentästä tietue, jonka loit vaiheessa 7.</span><span class="sxs-lookup"><span data-stu-id="03cf2-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="03cf2-146">Määritä **Mallin yhdistämisasetuksen oletusarvoksi** **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="03cf2-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="03cf2-147">[![Mallimäärityksen sivu](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="03cf2-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
