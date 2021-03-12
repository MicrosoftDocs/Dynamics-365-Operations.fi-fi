---
title: Tuotteen konfigurointimallin hyväksyntä
description: Tämän menettelyn suorittaminen edellyttää, että ainakin yksi tuotemääritysmalli on käytettävissä.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b548e2369f30e998ecde45408ff45893b88f9a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987101"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="06145-103">Tuotteen konfigurointimallin hyväksyntä</span><span class="sxs-lookup"><span data-stu-id="06145-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06145-104">Tämän menettelyn suorittaminen edellyttää, että ainakin yksi tuotemääritysmalli on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="06145-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="06145-105">Tämä menettely käyttää USMF-yrityksen demotietojen korkealaatuista kaiutinmallia.</span><span class="sxs-lookup"><span data-stu-id="06145-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="06145-106">Huomaa, että tämä malli on jo hyväksytty, mutta menettely selittää koko prosessin.</span><span class="sxs-lookup"><span data-stu-id="06145-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="06145-107">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="06145-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="06145-108">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="06145-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="06145-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="06145-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="06145-110">Valitse tähän menettelyyn Korkealaatuinen kaiutinmalli.</span><span class="sxs-lookup"><span data-stu-id="06145-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="06145-111">Valitse Versiot.</span><span class="sxs-lookup"><span data-stu-id="06145-111">Click Versions.</span></span>
5. <span data-ttu-id="06145-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="06145-112">Click New.</span></span>
6. <span data-ttu-id="06145-113">Anna tai valitse Tuotenumero -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="06145-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="06145-114">Tuotteen viite vastaa tuotemääritysmallin versiota.</span><span class="sxs-lookup"><span data-stu-id="06145-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="06145-115">Tässä luettelossa on vain poissulkevaa konfigurointitekniikkaa sisältävät päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="06145-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="06145-116">Syötä päivämäärä Päivämäärästä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="06145-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="06145-117">Valitse, milloin tuotemalliversio on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="06145-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="06145-118">Kirjoita päivämäärä Päivämäärään-kenttään.</span><span class="sxs-lookup"><span data-stu-id="06145-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="06145-119">Valitse päättymispäivä, jolloin tuotemalliversio vanhenee, tai valitse Ei koskaan.</span><span class="sxs-lookup"><span data-stu-id="06145-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="06145-120">Avaa valintaikkuna valitsemalla Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="06145-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="06145-121">Anna tai valitse Hyväksyjä-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="06145-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="06145-122">Valitse henkilö, joka vastaa työvaiheissa käytettävien tuotemallien hyväksymisestä.</span><span class="sxs-lookup"><span data-stu-id="06145-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="06145-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="06145-123">Click OK.</span></span>
12. <span data-ttu-id="06145-124">Valitse Hinnoittelumenetelmä-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="06145-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="06145-125">Aktivoi tuotemalliversio.</span><span class="sxs-lookup"><span data-stu-id="06145-125">Activate the product model version.</span></span> <span data-ttu-id="06145-126">Samanaikaisesti vain yksi tuotemallin tuote voi olla aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="06145-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="06145-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="06145-127">Close the page.</span></span>

