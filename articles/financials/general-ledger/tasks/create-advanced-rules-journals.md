---
title: Luo kirjauskansioiden lisäsäännöt
description: Tässä menettelyssä käsitellään kirjauskansioiden lisäsääntöjen luontia.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3eb34ac419aeab3663a8931d022abf7bcbfddd37
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916139"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="47505-103">Luo kirjauskansioiden lisäsäännöt</span><span class="sxs-lookup"><span data-stu-id="47505-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47505-104">Tässä menettelyssä käsitellään kirjauskansioiden lisäsääntöjen luontia.</span><span class="sxs-lookup"><span data-stu-id="47505-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="47505-105">Niitä ovat esimerkiksi kirjauskansion hallinnan ja käyttäjän kirjausrajoitusten määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="47505-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="47505-106">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="47505-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="47505-107">Määritä kirjauskansion hallinta</span><span class="sxs-lookup"><span data-stu-id="47505-107">Set up journal control</span></span>
1. <span data-ttu-id="47505-108">Siirry kohtaan **Siirtymisruutu** > **Moduulit > kirjanpito > kirjauskansion asetukset > Kirjauskansioiden nimet**.</span><span class="sxs-lookup"><span data-stu-id="47505-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="47505-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="47505-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="47505-110">Napsauta **Toimintoruudussa** **Kirjauskansion hallinta**.</span><span class="sxs-lookup"><span data-stu-id="47505-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="47505-111">Valitse **Mitä tilityyppejä voidaan kirjata** -pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="47505-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="47505-112">Avaa haku napsauttamalla **Yrityksen tilit** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="47505-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="47505-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="47505-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="47505-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47505-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="47505-115">Valitse **Mitkä segmenttiarvot ovat kelvollisia tälle kirjauskansiolle** -pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="47505-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="47505-116">Avaa haku napsauttamalla **Tilirakenne**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="47505-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="47505-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="47505-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="47505-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47505-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="47505-119">Avaa haku napsauttamalla **Segmentti**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="47505-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="47505-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47505-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="47505-121">Avaa haku napsauttamalla **Arvosta**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="47505-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="47505-122">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="47505-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="47505-123">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47505-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="47505-124">Avaa haku valitsemalla **Arvoon**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="47505-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="47505-125">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="47505-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="47505-126">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="47505-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="47505-127">Kirjausrajoitusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="47505-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="47505-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="47505-128">Close the page.</span></span>
2. <span data-ttu-id="47505-129">Valitse **Kirjausrajoitukset**.</span><span class="sxs-lookup"><span data-stu-id="47505-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="47505-130">Valitse **Miten haluat määrittää kirjaamisrajoitukset** -asetukseksi Käyttäjäryhmäkohtainen.</span><span class="sxs-lookup"><span data-stu-id="47505-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="47505-131">Valitse puussa ryhmä, jolle annat luvan kirjata tähän kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="47505-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="47505-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="47505-132">Click **OK**.</span></span>

