--- 
title: Luo jaksotusmalleja
description: "Tässä opastuksessa käsitellään jaksotusmallin luominen."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="59a80-103">Luo jaksotusmalleja</span><span class="sxs-lookup"><span data-stu-id="59a80-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59a80-104">Tässä opastuksessa käsitellään jaksotusmallin luominen.</span><span class="sxs-lookup"><span data-stu-id="59a80-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="59a80-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="59a80-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="59a80-106">Valitse Kirjanpito > Kirjauskansion asetukset > Jaksotusmallit.</span><span class="sxs-lookup"><span data-stu-id="59a80-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="59a80-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="59a80-107">Click New.</span></span>
3. <span data-ttu-id="59a80-108">Kirjoita Jaksotustunnus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="59a80-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="59a80-109">Kirjoita Jaksotusmallin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="59a80-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="59a80-110">Määritä Debet-kentässä haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="59a80-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="59a80-111">Määritetty päätili korvaa debet-päätilin kirjauskansion tositerivillä. Sitä käytetään myös kirjanpitojaksotusten tapahtumiin perustuvissa lykkäysten mitätöinnissä.</span><span class="sxs-lookup"><span data-stu-id="59a80-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="59a80-112">Määritä Kredit-kentässä haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="59a80-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="59a80-113">Määritetty päätili korvaa kredit-päätilin kirjauskansion tositerivillä. Sitä käytetään myös kirjanpitojaksotusten tapahtumiin perustuvissa lykkäysten mitätöinnissä.</span><span class="sxs-lookup"><span data-stu-id="59a80-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="59a80-114">Valitse Tosite-kentässä, miten tosite määritetään, kun tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="59a80-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="59a80-115">Kirjoita Kuvaus-kenttään arvo, joka kuvaa kirjattavia tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="59a80-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="59a80-116">Valitse Kausifrekvenssi-kentässä, kuinka usein tapahtumia pitäisi suorittaa.</span><span class="sxs-lookup"><span data-stu-id="59a80-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="59a80-117">Lisää Esiintymien määrä kausittain -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="59a80-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="59a80-118">Valitse Kirjaa tapahtumat -kentässä, milloin tapahtumat on kirjattava, esimerkiksi Kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="59a80-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


