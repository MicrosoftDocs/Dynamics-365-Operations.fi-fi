---
title: Vähennysten määritys
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008904"
---
# <a name="configure-deductions"></a><span data-ttu-id="3288d-102">Vähennysten määritys</span><span class="sxs-lookup"><span data-stu-id="3288d-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3288d-103">Microsoft Dynamics 365 Human Resourcesin vähennysten avulla voit määrittää, kuinka paljon (jos mitään) vähennetään työntekijän palkasta kunkin edun osalta.</span><span class="sxs-lookup"><span data-stu-id="3288d-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="3288d-104">Vähennyksillä on voimassaoloaika, joten voit ylläpitää vähennystietojen historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="3288d-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="3288d-105">VValitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Vähennykset**.</span><span class="sxs-lookup"><span data-stu-id="3288d-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="3288d-106">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="3288d-106">Select **New**.</span></span>

3. <span data-ttu-id="3288d-107">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="3288d-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3288d-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3288d-108">Field</span></span> | <span data-ttu-id="3288d-109">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3288d-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3288d-110">Pidätys</span><span class="sxs-lookup"><span data-stu-id="3288d-110">Deduction</span></span> | <span data-ttu-id="3288d-111">Yksilöllinen tunnus, jota käytetään edun vähennyksen tunnistamisessa.</span><span class="sxs-lookup"><span data-stu-id="3288d-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="3288d-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3288d-112">Description</span></span> | <span data-ttu-id="3288d-113">Vähennyksen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3288d-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="3288d-114">Voimassa</span><span class="sxs-lookup"><span data-stu-id="3288d-114">Effective</span></span> | <span data-ttu-id="3288d-115">Alkamispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3288d-115">The start date.</span></span> <span data-ttu-id="3288d-116">Oletusarvo on nykyinen järjestelmän päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3288d-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="3288d-117">Vanhentumisaika</span><span class="sxs-lookup"><span data-stu-id="3288d-117">Expiration</span></span> | <span data-ttu-id="3288d-118">Päättymispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3288d-118">The end date.</span></span> <span data-ttu-id="3288d-119">Oletusarvona on 12/31/2154, joka tarkoittaa ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="3288d-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="3288d-120">Otsikko</span><span class="sxs-lookup"><span data-stu-id="3288d-120">Heading</span></span> | <span data-ttu-id="3288d-121">Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennys käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa.</span><span class="sxs-lookup"><span data-stu-id="3288d-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="3288d-122">Tätä käytetään, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa.</span><span class="sxs-lookup"><span data-stu-id="3288d-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="3288d-123">Työntekijän palkanlaskennan vähennyksen viite</span><span class="sxs-lookup"><span data-stu-id="3288d-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="3288d-124">Palkanlaskentajärjestelmän vähennyskoodi, jota tämä vähennys käyttää vähennyksen työntekijän osassa, kun etuja käsitellään palkanlaskentaa varten.</span><span class="sxs-lookup"><span data-stu-id="3288d-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="3288d-125">Summan otsikko</span><span class="sxs-lookup"><span data-stu-id="3288d-125">Amount heading</span></span> | <span data-ttu-id="3288d-126">Palkanlaskentajärjestelmän otsikkokoodi, jota tämä vähennysmäärä käyttää vähennyksen työntekijäosuudesta, kun etuja käsitellään palkanlaskennassa.</span><span class="sxs-lookup"><span data-stu-id="3288d-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="3288d-127">Tätä käytetään yleensä, kun käytetään kolmannen osapuolen palkanlaskennan tarjoajaa.</span><span class="sxs-lookup"><span data-stu-id="3288d-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="3288d-128">Voi poistaa</span><span class="sxs-lookup"><span data-stu-id="3288d-128">Can delete</span></span> | <span data-ttu-id="3288d-129">Määrittää, voiko Dynamics 365 for Finance and Operationsista viety arvo aiheuttaa arvon poistamisen palkanlaskentajärjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="3288d-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="3288d-130">Yhdistetyt sarakkeet</span><span class="sxs-lookup"><span data-stu-id="3288d-130">Paired columns</span></span> | <span data-ttu-id="3288d-131">Määrittää, viedäänkö otsikko ja vähennysmäärä palkanlaskentajärjestelmä vierekkäisissä sarakkeissa.</span><span class="sxs-lookup"><span data-stu-id="3288d-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="3288d-132">Muutoksen voimaantulopäivämäärä</span><span class="sxs-lookup"><span data-stu-id="3288d-132">Change effective date</span></span> | <span data-ttu-id="3288d-133">Edun vähennysmuutoksen voimaantulon päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3288d-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="3288d-134">Tänä päivämääränä järjestelmä muuttaa edun vähennyksen automaattisesti ja päivittää kaikki tähän vähennykseen liittyvät etuussuunnitelmat, kunhan suoritat vähennysmuutoksen päivityskäsittelyn.</span><span class="sxs-lookup"><span data-stu-id="3288d-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="3288d-135">Vähennyksen muutos valmis</span><span class="sxs-lookup"><span data-stu-id="3288d-135">Deduction change completed</span></span> | <span data-ttu-id="3288d-136">Vähennysmuutos suoritettu -valintaruutu valitaan automaattisesti sen jälkeen, kun edun vähennysmuutokset on tehty vähennyksen päivityksen muutoskäsittelyn jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3288d-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="3288d-137">Voit seurata ja ylläpitää etuuskurssimäärityksen muutoksia valitsemalla **Toiminnot**ja sitten **Versioiden ylläpito**.</span><span class="sxs-lookup"><span data-stu-id="3288d-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="3288d-138">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3288d-138">Select **Save**.</span></span> 
