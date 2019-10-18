---
title: Luo ja määritä lisäsääntörakenteet
description: Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja määrittää lisäsääntörakenteen tilirakenteeseen.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175407"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="53c74-103">Luo ja määritä lisäsääntörakenteet</span><span class="sxs-lookup"><span data-stu-id="53c74-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53c74-104">Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja määrittää lisäsääntörakenteen tilirakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="53c74-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="53c74-105">Opastuksessa käytetään USMF-demoyritystä.</span><span class="sxs-lookup"><span data-stu-id="53c74-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="53c74-106">Luo kehittynyt sääntörakenne</span><span class="sxs-lookup"><span data-stu-id="53c74-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="53c74-107">Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Rakenteet > Lisäsääntörakenteet**.</span><span class="sxs-lookup"><span data-stu-id="53c74-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="53c74-108">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="53c74-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="53c74-109">Kirjoita **Lisäsääntörakenteet**-kenttää sääntörakennetta kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="53c74-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="53c74-110">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="53c74-110">Select **OK**.</span></span>
5. <span data-ttu-id="53c74-111">Valitse **Lisää segmentti**.</span><span class="sxs-lookup"><span data-stu-id="53c74-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="53c74-112">Valitse taloushallinnon dimensio segmenttiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="53c74-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="53c74-113">Esimerkki: **Myymälä**.</span><span class="sxs-lookup"><span data-stu-id="53c74-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="53c74-114">Valitse **Lisää segmentti**.</span><span class="sxs-lookup"><span data-stu-id="53c74-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="53c74-115">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="53c74-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="53c74-116">Käytä lisäsääntörakennetta tilirakenteeseen</span><span class="sxs-lookup"><span data-stu-id="53c74-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="53c74-117">Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Rakenteet > Tilirakenteiden konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="53c74-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="53c74-118">Etsi ja valitse luettelossa tilirakenne, johon haluat käyttää lisäsääntöä.</span><span class="sxs-lookup"><span data-stu-id="53c74-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="53c74-119">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="53c74-119">Select **Edit**.</span></span> <span data-ttu-id="53c74-120">Voit myös valita **Lisäsäännöt**, jolloin sinua pyydetään asettamalla tilirakenne **Luonnos**-tilaan.</span><span class="sxs-lookup"><span data-stu-id="53c74-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="53c74-121">Valitse **Lisäsäännöt**.</span><span class="sxs-lookup"><span data-stu-id="53c74-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="53c74-122">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="53c74-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="53c74-123">Kirjoita arvo **Lisäsääntö**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="53c74-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="53c74-124">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="53c74-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="53c74-125">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="53c74-125">Select **Create**.</span></span>
9. <span data-ttu-id="53c74-126">Valitse **Lisää uusia kriteerejä**.</span><span class="sxs-lookup"><span data-stu-id="53c74-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="53c74-127">Valitse **Missä**-kentässä päätili tai taloushallinnon dimensio.</span><span class="sxs-lookup"><span data-stu-id="53c74-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="53c74-128">Valitse **Käyttäjä**-kentässä vaihtoehto, kuten **on välillä** ja **sisältää**.</span><span class="sxs-lookup"><span data-stu-id="53c74-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="53c74-129">Kirjoita arvo **Arvo**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="53c74-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="53c74-130">Kirjoita **kautta**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="53c74-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="53c74-131">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="53c74-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="53c74-132">Etsi luettelosta lisäsääntörakenne, jota haluat käyttää, kun antamasi ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="53c74-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="53c74-133">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="53c74-133">Select **Add**.</span></span>
17. <span data-ttu-id="53c74-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="53c74-134">Close the page.</span></span>
18. <span data-ttu-id="53c74-135">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="53c74-135">Select **Activate**.</span></span>

