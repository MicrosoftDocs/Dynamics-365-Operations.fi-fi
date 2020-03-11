---
title: Maksutapojen rajoittaminen kuitittomille palautuksille
description: Tässä ohjeaiheessa käsitellään, miten tiettyjä palautusten maksutapoja voidaan rajoittaa, jos palautus tehdään ilman kuittia.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: dfc49e3c3132fe2687ea71e5da75fe31753d57f9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022448"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="f9836-103">Maksutapojen rajoittaminen kuitittomille palautuksille</span><span class="sxs-lookup"><span data-stu-id="f9836-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f9836-104">Jokainen vähittäismyyjän hyväksymä maksutapa on määritettävä, kun järjestelmä on määritetty.</span><span class="sxs-lookup"><span data-stu-id="f9836-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="f9836-105">Tässä ohjeaiheessa käsitellään, miten tiettyjä palautusten maksutapoja voidaan rajoittaa, jos palautus tehdään ilman kuittia.</span><span class="sxs-lookup"><span data-stu-id="f9836-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="f9836-106">Maksutapojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f9836-106">Set up payment methods</span></span>

<span data-ttu-id="f9836-107">Maksutapojen määrittämistä varten on suoritettava seuraavat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="f9836-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="f9836-108">Luo maksutavat, jotka hyväksytään koko organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="f9836-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="f9836-109">Organisaation laajuisten korttityyppien ja korttien numeroiden luominen.</span><span class="sxs-lookup"><span data-stu-id="f9836-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="f9836-110">Jos luottokortit tai pankkikortit hyväksytään, luo ensin yksi korttimaksuvälinetyyppi ja luo sitten organisaation laajuiset korttityypit ja korttien numerot.</span><span class="sxs-lookup"><span data-stu-id="f9836-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="f9836-111">Määritä myymälän maksutavat.</span><span class="sxs-lookup"><span data-stu-id="f9836-111">Set up store payment methods.</span></span> <span data-ttu-id="f9836-112">Liitä maksutavat kuhunkin myymälään ja määritä sitten myymäläkohtaiset asetukset kullekin myymälän maksutavalle.</span><span class="sxs-lookup"><span data-stu-id="f9836-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="f9836-113">Aseta liikkeille korttimaksutavat.</span><span class="sxs-lookup"><span data-stu-id="f9836-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="f9836-114">Suorita korttimaksujen määritys loppuun kaikille korttimaksutavoille, jotka hyväksyt liikkeessä.</span><span class="sxs-lookup"><span data-stu-id="f9836-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="f9836-115">![Myymälän asetukset](media/NoReceiptReturns1.png "Retail POS -asetukset")</span><span class="sxs-lookup"><span data-stu-id="f9836-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="f9836-116">Maksutapojen rajoittaminen kuitittomille palautuksille</span><span class="sxs-lookup"><span data-stu-id="f9836-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="f9836-117">Määritä kullekin myymälän maksutavalle **Myymälän hallinta** -sivun **Kuitittomat palautukset** -kohdan **Rajoitus kuitittomille palautuksille** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f9836-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="f9836-118">Vaihtokytkimen oletusarvo on **Ei**, mikä varmistaa, että maksutapa sallitaan palautuksille.</span><span class="sxs-lookup"><span data-stu-id="f9836-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="f9836-119">Kun **Rajoitus kuitittomille palautuksille** -asetukseksi on valittu **Kyllä**, valittua maksutapaa ei sallita palautuksille.</span><span class="sxs-lookup"><span data-stu-id="f9836-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="f9836-120">![Myymälän maksutapa](media/NoReceiptReturns3.png "Vähittäismyymälän maksutapa")</span><span class="sxs-lookup"><span data-stu-id="f9836-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="f9836-121">Kun kassa valitsee kuitittomien palautusten rajoitetun maksutavan, avautuva sanoma pyytää varmistamaan hyväksytyt maksutavat.</span><span class="sxs-lookup"><span data-stu-id="f9836-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="f9836-122">![Hyväksyttävät maksutavat](media/NoReceiptReturns4.png "Hyväksyttävät maksutavat")</span><span class="sxs-lookup"><span data-stu-id="f9836-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="f9836-123">Jos tapahtuma on sekä kuitillinen että kuititon palautus, rajoitusehtojen noudattamista ei pakoteta, koska tapahtuma palautetaan työnkulkuun kuitillisena.</span><span class="sxs-lookup"><span data-stu-id="f9836-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 
