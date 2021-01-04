---
title: Siirrä käyttöomaisuuserä
description: Tässä tehtäväoppaassa siirretään käyttöomaisuuskirjan taloushallinnon tiedot yhdestä taloushallinnon dimensiojoukosta uuteen taloushallinnon dimensiojoukkoon.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb38483d3ac61acb4513e87d8c36ddd0f8863a10
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442781"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="f224b-103">Siirrä käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="f224b-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f224b-104">Tässä tehtäväoppaassa siirretään käyttöomaisuuskirjan taloushallinnon tiedot yhdestä taloushallinnon dimensiojoukosta uuteen taloushallinnon dimensiojoukkoon.</span><span class="sxs-lookup"><span data-stu-id="f224b-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="f224b-105">Siinä käytetään kirjanpitäjän roolia ja USMF-yrityksen esittelytietoja.</span><span class="sxs-lookup"><span data-stu-id="f224b-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="f224b-106">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Käyttöomaisuuserät > Käyttöomaisuuserät**.</span><span class="sxs-lookup"><span data-stu-id="f224b-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="f224b-107">Etsi ja valitse luettelosta siirrettävä käyttöomaisuus.</span><span class="sxs-lookup"><span data-stu-id="f224b-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="f224b-108">Valitse toimintoruudussa **Käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="f224b-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="f224b-109">Valitse **Siirrä käyttöomaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="f224b-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="f224b-110">Kirjoita päivämäärä **Siirtopäivä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f224b-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="f224b-111">Syötä siirtoa kuvaavia kommentteja.</span><span class="sxs-lookup"><span data-stu-id="f224b-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="f224b-112">Tässä luettelossa on kaikki käyttöomaisuuden kirjat.</span><span class="sxs-lookup"><span data-stu-id="f224b-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="f224b-113">Merkitse uuteen taloushallinnon dimensioon siirrettävät kirjat.</span><span class="sxs-lookup"><span data-stu-id="f224b-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="f224b-114">Tässä luettelossa on valitun kirjan aiemmin luodut taloushallinnon dimensioiden arvot.</span><span class="sxs-lookup"><span data-stu-id="f224b-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="f224b-115">Valitse valitun käyttöomaisuuskirjan päivitettävä taloushallinnon dimensio.</span><span class="sxs-lookup"><span data-stu-id="f224b-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="f224b-116">Avaa haku valitsemalla **Taloushallinnon dimensio** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="f224b-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="f224b-117">Määritä tarvittaessa muut taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="f224b-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="f224b-118">Kaikki taloushallinnon dimension arvot muuttuvat siirron yhteydessä siitä huolimatta, onko arvo syötetty vai onko kohta jätetty tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="f224b-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="f224b-119">Ajatellaan, että syötit arvon BusinessUnit-kohteelle, mutta jätit CostCenter- ja Department-kohteen taloushallinnon dimensiot tyhjiksi.</span><span class="sxs-lookup"><span data-stu-id="f224b-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="f224b-120">Jos tilirakenne sallii CostCenter-kohteen ja Department-kohteen tyhjät arvot, siirron yhteydessä jokainen BusinessUnit-kohteen arvomalli saa uuden arvon. CostCenter ja Department jäävät tyhjiksi.</span><span class="sxs-lookup"><span data-stu-id="f224b-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="f224b-121">Valitse **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="f224b-121">Click **Update**.</span></span>
    * <span data-ttu-id="f224b-122">Voit esikatsella muutoksia ennen siirron tekemistä.</span><span class="sxs-lookup"><span data-stu-id="f224b-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="f224b-123">Tarkastele tuloksia, ennen kuin siirrät käyttöomaisuuskirjat.</span><span class="sxs-lookup"><span data-stu-id="f224b-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="f224b-124">Valitse **Siirrä**.</span><span class="sxs-lookup"><span data-stu-id="f224b-124">Click **Transfer**.</span></span>

