---
title: Tuotteen konfigurointimallin hyväksyntä
description: Tämän menettelyn suorittaminen edellyttää, että ainakin yksi tuotemääritysmalli on käytettävissä.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920504"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="30607-103">Tuotteen konfigurointimallin hyväksyntä</span><span class="sxs-lookup"><span data-stu-id="30607-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30607-104">Tämän menettelyn suorittaminen edellyttää, että ainakin yksi tuotemääritysmalli on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="30607-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="30607-105">Tämä menettely käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia.</span><span class="sxs-lookup"><span data-stu-id="30607-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="30607-106">Huomaa, että tämä malli on jo hyväksytty, mutta menettely selittää koko prosessin.</span><span class="sxs-lookup"><span data-stu-id="30607-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="30607-107">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="30607-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="30607-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="30607-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="30607-109">Valitse tähän menettelyyn Korkealaatuinen kaiutinmalli.</span><span class="sxs-lookup"><span data-stu-id="30607-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="30607-110">Valitse **Versiot**.</span><span class="sxs-lookup"><span data-stu-id="30607-110">Select **Versions**.</span></span>
1. <span data-ttu-id="30607-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="30607-111">Select **New**.</span></span>
1. <span data-ttu-id="30607-112">Anna tai valitse **Tuotenumero**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="30607-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="30607-113">Tuotteen viite vastaa tuotemääritysmallin versiota.</span><span class="sxs-lookup"><span data-stu-id="30607-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="30607-114">Tässä luettelossa on vain poissulkevaa konfigurointitekniikkaa sisältävät päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="30607-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="30607-115">Syötä päivämäärä **Päivämäärästä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="30607-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="30607-116">Valitse, milloin tuotemalliversio on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="30607-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="30607-117">Kirjoita päivämäärä **Päivämäärään**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="30607-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="30607-118">Valitse päättymispäivä, jolloin tuotemalliversio vanhenee, tai valitse Ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="30607-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="30607-119">Avaa valintaikkuna valitsemalla **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="30607-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="30607-120">Anna tai valitse **Hyväksyjä**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="30607-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="30607-121">Valitse henkilö, joka vastaa työvaiheissa käytettävien tuotemallien hyväksymisestä.</span><span class="sxs-lookup"><span data-stu-id="30607-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="30607-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="30607-122">Select **OK**.</span></span>
1. <span data-ttu-id="30607-123">Valitse **Hinnoittelumenetelmä**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="30607-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="30607-124">Aktivoi tuotemalliversio.</span><span class="sxs-lookup"><span data-stu-id="30607-124">Activate the product model version.</span></span> <span data-ttu-id="30607-125">Samanaikaisesti vain yksi tuotemallin tuote voi olla aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="30607-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="30607-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="30607-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]