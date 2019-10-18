---
title: EUR-00015 Osaouolen haku ALV-tunnuksen avulla
description: Tässä toimintaohjeessa esitellään, miten osapuolihaku tehdään rekisteröintitunnuksella.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0427b6e961173543f860ef6e098fc6248afd3aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183618"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="9257d-103">EUR-00015 Osaouolen haku ALV-tunnuksen avulla</span><span class="sxs-lookup"><span data-stu-id="9257d-103">EUR-00015 Party search using VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9257d-104">Tässä toimintaohjeessa esitellään, miten osapuolihaku tehdään rekisteröintitunnuksella.</span><span class="sxs-lookup"><span data-stu-id="9257d-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="9257d-105">Ennen kuin suoritat nämä toimet, ALV-tunnukset on määritettävä ja toimittajien, asiakkaiden ja yritysten ALV-tunnukset on syötettävä järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="9257d-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="9257d-106">Tämä menettely koskee kaikkia Euroopan maita/alueita.</span><span class="sxs-lookup"><span data-stu-id="9257d-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="9257d-107">Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa.</span><span class="sxs-lookup"><span data-stu-id="9257d-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="9257d-108">Nämä toimet tekee yleensä ostoreskontrapäällikkö tai myyntireskontrapäällikkö.</span><span class="sxs-lookup"><span data-stu-id="9257d-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="9257d-109">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="9257d-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="9257d-110">Valitse Organisaation hallinto > Yleinen osoitekirja > Yleinen osoitekirja.</span><span class="sxs-lookup"><span data-stu-id="9257d-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="9257d-111">Valitse Rekisteröintitunnuksen haku.</span><span class="sxs-lookup"><span data-stu-id="9257d-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="9257d-112">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="9257d-112">Click Add.</span></span>
4. <span data-ttu-id="9257d-113">Syötä tai valitse arvo Rekisteröintityyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9257d-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="9257d-114">Jos esimerkiksi haluat löytää osapuolet, joiden rekisteröintitunnus on tyyppiä ALV-tunnus, valitse ALV-tunnus.</span><span class="sxs-lookup"><span data-stu-id="9257d-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="9257d-115">Syötä tai valitse arvo Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9257d-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="9257d-116">Syötä arvoksi esimerkiksi DEU.</span><span class="sxs-lookup"><span data-stu-id="9257d-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="9257d-117">Kirjoita Rekisteröintinumero-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9257d-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="9257d-118">Valitse Etsi.</span><span class="sxs-lookup"><span data-stu-id="9257d-118">Click Find.</span></span>
    * <span data-ttu-id="9257d-119">Kaikki osapuolet, joilla on kyseinen rekisteröintitunnus näytetään.</span><span class="sxs-lookup"><span data-stu-id="9257d-119">All parties with that registration ID will be displayed.</span></span>  

