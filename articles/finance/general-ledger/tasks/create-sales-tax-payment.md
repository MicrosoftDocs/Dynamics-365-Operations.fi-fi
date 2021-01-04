---
title: Arvonlisäveromaksun luominen
description: Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aec00c2fb657f0b4074063ef7acad5f4372ebca
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646332"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="bc071-103">Arvonlisäveromaksun luominen</span><span class="sxs-lookup"><span data-stu-id="bc071-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc071-104">Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille.</span><span class="sxs-lookup"><span data-stu-id="bc071-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="bc071-105">Siirry kohtaan **Vero > Ilmoitukset > Arvonlisävero > Tilitä ja kirjaa arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="bc071-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="bc071-106">Avaa haku valitsemalla **Tilityskausi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="bc071-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bc071-107">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="bc071-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bc071-108">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bc071-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="bc071-109">Jos **Sisällytä korjaukset** -vaihtoehtoa ei ole valittu **Kirjanpidon parametri** -sivulla, tilitystä ei voi suorittaa eri versioille.</span><span class="sxs-lookup"><span data-stu-id="bc071-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="bc071-110">Alkuperäinen on kausivälin ensimmäinen tilitys. Se voidaan käsitellä vain kerran kausivälin aikana.</span><span class="sxs-lookup"><span data-stu-id="bc071-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="bc071-111">Uusimmat korjaukset tilittävät arvonlisäverotapahtumat, jotka on kirjattu alkuperäisen version luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bc071-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="bc071-112">Syötä **Tapahtumapäivä**-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="bc071-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="bc071-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc071-113">Click **OK**.</span></span>

