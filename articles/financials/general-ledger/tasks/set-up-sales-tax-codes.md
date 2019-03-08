---
title: Määritä arvonlisäverokoodit
description: Arvonlisäverokoodit luodaan jokaiselle epäsuoralle verolle tai tullimaksulle, jonka yritys on velvollinen laskemaan, perimään ja maksamaan veroviranomaisille.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "349167"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="a3334-103">Määritä arvonlisäverokoodit</span><span class="sxs-lookup"><span data-stu-id="a3334-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3334-104">Arvonlisäverokoodit luodaan jokaiselle epäsuoralle verolle tai tullimaksulle, jonka yritys on velvollinen laskemaan, perimään ja maksamaan veroviranomaisille.</span><span class="sxs-lookup"><span data-stu-id="a3334-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="a3334-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="a3334-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="a3334-106">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäverokoodit.</span><span class="sxs-lookup"><span data-stu-id="a3334-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="a3334-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a3334-107">Click New.</span></span>
3. <span data-ttu-id="a3334-108">Kirjoita Arvonlisäverokoodi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a3334-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="a3334-109">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a3334-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a3334-110">Valitse tilityskausi, kun haluat määrittää, arvonlisäveroviranomaiset, joille arvonlisävero ilmoitetaan ja maksetaan sekä ilmoitus- ja maksuvälit.</span><span class="sxs-lookup"><span data-stu-id="a3334-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="a3334-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a3334-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a3334-112">Valitse kirjanpidon kirjausryhmä, kun haluat määrittää päätilit arvonlisäveron kirjanpitoon kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="a3334-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="a3334-113">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a3334-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a3334-114">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a3334-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a3334-115">Laajenna Laskenta-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="a3334-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="a3334-116">Laskenta-pikavälilehti sisältää useita kenttiä, jotka ohjaavat arvonlisäverosummien laskentaa.</span><span class="sxs-lookup"><span data-stu-id="a3334-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="a3334-117">Valitse toimintoruudussa Arvonlisäverokoodi.</span><span class="sxs-lookup"><span data-stu-id="a3334-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="a3334-118">Valitse Arvot.</span><span class="sxs-lookup"><span data-stu-id="a3334-118">Click Values.</span></span>
13. <span data-ttu-id="a3334-119">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a3334-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="a3334-120">Syötä tämän verokoodin arvo.</span><span class="sxs-lookup"><span data-stu-id="a3334-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="a3334-121">Jos Summa Alkuperäinen-kentän Yksikkökohtainen summa -kohta on valittu, Laskenta-pikavälilehdessä arvo kerrotaan tapahtuman määrällä, kun arvonlisäverosumma lasketaan.</span><span class="sxs-lookup"><span data-stu-id="a3334-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="a3334-122">Jos verokoodi ei ole yksikköperusteinen vero, arvo esitetään prosenttiosuutena, joka kohdistetaan tämän verokoodin alkuperään arvonlisäverosumman laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="a3334-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="a3334-123">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a3334-123">Click Save.</span></span>
16. <span data-ttu-id="a3334-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a3334-124">Close the page.</span></span>
17. <span data-ttu-id="a3334-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a3334-125">Click Save.</span></span>

