---
title: Määritysten lopettaminen RCS:n yleisessä säilössä
description: Tässä aiheessa kuavataan määritysten lopettaminen RCS:n yleisessä säilössä.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018730"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="af5e5-103">Määritysten lopettaminen RCS:n yleisessä säilössä</span><span class="sxs-lookup"><span data-stu-id="af5e5-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af5e5-104">Tässä aiheessa kuavataan määrityksen lopettaminen RCS:n yleisessä säilössä.</span><span class="sxs-lookup"><span data-stu-id="af5e5-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="af5e5-105">Aiemmin vain ne konfiguraatiot, joita ei enää tarvita, oli mahdollista poistaa.</span><span class="sxs-lookup"><span data-stu-id="af5e5-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="af5e5-106">Nyt voit kuitenkin merkitä vapautetun konfiguraation **Lopetettu**-arvolla RCS:n yleisessä tietovarastossa.</span><span class="sxs-lookup"><span data-stu-id="af5e5-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="af5e5-107">Tämän toiminnallisuuden avulla voit myös hallita seuraavia:</span><span class="sxs-lookup"><span data-stu-id="af5e5-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="af5e5-108">Toimita etukäteisilmoitukset, kun konfiguraatio on tarkoitus lopettaa.</span><span class="sxs-lookup"><span data-stu-id="af5e5-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="af5e5-109">Sisällytä korvaavaa konfiguraatiota koskevat soveltuvat tiedot.</span><span class="sxs-lookup"><span data-stu-id="af5e5-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="af5e5-110">Määritä tietyn konfiguraation **Tuen päättymispäivämäärä**, joka ilmoittaa käyttäjälle, milloin se lopetetaan.</span><span class="sxs-lookup"><span data-stu-id="af5e5-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="af5e5-111">Kun lopetat konfigurointiversion, voit määrittää seuraavat valinnaiset tiedot:</span><span class="sxs-lookup"><span data-stu-id="af5e5-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="af5e5-112">**Korvauskonfiguraatio**</span><span class="sxs-lookup"><span data-stu-id="af5e5-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="af5e5-113">**Korvaava konfigurointiversio**</span><span class="sxs-lookup"><span data-stu-id="af5e5-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="af5e5-114">**Vapaatekstihuomautus**: Tämän kentän avulla voit antaa dokumentaatiolinkkejä tai viitteitä</span><span class="sxs-lookup"><span data-stu-id="af5e5-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="af5e5-115">**Tuen päättymispäivämäärä**: Tämä kenttä sisältää ehdotetun päivämäärän, johon saakka nykyistä konfiguraatiota/versiota tuetaan.</span><span class="sxs-lookup"><span data-stu-id="af5e5-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="af5e5-116">Tämä päivämäärä on päivitettävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="af5e5-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="af5e5-117">Lopeta konfiguraatio noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="af5e5-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="af5e5-118">Valitse, haluatko lopettaa yhden version vai kaikki versiot, joilla on samat asetukset, yhdessä vaiheessa, määrittämällä **Kaikki versiot** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="af5e5-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="af5e5-119">Määritä **Lopeta**-parametriksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="af5e5-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="af5e5-120">Lopeta konfiguraatiot valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="af5e5-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="af5e5-121">**Lopetuspäivämäärä**-kenttä täytetään, kun tallennat muutokset.</span><span class="sxs-lookup"><span data-stu-id="af5e5-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Konfiguraation lopettamisen tiedot](media/Discontinue-details-2.png)
  
<span data-ttu-id="af5e5-123">Voit palauttaa konfiguraation takaisin **jaetuksi** tai muokata lopetuksen tietoja milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="af5e5-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="af5e5-124">Jos jaat konfiguraation, määritä **Tuen päättymispäivämäärä** ja kaikki muut muut lopettamiseen liittyvät tiedot, jotka osoittavat suunnitelmasi tulevasta lopettamisesta.</span><span class="sxs-lookup"><span data-stu-id="af5e5-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="af5e5-125">Jos haluat jakaa suunniteltua lopettamista koskevat tiedot ennen varsinaista konfiguratiion lopettamista, käyttäjä voi täydentää korvaamiseen liittyvät kentät, mutta jättää **Lopetus**-parametrin arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="af5e5-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="af5e5-126">Lopettaminen ei rajoita työvaiheita konfiguraatioiden avulla.</span><span class="sxs-lookup"><span data-stu-id="af5e5-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="af5e5-127">Konfiguraatioita voi edelleen tuoda, suorittaa tai johtaa – nämä kentät vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="af5e5-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="af5e5-128">Finance tukee tämän tiedon näyttämista versiosta 10.0.14 alkaen</span><span class="sxs-lookup"><span data-stu-id="af5e5-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="af5e5-129">Dynamics 365 Finance tukee lopetustietojen näyttämista versiosta 10.0.14 alkaen.</span><span class="sxs-lookup"><span data-stu-id="af5e5-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="af5e5-130">**Yleinen tietovarasto** -sivulla voit tarkastella lopettamiseen liittyviä ajantasaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="af5e5-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="af5e5-131">Oletusarvoisesti lopetetut konfiguraatiot suodatetaan pois.</span><span class="sxs-lookup"><span data-stu-id="af5e5-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="af5e5-132">**Tuodut konfiguraatiot** (ERSolutionTable) -sivulla näkyvät konfiguraatiot, jotka on jo lopetettu tuomisen aikana.</span><span class="sxs-lookup"><span data-stu-id="af5e5-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="af5e5-133">Jos konfiguraatiot on lopetettu tuonnin jälkeen, lopetustiedot voi synkronoida suorittamalla **Tuo konfiguraatioiden päivitykset** -työn.</span><span class="sxs-lookup"><span data-stu-id="af5e5-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


