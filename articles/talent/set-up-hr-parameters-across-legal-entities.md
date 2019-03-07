---
title: Yritysten välisten henkilöstöhallinnon (HR) parametrien määrittäminen
description: Jaetut parametrit on määritettävä tietueille, jotka ovat yhteisiä yrityksille, kuten Toimi-tietueille. Tässä artikkelissa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304137"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="e3302-104">Yritysten välisten henkilöstöhallinnon (HR) parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e3302-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3302-105">Jaetut parametrit on määritettävä tietueille, jotka ovat yhteisiä yrityksille, kuten Toimi-tietueille.</span><span class="sxs-lookup"><span data-stu-id="e3302-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="e3302-106">Tässä artikkelissa käsitellään eri yritysten henkilöstöhallintoparametrien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="e3302-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="e3302-107">Jotkin tietuetyypit, kuten Toimi-tietueet, jaetaan yritysten kesken.</span><span class="sxs-lookup"><span data-stu-id="e3302-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="e3302-108">Näille tietueille on määritettävä jaetut parametrit.</span><span class="sxs-lookup"><span data-stu-id="e3302-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="e3302-109">Voit esimerkiksi käyttää **Henkilöstöhallinnon jaetut parametrit** -sivua yritysten kesken jaettujen henkilöstöparametrien määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="e3302-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="e3302-110">**Henkilöstöhallinnon jaetut parametrit** -sivulla parametrit ryhmitellään alueisiin niiden toimintojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e3302-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="e3302-111">Aiemmin julkaistu toiminto</span><span class="sxs-lookup"><span data-stu-id="e3302-111">Previously released functionality</span></span>
<span data-ttu-id="e3302-112">**Tunnus**-välilehdellä sinun on valittava tunnustyypit, jotka edustavat sivulla lueteltuja tunnistenumeroita.</span><span class="sxs-lookup"><span data-stu-id="e3302-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="e3302-113">On määritettävä tunnustyypit ennen kuin voit kirjoittaa tunnustiedot työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="e3302-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="e3302-114">Tietoa sosiaaliturvatunnuksesta, kansallisesta henkilötunnusnumerosta, valtuutustunnuksesta ja henkilökohtaisesta tunnuskoodista ylläpidetään **Tunnuksen tyyppi** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e3302-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="e3302-115">Määritä uusi tunnustyyppi tai tarkastele olemassa olevien tunnusten listaa valitsemalla **Henkilöstön hallinta** &gt; **Linkit-välilehti** &gt; **Asennus** &gt; **Tunnustyypit**.</span><span class="sxs-lookup"><span data-stu-id="e3302-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="e3302-116">Voit syöttää yksinkertaisen koodin ja kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="e3302-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="e3302-117">Jos käytät Dynamics 365 for Talentia</span><span class="sxs-lookup"><span data-stu-id="e3302-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="e3302-118">**Tunnus**-välilehdellä sinun on valittava tunnustyypit, jotka edustavat sivulla lueteltuja tunnistenumeroita.</span><span class="sxs-lookup"><span data-stu-id="e3302-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="e3302-119">On määritettävä tunnustyypit ennen kuin voit kirjoittaa tunnustiedot työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="e3302-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="e3302-120">Tietoa sosiaaliturvatunnuksesta, kansallisesta henkilötunnusnumerosta, valtuutustunnuksesta ja henkilökohtaisesta tunnuskoodista ylläpidetään **Tunnuksen tyyppi** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e3302-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="e3302-121">Määritä uusi tunnustyyppi tai tarkastele olemassa olevien tunnusten listaa valitsemalla **Henkilöstöhallinto** &gt; **Asetukset** &gt; **Tunnustyypit**.</span><span class="sxs-lookup"><span data-stu-id="e3302-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="e3302-122">Voit syöttää yksinkertaisen koodin ja kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="e3302-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="e3302-123">**Numerojärjestykset**-välilehdellä voit valita numerosarjat, joita käytetään seuraaville tietueille: Henkilöstönumero, Toimi, Käyttäjäpyynnön tunnus, -9-asiakirja, Hakija, Keskustelu, Etutunnus ja Henkilöstötoiminto (jos tämä tietuetyyppi on otettu käyttöön).</span><span class="sxs-lookup"><span data-stu-id="e3302-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="e3302-124">Jos haluat ylläpitää numerosarjaviitteitä ja koodeja, käytä **Numerojärjestykset**-luettelosivua.</span><span class="sxs-lookup"><span data-stu-id="e3302-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="e3302-125">Käytä sivun hakutoimintoa löytääksesi tämän sivun.</span><span class="sxs-lookup"><span data-stu-id="e3302-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="e3302-126">Ilmaise **Toimet**-välilehdellä, ovatko uudet toimet oletusarvoisesti käytettävissä toimeksiantoa varten:</span><span class="sxs-lookup"><span data-stu-id="e3302-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="e3302-127">**Aina** – Voit määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e3302-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="e3302-128">Kun toimet on luotu, **Käytettävissä toimeksiantoa varten** -päivämäärä ja -aika **Yleinen** -välilehden **Toimi**-sivulla asetetaan automaattisesti sen luontipäivämääräksi ja -ajaksi.</span><span class="sxs-lookup"><span data-stu-id="e3302-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="e3302-129">**Ei koskaan** – Et voi määrittää työntekijöitä uusiin toimiin toimien luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e3302-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="e3302-130">Jos valitset tämän vaihtoehdon, sinun on avattava **Toimi**-sivu kullekin uudelle toimelle sen tullessa saataville ja syötä tämän jälkeen **Yleinen**-välilehdellä **Käytettävissä toimeksiantoa varten** päivämäärä ottaaksesi käyttöön työntekijän määrityksen.</span><span class="sxs-lookup"><span data-stu-id="e3302-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="e3302-131">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e3302-131">Additional resources</span></span>
--------

[<span data-ttu-id="e3302-132">Määritä yrityskohtaisia henkilöstöhallinnon parametreja</span><span class="sxs-lookup"><span data-stu-id="e3302-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)



