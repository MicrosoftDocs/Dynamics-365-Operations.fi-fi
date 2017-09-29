--- 
title: Osapuolen haku ALV-tunnuksen avulla
description: "Tässä toimintaohjeessa esitellään, miten osapuolihaku tehdään rekisteröintitunnuksella."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f47dfd99a99995bff3a5c443631fa724d36165bf
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="party-search-using-vat-id"></a><span data-ttu-id="0c4e2-103">Osapuolen haku ALV-tunnuksen avulla</span><span class="sxs-lookup"><span data-stu-id="0c4e2-103">Party search using VAT ID</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c4e2-104">Tässä toimintaohjeessa esitellään, miten osapuolihaku tehdään rekisteröintitunnuksella.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="0c4e2-105">Ennen kuin suoritat nämä toimet, ALV-tunnukset on määritettävä ja toimittajien, asiakkaiden ja yritysten ALV-tunnukset on syötettävä järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="0c4e2-106">Tämä menettely koskee kaikkia Euroopan maita/alueita.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="0c4e2-107">Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="0c4e2-108">Nämä toimet tekee yleensä ostoreskontrapäällikkö tai myyntireskontrapäällikkö.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="0c4e2-109">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="0c4e2-110">Valitse Organisaation hallinto > Yleinen osoitekirja > Yleinen osoitekirja.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="0c4e2-111">Valitse Rekisteröintitunnuksen haku.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="0c4e2-112">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-112">Click Add.</span></span>
4. <span data-ttu-id="0c4e2-113">Syötä tai valitse arvo Rekisteröintityyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="0c4e2-114">Jos esimerkiksi haluat löytää osapuolet, joiden rekisteröintitunnus on tyyppiä ALV-tunnus, valitse ALV-tunnus.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="0c4e2-115">Syötä tai valitse arvo Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="0c4e2-116">Syötä arvoksi esimerkiksi DEU.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="0c4e2-117">Kirjoita Rekisteröintinumero-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="0c4e2-118">Valitse Etsi.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-118">Click Find.</span></span>
    * <span data-ttu-id="0c4e2-119">Kaikki osapuolet, joilla on kyseinen rekisteröintitunnus näytetään.</span><span class="sxs-lookup"><span data-stu-id="0c4e2-119">All parties with that registration ID will be displayed.</span></span>  


