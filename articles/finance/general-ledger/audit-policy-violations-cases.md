---
title: Valvo käytäntövirheitä ja tapauksia
description: Tässä artikkelissa kerrotaan, miten valvontatapaukset luodaan valvontakäytäntöjen sääntöjen rikkomuksista. Artikkeli sisältää tietoja myös valvontakäytäntöjen erilaisista tavoista käyttää asiakirjavalinnan päivämääräväliä.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d14894d331037033b27fac3fd7ff98c5521eaf98
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186782"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="a0243-104">Valvo käytäntövirheitä ja tapauksia</span><span class="sxs-lookup"><span data-stu-id="a0243-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0243-105">Tässä artikkelissa kerrotaan, miten valvontatapaukset luodaan valvontakäytäntöjen sääntöjen rikkomuksista.</span><span class="sxs-lookup"><span data-stu-id="a0243-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="a0243-106">Artikkeli sisältää tietoja myös valvontakäytäntöjen erilaisista tavoista käyttää asiakirjavalinnan päivämääräväliä.</span><span class="sxs-lookup"><span data-stu-id="a0243-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="a0243-107">Kuinka tarkasteltuja tapauksia luodaan</span><span class="sxs-lookup"><span data-stu-id="a0243-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="a0243-108">Valvontakäytäntöjä käytetään tunnistamaan kuluraportteja, ostotilauksia ja toimittajalaskuja, jotka eivät noudata liiketoimintasääntöjä, jotka määrittelet ja määrität valvontakäytäntösäännöiksi.</span><span class="sxs-lookup"><span data-stu-id="a0243-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="a0243-109">Vavontakäytännöt suoritetaan erätilassa.</span><span class="sxs-lookup"><span data-stu-id="a0243-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="a0243-110">Valvontakäytäntöä suoritettaessa kaikki käytäntösäännöt, jotka kuuluvat kyseiseen käytäntöön suoritetaan samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="a0243-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="a0243-111">Kunkin käytäntösääntö käsittelee useita asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="a0243-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="a0243-112">Käytäntösääntö valitsee asiakirjoja, jotka ovat asiakirjan valintapäivämäärän alueella ja jotka vastaavat määritettyjä ehtoja.</span><span class="sxs-lookup"><span data-stu-id="a0243-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="a0243-113">Esimerkiksi yksi käytäntösääntö saattaa valita kuluraportit, joissa on ateriat, jotka ylittävät 50,00.</span><span class="sxs-lookup"><span data-stu-id="a0243-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="a0243-114">Toinen käytäntösääntö saattaa valita toimittajalaskut, jotka suoritetaan tietylle toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="a0243-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="a0243-115">Kullekin valitulle asiakirjalle, joka on valittu joukossa, muodostuu rikkominen.</span><span class="sxs-lookup"><span data-stu-id="a0243-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="a0243-116">Rikkominen on tietue, että tietty asiakirja, kuten lasku 12345, ei seuraa käytäntösääntöä.</span><span class="sxs-lookup"><span data-stu-id="a0243-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="a0243-117">Useita valvontarikkomus tietueita on ryhmitelty ja ne liittyvät valvontatapauksiin.</span><span class="sxs-lookup"><span data-stu-id="a0243-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="a0243-118">Oletusarvona. kunkin valvontakäytännön tapaukset ryhmitellään valvontakäytäntösäännön perusteella.</span><span class="sxs-lookup"><span data-stu-id="a0243-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="a0243-119">Halutessasi voit valita muita ryhmittelyehtoja käyttämällä **Tapauksien ryhmittelyehdot** -sivua.</span><span class="sxs-lookup"><span data-stu-id="a0243-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="a0243-120">Voit ryhmitellä esimerkiksi kulujen otsikot projektitunnuksen mukaan ja toimittajalaskut toimittajatilin mukaan.</span><span class="sxs-lookup"><span data-stu-id="a0243-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="a0243-121">Tällöin kaikki kuluraportin otsikoiden rikkomiset, joilla on sama projektitunnus, ryhmitellään samaan tapaukseen ja kaikki toimittajalaskut, joilla on sama toimittajatili, ryhmitellään samaan tapaukseen.</span><span class="sxs-lookup"><span data-stu-id="a0243-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="a0243-122">Valvontakäytännön säännöt, jotka perustuvat **Duplikaatti**-kyselytyyppiin, rikkeitä ei ole ryhmitelty käytäntösäännöittäin tai ehtojen mukaan, jotka on määritetty **Tapausten ryhmittelyehto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a0243-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="a0243-123">Sen sijaan ryhmittelyperusteena ovat kriteerit, jotka sisältyvät tarkistuskäytännön sääntöön.</span><span class="sxs-lookup"><span data-stu-id="a0243-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="a0243-124">Esimerkiksi, jos käytäntösääntö laskee kuluraporttien kaksoiskappaleiden kulut samalle summalle, myyjän tunnukselle ja päivämäärälle, kaikki kulut, joilla on samat arvot niissä kentissä, ovat yksi tapaus.</span><span class="sxs-lookup"><span data-stu-id="a0243-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="a0243-125">Kulut, joilla on erilaiset arvot, ovat erillisessä laatikossa.</span><span class="sxs-lookup"><span data-stu-id="a0243-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="a0243-126">Sen jälkeen kun valvontatapaukset on luotu, kun ne käsitellään käyttämällä tyypillisiä prosesseja tapaushallinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="a0243-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="a0243-127">Asiakirjojen valinnan päivämäärävälit</span><span class="sxs-lookup"><span data-stu-id="a0243-127">Document selection date ranges</span></span>
<span data-ttu-id="a0243-128">Kun tarkistuskäytäntö suoritetaan, kukin käytäntösääntö valitsee tietyntyyppiset asiakirjat, joiden päivämäärä on asiakirjan valitulla päivämäärävälillä.</span><span class="sxs-lookup"><span data-stu-id="a0243-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="a0243-129">Asiakirjan valinnan päivämääräväli määritetään **Lisäasetukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a0243-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="a0243-130">Useisiin asiakirjoihin on liitetty useampi kuin yksi päivä.</span><span class="sxs-lookup"><span data-stu-id="a0243-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="a0243-131">Päivämääräkenttä, jota tarkistuskäytäntösääntö käyttää täsmennetään **Käytäntösääntötyyppi**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a0243-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="a0243-132">Tässä on muita tapoja, joilla tarkistuskäytäntö käyttää asiakirjan valinnan päivämääräväliä:</span><span class="sxs-lookup"><span data-stu-id="a0243-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="a0243-133">Menettely käyttää jokaisen käytäntösäännön sitä versiota, joka on voimassa asiakirjan valinnan päivämäärävälin viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="a0243-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="a0243-134">Voit tarkastella kunkin käytäntösäännön voimassaolopäivämääriä **Valvontakäytännöt**-luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="a0243-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="a0243-135">Käytäntösääntöä käyttää oraganisaation solmuja, jotka liittyvät käytäntöön viimeisenä päivänä asiakirjan valinnan päivämäärävälin aikana.</span><span class="sxs-lookup"><span data-stu-id="a0243-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="a0243-136">Vain ne organisaatiosolmut, jotka liittyvät käytäntöön nykyisin näkyvät **Valvontakäytännöt**-luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="a0243-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="a0243-137">Käytäntösäännöt, jotka perustuvat **Luettelohaku**-kyselylajiin, käytäntö käsittelee valvottuja asiakirjoja, jotka ovat voimassa asiakirjan valitun ajanjakson viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="a0243-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="a0243-138">Lisätietoja on kohdassa [Tilintarkastuskäytännön säännöt](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="a0243-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>


