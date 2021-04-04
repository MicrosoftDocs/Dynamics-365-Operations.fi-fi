---
title: Tietokannan lokikirjauksen määrittäminen ja hallinta
description: Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8057ebd0bc061c6bf78d8674c45e0885ffce681c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467646"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="65c10-103">Tietokannan lokikirjauksen määrittäminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="65c10-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="65c10-104">Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla.</span><span class="sxs-lookup"><span data-stu-id="65c10-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="65c10-105">Tässä ohjeaiheessa käsitellään seuraavia:</span><span class="sxs-lookup"><span data-stu-id="65c10-105">This topic describes how to:</span></span>

- <span data-ttu-id="65c10-106">Tietokantakirjauksen suojauksen ja suorituskyvyn hallinta</span><span class="sxs-lookup"><span data-stu-id="65c10-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="65c10-107">Määritä tietokantakirjaus</span><span class="sxs-lookup"><span data-stu-id="65c10-107">Set up database logging</span></span>
- <span data-ttu-id="65c10-108">Tietokantalokien tyhjentäminen</span><span class="sxs-lookup"><span data-stu-id="65c10-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="65c10-109">Tietokantakirjauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="65c10-109">Overview of database logging</span></span>

<span data-ttu-id="65c10-110">Tietokantakirjaus seuraa Microsoft Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia.</span><span class="sxs-lookup"><span data-stu-id="65c10-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="65c10-111">Lisääminen, päivittäminen tai poistaminen ovat tällaisia muutoksia.</span><span class="sxs-lookup"><span data-stu-id="65c10-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="65c10-112">Tietokantakirjaus tallentaa tietueen taulukoiden tai kenttien muutoksista tietokantakirjaustaulukkoon.</span><span class="sxs-lookup"><span data-stu-id="65c10-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="65c10-113">Tietokantakirjauksen käyttötapoja liiketoiminnassa:</span><span class="sxs-lookup"><span data-stu-id="65c10-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="65c10-114">Arkaluonteisia tietoja sisältäviin taulukoihin tehtyjen muutosten seurantatietueen luominen.</span><span class="sxs-lookup"><span data-stu-id="65c10-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="65c10-115">Yksittäisten tapahtumien seuraaminen.</span><span class="sxs-lookup"><span data-stu-id="65c10-115">Tracking single transactions.</span></span> <span data-ttu-id="65c10-116">Tietokantakirjausta ei ole tarkoitettu erätöissä suoritettavien automaattisten tapahtumien seuraamiseen.</span><span class="sxs-lookup"><span data-stu-id="65c10-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="65c10-117">Tietokantakirjauksen suojaus</span><span class="sxs-lookup"><span data-stu-id="65c10-117">Security for database logging</span></span>

<span data-ttu-id="65c10-118">Tietokantalokeissa voi olla arkaluonteisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="65c10-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="65c10-119">Lokitietojen käyttöoikeuden voi rajoittaa vain niille käyttöoikeusrooleille, joiden on voitava käyttää näitä tietoja.</span><span class="sxs-lookup"><span data-stu-id="65c10-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="65c10-120">Tietokantakirjaus ja suorituskyky</span><span class="sxs-lookup"><span data-stu-id="65c10-120">Database logging and performance</span></span>

<span data-ttu-id="65c10-121">Vaikka tietokantakirjaus voi olla arvokasta liiketoiminnan kannalta, se voi kuluttaa paljon resursseja ja edellyttää paljon hallintaa.</span><span class="sxs-lookup"><span data-stu-id="65c10-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="65c10-122">Tietokantakirjauksen vaikutukset suorituskykyyn:</span><span class="sxs-lookup"><span data-stu-id="65c10-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="65c10-123">Tietokantalokitaulukon koko voi kasvaa nopeasti, mikä puolestaan voi kasvattaa tietokannan kokoa.</span><span class="sxs-lookup"><span data-stu-id="65c10-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="65c10-124">Kasvu määräytyy sen mukaan, kuinka paljon lokiin kirjattuja tietoja päätät säilyttää.</span><span class="sxs-lookup"><span data-stu-id="65c10-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="65c10-125">Tietokantalokitaulukko sisältää oletusarvoisesti vain 30 päivän lokitiedot.</span><span class="sxs-lookup"><span data-stu-id="65c10-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="65c10-126">Tietokantakirjaus voi heikentää pitkäkestoisia automaattisia prosesseja, kuten pitkään kestäviä tietojen tuontia.</span><span class="sxs-lookup"><span data-stu-id="65c10-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="65c10-127">Parhaat käytännöt</span><span class="sxs-lookup"><span data-stu-id="65c10-127">Best practices</span></span>

<span data-ttu-id="65c10-128">Voit parantaa suorituskykyä rajaamalla lokikirjausten määrää ja valitsemalla lokiin tiettyjä kenttiä koko taulujen sijaan.</span><span class="sxs-lookup"><span data-stu-id="65c10-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="65c10-129">Kokonaissuorituskykyä ylläpidetään rajoittamalla tietokantakirjaus 20 taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="65c10-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="65c10-130">Yksittäisten kenttien osalta lokiin voidaan kirjata vain päivitykset.</span><span class="sxs-lookup"><span data-stu-id="65c10-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="65c10-131">Määritä tietokantakirjaus</span><span class="sxs-lookup"><span data-stu-id="65c10-131">Set up database logging</span></span>

<span data-ttu-id="65c10-132">Tietokantakirjauksen voi määrittää käyttämällä ohjattua **Tietokantamuutosten kirjaaminen lokiin** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="65c10-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="65c10-133">Ohjattu toiminto on joustava tapa määrittää taulukoiden tai kenttien lokiin kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="65c10-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="65c10-134">Valitse **Järjestelmänvalvoja > Linkit > Tietokanta > Tietokantalokin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="65c10-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="65c10-135">Käynnistä ohjattu **Tietokantamuutosten kirjaaminen lokiin** -toiminto valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="65c10-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="65c10-136">Suorita ohjattu toiminto loppuun.</span><span class="sxs-lookup"><span data-stu-id="65c10-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="65c10-137">Tietokantalokien tyhjentäminen</span><span class="sxs-lookup"><span data-stu-id="65c10-137">Clean up database logs</span></span>

<span data-ttu-id="65c10-138">Voit poistaa kaikki tietokantalokit tai osan niistä seuraavien vaihtoehtojen avulla:</span><span class="sxs-lookup"><span data-stu-id="65c10-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="65c10-139">Valitse kaikki tietyn taulukon lokit.</span><span class="sxs-lookup"><span data-stu-id="65c10-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="65c10-140">Valitse tietyntyyppiset tietokantalokit,</span><span class="sxs-lookup"><span data-stu-id="65c10-140">Select specific types of database log.</span></span>
- <span data-ttu-id="65c10-141">Valitse päivämäärä ja aika, jolloin loki luotiin.</span><span class="sxs-lookup"><span data-stu-id="65c10-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="65c10-142">Tietokantalokin tyhjentäminen määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="65c10-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="65c10-143">Valitse **Järjestelmänvalvoja > Linkit > Tietokanta > Tietokantaloki**.</span><span class="sxs-lookup"><span data-stu-id="65c10-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="65c10-144">Valitse **Tyhjennä loki**.</span><span class="sxs-lookup"><span data-stu-id="65c10-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="65c10-145">Valitse poistettavien lokien valintamenetelmä antamalla jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="65c10-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="65c10-146">Taulun tunnus</span><span class="sxs-lookup"><span data-stu-id="65c10-146">Table ID</span></span>
   - <span data-ttu-id="65c10-147">Lokin tyyppi</span><span class="sxs-lookup"><span data-stu-id="65c10-147">Type of log</span></span>
   - <span data-ttu-id="65c10-148">Luonnin päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="65c10-148">Created date and time</span></span>

3. <span data-ttu-id="65c10-149">Määritä lokin tyhjentämistehtävän suorittamisen ajankohta **Tietokantalokin tyhjentäminen** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="65c10-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="65c10-150">Tietokantalokit ovat oletusarvoisesti käytettävissä 30 päivää.</span><span class="sxs-lookup"><span data-stu-id="65c10-150">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]