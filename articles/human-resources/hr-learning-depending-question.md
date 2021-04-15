---
title: Tee kysymys edellisen kysymyksen vastauksen perusteella
description: Ehdollisten kysymysten avulla voit määrittää vastaajalle näkyvän seurantakysymyksen aiemman kysymyksen perusteella.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae4a792e53127196aacdf659bb483867d5c17494
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794730"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="9c2fb-103">Tee kysymys edellisen kysymyksen vastauksen perusteella</span><span class="sxs-lookup"><span data-stu-id="9c2fb-103">Make a question dependent on the answer of the previous question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="9c2fb-104">Ehdollisten kysymysten avulla voit määrittää vastaajalle näkyvän seurantakysymyksen aiemman kysymyksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="9c2fb-105">Jos kysymys on esimerkiksi Pidätkö kahvista vai teestä, looginen seurantakysymys voidaan määrittää sen perusteella, valitseeko vastaaja kahvin vai teen.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="9c2fb-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="9c2fb-107">Aiemmin määritetyn kyselylomakkeen etsiminen</span><span class="sxs-lookup"><span data-stu-id="9c2fb-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="9c2fb-108">Siirry kohtaan Kyselylomake > Suunnittelu > Kyselylomakkeet.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="9c2fb-109">Valitse luettelosta WorkFH-kyselylomake.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="9c2fb-110">Kaikkien kysymysten ja alikysymysten lisääminen kyselylomakkeeseen</span><span class="sxs-lookup"><span data-stu-id="9c2fb-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="9c2fb-111">Valitse Kysymykset.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-111">Click Questions.</span></span>
2. <span data-ttu-id="9c2fb-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-112">Click New.</span></span>
3. <span data-ttu-id="9c2fb-113">Valitse Kysymys-kentässä kysymys numero 00016.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="9c2fb-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9c2fb-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9c2fb-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-116">Click Save.</span></span>
7. <span data-ttu-id="9c2fb-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="9c2fb-118">Kyselylomakkeen järjestyksen määrittäminen ehdolliseksi ja kysymyksen määrittäminen sopivan vastauksen perusteella</span><span class="sxs-lookup"><span data-stu-id="9c2fb-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="9c2fb-119">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-119">Click Edit.</span></span>
2. <span data-ttu-id="9c2fb-120">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="9c2fb-121">Valitse Kysymysjärjestys-kentässä Ehdollinen.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="9c2fb-122">Valitse Ehdollinen kysymys.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-122">Click Conditional question.</span></span>
5. <span data-ttu-id="9c2fb-123">Valitse puussa solmu Questions\Explain why you answered the previous question the way you did?</span><span class="sxs-lookup"><span data-stu-id="9c2fb-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="9c2fb-124">Valitse Ensisijainen kysymys -kentässä kysymys numero 00009</span><span class="sxs-lookup"><span data-stu-id="9c2fb-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="9c2fb-125">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9c2fb-126">Syötä Vastaus-kenttään sen vastauksen numerojärjestyksen tunnus, jonka perusteella haluat määrittää kysymyksen.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="9c2fb-127">Syötä esimerkiksi 1 ensimmäiselle vastausvaihtoehdolle.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="9c2fb-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-128">Click Save.</span></span>
10. <span data-ttu-id="9c2fb-129">Valitse puussa solmu Questions\I am paid fairly for the work I do.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="9c2fb-130">Huomaa, että päivitetyssä kysymyksen puussa näkyy riippuvuus.</span><span class="sxs-lookup"><span data-stu-id="9c2fb-130">Note that the question tree updated to show the dependency.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]