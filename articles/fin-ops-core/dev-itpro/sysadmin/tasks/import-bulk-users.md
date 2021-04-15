---
title: Tuo käyttäjiä Azure Active Directorysta
description: Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda manuaalisesti valitut käyttäjät tai suuren määrän käyttäjiä Azure Active Directorysta.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745786"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="72948-103">Tuo käyttäjiä Azure Active Directorysta</span><span class="sxs-lookup"><span data-stu-id="72948-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="72948-104">Tuo valitut käyttäjät</span><span class="sxs-lookup"><span data-stu-id="72948-104">Import select users</span></span>

<span data-ttu-id="72948-105">Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda valitut käyttäjät Azure Active Directorysta (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="72948-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="72948-106">Tuodun käyttäjän oletusyrityksenä on nykyisen istunnon yritys.</span><span class="sxs-lookup"><span data-stu-id="72948-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="72948-107">Muuta nykyistä yritystä tarvittaessa ennen käyttäjien tuomista.</span><span class="sxs-lookup"><span data-stu-id="72948-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="72948-108">Valitse **Järjestelmänhallinta > Käyttäjät > Käyttäjä** t.</span><span class="sxs-lookup"><span data-stu-id="72948-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="72948-109">Valitse **Tuo käyttäjiä**.</span><span class="sxs-lookup"><span data-stu-id="72948-109">Click **Import users**.</span></span>
4. <span data-ttu-id="72948-110">Valitse tuotavat käyttäjät ja valitse sitten **Tuo käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="72948-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="72948-111">Kun tuonti on päättynyt, käyttäjien roolien määrittäminen on pakollista.</span><span class="sxs-lookup"><span data-stu-id="72948-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="72948-112">Käyttäjien joukkotuonti</span><span class="sxs-lookup"><span data-stu-id="72948-112">Import users in bulk</span></span>

<span data-ttu-id="72948-113">Näiden ohjeiden avulla järjestelmänvalvoja voi tuoda suuren määrän käyttäjiä Azure Active Directorysta.</span><span class="sxs-lookup"><span data-stu-id="72948-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="72948-114">Huomaa, että käyttäjiä ei voi valita Erätuonti-vaihtoehtoa käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="72948-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="72948-115">Suorita tuonti erätyönä</span><span class="sxs-lookup"><span data-stu-id="72948-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="72948-116">Tuodun käyttäjän oletusyrityksenä on nykyisen istunnon yritys.</span><span class="sxs-lookup"><span data-stu-id="72948-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="72948-117">Muuta nykyistä yritystä tarvittaessa ennen käyttäjien tuomista.</span><span class="sxs-lookup"><span data-stu-id="72948-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="72948-118">Valitse **Järjestelmänhallinta > Käyttäjät > Käyttäjä**.</span><span class="sxs-lookup"><span data-stu-id="72948-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="72948-119">Valitse **Erätuonti**.</span><span class="sxs-lookup"><span data-stu-id="72948-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="72948-120">Laajenna **Suorita taustalla** -osa.</span><span class="sxs-lookup"><span data-stu-id="72948-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="72948-121">Valitse **Eräkäsittely**-kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="72948-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="72948-122">Syötä tai valitse arvo **Eräryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="72948-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="72948-123">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="72948-123">This is an optional step.</span></span>  
7. <span data-ttu-id="72948-124">Valitse **Kyllä** **Yksityinen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="72948-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="72948-125">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="72948-125">This is an optional step.</span></span>  
8. <span data-ttu-id="72948-126">Valitse **Kyllä** **Kriittinen työ** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="72948-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="72948-127">Tämä on valinnainen vaihe.</span><span class="sxs-lookup"><span data-stu-id="72948-127">This is an optional step.</span></span>  
9. <span data-ttu-id="72948-128">Valitse vaihtoehto **Valvontaluokka**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="72948-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="72948-129">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="72948-129">Click **OK**.</span></span>

<span data-ttu-id="72948-130">Kun tuonti on päättynyt, käyttäjien roolien määrittäminen on pakollista.</span><span class="sxs-lookup"><span data-stu-id="72948-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="72948-131">Eristysympäristön suorittaminen</span><span class="sxs-lookup"><span data-stu-id="72948-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="72948-132">Valitse **Erätuonti**.</span><span class="sxs-lookup"><span data-stu-id="72948-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="72948-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="72948-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]