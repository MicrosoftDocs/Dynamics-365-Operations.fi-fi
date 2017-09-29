---
title: "Ehdollisen päätöksen konfiguroiminen työnkulkuun"
description: "Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: e9d5c8add546cad0446e863f64cac8f9cb603cbb
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="44d80-103">Ehdollisen päätöksen konfiguroiminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="44d80-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="44d80-104">Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="44d80-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="44d80-105">Ehdollista valintaa voidaan edellyttää, kun työnkulku jakautuu kahteen haaraan.</span><span class="sxs-lookup"><span data-stu-id="44d80-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="44d80-106">Ehdollinen päätös konfiguroidaan työnkulkueditorissa napsauttamalla ehdollista päätöstä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="44d80-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="44d80-107">Nimeä päätös</span><span class="sxs-lookup"><span data-stu-id="44d80-107">Name a decision</span></span>
<span data-ttu-id="44d80-108">Kirjoita näiden ohjeiden avulla nimi ehdolliselle päätökselle.</span><span class="sxs-lookup"><span data-stu-id="44d80-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="44d80-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="44d80-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="44d80-110">Kirjoita ehdollisen päätöksen yksilöivä nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="44d80-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="44d80-111"> Ehtojen asetus</span><span class="sxs-lookup"><span data-stu-id="44d80-111">Set conditions</span></span>
<span data-ttu-id="44d80-112">Järjestelmä päättää käytettävän haaran arvioimalla, täyttääkö lähetetty asiakirja erityisehdot.</span><span class="sxs-lookup"><span data-stu-id="44d80-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="44d80-113">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="44d80-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="44d80-114">Valitse **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="44d80-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="44d80-115">Määritä ehto.</span><span class="sxs-lookup"><span data-stu-id="44d80-115">Enter a condition.</span></span>
4.  <span data-ttu-id="44d80-116">Kirjoita kaikki muut tarvittavat ehdot.</span><span class="sxs-lookup"><span data-stu-id="44d80-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="44d80-117">Voit tarkistaa, onko ehdot määritetty oikein käymällä läpi seuraavat ohjeet:</span><span class="sxs-lookup"><span data-stu-id="44d80-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="44d80-118">Valitse **Testi**, jolloin **Testaa työnkulun ehto** -lomake tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="44d80-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="44d80-119">Valitse tietue lomakkeen **Tarkista ehto** -alueelta.</span><span class="sxs-lookup"><span data-stu-id="44d80-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="44d80-120">Valitse **Testi**.</span><span class="sxs-lookup"><span data-stu-id="44d80-120">Click **Test**.</span></span> <span data-ttu-id="44d80-121">Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.</span><span class="sxs-lookup"><span data-stu-id="44d80-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="44d80-122">Palaa **Ominaisuudet**-lomakkeeseen valitsemalla **OK** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="44d80-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






