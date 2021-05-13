---
title: Luo dimensioihin perustuvat konfiguraatiot
description: Seuraavassa kuvataan konfiguraation määrittäminen dimensioperustaiselle tuotteelle.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920678"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="231ed-103">Luo dimensioihin perustuvat konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="231ed-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="231ed-104">Seuraavassa kuvataan konfiguraation määrittäminen dimensioperustaiselle tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="231ed-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="231ed-105">Tämä on viimeinen kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan.</span><span class="sxs-lookup"><span data-stu-id="231ed-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="231ed-106">Tämän menettelyn suorittaminen on riippuvainen seitsemässä edellisessä osassa luoduista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="231ed-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="231ed-107">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="231ed-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="231ed-108">Paikanna dimensioihin perustuva päätuote</span><span class="sxs-lookup"><span data-stu-id="231ed-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="231ed-109">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="231ed-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="231ed-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="231ed-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="231ed-111">Valitse tämän kahdeksanosaisen tallennesarjan ensimmäisessä osassa luomasi dimensioperustainen päätuote.</span><span class="sxs-lookup"><span data-stu-id="231ed-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="231ed-112">Konfiguraatioiden luonti</span><span class="sxs-lookup"><span data-stu-id="231ed-112">Create configurations</span></span>

1. <span data-ttu-id="231ed-113">Valitse **Suunnittelu**-toimintoruudussa **Ylläpidä konfigurointeja**.</span><span class="sxs-lookup"><span data-stu-id="231ed-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="231ed-114">Valitse **Konfiguroi**.</span><span class="sxs-lookup"><span data-stu-id="231ed-114">Select **Configure**.</span></span>
1. <span data-ttu-id="231ed-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="231ed-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="231ed-116">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="231ed-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="231ed-117">Valitse nimikkeet ensimmäisestä konfiguraatioryhmästä.</span><span class="sxs-lookup"><span data-stu-id="231ed-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="231ed-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="231ed-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="231ed-119">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="231ed-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="231ed-120">Valitse nimike toisesta konfiguraatioryhmästä.</span><span class="sxs-lookup"><span data-stu-id="231ed-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="231ed-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="231ed-121">Select **OK**.</span></span>
1. <span data-ttu-id="231ed-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="231ed-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="231ed-123">Syötä arvo **Konfiguraatio**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="231ed-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="231ed-124">Määritä konfiguroinnin nimi, jonka avulla se on helppo tunnistaa.</span><span class="sxs-lookup"><span data-stu-id="231ed-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="231ed-125">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="231ed-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="231ed-126">Kirjoita konfiguraatiolle sen sisällön selittävä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="231ed-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="231ed-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="231ed-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]