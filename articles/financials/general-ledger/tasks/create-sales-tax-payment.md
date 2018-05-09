--- 
title: "Arvonlisäveromaksun luominen"
description: "Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 28d4b38ea2efeff5ada787e8a74b85037e6a78af
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="4eba9-103">Arvonlisäveromaksun luominen</span><span class="sxs-lookup"><span data-stu-id="4eba9-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4eba9-104">Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille.</span><span class="sxs-lookup"><span data-stu-id="4eba9-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="4eba9-105">Valitse Vero > Ilmoitukset > Arvonlisävero > Tilitä ja kirjaa arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="4eba9-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="4eba9-106">Avaa haku valitsemalla Tilityskausi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4eba9-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="4eba9-107">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4eba9-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4eba9-108">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4eba9-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="4eba9-109">Jos Sisällytä korjaukset -vaihtoehtoa ei ole valittu Kirjanpidon parametri -sivulla, tilitystä ei voi suorittaa eri versioille.</span><span class="sxs-lookup"><span data-stu-id="4eba9-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="4eba9-110">Alkuperäinen on kausivälin ensimmäinen tilitys. Se voidaan käsitellä vain kerran kausivälin aikana.</span><span class="sxs-lookup"><span data-stu-id="4eba9-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="4eba9-111">Uusimmat korjaukset tilittävät arvonlisäverotapahtumat, jotka on kirjattu alkuperäisen version luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="4eba9-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="4eba9-112">Syötä Tapahtumapäivä-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="4eba9-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="4eba9-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4eba9-113">Click OK.</span></span>


