---
title: Tietovaraston nollaaminen
description: Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, ja tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988989"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="d09e4-103">Tietovaraston nollaaminen</span><span class="sxs-lookup"><span data-stu-id="d09e4-103">When to reset a data mart</span></span>

<span data-ttu-id="d09e4-104">Tietovaraston nollaaminen voi kestää kauan.</span><span class="sxs-lookup"><span data-stu-id="d09e4-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="d09e4-105">Tämä toiminto ei välttämättä ole myöskään kaikkiin tilanteisiin sopiva ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="d09e4-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="d09e4-106">Tässä aiheessa käsitellään tilanteita, joissa tietovaraston nollaamisesta voi olla apua, sekä tilanteita, joissa tietovaraston nollaamisesta ei todennäköisesti ole apua.</span><span class="sxs-lookup"><span data-stu-id="d09e4-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="d09e4-107">Milloin tietovarasto on nollattava?</span><span class="sxs-lookup"><span data-stu-id="d09e4-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="d09e4-108">Seuraavia kysymyksiä kannattaa pohtia ennen tietovaraston nollaamista.</span><span class="sxs-lookup"><span data-stu-id="d09e4-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="d09e4-109">Jos vähintään yhteen kysymykseen vastataan myöntävästi, se voi olla osoitus siitä, että tietovaraston nollaamisesta voi olla hyötyä organisaatiolle.</span><span class="sxs-lookup"><span data-stu-id="d09e4-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="d09e4-110">Palautettiinko sovellustietokanta?</span><span class="sxs-lookup"><span data-stu-id="d09e4-110">Was the application database restored?</span></span>
- <span data-ttu-id="d09e4-111">Onko tukitapaus avattu ja tukihenkilö on ohjeistanut nollaamaan tietovaraston vianmääritysvaiheen osana?</span><span class="sxs-lookup"><span data-stu-id="d09e4-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="d09e4-112">Milloin tietovarastoa ei kannata nollata?</span><span class="sxs-lookup"><span data-stu-id="d09e4-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="d09e4-113">Joissakin tilanteissa tietovarastoa ei kannata nollata.</span><span class="sxs-lookup"><span data-stu-id="d09e4-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="d09e4-114">Niitä ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="d09e4-114">These include the following.</span></span> 

- <span data-ttu-id="d09e4-115">Sinulla on suorituskykyongelmia, jotka liittyvät tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="d09e4-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="d09e4-116">Nollausmalli toistuu jonkin seuraavan syyn vuoksi:</span><span class="sxs-lookup"><span data-stu-id="d09e4-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="d09e4-117">**Puuttuvat tiedot**</span><span class="sxs-lookup"><span data-stu-id="d09e4-117">**Missing data**</span></span> 
  - <span data-ttu-id="d09e4-118">**Juuttunut integroinnin tila**</span><span class="sxs-lookup"><span data-stu-id="d09e4-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="d09e4-119">**Vanhentuneet tietueet** – Tietueiden vanhentuminen ei välttämättä edellytä tietovaraston nollaamista.</span><span class="sxs-lookup"><span data-stu-id="d09e4-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="d09e4-120">Jos tietovarasto on suuri, nollausprosessin suorittaminen kestää jonkin aikaa mutta tuloksena ei todennäköisesti ole parannuksia.</span><span class="sxs-lookup"><span data-stu-id="d09e4-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="d09e4-121">Mikä on tietovaraston osajoukon palauttaminen?</span><span class="sxs-lookup"><span data-stu-id="d09e4-121">What is a data mart reset?</span></span>
- <span data-ttu-id="d09e4-122">Nollaus käynnistyy vasta, kun nykyiset tehtävät valmistuvat.</span><span class="sxs-lookup"><span data-stu-id="d09e4-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="d09e4-123">Näin varmistetaan, ettei vanhoja tietoja lisätä.</span><span class="sxs-lookup"><span data-stu-id="d09e4-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="d09e4-124">Tässä vaiheessa voi avautua esimerkiksi seuraavanlainen sanoma: Tietovaraston nollausta ei voitu käsitellä aktiivisen tehtävän vuoksi.</span><span class="sxs-lookup"><span data-stu-id="d09e4-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="d09e4-125">Yritä myöhemmin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d09e4-125">Please try again later.”</span></span>
- <span data-ttu-id="d09e4-126">Nollaus poistaa integrointitehtävät käytöstä ja poistaa kaikki tietovaraston tiedot.</span><span class="sxs-lookup"><span data-stu-id="d09e4-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="d09e4-127">Integrointi otetaan uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d09e4-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="d09e4-128">Jos tietovaraston osajoukko palautetaan, menetetäänkö jo suunnitellut raportit?</span><span class="sxs-lookup"><span data-stu-id="d09e4-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="d09e4-129">Ei, raportit tallennetaan SQL-tauluihin, joihin tietovaraston osajoukon nollaaminen ei vaikuta.</span><span class="sxs-lookup"><span data-stu-id="d09e4-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="d09e4-130">Jos olet huolissasi suunnittelemiesi raporttien menettämisestä, voit varmuuskopioida mallit, joita et halua menettää.</span><span class="sxs-lookup"><span data-stu-id="d09e4-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="d09e4-131">Voit varmuuskopioida ne avaamalla Report Designerin ja valitsemalla **Yritys > Yritykset > Rakenneosat > Vie**.</span><span class="sxs-lookup"><span data-stu-id="d09e4-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="d09e4-132">Onko kaikkien käyttäjien tarpeen poistua järjestelmästä tietovaraston osajoukon nollaamiseksi?</span><span class="sxs-lookup"><span data-stu-id="d09e4-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="d09e4-133">Ei, käyttäjät voivat jatkaa järjestelmässä työskentelyä tietovaraston osajoukon nollaamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="d09e4-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="d09e4-134">He eivät kuitenkaan voi käyttää Financial Reporterilla luotuja raportteja, ennen kuin nollaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="d09e4-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
