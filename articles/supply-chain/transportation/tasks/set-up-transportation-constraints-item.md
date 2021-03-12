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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 244cf7337ec856f7517a3c0c3e055a90ab65b13f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973932"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="07346-103">Määritä nimikkeen kuljetusrajoitteet</span><span class="sxs-lookup"><span data-stu-id="07346-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07346-104">Tässä menettelyssä asetetaan kuljetusrajoitus, jolla estetään valitun nimikkeen kuljetus valitun keskuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="07346-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="07346-105">Yleensä kuljetuskoordinaattori tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="07346-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="07346-106">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="07346-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="07346-107">Nimikerajoituksen luominen</span><span class="sxs-lookup"><span data-stu-id="07346-107">Create an item constaint</span></span>
1. <span data-ttu-id="07346-108">Siirry kohtaan Rajoitukset.</span><span class="sxs-lookup"><span data-stu-id="07346-108">Go to Constraints.</span></span>
2. <span data-ttu-id="07346-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="07346-109">Click New.</span></span>
3. <span data-ttu-id="07346-110">Kirjoita arvo Nimikerajoitus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="07346-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="07346-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="07346-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="07346-112">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="07346-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="07346-113">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="07346-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="07346-114">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="07346-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="07346-115">Syötä tai valitse Keskus-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="07346-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="07346-116">Valitse Rajoitustoiminto-kentästä haluamasi vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="07346-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="07346-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="07346-117">Click Save.</span></span>
11. <span data-ttu-id="07346-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="07346-118">Close the page.</span></span>

