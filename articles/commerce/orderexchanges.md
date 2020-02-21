---
title: Palautustilauksen vaihdon määritys ja käsittely
description: Tässä ohjeaiheessa kerrotaan, miten vaihto palautuksen yhteydessä konfiguroidaan ohjelmassa Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6d7688e78a375bc262b1156c5439c0fff7cd1f0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004432"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="e144e-103">Palautustilaukseen liittyvän vaihdon määritys ja käsittely</span><span class="sxs-lookup"><span data-stu-id="e144e-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e144e-104">Dynamics 365 Commercen aiemmissa versioissa asiakastilausten palautukset käsiteltiin käyttämällä palautustilauksen asiakirjaa Headquarters -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="e144e-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="e144e-105">Palautustilauksen asiakirjaa voidaan kuitenkin käyttää vain palautettavien tuotteiden käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="e144e-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="e144e-106">Palautetut tuotteet on merkitty palautustilauksen riveille negatiivisena määränä.</span><span class="sxs-lookup"><span data-stu-id="e144e-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="e144e-107">Sen sijaan myynti on merkitty on positiivisena määränä.</span><span class="sxs-lookup"><span data-stu-id="e144e-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="e144e-108">Palautustilauksen asiakirja ei kuitenkaan tue positiivisia määriä.</span><span class="sxs-lookup"><span data-stu-id="e144e-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="e144e-109">Tämän rajoituksen vuoksi sovelluksen aiemmat versiot eivät tukeneet tilanteita, joissa tuotteita vaihdettiin käyttämällä palautustilauksen asiakirjaa.</span><span class="sxs-lookup"><span data-stu-id="e144e-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="e144e-110">Toiminto on nyt lisätty tukemaan tilanteita, joissa palautustilauksiin liittyy tuotteiden vaihto.</span><span class="sxs-lookup"><span data-stu-id="e144e-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="e144e-111">Nyt Commerce käyttää palautustilauksen asiakirjan sijaan myyntitilauksen asiakirjaa käsittelemään tämäntyyppisiä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="e144e-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="e144e-112">Commercen määrittäminen tukemaan tuotteiden vaihtoa palautustilauksissa</span><span class="sxs-lookup"><span data-stu-id="e144e-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="e144e-113">Voit määrittää järjestelmän tukemaan vaihtoa palautustilauksissa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e144e-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="e144e-114">Valitse **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="e144e-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="e144e-115">Määritä **Asiakastilaukset**-pikavälilehdessä **Käsittele palautustilauksia myyntitilauksina** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e144e-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="e144e-116">Suorita **Yleinen määritysjakelun aikataulu** -työ (**1110**).</span><span class="sxs-lookup"><span data-stu-id="e144e-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="e144e-117">Vaihdon tekeminen</span><span class="sxs-lookup"><span data-stu-id="e144e-117">Make an exchange</span></span>

<span data-ttu-id="e144e-118">Kun järjestelmä on määritetty edellä kuvatulla tavalla, myyntipisteen käyttäjä edelleen valitsee palautuksen käsittelyyn myyntitilauksen tai myyntilaskun, kuten aiemmissa sovellusversioissakin.</span><span class="sxs-lookup"><span data-stu-id="e144e-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="e144e-119">Kun palautetut nimikkeet on lisätty ostoskoriin, käyttäjä voi kuitenkin lisätä myös uusia myyntirivejä ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="e144e-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="e144e-120">Näille uusille myyntiriveille käyttäjän on määritettävä kaikki määritteet, jotka tarvitaan asiakastilauksen rivin käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="e144e-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="e144e-121">Näihin määritteisiin kuuluvat toimitustapa sekä täyttämissijainti.</span><span class="sxs-lookup"><span data-stu-id="e144e-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="e144e-122">Tapahtuman maksettava summa on palautustilauksen rivien ja myyntitilausrivien nettosumma.</span><span class="sxs-lookup"><span data-stu-id="e144e-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="e144e-123">Kun tapahtuman maksu maksetaan, palautustilaus kirjataan myyntitilausasiakirjana Headquarters-sovelluksessa ja järjestelmä laskuttaa palautusrivit välittömästi.</span><span class="sxs-lookup"><span data-stu-id="e144e-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="e144e-124">Ostoskoriin on lisätty kolme uutta summakenttää, jotta ostoskorin eri summat erottuisivat selkeästi.</span><span class="sxs-lookup"><span data-stu-id="e144e-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="e144e-125">Näytön suunnitteluohjelmassa voit lisätä nämä uudet kentät myyntipisteen käyttöliittymään.</span><span class="sxs-lookup"><span data-stu-id="e144e-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="e144e-126">**Käytetty talletus** – Tallennussumma, jota käytetään tapahtumassa, kun käyttäjä suorittaa asiakastilauksen noudon.</span><span class="sxs-lookup"><span data-stu-id="e144e-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="e144e-127">Jos talletuksen ohitus ei ole käytössä ja määritetään 10 prosentin talletus, tähän kenttään tulee 90 prosenttia asiakastilauksen kokonaissummasta.</span><span class="sxs-lookup"><span data-stu-id="e144e-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="e144e-128">**Suoritussumma** – Niiden rivien kokonaissumma, joiden toimitustavaksi oli määritetty **Suoritus** asiakastilausta luotaessa tai muokattaessa tai asiakastilaukseen liittyvän vaihdon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e144e-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="e144e-129">Tämän kentän summa sisältää verot ja maksut.</span><span class="sxs-lookup"><span data-stu-id="e144e-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="e144e-130">**Palautussumma** – Niiden rivien kokonaissumma, joilla on negatiiviset määrät asiakastilauksen vaihdon aikana.</span><span class="sxs-lookup"><span data-stu-id="e144e-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="e144e-131">Tämän kentän summa sisältää verot ja maksut.</span><span class="sxs-lookup"><span data-stu-id="e144e-131">The amount in this field includes taxes and charges.</span></span>
