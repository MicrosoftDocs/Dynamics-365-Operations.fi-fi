---
title: Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen
description: Tässä tehtävän tallennuksessa esitellään arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen.
author: twheeloc
manager: AnnBe
ms.date: 07-01-2019
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
ms.openlocfilehash: a5b539129e62b9b0b10df1f505cbfec5c1143138
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141623"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="a2719-103">Arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a2719-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2719-104">Tässä tehtävän tallennuksessa esitellään arvonlisäveroryhmien ja nimikkeiden arvonlisäveroryhmien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="a2719-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="a2719-105">Arvonlisäveroryhmät ovat asiakkaisiin ja toimittajiin liitettyjen arvonlisäverokoodien ryhmiä.</span><span class="sxs-lookup"><span data-stu-id="a2719-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="a2719-106">Niitä on liitetty myös niiden tapahtumien kirjanpitotileihin, joita ei ole kirjattu tietylle toimittajalle tai asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="a2719-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="a2719-107">Nimikkeiden arvonlisäveroryhmät ovat resursseihin, kuten tuotteisiin, liitettyjen arvonlisäverokoodien ryhmiä.</span><span class="sxs-lookup"><span data-stu-id="a2719-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="a2719-108">Määritettyä tapahtumaa koskeva arvonlisävero määräytyy sekä tapahtuman arvonlisäveroryhmään että nimikkeen arvonlisäveroryhmään sisältyvien arvonlisäverokoodien mukaan.</span><span class="sxs-lookup"><span data-stu-id="a2719-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="a2719-109">Arvonlisävero voidaan laskea vain, jos arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä on valittu kullekin sellaiselle tapahtumalle, jonka osalta arvonlisävero on laskettava tai tallennettava.</span><span class="sxs-lookup"><span data-stu-id="a2719-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="a2719-110">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="a2719-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="a2719-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a2719-111">Click **New**.</span></span>
3. <span data-ttu-id="a2719-112">Kirjoita **Arvonlisäveroryhmä**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a2719-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="a2719-113">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a2719-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a2719-114">Ota käyttöön **Asetukset**-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="a2719-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="a2719-115">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a2719-115">Click **Add**.</span></span>
7. <span data-ttu-id="a2719-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a2719-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="a2719-117">Avaa haku valitsemalla **Arvonlisäverokoodi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a2719-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a2719-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a2719-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a2719-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a2719-119">Click **Save**.</span></span>
11. <span data-ttu-id="a2719-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a2719-120">Close the page.</span></span>
12. <span data-ttu-id="a2719-121">Siirry kohtaan **Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät**.</span><span class="sxs-lookup"><span data-stu-id="a2719-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="a2719-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a2719-122">Click **New**.</span></span>
14. <span data-ttu-id="a2719-123">Kirjoita **Nimikkeen arvonlisäveroryhmä** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a2719-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="a2719-124">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a2719-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="a2719-125">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a2719-125">Click **Add**.</span></span>
17. <span data-ttu-id="a2719-126">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a2719-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a2719-127">Avaa haku valitsemalla **Arvonlisäverokoodi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a2719-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="a2719-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a2719-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="a2719-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a2719-129">Click **Save**.</span></span>

