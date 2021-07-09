---
title: Tietovaraston osajoukon usein kysytyt kysymykset
description: Tämä ohjeaihe sisältää vastauksia eräisiin usein kysyttyihin tietovaraston osajoukon kysymyksiin.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266606"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="b725e-103">Tietovaraston osajoukon usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="b725e-103">Data mart resets FAQ</span></span>

<span data-ttu-id="b725e-104">Tämä ohjeaihe sisältää vastauksia eräisiin usein kysyttyihin tietovaraston osajoukon kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="b725e-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="b725e-105">Tietojen nollaaminen voi olla aika vievä prosessi, eikä se olosuhteista riippuen välttämättä ole tarvittava ratkaisu.</span><span class="sxs-lookup"><span data-stu-id="b725e-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="b725e-106">Siksi tämä ohjeaihe sisältää tietoja olosuhteista, joissa tietojen nollaaminen voi auttaa, sekä olosuhteista, joissa se ei todennäköisesti auta.</span><span class="sxs-lookup"><span data-stu-id="b725e-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="b725e-107">Mikä on tietovaraston osajoukon palauttaminen?</span><span class="sxs-lookup"><span data-stu-id="b725e-107">What is a data mart reset?</span></span>

<span data-ttu-id="b725e-108">Tietojen nollaaminen poistaa integrointitehtävät käytöstä, poistaa kaikki tiedot ja ottaa integroinnin uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b725e-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="b725e-109">Jotta voidaan varmistaa, että vanhoja tietoja ei lisätä, tietojen uudelleen nollaaminen voidaan aloittaa vasta, kun aiemmin luodut tehtävät on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="b725e-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="b725e-110">Jos yrität nollata tiedot ennen kaikkien tehtävien suorittamista, näyttöön voi tulla seuraava sanoma: "Tietojen uudelleen nollaaminen ei onnistunut aktiivisen tehtävän vuoksi.</span><span class="sxs-lookup"><span data-stu-id="b725e-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="b725e-111">Yritä myöhemmin uudelleen."</span><span class="sxs-lookup"><span data-stu-id="b725e-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="b725e-112">Milloin tietovarasto on nollattava?</span><span class="sxs-lookup"><span data-stu-id="b725e-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="b725e-113">Jos jokin seuraavista lausekkeista on voimassa tilanteessasi, organisaatiosi voi käyttää tietojen nollaamista:</span><span class="sxs-lookup"><span data-stu-id="b725e-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="b725e-114">Sovellustietokanta palautettiin.</span><span class="sxs-lookup"><span data-stu-id="b725e-114">The application database was restored.</span></span>
- <span data-ttu-id="b725e-115">Tukipalvelupyyntö on avattu ja tukihenkilö on ohjeistanut nollaamaan tietovaraston vianmääritysvaiheen osana.</span><span class="sxs-lookup"><span data-stu-id="b725e-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="b725e-116">Milloin tietovaraston osajoukon palautus ei kannata?</span><span class="sxs-lookup"><span data-stu-id="b725e-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="b725e-117">Tässä on joitain tilanteita, joissa emme suosittele tietovaraston nollaamista:</span><span class="sxs-lookup"><span data-stu-id="b725e-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="b725e-118">Sinulla on suorituskykyongelmia, jotka liittyvät tietojen synkronointiin.</span><span class="sxs-lookup"><span data-stu-id="b725e-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="b725e-119">Nollausmalli toistuu jonkin seuraavan syyn vuoksi:</span><span class="sxs-lookup"><span data-stu-id="b725e-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="b725e-120">**Puuttuvat tiedot** – Jos havaitset, että tietoja puuttuu, avaa Microsoftille tukipalvelupyyntö, jonka avulla voit tarkistaa raporttisi muodon ja mahdolliset tietojen synkronointiongelmat.</span><span class="sxs-lookup"><span data-stu-id="b725e-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="b725e-121">**Juuttunut integroinnin tila**</span><span class="sxs-lookup"><span data-stu-id="b725e-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="b725e-122">**Vanhentuneet tietueet** – Tietueiden vanhentuminen ei välttämättä edellytä tietovaraston nollaamista.</span><span class="sxs-lookup"><span data-stu-id="b725e-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="b725e-123">Jos tietovarasto on suuri, nollausprosessin suorittaminen kestää jonkin aikaa mutta se ei todennäköisesti johda parannuksiin.</span><span class="sxs-lookup"><span data-stu-id="b725e-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="b725e-124">Jos tietovaraston osajoukko palautetaan, menetetäänkö jo suunnitellut raportit?</span><span class="sxs-lookup"><span data-stu-id="b725e-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="b725e-125">Et voi.</span><span class="sxs-lookup"><span data-stu-id="b725e-125">No.</span></span> <span data-ttu-id="b725e-126">Raportit tallennetaan SQL-tauluihin, joihin tietovaraston osajoukon nollaaminen ei vaikuta.</span><span class="sxs-lookup"><span data-stu-id="b725e-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="b725e-127">Jos olet huolissasi suunnittelemiesi raporttien menettämisestä, voit varmuuskopioida mallit, joita et halua menettää.</span><span class="sxs-lookup"><span data-stu-id="b725e-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="b725e-128">Voit varmuuskopioida suunnitelmasi avaamalla Report Designerin ja valitsemalla **Yritys \> Yritykset \> Rakenneosat \> Vie**.</span><span class="sxs-lookup"><span data-stu-id="b725e-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="b725e-129">Onko kaikkien käyttäjien poistuttava järjestelmästä, ennen kuin voin nollata tiedot?</span><span class="sxs-lookup"><span data-stu-id="b725e-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="b725e-130">Et voi.</span><span class="sxs-lookup"><span data-stu-id="b725e-130">No.</span></span> <span data-ttu-id="b725e-131">Käyttäjät voivat jatkaa järjestelmässä työskentelyä tietovaraston osajoukon nollaamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="b725e-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="b725e-132">Käyttäjät eivät kuitenkaan voi käyttää Financial Reporterilla luotuja raportteja, ennen kuin nollaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="b725e-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
