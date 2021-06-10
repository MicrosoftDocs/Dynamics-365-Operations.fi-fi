---
title: Etukelpoisuuden käytännöt
description: Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 87a080c47e34a3265afea6494ff1733dac5bc384
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053102"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="0ecaf-103">Etuuskelpoisuuden käytännöt</span><span class="sxs-lookup"><span data-stu-id="0ecaf-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0ecaf-104">Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="0ecaf-105">Luodessasi etuja, voit päättää mitkä edut ovat saatavilla kullekin työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="0ecaf-106">Seuraavassa taulukossa on esimerkkejä eduista, joita voisit antaa käytettäväksi tietyille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="0ecaf-107">Etu</span><span class="sxs-lookup"><span data-stu-id="0ecaf-107">Benefit</span></span>          | <span data-ttu-id="0ecaf-108">Kenelle etu on käytettävissä</span><span class="sxs-lookup"><span data-stu-id="0ecaf-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="0ecaf-109">Sairasvakuutus</span><span class="sxs-lookup"><span data-stu-id="0ecaf-109">Health insurance</span></span> | <span data-ttu-id="0ecaf-110">Kaikki työntekijät</span><span class="sxs-lookup"><span data-stu-id="0ecaf-110">All employees</span></span>                   |
| <span data-ttu-id="0ecaf-111">Matkapuhelin</span><span class="sxs-lookup"><span data-stu-id="0ecaf-111">Mobile phone</span></span>     | <span data-ttu-id="0ecaf-112">Myyntihekilökunta, johtokunta</span><span class="sxs-lookup"><span data-stu-id="0ecaf-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="0ecaf-113">Pysäköintiliput</span><span class="sxs-lookup"><span data-stu-id="0ecaf-113">Parking passes</span></span>   | <span data-ttu-id="0ecaf-114">Johto</span><span class="sxs-lookup"><span data-stu-id="0ecaf-114">Executives</span></span>                      |

<span data-ttu-id="0ecaf-115">Seuraavia osia käytetään luomaan oikeutussääntöjä:</span><span class="sxs-lookup"><span data-stu-id="0ecaf-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="0ecaf-116">Käytäntösäännön tyypit</span><span class="sxs-lookup"><span data-stu-id="0ecaf-116">Policy rule types</span></span>
-   <span data-ttu-id="0ecaf-117">Etukelpoisuuden käytännöt</span><span class="sxs-lookup"><span data-stu-id="0ecaf-117">Benefit eligibility policies</span></span>

<span data-ttu-id="0ecaf-118">Käytäntösääntötyypit määrittävät kyselyn parametrit, joiden avulla voit kehittää tiettyjä käytäntösääntöjä.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="0ecaf-119">Luotuasi käytäntösääntötyypit, voit luoda etu oikeutussääntökäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="0ecaf-120">Käytäntöjen avulla voit luoda ryhmän sääntöjä, jotka koskevat yhtä tai useampaa yritystä.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="0ecaf-121">Jokaisessa käytännössä voit tarkastella mitä vain aiemmin luomistasi edun oikeutussääntötyypeistä.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="0ecaf-122">Sinä määrität säännön laajuuden käytännön sisällä.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="0ecaf-123">Esimerkiksi, jos luot edun oikeutussäännön käytäntösääntötyypin, jonka nimi on **Johtokunta**, voit määrittää mikä sääntö on, sen käytännön sisällä.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="0ecaf-124">Tässä esimerkissä sääntö voisi ilmoittaa, että johtaja-sanan sisältävä työnimike on sisällytettävä sääntöön.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="0ecaf-125">Kun olet määrittänyt säännön tai sääntöjen parametrit, jotka sisältyvät käytäntöön, voit määrittää edun tietyn säännön.</span><span class="sxs-lookup"><span data-stu-id="0ecaf-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]