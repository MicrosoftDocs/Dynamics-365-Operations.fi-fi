---
title: Kaksoiskirjoituksen yleiskatsaus
description: Tämä ohjeaihe sisältää kaksoiskirjoituksen yleiskatsauksen. Kaksoiskirjoitus on infrastruktuuri, joka sisältää lähes reaaliaikaisen vuorovaikutuksen Microsoft Dynamics 365:n mallipohjaisten sovellusten ja Finance and Operations -sovellusten välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075981"
---
# <a name="dual-write-overview"></a><span data-ttu-id="b597d-104">Kaksoiskirjoituksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b597d-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="b597d-105">Mikä on kaksoiskirjoitus?</span><span class="sxs-lookup"><span data-stu-id="b597d-105">What is dual-write?</span></span>

<span data-ttu-id="b597d-106">Kaksoiskirjoitus on valmis infrastruktuuri, joka sisältää lähes reaaliaikaisen vuorovaikutuksen Microsoft Dynamics 365:n mallipohjaisten sovellusten ja Finance and Operations -sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="b597d-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="b597d-107">Kun asiakkaiden, tuotteiden, henkilöiden ja toimintojen tiedot siirretään sovellusten ulkopuolelle, kaikki organisaation osastot voivat käyttää niitä.</span><span class="sxs-lookup"><span data-stu-id="b597d-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="b597d-108">Kaksoiskirjoitus sisältää tiukasti yhdistetyn kaksisuuntaisen integroinnin Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="b597d-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b597d-109">Kaikki tietojen muutokset Finance and Operations -sovelluksissa aiheuttavat kaksoiskirjoituksia Common Data Servicessä ja Common Data Servicen tietojen muutokset puolestaan kirjoituksia Finance and Operations -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="b597d-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="b597d-110">Tämä automatisoitu tietovirta tarjoaa integroidun käyttökokemuksen eri sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="b597d-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Tietojen suhde sovellusten välillä](media/dual-write-overview.jpg)

<span data-ttu-id="b597d-112">Kaksoiskirjoituksissa on eri osaa: *infrastruktuuri* ja *sovellus*.</span><span class="sxs-lookup"><span data-stu-id="b597d-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="b597d-113">Infrastruktuuri</span><span class="sxs-lookup"><span data-stu-id="b597d-113">Infrastructure</span></span>

<span data-ttu-id="b597d-114">Kaksoiskirjoituksen infrastruktuuri on laajennettavissa. Se on luotettava infrastruktuuri, joka sisältää seuraavat keskeiset ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="b597d-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="b597d-115">Sovellusten välinen synkroninen ja kaksisuuntainen tietovirta</span><span class="sxs-lookup"><span data-stu-id="b597d-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="b597d-116">Synkronisointi yhdessä toiston, pysäytyksen ja kertymän tilojen kanssa tukee järjestelmää online- ja offline-tilassa sekä asynkronisessa tilassa.</span><span class="sxs-lookup"><span data-stu-id="b597d-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="b597d-117">Mahdollisuus synkronoida alkuperäiset tiedot sovellusten välillä</span><span class="sxs-lookup"><span data-stu-id="b597d-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="b597d-118">Yhdistetty näkymä toiminto- ja virhelokeista tietojen järjestelmänvalvojille</span><span class="sxs-lookup"><span data-stu-id="b597d-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="b597d-119">Mahdollisuus määrittää mukautettuja hälytyksiä ja rajoja sekä tilata ilmoituksia</span><span class="sxs-lookup"><span data-stu-id="b597d-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="b597d-120">Intuitiivinen käyttöliittymä suodatusta ja muunnoksia varten</span><span class="sxs-lookup"><span data-stu-id="b597d-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="b597d-121">Mahdollisuus määrittää ja tarkastella entiteetin riippuvuuksia ja suhteita</span><span class="sxs-lookup"><span data-stu-id="b597d-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="b597d-122">Laajennettavuus sekä vakioentiteeteille että mukautetuille entiteeteille ja määrityksille</span><span class="sxs-lookup"><span data-stu-id="b597d-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="b597d-123">Luotettava sovelluksen elinkaaren hallinta</span><span class="sxs-lookup"><span data-stu-id="b597d-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="b597d-124">Uusien asiakkaiden valmis määrityskokemus</span><span class="sxs-lookup"><span data-stu-id="b597d-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="b597d-125">Hakemus</span><span class="sxs-lookup"><span data-stu-id="b597d-125">Application</span></span>

<span data-ttu-id="b597d-126">Kaksoiskirjoitus luo vastaavuuden Finance and Operations -sovellusten käsitteiden ja Dynamics 365:n mallipohjaisten sovellusten käsitteiden välille.</span><span class="sxs-lookup"><span data-stu-id="b597d-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="b597d-127">Tämä integraatio tukee seuraavia skenaarioita:</span><span class="sxs-lookup"><span data-stu-id="b597d-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="b597d-128">Integroidut asiakkaan päätiedot</span><span class="sxs-lookup"><span data-stu-id="b597d-128">Integrated customer master</span></span>
+ <span data-ttu-id="b597d-129">Asiakkaan kanta-asiakaskorttien ja palkkiopisteiden käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="b597d-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="b597d-130">Yhtenäinen tuotteiden hallinnan kokemus</span><span class="sxs-lookup"><span data-stu-id="b597d-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="b597d-131">Tietoja organisaatiohierarkiasta</span><span class="sxs-lookup"><span data-stu-id="b597d-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="b597d-132">Integroidut toimittajan päätiedot</span><span class="sxs-lookup"><span data-stu-id="b597d-132">Integrated vendor master</span></span>
+ <span data-ttu-id="b597d-133">Talous- ja veroviitetietojen käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="b597d-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="b597d-134">Tarvittaessa käytettävän hinnoitteluohjelman käyttökokemus</span><span class="sxs-lookup"><span data-stu-id="b597d-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="b597d-135">Integroitu prospektista käteiseksi -käyttökokemus</span><span class="sxs-lookup"><span data-stu-id="b597d-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="b597d-136">Mahdollisuus sekä sisäisten resurssien että asiakkaan resurssien käyttämiseen kentän edustajien kautta</span><span class="sxs-lookup"><span data-stu-id="b597d-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="b597d-137">Integroitu hankinnasta maksuun -käyttökokemus</span><span class="sxs-lookup"><span data-stu-id="b597d-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="b597d-138">Asiakastietojen ja asiakirjojen integroidut aktiviteetit ja huomautukset</span><span class="sxs-lookup"><span data-stu-id="b597d-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="b597d-139">Mahdollisuus etsiä käytettävissä olevan varaston saatavuutta ja tietoja</span><span class="sxs-lookup"><span data-stu-id="b597d-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="b597d-140">Projektista käteiseksi -käyttökokemus</span><span class="sxs-lookup"><span data-stu-id="b597d-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="b597d-141">Mahdollisuus käsitellä useita osoitteita ja rooleja osapuolen käsitteen kautta</span><span class="sxs-lookup"><span data-stu-id="b597d-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="b597d-142">Yhden lähteen hallinta käyttäjille</span><span class="sxs-lookup"><span data-stu-id="b597d-142">Single source management for users</span></span>
+ <span data-ttu-id="b597d-143">Vähittäiskaupan ja markkinoinnin integroidut kanavat</span><span class="sxs-lookup"><span data-stu-id="b597d-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="b597d-144">Kampanjoiden ja alennusten näkyvyys</span><span class="sxs-lookup"><span data-stu-id="b597d-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="b597d-145">Palvelupyyntöjen toiminnot</span><span class="sxs-lookup"><span data-stu-id="b597d-145">Request-for-service functions</span></span>
+ <span data-ttu-id="b597d-146">Yksinkertaistetut palvelutoiminnot</span><span class="sxs-lookup"><span data-stu-id="b597d-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="b597d-147">Yleisimmät syyt kaksoiskirjoittamisen käyttämiseksi</span><span class="sxs-lookup"><span data-stu-id="b597d-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="b597d-148">Kaksoiskirjoitus mahdollistaa tietojen integroinnin Microsoft Dynamics 365 -sovelluksissa</span><span class="sxs-lookup"><span data-stu-id="b597d-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="b597d-149">Tämä luotettava kehys linkittää ympäristöt ja mahdollistaa erilaisten liiketoimintasovellusten käyttämisen yhdessä.</span><span class="sxs-lookup"><span data-stu-id="b597d-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="b597d-150">Seuraavassa kerrotaan tärkeimmät syyt kaksoiskirjoituksen käyttämiseksi:</span><span class="sxs-lookup"><span data-stu-id="b597d-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="b597d-151">Kaksoiskirjoitus mahdollistaa tiiviisti yhdistetyn ja lähes reaaliaikaisen kaksisuuntaisen integroinnin Finance and Operations -sovellusten ja Dynamics 365:n mallipohjaisten sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="b597d-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="b597d-152">Tämä integraatio tekee Microsoft Dynamics 365:stä yhden pysähdyksen kaupan kaikille liiketoimintasovelluksille.</span><span class="sxs-lookup"><span data-stu-id="b597d-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="b597d-153">Asiakkaat, jotka käyttävät Dynamics 365 Finance- ja Dynamics 365 Supply Chain Management -sovellusta, mutta jotka käyttävät asiakkuudenhallintaan (CRM) jotain muuta kuin Microsoftin ratkaisua, siirtyvät kohti Dynamics 365:ttä sen kaksoiskirjoitustuen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="b597d-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="b597d-154">Asiakkaiden, tuotteiden, toimintojen, projektien ja esineiden internetin tiedot siirtyvät automaattisesti Common Data Serviceen kaksoiskirjoituksen kautta.</span><span class="sxs-lookup"><span data-stu-id="b597d-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="b597d-155">Tämä yhteys on erittäin hyödyllinen yrityksille, jotka ovat kiinnostuneita Microsoft Power Platform -laajennuksista.</span><span class="sxs-lookup"><span data-stu-id="b597d-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="b597d-156">Kaksoiskirjoitusinfrastruktuuri noudattaa kooditonta / vähäisen koodin periaatetta.</span><span class="sxs-lookup"><span data-stu-id="b597d-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="b597d-157">Vakiomuotoisten taulukosta taulukkoon -määritysten ja mukautettujen määritysten laajentamisessa ei tarvita paljon kehitystyötä.</span><span class="sxs-lookup"><span data-stu-id="b597d-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="b597d-158">Kaksoiskirjoitus tukee sekä online- että offline-tilaa.</span><span class="sxs-lookup"><span data-stu-id="b597d-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="b597d-159">Microsoft on ainoa yritys, joka tarjoaa tukea online-ja offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="b597d-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="b597d-160">Mitä kaksoiskirjoituds tarkoittaa CRM-tuotteiden käyttäjille ja suunnittelijoille?</span><span class="sxs-lookup"><span data-stu-id="b597d-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="b597d-161">Kaksoiskirjoitus automatisoi tietovirran Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="b597d-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b597d-162">Tulevissa versioissa Dynamics 365:n mallipohjaisten sovellusten käsitteet (esimerkiksi asiakas, yhteyshenkilö, tarjous ja tilaus) skaalataan keskisuurten ja suurten markkinoiden asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="b597d-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="b597d-163">Ensimmäisessä versiossa kaksoiskirjoitusratkaisut käsittelevät suurinta osaa automaatiosta.</span><span class="sxs-lookup"><span data-stu-id="b597d-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="b597d-164">Tulevissa versioissa näistä ratkaisuista tulee osa Common Data Servicea.</span><span class="sxs-lookup"><span data-stu-id="b597d-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="b597d-165">Common Data Servicen tulevien muutosten ymmärtäminen helpottaa työtä jatkossa.</span><span class="sxs-lookup"><span data-stu-id="b597d-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="b597d-166">Tässä esitellään joitakin tärkeitä muutoksia:</span><span class="sxs-lookup"><span data-stu-id="b597d-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="b597d-167">Common Data Service sisältää uusia käsitteitä, kuten yritys ja osapuoli.</span><span class="sxs-lookup"><span data-stu-id="b597d-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="b597d-168">Nämä käsitteet vaikuttavat kaikkiin Common Data Servicen avulla muodostettuihin sovelluksiin, kuten Dynamics 365 Sales-, Dynamics 365 Marketing-, Dynamics 365 Customer Service- ja Dynamics 365 Field Service -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="b597d-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="b597d-169">Toiminnot ja huomautukset ovat yhtenäisiä ja laajenevat tukemaan sekä C1 (järjestelmän käyttäjät)- että C2 (järjestelmän asiakkaat) -kohteita.</span><span class="sxs-lookup"><span data-stu-id="b597d-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="b597d-170">Tässä esitellään joitakin Common Data Servicen tärkeitä muutoksia:</span><span class="sxs-lookup"><span data-stu-id="b597d-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="b597d-171">Desimaalitietotyyppi korvaa raha-tietotyypin.</span><span class="sxs-lookup"><span data-stu-id="b597d-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="b597d-172">Voimassaolopäivä tukee mennyttä, nykyistä ja tulevaa päivämäärää samassa paikassa.</span><span class="sxs-lookup"><span data-stu-id="b597d-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="b597d-173">Valuutta- ja vaihtokursseja tuetaan aiempaa enemmän ja **Vaihtokurssi**-ohjelmointirajapintaa muutetaan.</span><span class="sxs-lookup"><span data-stu-id="b597d-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="b597d-174">Yksikkömuunnoksia tuetaan.</span><span class="sxs-lookup"><span data-stu-id="b597d-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="b597d-175">Lisätietoja tulevista muutoksista on kohdassa [Common Data Servicen tiedot – vaihe 1 ja 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span><span class="sxs-lookup"><span data-stu-id="b597d-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span></span>
