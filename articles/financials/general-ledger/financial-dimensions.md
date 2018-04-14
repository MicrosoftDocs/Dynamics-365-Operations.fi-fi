---
title: Taloushallinnon dimensiot
description: "Tässä ohjeaiheessa kerrotaan erityyppisistä taloushallinnon dimensioista ja niiden määrittämisestä."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3d3423b1d3cc235fa10f0a26aa5cd880d08be45b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="financial-dimensions"></a><span data-ttu-id="c86be-103">Taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="c86be-103">Financial dimensions</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c86be-104">Tässä ohjeaiheessa käsitellään erityyppisiä taloushallinnon dimensioita ja niiden määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="c86be-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="c86be-105">Luo **Taloushallinnon dimensiot** -sivun avulla tilikartan tilisegmentteinä käytettäviä taloushallinnon dimensioita.</span><span class="sxs-lookup"><span data-stu-id="c86be-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="c86be-106">Taloushallinnon dimensioita on kahdenlaisia: mukautettuja ja yksikön tukemia dimensioita.</span><span class="sxs-lookup"><span data-stu-id="c86be-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="c86be-107">Mukautetut dimensiot jaetaan yritysten välillä, ja käyttäjät vastaavat arvojen antamisesta ja ylläpidosta.</span><span class="sxs-lookup"><span data-stu-id="c86be-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="c86be-108">Yksikön tukemien dimensioiden arvot määritellään muualla järjestelmässä, esimerkiksi Asiakkaat- tai Myymälät-yksiköissä.</span><span class="sxs-lookup"><span data-stu-id="c86be-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="c86be-109">Jotkin yksikön tukemat dimensiot jaetaan yritysten välillä, kun taas toiset yksikön tukemat dimensiot ovat yrityskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="c86be-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="c86be-110">Kun taloushallinnon dimensiot on luotu, voit liittää jokaiselle taloushallinnon dimensiolle lisää ominaisuuksia **Taloushallinnon dimension arvot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c86be-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="c86be-111">Voit käyttää taloushallinnon dimensiota yritysten esittämiseen.</span><span class="sxs-lookup"><span data-stu-id="c86be-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="c86be-112">Yrityksiä ei tarvitse luoda Microsoft Dynamics 365 for Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="c86be-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c86be-113">Taloushallinnon dimensioita ei kuitenkaan ole suunniteltu käsittelemään yritysten operatiivisia tai liiketoiminnan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="c86be-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="c86be-114">Finance and Operationsin yksiköiden välisen kirjanpidon toiminnallisuus on suunniteltu käsittelemään vain jokaisen tapahtuman luomat kirjanpitomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="c86be-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="c86be-115">Ennen kuin määrität taloushallinnon dimensiot yrityksiksi, arvioi liiketoimintaprosessisi seuraavilla alueilla ja selvitä, voiko tätä asetusta käyttää organisaatiossasi:</span><span class="sxs-lookup"><span data-stu-id="c86be-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="c86be-116">Varasto</span><span class="sxs-lookup"><span data-stu-id="c86be-116">Inventory</span></span>
- <span data-ttu-id="c86be-117">Myynnit ja ostot taloushallinnon dimensioiden ja yritysten välillä</span><span class="sxs-lookup"><span data-stu-id="c86be-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="c86be-118">Arvonlisäveron laskenta ja ilmoittaminen</span><span class="sxs-lookup"><span data-stu-id="c86be-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="c86be-119">Toiminnan raportointi</span><span class="sxs-lookup"><span data-stu-id="c86be-119">Operational reporting</span></span>

<span data-ttu-id="c86be-120">Seuraavassa on joitakin rajoituksia:</span><span class="sxs-lookup"><span data-stu-id="c86be-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="c86be-121">Voit käyttää arvonlisäverotoimintoa ainoastaan yritysten kanssa, et taloushallinnon dimensioiden.</span><span class="sxs-lookup"><span data-stu-id="c86be-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="c86be-122">Jotkin raportit eivät sisällä taloushallinnon dimensioita.</span><span class="sxs-lookup"><span data-stu-id="c86be-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="c86be-123">Tämän vuoksi raportteja on ehkä muokattava taloushallinnon dimension mukaista raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="c86be-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="c86be-124">Mukautetut dimensiot</span><span class="sxs-lookup"><span data-stu-id="c86be-124">Custom dimensions</span></span>

<span data-ttu-id="c86be-125">Voit luoda käyttäjän määrittämän taloushallinnon dimension valitsemalla luoda **Käytä arvoja kohteesta** -kentässä **&lt; Mukautettu dimensio &gt;**.</span><span class="sxs-lookup"><span data-stu-id="c86be-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="c86be-126">Voit määrittää myös tilipeitteen rajoittamaan dimensioarvoille annettavaa summaa ja tietojen tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="c86be-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="c86be-127">Voit antaa jokaisessa dimensioarvossa samana pysyviä arvoja, kuten kirjaimia tai yhdysviivan (-).</span><span class="sxs-lookup"><span data-stu-id="c86be-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="c86be-128">Voit myös antaa numeromerkkejä (\#) ja et-merkkejä (&) kirjaimien ja numerojen paikkamerkkeinä, jotka muuttuvat aina, kun dimensioarvo luodaan.</span><span class="sxs-lookup"><span data-stu-id="c86be-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="c86be-129">Käytä numeromerkkiä (\#) numeron paikkamerkkinä ja et-merkkiä (&) kirjaimen paikkamerkkinä.</span><span class="sxs-lookup"><span data-stu-id="c86be-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="c86be-130">Muotoilupeitteen kenttä on käytettävissä vain, kun valitset **&lt; Mukautettu dimensio &gt;** **Käytä arvoja** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c86be-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="c86be-131">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="c86be-131">**Example**</span></span>

<span data-ttu-id="c86be-132">Jos haluat rajoittaa dimensioarvon kirjaimiin CC ja kolmeen numeroon, anna muotoilupeitteeksi **CC-\#\#\#**.</span><span class="sxs-lookup"><span data-stu-id="c86be-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="c86be-133">Yksikön tukemat dimensiot</span><span class="sxs-lookup"><span data-stu-id="c86be-133">Entity-backed dimensions</span></span>

<span data-ttu-id="c86be-134">Voit luoda yksikön tukeman taloushallinnon dimension valitsemalla **Käytä arvojaa** -kenttään järjestelmän määrittämä yksikkö, johon taloushallinnon dimensio perustuu.</span><span class="sxs-lookup"><span data-stu-id="c86be-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="c86be-135">Taloushallinnon dimensioarvot luodaan sitten tästä yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="c86be-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="c86be-136">Voit esimerkiksi luoda projektien dimensioarvot valitsemalla **Projektit**.</span><span class="sxs-lookup"><span data-stu-id="c86be-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="c86be-137">Jokaiselle projektin nimelle luodaan sitten dimensioarvo.</span><span class="sxs-lookup"><span data-stu-id="c86be-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="c86be-138">Yksikön arvot näkyvät **Taloushallinnon dimension arvot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c86be-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="c86be-139">Jos nämä arvot ovat yrityskohtaisia, myös yritys näkyy sivulla.</span><span class="sxs-lookup"><span data-stu-id="c86be-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="c86be-140">Dimensioiden aktivointi</span><span class="sxs-lookup"><span data-stu-id="c86be-140">Activating dimensions</span></span>

<span data-ttu-id="c86be-141">Kun aktivoit taloushallinnon dimension, taulu päivitetään sisältämään taloushallinnon dimension nimen.</span><span class="sxs-lookup"><span data-stu-id="c86be-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="c86be-142">Poistetut dimensiot poistetaan.</span><span class="sxs-lookup"><span data-stu-id="c86be-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="c86be-143">Voit antaa dimensioarvot ennen taloushallinnon dimension aktivointia.</span><span class="sxs-lookup"><span data-stu-id="c86be-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="c86be-144">Taloushallinnon dimensiota ei voi kuitenkaan kuluttaa missään, ennen kuin se on aktivoitu.</span><span class="sxs-lookup"><span data-stu-id="c86be-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="c86be-145">Et voi esimerkiksi lisätä taloushallinnon dimensiota tilirakenteeseen ennen dimension aktivointia.</span><span class="sxs-lookup"><span data-stu-id="c86be-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="c86be-146">Kun valitset **Aktivoi**, kaikki dimensiot päivitetään ja niiden tilan näytetään muuttuneen.</span><span class="sxs-lookup"><span data-stu-id="c86be-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="c86be-147">Käännökset</span><span class="sxs-lookup"><span data-stu-id="c86be-147">Translations</span></span>

<span data-ttu-id="c86be-148">Voit kirjoittaa valitun taloushallinnon dimension **Tekstin käännös** -sivulla erikielistä tekstiä.</span><span class="sxs-lookup"><span data-stu-id="c86be-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="c86be-149">Voit kirjoittaa päätilille erikielistä tekstiä **Päätilin käännös** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c86be-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="c86be-150">Yrityksen ohitukset</span><span class="sxs-lookup"><span data-stu-id="c86be-150">Legal entity overrides</span></span>

<span data-ttu-id="c86be-151">Kaikkia dimensioita ei voi käyttää kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="c86be-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="c86be-152">Lisäksi jotkin dimensiot voivat liittyä vain tiettyyn jaksoon.</span><span class="sxs-lookup"><span data-stu-id="c86be-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="c86be-153">Näissä tapauksissa voit määrittää **Yrityksen ohitukset** -osassa yritykset, joissa dimension käyttö pitäisi keskeyttää, omistaja sekä ajanjakso, jolloin dimensio on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="c86be-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="c86be-154">Taloushallinnon dimensioiden poistaminen</span><span class="sxs-lookup"><span data-stu-id="c86be-154">Deleting financial dimensions</span></span>

<span data-ttu-id="c86be-155">Tietojen viitteiden eheyden varmistamiseksi taloushallinnon dimensiot voi vain harvoin poistaa.</span><span class="sxs-lookup"><span data-stu-id="c86be-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="c86be-156">Jos yrität poistaa taloushallinnon dimension, seuraavat ehdot arvioidaan:</span><span class="sxs-lookup"><span data-stu-id="c86be-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="c86be-157">Onko taloushallinnon dimensiota käytetty missään kirjatussa tai kirjaamattomassa tapahtumassa tai jossain dimensioarvoyhdistelmässä?</span><span class="sxs-lookup"><span data-stu-id="c86be-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="c86be-158">Onko taloushallinnon dimensiota käytettä missään aktiivisessa tilirakenteessa, lisäasetuksia käyttävässä sääntörakenteessa tai taloushallinnon dimensiojoukossa?</span><span class="sxs-lookup"><span data-stu-id="c86be-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="c86be-159">Onko taloushallinnon dimensio osa oletusarvoista taloushallinnon dimension integrointimuotoa?</span><span class="sxs-lookup"><span data-stu-id="c86be-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="c86be-160">Onko taloushallinnon dimensio määritetty oletusdimensioksi?</span><span class="sxs-lookup"><span data-stu-id="c86be-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="c86be-161">Jos jokin ehdoista täyttyy, et voi poistaa taloushallinnon dimensiota.</span><span class="sxs-lookup"><span data-stu-id="c86be-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="c86be-162">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="c86be-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="c86be-163">Määritä taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="c86be-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="c86be-164">Ylläpidä taloushallinnon dimension oletusmalleja</span><span class="sxs-lookup"><span data-stu-id="c86be-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

