---
title: Vuokrasopimuksen hyväksyntätyönkulkujen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten uuden vuokrasopimuksen luomisen yhteydessä suoritettava hyväksynnän työnkulku määritetään.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4d5416b3b24d5fbb3ac46afb3c672212d41d42d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827551"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="51bcf-103">Vuokrasopimuksen hyväksyntätyönkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="51bcf-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51bcf-104">Tässä ohjeaiheessa kerrotaan, miten uuden vuokrasopimuksen luomisen yhteydessä suoritettava hyväksynnän työnkulku määritetään.</span><span class="sxs-lookup"><span data-stu-id="51bcf-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="51bcf-105">Lisätietoja työnkulun käyttämisestä on kohdassa [Vuokrasopimuksen hyväksyntätyönkulkujen käyttäminen](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="51bcf-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="51bcf-106">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokrauksen työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="51bcf-107">Valitse **Vuokrauksen työnkulku** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="51bcf-108">Valitse näkyviin tulevasta valintaikkunasta **Työnkulun tyyppi** -kohdassa **Vuokrauksen työnkulku** -linkki.</span><span class="sxs-lookup"><span data-stu-id="51bcf-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="51bcf-109">Sovellus avataan.</span><span class="sxs-lookup"><span data-stu-id="51bcf-109">The application is opened.</span></span> <span data-ttu-id="51bcf-110">Kun se on suoritettu, kirjaudu sisään Azure Active Directoryyn (Azure AD). Sinut ohjataan työnkulun sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="51bcf-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="51bcf-111">Vedä **Vuokrauksen työnkulun hyväksyntä** -elementti työkulkuun.</span><span class="sxs-lookup"><span data-stu-id="51bcf-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="51bcf-112">Yhdistä yksi solmu **alusta** **vuokrauksen työnkulun hyväksyntään**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="51bcf-113">Yhdistä sitten **vuokrauksen työnkulun hyväksyntä** **loppuun**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="51bcf-114">Kaksoisnapsauta **Vuokrauksen työnkulun hyväksyntä** -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="51bcf-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="51bcf-115">Valitse **Ominaisuudet** ja anna **Perustiedot**-kohdassa työnkulun nimi.</span><span class="sxs-lookup"><span data-stu-id="51bcf-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="51bcf-116">Tällä sivulla voit myös määrittää lisäparametreja työnkulkua varten.</span><span class="sxs-lookup"><span data-stu-id="51bcf-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="51bcf-117">Jos olet ottanut **automaattiset toiminnot** käyttöön, järjestelmä tekee automaattisesti tietyn toimenpiteen.</span><span class="sxs-lookup"><span data-stu-id="51bcf-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="51bcf-118">Ilmoitukset voidaan lähettää, jos ne on määritetty **Ilmoitukset**-välilehdessä. **Lisäasetukset**-välilehdessä voit määrittää lopullisen hyväksyjän, asettaa aikarajan ja määrittää tietyt toimenpiteet, jotka on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="51bcf-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="51bcf-119">Kun olet määrittänyt työnkulun parametrit, valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="51bcf-120">Valitse **Vaihe 1** ja valitse sitten **Ominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="51bcf-121">Anna **Perusasetukset**-kohdassa vaiheen nimi, luo hyväksyttävä aiherivi ja määritä hyväksynnän ohjeet.</span><span class="sxs-lookup"><span data-stu-id="51bcf-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="51bcf-122">Valitse **Määritys**-sivulla määrityksen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="51bcf-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="51bcf-123">Jos haluat määrittää hyväksyntään tiettyjä käyttäjiä, valitse **Käyttäjä**, valitse sitten vuokrasopimukset hyväksyvät käyttäjät. Valitse lopuksi **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="51bcf-124">Luo työnkulku valitsemalla **Tallenna ja sulje**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="51bcf-125">Valitse pyydettäessä **OK**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="51bcf-126">Valitse **Luo työnkulku** -sivulla **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="51bcf-127">Valitse uusi työnkulku ja valitse sitten **Versiot**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="51bcf-128">Varmista sitten, että työnkulku on aktiivinen, valitsemalla **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="51bcf-129">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-129">Select **Close**.</span></span> <span data-ttu-id="51bcf-130">Uusi aktiivinen versio tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="51bcf-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]