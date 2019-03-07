---
title: Kyselylomakkeiden tulosten tarkasteleminen ja arvioiminen
description: Tässä aiheessa kerrotaan, miten vastaajien täyttämien kyselylomakkeiden tuloksia voidaan tarkastella ja arvioida.
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 9fd4af5589cfab2a92c913639f1192029eb7c592
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304273"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="1129f-103">Kyselylomakkeiden tulosten tarkasteleminen ja arvioiminen</span><span class="sxs-lookup"><span data-stu-id="1129f-103">View and evaluate the results of questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1129f-104">Tässä aiheessa kerrotaan, miten vastaajien täyttämien kyselylomakkeiden tuloksia voidaan tarkastella ja arvioida.</span><span class="sxs-lookup"><span data-stu-id="1129f-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="1129f-105">Kun vastaajat ovat täyttäneet kyselylomakkeen, voit tarkastella ja arvioida kyselylomakkeen tuloksia seuraavilla tavoilla.</span><span class="sxs-lookup"><span data-stu-id="1129f-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="1129f-106">**Valmiit vastausistunnot** – Voit tarkastella kyselylomakkeen niitä tietoja, jotka vastaajat ovat täyttäneet, ja luoda yhteenvetoraportteja vastauksista ja saaduista pisteistä.</span><span class="sxs-lookup"><span data-stu-id="1129f-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="1129f-107">**Tulosryhmät** – Voit tarkastella kyselylomakkeiden tulosryhmän tietoja, kuten tilastotietoja.</span><span class="sxs-lookup"><span data-stu-id="1129f-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="1129f-108">Tulosryhmän tilastotiedot voidaan luoda kyselylomakkeen yhdelle vastausistunnolle tai kaikille vastausistuinnoille.</span><span class="sxs-lookup"><span data-stu-id="1129f-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="1129f-109">**Kyselylomakkeen tilastotiedot** – Voit määrittää ehdot, joiden mukaan tietyn vastaajaryhmän tilastotiedot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="1129f-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="1129f-110">Voit luoda erilaisia raportteja myös henkilön, vastausistunnon tai tulosryhmän mukaan lajiteltujen tulosten tarkastelemista varten.</span><span class="sxs-lookup"><span data-stu-id="1129f-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="1129f-111">Käytettävissä ovat seuraavat täytettyihin kyselylomakkeisiin liittyvät raportit:</span><span class="sxs-lookup"><span data-stu-id="1129f-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="1129f-112">Vastaukset</span><span class="sxs-lookup"><span data-stu-id="1129f-112">Answers</span></span>
-   <span data-ttu-id="1129f-113">Kyselylomakekohtaiset kysymykset</span><span class="sxs-lookup"><span data-stu-id="1129f-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="1129f-114">Henkilökohtaiset vastaukset</span><span class="sxs-lookup"><span data-stu-id="1129f-114">Answers per person</span></span>
-   <span data-ttu-id="1129f-115">Palauteanalyysi</span><span class="sxs-lookup"><span data-stu-id="1129f-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="1129f-116">Vastausistunnon tulokset</span><span class="sxs-lookup"><span data-stu-id="1129f-116">Answer session results</span></span>
<span data-ttu-id="1129f-117">Kun vastaajat ovat täyttäneet kyselylomakkeen, voit tarkastella valmiiden vastausistuntojen tuloksia.</span><span class="sxs-lookup"><span data-stu-id="1129f-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="1129f-118">Vastausistunto on yhden käyttäjän vastaus kyselylomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="1129f-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="1129f-119">Voit tarkastella valmiiden vastausistuntojen tietoja **Vastaukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="1129f-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="1129f-120">**Vastaukset**-sivun vastausistunnot suodatetaan eri tavoin riippuen siitä, miten sivu avataan.</span><span class="sxs-lookup"><span data-stu-id="1129f-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="1129f-121">Kaikki kyselylomakkeet</span><span class="sxs-lookup"><span data-stu-id="1129f-121">All questionnaires</span></span>
-   <span data-ttu-id="1129f-122">Tietty kyselylomake</span><span class="sxs-lookup"><span data-stu-id="1129f-122">A specific questionnaire</span></span>
-   <span data-ttu-id="1129f-123">Yksittäinen henkilö</span><span class="sxs-lookup"><span data-stu-id="1129f-123">A specific person</span></span>

<span data-ttu-id="1129f-124">**Vastaukset**-sivulla voit tarkastella vastausten, saatujen pisteiden, vastaajan vastauksia kussakin tulosryhmässä ja valitun kyselylomakkeen mahdollisen kysymyshierarkian tietoja.</span><span class="sxs-lookup"><span data-stu-id="1129f-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="1129f-125">Voit myös luoda ja tulostaa seuraavat raportit:</span><span class="sxs-lookup"><span data-stu-id="1129f-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="1129f-126">**Tulosraportti** – Tämä raportti sisältää graafisen esityksen valitussa vastausistunnossa saaduista pisteitä tulosryhmää kohti.</span><span class="sxs-lookup"><span data-stu-id="1129f-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="1129f-127">**Vastausraportti** – Tämä raportti sisältää vastaajan kyselylomakkeen kuhunkin kysymykseen valitsemat vastaukset.</span><span class="sxs-lookup"><span data-stu-id="1129f-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="1129f-128">**Väärät vastaukset** – Tämä raportti sisältää vastaajan valitsemiin vääriin vastauksiin liittyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="1129f-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="1129f-129">**Huomautus:** **Tulosraportti** on käytettävissä vain, jos kyselylomakkeessa on käytetty tulosryhmiä ja jos **Kyselylomakkeet**-sivun **tulossivu** on valittu.</span><span class="sxs-lookup"><span data-stu-id="1129f-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="1129f-130">**Vastausraportti** ja **väärien vastausten raportti** ovat käytettävissä vain, jos **Kyselylomakkeet**-sivun **vastausraportti** on valittu.</span><span class="sxs-lookup"><span data-stu-id="1129f-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="1129f-131">Kyselylomakkeen tilastotiedot</span><span class="sxs-lookup"><span data-stu-id="1129f-131">Questionnaire statistics</span></span>
<span data-ttu-id="1129f-132">Voit käyttää kyselylomakkeen tilastotietoja, kun haluat analysoida täytettyjen kyselylomakkeiden tulokset määrittämiesi laskelmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="1129f-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="1129f-133">Voit määrittää laskelmat seuraavien tehtävien avulla.</span><span class="sxs-lookup"><span data-stu-id="1129f-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="1129f-134">Valitse tilastotietojen laskemisessa ja näyttämisessä käytettävät ehdot.</span><span class="sxs-lookup"><span data-stu-id="1129f-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="1129f-135">Voit näyttää tilastotiedot kyselylomakkeen, kysymysten, kysymysrivien tai tulosryhmien mukaan.</span><span class="sxs-lookup"><span data-stu-id="1129f-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="1129f-136">Valitse tulosten tarkastelemisessa käytettävä kaaviotyyppi.</span><span class="sxs-lookup"><span data-stu-id="1129f-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="1129f-137">Valitse niiden verkkoon kuuluvien henkilöiden tyypit (työntekijä, yhteyshenkilö tai hakija), joiden vastaukset haluat ottaa mukaan.</span><span class="sxs-lookup"><span data-stu-id="1129f-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="1129f-138">Voit ottaa mukaan myös nimettömästi täytettyjen kyselylomakkeiden vastaukset.</span><span class="sxs-lookup"><span data-stu-id="1129f-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="1129f-139">Määritä tulosten analysoimista varten välit iän tai virkaiän perusteella.</span><span class="sxs-lookup"><span data-stu-id="1129f-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="1129f-140">Tässä välilehdessä voit valita ja tarkistaa tilastoitavan kohteen tarkentavia asetuksia.</span><span class="sxs-lookup"><span data-stu-id="1129f-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="1129f-141">Esimerkiksi valitsemalla postinumeron voit analysoida kyseisellä postinumeroalueella olevien vastaajien tuloksia.</span><span class="sxs-lookup"><span data-stu-id="1129f-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="1129f-142">Valitse tai tarkista ehdot, kun haluat analysoida tulokset vastaajan tai kyselylomakkeen ominaisuuksien perusteella.</span><span class="sxs-lookup"><span data-stu-id="1129f-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="1129f-143">Voit analysoida esimerkiksi vastaajan sijainnin ja oikeiden vastausten välisen korrelaation valitsemalla **Postinumero**.</span><span class="sxs-lookup"><span data-stu-id="1129f-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="1129f-144">Määrittämäsi asetukset tallennetaan ja niitä voidaan käyttää tulosten kausittaiseen uudelleenlaskemiseen.</span><span class="sxs-lookup"><span data-stu-id="1129f-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1129f-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1129f-145">Additional resources</span></span>
--------

[<span data-ttu-id="1129f-146">Kyselylomakkeiden suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="1129f-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="1129f-147">Kyselylomakkeiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="1129f-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="1129f-148">Kyselylomakkeiden jakelu ja täyttäminen</span><span class="sxs-lookup"><span data-stu-id="1129f-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

