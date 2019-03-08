---
title: Palautusten pakkausluettelopäivitykset
description: Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aba61e6acf5fb959917da9ddea94c21fe1460d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "344866"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="83deb-103">Palautusten pakkausluettelopäivitykset</span><span class="sxs-lookup"><span data-stu-id="83deb-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="83deb-104">Ennen kuin palautetut nimikkeet voidaan vastaanottaa varastoon, sen tilauksen pakkausluettelo, johon palautetut nimikkeet kuuluvat, on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="83deb-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="83deb-105">Samalla tavoin kuin laskun päivitysprosessi kirjanpitotapahtumaksi pakkausluettelon päivitysprosessi on varastotietueen fyysinen päivitys eli se vahvistaa muutokset varastoon.</span><span class="sxs-lookup"><span data-stu-id="83deb-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="83deb-106">Kun kyseessä on palautus, käsittelytoimenpiteen vaiheet toteutetaan pakkausluettelon päivityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="83deb-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="83deb-107">Pakkausluettelon päivitys voidaan käsitellä joko nimikkeen saapumisen kirjauskansiossa tai palautustilauksessa.</span><span class="sxs-lookup"><span data-stu-id="83deb-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="83deb-108">Pakkausluetteloiden kirjaamisprosessin osana on mahdollista liittää pakkausluettelon viitenumero asiakkaan toimitusasiakirjoista tilausriveille.</span><span class="sxs-lookup"><span data-stu-id="83deb-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="83deb-109">Tämä liitos on valinnainen ja se on tarkoitettu vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="83deb-109">This association is optional and for reference only.</span></span> <span data-ttu-id="83deb-110">Se ei luo mitään tapahtumaan liittyviä päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="83deb-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="83deb-111">Jos kaikki odotetut palautetut nimikkeet eivät ole vielä saapuneet, sisällytä vain vastaanotettu määrä pakkausluettelon päivitykseen.</span><span class="sxs-lookup"><span data-stu-id="83deb-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="83deb-112">Puuttuvat nimikkeet jätetään tilaukseen siihen saakka, kunnes loput palautuksesta on saapunut.</span><span class="sxs-lookup"><span data-stu-id="83deb-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="83deb-113">Pakkausluettelo on päivitettävä, jos nimike lähetetään takaisin karanteenista lähetys- ja vastaanotto-osastolle esimerkiksi tilanteessa, jossa karanteenitarkastaja ei tiedä, mihin nimike varastoidaan. Näin voidaan varmistaa oikeanlainen rekisteröinti sekä karanteenin tuloksena määritettyyn käsittelykoodiin liittyvä toimenpide.</span><span class="sxs-lookup"><span data-stu-id="83deb-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="83deb-114">Kun päivität myyntisopimukseen kuuluvan palautetun nimikkeen pakkausluettelon, kyseisen nimikkeen myyntisopimuksen sitoumus päivitetään automaattisesti määrän tai summan muutoksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="83deb-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="83deb-115">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="83deb-115">See also</span></span>

[<span data-ttu-id="83deb-116">Laskun päivitysten suorittaminen palautuksille</span><span class="sxs-lookup"><span data-stu-id="83deb-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


