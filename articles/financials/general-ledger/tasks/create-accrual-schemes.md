---
title: Luo jaksotusmalleja
description: Tässä opastuksessa käsitellään jaksotusmallin luominen.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0ae55000a5cf1593d057d940dc3dbbf9e5cb3f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834879"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="f839f-103">Luo jaksotusmalleja</span><span class="sxs-lookup"><span data-stu-id="f839f-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f839f-104">Tässä opastuksessa käsitellään jaksotusmallin luominen.</span><span class="sxs-lookup"><span data-stu-id="f839f-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="f839f-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="f839f-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f839f-106">Valitse Kirjanpito > Kirjauskansion asetukset > Jaksotusmallit.</span><span class="sxs-lookup"><span data-stu-id="f839f-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="f839f-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f839f-107">Click New.</span></span>
3. <span data-ttu-id="f839f-108">Kirjoita Jaksotustunnus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f839f-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="f839f-109">Kirjoita Jaksotusmallin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f839f-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="f839f-110">Määritä Debet-kentässä haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="f839f-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="f839f-111">Määritetty päätili korvaa debet-päätilin kirjauskansion tositerivillä. Sitä käytetään myös kirjanpitojaksotusten tapahtumiin perustuvissa lykkäysten mitätöinnissä.</span><span class="sxs-lookup"><span data-stu-id="f839f-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="f839f-112">Määritä Kredit-kentässä haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="f839f-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="f839f-113">Määritetty päätili korvaa kredit-päätilin kirjauskansion tositerivillä. Sitä käytetään myös kirjanpitojaksotusten tapahtumiin perustuvissa lykkäysten mitätöinnissä.</span><span class="sxs-lookup"><span data-stu-id="f839f-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="f839f-114">Valitse Tosite-kentässä, miten tosite määritetään, kun tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="f839f-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="f839f-115">Kirjoita Kuvaus-kenttään arvo, joka kuvaa kirjattavia tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="f839f-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="f839f-116">Valitse Kausifrekvenssi-kentässä, kuinka usein tapahtumia pitäisi suorittaa.</span><span class="sxs-lookup"><span data-stu-id="f839f-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="f839f-117">Lisää Esiintymien määrä kausittain -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f839f-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="f839f-118">Valitse Kirjaa tapahtumat -kentässä, milloin tapahtumat on kirjattava, esimerkiksi Kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="f839f-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>

