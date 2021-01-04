---
title: Dynamics 365 Commerce -hinnoittelumoduulin käyttäminen Dynamics 365 Salesin kanssa
description: Tässä aiheessa kuvataan, kuinka Dynamics 365 Commerce -hinnoittelumoduulia käytetään myyntitarjousten luomiseen Dynamics 365 Salesissa.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594915"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="a2b3b-103">Dynamics 365 Commerce -hinnoittelumoduulin käyttäminen Dynamics 365 Salesin kanssa</span><span class="sxs-lookup"><span data-stu-id="a2b3b-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2b3b-104">Tässä aiheessa kuvataan, kuinka Dynamics 365 Commerce -hinnoittelumoduulia käytetään myyntitarjousten luomiseen Dynamics 365 Salesissa.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="a2b3b-105">Dynamics 365 Commerce -hinnoittelumoduuli tukee useimpia kuluttajakaupan (B2C) hinnoitteluskenaarioita, kuten myymälätason hinnoittelua, kumppanuus- ja lojaalisuushinnoittelua, yhdistelmäalennuksia, määräalennuksia ja kynnysalennuksia.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="a2b3b-106">Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="a2b3b-107">Kun käytät [kaksoiskirjoittamista ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), hinnoittelutarpeisiisi on kolme vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="a2b3b-108">Voit käyttää kiinteähintaista hinnoittelua, joka tulee Dynamics 365 Salesin hinnastosta, hinnoittelumoduulia Dynamics 365 Supply Chain Managementissa, tai hinnoittelumoduulia Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a2b3b-109">Näiden vaihtoehtojen joukossa on Commercen hinnoittelumoduuli, joka soveltuu parhaiten asiakaskaupan skenaarioihin.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="a2b3b-110">Käytä Commercen hinnoittelumoduulia Salesissa</span><span class="sxs-lookup"><span data-stu-id="a2b3b-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="a2b3b-111">Tällä hetkellä Commercen hinnoittelumoduulia voidaan käyttää vain tarjousten luomiseen Salesissa.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="a2b3b-112">Myyntitilausten integrointi Commercen hinnoittelumoduuliin ei ole vielä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="a2b3b-113">Kun käyttäjät aloittavat tarjouksen Salesissa, kaksoiskirjoituskehys kopioi tarjouksen tiedot Commerceen.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="a2b3b-114">Aiemmin luotuihin tarjousriveihin tai uusiin tarjousriveihin Salesissa tehdyt muutokset kopioidaan Commerceen.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="a2b3b-115">Kun käyttäjät haluavat käyttää Commercen hinnoittelumoduulia tarjouksen hinnoittelussa, he voivat valita **Hintatarjouksen** päivittääkseen tarjouksen hinnat Commercen hinnoittelumoduulin perusteella.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="a2b3b-116">Tämän jälkeen hinnat päivitetään automaattisesti sekä Salesissa että Commercessa.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a2b3b-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="a2b3b-117">Prerequisites</span></span>

- <span data-ttu-id="a2b3b-118">Ennen kuin voit käyttää Commercen hinnoittelu moduulia Salesissa, sinun on suoritettava vaiheet kohdassa [Mahdollisesta asiakkaasta käteiseen kaksoiskirjoituksella](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="a2b3b-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="a2b3b-119">Sinun on poistettava kauppasopimuksen arviointi käytöstä manuaaliselle syötölle seuraamalla näitä vaiheita:</span><span class="sxs-lookup"><span data-stu-id="a2b3b-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="a2b3b-120">Siirry Commerce-ympäristössäsi kohtaan **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="a2b3b-121">Tyhjennä **Hinnat** välilehden **Kauppasopimuksen arviointi** -pikavälilehdellä **Manuaalinen syöttö** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a2b3b-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2b3b-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a2b3b-122">Additional resources</span></span>

[<span data-ttu-id="a2b3b-123">Prospektista käteiseksi -kaksoiskirjoitus</span><span class="sxs-lookup"><span data-stu-id="a2b3b-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)
