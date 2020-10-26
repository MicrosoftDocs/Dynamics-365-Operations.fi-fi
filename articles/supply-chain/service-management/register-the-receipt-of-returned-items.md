---
title: Palautettujen nimikkeiden vastaanoton rekisteröiminen
description: Voit rekisteröidä palautetut nimikkeet vastaanotetuiksi Saapumisten yleiskatsaus -lomakkeella tai Rekisteröinti-lomakkeella.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42ca1d4d2d9b45d79cf479833f83e498e3b73540
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975629"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="110a0-103">Palautettujen nimikkeiden vastaanoton rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="110a0-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="110a0-104">Järjestelmässä on kaksi tapaa rekisteröidä palautettujen nimikkeiden vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="110a0-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="110a0-105">Ensimmäinen menetelmä on vastaanottavan varaston prosessi, joka käyttää **Saapumisten yleiskatsaus** -lomaketta.</span><span class="sxs-lookup"><span data-stu-id="110a0-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="110a0-106">Toinen käyttää **Rekisteröinti**-lomaketta.</span><span class="sxs-lookup"><span data-stu-id="110a0-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="110a0-107">Rekisteröi palautettujen nimikkeiden vastaanotto Saapumisten yhteenveto -lomakkeella</span><span class="sxs-lookup"><span data-stu-id="110a0-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="110a0-108">Voit käyttää **Saapumisten yleiskatsaus** -lomaketta tunnistamaan palautuslähetyksen palautusnumeron (RMA) perusteella.</span><span class="sxs-lookup"><span data-stu-id="110a0-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="110a0-109">Jos kirjauskansion nimi on määritetty **Määritys**-välilehdellä ja kirjauskansiorivit, jotka vastaavat **Saapumisten yleiskatsaus** -lomakkeella valittuja rivejä ovat olemassa, uuden kirjauskansion otsikko luodaan, kun valitset **Aloita saapuminen**.</span><span class="sxs-lookup"><span data-stu-id="110a0-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="110a0-110">Napsauta **Varastonhallinta** \> **Kausittainen** \> **Saapumisten yhteenveto**.</span><span class="sxs-lookup"><span data-stu-id="110a0-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="110a0-111">Valitse **Asetusten nimi** -kentässä **Palautustilaus**, ja napsauta sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="110a0-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="110a0-112">Voit kaventaa hakutuloksia <STRONG>Alue</STRONG>-kenttien avulla.</span><span class="sxs-lookup"><span data-stu-id="110a0-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="110a0-113">Voit kirjoittaa tai valita palautusnumeron <STRONG>Palautusnumero</STRONG>-kentässä, kun haluat saada tarkan tuloksen.</span><span class="sxs-lookup"><span data-stu-id="110a0-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="110a0-114">Määritä ja tallenna suodatinjoukko, joka rajaa näytettäviä saapumisia, napsauttamalla <STRONG>Määritys</STRONG>-välilehteä. Käytettävissä on suodattimet tyyppien, varastojen ja laiturien mukaan.</span><span class="sxs-lookup"><span data-stu-id="110a0-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="110a0-115">Palautustilauksia ei voi sekoittaa muiden saapumistyyppien kanssa <STRONG>Saapumisten yleiskatsaus</STRONG> -lomakkeella.</span><span class="sxs-lookup"><span data-stu-id="110a0-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="110a0-116">Tämän vuoksi viitteenä on aina oltava myyntitilaus, mutta myyntitilauksen tunnusta ei määritetä kirjauskansion otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="110a0-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="110a0-117">Etsi **Kuitit**-ruudukossa rivi, joka vastaa palautettavaa nimikettä ja valitse sitten **Valitse saapumiseen** -sarakkeen valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="110a0-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="110a0-118">Jos haluat sulkea tietyt rivit, kuten alkuperäisen tilauksen palautuslähetyksestä poissuljetut rivit, pois palautuksen vastaanotosta, poista liittyvien **Valitse saapumiseen** -ruutujen valinnat lomakkeen alaosan **Rivit**-taulusta.</span><span class="sxs-lookup"><span data-stu-id="110a0-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="110a0-119">Valitse **Aloita saapuminen** -painike ja luo saapumisen kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="110a0-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="110a0-120">Voit valita useita palautustilauksia ja sisällyttää ne kaikki yhteen saapumisprosessiin.</span><span class="sxs-lookup"><span data-stu-id="110a0-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="110a0-121">Jokainen palautustilausrivi kopioidaan vastaavan nimikkeen saapumisen kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="110a0-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="110a0-122">Voit luoda saapumisen kirjauskansion myös manuaalisesti <STRONG>Nimikkeen saapuminen</STRONG> -lomakkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="110a0-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="110a0-123">Napsauta **Varastonhallinta** \> **Kirjauskansiot** \> **Nimikkeen saapuminen** \> **Nimikkeen saapuminen**.</span><span class="sxs-lookup"><span data-stu-id="110a0-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="110a0-124">Valitse juuri luomasi saapumisen kirjauskansio ja valitse sitten **Rivit** avataksesi **Kirjauskansion rivit, sijainnit** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="110a0-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="110a0-125">Säädä **Yleinen**-välilehdessä numeroa **Määrä**-kentässä, jos tämä on tarpeen, ja määritä sitten käsittelykoodi **Käsittelykoodi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="110a0-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="110a0-126">Vaihtoehtoisesti voit valita **Karanteeninhallinta**-valintaruudun, joka asettaa palautetut nimikkeet lähetettäväksi tarkastusprosessin kautta karanteenitilauksen kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="110a0-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="110a0-127">Jos lähetät palautetut nimikkeet karanteenissa kautta, et voi määrittää käsittelykoodia.</span><span class="sxs-lookup"><span data-stu-id="110a0-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="110a0-128">Valitse **Vahvista**-painike.</span><span class="sxs-lookup"><span data-stu-id="110a0-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="110a0-129">Jos oikeellisuustarkistuksessa ei ole virheitä, valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="110a0-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="110a0-130">Rekisteröi palautettujen nimikkeiden vastaanotto rekisteröintilomakkeella</span><span class="sxs-lookup"><span data-stu-id="110a0-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="110a0-131">**Saapumisten yleiskatsaus** -lomakkeen sijasta voit käyttää palautettujen nimikkeiden saapumisten rekisteröimiseen **Rekisteröinti**-lomaketta.</span><span class="sxs-lookup"><span data-stu-id="110a0-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="110a0-132">Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**.</span><span class="sxs-lookup"><span data-stu-id="110a0-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="110a0-133">Luo uusi palautustilaus tai avaa palautustilaus luettelosta.</span><span class="sxs-lookup"><span data-stu-id="110a0-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="110a0-134">Valitse palautustilausrivi **Rivit**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="110a0-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="110a0-135">Valitse **Päivitä rivi**, ja valitse sitten **Rekisteröinti**.</span><span class="sxs-lookup"><span data-stu-id="110a0-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="110a0-136">Määritä käsittelykoodi **Käsittelykoodi**-kenttään ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="110a0-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="110a0-137">Nimikkeen lähettäminen tarkastettavaksi karanteenitilauksena ei ole mahdollista <STRONG>Rekisteröinti</STRONG>-lomakkeen avulla.</span><span class="sxs-lookup"><span data-stu-id="110a0-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="110a0-138">Valitse **Tapahtumat**-ruudukossa rekisteröitävä tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="110a0-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="110a0-139">Valitse **Rekisteröi nyt** -ruudukossa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="110a0-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="110a0-140">Toista kaksi aiempaa vaihetta, kunnes kaikki palautetut nimikkeet näkyvät **Rekisteröi nyt** -ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="110a0-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="110a0-141">Napsauta **Kirjaa kaikki**.</span><span class="sxs-lookup"><span data-stu-id="110a0-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="110a0-142">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="110a0-142">See also</span></span>

<span data-ttu-id="110a0-143">[Saapumisten yhteenveto (lomake)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="110a0-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  


