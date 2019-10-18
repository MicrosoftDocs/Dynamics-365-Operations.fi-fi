---
title: Määritä arvonlisäverokoodit
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäverokoodit Dynamics 365 Financeissa.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45a4a7a20b20961d707e43b35d61c10a08c74943
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185977"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="3706d-103">Määritä arvonlisäverokoodit</span><span class="sxs-lookup"><span data-stu-id="3706d-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3706d-104">Tässä ohjeaiheessa kuvataan, kuinka voit määrittää arvonlisäverokoodit.</span><span class="sxs-lookup"><span data-stu-id="3706d-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="3706d-105">Arvonlisäverokoodit luodaan jokaiselle epäsuoralle verolle tai tullimaksulle, jonka yritys on velvollinen laskemaan, perimään ja maksamaan veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="3706d-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="3706d-106">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="3706d-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3706d-107">Siirry kohtaan **Siirtymisruutu > Vero > Välilliset verot > Arvonlisävero > Arvonlisäverokoodit**.</span><span class="sxs-lookup"><span data-stu-id="3706d-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="3706d-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="3706d-108">Select **New**.</span></span>
3. <span data-ttu-id="3706d-109">Kirjoita **Arvonlisäverokoodi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="3706d-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="3706d-110">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="3706d-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="3706d-111">Valitse **tilityskausi** avaamalla avattava luettelo, kun haluat määrittää, arvonlisäveroviranomaiset, joille arvonlisävero ilmoitetaan ja maksetaan sekä ilmoitus- ja maksuvälit.</span><span class="sxs-lookup"><span data-stu-id="3706d-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="3706d-112">Valitse **kirjanpidon kirjausryhmä**, kun haluat määrittää päätilit arvonlisäveron kirjanpitoon kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="3706d-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="3706d-113">Laajenna **Laskenta**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="3706d-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="3706d-114">Se sisältää useita kenttiä, jotka ohjaavat arvonlisäverosummien laskentaa.</span><span class="sxs-lookup"><span data-stu-id="3706d-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="3706d-115">Täytä nämä kentät tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="3706d-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="3706d-116">Valitse käyttöliittymän yläosan **toimintoruudussa** **Arvonlisäverokoodi**.</span><span class="sxs-lookup"><span data-stu-id="3706d-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="3706d-117">Valitse **Arvot**.</span><span class="sxs-lookup"><span data-stu-id="3706d-117">Select **Values**.</span></span>
10. <span data-ttu-id="3706d-118">Kirjoita tämän verokoodin arvo **Arvo**-sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="3706d-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="3706d-119">Jos Summa Alkuperäinen-kentän Yksikkökohtainen summa -kohta on valittu, **Laskenta**-pikavälilehdessä arvo kerrotaan tapahtuman määrällä, kun arvonlisäverosumma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="3706d-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="3706d-120">Jos verokoodi ei ole yksikköperusteinen vero, arvo esitetään prosenttiosuutena, joka kohdistetaan tämän verokoodin alkuperään arvonlisäverosumman laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="3706d-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="3706d-121">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3706d-121">Select **Save**.</span></span>
12. <span data-ttu-id="3706d-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3706d-122">Close the page.</span></span>
13. <span data-ttu-id="3706d-123">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3706d-123">Select **Save**.</span></span>

