---
title: Resurssien ja resurssityyppien takuut
description: Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssien ja resurssityyppien takuut resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78ac93b1e681fca7d7eefd921f282a8496aa9d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245320"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="1b01a-103">Resurssien ja resurssityyppien takuut</span><span class="sxs-lookup"><span data-stu-id="1b01a-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="1b01a-104">Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssien ja resurssityyppien takuut resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="1b01a-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="1b01a-105">Takuun määrittäminen resurssityypille</span><span class="sxs-lookup"><span data-stu-id="1b01a-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="1b01a-106">Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssityypit** \> **Resurssityypit**.</span><span class="sxs-lookup"><span data-stu-id="1b01a-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="1b01a-107">Valitse vasemmanpuoleisesta ruudusta käyttöomaisuustyyppi, johon toimittajan takuusopimus liitetään, ja valitse **Resurssin oletustyypit**.</span><span class="sxs-lookup"><span data-stu-id="1b01a-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="1b01a-108">Valitse sopimus **Yleiset**-pikavälilehden **Toimittajan takuu** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1b01a-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="1b01a-109">Takuun määrittäminen resurssille</span><span class="sxs-lookup"><span data-stu-id="1b01a-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="1b01a-110">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="1b01a-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="1b01a-111">Valitse käyttöomaisuuserä ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="1b01a-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="1b01a-112">Valitse takuusopimus **Toimittaja**-pikavälilehden **Toimittajan takuu**-osan **Takuu**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1b01a-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="1b01a-113">Valitse **Takuun alkamispäivämäärä**- ja **Takuun päättymispäivämäärä** -kentissä alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="1b01a-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1b01a-114">Jos työtilauksen **Takuun alkamispäivämäärä** -kentässä on valittu päivämäärä, takuu on voimassa kyseisenä päivänä työtilaukselle.</span><span class="sxs-lookup"><span data-stu-id="1b01a-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="1b01a-115">Kun luot työtilauksen, **Takuun alkamispäivämäärä** -kentän arvoksi tulee automaattisesti luontipäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="1b01a-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="1b01a-116">Voit kuitenkin muuttaa päivää niin, että se vastaa esimerkiksi takuusopimuksen alkamispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="1b01a-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Työtilaussivu](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="1b01a-118">Kun luot työtilauksen käyttöomaisuudelle, joka kuuluu toimittajan takuun piiriin ja jos työtilauksen odotettu alkamispäivämäärä on takuukauden aikana, saat takuusopimuksesta ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="1b01a-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="1b01a-119">Tämän jälkeen voit peruuttaa työtilauksen tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1b01a-119">You can then cancel the work order, as you require.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]