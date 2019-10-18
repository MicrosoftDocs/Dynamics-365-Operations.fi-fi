---
title: Ehdollisten päätösten konfiguroiminen työnkulkuun
description: Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 278773a5ad8be35f9b6dcd1ec0d0a35e32222bb1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177629"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="9023e-103">Ehdollisten päätösten konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="9023e-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9023e-104">Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="9023e-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="9023e-105">Ehdollista valintaa voidaan edellyttää, kun työnkulku jakautuu kahteen haaraan.</span><span class="sxs-lookup"><span data-stu-id="9023e-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="9023e-106">Ehdollinen päätös konfiguroidaan työnkulkueditorissa napsauttamalla ehdollista päätöstä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="9023e-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="9023e-107">Nimeä päätös</span><span class="sxs-lookup"><span data-stu-id="9023e-107">Name a decision</span></span>

<span data-ttu-id="9023e-108">Kirjoita näiden ohjeiden avulla nimi ehdolliselle päätökselle.</span><span class="sxs-lookup"><span data-stu-id="9023e-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="9023e-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="9023e-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="9023e-110">Kirjoita ehdollisen päätöksen yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9023e-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="9023e-111"> Ehtojen asetus</span><span class="sxs-lookup"><span data-stu-id="9023e-111">Set conditions</span></span>

<span data-ttu-id="9023e-112">Järjestelmä päättää käytettävän haaran arvioimalla, täyttääkö lähetetty asiakirja erityisehdot.</span><span class="sxs-lookup"><span data-stu-id="9023e-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="9023e-113">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="9023e-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="9023e-114">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="9023e-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="9023e-115">Määritä ehto.</span><span class="sxs-lookup"><span data-stu-id="9023e-115">Enter a condition.</span></span>
4. <span data-ttu-id="9023e-116">Kirjoita kaikki muut tarvittavat ehdot.</span><span class="sxs-lookup"><span data-stu-id="9023e-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="9023e-117">Voit tarkistaa, onko ehdot määritetty oikein käymällä läpi seuraavat ohjeet:</span><span class="sxs-lookup"><span data-stu-id="9023e-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="9023e-118">Valitse **Testi**, jolloin **Testaa työnkulun ehto** -lomake tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="9023e-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="9023e-119">Valitse tietue lomakkeen **Tarkista ehto** -alueelta.</span><span class="sxs-lookup"><span data-stu-id="9023e-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="9023e-120">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="9023e-120">Click **Test**.</span></span> <span data-ttu-id="9023e-121">Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.</span><span class="sxs-lookup"><span data-stu-id="9023e-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="9023e-122">Palaa **Ominaisuudet**-lomakkeeseen valitsemalla **OK** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="9023e-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>
