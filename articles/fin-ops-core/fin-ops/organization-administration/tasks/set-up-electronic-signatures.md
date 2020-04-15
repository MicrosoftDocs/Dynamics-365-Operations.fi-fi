---
title: Sähköisten allekirjoitusten määrittäminen
description: Määritä sähköiset allekirjoitukset tällä menettelyllä.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b8b248481f04856fe15dadbc245caae5330ef8f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140533"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="e4296-103">Sähköisten allekirjoitusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e4296-103">Set up electronic signatures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4296-104">Määritä sähköiset allekirjoitukset tällä menettelyllä.</span><span class="sxs-lookup"><span data-stu-id="e4296-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="e4296-105">Sähköisellä allekirjoituksella vahvistetaan uuden tietojenkäsittelyprosessin aloittavan tai prosessin hyväksynnän aloittavan henkilön henkilöllisyys.</span><span class="sxs-lookup"><span data-stu-id="e4296-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="e4296-106">Tämän menettelyn luomisessa käytetty esittely-yritys on DAT.</span><span class="sxs-lookup"><span data-stu-id="e4296-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="e4296-107">Ota sähköisen allekirjoituksen määritysavain käyttöön</span><span class="sxs-lookup"><span data-stu-id="e4296-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="e4296-108">Valitse Järjestelmän hallinta > Asetukset > Käyttöoikeuden konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="e4296-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="e4296-109">Laajenna Hallinto-vaihtoehto puussa.</span><span class="sxs-lookup"><span data-stu-id="e4296-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="e4296-110">Tarkista, että Sähköinen allekirjoitus -valintaruutu on valittu.</span><span class="sxs-lookup"><span data-stu-id="e4296-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="e4296-111">Jos Sähköinen allekirjoitus -valintaruutua ei ole valittu, ota ylläpitotila käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e4296-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="e4296-112">Ylläpitotila voidaan ottaa käyttöön tässä ympäristössä suorittamalla ylläpitotyö Lifecycle Servicesistä tai käyttämällä paikallisesti Deployment.Setup-työkalua.</span><span class="sxs-lookup"><span data-stu-id="e4296-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="e4296-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e4296-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="e4296-114">Sähköisten allekirjoitusten parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e4296-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="e4296-115">Valitse Organisaation hallinto > Asetukset > Sähköinen allekirjoitus > Sähköisen allekirjoituksen parametrit.</span><span class="sxs-lookup"><span data-stu-id="e4296-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="e4296-116">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="e4296-116">Click Edit.</span></span>
3. <span data-ttu-id="e4296-117">Kirjoita Ilmoitus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e4296-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="e4296-118">Kirjoita ilmoitus, jonka allekirjoittajat saavat allekirjoitusta pyydettäessä.</span><span class="sxs-lookup"><span data-stu-id="e4296-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="e4296-119">Voit käyttää mitä tahansa tekstiä.</span><span class="sxs-lookup"><span data-stu-id="e4296-119">You can enter any text.</span></span> <span data-ttu-id="e4296-120">Yleensä tämä teksti kertoo käyttäjälle, mitä tiedoston sähköinen allekirjoitus tarkoittaa.</span><span class="sxs-lookup"><span data-stu-id="e4296-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="e4296-121">Jos haluat antaa huomautustekstin muilla kielillä, valitse Käännökset.</span><span class="sxs-lookup"><span data-stu-id="e4296-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="e4296-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e4296-122">Click Save.</span></span>
5. <span data-ttu-id="e4296-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e4296-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="e4296-124">Syykoodien määrittäminen sähköisille allekirjoituksille</span><span class="sxs-lookup"><span data-stu-id="e4296-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="e4296-125">Valitse Organisaation hallinto > Asetukset > Sähköinen allekirjoitus > Sähköisen allekirjoituksen syykoodit.</span><span class="sxs-lookup"><span data-stu-id="e4296-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="e4296-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e4296-126">Click New.</span></span>
    * <span data-ttu-id="e4296-127">Syykoodit on määritettävä ennen sähköisten allekirjoitusten käyttöä.</span><span class="sxs-lookup"><span data-stu-id="e4296-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="e4296-128">Voimassa oleva syykoodi tarvitaan tiedostoa allekirjoitettaessa.</span><span class="sxs-lookup"><span data-stu-id="e4296-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="e4296-129">Allekirjoittaja valitsee syykoodin, joka ilmaisee sähköisen allekirjoituksen syyn.</span><span class="sxs-lookup"><span data-stu-id="e4296-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="e4296-130">Syykoodin avulla voi ilmaista esimerkiksi virallisen hyväksynnän.</span><span class="sxs-lookup"><span data-stu-id="e4296-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="e4296-131">Kirjoita Syykoodi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e4296-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="e4296-132">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e4296-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e4296-133">Anna tarvittaessa lisää syykoodeja.</span><span class="sxs-lookup"><span data-stu-id="e4296-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="e4296-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e4296-134">Click Save.</span></span>
6. <span data-ttu-id="e4296-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e4296-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="e4296-136">Sähköisten allekirjoitusten edellyttäminen aiemmin luoduissa prosesseissa</span><span class="sxs-lookup"><span data-stu-id="e4296-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="e4296-137">Valitse Organisaation hallinto > Asetukset > Sähköinen allekirjoitus > Sähköisen allekirjoituksen vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="e4296-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="e4296-138">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e4296-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e4296-139">Valitse prosessi, jossa käytettävä sähköisiä allekirjoituksia.</span><span class="sxs-lookup"><span data-stu-id="e4296-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="e4296-140">Valitse Allekirjoitus vaaditaan -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="e4296-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="e4296-141">Toista nämä vaiheet jokaisen sähköistä allekirjoitusta edellyttävän prosessin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="e4296-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="e4296-142">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e4296-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="e4296-143">Sähköisten allekirjoitusten mukautetun edellytyksen luominen</span><span class="sxs-lookup"><span data-stu-id="e4296-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="e4296-144">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="e4296-144">Click New.</span></span>
2. <span data-ttu-id="e4296-145">Valitse Allekirjoitus vaaditaan -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="e4296-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="e4296-146">Kirjoita sähköistä allekirjoitusta edellyttävän prosessin nimi Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e4296-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="e4296-147">Avaa haku napsauttamalla Taulun nimi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="e4296-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e4296-148">Etsi ja valitse luettelosta taulu, johon allekirjoitusta edellyttävät tiedot on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="e4296-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="e4296-149">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e4296-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e4296-150">Avaa haku napsauttamalla Kentän nimi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="e4296-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e4296-151">Etsi ja valitse luettelossa se taulun kenttä, jota haluat seurata.</span><span class="sxs-lookup"><span data-stu-id="e4296-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="e4296-152">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="e4296-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e4296-153">Määritä, milloin allekirjoitus vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="e4296-153">Specify when a signature is required.</span></span>     <span data-ttu-id="e4296-154">Valitse Aina, jos allekirjoitus vaaditaan kentän tietojen muuttuessa.</span><span class="sxs-lookup"><span data-stu-id="e4296-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="e4296-155">Valitse Vain, jos allekirjoitus vaaditaan vain tietyissä tilanteissa.</span><span class="sxs-lookup"><span data-stu-id="e4296-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="e4296-156">Jos valitset Vain, sinun on valittava jokin seuraavista vaihtoehdoista: Kun tietue lisätään, Kun tietue päivitetään tai Kun tietue poistetaan.</span><span class="sxs-lookup"><span data-stu-id="e4296-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="e4296-157">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e4296-157">Click Save.</span></span>
11. <span data-ttu-id="e4296-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e4296-158">Close the page.</span></span>

