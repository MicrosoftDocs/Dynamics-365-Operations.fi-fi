--- 
title: "Määritä arvonlisäveroilmoituksen koodit"
description: "Arvonlisäveroraportin koodit viittaavat arvonlisäveroraportin kenttänumeroon."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4543cf7eaa0b1ef8e32d3fdafa2c354cd3739256
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="bc9ef-103">Määritä arvonlisäveroilmoituksen koodit</span><span class="sxs-lookup"><span data-stu-id="bc9ef-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc9ef-104">Arvonlisäveroraportin koodit viittaavat arvonlisäveroraportin kenttänumeroon.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="bc9ef-105">Niitä käytetään maakohtaisten raporttien asetteluissa ja arvonlisäveromaksu koodeittain -raportissa, kun arvonlisäverosummat tulostetaan tilityskaudella raportointikoodin mukaisena yhteenvetona.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="bc9ef-106">Kun olet luonut arvonlisäveroraportin koodit, voit viitata niihin Arvonlisäverokoodi-sivun Raportin asetukset -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="bc9ef-107">Tässä tallenteessa käytetään esittely-yritystä DEMF.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="bc9ef-108">Valitse Vero > Asetukset > Arvonlisäveroraportin koodit.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="bc9ef-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-109">Click New.</span></span>
3. <span data-ttu-id="bc9ef-110">Valitse raportin asettelu, johon raportointikoodi kuuluu.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="bc9ef-111">Tätä asettelua käytetään arvonlisäverokoodin käytettävissä olevien raportointikoodien suodattamisessa.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="bc9ef-112">Kukin arvonlisäverokoodi kuuluu tilityskauteen, joka kuuluu raportin asettelua käyttävälle arvonlisäveroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="bc9ef-113">Syötä numero, joka viittaa arvonlisäveroraportin kenttään.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="bc9ef-114">Syötä Raportin teksti -kenttään raporteissa näkyvä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="bc9ef-115">Syötä Lyhyt kuvaus -kenttään kuvaus sisäistä käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="bc9ef-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="bc9ef-116">Click Save.</span></span>


