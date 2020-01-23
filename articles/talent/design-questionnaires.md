---
title: Suunnittele kyselylomakkeita
description: Tässä aiheessa kuvataan kyselylomakkeen luontiprosessia. Ensimmäinen vaihe kyselylomakkeen suunnittelu. Kyselylomakkeen suunnittelu sisältää kysymysten ja vastausten kirjoittamisen lisäksi myös vastausten tallentamisen ja vastausten välillä sarkaimella siirtymisen mahdollistavan rakenteen luomisen.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 7559a986c1a112eb1ccc6069ba5b8eb5c6e5b72b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898732"
---
# <a name="design-questionnaires"></a><span data-ttu-id="980aa-105">Suunnittele kyselylomakkeita</span><span class="sxs-lookup"><span data-stu-id="980aa-105">Design questionnaires</span></span>

<span data-ttu-id="980aa-106">Tässä aiheessa kuvataan kyselylomakkeen luontiprosessia.</span><span class="sxs-lookup"><span data-stu-id="980aa-106">This topic describes the process for creating a questionnaire.</span></span> <span data-ttu-id="980aa-107">Ensimmäinen vaihe kyselylomakkeen suunnittelu.</span><span class="sxs-lookup"><span data-stu-id="980aa-107">The first step is to design the questionnaire.</span></span> <span data-ttu-id="980aa-108">Kyselylomakkeen suunnittelu sisältää kysymysten ja vastausten kirjoittamisen lisäksi myös vastausten tallentamisen ja vastausten välillä sarkaimella siirtymisen mahdollistavan rakenteen luomisen.</span><span class="sxs-lookup"><span data-stu-id="980aa-108">When you design a questionnaire, you not only write the questions and answers, but also create the structure that enables answers to be recorded and tabulated.</span></span> 

<span data-ttu-id="980aa-109">Huolellisesti suunnittelu kyselylomake voi parantaa keräämiesi tietojen laatua.</span><span class="sxs-lookup"><span data-stu-id="980aa-109">A carefully designed questionnaire can help increase the quality of the data that you collect.</span></span> <span data-ttu-id="980aa-110">Huolellisen suunnittelun avulla voit valita kyselylomakkeeseen kulloinkin sopivat vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="980aa-110">Through careful design, you can better select the appropriate options at the appropriate time for a questionnaire.</span></span> <span data-ttu-id="980aa-111">Seuraavat seikat auttavat tehokkaan kyselylomakkeen suunnittelemisessa:</span><span class="sxs-lookup"><span data-stu-id="980aa-111">The following points can help you plan an effective questionnaire:</span></span>

-   <span data-ttu-id="980aa-112">Määritä kyselylomakkeen tarkoitus selvästi, jolloin voit varmistaa, että kysymykset tukevat sitä.</span><span class="sxs-lookup"><span data-stu-id="980aa-112">Clearly define the purpose of the questionnaire to help guarantee that the questions support the purpose.</span></span>
-   <span data-ttu-id="980aa-113">Määritä yksittäinen henkilö tai henkilöryhmä, jonka haluat täyttävän kyselylomakkeen.</span><span class="sxs-lookup"><span data-stu-id="980aa-113">Determine the individual person or the group of people who should complete the questionnaire.</span></span>
-   <span data-ttu-id="980aa-114">Tee kyselylomakkeessa näkyvät kysymykset ja sisällytä mahdolliset vastausvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="980aa-114">Write questions that will appear on the questionnaire, and include answer choices, if applicable.</span></span>
-   <span data-ttu-id="980aa-115">Varmista, että kyselylomake on looginen. Näin vastaajien mielenkiinto sitä kohtaan säilyy.</span><span class="sxs-lookup"><span data-stu-id="980aa-115">Be sure that the questionnaire flows logically, so that respondents remain engaged.</span></span>
-   <span data-ttu-id="980aa-116">Järjestä kysymykset ja vastaukset vastaajille näytettävään järjestykseen.</span><span class="sxs-lookup"><span data-stu-id="980aa-116">Arrange questions and answers in the order that they should be presented to respondents in.</span></span>
-   <span data-ttu-id="980aa-117">Päätä, miten tulokset arvioidaan, jos arviointi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="980aa-117">Decide how the results should be evaluated, if applicable.</span></span>
-   <span data-ttu-id="980aa-118">Päätä, tarvitaanko kyselylomakkeessa lisätoimintoja.</span><span class="sxs-lookup"><span data-stu-id="980aa-118">Decide whether you’ll need additional features.</span></span> <span data-ttu-id="980aa-119">Voit esimerkiksi määrittää, luokitellaanko tulokset ja tulosten luokittelutavan, mahdollisen aikarajan tai sen, ovatko kaikki kysymykset pakollisia.</span><span class="sxs-lookup"><span data-stu-id="980aa-119">For example, determine whether and how results should be categorized, whether a time limit is required, or whether all the questions will be mandatory.</span></span>

<span data-ttu-id="980aa-120">Tämän tilauksen suunnitteluvaihe sisältää neljä tehtäväluokkaa.</span><span class="sxs-lookup"><span data-stu-id="980aa-120">The design phase includes four categories of tasks that you must complete in this order:</span></span>

1.  <span data-ttu-id="980aa-121">Määritä tarvittavat edellytykset.</span><span class="sxs-lookup"><span data-stu-id="980aa-121">Set up prerequisites, as required.</span></span>
2.  <span data-ttu-id="980aa-122">Määritä mahdolliset vastausryhmät ja vastaukset.</span><span class="sxs-lookup"><span data-stu-id="980aa-122">Set up answer groups and answers, if applicable.</span></span>
3.  <span data-ttu-id="980aa-123">Määritä kysymykset ja niiden liitokset vastausryhmiin.</span><span class="sxs-lookup"><span data-stu-id="980aa-123">Set up questions and their association with the answer groups.</span></span>
4.  <span data-ttu-id="980aa-124">Määritä kyselylomake ja liitä siihen kysymykset.</span><span class="sxs-lookup"><span data-stu-id="980aa-124">Set up the questionnaire itself, and attach questions to it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="980aa-125">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="980aa-125">Prerequisites</span></span>
<span data-ttu-id="980aa-126">Joidenkin edellytysten on täytyttävä, ennen kuin kyselylomakkeet, vastaukset ja kysymykset voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="980aa-126">Some prerequisites must be in place before you can create questionnaires, answers, and questions.</span></span> <span data-ttu-id="980aa-127">Kaikkia toimintoja voi kuitenkin käyttää, vaikka kaikki edellytykset eivät täyttyisikään.</span><span class="sxs-lookup"><span data-stu-id="980aa-127">However, not all prerequisites are required for full functionality.</span></span>

### <a name="required"></a><span data-ttu-id="980aa-128">Vaadittu</span><span class="sxs-lookup"><span data-stu-id="980aa-128">Required</span></span>

| <span data-ttu-id="980aa-129">Edellytys</span><span class="sxs-lookup"><span data-stu-id="980aa-129">Prerequisite</span></span>        | <span data-ttu-id="980aa-130">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="980aa-130">Description</span></span>                |
|---------------------|----------------------------|
| <span data-ttu-id="980aa-131">Kyselylomaketyypit</span><span class="sxs-lookup"><span data-stu-id="980aa-131">Questionnaire types</span></span> | <span data-ttu-id="980aa-132">Luokittele kyselylomakkeet.</span><span class="sxs-lookup"><span data-stu-id="980aa-132">Categorize questionnaires.</span></span> |
| <span data-ttu-id="980aa-133">Kysymystyypit</span><span class="sxs-lookup"><span data-stu-id="980aa-133">Question types</span></span>      | <span data-ttu-id="980aa-134">Luokittele kysymykset.</span><span class="sxs-lookup"><span data-stu-id="980aa-134">Categorize questions.</span></span>      |

### <a name="optional"></a><span data-ttu-id="980aa-135">Valinnainen</span><span class="sxs-lookup"><span data-stu-id="980aa-135">Optional</span></span>

| <span data-ttu-id="980aa-136">Edellytys</span><span class="sxs-lookup"><span data-stu-id="980aa-136">Prerequisite</span></span>             | <span data-ttu-id="980aa-137">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="980aa-137">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="980aa-138">Kyselylomakeparametrit</span><span class="sxs-lookup"><span data-stu-id="980aa-138">Questionnaire parameters</span></span> | <span data-ttu-id="980aa-139">Muokkaa perusohjausobjekteja ja kyselylomakkeen oletusasetuksia.</span><span class="sxs-lookup"><span data-stu-id="980aa-139">Modify basic controls and default settings for questionnaires.</span></span> |

### <a name="questionnaire-types"></a><span data-ttu-id="980aa-140">Kyselylomaketyypit</span><span class="sxs-lookup"><span data-stu-id="980aa-140">Questionnaire types</span></span>

<span data-ttu-id="980aa-141">Kyselylomakkeen tyypit ovat pakollisia. Ne on liitettävä kyselylomakkeen luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="980aa-141">Questionnaire types are required and must be assigned when you create a questionnaire.</span></span> <span data-ttu-id="980aa-142">Kyselylomakkeen tyypit auttavat kyselylomakkeiden hallinnassa ja luokittelussa.</span><span class="sxs-lookup"><span data-stu-id="980aa-142">Questionnaire types help you manage and classify questionnaires more easily.</span></span> <span data-ttu-id="980aa-143">Kyselylomaketyyppien avulla voit luokitella kyselylomakkeita ja erottaa ne toisistaan.</span><span class="sxs-lookup"><span data-stu-id="980aa-143">Use questionnaire types to classify questionnaires and differentiate them from each other.</span></span> <span data-ttu-id="980aa-144">Jos esimerkiksi valittavissa on useita kyselylomakkeita, tietyn kyselylomakkeen löytäminen helpottuu, kun suodatat niitä tyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="980aa-144">For example, if you have multiple questionnaires to select from, you can filter them by type to help make it easier to find a particular questionnaire.</span></span> <span data-ttu-id="980aa-145">Seuraavassa on joitakin esimerkkejä kyselylomaketyypeistä:</span><span class="sxs-lookup"><span data-stu-id="980aa-145">Here are some examples of questionnaire types:</span></span>

-   <span data-ttu-id="980aa-146">henkilöstön kehitys</span><span class="sxs-lookup"><span data-stu-id="980aa-146">Human resource development</span></span>
-   <span data-ttu-id="980aa-147">asiakastutkimukset</span><span class="sxs-lookup"><span data-stu-id="980aa-147">Customer surveys</span></span>
-   <span data-ttu-id="980aa-148">Tarkistus</span><span class="sxs-lookup"><span data-stu-id="980aa-148">Review process</span></span>

### <a name="question-types"></a><span data-ttu-id="980aa-149">Kysymystyypit</span><span class="sxs-lookup"><span data-stu-id="980aa-149">Question types</span></span>

<span data-ttu-id="980aa-150">Kysymystyypit ovat pakollisia. Ne on liitettävä kysymykseen luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="980aa-150">Question types are required and must be assigned when you create a question.</span></span> 

<span data-ttu-id="980aa-151">Kysymystyyppien avulla voit luokitella kysymyksiä raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="980aa-151">Use question types to categorize questions for reporting.</span></span> <span data-ttu-id="980aa-152">Kysymystyyppien avulla on myös helppo etsiä kysymyksiä, koska voit käyttää tyyppejä suodattimina **Kysymykset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="980aa-152">Question types also make it easier to find questions, because you can use types as filters on the **Questions** page.</span></span> <span data-ttu-id="980aa-153">Seuraavassa on joitakin esimerkkejä kysymystyypeistä:</span><span class="sxs-lookup"><span data-stu-id="980aa-153">Here are some examples of question types:</span></span>

-   <span data-ttu-id="980aa-154">henkilöstöhallinto</span><span class="sxs-lookup"><span data-stu-id="980aa-154">Human resource</span></span>
-   <span data-ttu-id="980aa-155">liiketoiminnan hallinta</span><span class="sxs-lookup"><span data-stu-id="980aa-155">Managing business</span></span>
-   <span data-ttu-id="980aa-156">kurssin arviointi.</span><span class="sxs-lookup"><span data-stu-id="980aa-156">Course evaluation</span></span>

### <a name="questionnaire-parameters"></a><span data-ttu-id="980aa-157">Kyselylomakeparametrit</span><span class="sxs-lookup"><span data-stu-id="980aa-157">Questionnaire parameters</span></span>

<span data-ttu-id="980aa-158">Kyselylomakeparametrit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="980aa-158">Questionnaire parameters are optional.</span></span> <span data-ttu-id="980aa-159">Organisaation vaatimuksista riippuen ne eivät välttämättä ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="980aa-159">You might not use them, depending on your company’s requirements.</span></span> 

<span data-ttu-id="980aa-160">Kyselylomakeparametrit määrittävät anonyymin tilan, numerosarjan koodit ja kyselylomakkeen viitetyypit.</span><span class="sxs-lookup"><span data-stu-id="980aa-160">Questionnaire parameters define the anonymity, number sequence codes, and reference types of a questionnaire.</span></span> <span data-ttu-id="980aa-161">Kun organisaatio jakelee kyselylomakkeen, anonyymisti vastaamisen vaihtoehtoon tulee kiinnittää huomiota.</span><span class="sxs-lookup"><span data-stu-id="980aa-161">When an organization distributes a questionnaire, the option to allow respondents to remain anonymous might be of concern.</span></span> 

<span data-ttu-id="980aa-162">Numerosarjan koodeja käytetään kysymysten ja vastausten järjestämisessä.</span><span class="sxs-lookup"><span data-stu-id="980aa-162">The number sequence codes are used to organize questions and answers.</span></span> <span data-ttu-id="980aa-163">Arvot liitetään automaattisesti nimikkeisiin näiden numerosarjan koodien perusteella.</span><span class="sxs-lookup"><span data-stu-id="980aa-163">Based on these number sequence codes, values are automatically assigned to items.</span></span> 

<span data-ttu-id="980aa-164">Kaikki parametrit tulee määritettävä, ennen kuin tietoja aletaan luoda.</span><span class="sxs-lookup"><span data-stu-id="980aa-164">You should define all parameters before you begin to create your data.</span></span> <span data-ttu-id="980aa-165">Voit muokata kyselylomakeparametrien asetuksia milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="980aa-165">You can modify the questionnaire parameter settings at any time.</span></span>

## <a name="questionnaire-components"></a><span data-ttu-id="980aa-166">Kyselylomakkeen osat</span><span class="sxs-lookup"><span data-stu-id="980aa-166">Questionnaire components</span></span>
<span data-ttu-id="980aa-167">Kyselylomake muodostuu kolmesta pääelementistä: vastausryhmistä, jotka sisältävät monivalintakysymysten vastaukset, kysymyksistä ja itse kyselylomakkeesta.</span><span class="sxs-lookup"><span data-stu-id="980aa-167">Questionnaires comprise three main elements: answer groups that contain the answers for multiple choice questions, questions, and the questionnaire itself.</span></span><span data-ttu-id="980aa-168"> Voit halutessasi ryhmitellä kyselylomakkeen kysymykset tulosryhmiin.</span><span class="sxs-lookup"><span data-stu-id="980aa-168"> You can optionally group the questions on a questionnaire into result groups.</span></span> <span data-ttu-id="980aa-169">Tulosryhmien avulla voit luokitella kysymykset ja tehdä kyselylomakkeesta lisäanalyysin.</span><span class="sxs-lookup"><span data-stu-id="980aa-169">Result groups let you categorize questions and provide further analysis on the questionnaire.</span></span> 

<span data-ttu-id="980aa-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span><span class="sxs-lookup"><span data-stu-id="980aa-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span></span>

### <a name="answer-groups-and-answers"></a><span data-ttu-id="980aa-171">Vastausryhmät ja vastaukset</span><span class="sxs-lookup"><span data-stu-id="980aa-171">Answer groups and answers</span></span>

<span data-ttu-id="980aa-172">Vastaajat voivat vastata kysymykseen kahdella eri tavalla kysymyksen aiheen mukaan.</span><span class="sxs-lookup"><span data-stu-id="980aa-172">Respondents can answer a question in two ways, depending on the subject of the question:</span></span>

-   <span data-ttu-id="980aa-173">Avointen kysymysten vastausten ei tarvitse olla tietyn muotoisia.</span><span class="sxs-lookup"><span data-stu-id="980aa-173">Open-ended questions don’t require responses in a specific format.</span></span> <span data-ttu-id="980aa-174">Vastaajat voivat kirjoittaa vastauksen tekstinä, numerona, päivämääränä tai aikana.</span><span class="sxs-lookup"><span data-stu-id="980aa-174">Respondents can type a response as text, a number, a date, or a time.</span></span> <span data-ttu-id="980aa-175">Kysymykset edellyttävät vastaajilta yleensä subjektiivisia tietoja kuten mielipiteitä, kuvauksia, arviointeja tai arvioita.</span><span class="sxs-lookup"><span data-stu-id="980aa-175">These questions typically require that the respondents provide subjective information in their answers, such as an opinion, description, evaluation, or estimate.</span></span>
-   <span data-ttu-id="980aa-176">Monivalintakysymykset edellyttävät, että vastaaja valitsee vastauksen mahdollisten oikeiden vastausten luettelosta.</span><span class="sxs-lookup"><span data-stu-id="980aa-176">Closed-ended questions require that the respondent select an answer in a list of possible correct answers.</span></span>

<span data-ttu-id="980aa-177">Voit määrittää monivalintakysymysten mahdollisten vastausten luettelon luomalla vastaukset **Vastausryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="980aa-177">To provide a list of possible answers for closed-ended questions, you can create answers on the **Answer groups** page.</span></span> 

<span data-ttu-id="980aa-178">Vastausryhmät ja vastaukset ovat komponentteja, jotka muodostavat kysymysten luomisessa käytettävien tietojen päätekstiosan.</span><span class="sxs-lookup"><span data-stu-id="980aa-178">Answer groups and answers are components that make up the main body of information that questions are created from.</span></span> <span data-ttu-id="980aa-179">Kun olet luonut vastausryhmän, voit liittää sen kysymykseen **Kysymykset**-sivun **Vastausryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="980aa-179">After you create an answer group, you can associate the answer group with a question in the **Answer group** field on the **Questions** page.</span></span> 

<span data-ttu-id="980aa-180">Vastausryhmää voit käyttää useassa saman kyselylomakkeen kysymyksessä tai useassa eri kyselylomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="980aa-180">An answer group can be used for more than one question on the same questionnaire, and can also be used on more than one questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="980aa-181">Tietojen arviointi vaikeutuu, jos täytetyissä kysymyslomakkeissa käytettyjen vastausryhmien vastausten tekstiä muokataan, eivätkä kyselylomakkeen tulokset välttämättä ole enää voimassa.</span><span class="sxs-lookup"><span data-stu-id="980aa-181">If you modify answer text in answer groups that have already been used on completed questionnaires, data can become difficult to evaluate, and questionnaire results might no longer be valid.</span></span> <span data-ttu-id="980aa-182">Jos vastausryhmää on muutettava, kannattaa ehkä luoda uusi vastausryhmä aiemmin luodun ryhmän muuttamisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="980aa-182">If you must change an answer group, consider creating a new answer group instead of changing an existing one.</span></span> <span data-ttu-id="980aa-183">Kysymykseen tai vastaukseen liitettyjä vastausryhmiä tai vastausryhmiä, joihin on vastattu, ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="980aa-183">You can't delete answer groups that are attached to a question or answer, or that have been answered.</span></span>

### <a name="questions"></a><span data-ttu-id="980aa-184">Kysymykset</span><span class="sxs-lookup"><span data-stu-id="980aa-184">Questions</span></span>

<span data-ttu-id="980aa-185">Kyselylomakkeessa on oltava kysymyksiä.</span><span class="sxs-lookup"><span data-stu-id="980aa-185">A questionnaire must contain questions.</span></span> <span data-ttu-id="980aa-186">Kysymykset voivat olla joko avoimia tai rajattuja.</span><span class="sxs-lookup"><span data-stu-id="980aa-186">Questions can be either open-ended or closed-ended.</span></span>

-   <span data-ttu-id="980aa-187">Avointen kysymysten vastauksia ei ohjata, vaan vastaajat voivat kirjoittaa vastauksensa.</span><span class="sxs-lookup"><span data-stu-id="980aa-187">The responses to open-ended questions aren't controlled, and respondents can type their answers.</span></span>
-   <span data-ttu-id="980aa-188">Monivalintakysymykset vaativat luettelon ennalta määritetyistä vastausvaihtoehdoista. Kysymysten rakenne voidaan määrittää niin, että vastaaja voi valita useita vastauksia.</span><span class="sxs-lookup"><span data-stu-id="980aa-188">Closed-ended questions require a list of predefined response options, and the questions can be structured to let a respondent select multiple responses.</span></span> <span data-ttu-id="980aa-189">Kysymykset tulisi suunnitella siten, että ne houkuttelevat vastaajan antamaan yksityiskohtaisia tietoja. Kysymykset tulee linkittää vastausryhmään, joka sisältää kunkin monivalintakysymyksen vastausvaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="980aa-189">Questions should be designed to elicit specific information from a respondent and must be linked to an answer group that provides the response options for each closed-ended question.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="980aa-190">Vastausryhmät ja vastaukset on luotava ennen monivalintakysymysten määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="980aa-190">Before you can set up closed-ended questions, you must create answer groups and answers.</span></span>

<span data-ttu-id="980aa-191">Kysymykset voidaan järjestää ehdolliseen kysymyshierarkiaan niin, että toissijaiset kysymykset riippuvat edellisen kysymyksen kohdalla valitusta vastauksesta.</span><span class="sxs-lookup"><span data-stu-id="980aa-191">Questions can be arranged in a conditional question hierarchy, so that secondary questions depend on the answer that the respondent selects for the previous question.</span></span> <span data-ttu-id="980aa-192">Voit kirjoittaa kysymykset ensin ja järjestää ne hierarkiaan myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="980aa-192">You can write the questions first and then arrange them into a hierarchy later.</span></span>

## <a name="setting-up-questionnaires"></a><span data-ttu-id="980aa-193">Kyselylomakkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="980aa-193">Setting up questionnaires</span></span>

> [!NOTE]
> <span data-ttu-id="980aa-194">Ennen kyselylomakkeen määrittämistä on määritettävä vastaukset, kysymykset ja edellytykset.</span><span class="sxs-lookup"><span data-stu-id="980aa-194">Before you can set up a questionnaire, you must set up answers, questions, and prerequisites.</span></span> 

<span data-ttu-id="980aa-195">Voit määrittää kullekin kyselylomakkeelle seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="980aa-195">For each questionnaire, you can specify the following information:</span></span>

-   <span data-ttu-id="980aa-196">pakollisiin kysymyksiin vastaamisen kokonaisaika tai aikaraja</span><span class="sxs-lookup"><span data-stu-id="980aa-196">The total time or time limit to answer mandatory questions.</span></span>
-   <span data-ttu-id="980aa-197">kaikkien kysymysten pakollisuus</span><span class="sxs-lookup"><span data-stu-id="980aa-197">Whether all questions are mandatory.</span></span>
-   <span data-ttu-id="980aa-198">lasketaanko kyselylomakkeen pisteiden enimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="980aa-198">Whether to calculate points on a questionnaire.</span></span>
-   <span data-ttu-id="980aa-199">tulosten luokittelutapa</span><span class="sxs-lookup"><span data-stu-id="980aa-199">How to categorize results.</span></span>
-   <span data-ttu-id="980aa-200">kyselylomakkeen käyttäminen rajoitetussa vastaajajoukossa</span><span class="sxs-lookup"><span data-stu-id="980aa-200">Whether the questionnaire will be available to a restricted set of respondents.</span></span>
-   <span data-ttu-id="980aa-201">lomakemallin näyttäminen kyselylomakkeen sivujen taustalla</span><span class="sxs-lookup"><span data-stu-id="980aa-201">Whether a form template should be displayed as a background behind each page of the questionnaire.</span></span>
-   <span data-ttu-id="980aa-202">lisähuomautusten pakollisuus, kun halutaan selventää kyselylomakkeen tarkoitusta vastaajille</span><span class="sxs-lookup"><span data-stu-id="980aa-202">Whether additional notes are required in order to clarify the intent of the questionnaire for the respondents.</span></span>
-   <span data-ttu-id="980aa-203">kysymysten näyttäminen kiinteässä järjestyksessä tai kysymysten valitseminen poolista satunnaisessa järjestyksessä</span><span class="sxs-lookup"><span data-stu-id="980aa-203">Whether to display questions in a fixed order or randomly select them from a pool.</span></span>
-   <span data-ttu-id="980aa-204">kysymysten esittäminen vain silloin, kun edelliset vastaukset sisältävät tiettyjä elementtejä.</span><span class="sxs-lookup"><span data-stu-id="980aa-204">Whether questions will be asked only if specific responses are given for previous answers.</span></span>

### <a name="set-up-a-questionnaire"></a><span data-ttu-id="980aa-205">Kyselylomakkeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="980aa-205">Set up a questionnaire</span></span>

<span data-ttu-id="980aa-206">Ensisijainen sivu, jota käytetään kyselylomakkeen määrittämisessä **Kyselylomakkeet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="980aa-206">The primary page that you use to set up a questionnaire is the **Questionnaires** page.</span></span> <span data-ttu-id="980aa-207">Voit määrittää kyselylomakkeen suorittamalla seuraavat tehtävät järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="980aa-207">To set up a questionnaire, complete the following tasks in order:</span></span>

1.  <span data-ttu-id="980aa-208">Luo kyselylomake.</span><span class="sxs-lookup"><span data-stu-id="980aa-208">Create a questionnaire.</span></span>
2.  <span data-ttu-id="980aa-209">Liitä kyselylomakkeeseen kysymykset näiden vaiheiden avulla:</span><span class="sxs-lookup"><span data-stu-id="980aa-209">Follow one of these steps to attach questions to the questionnaire:</span></span>
    -   <span data-ttu-id="980aa-210">Jos käytössä ovat tulosryhmät, voit liittää kysymykset kyselylomakkeeseen niiden avulla.</span><span class="sxs-lookup"><span data-stu-id="980aa-210">If you're using result groups, you can attach questions to a questionnaire by using result groups.</span></span> <span data-ttu-id="980aa-211">Määritä ensin kyselylomakkeen tulosryhmät ja lisää sitten tulosryhmiin kysymykset.</span><span class="sxs-lookup"><span data-stu-id="980aa-211">First set up the result groups for the questionnaire, and then add questions to the result groups.</span></span>
    -   <span data-ttu-id="980aa-212">Jos tulosryhmät eivät ole käytössä, voit liittää kysymykset suoraan kyselylomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="980aa-212">If you aren't using result groups, you can attach questions directly to the questionnaire.</span></span>

3.  <span data-ttu-id="980aa-213">Määritä ehdollinen kysymyshierarkia, jos se vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="980aa-213">Set up a conditional question hierarchy, if it's required.</span></span>
4.  <span data-ttu-id="980aa-214">Testaa kyselylomake.</span><span class="sxs-lookup"><span data-stu-id="980aa-214">Test the questionnaire.</span></span>

<span data-ttu-id="980aa-215">Valitse **Kyselylomakkeet**-sivulla **Vahvista** testataksesi, onko kyselylomake koottu oikein.</span><span class="sxs-lookup"><span data-stu-id="980aa-215">On the **Questionnaires** page, click **Validate** to test whether the questionnaire is assembled correctly.</span></span> <span data-ttu-id="980aa-216">Kyselylomake kannattaa täyttää ja testata itse ennen sen lähettämistä.</span><span class="sxs-lookup"><span data-stu-id="980aa-216">However, it's also a good idea to complete the questionnaire and test it yourself before you distribute it.</span></span>

### <a name="modify-a-questionnaire"></a><span data-ttu-id="980aa-217">Kyselylomakkeen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="980aa-217">Modify a questionnaire</span></span>

<span data-ttu-id="980aa-218">Voit toteuttaa seuraavat tehtävät **Kyselylomakkeet**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="980aa-218">You can complete the following tasks on the **Questionnaires** page:</span></span>

-   <span data-ttu-id="980aa-219">muokata kyselylomakkeen tietoja, kuten tulosryhmiä ja kysymyksiä</span><span class="sxs-lookup"><span data-stu-id="980aa-219">Modify information in the questionnaire, such as the result groups and questions.</span></span>
-   <span data-ttu-id="980aa-220">poistaa ja lisätä kysymyksiä</span><span class="sxs-lookup"><span data-stu-id="980aa-220">Delete and add questions.</span></span>
-   <span data-ttu-id="980aa-221">muuttaa tulosryhmiä ja järjestysnumeroa.</span><span class="sxs-lookup"><span data-stu-id="980aa-221">Make changes in the result groups and sequence number.</span></span> 

> [!CAUTION]
> <span data-ttu-id="980aa-222">Ole tarkkana, kun teet muutoksia kyselylomakkeisiin, joihin on jo vastattu.</span><span class="sxs-lookup"><span data-stu-id="980aa-222">Be careful when you change questionnaires that have already been answered.</span></span> <span data-ttu-id="980aa-223">Muutosten tekeminen voi vähentää tilastojen ja arviointien tarkkuutta.</span><span class="sxs-lookup"><span data-stu-id="980aa-223">Changes can reduce the accuracy of statistics and therefore make them a poor basis for evaluation.</span></span> <span data-ttu-id="980aa-224">Vastatun kysymyksen muuttamisen sijaan kannattaa luoda uusi kysymys.</span><span class="sxs-lookup"><span data-stu-id="980aa-224">Consider creating a new question instead of changing a question that has already been answered.</span></span>

<span data-ttu-id="980aa-225">Seuraavia kysymystyyppejä ei voi poistaa kyselylomakkeesta:</span><span class="sxs-lookup"><span data-stu-id="980aa-225">In a questionnaire, you can't delete the following types of questions:</span></span>

-   <span data-ttu-id="980aa-226">kyselylomakkeeseen liitetyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="980aa-226">Questions that are attached to a questionnaire</span></span>
-   <span data-ttu-id="980aa-227">kysymykset, joihin on jo vastattu ja jotka näkyvät sen vuoksi **Vastaukset**-valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="980aa-227">Questions that have already been answered and therefore appear in the **Answers** dialog box.</span></span>

### <a name="result-groups"></a><span data-ttu-id="980aa-228">Tulosryhmät</span><span class="sxs-lookup"><span data-stu-id="980aa-228">Result groups</span></span>

<span data-ttu-id="980aa-229">Tulosryhmiä ei ole pakko käyttää, kun kyselylomakkeeseen liitetään kysymyksiä.</span><span class="sxs-lookup"><span data-stu-id="980aa-229">Result groups are optional when you attach questions to a questionnaire.</span></span> 

<span data-ttu-id="980aa-230">Tulosryhmää käytetään pisteiden laskemisessa ja kyselylomakkeen tulosten luokittelussa.</span><span class="sxs-lookup"><span data-stu-id="980aa-230">A result group is used to calculate points and categorize the results of a questionnaire.</span></span> <span data-ttu-id="980aa-231">Jos tulosryhmät ovat käytössä, voit suorittaa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="980aa-231">If you use result groups, you can perform the following tasks:</span></span>

-   <span data-ttu-id="980aa-232">kyselylomakkeen tulosten arvioiminen pistetilastotietojen perusteella</span><span class="sxs-lookup"><span data-stu-id="980aa-232">Evaluate questionnaire results, based on point statistics.</span></span>
-   <span data-ttu-id="980aa-233">vastaajan pisteiden arvioiminen jokaisessa määritetyssä tulosryhmässä.</span><span class="sxs-lookup"><span data-stu-id="980aa-233">Evaluate a respondent’s score for each result group that you set up.</span></span>
-   <span data-ttu-id="980aa-234">Voit luoda kustakin tulosryhmästä tilastotietoja, jos haluat analysoida tuloksia.</span><span class="sxs-lookup"><span data-stu-id="980aa-234">Generate statistics for each result group to help you analyze results.</span></span>
-   <span data-ttu-id="980aa-235">Tulosta raportti, jossa näkyvät kunkin tulosryhmän tulokset sekä valinnaiset pisteet/tekstit, jotka perustuvat samassa tulosryhmässä saatuihin pisteisiin.</span><span class="sxs-lookup"><span data-stu-id="980aa-235">Print a report that shows results for each result group, and also optional points/texts that are based on points that are earned in each result group.</span></span>

> [!NOTE]
> <span data-ttu-id="980aa-236">Seuraavat tehtävät on suoritettava ennen tulosryhmien määrittämistä:</span><span class="sxs-lookup"><span data-stu-id="980aa-236">Before you can set up result groups, you must complete the following tasks:</span></span>

-   <span data-ttu-id="980aa-237">Määritä monivalintakysymykset.</span><span class="sxs-lookup"><span data-stu-id="980aa-237">Set up closed-ended questions.</span></span> <span data-ttu-id="980aa-238">Monivalintakysymysten **Kysymykset**-sivun syöttötyypiksi on määritettävä **valintaruutu**, **vaihtoehtopainike** tai **yhdistelmäruutu**.</span><span class="sxs-lookup"><span data-stu-id="980aa-238">For a closed-ended question, the input type on the **Questions** page must be **Check box**, **Alternative button**, or **Combo box**.</span></span>
-   <span data-ttu-id="980aa-239">Määritä pisteet vastauksille, jotka kuuluvat kuhunkin kysymykseen liitettyyn vastausryhmään.</span><span class="sxs-lookup"><span data-stu-id="980aa-239">Define points for answers in the answer groups that are assigned to each question.</span></span>
-   <span data-ttu-id="980aa-240">Määritä kyselylomake.</span><span class="sxs-lookup"><span data-stu-id="980aa-240">Set up a questionnaire.</span></span>

<span data-ttu-id="980aa-241">Voit liittää kyselylomakkeeseen kysymykset tulosryhmien avulla määrittämällä ensin kyselylomakkeen tulosryhmät ja lisäämällä sitten tulosryhmiin kysymykset.</span><span class="sxs-lookup"><span data-stu-id="980aa-241">To attach questions to a questionnaire by using result groups, first set up the result groups for the questionnaire, and then add questions to the result groups.</span></span> <span data-ttu-id="980aa-242">Jos et käytä tulosryhmiä, voit liittää kysymykset suoraan kyselylomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="980aa-242">If you don't use result groups, you can attach questions directly to a questionnaire.</span></span> 

<span data-ttu-id="980aa-243">Voit määrittää useita tulosryhmiä, kun haluat arvioida vastaajien kussakin luokassa saamat pisteet.</span><span class="sxs-lookup"><span data-stu-id="980aa-243">You can set up multiple result groups to evaluate the points that a respondent earns in each category.</span></span> <span data-ttu-id="980aa-244">Kun kyselylomake on valmis, näkyviin tulevat kussakin tulosryhmässä saadut pisteet.</span><span class="sxs-lookup"><span data-stu-id="980aa-244">After a questionnaire is completed, you can view the points that have been achieved for each result group.</span></span> 

> [!TIP]
> <span data-ttu-id="980aa-245">Voit arvioida kyselylomakkeen käyttämällä pisteitä ilman erillisiä luokkia, kun lisäät kaikki kysymykset yhteen tulosryhmään.</span><span class="sxs-lookup"><span data-stu-id="980aa-245">To evaluate a questionnaire by using points but not separate categories, you can add all questions to a single result group.</span></span> 

<span data-ttu-id="980aa-246">Voit myös määrittää jokaiselle tulosryhmälle vähintään yhden pisteisiin perustuvan sanoman, joka lähetetään vastaajille, kun he ovat täyttäneet kyselylomakkeen.</span><span class="sxs-lookup"><span data-stu-id="980aa-246">For each result group, you can also set up one or more point-based messages that respondents receive after they complete a questionnaire.</span></span> <span data-ttu-id="980aa-247">Näyttöön tuleva teksti voi vaihdella sen mukaan, mitkä pisteet vastaaja on saanut tulosryhmässä.</span><span class="sxs-lookup"><span data-stu-id="980aa-247">The text that is shown can vary, depending on the score that a respondent achieves in a result group.</span></span> <span data-ttu-id="980aa-248">Voit käyttää pisteisiin perustuvia sanomia, kun määrität pistevälit ja kunkin pistevälin kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="980aa-248">To use point-based messages, you must define point intervals and a description of each interval.</span></span> <span data-ttu-id="980aa-249">Kun vastaaja saa tiettyyn pisteväliin kuuluvan tuloksen, kyseiseen pisteväliin liittyvä teksti näkyy tulosraportissa.</span><span class="sxs-lookup"><span data-stu-id="980aa-249">When a respondent achieves a score in a specific interval, the text for that interval is included on the results report.</span></span> 

<span data-ttu-id="980aa-250">Koska tulosryhmä liittyy pisteisiin, jotka on liitetty kyselylomakkeen tiettyihin joukkoihin, voit käyttää vain tiettyä kyselylomakkeen tulosjoukkoa.</span><span class="sxs-lookup"><span data-stu-id="980aa-250">Because a result group is related to the points that are associated with specific sets of questions on a questionnaire, you can use only a specific result group for a questionnaire.</span></span>

#### <a name="example-pointstexts-for-result-group-3"></a><span data-ttu-id="980aa-251">Esimerkki: Pisteiden tai tekstien luominen tulosryhmää 3 varten</span><span class="sxs-lookup"><span data-stu-id="980aa-251">Example: Points/texts for result group 3</span></span>

<span data-ttu-id="980aa-252">Käytössä on johtamistaitotestin kyselylomake, jossa on 15 kysymystä kolmessa eri luokassa.</span><span class="sxs-lookup"><span data-stu-id="980aa-252">You're using a questionnaire for a leadership test that has 15 questions in three categories.</span></span> <span data-ttu-id="980aa-253">Luo kolme tulosryhmää ja lisää kuhunkin tulosryhmään viisi kysymystä.</span><span class="sxs-lookup"><span data-stu-id="980aa-253">You create three result groups and add five questions to each result group.</span></span> <span data-ttu-id="980aa-254">Kolmen ryhmän pisteet lasketaan yhteen.</span><span class="sxs-lookup"><span data-stu-id="980aa-254">Points are then totaled in the three groups.</span></span> <span data-ttu-id="980aa-255">Kolme tulosryhmää ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="980aa-255">The three result groups are as follows:</span></span>

-   <span data-ttu-id="980aa-256">luovat taidot</span><span class="sxs-lookup"><span data-stu-id="980aa-256">Creative abilities</span></span>
-   <span data-ttu-id="980aa-257">johtamistaidot</span><span class="sxs-lookup"><span data-stu-id="980aa-257">Leadership abilities</span></span>
-   <span data-ttu-id="980aa-258">tekniset taidot.</span><span class="sxs-lookup"><span data-stu-id="980aa-258">Technical abilities</span></span>

<span data-ttu-id="980aa-259">Kun käytössä ovat pisteisiin perustuvat viestit, voit määrittää jokaiselle tulosryhmälle tekstivälit.</span><span class="sxs-lookup"><span data-stu-id="980aa-259">To use point-based messages, you set up text intervals for each result group.</span></span> <span data-ttu-id="980aa-260">Jokaiseen kysymykseen liitetään kaksi pistettä.</span><span class="sxs-lookup"><span data-stu-id="980aa-260">Each question is assigned two points.</span></span> <span data-ttu-id="980aa-261">Tämän vuoksi kunkin tulosryhmän enimmäispistemäärä on 10</span><span class="sxs-lookup"><span data-stu-id="980aa-261">Therefore, the maximum point total in each result group is 10.</span></span> 

<span data-ttu-id="980aa-262">Seuraavassa taulussa näkyvät johtamistaidot-tulosryhmälle määritetyt pisteisiin perustuvat sanomat.</span><span class="sxs-lookup"><span data-stu-id="980aa-262">The following table shows the point-based messages that you define for the “leadership abilities” result group.</span></span>

| <span data-ttu-id="980aa-263">Pisteväli</span><span class="sxs-lookup"><span data-stu-id="980aa-263">Point interval</span></span> | <span data-ttu-id="980aa-264">Teksti</span><span class="sxs-lookup"><span data-stu-id="980aa-264">Text</span></span>                                       |
|----------------|--------------------------------------------|
| <span data-ttu-id="980aa-265">1−3</span><span class="sxs-lookup"><span data-stu-id="980aa-265">1 to 3</span></span>         | <span data-ttu-id="980aa-266">Sinulla on keskinkertaiset johtamistaidot.</span><span class="sxs-lookup"><span data-stu-id="980aa-266">You have average leadership abilities.</span></span>     |
| <span data-ttu-id="980aa-267">4−7</span><span class="sxs-lookup"><span data-stu-id="980aa-267">4 to 7</span></span>         | <span data-ttu-id="980aa-268">Sinulla on hyvät johtamistaidot.</span><span class="sxs-lookup"><span data-stu-id="980aa-268">You have good leadership abilities.</span></span>        |
| <span data-ttu-id="980aa-269">8−10</span><span class="sxs-lookup"><span data-stu-id="980aa-269">8 to 10</span></span>        | <span data-ttu-id="980aa-270">Sinulla on loistavat johtamistaidot.</span><span class="sxs-lookup"><span data-stu-id="980aa-270">You have outstanding leadership abilities.</span></span> |

<span data-ttu-id="980aa-271">Voit määrittää pistevälejä ja tekstejä jokaiselle kyselylomakkeen tulosryhmälle.</span><span class="sxs-lookup"><span data-stu-id="980aa-271">You can set up point intervals and texts for each result group on a questionnaire.</span></span> <span data-ttu-id="980aa-272">Kunkin vastaajan tuloksia vastaava teksti näkyy tulosryhmän kohdalla.</span><span class="sxs-lookup"><span data-stu-id="980aa-272">Texts that correspond to each respondent’s score are displayed for each result group.</span></span> 

> [!NOTE]
> <span data-ttu-id="980aa-273">Voit muuttaa välejä ja tekstejä.</span><span class="sxs-lookup"><span data-stu-id="980aa-273">You can change intervals and texts.</span></span> <span data-ttu-id="980aa-274">Jos kyselylomake on täytetty, muutokset voivat aiheuttaa eroja edellisten ja uusien tulosraporttien välillä.</span><span class="sxs-lookup"><span data-stu-id="980aa-274">However, if a questionnaire has been completed, changes might cause differences between previous and new result reports.</span></span>

### <a name="conditional-question-hierarchies"></a><span data-ttu-id="980aa-275">Ehdolliset kysymyshierarkiat</span><span class="sxs-lookup"><span data-stu-id="980aa-275">Conditional question hierarchies</span></span>

<span data-ttu-id="980aa-276">Ehdolliset kysymyshierarkiat ovat valinnaisia kyselylomakkeen määrittämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="980aa-276">Conditional question hierarchies are optional when you set up a questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="980aa-277">Ennen kuin voit määrittää ehdollisen kysymyshierarkian, kyselylomakkeeseen täytyy liittää kysymykset, joille on liitetty kysymysryhmät.</span><span class="sxs-lookup"><span data-stu-id="980aa-277">Before you can set up a conditional question hierarchy, you must attach questions that have assigned answer groups to the questionnaire.</span></span> 

<span data-ttu-id="980aa-278">Jos käytät ehdollisia kysymyksiä kyselylomakkeen kysymyshierarkian luomiseen, voit muodostaa järjestyksen, jossa kysymykset esitetään vastaajan kysymykseen valitseman vastauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="980aa-278">To use conditional questions to create a question hierarchy in a questionnaire, you can make the sequence that questions are presented in depend on the answer that a respondent selects for each question.</span></span> <span data-ttu-id="980aa-279">Kun kysymysten järjestys perustuu vastaajan vastaukseen, voit muokata kyselylomaketta samalla, kun vastaaja täyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="980aa-279">By basing the question sequence on a respondent’s answer, you can modify the questionnaire as the respondent completes it.</span></span>

#### <a name="examples"></a><span data-ttu-id="980aa-280">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="980aa-280">Examples</span></span>

<span data-ttu-id="980aa-281">Yritys tarjoaa asiakkailleen sekä nimikkeitä että palveluita.</span><span class="sxs-lookup"><span data-stu-id="980aa-281">A legal entity offers both items and services to its customers.</span></span> <span data-ttu-id="980aa-282">Tällaisissa tapauksissa käy usein niin, että asiakkaat saattavat ostaa pelkästään tuotteita tai palveluita tai molempia.</span><span class="sxs-lookup"><span data-stu-id="980aa-282">As typically occurs in such cases, some customers purchase only items, some purchase only services, and some purchase both items and services.</span></span> <span data-ttu-id="980aa-283">Ku yritys siis lähettää asiakastyytyväisyyskyselyn, kyselylomakkeeseen lisätään ehdollinen rakenne, jolloin vain palveluita ostaneiden asiakkaiden ei tarvitse vastata nimikkeitä koskeviin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="980aa-283">Therefore, when the legal entity distributes a customer satisfaction survey, it applies a conditional structure to the questionnaire, so that customers who purchase only services don't have to answer questions about items.</span></span> 

<span data-ttu-id="980aa-284">Vaihtoehtoisesti kyselylomakkeen voi määrittää niin, että jos vastaaja valitsee kysymykseen 1 vastaksen A, seuraavaksi esitetään kysymys 2.</span><span class="sxs-lookup"><span data-stu-id="980aa-284">Alternatively, you set up a questionnaire so that if a respondent selects answer A for question 1, question 2 is next in the question sequence.</span></span> <span data-ttu-id="980aa-285">Mutta jos vastaaja valitsee kysymykseen 1 vastauksen B, seuraavaksi esitetään kysymys 5.</span><span class="sxs-lookup"><span data-stu-id="980aa-285">However, if the respondent selects answer B for question 1, question 5 is next.</span></span>

<a name="additional-resources"></a><span data-ttu-id="980aa-286">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="980aa-286">Additional resources</span></span>
--------

[<span data-ttu-id="980aa-287">Kyselylomakkeet</span><span class="sxs-lookup"><span data-stu-id="980aa-287">Questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="980aa-288">Kyselylomakkeiden jakelu ja aikataulutus</span><span class="sxs-lookup"><span data-stu-id="980aa-288">Distribute and schedule questionnaires</span></span>](distribute-questionnaires.md)

[<span data-ttu-id="980aa-289">Kyselylomakkeiden tulosten tarkasteleminen ja arvioiminen</span><span class="sxs-lookup"><span data-stu-id="980aa-289">View and evaluate the results of questionnaires</span></span>](evaluate-questionnaire-results.md)

