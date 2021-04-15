---
title: Tietokannan lokikirjauksen määrittäminen ja hallinta
description: Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801332"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="653b5-103">Tietokannan lokikirjauksen määrittäminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="653b5-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="653b5-104">Voit seurata Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia tietokantakirjausten avulla.</span><span class="sxs-lookup"><span data-stu-id="653b5-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="653b5-105">Tässä ohjeaiheessa käsitellään seuraavia:</span><span class="sxs-lookup"><span data-stu-id="653b5-105">This topic describes how to:</span></span>

- <span data-ttu-id="653b5-106">Tietokantakirjauksen suojauksen ja suorituskyvyn hallinta</span><span class="sxs-lookup"><span data-stu-id="653b5-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="653b5-107">Määritä tietokantakirjaus</span><span class="sxs-lookup"><span data-stu-id="653b5-107">Set up database logging</span></span>
- <span data-ttu-id="653b5-108">Tietokantalokien tyhjentäminen</span><span class="sxs-lookup"><span data-stu-id="653b5-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="653b5-109">Tietokantakirjauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="653b5-109">Overview of database logging</span></span>

<span data-ttu-id="653b5-110">Tietokantakirjaus seuraa Microsoft Dynamics 365 Human Resourcesin taulukoiden ja kenttien muutoksia.</span><span class="sxs-lookup"><span data-stu-id="653b5-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="653b5-111">Lisääminen, päivittäminen tai poistaminen ovat tällaisia muutoksia.</span><span class="sxs-lookup"><span data-stu-id="653b5-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="653b5-112">Tietokantakirjaus tallentaa tietueen taulukoiden tai kenttien muutoksista tietokantakirjaustaulukkoon.</span><span class="sxs-lookup"><span data-stu-id="653b5-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="653b5-113">Tietokantakirjauksen käyttötapoja liiketoiminnassa:</span><span class="sxs-lookup"><span data-stu-id="653b5-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="653b5-114">Arkaluonteisia tietoja sisältäviin taulukoihin tehtyjen muutosten seurantatietueen luominen.</span><span class="sxs-lookup"><span data-stu-id="653b5-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="653b5-115">Yksittäisten tapahtumien seuraaminen.</span><span class="sxs-lookup"><span data-stu-id="653b5-115">Tracking single transactions.</span></span> <span data-ttu-id="653b5-116">Tietokantakirjausta ei ole tarkoitettu erätöissä suoritettavien automaattisten tapahtumien seuraamiseen.</span><span class="sxs-lookup"><span data-stu-id="653b5-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="653b5-117">Tietokantakirjauksen suojaus</span><span class="sxs-lookup"><span data-stu-id="653b5-117">Security for database logging</span></span>

<span data-ttu-id="653b5-118">Tietokantalokeissa voi olla arkaluonteisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="653b5-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="653b5-119">Lokitietojen käyttöoikeuden voi rajoittaa vain niille käyttöoikeusrooleille, joiden on voitava käyttää näitä tietoja.</span><span class="sxs-lookup"><span data-stu-id="653b5-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="653b5-120">Tietokantakirjaus ja suorituskyky</span><span class="sxs-lookup"><span data-stu-id="653b5-120">Database logging and performance</span></span>

<span data-ttu-id="653b5-121">Vaikka tietokantakirjaus voi olla arvokasta liiketoiminnan kannalta, se voi kuluttaa paljon resursseja ja edellyttää paljon hallintaa.</span><span class="sxs-lookup"><span data-stu-id="653b5-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="653b5-122">Tietokantakirjauksen vaikutukset suorituskykyyn:</span><span class="sxs-lookup"><span data-stu-id="653b5-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="653b5-123">Tietokantalokitaulukon koko voi kasvaa nopeasti, mikä puolestaan voi kasvattaa tietokannan kokoa.</span><span class="sxs-lookup"><span data-stu-id="653b5-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="653b5-124">Kasvu määräytyy sen mukaan, kuinka paljon lokiin kirjattuja tietoja päätät säilyttää.</span><span class="sxs-lookup"><span data-stu-id="653b5-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="653b5-125">Tietokantalokitaulukko sisältää oletusarvoisesti vain 30 päivän lokitiedot.</span><span class="sxs-lookup"><span data-stu-id="653b5-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="653b5-126">Tietokantakirjaus voi heikentää pitkäkestoisia automaattisia prosesseja, kuten pitkään kestäviä tietojen tuontia.</span><span class="sxs-lookup"><span data-stu-id="653b5-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="653b5-127">Parhaat käytännöt</span><span class="sxs-lookup"><span data-stu-id="653b5-127">Best practices</span></span>

<span data-ttu-id="653b5-128">Voit parantaa suorituskykyä rajaamalla lokikirjausten määrää ja valitsemalla lokiin tiettyjä kenttiä koko taulujen sijaan.</span><span class="sxs-lookup"><span data-stu-id="653b5-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="653b5-129">Kokonaissuorituskykyä ylläpidetään rajoittamalla tietokantakirjaus 20 taulukkoon.</span><span class="sxs-lookup"><span data-stu-id="653b5-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="653b5-130">Yksittäisten kenttien osalta lokiin voidaan kirjata vain päivitykset.</span><span class="sxs-lookup"><span data-stu-id="653b5-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="653b5-131">Määritä tietokantakirjaus</span><span class="sxs-lookup"><span data-stu-id="653b5-131">Set up database logging</span></span>

<span data-ttu-id="653b5-132">Tietokantakirjauksen voi määrittää käyttämällä ohjattua **Tietokantamuutosten kirjaaminen lokiin** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="653b5-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="653b5-133">Ohjattu toiminto on joustava tapa määrittää taulukoiden tai kenttien lokiin kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="653b5-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="653b5-134">Valitse **Järjestelmänvalvoja > Linkit > Tietokanta > Tietokantalokin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="653b5-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="653b5-135">Käynnistä ohjattu **Tietokantamuutosten kirjaaminen lokiin** -toiminto valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="653b5-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="653b5-136">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="653b5-136">Select **Next**.</span></span> 
3. <span data-ttu-id="653b5-137">Valitse ohjatun toiminnon **Taulut ja kentät** -sivulla taulut ja kentät, joille tietokannan lokiin kirjaamisen haluat ottaa käyttöön, ja valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="653b5-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="653b5-138">Tietokannan lokiinkirjaus ei ole käytettävissä kaikissa Human Resources -tietokannan taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="653b5-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="653b5-139">Jos valitset **Näytä kaikki taulukot** luettelon alapuolella taulujen ja kenttien luettelo laajennetaan näyttämään kaikkien ne tietokantataulut, joiden tietokantaloki on käytettävissä, mutta tämä on kaikkien tietokantataulujen luettelon osajoukko.</span><span class="sxs-lookup"><span data-stu-id="653b5-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="653b5-140">Valitse ohjatun toiminnon **Muutostyypit**-sivulla tietotoiminnot, joiden muutoksia haluat seurata kullekin taululle ja kentälle, ja valitse sitten **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="653b5-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="653b5-141">Alla olevassa taulukossa on lokiin kirjattavissa olevien tietotoimintojen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="653b5-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="653b5-142">Tarkista tehdyt muutokset **Valmis**-sivulla ja valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="653b5-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="653b5-143">Toiminto</span><span class="sxs-lookup"><span data-stu-id="653b5-143">Operation</span></span> | <span data-ttu-id="653b5-144">kuvaus</span><span class="sxs-lookup"><span data-stu-id="653b5-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="653b5-145">Seuraa uusia tapahtumia</span><span class="sxs-lookup"><span data-stu-id="653b5-145">Track new transactions</span></span> | <span data-ttu-id="653b5-146">Luo loki tauluun luoduille uusille tietueille.</span><span class="sxs-lookup"><span data-stu-id="653b5-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="653b5-147">Päivitys</span><span class="sxs-lookup"><span data-stu-id="653b5-147">Update</span></span> | <span data-ttu-id="653b5-148">Luo loki taulutietueiden päivitystä varten tai taulun yksittäisten kenttien päivitykselle.</span><span class="sxs-lookup"><span data-stu-id="653b5-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="653b5-149">Jos kirjaat lokiin taulun päivitykset, lokitietue luodaan aina, kun taulun mihin tahansa tietueen kenttään tehdään päivitys.</span><span class="sxs-lookup"><span data-stu-id="653b5-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="653b5-150">Jos kirjaat lokiin tiettyjen kenttien päivitykset, lokitietue luodaan vain, kun taulutietueiden kyseisiin kenttiin tehdään päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="653b5-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="653b5-151">Delete-näppäin</span><span class="sxs-lookup"><span data-stu-id="653b5-151">Delete</span></span> | <span data-ttu-id="653b5-152">Luo loki taulusta poistettuja tietueita varten.</span><span class="sxs-lookup"><span data-stu-id="653b5-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="653b5-153">Nimeä tunnus uudelleen</span><span class="sxs-lookup"><span data-stu-id="653b5-153">Rename key</span></span> | <span data-ttu-id="653b5-154">Luo lokitietue, kun taulun avain nimetään uudelleen.</span><span class="sxs-lookup"><span data-stu-id="653b5-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="653b5-155">Tietokantalokien tyhjentäminen</span><span class="sxs-lookup"><span data-stu-id="653b5-155">Clean up database logs</span></span>

<span data-ttu-id="653b5-156">Voit poistaa kaikki tietokantalokit tai osan niistä seuraavien vaihtoehtojen avulla:</span><span class="sxs-lookup"><span data-stu-id="653b5-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="653b5-157">Valitse kaikki tietyn taulukon lokit.</span><span class="sxs-lookup"><span data-stu-id="653b5-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="653b5-158">Valitse tietyntyyppiset tietokantalokit,</span><span class="sxs-lookup"><span data-stu-id="653b5-158">Select specific types of database log.</span></span>
- <span data-ttu-id="653b5-159">Valitse päivämäärä ja aika, jolloin loki luotiin.</span><span class="sxs-lookup"><span data-stu-id="653b5-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="653b5-160">Tietokantalokin tyhjentäminen määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="653b5-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="653b5-161">Valitse **Järjestelmänvalvoja > Linkit > Tietokanta > Tietokantaloki**.</span><span class="sxs-lookup"><span data-stu-id="653b5-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="653b5-162">Valitse **Tyhjennä loki**.</span><span class="sxs-lookup"><span data-stu-id="653b5-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="653b5-163">Valitse poistettavien lokien valintamenetelmä antamalla jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="653b5-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="653b5-164">Taulun tunnus</span><span class="sxs-lookup"><span data-stu-id="653b5-164">Table ID</span></span>
   - <span data-ttu-id="653b5-165">Lokin tyyppi</span><span class="sxs-lookup"><span data-stu-id="653b5-165">Type of log</span></span>
   - <span data-ttu-id="653b5-166">Luonnin päivämäärä ja aika</span><span class="sxs-lookup"><span data-stu-id="653b5-166">Created date and time</span></span>

3. <span data-ttu-id="653b5-167">Määritä lokin tyhjentämistehtävän suorittamisen ajankohta **Tietokantalokin tyhjentäminen** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="653b5-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="653b5-168">Tietokantalokit ovat oletusarvoisesti käytettävissä 30 päivää.</span><span class="sxs-lookup"><span data-stu-id="653b5-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
