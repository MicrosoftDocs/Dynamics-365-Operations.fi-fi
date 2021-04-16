---
title: Ylläpitosopimuksen työnkulun yleiskuvaus
description: Tässä aiheessa on yleiskuvaus ylläpitosopimuksen työnkulusta.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbc87dc9c6327550020270468346800a7b80f4c3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817386"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="64be8-103">Ylläpitosopimuksen työnkulun yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="64be8-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="64be8-104">Olet vastuussa valoyrityksen ylläpitosopimuksista. Yrityksesi tarjoaa valotelineiden huollon ylläpitosopimuksia.</span><span class="sxs-lookup"><span data-stu-id="64be8-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="64be8-105">Asiakas lähestyy yritystä ostaakseen valotelineen huollon ylläpitosopimuksen vuodeksi.</span><span class="sxs-lookup"><span data-stu-id="64be8-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="64be8-106">Ylläpitosopimuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="64be8-106">Setting up subscriptions</span></span>

<span data-ttu-id="64be8-107">Ylläpitosopimuksen määrittäminen alkaa siitä, että luot ylläpitosopimusryhmän uudelle huoltosopimukselle tai tarkistat, että ylläpitosopimusryhmä on olemassa.</span><span class="sxs-lookup"><span data-stu-id="64be8-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="64be8-108">Jos ylläpitosopimusryhmä on olemassa, se on määritettävä niin, että asiakasta laskutetaan kerran vuodessa ja että myyntituotto jaksotetaan kerran kuukaudessa.</span><span class="sxs-lookup"><span data-stu-id="64be8-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="64be8-109">Lisätietoja nimikkeiden veroryhmien määrittämisestä on kohdassa [Ylläpitosopimusryhmien määrittäminen](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="64be8-110">Voit luoda ylläpitosopimuksen ylläpitosopimusryhmän luonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="64be8-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="64be8-111">Lisätietoja huollon ylläpitosopimusten luonnista on kohdassa [Huollon ylläpitosopimusten luominen ylläpitosopimusryhmästä](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="64be8-112">Ylläpitosopimustapahtumien luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="64be8-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="64be8-113">Ylläpitosopimuksen määrittämisen jälkeen voit luoda ylläpitosopimuksen maksutapahtuman ensimmäiselle laskutuskaudelle, joka on yksi vuosi.</span><span class="sxs-lookup"><span data-stu-id="64be8-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="64be8-114">Tapahtumien tyyppi on **Säännöllinen**.</span><span class="sxs-lookup"><span data-stu-id="64be8-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="64be8-115">Voit luoda siksi vain ylläpitosopimustapahtumia, joiden aloituspäivämäärä ja lopetuspäivämäärä vastaavat jaksoja, jotka on luotu aiemmin **Kausityypit**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="64be8-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="64be8-116">Saat lisätietoja maksutapahtumista kohdasta [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="64be8-117">Muistat asiakkaan ylläpitosopimuksen määrittämisen jälkeen, että he neuvottelivat 10 prosentin alennuksen kaikista palvelutarjonnoista.</span><span class="sxs-lookup"><span data-stu-id="64be8-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="64be8-118">Sinun on siis alennettava luomasi tapahtumamaksun hintaa.</span><span class="sxs-lookup"><span data-stu-id="64be8-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="64be8-119">Asiakas soittaa myöhemmin samana päivänä ja ilmoittaa, että samalla kun he yhä haluavat valotelineen huoltosopimuksen, he ovat aikeissa tuoda markkinoille uuden valotelineen myöhemmin tänä vuonna.</span><span class="sxs-lookup"><span data-stu-id="64be8-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="64be8-120">Siksi he tarvitsevat huoltoa vain lokakuulle 2013 asti.</span><span class="sxs-lookup"><span data-stu-id="64be8-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="64be8-121">Voit vähentää asiakkaan ylläpitosopimuskuukausien määrää luomalla uuden ylläpitosopimuksen maksutapahtuman, jonka tyyppi on **Vähennyspäivät**.</span><span class="sxs-lookup"><span data-stu-id="64be8-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="64be8-122">Lisätietoja päivien vähentämisestä on kohdassa [Ylläpitosopimusmaksujen päivien vähentäminen](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="64be8-123">Ylläpitotapahtumien laskuttaminen ja jaksottaminen</span><span class="sxs-lookup"><span data-stu-id="64be8-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="64be8-124">Nyt ylläpitotapahtumien määritys on valmis ja voit laskuttaa ylläpitosopimuksen asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="64be8-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="64be8-125">Lisätietoja ylläpitotilausten laskuttamisesta on kohdassa [Ylläpitosopimustapahtumien laskuttaminen](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="64be8-126">Kaksi päivää myöhemmin asiakas soittaa ja haluaa ylläpitosopimuksen laskutettavan Yhdysvaltain dollareina eurojen sijaan.</span><span class="sxs-lookup"><span data-stu-id="64be8-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="64be8-127">Luot siksi hyvityslaskun ja sen jälkeen uuden ylläpitotapahtuman oikeassa valuutassa.</span><span class="sxs-lookup"><span data-stu-id="64be8-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="64be8-128">Lisätietoja ylläpitotilausten hyvityksistä on kohdassa [Ylläpitosopimustapahtumien hyvittäminen](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="64be8-129">Joka kuukauden lopussa jaksotat yhden kuukauden tuoton asiakkaan ylläpitosopimuksesta tulostilille ja KET-tileille.</span><span class="sxs-lookup"><span data-stu-id="64be8-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="64be8-130">Lisätietoja ylläpitosopimusten tuottojen jaksottamisesta on kohdassa [Ylläpitosopimuksen tuoton jaksotus](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="64be8-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]