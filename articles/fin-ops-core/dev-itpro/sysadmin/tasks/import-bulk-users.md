---
title: Tuo käyttäjiä Azure Active Directorysta
description: Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda manuaalisesti valitut käyttäjät tai suuren määrän käyttäjiä Azure Active Directorysta.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679811"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="20584-103">Tuo käyttäjiä Azure Active Directorysta</span><span class="sxs-lookup"><span data-stu-id="20584-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="20584-104">Tuo valitut käyttäjät</span><span class="sxs-lookup"><span data-stu-id="20584-104">Import select users</span></span>

<span data-ttu-id="20584-105">Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda valitut käyttäjät Azure Active Directorysta (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="20584-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="20584-106">Tuodun käyttäjän oletusyrityksenä on nykyisen istunnon yritys.</span><span class="sxs-lookup"><span data-stu-id="20584-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="20584-107">Muuta nykyistä yritystä tarvittaessa ennen käyttäjien tuomista.</span><span class="sxs-lookup"><span data-stu-id="20584-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="20584-108">Valitse **Järjestelmänhallinta > Käyttäjät > Käyttäjä** t.</span><span class="sxs-lookup"><span data-stu-id="20584-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="20584-109">Valitse **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="20584-109">Click **Import users**.</span></span>
4. <span data-ttu-id="20584-110">Valitse tuotavat käyttäjät ja valitse sitten **Tuo käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="20584-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="20584-111">Kun tuonti on päättynyt, käyttäjien roolien määrittäminen on pakollista.</span><span class="sxs-lookup"><span data-stu-id="20584-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="20584-112">Käyttäjien joukkotuonti</span><span class="sxs-lookup"><span data-stu-id="20584-112">Import users in bulk</span></span>

<span data-ttu-id="20584-113">Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda suuren määrän käyttäjiä Azure Active Directorysta.</span><span class="sxs-lookup"><span data-stu-id="20584-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="20584-114">Huomaa, että käyttäjiä ei voi valita Erätuonti-vaihtoehtoa käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="20584-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="20584-115">Suorita tuonti erätyönä</span><span class="sxs-lookup"><span data-stu-id="20584-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="20584-116">Tuodun käyttäjän oletusyrityksenä on nykyisen istunnon yritys.</span><span class="sxs-lookup"><span data-stu-id="20584-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="20584-117">Muuta nykyistä yritystä tarvittaessa ennen käyttäjien tuomista.</span><span class="sxs-lookup"><span data-stu-id="20584-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="20584-118">Valitse **Järjestelmänhallinta > Käyttäjät > Käyttäjä**.</span><span class="sxs-lookup"><span data-stu-id="20584-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="20584-119">Valitse **Erätuonti**.</span><span class="sxs-lookup"><span data-stu-id="20584-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="20584-120">Laajenna **Suorita taustalla** -osa.</span><span class="sxs-lookup"><span data-stu-id="20584-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="20584-121">Valitse **Kyllä** **Eräkäsittely**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="20584-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="20584-122">Syötä tai valitse arvo **Eräryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="20584-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="20584-123">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="20584-123">This is an optional step.</span></span>  
7. <span data-ttu-id="20584-124">Valitse **Kyllä** **Yksityinen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="20584-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="20584-125">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="20584-125">This is an optional step.</span></span>  
8. <span data-ttu-id="20584-126">Valitse **Kyllä** **Kriittinen työ** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="20584-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="20584-127">bTämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="20584-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="20584-128">Valitse vaihtoehto \*\*Valvontaluokka-kentässä.</span><span class="sxs-lookup"><span data-stu-id="20584-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="20584-129">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="20584-129">Click **OK**.</span></span>

<span data-ttu-id="20584-130">Kun tuonti on päättynyt, käyttäjien roolien määrittäminen on pakollista.</span><span class="sxs-lookup"><span data-stu-id="20584-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="20584-131">Eristysympäristön suorittaminen</span><span class="sxs-lookup"><span data-stu-id="20584-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="20584-132">Valitse **Erätuonti**.</span><span class="sxs-lookup"><span data-stu-id="20584-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="20584-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="20584-133">Select **OK**.</span></span>
