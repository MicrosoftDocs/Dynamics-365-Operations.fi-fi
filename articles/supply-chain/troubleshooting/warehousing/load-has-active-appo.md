---
title: Lähetystä ei voi vahvistaa kalenterin ongelman vuoksi
description: Lähetystä ei voi vahvistaa kalenterin ongelman vuoksi
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938464"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="432ce-103">Lähetystä ei voi vahvistaa kalenterin ongelman vuoksi</span><span class="sxs-lookup"><span data-stu-id="432ce-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="432ce-104">Virhekoodi: TRX2716</span><span class="sxs-lookup"><span data-stu-id="432ce-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="432ce-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="432ce-105">Symptoms</span></span>

<span data-ttu-id="432ce-106">Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="432ce-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="432ce-107">Kalenterityyppi %1 edellyttää tapaamisen %2 sisään- ja uloskuittausta.</span><span class="sxs-lookup"><span data-stu-id="432ce-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="432ce-108">Et siis voi vahvistaa lähetystä kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="432ce-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="432ce-109">Syy</span><span class="sxs-lookup"><span data-stu-id="432ce-109">Cause</span></span>

<span data-ttu-id="432ce-110">Kuormitusta varten on aktiivisia tapaamisia.</span><span class="sxs-lookup"><span data-stu-id="432ce-110">Active appointments for the load exist.</span></span> <span data-ttu-id="432ce-111">On esimerkiksi sääntö, joka edellyttää kuljettajan sisäänkuittausta.</span><span class="sxs-lookup"><span data-stu-id="432ce-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="432ce-112">Näin ollen kuorma on tilassa, jossa lähetysvahvistus epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="432ce-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="432ce-113">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="432ce-113">Resolution</span></span>

<span data-ttu-id="432ce-114">Kuormitukseen linkitettyihin aktiivisisiin tapaamisiin liittyvät ongelmat on selvitettävä ja korjattava.</span><span class="sxs-lookup"><span data-stu-id="432ce-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="432ce-115">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="432ce-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="432ce-116">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="432ce-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="432ce-117">Valitse sitten toimintoruudussa **Kuljetus**-välilehden **Tapaamiset**-ryhmässä **Tapaamisen ajoittaminen**.</span><span class="sxs-lookup"><span data-stu-id="432ce-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="432ce-118">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="432ce-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="432ce-119">Varmista, että kuljettajan sisään- tai uloskuittaus on valmis.</span><span class="sxs-lookup"><span data-stu-id="432ce-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="432ce-120">Tee tapaaminen valmiiksi tai peruuta se.</span><span class="sxs-lookup"><span data-stu-id="432ce-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="432ce-121">Poista liittyvän tapaamissäännön **Kuljettajan sisäänkuittaus tarvitaan** -vaihtoehto käytöstä.</span><span class="sxs-lookup"><span data-stu-id="432ce-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
