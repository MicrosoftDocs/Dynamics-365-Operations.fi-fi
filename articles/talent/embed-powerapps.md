---
title: PowerApps-sovellusten upottaminen Dynamics 365 – Core HR:ssä
description: Tässä ohjeaiheessa käsitellään tapaa, jolla ratkaistaan ongelma, jossa PowerApps-valikkovaihtoehto on kadonnut järjestelmänhallintamoduulista.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551000"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="8453c-103">PowerApps-sovellusten upottaminen Dynamics 365 – Core HR:ssä</span><span class="sxs-lookup"><span data-stu-id="8453c-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8453c-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="8453c-104">**Issue**</span></span>

<span data-ttu-id="8453c-105">**PowerApps**-valikkovaihtoehto on kadonnut **Järjestelmänhallinta**-moduulista.</span><span class="sxs-lookup"><span data-stu-id="8453c-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="8453c-106">**Syy**</span><span class="sxs-lookup"><span data-stu-id="8453c-106">**Cause**</span></span>

<span data-ttu-id="8453c-107">Käyttöliittymää on muutettu ja Microsoft PowerApps sisältyy vakiomukautusmalliin.</span><span class="sxs-lookup"><span data-stu-id="8453c-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="8453c-108">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="8453c-108">**Resolution**</span></span>

<span data-ttu-id="8453c-109">PowerApps-sovellusten upotustapaa on muutettu.</span><span class="sxs-lookup"><span data-stu-id="8453c-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="8453c-110">PowerApps-sovellukset lisätään nyt mukautusmallin avulla.</span><span class="sxs-lookup"><span data-stu-id="8453c-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="8453c-111">Voit lisätä PowerApps-sovelluksia lähes kaikille Microsoft Dynamics 365 Talentin sivuille.</span><span class="sxs-lookup"><span data-stu-id="8453c-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="8453c-112">Lisätietoja PowerApps-sovelluksen upottamisesta Talentissa on kohdassa [PowerApps-sovellusten upottaminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="8453c-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="8453c-113">Jokainen PowerApps-asiakas, joka on upottanut sovelluksia ennen muutosta, olisi pitänyt päivittää uuteen malliin.</span><span class="sxs-lookup"><span data-stu-id="8453c-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="8453c-114">**PowerApps**-painike on lähes jokaisen Talent-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="8453c-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="8453c-115">Voit lisätä PowerApps-sovelluksen tällä painikkeella.</span><span class="sxs-lookup"><span data-stu-id="8453c-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="8453c-116">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="8453c-116">Here is an example.</span></span>

1. <span data-ttu-id="8453c-117">Valitse **Henkilöstön hallinta \> Linkit \> Työntekijät \> Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="8453c-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="8453c-118">Valitse ensin **PowerApps**-painike ja sitten **Lisää PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="8453c-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-painike](media/png.png)

3. <span data-ttu-id="8453c-120">Täytä **Lisää PowerApp** -valintaikkunan kentät.</span><span class="sxs-lookup"><span data-stu-id="8453c-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Lisää PowerApp -valintaikkuna](media/insert-powerapp.png)

<span data-ttu-id="8453c-122">Voit vaihtoehtoisesti noudattaa seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="8453c-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="8453c-123">Valitse sivun toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä **Mukauta tämä lomake**.</span><span class="sxs-lookup"><span data-stu-id="8453c-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Mukauta-ryhmä Asetukset-välilehdessä](media/options.png)

    <span data-ttu-id="8453c-125">Mukauttamisen työkalurivi tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="8453c-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="8453c-126">Valitse työkalurivillä **Lisää \>PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="8453c-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![PowerApps-sovelluksen lisääminen mukauttamisen työkalurivin avulla](media/powerapp-bar.png)
