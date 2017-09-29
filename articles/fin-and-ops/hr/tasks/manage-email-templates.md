--- 
title: "Sähköpostimallien hallinta"
description: "Voit siirtää tietoja organisaation tietokannasta uuden asiakirjan kirjanmerkkeihin ja käyttää sitä malleissa. Tämä tehostaa viestintää hakijoiden ja ehdokkaiden kanssa."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1eeaf1675b6653ab2c8c04d05ec1bff3cd0bb18d
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="manage-email-templates"></a><span data-ttu-id="de5a9-103">Sähköpostimallien hallinta</span><span class="sxs-lookup"><span data-stu-id="de5a9-103">Manage email templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de5a9-104">Voit siirtää tietoja organisaation tietokannasta uuden asiakirjan kirjanmerkkeihin ja käyttää sitä malleissa. Tämä tehostaa viestintää hakijoiden ja ehdokkaiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="de5a9-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="de5a9-105">Voit tehdä tämän luomalla mallin, joka sisältää vakiotekstiä ja muutamia kirjanmerkkejä, joihin järjestelmätiedot lisätään.</span><span class="sxs-lookup"><span data-stu-id="de5a9-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="de5a9-106">Voit esimerkiksi lisätä hakijan osoitteen ja yhteystiedot Microsoft Word -asiakirjaan, jota käytät viestinnässä hakijan kanssa.</span><span class="sxs-lookup"><span data-stu-id="de5a9-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="de5a9-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="de5a9-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="de5a9-108">Sähköpostimalleissa käytettävien kirjanmerkkien valitseminen</span><span class="sxs-lookup"><span data-stu-id="de5a9-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="de5a9-109">Siirry Hakemuksen kirjanmerkit -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="de5a9-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="de5a9-110">Etsi haluamasi vastaustoimenpide luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="de5a9-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="de5a9-111">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="de5a9-111">Click Edit.</span></span>
4. <span data-ttu-id="de5a9-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="de5a9-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="de5a9-113">Valitse kentät, joita haluat käyttää valitun vastaustoimenpiteen sähköpostimallissa, ja siirrä ne kirjanmerkkikenttiin.</span><span class="sxs-lookup"><span data-stu-id="de5a9-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="de5a9-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="de5a9-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="de5a9-115">Sähköpostimallin luominen</span><span class="sxs-lookup"><span data-stu-id="de5a9-115">Create an email template</span></span>
1. <span data-ttu-id="de5a9-116">Valitse Henkilöstöhallinto > Työhönotto > Viestintä > Sähköpostimallit.</span><span class="sxs-lookup"><span data-stu-id="de5a9-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="de5a9-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="de5a9-117">Click New.</span></span>
3. <span data-ttu-id="de5a9-118">Valitse Vastaustoimenpide-kentässä Haastattelu.</span><span class="sxs-lookup"><span data-stu-id="de5a9-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="de5a9-119">Valitse vastaustoimenpide, joka sisältää tämän tyyppisessä sähköpostiviestinnässä käytettävät kirjanmerkit.</span><span class="sxs-lookup"><span data-stu-id="de5a9-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="de5a9-120">Syötä arvo Sähköpostimalli-kenttään.</span><span class="sxs-lookup"><span data-stu-id="de5a9-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="de5a9-121">Kirjoita arvo Aihe-kenttään.</span><span class="sxs-lookup"><span data-stu-id="de5a9-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="de5a9-122">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="de5a9-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="de5a9-123">Etsi haluamasi kirjanmerkkikenttä luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="de5a9-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="de5a9-124">Jatka sähköpostiviestin kirjoittamista. Lisää kirjanmerkkikenttiä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="de5a9-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="de5a9-125">Jatka sähköpostiviestin kirjoittamista. Lisää kirjanmerkkikenttiä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="de5a9-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="de5a9-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="de5a9-126">Click Save.</span></span>


