---
title: Palautettujen nimikkeiden vastaanottaminen tarkastuksen kautta
description: Palautettujen nimikkeiden vastaanottaminen tarkastuksen kautta.
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
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
ms.openlocfilehash: df209cfdbdef591e9f24161b3651316c43d69ee0
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---


# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="a1146-103">Palautettujen nimikkeiden vastaanottaminen tarkastuksen kautta</span><span class="sxs-lookup"><span data-stu-id="a1146-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="a1146-104">Valitse **Varastonhallinta** \> **Kausittainen** \> **Laadunhallinta** \> **Karanteenitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="a1146-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="a1146-105">Etsi tilausrivi, joka vastaa tarkastettavaa palautettua nimikettä.</span><span class="sxs-lookup"><span data-stu-id="a1146-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="a1146-106">Karanteenitilaus voidaan liittää vain yhteen nimiketunnukseen.</span><span class="sxs-lookup"><span data-stu-id="a1146-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="a1146-107">Jos kymmenen nimikettä palautetaan samasta lähetyksestä ja lähetetään karanteeniin ja nimikkeillä on eri nimiketunnukset, luodaan kymmenen erillistä karanteenitilausta.</span><span class="sxs-lookup"><span data-stu-id="a1146-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="a1146-108">Kun olet tutkinut nimikkeen, valitse **Käsittelykoodi**-kentässä, mitä nimikkeelle tehdään ja miten nimikkeeseen liittyvä kirjanpitotapahtuma käsitellään.</span><span class="sxs-lookup"><span data-stu-id="a1146-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="a1146-109">Esimerkkejä: nimike voidaan palauttaa varastoon ja asiakkaalle voidaan maksaa palautus, nimike voidaan hävittää ja asiakkaalle voidaan lähettää korvaava nimike tai nimike voidaan palauttaa asiakkaalle ilman hyvitystä.</span><span class="sxs-lookup"><span data-stu-id="a1146-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="a1146-110">Jos saman nimiketunnuserän useille palautetuille nimikkeille ei voi määrittää samaa käsittelykoodia, karanteenitilaus on jaettava (<STRONG>Toiminnot</STRONG> &gt; <STRONG>Jako</STRONG>). Tällöin kullekin osaerälle voidaan määrittää eri käsittelykoodi.</span><span class="sxs-lookup"><span data-stu-id="a1146-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="a1146-111">Kun tarkistus on valmis, vapauta palautetut nimikkeet ja luo nimikkeen saapumisen kirjauskansion merkintä valitsemalla **Ilmoita valmiiksi**.</span><span class="sxs-lookup"><span data-stu-id="a1146-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="a1146-112">Nimikkeen vastaanottanut työntekijä tai osasto käsittelee tämän jälkeen varastoon palautettavien nimikkeiden kirjauskansion.</span><span class="sxs-lookup"><span data-stu-id="a1146-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="a1146-113">–TAI–</span><span class="sxs-lookup"><span data-stu-id="a1146-113">–or–</span></span>
    
    <span data-ttu-id="a1146-114">Päätä karanteenitilaus ja siirrä nimikkeet suoraan takaisin varastoon käyttämällä yhtä **Varasto**-painikkeista.</span><span class="sxs-lookup"><span data-stu-id="a1146-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="a1146-115">Tallenna muutokset sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="a1146-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1146-116">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a1146-116">See also</span></span>

[<span data-ttu-id="a1146-117">Palautettujen nimikkeiden poistotavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a1146-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  



