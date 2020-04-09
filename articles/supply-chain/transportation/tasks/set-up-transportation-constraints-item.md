---
title: Määritä nimikkeen kuljetusrajoitteet
description: Tässä menettelyssä asetetaan kuljetusrajoitus, jolla estetään valitun nimikkeen kuljetus valitun keskuksen kautta.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ccd7d79fbcdd600f78dbff98ce39c04865afe37
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146143"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="30dad-103">Määritä nimikkeen kuljetusrajoitteet</span><span class="sxs-lookup"><span data-stu-id="30dad-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30dad-104">Tässä menettelyssä asetetaan kuljetusrajoitus, jolla estetään valitun nimikkeen kuljetus valitun keskuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="30dad-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="30dad-105">Yleensä kuljetuskoordinaattori tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="30dad-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="30dad-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="30dad-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="30dad-107">Nimikerajoituksen luominen</span><span class="sxs-lookup"><span data-stu-id="30dad-107">Create an item constaint</span></span>
1. <span data-ttu-id="30dad-108">Siirry kohtaan Rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="30dad-108">Go to Constraints.</span></span>
2. <span data-ttu-id="30dad-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="30dad-109">Click New.</span></span>
3. <span data-ttu-id="30dad-110">Kirjoita arvo Nimikerajoitus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="30dad-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="30dad-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="30dad-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="30dad-112">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="30dad-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="30dad-113">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="30dad-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="30dad-114">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="30dad-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="30dad-115">Syötä tai valitse Keskus-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="30dad-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="30dad-116">Valitse Rajoitustoiminto-kentästä haluamasi vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="30dad-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="30dad-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="30dad-117">Click Save.</span></span>
11. <span data-ttu-id="30dad-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="30dad-118">Close the page.</span></span>

