---
title: Arvonlisäveromaksun luominen
description: Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5066689fb85dd176da1ca1561614e443cb87d816
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832751"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="1bd3b-103">Arvonlisäveromaksun luominen</span><span class="sxs-lookup"><span data-stu-id="1bd3b-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1bd3b-104">Tilitys- ja arvonlisäveron kirjaustyö tilittävät arvonlisäverosaldot arvonlisäverotileille ja tekee niistä vastakirjauksen kyseisen kauden arvonlisäveron tilitystilille.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="1bd3b-105">Siirry kohtaan **Vero > Ilmoitukset > Arvonlisävero > Tilitä ja kirjaa arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="1bd3b-106">Avaa haku valitsemalla **Tilityskausi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1bd3b-107">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1bd3b-108">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="1bd3b-109">Jos **Sisällytä korjaukset** -vaihtoehtoa ei ole valittu **Kirjanpidon parametri** -sivulla, tilitystä ei voi suorittaa eri versioille.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="1bd3b-110">Alkuperäinen on kausivälin ensimmäinen tilitys. Se voidaan käsitellä vain kerran kausivälin aikana.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="1bd3b-111">Uusimmat korjaukset tilittävät arvonlisäverotapahtumat, jotka on kirjattu alkuperäisen version luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="1bd3b-112">Syötä **Tapahtumapäivä**-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="1bd3b-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1bd3b-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]