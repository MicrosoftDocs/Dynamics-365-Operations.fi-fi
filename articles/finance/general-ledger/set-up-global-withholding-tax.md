---
title: Määritä yleinen ennakonpidätys
description: Tässä ohjeaiheessa on luettelo vaiheista myynnin ja ostojen yleisen ennakonpidätyksen määrittämiseksi.
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
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ee577651694f0553447d6e9d0851402a586f363
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060730"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="d25f9-103">Määritä yleinen ennakonpidätys</span><span class="sxs-lookup"><span data-stu-id="d25f9-103">Set up global withholding tax</span></span>

<span data-ttu-id="d25f9-104">Tässä ohjeaiheessa on luettelo vaiheista myynnin ja ostojen yleisen ennakonpidätyksen määrittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="d25f9-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="d25f9-105">Määritä ennakonpidätysviranomaiset **Ennakonpidätysviranomaiset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d25f9-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="d25f9-106">Määritä ennakonpidätyksen tilityskaudet **Ennakonpidätyksen tilityskaudet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d25f9-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="d25f9-107">Määritä ennakonpidätyksen kirjanpidon kirjausryhmä **Ennakonpidätys > Kirjanpidon kirjausryhmä** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d25f9-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="d25f9-108">**Ennakonpidätys**-tilille määritetään päätili, jonka **Kirjaustyyppi** on Ennakonpidätys.</span><span class="sxs-lookup"><span data-stu-id="d25f9-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="d25f9-109">**Ennakonpidätyksen vastatilille** määritetään myös päätili, jonka **Kirjaustyyppi** on Ennakonpidätyksen vastatili.</span><span class="sxs-lookup"><span data-stu-id="d25f9-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="d25f9-110">Siirry kohtaan **Kirjanpito > Tilikartta > Tilit > Päätilit** ja määritä päätileille **Kirjaustyyppi** alilomakkeessa **Kirjauksen oikeellisuustarkistus**.</span><span class="sxs-lookup"><span data-stu-id="d25f9-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="d25f9-111">Määritä ennakonpidätyskoodit **Ennakonpidätyskoodit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d25f9-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="d25f9-112">Määritä ennakonpidätysryhmät **Ennakonpidätysryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d25f9-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="d25f9-113">Määritä ennakonpidätyksen tuottotyypit **Ennakonpidätyksen** **tuottotyypit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d25f9-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="d25f9-114">Määritä nimikkeen tai palvelun ennakonpidätysryhmät **Nimikkeen ennakonpidätysryhmät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d25f9-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="d25f9-115">Määritä **Laskun vähimmäissumma** sivulla **Kirjanpitoparametrit > Ennakonpidätys**.</span><span class="sxs-lookup"><span data-stu-id="d25f9-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>
