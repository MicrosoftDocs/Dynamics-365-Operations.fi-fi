---
title: Sähköpostimallien hallinta
description: Tässä ohjeaiheessa käsitellään sähköpostimallien hallintaa.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ecfa720dfa9b3ed6ee15ec68498d2a46612a9ae
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867484"
---
# <a name="manage-email-templates"></a><span data-ttu-id="875c6-103">Sähköpostimallien hallinta</span><span class="sxs-lookup"><span data-stu-id="875c6-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="875c6-104">Voit siirtää tietoja organisaation tietokannasta uuden asiakirjan kirjanmerkkeihin ja käyttää sitä malleissa. Tämä tehostaa viestintää hakijoiden ja ehdokkaiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="875c6-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="875c6-105">Voit tehdä tämän luomalla mallin, joka sisältää vakiotekstiä ja muutamia kirjanmerkkejä, joihin järjestelmätiedot lisätään.</span><span class="sxs-lookup"><span data-stu-id="875c6-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="875c6-106">Voit esimerkiksi lisätä hakijan osoitteen ja yhteystiedot Microsoft Word -asiakirjaan, jota käytät viestinnässä hakijan kanssa.</span><span class="sxs-lookup"><span data-stu-id="875c6-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="875c6-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="875c6-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="875c6-108">Sähköpostimalleissa käytettävien kirjanmerkkien valitseminen</span><span class="sxs-lookup"><span data-stu-id="875c6-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="875c6-109">Siirry siirtymisruudussa kohtaan **Moduulit > Henkilöstöhallinto > Työhönotto > Viestintä > Hakemuksen kirjanmerkit**.</span><span class="sxs-lookup"><span data-stu-id="875c6-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="875c6-110">Etsi haluamasi vastaustoimenpide luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="875c6-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="875c6-111">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="875c6-111">Select **Edit**.</span></span>
4. <span data-ttu-id="875c6-112">Valitse kentät, joita haluat käyttää valitun vastaustoimenpiteen sähköpostimallissa, ja siirrä ne kirjanmerkkikenttiin.</span><span class="sxs-lookup"><span data-stu-id="875c6-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="875c6-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="875c6-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="875c6-114">Luo sähköpostimalli</span><span class="sxs-lookup"><span data-stu-id="875c6-114">Create an email template</span></span>
1. <span data-ttu-id="875c6-115">Siirry siirtymisruudussa kohtaan **Moduulit > Henkilöstöhallinto > Työhönotto > Viestintä > Sähköpostimallit**.</span><span class="sxs-lookup"><span data-stu-id="875c6-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="875c6-116">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="875c6-116">Select **New**.</span></span>
3. <span data-ttu-id="875c6-117">Valitse **Vastaustoimenpide**-kentässä **Haastattelu**.</span><span class="sxs-lookup"><span data-stu-id="875c6-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="875c6-118">Valitse vastaustoimenpide, joka sisältää tämän tyyppisessä sähköpostiviestinnässä käytettävät kirjanmerkit.</span><span class="sxs-lookup"><span data-stu-id="875c6-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="875c6-119">Syötä arvo **Sähköpostimalli**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="875c6-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="875c6-120">Kirjoita arvo **Aihe**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="875c6-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="875c6-121">Kirjoita arvo **Teksti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="875c6-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="875c6-122">Etsi haluamasi kirjanmerkkikenttä luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="875c6-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="875c6-123">Jatka sähköpostiviestin kirjoittamista. Lisää kirjanmerkkikenttiä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="875c6-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="875c6-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="875c6-124">Select **Save**.</span></span>

