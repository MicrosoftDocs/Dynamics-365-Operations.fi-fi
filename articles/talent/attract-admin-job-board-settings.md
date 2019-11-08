---
title: Broadbean-integroinnin ottaminen käyttöön Microsoft Dynamics 365 Talent – Attractissa
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent – Attractin määrittämistä julkaisemaan työpaikat ulkopuolisissa työpaikkailmoitussivustoissa, kuten Broadbeanissa.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0ca655655f79ddf88b6f6c7377a1b596477c35a7
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552137"
---
# <a name="enable-broadbean-integration-in-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="891e0-103">Broadbean-integroinnin ottaminen käyttöön Microsoft Dynamics 365 Talent – Attractissa</span><span class="sxs-lookup"><span data-stu-id="891e0-103">Enable Broadbean integration in Microsoft Dynamics 365 Talent - Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="891e0-104">Haluat saada työpaikkailmoituksesi mahdollisimman monen pätevän ehdokkaan näkyville kuin mahdollista.</span><span class="sxs-lookup"><span data-stu-id="891e0-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="891e0-105">Työhönoton sivustot, kuten Broadbean, voi auttaa saavuttamaan tämän tavoitteen.</span><span class="sxs-lookup"><span data-stu-id="891e0-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="891e0-106">Microsoft Dynamics 365 Talent: Attractin avulla voit nyt julkaista työpaikkoja Broadbeanissa, ja Microsoft tarjoaa koko ajan uusia mahdollisuuksia tällä alueella.</span><span class="sxs-lookup"><span data-stu-id="891e0-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="891e0-107">Voit julkaista töitä ulkoisille sivustoille vain jos sinulla on [kattava työhönottolaajennus](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="891e0-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="891e0-108">Jos haluat kirjata työt Broadbean-tilaan Attractilla, sinulla on oltava Broadbean-tilaus.</span><span class="sxs-lookup"><span data-stu-id="891e0-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="891e0-109">Tämä ominaisuus on tällä hetkellä vain esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="891e0-109">This feature is currently in preview.</span></span> <span data-ttu-id="891e0-110">Voit halutessasi kokeilla sitä [ottamalla sen käyttöön Attractin järjestelmänvalvojan asetuksissa](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="891e0-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="891e0-111">Broadbean-integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="891e0-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="891e0-112">Kirjaudu Attractiin järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="891e0-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="891e0-113">Valitse **Asetukset**-painike (rataskuvake) sivun oikeassa yläkulmassa ja valitse sitten **Hallintakeskus**.</span><span class="sxs-lookup"><span data-stu-id="891e0-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="891e0-114">Muodosta yhteys Broadbeaniin ja anna tietosi **Käyttäjätunnus**-, **Asiakastunnus**- ja **Salaustunnus** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="891e0-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="891e0-115">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="891e0-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="891e0-116">Broadbean-tunnistetietosi ovat luottamuksellisia.</span><span class="sxs-lookup"><span data-stu-id="891e0-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="891e0-117">Siksi tallenna ja jaa niitä vastuuntuntoisesti.</span><span class="sxs-lookup"><span data-stu-id="891e0-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="891e0-118">Kaikki käyttäjät, joilla on järjestelmänvalvojan rooli Attractissa, voivat tarkastella näitä tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="891e0-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="891e0-119">Microsoft ja Attract eivät ole mukana luomassa ja ylläpitämässä näitä arvoja.</span><span class="sxs-lookup"><span data-stu-id="891e0-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="891e0-120">On omalla vastuullasi pitää ne ajan tasalla Attractissa ja selvittää mahdolliset ongelmat Broadbeanin kanssa.</span><span class="sxs-lookup"><span data-stu-id="891e0-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
