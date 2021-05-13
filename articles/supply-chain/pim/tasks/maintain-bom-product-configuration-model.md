---
title: Ylläpidä tuotemääritysmallin tuoterakennetta
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921314"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="2e292-103">Ylläpidä tuotemääritysmallin tuoterakennetta</span><span class="sxs-lookup"><span data-stu-id="2e292-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e292-104">Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="2e292-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="2e292-105">Tämä menettely luodaan käyttämällä USMF-demoyrityksen Korkealaatuinen kaiutin -mallia.</span><span class="sxs-lookup"><span data-stu-id="2e292-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="2e292-106">Lisää tuoterakennerivi</span><span class="sxs-lookup"><span data-stu-id="2e292-106">Add a BOM line</span></span>

1. <span data-ttu-id="2e292-107">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="2e292-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="2e292-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2e292-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e292-109">Valitse tähän menettelyyn korkealaatuinen kaiutin.</span><span class="sxs-lookup"><span data-stu-id="2e292-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="2e292-110">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="2e292-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="2e292-111">Laajenna **Tuoterakennerivi**-osa.</span><span class="sxs-lookup"><span data-stu-id="2e292-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="2e292-112">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="2e292-112">Select **Add**.</span></span>
1. <span data-ttu-id="2e292-113">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2e292-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="2e292-114">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2e292-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="2e292-115">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2e292-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="2e292-116">Lisää tuoterakennerivin tiedot</span><span class="sxs-lookup"><span data-stu-id="2e292-116">Add BOM line details</span></span>

1. <span data-ttu-id="2e292-117">Valitse **Tuoterakennerivin tiedot**.</span><span class="sxs-lookup"><span data-stu-id="2e292-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="2e292-118">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2e292-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="2e292-119">Valitse esimerkiksi nimike M0055.</span><span class="sxs-lookup"><span data-stu-id="2e292-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="2e292-120">Voit valita kunkin tuoterakennerivin ominaisuuden kohdalla, annetaanko sille kiinteä arvo vai yhdistetäänkö se määritteeseen.</span><span class="sxs-lookup"><span data-stu-id="2e292-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="2e292-121">Valitse **Määritä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2e292-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="2e292-122">Valitse **Laskenta**-kentässä *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="2e292-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="2e292-123">**Laskelma**-ominaisuuden määrittäminen arvoksi *Kyllä* varmistaa, että tuoterakennerivi sisältyy kustannuslaskentaan.</span><span class="sxs-lookup"><span data-stu-id="2e292-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="2e292-124">Valitse **Määritys**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2e292-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="2e292-125">Valitse **Määritä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="2e292-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="2e292-126">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="2e292-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="2e292-127">Määräkenttä määrittää, miten suuri osa nimikkeestä sisällytetään tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="2e292-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="2e292-128">Tämä voisi olla hyvä ehdokas määritteen yhdistämiselle.</span><span class="sxs-lookup"><span data-stu-id="2e292-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="2e292-129">Valitse **Dimensio**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2e292-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="2e292-130">Tarkista, onko yksikään tuotedimensio aktiviinen ja onko sillä siksi oltava arvo tai määrite määritettynä.</span><span class="sxs-lookup"><span data-stu-id="2e292-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="2e292-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e292-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]