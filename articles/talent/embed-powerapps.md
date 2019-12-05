---
title: Power Apps-sovellusten upottaminen Dynamics 365 – Core HR:ssä
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830206"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="9a03f-103">Power Apps-sovellusten upottaminen Dynamics 365 – Core HR:ssä</span><span class="sxs-lookup"><span data-stu-id="9a03f-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a03f-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="9a03f-104">**Issue**</span></span>

<span data-ttu-id="9a03f-105">**Power Apps**-valikkovaihtoehto on kadonnut **Järjestelmänhallinta**-moduulista.</span><span class="sxs-lookup"><span data-stu-id="9a03f-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="9a03f-106">**Syy**</span><span class="sxs-lookup"><span data-stu-id="9a03f-106">**Cause**</span></span>

<span data-ttu-id="9a03f-107">Käyttöliittymää on muutettu ja Microsoft Power Apps sisältyy vakiomukautusmalliin.</span><span class="sxs-lookup"><span data-stu-id="9a03f-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="9a03f-108">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="9a03f-108">**Resolution**</span></span>

<span data-ttu-id="9a03f-109">Power Appsin upotustapaa on muutettu.</span><span class="sxs-lookup"><span data-stu-id="9a03f-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="9a03f-110">Power Apps lisätään nyt mukautusmallin avulla.</span><span class="sxs-lookup"><span data-stu-id="9a03f-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="9a03f-111">Voit lisätä Power Appsin lähes kaikille Microsoft Dynamics 365 Talentin sivuille.</span><span class="sxs-lookup"><span data-stu-id="9a03f-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="9a03f-112">Lisätietoja Power Appsin upottamisesta Talentissa on kohdassa [Microsoft Power Appsin upottaminen](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="9a03f-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="9a03f-113">Jokainen Power Apps-asiakas, joka on upottanut sovelluksia ennen muutosta, olisi pitänyt päivittää uuteen malliin.</span><span class="sxs-lookup"><span data-stu-id="9a03f-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="9a03f-114">**Power Apps**-painike on lähes jokaisen Talent-sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="9a03f-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="9a03f-115">Voit lisätä Power Appsin tällä painikkeella.</span><span class="sxs-lookup"><span data-stu-id="9a03f-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="9a03f-116">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="9a03f-116">Here is an example.</span></span>

1. <span data-ttu-id="9a03f-117">Valitse **Henkilöstön hallinta \> Linkit \> Työntekijät \> Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="9a03f-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="9a03f-118">Valitse ensin **Power Apps**-painike ja sitten **Lisää PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="9a03f-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps-painike](media/png.png)

3. <span data-ttu-id="9a03f-120">Täytä **Lisää PowerApp** -valintaikkunan kentät.</span><span class="sxs-lookup"><span data-stu-id="9a03f-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Lisää PowerApp -valintaikkuna](media/insert-powerapp.png)

<span data-ttu-id="9a03f-122">Voit vaihtoehtoisesti noudattaa seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="9a03f-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="9a03f-123">Valitse sivun toimintoruudun **Asetukset**-välilehden **Mukauta**-ryhmässä **Mukauta tämä lomake**.</span><span class="sxs-lookup"><span data-stu-id="9a03f-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Mukauta-ryhmä Asetukset-välilehdessä](media/options.png)

    <span data-ttu-id="9a03f-125">Mukauttamisen työkalurivi tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="9a03f-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="9a03f-126">Valitse työkalurivillä **Lisää \>PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="9a03f-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Power Apps-sovelluksen lisääminen mukauttamisen työkalurivin avulla](media/powerapp-bar.png)
