---
title: Määritä nimikkeen kuljetusrajoitteet
description: Tässä menettelyssä asetetaan kuljetusrajoitus, jolla estetään valitun nimikkeen kuljetus valitun keskuksen kautta.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f351da832f8fa62935d09c6ce6ede277971dbbbc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982304"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="97a2b-103">Määritä nimikkeen kuljetusrajoitteet</span><span class="sxs-lookup"><span data-stu-id="97a2b-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97a2b-104">Tässä menettelyssä asetetaan kuljetusrajoitus, jolla estetään valitun nimikkeen kuljetus valitun keskuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="97a2b-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="97a2b-105">Yleensä kuljetuskoordinaattori tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="97a2b-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="97a2b-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="97a2b-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="97a2b-107">Nimikerajoituksen luominen</span><span class="sxs-lookup"><span data-stu-id="97a2b-107">Create an item constaint</span></span>
1. <span data-ttu-id="97a2b-108">Siirry kohtaan Rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="97a2b-108">Go to Constraints.</span></span>
2. <span data-ttu-id="97a2b-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="97a2b-109">Click New.</span></span>
3. <span data-ttu-id="97a2b-110">Kirjoita arvo Nimikerajoitus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="97a2b-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="97a2b-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="97a2b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="97a2b-112">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="97a2b-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="97a2b-113">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="97a2b-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="97a2b-114">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="97a2b-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="97a2b-115">Syötä tai valitse Keskus-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="97a2b-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="97a2b-116">Valitse Rajoitustoiminto-kentästä haluamasi vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="97a2b-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="97a2b-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="97a2b-117">Click Save.</span></span>
11. <span data-ttu-id="97a2b-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="97a2b-118">Close the page.</span></span>

