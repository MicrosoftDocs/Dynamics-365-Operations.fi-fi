---
title: Vähennysten määrittäminen
description: Microsoft Dynamics 365 Human Resourcesin vähennysten avulla voit määrittää, kuinka paljon (jos mitään) vähennetään työntekijän palkasta kunkin edun osalta.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5e645c3f098163626cb686aba347897781d7ebc0
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230059"
---
# <a name="configure-deductions"></a><span data-ttu-id="48225-103">Vähennysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="48225-103">Configure deductions</span></span>

<span data-ttu-id="48225-104">Microsoft Dynamics 365 Human Resourcesin vähennysten avulla voit määrittää, kuinka paljon (jos mitään) vähennetään työntekijän palkasta kunkin edun osalta.</span><span class="sxs-lookup"><span data-stu-id="48225-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="48225-105">Vähennyksillä on voimassaoloaika, joten voit ylläpitää vähennystietojen historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="48225-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="48225-106">VValitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Vähennykset**.</span><span class="sxs-lookup"><span data-stu-id="48225-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="48225-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="48225-107">Select **New**.</span></span>

3. <span data-ttu-id="48225-108">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="48225-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="48225-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="48225-109">Field</span></span> | <span data-ttu-id="48225-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="48225-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="48225-111">**Pidätys**</span><span class="sxs-lookup"><span data-stu-id="48225-111">**Deduction**</span></span> | <span data-ttu-id="48225-112">Yksilöllinen tunnus, jota käytetään edun vähennyksen tunnistamisessa.</span><span class="sxs-lookup"><span data-stu-id="48225-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="48225-113">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="48225-113">**Description**</span></span> | <span data-ttu-id="48225-114">Vähennyksen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="48225-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="48225-115">**Voimassa**</span><span class="sxs-lookup"><span data-stu-id="48225-115">**Effective**</span></span> | <span data-ttu-id="48225-116">Alkamispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="48225-116">The start date.</span></span> <span data-ttu-id="48225-117">Oletusarvo on nykyinen järjestelmän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="48225-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="48225-118">**Vanhentumisaika**</span><span class="sxs-lookup"><span data-stu-id="48225-118">**Expiration**</span></span> | <span data-ttu-id="48225-119">Päättymispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="48225-119">The end date.</span></span> <span data-ttu-id="48225-120">Oletusarvona on 12/31/2154, joka tarkoittaa ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="48225-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="48225-121">**Otsikko**</span><span class="sxs-lookup"><span data-stu-id="48225-121">**Heading**</span></span> | <span data-ttu-id="48225-122">Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennys käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa.</span><span class="sxs-lookup"><span data-stu-id="48225-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="48225-123">Tätä käytetään, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa.</span><span class="sxs-lookup"><span data-stu-id="48225-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="48225-124">**Työntekijän palkanlaskennan vähennyksen viite**</span><span class="sxs-lookup"><span data-stu-id="48225-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="48225-125">Palkanlaskentajärjestelmän vähennyskoodi, jota tämä vähennys käyttää vähennyksen työntekijän osassa, kun etuja käsitellään palkanlaskentaa varten.</span><span class="sxs-lookup"><span data-stu-id="48225-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="48225-126">**Summan otsikko**</span><span class="sxs-lookup"><span data-stu-id="48225-126">**Amount heading**</span></span> | <span data-ttu-id="48225-127">Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennysmäärä käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa.</span><span class="sxs-lookup"><span data-stu-id="48225-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="48225-128">Tätä käytetään yleensä, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa.</span><span class="sxs-lookup"><span data-stu-id="48225-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="48225-129">**Voi poistaa**</span><span class="sxs-lookup"><span data-stu-id="48225-129">**Can delete**</span></span> | <span data-ttu-id="48225-130">Määrittää, voiko Dynamics 365 for Finance and Operationsista viety arvo aiheuttaa arvon poistamisen palkanlaskentajärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="48225-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="48225-131">**Yhdistetyt sarakkeet**</span><span class="sxs-lookup"><span data-stu-id="48225-131">**Paired columns**</span></span> | <span data-ttu-id="48225-132">Määrittää, viedäänkö otsikko ja vähennysmäärä palkanlaskentajärjestelmä vierekkäisissä sarakkeissa.</span><span class="sxs-lookup"><span data-stu-id="48225-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="48225-133">**Muutoksen voimaantulopäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="48225-133">**Change effective date**</span></span> | <span data-ttu-id="48225-134">Edun vähennysmuutoksen voimaantulon päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="48225-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="48225-135">Tänä päivämääränä järjestelmä muuttaa edun vähennyksen automaattisesti ja päivittää kaikki tähän vähennykseen liittyvät etuussuunnitelmat, kunhan suoritat **Vähennysmuutoksen päivitys** -käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="48225-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="48225-136">**Vähennyksen muutos valmis**</span><span class="sxs-lookup"><span data-stu-id="48225-136">**Deduction change completed**</span></span> | <span data-ttu-id="48225-137">**Vähennysmuutos suoritettu** -valintaruutu valitaan automaattisesti sen jälkeen, kun edun vähennysmuutokset on tehty vähennyksen päivityksen muutoskäsittelyn jälkeen.</span><span class="sxs-lookup"><span data-stu-id="48225-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="48225-138">Voit seurata ja ylläpitää etuuskurssimäärityksen muutoksia valitsemalla **Toiminnot**ja sitten **Versioiden ylläpito**.</span><span class="sxs-lookup"><span data-stu-id="48225-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="48225-139">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="48225-139">Select **Save**.</span></span> 
