---
title: Virhe tapahtuu, kun sijainti valitaan keräysluettelon rekisteröinnin aikana
description: Virhe tapahtuu, kun sijainti valitaan keräysluettelon rekisteröinnin aikana.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026457"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="a222b-103">Virhe tapahtuu, kun sijainti valitaan keräysluettelon rekisteröinnin aikana</span><span class="sxs-lookup"><span data-stu-id="a222b-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="a222b-104">Tietopankin numero: 4613106</span><span class="sxs-lookup"><span data-stu-id="a222b-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="a222b-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="a222b-105">Symptoms</span></span>

<span data-ttu-id="a222b-106">Tämä ongelma ilmenee, kun järjestelmä on määritetty varaamaan myyntitilaukset automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a222b-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="a222b-107">Jos yrität valita keräysluettelon rekisteröintirivin sijainnin, näkyviin tulee seuraava virhesanoma käytettäessä varastonhallinnan (WMS) varausprosesseja:</span><span class="sxs-lookup"><span data-stu-id="a222b-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="a222b-108">Määrää ei voi päivittää uusilla dimensioilla</span><span class="sxs-lookup"><span data-stu-id="a222b-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="a222b-109">Tämä ongelma voi ilmetä, koska käytettävissä oleva varasto ei riitä määritettyyn sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="a222b-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="a222b-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="a222b-110">Resolution</span></span>

<span data-ttu-id="a222b-111">Järjestelmä käyttäytyy suunnitellulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="a222b-111">The system is behaving as designed.</span></span>

<span data-ttu-id="a222b-112">Varastotason varausprosessia käytettäessä, jos käyttövarastoa ei varata kaikille varastodimensiotasoille eikä käyttövarastoa ole tarpeeksi määritetyssä sijainnissa, on suositeltavaa käyttää keräilyrivin manuaalista varausprosessia.</span><span class="sxs-lookup"><span data-stu-id="a222b-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="a222b-113">Tämän jälkeen voit jakaa kaikkien käytettävissä olevien varastomäärien alemmat varaukset, kuten sijainnin, *Varaa erä* -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="a222b-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
