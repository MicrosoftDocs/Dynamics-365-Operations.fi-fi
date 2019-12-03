---
title: Eräseurannassa olevien nimikkeiden parannettu käsitteleminen
description: Tässä aiheessa kuvataan parannuksia, jotka on tehty eräseurannassa olevien nimikkeiden vähittäismyynnin laskelman kirjausprosessin aikana tehtävää erien käsittelyä varten.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5bbddf649f66ded9588cdb1e3f43c75630dc248a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770160"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="6f8b6-103">Eräseurannassa olevien nimikkeiden parannettu käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="6f8b6-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="6f8b6-104">Retail Point of Sale (POS) -sovelluksen myyntipisteen eränumeroita ei voi tallentaa eräseurannassa oleville nimikkeille myynnin aikana.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-104">In Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="6f8b6-105">Kun myynti kirjataan pääkonttorissa asiakastilausten tai laskelman kirjauksen avulla, Microsoft Dynamics -järjestelmä kuitenkin odottaa, että tietyissä määrityksissä on sallitut eränumerot eräseurannassa oleville nimikkeille ja että niitä käytetään laskutusprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="6f8b6-106">Jos tuotteilla on sallitut eränumerot, laskelman kirjauksen asiakastilauksen ja myyntitilauksen laskutusprosessi käyttää niitä.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="6f8b6-107">Muussa tapauksessa asiakastilauksen laskutusprosessi ei voi tehdä kirjausta, ja myyntipisteen käyttäjälle lähetetään virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="6f8b6-108">Tällöin laskelman kirjaus siirtyy virhetilaan.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="6f8b6-109">Tämä virhetila ilmenee, vaikka tuotteille olisi otettu käyttöön negatiivinen varasto.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="6f8b6-110">Retail-sovelluksen versioon 10.0.4 ja uudempiin versioihin tehdyt parannukset varmistavat sen, että negatiivisen varaston ollessa käytössä eräseurannassa oleville nimikkeille, asiakastilausten ja myyntitilausten laskutusta laskelman kirjauksen kautta ei estetä nimikkeille, jos varasto on 0 (nolla) tai eränumeroa ei ole saatavilla.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="6f8b6-111">Uusi toiminto käyttää myyntiriveissä oletuserätunnusta, kun eränumerot eivät ole saatavilla.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="6f8b6-112">Voit määrittää asiakastilauksissa käytettävän oletuserätunnuksen **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Vähittäismyynnin parametrit** -sivun **Oletuserätunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="6f8b6-113">Voit määrittää laskelman kirjauksen myyntitilauksen laskutuksessa käytettävän oletuserätunnuksen **Varaston päivitys** -pikavälilehden **Kirjaus**-välilehden **Vähittäismyynnin parametrit** -sivun **Oletuserätunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8b6-114">Tämä toiminto on käytettävissä vain, kun edistyksellinen varastotoiminto on käytössä tietyn myymälän varastoa ja nimikkeitä varten.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="6f8b6-115">Myöhemmässä versiossa toimintoa tuetaan myös skenaarioissa, joissa edistyksellistä varastonhallintaa ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8b6-116">Parannetun eräseurannassa olevien nimikkeiden käsittelyn tuki laskelman kirjaamisen aikana muissa kuin edistyksellisen varastonhallinnan skenaarioissa sisältyi Retail-sovelluksen versioon 10.0.5.</span><span class="sxs-lookup"><span data-stu-id="6f8b6-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>
