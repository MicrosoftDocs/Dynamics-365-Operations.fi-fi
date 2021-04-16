---
title: Ehdollisten päätösten konfiguroiminen työnkulkuun
description: Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed53eeb26e1b4b1df1647739ce1d115c7dd169f8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747928"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="7929c-103">Ehdollisten päätösten konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="7929c-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7929c-104">Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="7929c-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="7929c-105">Ehdollista valintaa voidaan edellyttää, kun työnkulku jakautuu kahteen haaraan.</span><span class="sxs-lookup"><span data-stu-id="7929c-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="7929c-106">Ehdollinen päätös konfiguroidaan työnkulkueditorissa napsauttamalla ehdollista päätöstä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="7929c-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="7929c-107">Nimeä päätös</span><span class="sxs-lookup"><span data-stu-id="7929c-107">Name a decision</span></span>

<span data-ttu-id="7929c-108">Kirjoita näiden ohjeiden avulla nimi ehdolliselle päätökselle.</span><span class="sxs-lookup"><span data-stu-id="7929c-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="7929c-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="7929c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="7929c-110">Kirjoita ehdollisen päätöksen yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7929c-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="7929c-111"> Ehtojen asetus</span><span class="sxs-lookup"><span data-stu-id="7929c-111">Set conditions</span></span>

<span data-ttu-id="7929c-112">Järjestelmä päättää käytettävän haaran arvioimalla, täyttääkö lähetetty asiakirja erityisehdot.</span><span class="sxs-lookup"><span data-stu-id="7929c-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="7929c-113">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="7929c-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="7929c-114">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="7929c-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="7929c-115">Määritä ehto.</span><span class="sxs-lookup"><span data-stu-id="7929c-115">Enter a condition.</span></span>
4. <span data-ttu-id="7929c-116">Kirjoita kaikki muut tarvittavat ehdot.</span><span class="sxs-lookup"><span data-stu-id="7929c-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="7929c-117">Voit tarkistaa, onko ehdot määritetty oikein käymällä läpi seuraavat ohjeet:</span><span class="sxs-lookup"><span data-stu-id="7929c-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="7929c-118">Valitse **Testi**, jolloin **Testaa työnkulun ehto** -lomake tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="7929c-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="7929c-119">Valitse tietue lomakkeen **Tarkista ehto** -alueelta.</span><span class="sxs-lookup"><span data-stu-id="7929c-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="7929c-120">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="7929c-120">Click **Test**.</span></span> <span data-ttu-id="7929c-121">Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.</span><span class="sxs-lookup"><span data-stu-id="7929c-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="7929c-122">Palaa **Ominaisuudet**-lomakkeeseen valitsemalla **OK** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="7929c-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]