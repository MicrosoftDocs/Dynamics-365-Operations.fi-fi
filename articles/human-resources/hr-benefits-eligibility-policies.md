---
title: Etukelpoisuuden käytännöt
description: Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e0c0aa7eebf32fc404e0519c6068b4427e6b87b2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465147"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="e2cf8-103">Etuuskelpoisuuden käytännöt</span><span class="sxs-lookup"><span data-stu-id="e2cf8-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e2cf8-104">Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="e2cf8-105">Luodessasi etuja, voit päättää mitkä edut ovat saatavilla kullekin työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="e2cf8-106">Seuraavassa taulukossa on esimerkkejä eduista, joita voisit antaa käytettäväksi tietyille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="e2cf8-107">Etu</span><span class="sxs-lookup"><span data-stu-id="e2cf8-107">Benefit</span></span>          | <span data-ttu-id="e2cf8-108">Kenelle etu on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="e2cf8-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="e2cf8-109">Sairasvakuutus</span><span class="sxs-lookup"><span data-stu-id="e2cf8-109">Health insurance</span></span> | <span data-ttu-id="e2cf8-110">Kaikki työntekijät</span><span class="sxs-lookup"><span data-stu-id="e2cf8-110">All employees</span></span>                   |
| <span data-ttu-id="e2cf8-111">Matkapuhelin</span><span class="sxs-lookup"><span data-stu-id="e2cf8-111">Mobile phone</span></span>     | <span data-ttu-id="e2cf8-112">Myyntihekilökunta, johtokunta</span><span class="sxs-lookup"><span data-stu-id="e2cf8-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="e2cf8-113">Pysäköintiliput</span><span class="sxs-lookup"><span data-stu-id="e2cf8-113">Parking passes</span></span>   | <span data-ttu-id="e2cf8-114">Johto</span><span class="sxs-lookup"><span data-stu-id="e2cf8-114">Executives</span></span>                      |

<span data-ttu-id="e2cf8-115">Seuraavia osia käytetään luomaan oikeutussääntöjä:</span><span class="sxs-lookup"><span data-stu-id="e2cf8-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="e2cf8-116">Käytäntösäännön tyypit</span><span class="sxs-lookup"><span data-stu-id="e2cf8-116">Policy rule types</span></span>
-   <span data-ttu-id="e2cf8-117">Etukelpoisuuden käytännöt</span><span class="sxs-lookup"><span data-stu-id="e2cf8-117">Benefit eligibility policies</span></span>

<span data-ttu-id="e2cf8-118">Käytäntösääntötyypit määrittävät kyselyn parametrit, joiden avulla voit kehittää tiettyjä käytäntösääntöjä.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="e2cf8-119">Luotuasi käytäntösääntötyypit, voit luoda etu oikeutussääntökäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="e2cf8-120">Käytäntöjen avulla voit luoda ryhmän sääntöjä, jotka koskevat yhtä tai useampaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="e2cf8-121">Jokaisessa käytännössä voit tarkastella mitä vain aiemmin luomistasi edun oikeutussääntötyypeistä.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="e2cf8-122">Sinä määrität säännön laajuuden käytännön sisällä.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="e2cf8-123">Esimerkiksi, jos luot edun oikeutussäännön käytäntösääntötyypin, jonka nimi on **Johtokunta**, voit määrittää mikä sääntö on, sen käytännön sisällä.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="e2cf8-124">Tässä esimerkissä sääntö voisi ilmoittaa, että johtaja-sanan sisältävä työnimike on sisällytettävä sääntöön.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="e2cf8-125">Kun olet määrittänyt säännön tai sääntöjen parametrit, jotka sisältyvät käytäntöön, voit määrittää edun tietyn säännön.</span><span class="sxs-lookup"><span data-stu-id="e2cf8-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]