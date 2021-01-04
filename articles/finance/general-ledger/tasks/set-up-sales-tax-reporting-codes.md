---
title: Määritä arvonlisäveroilmoituksen koodit
description: Arvonlisäveron raportointikoodit viittaavat arvonlisäveroraportin kenttänumeroon.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 362d30e56fe35b85d50bfa2df57364733b366fef
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646178"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="16745-103">Määritä arvonlisäveroilmoituksen koodit</span><span class="sxs-lookup"><span data-stu-id="16745-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16745-104">Arvonlisäveron raportointikoodit viittaavat arvonlisäveroraportin kenttänumeroon.</span><span class="sxs-lookup"><span data-stu-id="16745-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="16745-105">Niitä käytetään maakohtaisissa raportin asetteluissa.</span><span class="sxs-lookup"><span data-stu-id="16745-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="16745-106">Niitä käytetään myös arvonlisäveromaksu koodeittain -raportissa.</span><span class="sxs-lookup"><span data-stu-id="16745-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="16745-107">Raportissa näkyvät kunkin raportointikoodin tilityskauden yhteenlasketut arvonlisäverosummat.</span><span class="sxs-lookup"><span data-stu-id="16745-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="16745-108">Kun olet luonut arvonlisäveroraportin koodit, voit viitata niihin **Arvonlisäverokoodi**-sivun Raportin asetukset -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="16745-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="16745-109">Tässä tallenteessa käytetään esittely-yritystä DEMF.</span><span class="sxs-lookup"><span data-stu-id="16745-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="16745-110">Siirry **siirtymisruudussa** kohtaan **Vero > Asetukset > Arvonlisävero > Arvonlisäveroilmoituksen koodit**.</span><span class="sxs-lookup"><span data-stu-id="16745-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="16745-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="16745-111">Click **New**.</span></span>
3. <span data-ttu-id="16745-112">Valitse raportin asettelu, johon raportointikoodi kuuluu.</span><span class="sxs-lookup"><span data-stu-id="16745-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="16745-113">Tätä asettelua käytetään arvonlisäverokoodin käytettävissä olevien raportointikoodien suodattamisessa.</span><span class="sxs-lookup"><span data-stu-id="16745-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="16745-114">Kukin arvonlisäverokoodi kuuluu tilityskauteen, joka kuuluu raportin asettelua käyttävälle arvonlisäveroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="16745-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="16745-115">Kirjoita numero **Raportointikoodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="16745-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="16745-116">Syötä **Raportin teksti** -kenttään raporteissa näkyvä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="16745-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="16745-117">Syötä **Lyhyt kuvaus** -kenttään kuvaus sisäistä käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="16745-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="16745-118">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="16745-118">Click **Save**.</span></span>

