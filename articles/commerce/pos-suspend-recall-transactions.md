---
title: Tapahtuman keskeyttäminen ja jatkaminen myyntipisteessä
description: Tässä ohjeaiheessa kerrotaan, miten käyttäjä voi keskeyttää meneillään olevat tapahtumat ja jatkaa niitä sitten myöhemmin tai toisessa kassakoneessa Dynamics 365 Commercessa.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb92de200690b03a55a3a173fd433478c8e3175d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231269"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="627d9-103">Tapahtuman keskeyttäminen ja jatkaminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="627d9-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="627d9-104">Myyntipisteen käyttäjät voivat keskeyttää meneillään olevat tapahtumat ja jatkaa niitä sitten myöhemmin tai toisessa kassakoneessa.</span><span class="sxs-lookup"><span data-stu-id="627d9-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="627d9-105">Tapahtumat keskeytetään usein sen vuoksi, että kassakoneella voi tehdä jonkin muun tehtävän. Jos näin tehdään, nykyinen tapahtuma jää keskeytyskohtaan odottamaan jatkamista.</span><span class="sxs-lookup"><span data-stu-id="627d9-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="627d9-106">Vaikka myymälän myyjä voi esimerkiksi aloittaa asiakkaan tapahtuman käsittelyn mobiililaitteessa, hän tarvitsee sen viimeistelyyn kuitenkin kassakoneen.</span><span class="sxs-lookup"><span data-stu-id="627d9-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="627d9-107">Myyjä voi tässä tapauksessa keskeyttää tapahtuman mobiililaitteessa ja jatkaa sitä sitten kassakoneessa.</span><span class="sxs-lookup"><span data-stu-id="627d9-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="627d9-108">Keskeytys- ja jatkamistoimintojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="627d9-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="627d9-109">POS-toiminnot</span><span class="sxs-lookup"><span data-stu-id="627d9-109">POS operations</span></span>

<span data-ttu-id="627d9-110">Kahden [myyntipistetoiminnon](pos-operations.md) ansiosta myyntipiste tukee keskeytys- ja jatkamisskenaarioita.</span><span class="sxs-lookup"><span data-stu-id="627d9-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="627d9-111">Voit määrittää nämä toiminnot [painikeruudukkoihin](pos-screen-layouts.md) tapahtuma- tai aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="627d9-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="627d9-112">503: Keskeytä tapahtuma</span><span class="sxs-lookup"><span data-stu-id="627d9-112">503: Suspend transaction</span></span>
- <span data-ttu-id="627d9-113">504: Jatka tapahtumaa</span><span class="sxs-lookup"><span data-stu-id="627d9-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="627d9-114">Kuittimalli</span><span class="sxs-lookup"><span data-stu-id="627d9-114">Receipt template</span></span>

<span data-ttu-id="627d9-115">Myyntipiste voidaan määrittää luomaan tulostettu luettelo, kun tapahtuma keskeytetään.</span><span class="sxs-lookup"><span data-stu-id="627d9-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="627d9-116">Tapahtuma voidaan sitten myöhemmin tunnistaa ja uudelleenkutsua nopeasti tämän luettelon avulla.</span><span class="sxs-lookup"><span data-stu-id="627d9-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="627d9-117">Myyntipiste voi tulostaa luettelon, kun **Keskeytetty tapahtuma** -kuittimuoto on lisätty myymälän kuittiprofiiliin.</span><span class="sxs-lookup"><span data-stu-id="627d9-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="627d9-118">Voit suunnitella kuitin muodon siten, että se joko sisältää tietyt tapahtumaa koskevat tiedot tai että ne jäävät pois.</span><span class="sxs-lookup"><span data-stu-id="627d9-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="627d9-119">Muoto voi sisältää esimerkiksi lukemista tukevan viivakoodin.</span><span class="sxs-lookup"><span data-stu-id="627d9-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="627d9-120">Kuitin numerointi</span><span class="sxs-lookup"><span data-stu-id="627d9-120">Receipt numbering</span></span>

<span data-ttu-id="627d9-121">Muiden tulostetun kuitin luovien myyntipisteen tapahtumatyyppien tavoin keskeytetyille tapahtumille voi määrittää numerosarjan myymälän toimintoprofiilin **Kuitin numerointi** -osassa.</span><span class="sxs-lookup"><span data-stu-id="627d9-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="627d9-122">Mitätöi, kun vuoro suljetaan</span><span class="sxs-lookup"><span data-stu-id="627d9-122">Void when closing shift</span></span>

<span data-ttu-id="627d9-123">Voit edellyttää **Mitätöi, kun vuoro suljetaan** -asetuksen avulla, että käyttäjät joko viimeistelevät tai mitätöivät kaikki keskeytetyt toiminnot ennen vuoron sulkemista.</span><span class="sxs-lookup"><span data-stu-id="627d9-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="627d9-124">Myyntipiste pyytää **Sulje vuoro** -toiminnon aikana, että käyttäjät joko tarkastelevat tai mitätöivät keskeneräiset keskeytetyt tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="627d9-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="627d9-125">Tapahtuman keskeyttäminen ja jatkaminen</span><span class="sxs-lookup"><span data-stu-id="627d9-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="627d9-126">Tapahtuman keskeyttäminen</span><span class="sxs-lookup"><span data-stu-id="627d9-126">Suspend a transaction</span></span>

<span data-ttu-id="627d9-127">Jos käyttäjällä on riittävät oikeudet ja jos hänen näyttöasetteluunsa sisältyy **Keskeytä tapahtuma** -toiminto, käyttäjä voi keskeyttää tapahtuman siten, että se voidaan kutsua myöhemmin uudelleen tai että sitä voidaan käyttää toisessa kassakoneessa.</span><span class="sxs-lookup"><span data-stu-id="627d9-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="627d9-128">Tapahtumat voidaan keskeyttää vain, jos niissä **ei** ole seuraavia rivityyppejä:</span><span class="sxs-lookup"><span data-stu-id="627d9-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="627d9-129">Aktiiviset maksurivit</span><span class="sxs-lookup"><span data-stu-id="627d9-129">Active payment lines</span></span>
- <span data-ttu-id="627d9-130">Lahjakorttirivit (joko lahjakortin myöntämiseen tai lahjakorttisaldoon lisäämiseen)</span><span class="sxs-lookup"><span data-stu-id="627d9-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="627d9-131">Keskeytetty tapahtuma ei vaikuta myymälän myyntitietoihin tai käytettävissä olevan varaston tietoihin.</span><span class="sxs-lookup"><span data-stu-id="627d9-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="627d9-132">Keskeytetyn tapahtuman jatkaminen</span><span class="sxs-lookup"><span data-stu-id="627d9-132">Resume a suspended transaction</span></span>

<span data-ttu-id="627d9-133">Kuka tahansa saman myymälän käyttäjä, jolla on riittävät oikeudet, voi kutsua keskeytetyt tapahtumat uudelleen ja jatkaa niitä. Lisäksi kyseisellä käyttäjällä on oltava näyttö. jossa on **Jatka tapahtumaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="627d9-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="627d9-134">Keskeytettyä tapahtumaa voi jatkaa nopeasti ja kätevästi lukemalla viivakoodin tulostetussa luettelossa samalla, kun tarkastelet **Jatka tapahtumaa** -toiminnon tapahtumaluetteloa.</span><span class="sxs-lookup"><span data-stu-id="627d9-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="627d9-135">Offline-tilaa koskevia huomautuksia</span><span class="sxs-lookup"><span data-stu-id="627d9-135">Considerations for offline mode</span></span>

- <span data-ttu-id="627d9-136">Jos tapahtuma on keskeytetty, kun myyntipiste on online-tilassa, sitä ei voi jatkaa offline-tilassa, sillä tietoja ei ole synkronoitu offline-tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="627d9-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="627d9-137">Jos keskeytät tapahtuman, kun myyntipiste on offline-tilassa, voit jatkaa sitä offline-tilassa, kunhan kyseinen myyntipiste ei ole siirtynyt missään vaiheessa takaisin online-tilaan tapahtuman keskeytyksen aikana.</span><span class="sxs-lookup"><span data-stu-id="627d9-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="627d9-138">Kun myyntipiste siirtyy takaisin online-tilaan, keskeytettyjen tapahtumien tiedot siirretään online-tietokantaan ja poistetaan offline-tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="627d9-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="627d9-139">Tämän vuoksi tapahtumia voidaan jatkaa vain online-tilassa.</span><span class="sxs-lookup"><span data-stu-id="627d9-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="627d9-140">Jos myyntipiste siirretään takaisin offline-tilaan, kyseisiä keskeytettyjä tapahtumia ei voi jatkaa, koska ne on jo poistettu offline-tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="627d9-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="627d9-141">Keskeytetyn tapahtuman mitätöinti</span><span class="sxs-lookup"><span data-stu-id="627d9-141">Void a suspended transaction</span></span>

<span data-ttu-id="627d9-142">Voit mitätöidä keskeytetyt tapahtumat joko jatkamalla tapahtumaa ja suorittamalla sitten **Mitätöi tapahtuma** -toiminnon tai valitsemalla tapahtuman **Jatka tapahtumaa** -luettelossa ja valitsemalla sitten sovelluspalkissa **Mitätön**.</span><span class="sxs-lookup"><span data-stu-id="627d9-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="627d9-143">Myymälä voidaan määrittää myös pyytämään käyttäjät mitätöimään keskeytetyt tapahtumat vuoron sulkemisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="627d9-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]