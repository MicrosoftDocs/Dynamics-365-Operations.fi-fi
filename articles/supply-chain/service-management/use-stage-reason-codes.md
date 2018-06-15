---
title: "Käytä jaksosyykoodeja"
description: "Käytä syykoodia osoittamaan, miksi huoltotasosopimus on peruutettu tai miksi huoltotasosopimuksessa asetettu huoltosopimuksen aikaraja on ylitetty."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e42172fe1b484b91e9a3e3d05d438e7e9b0b0eb4
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---


# <a name="use-stage-reason-codes"></a><span data-ttu-id="18011-103">Käytä jaksosyykoodeja</span><span class="sxs-lookup"><span data-stu-id="18011-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="18011-104">Käytä syykoodia osoittamaan, miksi huoltotasosopimus on peruutettu tai miksi huoltotasosopimuksessa asetettu huoltosopimuksen aikaraja on ylitetty.</span><span class="sxs-lookup"><span data-stu-id="18011-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="18011-105">Voit myös määrittää syykoodin pakolliseksi, kun huoltotasospimus peruutetaan tai kun huoltotasosopimuksessa asetettu huoltosopimuksen aikaraja ylitetään.</span><span class="sxs-lookup"><span data-stu-id="18011-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="18011-106">Jos olet määrittänyt syykoodin pakolliseksi, syykoodi on annettava seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="18011-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="18011-107">kun huoltotilaus siirretään tasolle, jossa huoltotilauksen huoltotasosopimuksen ajan tallennus lopetetaan</span><span class="sxs-lookup"><span data-stu-id="18011-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="18011-108">kun huoltotilaus hyväksytään</span><span class="sxs-lookup"><span data-stu-id="18011-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="18011-109">kun ajan tallennus lopetetaan manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="18011-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="18011-110">Määritä syykoodit</span><span class="sxs-lookup"><span data-stu-id="18011-110">Set up reason codes</span></span>

1.  <span data-ttu-id="18011-111">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Vaiheen syykoodit**.</span><span class="sxs-lookup"><span data-stu-id="18011-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="18011-112">Luo uusi syykoodi **Vaiheen syykoodit** -lomakkeella napsauttamalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="18011-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="18011-113">Anna **Vaiheen syykoodi** -kentässä yksilöivä vaiheen syykoodi.</span><span class="sxs-lookup"><span data-stu-id="18011-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="18011-114">Anna **Kuvaus**-kentässä vaiheen syykoodin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="18011-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="18011-115">Tallenna muutokset sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="18011-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="18011-116">Syykoodien vaatiminen, kun huoltotasosopimus peruutetaan</span><span class="sxs-lookup"><span data-stu-id="18011-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="18011-117">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltohallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="18011-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="18011-118">Napsauta **Huollon hallinnan parametrit** -lomakkeessa **Yleiset**-linkkiä ja valitse sitten **Syykoodi peruutettaessa** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="18011-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="18011-119">Syykoodien vaatiminen, kun huoltotasosopimuksen asettama huoltosopimuksen aikaraja ylitetään</span><span class="sxs-lookup"><span data-stu-id="18011-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="18011-120">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltohallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="18011-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="18011-121">Napsauta **Huollon hallinnan parametrit** -lomakkeessa **Yleiset**-linkkiä ja valitse sitten **Syykoodi ajan ylittyessä** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="18011-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="18011-122">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="18011-122">See also</span></span>

[<span data-ttu-id="18011-123">Huoltotilauksen ajanseurannan aloittaminen ja pysäyttäminen</span><span class="sxs-lookup"><span data-stu-id="18011-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


