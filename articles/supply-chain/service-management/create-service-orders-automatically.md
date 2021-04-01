---
title: Huoltotilausten luominen automaattisesti
description: Voit luoda huoltotilauksia yhtä huoltosopimusta tai useita huoltosopimuksia varten.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 790c9007b4387b31e65cac650a57b873a37a70d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234846"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="2c3c0-103">Huoltotilausten luominen automaattisesti</span><span class="sxs-lookup"><span data-stu-id="2c3c0-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2c3c0-104">Voit luoda huoltotilauksia yhtä huoltosopimusta tai useita huoltosopimuksia varten.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="2c3c0-105">Kun huoltotilaukset on luotu, voit tarkastella niitä **Huoltotilaukset**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="2c3c0-106">Huoltotilauksia luodaan vain huoltosopimuksen voimassaolokaudelle.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="2c3c0-107">Jos **Luo huoltotilauksia** -lomakkeessa määritetty jakso on ennen huoltosopimuksen alkupäivämäärää tai loppupäivämäärän jälkeen, huoltotilauksia luodaan vain jaksolle, joka kuuluu huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="2c3c0-108">Kun huoltotilauksia luodaan manuaalisesti tai automaattisesti huoltosopimusriviltä, huoltotilauksen on sijoituttava alkamis- ja päättymispäivän väliselle kaudelle, ellei rivillä määritetä päättymispäivää.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="2c3c0-109">Huoltotilausten automaattinen luonti huoltosopimukseen</span><span class="sxs-lookup"><span data-stu-id="2c3c0-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="2c3c0-110">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="2c3c0-111">Valitse huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="2c3c0-112">Valitse **Toimita**-välilehti ja valitse sitten **Suunnitellut huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="2c3c0-113">Määritä huoltojakso antamalla päivämäärät **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="2c3c0-114">Valitse **Näytä infoloki** -valintaruutu, niin näyttöön tulee luotujen huoltotilausten luettelo.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="2c3c0-115">Valitse tapahtumatyypit **Sisällytä tapahtumatyypit** -kenttäryhmässä.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="2c3c0-116">Tapahtumatyypit vastaavat huoltosopimuksessa luotuja rivejä, ja kukin valittu tapahtumatyyppi luo useita huoltotilauksia sen mukaan, mikä huoltoväli huoltosopimuksen rivillä on määritetty.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="2c3c0-117">Valitse **Jatkuva**-valintaruutu, jos haluat luoda huoltotilauksia, jotka puuttuvat huoltotilausten jatkuvasta sarjasta.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="2c3c0-118">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="2c3c0-119">Huoltotilausten automaattinen luonti useisiin huoltosopimuksiin</span><span class="sxs-lookup"><span data-stu-id="2c3c0-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="2c3c0-120">Valitse **Huoltohallinta** \> **Kausittainen** \> **Huoltotilaukset** \> **Luo huoltotilauksia**</span><span class="sxs-lookup"><span data-stu-id="2c3c0-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="2c3c0-121">Napsauta **Valitse**, niin voit lisätä tai poistaa ehdot, joiden avulla luot huoltotilauksia.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="2c3c0-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c3c0-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c3c0-123">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="2c3c0-123">See also</span></span>

[<span data-ttu-id="2c3c0-124">Huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="2c3c0-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="2c3c0-125">Huoltotilausten automaattinen luonti</span><span class="sxs-lookup"><span data-stu-id="2c3c0-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]