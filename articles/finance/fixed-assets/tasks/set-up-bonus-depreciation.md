---
title: Bonuspoiston määrittäminen
description: Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad1b7f584d2b2a63dba5f8519ada9d89d6265e7b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815617"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="ab350-103">Bonuspoiston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ab350-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab350-104">Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="ab350-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="ab350-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="ab350-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="ab350-106">Erityisen poistovähennyksen luominen</span><span class="sxs-lookup"><span data-stu-id="ab350-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="ab350-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Erityinen poistovähennys.</span><span class="sxs-lookup"><span data-stu-id="ab350-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="ab350-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ab350-108">Click New.</span></span>
3. <span data-ttu-id="ab350-109">Kirjoita Erityinen poistovähennys -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ab350-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="ab350-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ab350-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ab350-111">Syötä Prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="ab350-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="ab350-112">Määritä summa, jos prosenttia ei ole ilmoitettu.</span><span class="sxs-lookup"><span data-stu-id="ab350-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="ab350-113">Erityisen poistovähennyksen liittäminen käyttöomaisuusryhmän kirjaan</span><span class="sxs-lookup"><span data-stu-id="ab350-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="ab350-114">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="ab350-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="ab350-115">Valitse luettelosta erityiseen poistovähennykseen liitetty käyttöomaisuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="ab350-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="ab350-116">Valitse Kirjat.</span><span class="sxs-lookup"><span data-stu-id="ab350-116">Click Books.</span></span>
4. <span data-ttu-id="ab350-117">Valitse luettelosta erityiseen poistovähennykseen liitetty kirja.</span><span class="sxs-lookup"><span data-stu-id="ab350-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="ab350-118">Valitse Erityinen poistovähennys.</span><span class="sxs-lookup"><span data-stu-id="ab350-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="ab350-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ab350-119">Click New.</span></span>
7. <span data-ttu-id="ab350-120">Kirjoita tai valitse Erityinen poistovähennys -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ab350-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="ab350-121">Prosentin tai summan oletusarvo saadaan erityisen poistovähennyksen asetuksista.</span><span class="sxs-lookup"><span data-stu-id="ab350-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="ab350-122">Syötä numero Prioriteetti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ab350-122">In the Priority field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]