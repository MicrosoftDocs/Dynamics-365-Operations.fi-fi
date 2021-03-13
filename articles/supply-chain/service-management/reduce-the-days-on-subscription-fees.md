---
title: Ylläpitosopimusmaksujen päivien vähentäminen
description: Jos haluat vähentää aiemmin luodun ylläpitosopimusmaksun päivien määrää, voit luoda uuden tapahtuman, jossa poistat ylläpitosopimusmaksuvälin tarpeettoman ajanjakson.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2486d08e89c06d76ab9945ccce25c5e97f1500
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010559"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="56527-103">Ylläpitosopimusmaksujen päivien vähentäminen</span><span class="sxs-lookup"><span data-stu-id="56527-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="56527-104">Jos haluat vähentää aiemmin luodun ylläpitosopimusmaksun päivien määrää, voit luoda uuden tapahtuman, jossa poistat ylläpitosopimusmaksuvälin tarpeettoman ajanjakson.</span><span class="sxs-lookup"><span data-stu-id="56527-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="56527-105">Ylläpitosopimusmaksujen päivien vähentäminen</span><span class="sxs-lookup"><span data-stu-id="56527-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="56527-106">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Kaikki huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="56527-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="56527-107">Valitse huollon ylläpitosopimus ja valitse toimintoruudussa **Ylläpitosopimusmaksut**</span><span class="sxs-lookup"><span data-stu-id="56527-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="56527-108">Valitse **Ylläpitosopimustyyppi**-kentässä **Vähennyspäivät**.</span><span class="sxs-lookup"><span data-stu-id="56527-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="56527-109">Kirjoita **Aloituspäivämäärä** - ja **Päättymispäivämäärä**-kenttiin sen ylläpitosopimusmaksun päivämääräväli, josta haluat poistaa kauden, ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="56527-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="56527-110">Voit katsella luotua tapahtumaa **Ylläpitosopimus**-lomakkeessa valitsemalla **Maksutapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="56527-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="56527-111">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="56527-111">Example</span></span>

<span data-ttu-id="56527-112">Jos ylläpitosopimustapahtuman kausi on 1.–31.1. ja haluat vähentää kautta 10 päivällä, luo uusi tapahtuma, jossa vähennyskausi on 1.–10.1.</span><span class="sxs-lookup"><span data-stu-id="56527-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="56527-113">(Vähennyskausi voi olla myös 5.–15.1 tai mikä tahansa muu kymmenen päivän jakso).</span><span class="sxs-lookup"><span data-stu-id="56527-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="56527-114">Jos vähennyskauden **Aloituspäivämäärä**-arvo on 21.1. (31 miinus 10), voit määrittää **Päättymispäivämäärä**-kentän arvoksi minkä tahansa tammikuun 31. päivän jälkeisen päivän. Tällöinkin maksutapahtuman kaudesta vähennetään 10 päivää.</span><span class="sxs-lookup"><span data-stu-id="56527-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="56527-115">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="56527-115">See also</span></span>

[<span data-ttu-id="56527-116">Esimerkki vähennyspäivistä</span><span class="sxs-lookup"><span data-stu-id="56527-116">Reduction days example</span></span>](reduction-days-example.md)

  


