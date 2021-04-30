---
title: Ympäristön määrittäminen päätietojen hakua varten
description: Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869061"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="4c9a1-103">Ympäristön määrittäminen päätietojen hakua varten</span><span class="sxs-lookup"><span data-stu-id="4c9a1-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="4c9a1-104">Tässä aiheessa kerrotaan, miten ympäristö määritetään käyttämään veron laskennan perustietojen hakutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="4c9a1-105">Määritä power platformin integraatio Lifecycle Services (LCS) -palveluissa.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="4c9a1-106">Lisätietoja on kohdassa [Microsoft Power Platform -apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4c9a1-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="4c9a1-107">Määritä Dynamics 365 Finance ja Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="4c9a1-108">Lisätietoja on kohdassa [Ratkaisun saaminen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ja [todennus ja hyväksyntä](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="4c9a1-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="4c9a1-109">Tuo *Veropalvelun virtuaaliyksikköratkaisu* [Veropalvelun virtuaaliyksiköstä](https://go.microsoft.com/fwlink/?linkid=2158160).</span><span class="sxs-lookup"><span data-stu-id="4c9a1-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="4c9a1-110">Määritä Dynamics 365 Regulatory Configuration Service (RCS) -palvelu.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="4c9a1-111">Luo Microsoftille palvelupyyntö, jonka avulla voidaan ottaa käyttöön seuraavien ominaisuuksien lento:</span><span class="sxs-lookup"><span data-stu-id="4c9a1-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="4c9a1-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="4c9a1-112">ERCdsFeature</span></span>
      - <span data-ttu-id="4c9a1-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="4c9a1-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="4c9a1-114">Mene kohtaan Finance ja Ota **Ominaisuuksien hallinta** -työtilassa käyttöön seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="4c9a1-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="4c9a1-115">(Esiversio) Sähköisen raportoinnin Dataverse -tietolähteet tukevat</span><span class="sxs-lookup"><span data-stu-id="4c9a1-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="4c9a1-116">(Esiversio) Veropalvelun Dataverse-tietolähteiden tuki</span><span class="sxs-lookup"><span data-stu-id="4c9a1-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="4c9a1-117">(Esiversio) Globalisaatio-ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4c9a1-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="4c9a1-118">Kirjaudu RCS-malliin vuokraajatiliä käyttäen.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="4c9a1-119">Siirry kohtaan **sähköinen raportointi** > **Liittyvät sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="4c9a1-120">Lisää tietue valitsemalla **Uusi** ja lisää seuraavat kenttätiedot.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="4c9a1-121">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="4c9a1-122">Valitse **Tyyppi**-kentässä **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="4c9a1-123">Kirjoita **Sovellus**-kenttään Dataverse-URL-osoitteesi.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="4c9a1-124">Kirjoita **Vuokraaja**-kenttään vuokraajasi.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="4c9a1-125">Kirjoita **Mukautetun URL-osoitteen** kenttään Dataverse-URL-osoite ja liitä siihen teksti "/api/data/v9.1".</span><span class="sxs-lookup"><span data-stu-id="4c9a1-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="4c9a1-126">Valitse **Tarkista yhteys** ja viimeistele yhteysprosessi.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="4c9a1-127">[![Tarkista yhteys -painike](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="4c9a1-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="4c9a1-128">Siirry kohtaan **sähköinen raportointi** > **Verokonfiguraatiot** ja tuo verokonfiguraatiot kohteesta [Vero-konfiguraatiot](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="4c9a1-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="4c9a1-129">[![Verokonfiguraatiot-sivu, Verotietomallipuu](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="4c9a1-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="4c9a1-130">Siirry **verotettavaan tiedostomallin määritykseen** tai **Dataverse-mallimääritykseen**, jos käytät Microsoft-konfiguraatiota, ja valitse **Yhteydessä oleva sovellus** -kentästä tietue, jonka loit vaiheessa 7.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="4c9a1-131">Määritä **Mallin yhdistämisasetuksen oletusarvoksi** **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4c9a1-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="4c9a1-132">[![Mallimäärityksen sivu](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="4c9a1-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
