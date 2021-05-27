---
title: Sijaintiprofiili ei salli negatiivista varastoa, mutta negatiivinen käytettävissä oleva varasto sallitaan
description: Sijaintiprofiilin Salli negatiivinen varasto -asetuksena on Ei, mutta järjestelmä sallii silti negatiivisen käytettävissä olevan varaston.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026471"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="18d6b-103">Sijaintiprofiili ei salli negatiivista varastoa, mutta negatiivinen käytettävissä oleva varasto sallitaan</span><span class="sxs-lookup"><span data-stu-id="18d6b-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="18d6b-104">Tietopankin numero: 4613622</span><span class="sxs-lookup"><span data-stu-id="18d6b-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="18d6b-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="18d6b-105">Symptoms</span></span>

<span data-ttu-id="18d6b-106">Sijaintiprofiilin **Salli negatiivinen varasto** -asetuksena on *Ei*, mutta järjestelmä sallii silti negatiivisen käytettävissä olevan varaston.</span><span class="sxs-lookup"><span data-stu-id="18d6b-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="18d6b-107">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="18d6b-107">Example scenario</span></span>

<span data-ttu-id="18d6b-108">Valtion sääntelemien tapahtumien osalta järjestelmän on pystyttävä kirjaamaan negatiivinen varasto tappioiden kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="18d6b-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="18d6b-109">Haluat, että nimikkeellä voi olla negatiivinen varasto, mutta vain määritetyissä sijainneissa, kuten säiliöissä.</span><span class="sxs-lookup"><span data-stu-id="18d6b-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="18d6b-110">Jos nimikemalliryhmä sallii negatiivisen varaston, sillä ei ole väliä, onko sijainti määritetty sallimaan negatiivinen varasto.</span><span class="sxs-lookup"><span data-stu-id="18d6b-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="18d6b-111">Jos nimike on määritetty niin, että negatiivinen varasto ei ole sallittu, sijaintiprofiilin asetukset eivät vaikuta siihen.</span><span class="sxs-lookup"><span data-stu-id="18d6b-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="18d6b-112">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="18d6b-112">Resolution</span></span>

<span data-ttu-id="18d6b-113">Sijaintiprofiilin **Salli negatiivinen varasto** -asetus koskee vain varastoprosesseja, kuten keräilyä.</span><span class="sxs-lookup"><span data-stu-id="18d6b-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="18d6b-114">Kuitenkin nimikkeen malliryhmät, jotka on asetettu sallimaan negatiivinen varasto, vaikuttavat kaikkiin inventoinnin- ja varastonhallintamoduuleihin, eikä sijaintiprofiili ohita asetusta.</span><span class="sxs-lookup"><span data-stu-id="18d6b-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="18d6b-115">Voit määrittää, saako varasto käyttää negatiivista varastoa.</span><span class="sxs-lookup"><span data-stu-id="18d6b-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="18d6b-116">Määritä nimikemalliryhmät estämään negatiivinen fyysinen varasto ja määritä vain asianmukainen varasto sallimaan negatiivinen varasto.</span><span class="sxs-lookup"><span data-stu-id="18d6b-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
