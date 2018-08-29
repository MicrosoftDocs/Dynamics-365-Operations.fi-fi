---
title: "Etukelpoisuuden käytännöt"
description: "Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ae4be70058e61cdbc1d2b063b346b45b023eb9e9
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="9bc18-103">Etukelpoisuuden käytännöt</span><span class="sxs-lookup"><span data-stu-id="9bc18-103">Benefit eligibility policies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9bc18-104">Tässä aiheessa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.</span><span class="sxs-lookup"><span data-stu-id="9bc18-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="9bc18-105">Luodessasi etuja, voit päättää mitkä edut ovat saatavilla kullekin työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="9bc18-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="9bc18-106">Seuraavassa taulukossa on esimerkkejä eduista, joita voisit antaa käytettäväksi tietyille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="9bc18-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="9bc18-107">Etu</span><span class="sxs-lookup"><span data-stu-id="9bc18-107">Benefit</span></span>          | <span data-ttu-id="9bc18-108">Kenelle etu on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="9bc18-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="9bc18-109">Sairasvakuutus</span><span class="sxs-lookup"><span data-stu-id="9bc18-109">Health insurance</span></span> | <span data-ttu-id="9bc18-110">Kaikki työntekijät</span><span class="sxs-lookup"><span data-stu-id="9bc18-110">All employees</span></span>                   |
| <span data-ttu-id="9bc18-111">Matkapuhelin</span><span class="sxs-lookup"><span data-stu-id="9bc18-111">Mobile phone</span></span>     | <span data-ttu-id="9bc18-112">Myyntihekilökunta, johtokunta</span><span class="sxs-lookup"><span data-stu-id="9bc18-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="9bc18-113">Pysäköintiliput</span><span class="sxs-lookup"><span data-stu-id="9bc18-113">Parking passes</span></span>   | <span data-ttu-id="9bc18-114">Johto</span><span class="sxs-lookup"><span data-stu-id="9bc18-114">Executives</span></span>                      |

<span data-ttu-id="9bc18-115">Seuraavia osia käytetään luomaan oikeutussääntöjä:</span><span class="sxs-lookup"><span data-stu-id="9bc18-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="9bc18-116">Käytäntösäännön tyypit</span><span class="sxs-lookup"><span data-stu-id="9bc18-116">Policy rule types</span></span>
-   <span data-ttu-id="9bc18-117">Etukelpoisuuden käytännöt</span><span class="sxs-lookup"><span data-stu-id="9bc18-117">Benefit eligibility policies</span></span>

<span data-ttu-id="9bc18-118">Käytäntösääntötyypit määrittävät kyselyn parametrit, joiden avulla voit kehittää tiettyjä käytäntösääntöjä.</span><span class="sxs-lookup"><span data-stu-id="9bc18-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="9bc18-119">Luotuasi käytäntösääntötyypit, voit luoda etu oikeutussääntökäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="9bc18-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="9bc18-120">Käytäntöjen avulla voit luoda ryhmän sääntöjä, jotka koskevat yhtä tai useampaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="9bc18-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="9bc18-121">Jokaisessa käytännössä voit tarkastella mitä vain aiemmin luomistasi edun oikeutussääntötyypeistä.</span><span class="sxs-lookup"><span data-stu-id="9bc18-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="9bc18-122">Sinä määrität säännön laajuuden käytännön sisällä.</span><span class="sxs-lookup"><span data-stu-id="9bc18-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="9bc18-123">Esimerkiksi, jos luot edun oikeutussäännön käytäntösääntötyypin, jonka nimi on **Johtokunta**, voit määrittää mikä sääntö on, sen käytännön sisällä.</span><span class="sxs-lookup"><span data-stu-id="9bc18-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="9bc18-124">Tässä esimerkissä sääntö saattaa merkitä, että kaikki ammattinimikkeet, jotka sisältävät sanan "johtaja" sisällytetään sääntöön.</span><span class="sxs-lookup"><span data-stu-id="9bc18-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="9bc18-125">Kun olet määrittänyt säännön tai sääntöjen parametrit, jotka sisältyvät käytäntöön, voit määrittää edun tietyn säännön.</span><span class="sxs-lookup"><span data-stu-id="9bc18-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9bc18-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9bc18-126">Additional resources</span></span>
--------

[<span data-ttu-id="9bc18-127">Etuohjelman määrittäminen ja hallinta</span><span class="sxs-lookup"><span data-stu-id="9bc18-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




