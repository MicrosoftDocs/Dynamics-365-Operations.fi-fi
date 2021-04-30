---
title: Regulatory Configuration Service
description: Tämä ohjeaihe sisältää yhteenvedon Regulatory Configuration Servicen (RCS) ominaisuuksista ja tietoja palvelun käytön ominaisuudesta.
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890797"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="5714a-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="5714a-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5714a-104">Regulatory Configuration Service (RCS) on erillinen suunnittelu- ja elinkaaren hallintapalvelu, jossa ei ole koodia tai koodia vähäisen koodin yleistystoimintoa.</span><span class="sxs-lookup"><span data-stu-id="5714a-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="5714a-105">RCS:n globalisoinnin laajennus ja mukauttaminen laajentavat ja mukauttavat verotuksen, sähköisen laskutuksen, säännösten raportoinnin, pankki- ja liiketoiminta-asiakirjojen tärkeimpiä globalisointialueita ilman kehittäjien apua.</span><span class="sxs-lookup"><span data-stu-id="5714a-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="5714a-106">Tämä ei-koodia/vähäisen koodin globalisoinnin menetelmä helpottaa ja nopeuttaa globalisointia ja kustannuksien tehokasta luontia tai ulottumista.</span><span class="sxs-lookup"><span data-stu-id="5714a-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="5714a-107">RCS tarjoaa seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="5714a-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="5714a-108">Kaikkien sähköisen raportoinnin (ER) toimintojen tuki.</span><span class="sxs-lookup"><span data-stu-id="5714a-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="5714a-109">Uusien globalisoinnin mikropalveluiden konfiguroimisen edellytykset.</span><span class="sxs-lookup"><span data-stu-id="5714a-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="5714a-110">Sähköisen laskutuksen tuki.</span><span class="sxs-lookup"><span data-stu-id="5714a-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="5714a-111">Lisätietoja kohdassa [Sähköinen laskutus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="5714a-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="5714a-112">Veron laskennan tuet.</span><span class="sxs-lookup"><span data-stu-id="5714a-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="5714a-113">Lisätietoja on kohdassa [Veropalvelu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="5714a-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="5714a-114">Tuki uusille globalisointitoiminnon toiminnoille, jotka yksinkertaistavat monikomponentin ominaisuuksien elinkaaren hallintaa, sekä mahdollistaa toimintojen konfiguroinnin ja ominaisuusparametrien määrittämisen lisätoiminnon.</span><span class="sxs-lookup"><span data-stu-id="5714a-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="5714a-115">Lisätietoja on kohdassa [Regulatory Configuration Service – globalisointipaleluiden yksinkertaisen globalisoinnin ominaisuuksien hallinta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="5714a-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="5714a-116">Tukee keskitettyä julkaisu- ja varastointitilaa sekä mukautettujen konfiguraatioiden jakamista yleisessä tietovarastossa, jotta konfiguroinnin hallintaa voidaan yksinkertaistaa edellyttämättä Microsoft Dynamics Lifecycle Services (LCS) -palveluiden käyttöä.</span><span class="sxs-lookup"><span data-stu-id="5714a-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="5714a-117">Käytä RCS:ää</span><span class="sxs-lookup"><span data-stu-id="5714a-117">Access RCS</span></span>

<span data-ttu-id="5714a-118">Voit rekisteröityä tai kirjautua sisään RCS-palveluun [Regulatory Configuration Service -sivulla](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="5714a-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS:n rekisteröityminen/sisäänkirjaus](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="5714a-120">Tarkista ja hyväksy **Regulatory Configuration Service** -sivulla palvelun käytön lisäehdot ja -ehdot ja valitse sitten jokin seuraavista painikkeista:</span><span class="sxs-lookup"><span data-stu-id="5714a-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="5714a-121">**Rekisteröityminen**, jos olet palvelun ensimmäinen käyttäjä ja käytät yrityksen sähköpostiosoitetta organisaatiosi palveluympäristön järjestämiseen</span><span class="sxs-lookup"><span data-stu-id="5714a-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="5714a-122">**kirjaudu sisään**, jos olet aiemmin rekisteröitynyt palveluun ja haluat käyttää organisaatioympäristöäsi</span><span class="sxs-lookup"><span data-stu-id="5714a-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="5714a-123">Paikallinen käytettävyys</span><span class="sxs-lookup"><span data-stu-id="5714a-123">Regional availability</span></span>

<span data-ttu-id="5714a-124">RCS on yleensä käytettävissä seuraavilla alueilla:</span><span class="sxs-lookup"><span data-stu-id="5714a-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="5714a-125">Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="5714a-125">United States</span></span>
- <span data-ttu-id="5714a-126">Intia</span><span class="sxs-lookup"><span data-stu-id="5714a-126">India</span></span>
- <span data-ttu-id="5714a-127">Ranska</span><span class="sxs-lookup"><span data-stu-id="5714a-127">France</span></span>
- <span data-ttu-id="5714a-128">Eurooppa</span><span class="sxs-lookup"><span data-stu-id="5714a-128">Europe</span></span>

<span data-ttu-id="5714a-129">Täydellinen luettelo alueista on kohdassa [Dynamics 365 ja Power Platform: Saatavuus, tietojen sijainti, kieli ja lokalisointi](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="5714a-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="5714a-130">Aiheeseen liittyviä RCS-asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="5714a-130">Related RCS documentation</span></span>

<span data-ttu-id="5714a-131">Katso lisätietoja liittyvistä komponenteista seuraavista ohjeista:</span><span class="sxs-lookup"><span data-stu-id="5714a-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="5714a-132">**Yleinen säilö:**</span><span class="sxs-lookup"><span data-stu-id="5714a-132">**Global repository:**</span></span>

    - [<span data-ttu-id="5714a-133">Luo ER-konfiguraatio ja lataa global repo -palveluun</span><span class="sxs-lookup"><span data-stu-id="5714a-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="5714a-134">Jaa konfiguraatio Global repo -määrityksessä</span><span class="sxs-lookup"><span data-stu-id="5714a-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="5714a-135">Parannettu suodatus Global repossa</span><span class="sxs-lookup"><span data-stu-id="5714a-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="5714a-136">Sähköisen raportoinnin konfiguraatioiden lataaminen Global reposta</span><span class="sxs-lookup"><span data-stu-id="5714a-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="5714a-137">Määritysten lopettaminen Global repossa</span><span class="sxs-lookup"><span data-stu-id="5714a-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="5714a-138">**Globalisaatio-ominaisuus:**</span><span class="sxs-lookup"><span data-stu-id="5714a-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="5714a-139">Regulatory configuration service (RCS) – globalisointiominaisuus</span><span class="sxs-lookup"><span data-stu-id="5714a-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)