---
title: Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen
description: Tässä tehtävän tallennuksessa esitellään arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c58755be2c927de1d308576a2bff2ed3340db34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846268"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="64016-103">Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="64016-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64016-104">Tässä tehtävän tallennuksessa esitellään arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="64016-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="64016-105">Arvonlisäveroryhmät ovat asiakkaisiin ja toimittajiin liitettyjen arvonlisäverokoodien ryhmiä.</span><span class="sxs-lookup"><span data-stu-id="64016-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="64016-106">Niitä on liitetty myös niiden tapahtumien kirjanpitotileihin, joita ei ole kirjattu tietylle toimittajalle tai asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="64016-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="64016-107">Nimikkeiden arvonlisäveroryhmät ovat resursseihin, kuten tuotteisiin, liitettyjen arvonlisäverokoodien ryhmiä.</span><span class="sxs-lookup"><span data-stu-id="64016-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="64016-108">Määritettyä tapahtumaa koskeva arvonlisävero määräytyy sekä tapahtuman arvonlisäveroryhmään että nimikkeen arvonlisäveroryhmään sisältyvien arvonlisäverokoodien mukaan.</span><span class="sxs-lookup"><span data-stu-id="64016-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="64016-109">Arvonlisävero voidaan laskea vain, jos arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä on valittu kullekin sellaiselle tapahtumalle, jonka osalta arvonlisävero on laskettava tai tallennettava.</span><span class="sxs-lookup"><span data-stu-id="64016-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="64016-110">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät.</span><span class="sxs-lookup"><span data-stu-id="64016-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="64016-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="64016-111">Click New.</span></span>
3. <span data-ttu-id="64016-112">Kirjoita Arvonlisäveroryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="64016-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="64016-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="64016-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="64016-114">Ota käyttöön Asetukset-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="64016-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="64016-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="64016-115">Click Add.</span></span>
7. <span data-ttu-id="64016-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="64016-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="64016-117">Avaa haku valitsemalla Arvonlisäverokoodi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="64016-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="64016-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="64016-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="64016-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="64016-119">Click Save.</span></span>
11. <span data-ttu-id="64016-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="64016-120">Close the page.</span></span>
12. <span data-ttu-id="64016-121">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät.</span><span class="sxs-lookup"><span data-stu-id="64016-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="64016-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="64016-122">Click New.</span></span>
14. <span data-ttu-id="64016-123">Kirjoita Nimikkeen arvonlisäveroryhmä -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="64016-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="64016-124">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="64016-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="64016-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="64016-125">Click Add.</span></span>
17. <span data-ttu-id="64016-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="64016-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="64016-127">Avaa haku valitsemalla Arvonlisäverokoodi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="64016-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="64016-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="64016-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="64016-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="64016-129">Click Save.</span></span>

