---
title: "Toimittajaportaalin käyttäjäsuojaus"
description: "Tässä artikkelissa käsitellään käyttöoikeuksien määrittämistä Toimittajaportaalia käyttäville ulkoisille toimittajille. Tämän aiheen tiedot koskevat vain Dynamics AX:n helmikuun 2016 ja 2016 toukokuun versioita."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ab096bcc7003f60851077d9c7e03b16c5d46ce2a
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="5c5cb-104">Toimittajaportaalin käyttäjäsuojaus</span><span class="sxs-lookup"><span data-stu-id="5c5cb-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5c5cb-105">Tässä artikkelissa käsitellään käyttöoikeuksien määrittämistä Toimittajaportaalia käyttäville ulkoisille toimittajille.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="5c5cb-106">Tämän aiheen tiedot koskevat vain Dynamics AX:n helmikuun 2016 ja 2016 toukokuun versioita.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="5c5cb-107">Toimittajaportaalin toiminnot on korvattu laajennetulla toimittajayhteistyötoiminnallisuudella Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="5c5cb-108">Saat lisätietoja toimittajayhteistyön suojauksen määrittämisestä ohjeaiheesta [Toimittajayhteistyön määritys ja ylläpito](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="5c5cb-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="5c5cb-109">Toimittajaportaali paljastaa rajatun määrän ostotilauksia koskevaa tietoa ulkopuolisille toimittajille.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="5c5cb-110">On tärkeää, että määrität Toimittajaportaalin käyttöoikeudet oikein Microsoft Dynamics AX:ssä niin, että toimittajilla ei ole liian laajaa pääsyä Dynamics AX:si lisätietoihin.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="5c5cb-111">**Tärkeää:** Muista käyttäjistä poiketen, ulkoisilla toimittajilla ei pitäisi olla **Järjestelmänkäyttäjä**-roolia.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="5c5cb-112">**Järjestelmänkäyttäjä**-roolille myönnetään oikeuksia, jotka eivät sovellu ulkoisille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="5c5cb-113">Toimittajaportaalin käyttäjän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5c5cb-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="5c5cb-114">Ennen kuin luot käyttäjätilin henkilölle, joka tulee käyttämään Toimittajaportaalia, sinun on määritettävä kyseiselle toimittajalle Toimittajaportaaliyhteistyön salliminen.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="5c5cb-115">Käytä **Ostotilausyhteistyö**-kenttää **Yleinen**-välilehdessä **Toimittajat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="5c5cb-116">Ulkoisilla toimittajilla, jotka käyttävät Toimittajaportaalia, on oltava seuraavat asetukset.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="5c5cb-117">Microsoft Azure Active Directory (AAD) -käyttäjätili on rekisteröitävä toimittajalle Dynamics AX:n **Käyttäjät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="5c5cb-118">Toimittajalla on oltava **Toimittaja (ulkoinen)** -käyttöoikeusrooli **Järjestelmänkäyttäjä**-roolin sijaan.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="5c5cb-119">**Huomautus:****Järjestelmänkäyttäjä**-rooli myönnetään automaattisesti, kun luot uuden käyttäjätilin Dynamics AX:ssä.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="5c5cb-120">Sinun on siksi poistettava kyseinen rooli ja hyväksyttävä saamasi varoitusviesti.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="5c5cb-121">Toimittajakäyttäjälle ei pitäisi myöntää oikeutta lisätä kenttiä ostotilaustaulukoista omaan ostotilausnäkymäänsä.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="5c5cb-122">Määritä **Mukauttaminen**-välilehden **Käyttäjät** välilehdellä **Eksplisiittinen mukauttaminen sallittu** -vaihtoehto käyttäjälle arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="5c5cb-123">Käyttäjätilin on oltava liitettynä rekisteröityyn yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="5c5cb-124">Valitse **Käyttäjät**-sivulla yhteyshenkilö **Nimi**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="5c5cb-125">Valitsemallasi henkilöllä tulisi olla kyseisen toimittajan **Yhteyshenkilö**-rooli.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="5c5cb-126">Jos sama henkilö tarvitsee käyttöoikeudet Toimittajaportaalissa useille toimittajatileille (esimerkiksi eri yrityksille), kunkin kyseisen henkilön käyttäjätilin on oltava liitettynä samaan rekisteröityyn yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="5c5cb-127">**Toimittaja (ulkoinen)** -rooli sisältää kaikki perusominaisuudet, jotka tarvitaan Toimittajaportaalissa satavilla olevien toiminnallisuuksien käyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="5c5cb-128">Nämä asetukset auttavat varmistamaan, että ulkoisen käyttäjän näkemä käyttöliittymä näyttää vain halutun skenaarion.</span><span class="sxs-lookup"><span data-stu-id="5c5cb-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="5c5cb-129">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="5c5cb-129">See also</span></span>
--------

[<span data-ttu-id="5c5cb-130">Toimittajayhteistyö</span><span class="sxs-lookup"><span data-stu-id="5c5cb-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




