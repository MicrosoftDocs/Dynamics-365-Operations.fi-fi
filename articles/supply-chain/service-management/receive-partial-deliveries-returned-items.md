---
title: Palautettujen nimikkeiden osittaisten toimitusten vastaanottaminen
description: "Osatoimitukset määritetään palautustilausrivien, ei palautustilauslähetyksen mukaan."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f9f596d31f2438a353b02bf939786b284937db86
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="04dbd-103">Palautettujen nimikkeiden osittaisten toimitusten vastaanottaminen</span><span class="sxs-lookup"><span data-stu-id="04dbd-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="04dbd-104">Osatoimitukset määritetään palautustilausrivien, ei palautustilauslähetyksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="04dbd-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="04dbd-105">Se tarkoittaa sitä, että jos vastaanotat yhdellä palautustilausrivillä osoitetun koko määrän, mutta et vastaanota mitään muilla palautustilausriveillä osoitettuja määriä, toimitus ei ole osatoimitus.</span><span class="sxs-lookup"><span data-stu-id="04dbd-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="04dbd-106">Jos kuitenkin palautustilausrivi edellyttää palautettavaksi tietyn nimikkeen kymmentä yksikköä ja vastaanotat vain neljä, kyseessä on osatoimitus.</span><span class="sxs-lookup"><span data-stu-id="04dbd-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="04dbd-107">Jos palautuslähetyksen määrä on pienempi kuin palautustilausrivin koko määrä, voit siirtää lähetyksen sivuun ja odottaa määrän loppuosan saapumista. Vaihtoehtoisesti voit rekisteröidä osittaisen määrän ja kirjata sen.</span><span class="sxs-lookup"><span data-stu-id="04dbd-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="04dbd-108">Osatoimituksen rekisteröiminen ja kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="04dbd-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="04dbd-109">Kun olet valinnut palautustilauksen saapuvaksi **Saapumisten yhteenveto - Varasto: %1, Laituri: %2, Kirjauskansion nimi: %3** -lomakkeessa, napsauta **Aloita saapuminen** luodaksesi saapumisen kirjauskansion, ja napsauta sitten **Kirjauskansiot** \> **Näytä vastaanottojen saapumiset** avataksesi **Sijainnin kirjauskansio** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="04dbd-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="04dbd-110">Valitse kirjauskansion rivi, jota haluat käsitellä. Napsauta sitten **Rivit** avataksesi **Kirjauskansion rivit, sijainnit** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="04dbd-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="04dbd-111">Valitse sen nimiketunnuksen rivi, jolle saapui vain osa määrästä. Napsauta sitten **Toiminnot** \> **Jako** avataksesi **Jako**-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="04dbd-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="04dbd-112">Kirjoita **Jaettava määrä** -kenttään vastaanotettujen nimikkeiden kokonaismäärä. Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="04dbd-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="04dbd-113">Valitse **Kirjauskansion rivit, sijainnit**  -lomakkeessa määrän vastaanottaneen nimikkeen rivi. Valitse sitten **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="04dbd-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="04dbd-114">Voit kirjata lisämäärän rivin nimikkeiden saapumisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="04dbd-114">You can post the line for the additional quantity after the items have arrived.</span></span>




