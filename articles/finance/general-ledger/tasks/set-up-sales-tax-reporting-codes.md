---
title: Määritä arvonlisäveroilmoituksen koodit
description: Arvonlisäveroraportin koodit viittaavat arvonlisäveroraportin kenttänumeroon.
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
ms.openlocfilehash: 6c18f4fb0db31a959647bb10d2b99d940646676e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976790"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="f62d1-103">Määritä arvonlisäveroilmoituksen koodit</span><span class="sxs-lookup"><span data-stu-id="f62d1-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f62d1-104">Arvonlisäveroraportin koodit viittaavat arvonlisäveroraportin kenttänumeroon.</span><span class="sxs-lookup"><span data-stu-id="f62d1-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="f62d1-105">Niitä käytetään maakohtaisten raporttien asetteluissa ja arvonlisäveromaksu koodeittain -raportissa, kun arvonlisäverosummat tulostetaan tilityskaudella raportointikoodin mukaisena yhteenvetona.</span><span class="sxs-lookup"><span data-stu-id="f62d1-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="f62d1-106">Kun olet luonut arvonlisäveroraportin koodit, voit viitata niihin Arvonlisäverokoodi-sivun Raportin asetukset -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="f62d1-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="f62d1-107">Tässä tallenteessa käytetään esittely-yritystä DEMF.</span><span class="sxs-lookup"><span data-stu-id="f62d1-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="f62d1-108">Siirry **siirtymisruudussa** kohtaan **Vero > Asetukset > Arvonlisävero > Arvonlisäveroilmoituksen koodit**.</span><span class="sxs-lookup"><span data-stu-id="f62d1-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="f62d1-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f62d1-109">Click **New**.</span></span>
3. <span data-ttu-id="f62d1-110">Valitse raportin asettelu, johon raportointikoodi kuuluu.</span><span class="sxs-lookup"><span data-stu-id="f62d1-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="f62d1-111">Tätä asettelua käytetään arvonlisäverokoodin käytettävissä olevien raportointikoodien suodattamisessa.</span><span class="sxs-lookup"><span data-stu-id="f62d1-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="f62d1-112">Kukin arvonlisäverokoodi kuuluu tilityskauteen, joka kuuluu raportin asettelua käyttävälle arvonlisäveroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="f62d1-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="f62d1-113">Kirjoita numero **Raportointikoodi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f62d1-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="f62d1-114">Syötä **Raportin teksti** -kenttään raporteissa näkyvä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f62d1-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="f62d1-115">Syötä **Lyhyt kuvaus** -kenttään kuvaus sisäistä käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="f62d1-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="f62d1-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f62d1-116">Click **Save**.</span></span>

