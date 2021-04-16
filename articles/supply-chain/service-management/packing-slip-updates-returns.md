---
title: Palautusten pakkausluettelopäivitykset
description: Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9b5c7e5726c36aa963e5750c63df20c1e2e6c35
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810699"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="52a8e-103">Palautusten pakkausluettelopäivitykset</span><span class="sxs-lookup"><span data-stu-id="52a8e-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="52a8e-104">Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="52a8e-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="52a8e-105">Samalla tavoin kuin laskun päivitysprosessi kirjanpitotapahtumaksi pakkausluettelon päivitysprosessi on varastotietueen fyysinen päivitys eli se vahvistaa muutokset varastoon.</span><span class="sxs-lookup"><span data-stu-id="52a8e-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="52a8e-106">Kun kyseessä on palautus, käsittelytoimenpiteen vaiheet toteutetaan pakkausluettelon päivityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="52a8e-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="52a8e-107">Pakkausluettelon päivitys voidaan käsitellä joko nimikkeen saapumisen kirjauskansiossa tai palautustilauksessa.</span><span class="sxs-lookup"><span data-stu-id="52a8e-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="52a8e-108">Pakkausluetteloiden kirjaamisprosessin osana on mahdollista liittää pakkausluettelon viitenumero asiakkaan toimitusasiakirjoista tilausriveille.</span><span class="sxs-lookup"><span data-stu-id="52a8e-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="52a8e-109">Tämä liitos on valinnainen ja se on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="52a8e-109">This association is optional and for reference only.</span></span> <span data-ttu-id="52a8e-110">Se ei luo mitään tapahtumaan liittyviä päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="52a8e-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="52a8e-111">Jos kaikki odotetut palautetut nimikkeet eivät ole vielä saapuneet, sisällytä vain vastaanotettu määrä pakkausluettelon päivitykseen.</span><span class="sxs-lookup"><span data-stu-id="52a8e-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="52a8e-112">Puuttuvat nimikkeet jätetään tilaukseen siihen saakka, kunnes loput palautuksesta on saapunut.</span><span class="sxs-lookup"><span data-stu-id="52a8e-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="52a8e-113">Pakkausluettelo on päivitettävä, jos nimike lähetetään takaisin karanteenista lähetys- ja vastaanotto-osastolle esimerkiksi tilanteessa, jossa karanteenitarkastaja ei tiedä, mihin nimike varastoidaan. Näin voidaan varmistaa oikeanlainen rekisteröinti sekä karanteenin tuloksena määritettyyn käsittelykoodiin liittyvä toimenpide.</span><span class="sxs-lookup"><span data-stu-id="52a8e-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="52a8e-114">Kun päivität myyntisopimukseen kuuluvan palautetun nimikkeen pakkausluettelon, kyseisen nimikkeen myyntisopimuksen sitoumus päivitetään automaattisesti määrän tai summan muutoksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="52a8e-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="52a8e-115">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="52a8e-115">See also</span></span>

[<span data-ttu-id="52a8e-116">Laskun päivitysten suorittaminen palautuksille</span><span class="sxs-lookup"><span data-stu-id="52a8e-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]