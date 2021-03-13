---
title: Ennakonpidätysmaksun luominen
description: Ennakonpidätyksen maksutyö tilittää ennakonpidätyssaldot ostoreskontrasta ennakonpidätystileille ja tekee niistä vastakirjauksen kyseisen kauden ennakonpidätyksen tilitystilille. Tässä aiheessa luetellaan ennakonpidätysmaksun määrittämisen vaiheet.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060732"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="2fc4f-104">Ennakonpidätysmaksun luominen</span><span class="sxs-lookup"><span data-stu-id="2fc4f-104">Create a withholding tax payment</span></span>

<span data-ttu-id="2fc4f-105">Ennakonpidätyksen maksutyö tilittää ennakonpidätyssaldot ostoreskontrasta ennakonpidätystileille ja tekee niistä vastakirjauksen kyseisen kauden ennakonpidätyksen tilitystilille.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="2fc4f-106">Tässä aiheessa luetellaan ennakonpidätysmaksun määrittämisen vaiheet.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="2fc4f-107">Ennakonpidätyksen vastakirjausta (myyntireskontrasta) ei oteta huomioon, kun ennakonpidätysmaksu lasketaan.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="2fc4f-108">Siirry kohtaan **Siirtymisruutu > Moduulit > Vero > Ilmoitukset > Ennakonpidätys > Ennakonpidätysmaksu**.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="2fc4f-109">Avaa haku valitsemalla **Tilityskausi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2fc4f-110">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2fc4f-111">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="2fc4f-112">Syötä **Tapahtumapäivä**-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="2fc4f-113">Valitse **Päivitä**, kun haluat kirjata ennakonpidätyksen maksutositteen ennakonpidätyksen tilitystilille.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="2fc4f-114">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2fc4f-114">Click **OK**.</span></span>

![Ennakonpidätysmaksun parametrit](media/withholding-tax-payment.png)