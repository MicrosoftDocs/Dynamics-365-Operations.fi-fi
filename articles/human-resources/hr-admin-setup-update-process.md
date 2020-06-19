---
title: Päivitysprosessi
description: Microsoft Dynamics 365 Human Resourceson todellinen ohjelmisto palveluna (SaaS), joka tarjoaa jatkuvia ja kosketusvapaita palvelupäivityksiä sovellus- ja ympäristömuutoksille.
author: andreabichsel
manager: AnnBe
ms.date: 02/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 006f3c7218436c1c70e29e51f8b1b784ae36b2dd
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431173"
---
# <a name="update-process"></a><span data-ttu-id="fddcc-103">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="fddcc-103">Update process</span></span>

<span data-ttu-id="fddcc-104">Microsoft Dynamics 365 Human Resourceson todellinen ohjelmisto palveluna (SaaS), joka tarjoaa jatkuvia ja kosketusvapaita palvelupäivityksiä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="fddcc-105">Nämä päivitykset sisältävät sekä sovellus -että ympäristömuutoksia, jotka usein tarjoavat tärkeitä parannuksia palveluun, lakisääteiset päivitykset mukaan luettuna.</span><span class="sxs-lookup"><span data-stu-id="fddcc-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="fddcc-106">Päivityskäytäntö</span><span class="sxs-lookup"><span data-stu-id="fddcc-106">Update policy</span></span>

<span data-ttu-id="fddcc-107">Päivitykset julkaistaan säännöllisesti kaikkiin ympäristöihin.</span><span class="sxs-lookup"><span data-stu-id="fddcc-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="fddcc-108">Human Resourcesia tuetaan [Microsoftin elinkaarikäytännön](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) mukaisesti. Se tarjoaa johdonmukaisia ja ennakoitavia ohjeita tuen saatavuudesta.</span><span class="sxs-lookup"><span data-stu-id="fddcc-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="fddcc-109">Päivitysväli</span><span class="sxs-lookup"><span data-stu-id="fddcc-109">Release cadence</span></span>

<span data-ttu-id="fddcc-110">Human Resources -päivitykset tehdään kaikissa ympäristöissä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="fddcc-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="fddcc-111">Human Resourcesiin liittyy kahdenlaisia julkaisuja:</span><span class="sxs-lookup"><span data-stu-id="fddcc-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="fddcc-112">**Palvelupäivitykset**: Kahden viikon välein ilmestyvät päivitykset, joissa on virheiden korjauksia ja uusia toimintoja.</span><span class="sxs-lookup"><span data-stu-id="fddcc-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="fddcc-113">Palvelupäivityksiin kuuluvat myös soveltuvat Platform updatet, kun ne julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="fddcc-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="fddcc-114">Jos haluat saada käsityksen siitä, milloin Platform updatet julkaistaan, katso [Taulukko 3: Platform-julkaisut ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="fddcc-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="fddcc-115">Kahdesti viikossa ilmestyvillä päivityksillä on vaiheittainen maailmanlaajuinen käyttöönotto alueiden välillä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="fddcc-116">Lisätietoja kahdesti viikossa ilmestyvistä päivityksistä esitetään kohdassa [Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="fddcc-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="fddcc-117">Kaikki tuetut palvelinkeskukset päivittyvät kahden viikon välein, ellei muuta mainita.</span><span class="sxs-lookup"><span data-stu-id="fddcc-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="fddcc-118">Alueet Yhdysvallat, Australia, Eurooppa, Yhdistynyt kuningaskunta ja Kanada kuuluvat kahdesti viikossa ilmestyvien päivitysten piiriin.</span><span class="sxs-lookup"><span data-stu-id="fddcc-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="fddcc-119">**Common Data Service -ratkaisujen päivitykset**: Nämä päivitykset suoritetaan noin kuuden viikon välein tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="fddcc-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="fddcc-120">Niihin kuuluu uusia yksikköjä ja muutoksia olemassa oleviin yksikköihin Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="fddcc-121">Nämä päivitykset julkaistaan samoilla alueilla kuin kahdesti viikossa ilmestyvät päivitykset, ja niiden replikointi kaikissa palvelinkeskuksissa kestää noin kuusi viikkoa.</span><span class="sxs-lookup"><span data-stu-id="fddcc-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="fddcc-122">Ratkaisupäivitykset saattavat olla linjassa kahdesti viikossa ilmestyvien palvelupäivitysten kanssa.</span><span class="sxs-lookup"><span data-stu-id="fddcc-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="fddcc-123">Ratkaisupäivitykset ovat käytettävissä kaikissa palvelinkeskuksissa, kun ne on julkaistu.</span><span class="sxs-lookup"><span data-stu-id="fddcc-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="fddcc-124">Jos et halua odottaa päivitysten automaattista replikointia, voit suorittaa nämä päivitykset manuaalisesti minkä tahansa palvelinkeskuksen missä tahansa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="fddcc-125">Tarvittaessa Human Resources tarjoaa myös seuraavanlaisia korjauksia:</span><span class="sxs-lookup"><span data-stu-id="fddcc-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="fddcc-126">**Aliversio (hotfix)**: Ohjelmakorjauksia, jotka voidaan suorittaa joko kahdesti viikossa ilmestyvien palvelupäivitysjulkaisun yhteydessä tai erillään siitä</span><span class="sxs-lookup"><span data-stu-id="fddcc-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="fddcc-127">**Hätäkorjaus**: ennakoivia ja reaktiivisia hotfix-korjauksia, jotka ovat luonteeltaan erillisiä, voivat sisältää vain määritykseen tai koodiin kohdistuvia muutoksia käytössä olevan sivun ongelmien ratkaisemiseksi ja voidaan suorittaa erillään kahdesti viikossa ilmestyvistä palvelupäivitysjulkaisuista</span><span class="sxs-lookup"><span data-stu-id="fddcc-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="fddcc-128">Julkaisut tarkistetaan, testataan ja vahvistetaan sisäisessä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="fddcc-129">Kun koontiversiot on hyväksytty, ne otetaan käyttöön tuotannossa.</span><span class="sxs-lookup"><span data-stu-id="fddcc-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="fddcc-130">Vapauta tahtipoikkeukset vuonna 2020</span><span class="sxs-lookup"><span data-stu-id="fddcc-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="fddcc-131">Seuraavat päivämäärät ovat poikkeuksia vakiojulkaisuaikataulusta:</span><span class="sxs-lookup"><span data-stu-id="fddcc-131">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="fddcc-132">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="fddcc-132">Date</span></span> | <span data-ttu-id="fddcc-133">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fddcc-133">Description</span></span> |
| --- | --- |
| <span data-ttu-id="fddcc-134">Marraskuun 23. päivän viikko</span><span class="sxs-lookup"><span data-stu-id="fddcc-134">Week of November 23</span></span> | <span data-ttu-id="fddcc-135">Ei päivityksiä</span><span class="sxs-lookup"><span data-stu-id="fddcc-135">No updates</span></span> |
| <span data-ttu-id="fddcc-136">Joulukuun 14. päivän viikko</span><span class="sxs-lookup"><span data-stu-id="fddcc-136">Week of December 14</span></span> | <span data-ttu-id="fddcc-137">Vain vähäisiä päivityksiä</span><span class="sxs-lookup"><span data-stu-id="fddcc-137">Minor updates only</span></span> |
| <span data-ttu-id="fddcc-138">Joulukuun 21. päivän viikko</span><span class="sxs-lookup"><span data-stu-id="fddcc-138">Week of December 21</span></span> | <span data-ttu-id="fddcc-139">Ei päivityksiä</span><span class="sxs-lookup"><span data-stu-id="fddcc-139">No updates</span></span> |
| <span data-ttu-id="fddcc-140">Joulukuun 28. päivän viikko</span><span class="sxs-lookup"><span data-stu-id="fddcc-140">Week of December 28</span></span> | <span data-ttu-id="fddcc-141">Ei päivityksiä</span><span class="sxs-lookup"><span data-stu-id="fddcc-141">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="fddcc-142">Viestintä</span><span class="sxs-lookup"><span data-stu-id="fddcc-142">Communications</span></span>

<span data-ttu-id="fddcc-143">Tietoa siitä, mitä Human Resourcesin osalta suunnitellaan ja mitä siihen liittyen on julkaistu, saat seuraavista paikoista:</span><span class="sxs-lookup"><span data-stu-id="fddcc-143">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="fddcc-144">Dynamics 365 Human Resourcesin toteutussuunnitelma</span><span class="sxs-lookup"><span data-stu-id="fddcc-144">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="fddcc-145">Dynamics 365:n julkaisusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="fddcc-145">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="fddcc-146">Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="fddcc-146">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="fddcc-147">[Lifecycle Servicesin (LCS) ongelmahaku](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (vain Platformiin liittyvät virheet)</span><span class="sxs-lookup"><span data-stu-id="fddcc-147">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="fddcc-148">Human Resources -blogi</span><span class="sxs-lookup"><span data-stu-id="fddcc-148">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="fddcc-149">Human Resourcesin Yammer-yhteisö</span><span class="sxs-lookup"><span data-stu-id="fddcc-149">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="fddcc-150">Ominaisuuksien esikatselu eristysympäristössä</span><span class="sxs-lookup"><span data-stu-id="fddcc-150">Preview features in a sandbox environment</span></span>

<span data-ttu-id="fddcc-151">Voit varmentaa esikatseluominaisuudet eristysympäristössä, ennen kuin otat ne käyttöön tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-151">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="fddcc-152">Lisätietoja uusien ominaisuuksien käyttöönotosta on kohdassa [ominaisuuksien hallinnan yleiskuvaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="fddcc-152">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="fddcc-153">Kaikki uudet toiminnot pysyvät esiversiossa ainakin 30 päivää ja yleensä 30–60 päivää.</span><span class="sxs-lookup"><span data-stu-id="fddcc-153">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="fddcc-154">Tärkeimmät toiminnot ovat yleensä saatavana kunkin vuoden lokakuussa ja huhtikuussa esiversiojakson jälkeen.</span><span class="sxs-lookup"><span data-stu-id="fddcc-154">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="fddcc-155">Voit ottaa uudet ominaisuudet käyttöön heti, kun näet ne Toimintojen hallinta -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="fddcc-155">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="fddcc-156">Jotkin toiminnot on ehkä otettu käyttöön oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="fddcc-156">Some features may be on by default.</span></span>

<span data-ttu-id="fddcc-157">Joskus keskeinen toiminto on otettu käyttöön oletusarvoisesti eikä sitä voi poistaa käytöstä (esimerkiksi Toimintojen hallinta -työtilassa).</span><span class="sxs-lookup"><span data-stu-id="fddcc-157">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="fddcc-158">Kun toiminto on yleisesti saatavana, se voidaan ottaa käyttöön tai poistaa käytöstä tuotantoympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-158">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="fddcc-159">Toimintojen hallinta -työtila ilmaisee, milloin esiversiotoiminto tulee pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="fddcc-159">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="fddcc-160">Tämä päivämäärä on yleensä 1. lokakuuta tai 1. huhtikuuta eli ne vastaavat puolivuotisia julkaisusuunnitelmia.</span><span class="sxs-lookup"><span data-stu-id="fddcc-160">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="fddcc-161">Pakollisia toimintoja ei voi poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-161">You can't turn off mandatory features.</span></span> <span data-ttu-id="fddcc-162">Toiminnon voi ottaa käyttöön ja poistaa käytöstä kaikissa ympäristöissä siihen saakka, että muuttuu pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="fddcc-162">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="fddcc-163">Suosittelemme vahvasti ominaisuuksien esikatselua eristys- tai kokeiluympäristössä.</span><span class="sxs-lookup"><span data-stu-id="fddcc-163">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="fddcc-164">On parasta luoda kopio nykyisestä tuotantoympäristöstä tai tietokannasta eristetyssä ympäristössä, jotta voit tutustua uusien ominaisuuksien kokonaiskokemukseen tietojasi käyttäen.</span><span class="sxs-lookup"><span data-stu-id="fddcc-164">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="fddcc-165">Lisä tietoja eristysympäristön valmistelemisesta on kohdassa [Human Resources -projektin valmistelu](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="fddcc-165">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="fddcc-166">Katso kokeiluympäristön poistamista varten [Poista esiintymä](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="fddcc-166">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="fddcc-167">Virheistä ilmoittaminen</span><span class="sxs-lookup"><span data-stu-id="fddcc-167">Report bugs</span></span>

<span data-ttu-id="fddcc-168">Kun testaat esikatseluominaisuuksia tai kokeilet uusia toimintoja, saatat löytää asioita, jotka eivät toimi odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="fddcc-168">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="fddcc-169">Ilmoita kaikista virheistä [Microsoft Dynamics 365 -tuen](https://dynamics.microsoft.com/support/) avulla.</span><span class="sxs-lookup"><span data-stu-id="fddcc-169">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="fddcc-170">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="fddcc-170">See also</span></span>

[<span data-ttu-id="fddcc-171">Dynamics 365:n ja Power Platformin julkaisusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="fddcc-171">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="fddcc-172">Dynamics 365 Human Resourcen uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="fddcc-172">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="fddcc-173">Ohjelmiston elinkaarikäytäntö</span><span class="sxs-lookup"><span data-stu-id="fddcc-173">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

