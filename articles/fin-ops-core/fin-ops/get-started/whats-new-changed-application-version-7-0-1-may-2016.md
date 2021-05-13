---
title: Dynamics AX -sovelluksen version 7.0.1 uudet ja muuttuneet ominaisuudet (toukokuu 2016)
description: Tässä artikkelissa käsitellään Microsoft Dynamics AX -sovellusversion 7.0.1 uusia tai muuttuneita ominaisuuksia. Tämä versio julkaistiin toukokuussa 2016 ja sen koontiversio on 7.0.1265.23014.
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c4d762a6750a295b91a1d146b7bf0ae750e2e9bd
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923186"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="04739-104">Dynamics AX -sovelluksen version 7.0.1 uudet ja muuttuneet ominaisuudet (toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="04739-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04739-105">Tässä artikkelissa käsitellään Microsoft Dynamics AX -sovellusversion 7.0.1 uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="04739-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="04739-106">Tämä versio julkaistiin toukokuussa 2016 ja sen koontiversio on 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="04739-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="04739-107">Sähköinen raportointi (ER)</span><span class="sxs-lookup"><span data-stu-id="04739-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="04739-108">Mitä voit tehdä?</span><span class="sxs-lookup"><span data-stu-id="04739-108">What can you do?</span></span> | <span data-ttu-id="04739-109">Miksi tämä on tärkeää?</span><span class="sxs-lookup"><span data-stu-id="04739-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="04739-110">Määritä sähköisen raportoinnin (ER) raporttisuunnittelun suorituksenaikainen valintaikkuna, jotta käyttäjät voivat valita sopivat taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="04739-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="04739-111">Käyttäjät voivat valita suorituksen aikana useita taloushallinnon dimensioita ER-raportin suorittamisen valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="04739-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="04739-112">Valittujen taloushallinnon dimensioiden tiedot näytetään luotavassa sähköisessä asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="04739-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="04739-113">Määritä useiden taloushallinnon dimensioiden käyttöoikeus ER-raportin suunnittelun aikana yhdellä yhdistämismäärityksellä haluttuun tietolähteeseen.</span><span class="sxs-lookup"><span data-stu-id="04739-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="04739-114">Samaa ER-raporttimääritystä voidaan käyttää luomaan sähköisiä asiakirjoja, jotka esittävät tapahtumatiedot yhdessä taloushallinnon dimensioiden tiedot, riippumatta käyttäjän valitsemien tai nykyiselle yritykselle tai -esiintymälle määritettyjen taloushallinnon dimensioiden määrästä.</span><span class="sxs-lookup"><span data-stu-id="04739-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="04739-115">Määritä ER-raportti antamaan tiedot OPENXML-laskentataulukkomuodossa luodun sähköisen asiakirjan dynaamisesti luotuihin sarakkeisiin.</span><span class="sxs-lookup"><span data-stu-id="04739-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="04739-116">ER-raportti voi antaa tiedot luotavaan OPENXML-laskentataulukkoon replikoimalla sarakkeet vaakasuunnassa.</span><span class="sxs-lookup"><span data-stu-id="04739-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="04739-117">Tämän vuoksi samaa ER-raportin määritystä voidaan käyttää uudelleen luomaan sähköisiä asiakirjoja, joilla on eri määrä dynaamisesti luotuja sarakkeita.</span><span class="sxs-lookup"><span data-stu-id="04739-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="04739-118">Määritä ER-kohteet niin, että muodon tulos on ohjattava tiettyyn kohteeseen: tiedosto, sähköposti tai arkisto (Microsoft SharePoint -kansio tai Microsoft Azuren tallennustila).</span><span class="sxs-lookup"><span data-stu-id="04739-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="04739-119">Kun ER-määritys suoritettiin aiemmin, avautuva sanomaruutu pyysi käyttäjää tallentamaan tai avaamaan tiedoston.</span><span class="sxs-lookup"><span data-stu-id="04739-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="04739-120">Voit nyt määrittää kohteen valmiiksi erikseen kullekin muotomääritykselle ja tuloskomponentille (kansio tai tiedosto).</span><span class="sxs-lookup"><span data-stu-id="04739-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="04739-121">Käyttäjät, joilla on tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="04739-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="04739-122">Myyntipiste – Microsoft Dynamics AX vähittäismyynti</span><span class="sxs-lookup"><span data-stu-id="04739-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="04739-123">Mitä voit tehdä?</span><span class="sxs-lookup"><span data-stu-id="04739-123">What can you do?</span></span> | <span data-ttu-id="04739-124">Miksi tämä on tärkeää?</span><span class="sxs-lookup"><span data-stu-id="04739-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="04739-125">Käytä Google Chrome -selainta.</span><span class="sxs-lookup"><span data-stu-id="04739-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="04739-126">Vähittäismyyjät voivat nyt käynnistää pilvimyyntipisteen Chrome-selaimesta ja saada käyttöönsä kaikki pilvimyyntipisteen Microsoft Edgessä ja Internet Explorerissa käytettävissä olevat toiminnot.</span><span class="sxs-lookup"><span data-stu-id="04739-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="04739-127">Taloushallinnan raportointi</span><span class="sxs-lookup"><span data-stu-id="04739-127">Financial reporting</span></span>

| <span data-ttu-id="04739-128">Mitä voit tehdä?</span><span class="sxs-lookup"><span data-stu-id="04739-128">What can you do?</span></span> | <span data-ttu-id="04739-129">Miksi tämä on tärkeää?</span><span class="sxs-lookup"><span data-stu-id="04739-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="04739-130">Luo talousraportoinnin tietovarasto.</span><span class="sxs-lookup"><span data-stu-id="04739-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="04739-131">Kun siirrät Dynamics AX -tietokantoja ympäristöjen välillä tai teet muita perusteellisia muutoksia ympäristössä, talousraportointitietokanta on ehkä muodostettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="04739-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="04739-132">Windows PowerShell -komentosarja on nyt käytettävissä tietokannan uudelleenmuodostusta varten.</span><span class="sxs-lookup"><span data-stu-id="04739-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="04739-133">Et voi enää valita raportin suunnittelutoiminnon asetuksia, jotka eivät kelpaa.</span><span class="sxs-lookup"><span data-stu-id="04739-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="04739-134">Useita Management Reporterin markkinointiversioissa käytettyjä raportin suunnittelutoiminnon asetuksia ei voi käyttää tässä Dynamics AX -versiossa.</span><span class="sxs-lookup"><span data-stu-id="04739-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="04739-135">Nämä asetukset liittyivät talousraportin suunnitteluun, tulostukseen ja linkittämiseen.</span><span class="sxs-lookup"><span data-stu-id="04739-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="04739-136">Nämä asetukset on poistettu talousraportin suunnittelutoiminnosta käyttäjän virheiden estämiseksi.</span><span class="sxs-lookup"><span data-stu-id="04739-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="04739-137">Taloushallinto</span><span class="sxs-lookup"><span data-stu-id="04739-137">Financial management</span></span>

| <span data-ttu-id="04739-138">Mitä voit tehdä?</span><span class="sxs-lookup"><span data-stu-id="04739-138">What can you do?</span></span> | <span data-ttu-id="04739-139">Miksi tämä on tärkeää?</span><span class="sxs-lookup"><span data-stu-id="04739-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="04739-140">Luo positiivisia maksutiedostoja ostoreskontramaksuille.</span><span class="sxs-lookup"><span data-stu-id="04739-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="04739-141">Positiivisia maksutiedostoja voidaan luoda sekkipetosten ehkäisemiseksi.</span><span class="sxs-lookup"><span data-stu-id="04739-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="04739-142">Fyysinen varasto ja tuotanto</span><span class="sxs-lookup"><span data-stu-id="04739-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04739-143">Mitä voit tehdä?</span><span class="sxs-lookup"><span data-stu-id="04739-143">What can you do?</span></span></th>
<th><span data-ttu-id="04739-144">Miksi tämä on tärkeää?</span><span class="sxs-lookup"><span data-stu-id="04739-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04739-145">Määritä fyysisen varaston työkäytäntö ohjaamaan työn luontia työjoukolle tietyissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="04739-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="04739-146">Varastointiprosessit eivät aina sisällä työtä.</span><span class="sxs-lookup"><span data-stu-id="04739-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="04739-147">Voit käyttää uutta fyysisen varaston työkäytäntöä estämään raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonti tietyille tuotejoukoille tietyissä sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="04739-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04739-148">Määritä, että tuotannon tuotossijainti ei ole rekisterikilpiohjattu.</span><span class="sxs-lookup"><span data-stu-id="04739-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="04739-149">Voit nyt määrittää, että tuotteen tuotossijainti ei ole rekisterikilpiohjattu.</span><span class="sxs-lookup"><span data-stu-id="04739-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="04739-150">Tämä ominaisuus on kätevä, kun ylöspäinsuuntautuva tuotantotilaus raportoi nimikkeet valmistuneiksi suoraan sijaintiin, joka toimii alaspäinsuuntautuvan tuotantotilauksen syöttösijaintina.</span><span class="sxs-lookup"><span data-stu-id="04739-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04739-151">Tue saman nimikkeen eri tuotedimensioita sisältävien nimikkeiden tuoterakenteita.</span><span class="sxs-lookup"><span data-stu-id="04739-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="04739-152">Kun tuotannossa käytetään yhtä tuotedimensiota tai useita dimensioita, voi syntyä tilanne, jossa haluat tuottaa nimikkeen saman nimikkeen eri variantin perusteella.</span><span class="sxs-lookup"><span data-stu-id="04739-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="04739-153">Lisätietoja on <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">tässä blogissa</a>.</span><span class="sxs-lookup"><span data-stu-id="04739-153">For more information, see <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04739-154">Tuoterakenteet, joiden tuoterakenteiden ensimmäisellä tasolla on kehärakenteita, jätetään materiaalin resurssisuunnittelun tuoterakennetason laskennan ulkopuolelle.</span><span class="sxs-lookup"><span data-stu-id="04739-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="04739-155">Tuoterakennehierarkiaan kehäkiertoa aiheuttavien tuotantotilausten tuotevarianteille ei voi määrittää oikeita tuoterakennetasoja.</span><span class="sxs-lookup"><span data-stu-id="04739-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04739-156">Laske erilliset tuoterakennetasot materiaalin resurssisuunnittelulle ja kustannuslaskennalle:</span><span class="sxs-lookup"><span data-stu-id="04739-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="04739-157">Materiaalin resurssisuunnittelun tuoterakennetasot lasketaan uudessa <strong>ReqItemLevel</strong>-taulussa.</span><span class="sxs-lookup"><span data-stu-id="04739-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="04739-158">Päättyneet tuotantotilaukset ohitetaan laskennassa.</span><span class="sxs-lookup"><span data-stu-id="04739-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="04739-159">Tuotannon kustannuslaskennan tuoterakennetasot lasketaan <strong>InventTable</strong>-taulussa.</span><span class="sxs-lookup"><span data-stu-id="04739-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="04739-160">Päättyneet tuotantotilaukset sisällytetään laskentaan.</span><span class="sxs-lookup"><span data-stu-id="04739-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="04739-161">Kun suoritetaan materiaalin resurssisuunnittelua, kuten pääsuunnittelun suunnitelman ajoitusta ja hajotusta, vain materiaalin resurssisuunnittelussa käytetyt tuoterakennetasot on laskettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="04739-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="04739-162">Toisin sanoen tuotannon kustannuslaskennassa käytettyjä tuoterakennetasoja ei tarvitse laskea.</span><span class="sxs-lookup"><span data-stu-id="04739-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="04739-163">Kun suoritetaan kustannuslaskentatoimintoja, kuten varaston sulkemista, vain tuotannon kustannuslaskennan tuoterakennetasot on laskettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="04739-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="04739-164">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="04739-164">Additional resources</span></span>

[<span data-ttu-id="04739-165">Uudet ja muuttuneet ominaisuudet Finance and Operationsin aloitussivulla</span><span class="sxs-lookup"><span data-stu-id="04739-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="04739-166">Uudet tai päivitetyt tehtäväoppaat (toukokuu 2016)</span><span class="sxs-lookup"><span data-stu-id="04739-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]