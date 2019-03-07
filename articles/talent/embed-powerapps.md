---
title: PowerApps-sovellusten upottaminen Core HR:ään
description: Tässä ohjeaihe on ratkaisu ongelmalle, jossa PowerApps-valikkovaihtoehto on kadonnut järjestelmänhallintamoduulista.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304239"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="c6325-103">PowerApps-sovellusten upottaminen Core HR:ään</span><span class="sxs-lookup"><span data-stu-id="c6325-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6325-104">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="c6325-104">**Issue**</span></span>

<span data-ttu-id="c6325-105">**PowerApps**-valikkovaihto on kadonnut **Järjestelmänhallinta**-moduulista.</span><span class="sxs-lookup"><span data-stu-id="c6325-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="c6325-106">**Syy**</span><span class="sxs-lookup"><span data-stu-id="c6325-106">**Cause**</span></span>

<span data-ttu-id="c6325-107">Käyttöliittymää on muutettu ja Microsoft PowerApps sisältyy vakiomukautusmalliin.</span><span class="sxs-lookup"><span data-stu-id="c6325-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="c6325-108">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="c6325-108">**Resolution**</span></span>

<span data-ttu-id="c6325-109">PowerApps-sovellusten upotustapaa on muutettu.</span><span class="sxs-lookup"><span data-stu-id="c6325-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="c6325-110">PowerApps-sovellukset lisätään nyt mukautusmallin avulla.</span><span class="sxs-lookup"><span data-stu-id="c6325-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="c6325-111">Voit lisätä PowerApps-sovelluksia lähes kaikille Microsoft Dynamics 365 for Talentin sivuille.</span><span class="sxs-lookup"><span data-stu-id="c6325-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="c6325-112">Lisätietoja PowerApps-sovelluksen upottamisesta Talentissa on kohdassa [PowerApps-sovellusten upottaminen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="c6325-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="c6325-113">Jokainen ennen muutoksia sovelluksia upottanut PowerApps-asiakas olisi pitänyt päivittää uuteen malliin.</span><span class="sxs-lookup"><span data-stu-id="c6325-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="c6325-114">**PowerApps**-painike on lähes jokaisen Talent-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="c6325-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="c6325-115">Voit lisätä PowerApps-sovelluksen tällä painikkeella.</span><span class="sxs-lookup"><span data-stu-id="c6325-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="c6325-116">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="c6325-116">Here is an example.</span></span>

1. <span data-ttu-id="c6325-117">Valitse **Henkilöstön hallinta \> Linkit \> Työntekijät \> Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="c6325-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="c6325-118">Valitse ensin **PowerApps**-painike ja sitten **Lisää PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="c6325-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-painike](media/png.png)

3. <span data-ttu-id="c6325-120">Täytä **Lisää PowerApp** -valintaikkunan kentät.</span><span class="sxs-lookup"><span data-stu-id="c6325-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Lisää PowerApp -valintaikkuna](media/insert-powerapp.png)

<span data-ttu-id="c6325-122">Voit vaihtoehtoisesti noudattaa seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="c6325-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="c6325-123">Valitse sivun toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä **Mukauta tämä lomake**.</span><span class="sxs-lookup"><span data-stu-id="c6325-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Mukauta-ryhmä Asetukset-välilehdessä](media/options.png)

    <span data-ttu-id="c6325-125">Mukauttamisen työkalurivi tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="c6325-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="c6325-126">Valitse työkalurivillä **Lisää \>PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="c6325-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![PowerApps-sovelluksen lisääminen mukauttamisen työkalurivin avulla](media/powerapp-bar.png)
