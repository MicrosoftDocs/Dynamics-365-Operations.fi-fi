---
title: Regulatory Configuration Service
description: Tämä ohjeaihe sisältää yhteenvedon Regulatory Configuration Servicen (RCS) ominaisuuksista ja tietoja palvelun käytön ominaisuudesta.
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216559"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="7d472-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="7d472-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d472-104">Regulatory Configuration Service (RCS) on erillinen suunnittelu- ja elinkaaren hallintapalvelu, jossa ei ole koodia tai koodia vähäisen koodin yleistystoimintoa.</span><span class="sxs-lookup"><span data-stu-id="7d472-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="7d472-105">RCS:n globalisoinnin laajennus ja mukauttaminen laajentavat ja mukauttavat verotuksen, sähköisen laskutuksen, säännösten raportoinnin, pankki- ja liiketoiminta-asiakirjojen tärkeimpiä globalisointialueita ilman kehittäjien apua.</span><span class="sxs-lookup"><span data-stu-id="7d472-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="7d472-106">Tämä ei-koodia/vähäisen koodin globalisoinnin menetelmä helpottaa ja nopeuttaa globalisointia ja kustannuksien tehokasta luontia tai ulottumista.</span><span class="sxs-lookup"><span data-stu-id="7d472-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="7d472-107">RCS tarjoaa seuraavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="7d472-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="7d472-108">Kaikkien sähköisen raportoinnin (ER) toimintojen tuki.</span><span class="sxs-lookup"><span data-stu-id="7d472-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="7d472-109">Uusien globalisoinnin mikropalveluiden konfiguroimisen edellytykset.</span><span class="sxs-lookup"><span data-stu-id="7d472-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="7d472-110">Sähköisen laskutuksen tuki.</span><span class="sxs-lookup"><span data-stu-id="7d472-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="7d472-111">Lisätietoja kohdassa [Sähköinen laskutus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="7d472-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="7d472-112">Veron laskennan tuet.</span><span class="sxs-lookup"><span data-stu-id="7d472-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="7d472-113">Lisätietoja on kohdassa [Veropalvelu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="7d472-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="7d472-114">Tuki uusille globalisointitoiminnon toiminnoille, jotka yksinkertaistavat monikomponentin ominaisuuksien elinkaaren hallintaa, sekä mahdollistaa toimintojen konfiguroinnin ja ominaisuusparametrien määrittämisen lisätoiminnon.</span><span class="sxs-lookup"><span data-stu-id="7d472-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="7d472-115">Lisätietoja on kohdassa [Regulatory Configuration Service – globalisointipaleluiden yksinkertaisen globalisoinnin ominaisuuksien hallinta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="7d472-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="7d472-116">Tukee keskitettyä julkaisu- ja varastointitilaa sekä mukautettujen konfiguraatioiden jakamista yleisessä tietovarastossa, jotta konfiguroinnin hallintaa voidaan yksinkertaistaa edellyttämättä Microsoft Dynamics Lifecycle Services (LCS) -palveluiden käyttöä.</span><span class="sxs-lookup"><span data-stu-id="7d472-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="7d472-117">Käytä RCS:ää</span><span class="sxs-lookup"><span data-stu-id="7d472-117">Access RCS</span></span>

<span data-ttu-id="7d472-118">Voit rekisteröityä tai kirjautua sisään RCS-palveluun [Regulatory Configuration Service -sivulla](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="7d472-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS:n rekisteröityminen/sisäänkirjaus](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="7d472-120">Tarkista ja hyväksy **Regulatory Configuration Service** -sivulla palvelun käytön lisäehdot ja -ehdot ja valitse sitten jokin seuraavista painikkeista:</span><span class="sxs-lookup"><span data-stu-id="7d472-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="7d472-121">**Rekisteröityminen**, jos olet palvelun ensimmäinen käyttäjä ja käytät yrityksen sähköpostiosoitetta organisaatiosi palveluympäristön järjestämiseen</span><span class="sxs-lookup"><span data-stu-id="7d472-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="7d472-122">**kirjaudu sisään**, jos olet aiemmin rekisteröitynyt palveluun ja haluat käyttää organisaatioympäristöäsi</span><span class="sxs-lookup"><span data-stu-id="7d472-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="7d472-123">Paikallinen käytettävyys</span><span class="sxs-lookup"><span data-stu-id="7d472-123">Regional availability</span></span>

<span data-ttu-id="7d472-124">RCS on yleensä käytettävissä seuraavilla alueilla:</span><span class="sxs-lookup"><span data-stu-id="7d472-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="7d472-125">Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="7d472-125">United States</span></span>
- <span data-ttu-id="7d472-126">Intia</span><span class="sxs-lookup"><span data-stu-id="7d472-126">India</span></span>
- <span data-ttu-id="7d472-127">Ranska</span><span class="sxs-lookup"><span data-stu-id="7d472-127">France</span></span>
- <span data-ttu-id="7d472-128">Eurooppa</span><span class="sxs-lookup"><span data-stu-id="7d472-128">Europe</span></span>

<span data-ttu-id="7d472-129">Täydellinen luettelo alueista on kohdassa [Dynamics 365 ja Power Platform: Saatavuus, tietojen sijainti, kieli ja lokalisointi](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="7d472-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="7d472-130">RCS-oletusyritys</span><span class="sxs-lookup"><span data-stu-id="7d472-130">RCS default company</span></span>

<span data-ttu-id="7d472-131">Suunnittele RCS:ssä käytettävät aikatoiminnot, jotka jaetaan kaikille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="7d472-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="7d472-132">Yrityskohtaisia toimintoja ei ole.</span><span class="sxs-lookup"><span data-stu-id="7d472-132">There is no company-specific functionality.</span></span> <span data-ttu-id="7d472-133">Siksi on suositeltavaa käyttää yhtä yritystä (**DAT**) RCS-ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="7d472-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="7d472-134">Joissakin tilanteissa haluat ehkä kuitenkin ER-muotojen käyttävän tiettyyn yritykseen liittyviä parametreja.</span><span class="sxs-lookup"><span data-stu-id="7d472-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="7d472-135">Vain näissä tilanteissa on käytettävä oletusyrityksen valitsinta.</span><span class="sxs-lookup"><span data-stu-id="7d472-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="7d472-136">Katso esimerkiksi: [Sähköisen raportoinnin muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="7d472-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="7d472-137">Aiheeseen liittyviä RCS-asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="7d472-137">Related RCS documentation</span></span>

<span data-ttu-id="7d472-138">Katso lisätietoja liittyvistä komponenteista seuraavista aiheista:</span><span class="sxs-lookup"><span data-stu-id="7d472-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="7d472-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="7d472-139">**RCS:**</span></span>

    - [<span data-ttu-id="7d472-140">Sähköisen raportoinnin konfiguraatioiden luominen RCS:ssä ja niiden lataaminen yleiseen säilöön</span><span class="sxs-lookup"><span data-stu-id="7d472-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="7d472-141">**Yleinen säilö:**</span><span class="sxs-lookup"><span data-stu-id="7d472-141">**Global repository:**</span></span>

    - [<span data-ttu-id="7d472-142">Luo ER-konfiguraatio ja lataa global repo -palveluun</span><span class="sxs-lookup"><span data-stu-id="7d472-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="7d472-143">Jaa konfiguraatio Global repo -määrityksessä</span><span class="sxs-lookup"><span data-stu-id="7d472-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="7d472-144">Parannettu suodatus Global repossa</span><span class="sxs-lookup"><span data-stu-id="7d472-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="7d472-145">Sähköisen raportoinnin konfiguraatioiden lataaminen Global reposta</span><span class="sxs-lookup"><span data-stu-id="7d472-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="7d472-146">Määritysten lopettaminen Global repossa</span><span class="sxs-lookup"><span data-stu-id="7d472-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="7d472-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) -tallennustilan vanhentuminen</span><span class="sxs-lookup"><span data-stu-id="7d472-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="7d472-148">**Globalisaatio-ominaisuus:**</span><span class="sxs-lookup"><span data-stu-id="7d472-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="7d472-149">Regulatory configuration service (RCS) – globalisointiominaisuus</span><span class="sxs-lookup"><span data-stu-id="7d472-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="7d472-150">RCS-rekisteröinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="7d472-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="7d472-151">Kun rekisteröidyt RCS:ään palvelun sivulta, saatat kohdata Azure Active Directoryyn (Azure AD) liittyvän ongelman.</span><span class="sxs-lookup"><span data-stu-id="7d472-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="7d472-152">Näyttöön avautuva virhesanoma ilmoittaa, että RCS-rekisteröityminen on poistettuna käytöstä, ja se on otettava käyttöön, ennen kuin rekisteröintiprosessi voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="7d472-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![RCS-rekisteröitymisen virhesanoma](media/01_RCSSignUpError.jpg)

<span data-ttu-id="7d472-154">Tämä ongelma ilmenee, koska ad-hoc-tilausten rekisteröityminen on estetty ja `AllowAdHocSubscriptions`-ominaisuus on otettava käyttöön vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="7d472-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="7d472-155">Jos IT-osastosi hallitsee organisaatiosi Azure-vuokraajia, ota yhteyttä tähän osastoon ja raportoi ongelma.</span><span class="sxs-lookup"><span data-stu-id="7d472-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="7d472-156">Jos vastaat Azure-vuokraajien hallinnasta, voit korjata ongelmat noudattamalla seuraavia ohjeita: [Azure Active Directory -rekisteröityminen itsepalveluna](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="7d472-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
