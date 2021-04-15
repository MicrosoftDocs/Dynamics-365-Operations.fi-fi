---
title: Tietovaraston nollaaminen
description: Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, ja tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754141"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="b9c41-103">Tietovaraston nollaaminen</span><span class="sxs-lookup"><span data-stu-id="b9c41-103">When to reset a data mart</span></span>

<span data-ttu-id="b9c41-104">Tietovaraston nollaaminen voi kestää kauan.</span><span class="sxs-lookup"><span data-stu-id="b9c41-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="b9c41-105">Tämä toiminto ei välttämättä ole myöskään kaikkiin tilanteisiin sopiva ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="b9c41-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="b9c41-106">Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, sekä tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.</span><span class="sxs-lookup"><span data-stu-id="b9c41-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="b9c41-107">Milloin tietovarasto on nollattava?</span><span class="sxs-lookup"><span data-stu-id="b9c41-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="b9c41-108">Seuraavia kysymyksiä kannattaa pohtia ennen tietovaraston nollaamista.</span><span class="sxs-lookup"><span data-stu-id="b9c41-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="b9c41-109">Jos vähintään yhteen kysymykseen vastataan myöntävästi, se voi olla osoitus siitä, että tietovaraston nollaamisesta voi olla hyötyä organisaatiolle.</span><span class="sxs-lookup"><span data-stu-id="b9c41-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="b9c41-110">Sovellustietokanta on palautettu, mutta tietovaraston tietokantaa ei palautettu.</span><span class="sxs-lookup"><span data-stu-id="b9c41-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="b9c41-111">Tilikauden tiedoissa on virheitä, eikä syy tähän ole raportin rakenteellinen ongelma.</span><span class="sxs-lookup"><span data-stu-id="b9c41-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="b9c41-112">Tilikauden tiedoissa on virheitä ja raportin suunnitteluohjelman **Integroinnin tila** -sivun yritettyjen integrointien luettelossa on tietueita. (Käynnistä raportin suunnitteluohjelma ja valitset **Työkalut > Integroinnin tila**).</span><span class="sxs-lookup"><span data-stu-id="b9c41-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="b9c41-113">Tukitapaus on avattu ja tukihenkilö on ohjeistanut nollaamaan tietovaraston vianmääritysvaiheen osana.</span><span class="sxs-lookup"><span data-stu-id="b9c41-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="b9c41-114">Milloin tietovarastoa ei kannata nollata?</span><span class="sxs-lookup"><span data-stu-id="b9c41-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="b9c41-115">Joissakin tilanteissa tietovarastoa ei kannata nollata.</span><span class="sxs-lookup"><span data-stu-id="b9c41-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="b9c41-116">Niitä ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="b9c41-116">These include the following.</span></span> 

- <span data-ttu-id="b9c41-117">Nollauksen syytä ei mainita tässä aiheessa.</span><span class="sxs-lookup"><span data-stu-id="b9c41-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="b9c41-118">Suorituskykyongelmat liittyvät tietojen synkronointiin. Tässä tilanteessa tietovaraston nollaamisesta ei ole luultavasti apua.</span><span class="sxs-lookup"><span data-stu-id="b9c41-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="b9c41-119">Nollausmalli toistuu jonkin seuraavan syyn vuoksi:</span><span class="sxs-lookup"><span data-stu-id="b9c41-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="b9c41-120">**Puuttuvat tiedot** – Sulje pois ensin raportin rakenteeseen ja tietojen synkronoinnin ajoittamiseen liittyvät ongelmat. Voit esimerkiksi huomata, että yhdistämismääritystä ei ole suoritettu puuttuvien tietojen kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b9c41-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="b9c41-121">**Juuttunut integroinnin tila** – jos integrointi tapahtuu hitaasti tai näyttää juuttuvan, tietovaraston nollaaminen ei todennäköisesti ratkaise ongelmaa.</span><span class="sxs-lookup"><span data-stu-id="b9c41-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="b9c41-122">**Nollaamisyritykset eivät ole onnistuneet** – jos nollaamista on yritetty useita kertoja eikä se ole onnistunut puuttuvien tietojen vuoksi, suosituksena on tukitapauksen avaaminen ja tilanteen analysointi yhdessä tukihenkilön kanssa, ennen kuin tietovaraston nollaamista yritetään seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="b9c41-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="b9c41-123">**Vanhentuneet tietueet** – Tietueiden vanhentuminen ei välttämättä edellytä tietovaraston nollaamista.</span><span class="sxs-lookup"><span data-stu-id="b9c41-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="b9c41-124">Jos tietovarasto on suuri, nollausprosessin suorittaminen kestää jonkin aikaa mutta tuloksena ei todennäköisesti ole parannuksia.</span><span class="sxs-lookup"><span data-stu-id="b9c41-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="b9c41-125">Tietovaraston nollaamisen ei ole vaikutusta seuraaviin</span><span class="sxs-lookup"><span data-stu-id="b9c41-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="b9c41-126">Nollaus käynnistyy vasta, kun nykyiset tehtävät valmistuvat.</span><span class="sxs-lookup"><span data-stu-id="b9c41-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="b9c41-127">Näin varmistetaan, ettei vanhoja tietoja lisätä.</span><span class="sxs-lookup"><span data-stu-id="b9c41-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="b9c41-128">Tässä vaiheessa voi avautua esimerkiksi seuraavanlainen sanoma: Tietovaraston nollausta ei voitu käsitellä aktiivisen tehtävän vuoksi.</span><span class="sxs-lookup"><span data-stu-id="b9c41-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="b9c41-129">Yritä myöhemmin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b9c41-129">Please try again later.”</span></span>
- <span data-ttu-id="b9c41-130">Nollaus poistaa integrointitehtävät käytöstä ja poistaa kaikki tietovaraston tiedot.</span><span class="sxs-lookup"><span data-stu-id="b9c41-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="b9c41-131">Integrointi otetaan uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b9c41-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="b9c41-132">Seuraavaksi määritetään kaksi seikkaa, joita tietovaraston nollaus *ei* tee.</span><span class="sxs-lookup"><span data-stu-id="b9c41-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="b9c41-133">Nollaukset eivät tyhjennä raportin rakenteita.</span><span class="sxs-lookup"><span data-stu-id="b9c41-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="b9c41-134">Nollaukset eivät tyhjennä yritystietoja tai käyttäjätietoja, ellei niitä ole valittu.</span><span class="sxs-lookup"><span data-stu-id="b9c41-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]