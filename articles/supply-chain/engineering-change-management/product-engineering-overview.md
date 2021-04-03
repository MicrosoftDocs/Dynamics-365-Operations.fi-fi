---
title: Suunnittelun muutostenhallinnan yleiskuvaus
description: Tässä aiheessa on yleiskatsaus suunnittelun muutostenhallintaan, jonka avulla voi suunnitella ja hallita tuotteen versiointia sekä hallita tuotteen elinkaaria ja suunnittelun muutoksia.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 3fde9194ece4774c4d39785e337caf2413052159
ms.sourcegitcommit: ee7a890e3e4ed6436898e5ab6eff309082a073f8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/18/2021
ms.locfileid: "5476672"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="a609b-103">Suunnittelun muutostenhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="a609b-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="a609b-104">Toiminnon yhteenveto</span><span class="sxs-lookup"><span data-stu-id="a609b-104">Feature summary</span></span>

<span data-ttu-id="a609b-105">Valmistajat tarvitset nykyisin tehokasta tuotetietojen hallintaa, versionhallintaa ja suunnittelun muutoksenhallintaa, jotta ne menestyisivät jatkuvasti lyhenevistä tuotteiden elinkaaresta, kasvavista laatu- ja luotettavuusvaatimuksista sekä entistä tarkemmasta tuotteiden turvallisuustarkkailusta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="a609b-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="a609b-106">Suunnittelun muutostenhallinta tuo rakennetta ja täsmällisyyttä tuotetietojen hallintaprosessiin sekä mahdollistaa tuotteiden hallitun määrittämisen, vapauttamisen ja korjaamiseen työnkulkujen avulla.</span><span class="sxs-lookup"><span data-stu-id="a609b-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="a609b-107"> Tuoteversioiden ja suunnittelun muutostenhallinnan ansiosta suunnittelun muutokset voidaan dokumentoida, niiden vaikutus voidaan arvioida ja ne voidaan ottaa käyttöön koko tuotteen elinkaaren ajan.</span><span class="sxs-lookup"><span data-stu-id="a609b-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="a609b-108">Suunnittelun muutostenhallinta auttaa suunnittelemaan ja hallitsemaan tuotteen versiointia sekä hallitsemaan tuotteen elinkaaria ja suunnittelun muutoksia.</span><span class="sxs-lookup"><span data-stu-id="a609b-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="a609b-109">Tärkeimmät toiminnot:</span><span class="sxs-lookup"><span data-stu-id="a609b-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="a609b-110">Tuotteen versiointi</span><span class="sxs-lookup"><span data-stu-id="a609b-110">Product versioning</span></span>
- <span data-ttu-id="a609b-111">Parannettujen tuotteen vapautustoimintojen avulla voidaan ylläpitää tuotteen päätietoja yhdessä yrityksessä (suunnitteluyritys) ja julkaista täysin määritetyt vapautetut tuotteet muihin yrityksiin</span><span class="sxs-lookup"><span data-stu-id="a609b-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="a609b-112">Säännöt, joilla tarkistetaan, että pakolliset tiedot on annettu ennen tuoteversion aktivointia (valmiustarkistukset)</span><span class="sxs-lookup"><span data-stu-id="a609b-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="a609b-113">Parannettu tuotteen elinkaaren hallinta valvomalla tarkasti, milloin vapautettua tuotetta voidaan käyttää tietyissä liiketoimintaprosesseissa</span><span class="sxs-lookup"><span data-stu-id="a609b-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="a609b-114">Työnkulkujen tukemat suunnittelun muutospyynnöt</span><span class="sxs-lookup"><span data-stu-id="a609b-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="a609b-115">Työnkulkujen tukemat suunnittelun muutostilaukset</span><span class="sxs-lookup"><span data-stu-id="a609b-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="a609b-116">Edellä oleva video ([Dynamics 365 Supply Chain Managementin muutostenhallinnan ominaisuudet](https://youtu.be/N313FqvRuBc)) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavana YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="a609b-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="a609b-117">Ota suunnittelun muutostenhallinnan ja versiodimension toiminnot käyttöön järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="a609b-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="a609b-118">Ennen kuin voit käyttää suunnittelun muutostenhallintaa, sinun on otettava käyttöön sekä *Suunnittelun muutostenhallinta* -toiminto että sen määritysavain.</span><span class="sxs-lookup"><span data-stu-id="a609b-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="a609b-119">Jos haluat seurata myös tapahtumien versiodimensiota (valinnainen), sinun on otettava käyttöön myös *Tuoteversion dimensio* -toiminto ja sen määritysavain.</span><span class="sxs-lookup"><span data-stu-id="a609b-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="a609b-120">Ota toiminnot ensin käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a609b-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="a609b-121">Mene [Toimintojen hallintaan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a609b-121">Go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
1. <span data-ttu-id="a609b-122">Tarkista päivitysten saatavuus.</span><span class="sxs-lookup"><span data-stu-id="a609b-122">Check for updates.</span></span>
1. <span data-ttu-id="a609b-123">Ota käyttöön **Suunnittelun muutostenhallinta** -niminen toiminto.</span><span class="sxs-lookup"><span data-stu-id="a609b-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="a609b-124">Jos haluat käyttää sitä, sinun on otettava käyttöön myös **Tuotteen dimensioversio** -niminen toiminto.</span><span class="sxs-lookup"><span data-stu-id="a609b-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="a609b-125">Ota seuraavaksi määritysavaimet käyttöön seuraavia vaiheita noudattamalla.</span><span class="sxs-lookup"><span data-stu-id="a609b-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="a609b-126">Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="a609b-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="a609b-127">Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="a609b-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="a609b-128">**Kauppa**-solmun laajentaminen</span><span class="sxs-lookup"><span data-stu-id="a609b-128">Expand the **Trade** node</span></span>
1. <span data-ttu-id="a609b-129">Valitse **Suunnittelun muutostenhallinta** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a609b-129">Select the **Engineering Change Management** check box.</span></span>
1. <span data-ttu-id="a609b-130">Jos haluat käyttää sitä, valitse myös **Tuotedimensio – Versio** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a609b-130">If you want to use it, then also select the **Product dimension - Version** check box.</span></span>
1. <span data-ttu-id="a609b-131">Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="a609b-131">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
