---
title: Power Apps -sovellusten upottaminen Dynamics 365 Human Resourcesissa
description: Tässä ohjeaiheessa käsitellään tapaa, jolla ratkaistaan ongelma, jossa Microsoft Power Apps-valikkovaihtoehto on kadonnut järjestelmänhallintamoduulista.
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017870"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="c9f3e-103">Power Apps -sovellusten upottaminen Dynamics 365 Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="c9f3e-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="c9f3e-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="c9f3e-104">**Issue**</span></span>

<span data-ttu-id="c9f3e-105">**Power Apps**-valikkovaihtoehto on kadonnut **Järjestelmänhallinta**-moduulista.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="c9f3e-106">**Syy**</span><span class="sxs-lookup"><span data-stu-id="c9f3e-106">**Cause**</span></span>

<span data-ttu-id="c9f3e-107">Käyttöliittymää on muutettu ja Microsoft Power Apps sisältyy vakiomukautusmalliin.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="c9f3e-108">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="c9f3e-108">**Resolution**</span></span>

<span data-ttu-id="c9f3e-109">Power Appsin upotustapaa on muutettu.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="c9f3e-110">Power Apps lisätään nyt mukautusmallin avulla.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="c9f3e-111">Voit lisätä Power Appsin lähes kaikille Microsoft Dynamics 365 Talentin sivuille.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="c9f3e-112">Lisätietoja Power Appsin upottamisesta Talentissa on kohdassa [Power Appsin upottaminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="c9f3e-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="c9f3e-113">Jokainen Power Apps-asiakas, joka on upottanut sovelluksia ennen muutosta, olisi pitänyt päivittää uuteen malliin.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="c9f3e-114">**Power Apps**-painike on lähes jokaisen Talent-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="c9f3e-115">Voit lisätä sovelluksia tällä painikkeella.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="c9f3e-116">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="c9f3e-116">Here is an example.</span></span>

1. <span data-ttu-id="c9f3e-117">Valitse **Henkilöstön hallinta \> Linkit \> Työntekijät \> Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="c9f3e-118">Valitse- **Power Apps** -painike ja sitten **Lisää sovellus Power Appsista**.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Power Apps-painike](media/png.png)

3. <span data-ttu-id="c9f3e-120">Täytä kentät **Lisää sovellus Power Appsista** -valintaruudussa.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Sovelluksen lisääminen Power Apps -valintaruudusta](media/insert-powerapp.png)

<span data-ttu-id="c9f3e-122">Voit vaihtoehtoisesti noudattaa seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="c9f3e-123">Valitse sivun toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä **Mukauta tämä sivu**.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Mukauta-ryhmä Asetukset-välilehdessä](media/options.png)

    <span data-ttu-id="c9f3e-125">Mukauttamisen työkalurivi tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="c9f3e-126">Valitse työkaluriviltä **Lisää sovellus Power Appsista**.</span><span class="sxs-lookup"><span data-stu-id="c9f3e-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Power Apps-sovelluksen lisääminen mukauttamisen työkalurivin avulla](media/powerapp-bar.png)
