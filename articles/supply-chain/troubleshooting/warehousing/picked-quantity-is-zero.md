---
title: Et voi vahvistaa lähetystä, koska määrä on nolla.
description: Et voi vahvistaa lähetystä, koska määrä on nolla.
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938461"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="f5d92-103">Et voi vahvistaa lähetystä, koska määrä on nolla.</span><span class="sxs-lookup"><span data-stu-id="f5d92-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="f5d92-104">Virhekoodi: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="f5d92-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="f5d92-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="f5d92-105">Symptoms</span></span>

<span data-ttu-id="f5d92-106">Kun yrität vahvistaa lähetyksen, järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="f5d92-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f5d92-107">Nimikkeen %1 ja lähetyksen %2 kuormariville on päivitetty nollamäärä, koska alitoimituksen asetukset sallivat, ettei tämän nimikkeen määriä lähetetä.</span><span class="sxs-lookup"><span data-stu-id="f5d92-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="f5d92-108">Et siis voi vahvistaa lähetystä kuormaa varten.</span><span class="sxs-lookup"><span data-stu-id="f5d92-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f5d92-109">Syy</span><span class="sxs-lookup"><span data-stu-id="f5d92-109">Cause</span></span>

<span data-ttu-id="f5d92-110">Järjestelmä arvioi, onko kerätty määrä odotettujen rajojen sisällä kerätyn määrän, kuormitusrivin määrän ja alitoimitusprosentin perusteella.</span><span class="sxs-lookup"><span data-stu-id="f5d92-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="f5d92-111">Jos järjestelmä havaitsee, että kerätty määrä kuormitusrivillä on 0 (nolla), lähetystä ei voi vahvistaa.</span><span class="sxs-lookup"><span data-stu-id="f5d92-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="f5d92-112">Tämä ongelma voi ilmetä esimerkiksi, jos työ on peruutettu ja kuormitusrivin alitoimitusprosentti on 100 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="f5d92-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="f5d92-113">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="f5d92-113">Resolution</span></span>

<span data-ttu-id="f5d92-114">Tarkista kuormitusrivit ja varmista, että alitoimitusprosentti ja määrät ovat suhteessa kerättyyn työhön.</span><span class="sxs-lookup"><span data-stu-id="f5d92-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="f5d92-115">Siirry kohtaan **Varastonhallinta \> Kuormat \> Kaikki kuormat**.</span><span class="sxs-lookup"><span data-stu-id="f5d92-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f5d92-116">Valitse kuormitus, jolle ei voi vahvistaa lähetystä.</span><span class="sxs-lookup"><span data-stu-id="f5d92-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f5d92-117">Valitse **Kuormitusrivit**-pikavälilehdessä nimikkeelle kuormitusrivi, joka ylittää alitoimitusprosentin.</span><span class="sxs-lookup"><span data-stu-id="f5d92-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="f5d92-118">Muuta tarvittaessa **Alitoimitus**-kentän tai **Määrä**-kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="f5d92-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="f5d92-119">Jos ongelmaa ei ole vielä korjattu, liittyvien myyntitilausten tai siirtotilausten keräystöitä on ehkä vielä jatkettava, kunnes käytettävissä oleva määrä on kohdistettu kuormituksen tai lähetyksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="f5d92-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
