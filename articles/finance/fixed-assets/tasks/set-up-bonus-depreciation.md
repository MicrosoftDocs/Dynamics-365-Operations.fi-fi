---
title: Bonuspoiston määrittäminen
description: Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91243a4cee44410a221902990d31a10f1805eb08
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138250"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="87bbd-103">Bonuspoiston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="87bbd-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87bbd-104">Tässä menettelyssä kerrotaan, miten erityinen poistovähennys luodaan ja liitetään käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="87bbd-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="87bbd-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="87bbd-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="87bbd-106">Erityisen poistovähennyksen luominen</span><span class="sxs-lookup"><span data-stu-id="87bbd-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="87bbd-107">Siirry kohtaan Käyttöomaisuus > Asetukset > Erityinen poistovähennys.</span><span class="sxs-lookup"><span data-stu-id="87bbd-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="87bbd-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="87bbd-108">Click New.</span></span>
3. <span data-ttu-id="87bbd-109">Kirjoita Erityinen poistovähennys -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="87bbd-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="87bbd-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="87bbd-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="87bbd-111">Syötä Prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="87bbd-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="87bbd-112">Määritä summa, jos prosenttia ei ole ilmoitettu.</span><span class="sxs-lookup"><span data-stu-id="87bbd-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="87bbd-113">Erityisen poistovähennyksen liittäminen käyttöomaisuusryhmän kirjaan</span><span class="sxs-lookup"><span data-stu-id="87bbd-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="87bbd-114">Siirry kohtaan Käyttöomaisuus > Asetukset > Käyttöomaisuusryhmät.</span><span class="sxs-lookup"><span data-stu-id="87bbd-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="87bbd-115">Valitse luettelosta erityiseen poistovähennykseen liitetty käyttöomaisuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="87bbd-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="87bbd-116">Valitse Kirjat.</span><span class="sxs-lookup"><span data-stu-id="87bbd-116">Click Books.</span></span>
4. <span data-ttu-id="87bbd-117">Valitse luettelosta erityiseen poistovähennykseen liitetty kirja.</span><span class="sxs-lookup"><span data-stu-id="87bbd-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="87bbd-118">Valitse Erityinen poistovähennys.</span><span class="sxs-lookup"><span data-stu-id="87bbd-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="87bbd-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="87bbd-119">Click New.</span></span>
7. <span data-ttu-id="87bbd-120">Kirjoita tai valitse Erityinen poistovähennys -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="87bbd-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="87bbd-121">Prosentin tai summan oletusarvo saadaan erityisen poistovähennyksen asetuksista.</span><span class="sxs-lookup"><span data-stu-id="87bbd-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="87bbd-122">Syötä numero Prioriteetti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="87bbd-122">In the Priority field, enter a number.</span></span>

