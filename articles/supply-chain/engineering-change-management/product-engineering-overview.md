---
title: Suunnittelun muutostenhallinnan yleiskuvaus
description: Tässä aiheessa on yleiskatsaus suunnittelun muutostenhallintaan, jonka avulla voi suunnitella ja hallita tuotteen versiointia sekä hallita tuotteen elinkaaria ja suunnittelun muutoksia.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947517"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="8cebc-103">Suunnittelun muutostenhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="8cebc-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="8cebc-104">Toiminnon yhteenveto</span><span class="sxs-lookup"><span data-stu-id="8cebc-104">Feature summary</span></span>

<span data-ttu-id="8cebc-105">Valmistajat tarvitset nykyisin tehokasta tuotetietojen hallintaa, versionhallintaa ja suunnittelun muutoksenhallintaa, jotta ne menestyisivät jatkuvasti lyhenevistä tuotteiden elinkaaresta, kasvavista laatu- ja luotettavuusvaatimuksista sekä entistä tarkemmasta tuotteiden turvallisuustarkkailusta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="8cebc-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="8cebc-106">Suunnittelun muutostenhallinta tuo rakennetta ja täsmällisyyttä tuotetietojen hallintaprosessiin sekä mahdollistaa tuotteiden hallitun määrittämisen, vapauttamisen ja korjaamiseen työnkulkujen avulla.</span><span class="sxs-lookup"><span data-stu-id="8cebc-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="8cebc-107"> Tuoteversioiden ja suunnittelun muutostenhallinnan ansiosta suunnittelun muutokset voidaan dokumentoida, niiden vaikutus voidaan arvioida ja ne voidaan ottaa käyttöön koko tuotteen elinkaaren ajan.</span><span class="sxs-lookup"><span data-stu-id="8cebc-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="8cebc-108">Suunnittelun muutostenhallinta auttaa suunnittelemaan ja hallitsemaan tuotteen versiointia sekä hallitsemaan tuotteen elinkaaria ja suunnittelun muutoksia.</span><span class="sxs-lookup"><span data-stu-id="8cebc-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="8cebc-109">Tärkeimmät toiminnot:</span><span class="sxs-lookup"><span data-stu-id="8cebc-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="8cebc-110">Tuotteen versiointi</span><span class="sxs-lookup"><span data-stu-id="8cebc-110">Product versioning</span></span>
- <span data-ttu-id="8cebc-111">Parannettujen tuotteen vapautustoimintojen avulla voidaan ylläpitää tuotteen päätietoja yhdessä yrityksessä (suunnitteluyritys) ja julkaista täysin määritetyt vapautetut tuotteet muihin yrityksiin</span><span class="sxs-lookup"><span data-stu-id="8cebc-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="8cebc-112">Säännöt, joilla tarkistetaan, että pakolliset tiedot on annettu ennen tuoteversion aktivointia (valmiustarkistukset)</span><span class="sxs-lookup"><span data-stu-id="8cebc-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="8cebc-113">Parannettu tuotteen elinkaaren hallinta valvomalla tarkasti, milloin vapautettua tuotetta voidaan käyttää tietyissä liiketoimintaprosesseissa</span><span class="sxs-lookup"><span data-stu-id="8cebc-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="8cebc-114">Työnkulkujen tukemat suunnittelun muutospyynnöt</span><span class="sxs-lookup"><span data-stu-id="8cebc-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="8cebc-115">Työnkulkujen tukemat suunnittelun muutostilaukset</span><span class="sxs-lookup"><span data-stu-id="8cebc-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="8cebc-116">Edellä oleva video ([Dynamics 365 Supply Chain Managementin muutostenhallinnan ominaisuudet](https://youtu.be/N313FqvRuBc)) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavana YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="8cebc-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="8cebc-117">Ota suunnittelun muutostenhallinnan ja versiodimension toiminnot käyttöön järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="8cebc-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="8cebc-118">Ennen kuin voit käyttää suunnittelun muutostenhallintaa, sinun on otettava käyttöön sekä *Suunnittelun muutostenhallinta* -toiminto että sen määritysavain.</span><span class="sxs-lookup"><span data-stu-id="8cebc-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="8cebc-119">Jos haluat seurata myös tapahtumien versiodimensiota (valinnainen), sinun on otettava käyttöön myös *Tuoteversion dimensio* -toiminto ja sen määritysavain.</span><span class="sxs-lookup"><span data-stu-id="8cebc-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="8cebc-120">Ota toiminnot ensin käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="8cebc-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="8cebc-121">Valitse [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtila.</span><span class="sxs-lookup"><span data-stu-id="8cebc-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="8cebc-122">Tarkista päivitysten saatavuus.</span><span class="sxs-lookup"><span data-stu-id="8cebc-122">Check for updates.</span></span>
1. <span data-ttu-id="8cebc-123">Ota käyttöön **Suunnittelun muutostenhallinta** -niminen toiminto.</span><span class="sxs-lookup"><span data-stu-id="8cebc-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="8cebc-124">Jos haluat käyttää sitä, sinun on otettava käyttöön myös **Tuotteen dimensioversio** -niminen toiminto.</span><span class="sxs-lookup"><span data-stu-id="8cebc-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="8cebc-125">Ota seuraavaksi määritysavaimet käyttöön seuraavia vaiheita noudattamalla.</span><span class="sxs-lookup"><span data-stu-id="8cebc-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="8cebc-126">Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="8cebc-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="8cebc-127">Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="8cebc-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="8cebc-128">**Kauppa**-solmun laajentaminen.</span><span class="sxs-lookup"><span data-stu-id="8cebc-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="8cebc-129">Ota pääominaisuuden määritysavain käyttöön valitsemalla **Suunnittelun muutostenhallinta** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="8cebc-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** check box.</span></span> <span data-ttu-id="8cebc-130">(Solmua ei tarvitse laajentaa, ellet halua poistaa yhtä tai molempia sen aliominaisuuksista käytöstä.)</span><span class="sxs-lookup"><span data-stu-id="8cebc-130">(It isn't necessary to expand the node unless you also want to disable one or both of its sub-features.)</span></span>
1. <span data-ttu-id="8cebc-131">Jos haluat myös käyttää versiodimensiota, valitse myös **Tuotedimensio – Versio** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="8cebc-131">If you also want to use the version dimension, then select the **Product dimension - Version** check box.</span></span> <span data-ttu-id="8cebc-132">(Tämä valintaruutu on luettelossa alempana, ei **Suunnittelun muutoshallinta** -solmussa.)</span><span class="sxs-lookup"><span data-stu-id="8cebc-132">(This check box is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="8cebc-133">Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="8cebc-133">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cebc-134">Huhtikuussa 2022 alkaen sekä **Suunnittelun muutostenhallinta**- että **Tuotedimensio - Versio** -lisenssiavaimet ovat oletusarvon mukaan käytössä kaikissa uusissa asennuksissa, mutta ne voidaan tarvittaessa poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="8cebc-134">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
