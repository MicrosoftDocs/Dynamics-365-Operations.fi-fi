---
title: Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksissa ja Common Data Servicessä
description: Tässä ohjeaiheessa kerrotaan, miten voit määrittää, onko Finance and Operations -sovelluksissa ja Common Data Service -moduulissa määritetty kaksoiskirjoitus.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172642"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="61959-103">Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksissa ja Common Data Servicessä</span><span class="sxs-lookup"><span data-stu-id="61959-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="61959-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="61959-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="61959-105">Erityisesti se selittää miten voit määrittää, onko Finance and Operations -sovelluksissa ja Common Data Service -moduulissa määritetty kaksoiskirjoitus.</span><span class="sxs-lookup"><span data-stu-id="61959-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="61959-106">Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="61959-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="61959-107">Jos haluat määrittää, näytetäänkö kaksoiskirjoitusvirheet, kun yrität tallentaa tietoja päivitystä varten, varmista ensin, että kaksoiskirjoitus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="61959-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="61959-108">Jos sinulla on Finance and Operations -sovelluksen järjestelmänvalvojan oikeudet, siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="61959-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="61959-109">Jos linkitettyjen ympäristöjen tiedot ja käytössä olevan yksikkökarttojen luettelo näytetään, kaksoiskirjoitus määritetään.</span><span class="sxs-lookup"><span data-stu-id="61959-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla on järjestelmänvalvojan oikeudet](media/verify_fin_ops_1.png)

+ <span data-ttu-id="61959-111">Jos sinulla ei ole järjestelmänvalvojan oikeuksia, näyttöön tulee virhesanoma *Tietoja ei voi kirjoittaa yksikköön \<yksikön nimi\>*.</span><span class="sxs-lookup"><span data-stu-id="61959-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="61959-112">Seuraavassa esimerkissä asiakastietuetta ei voi luoda Finance and Operations -sovelluksessa, koska kaksoiskirjoitus on määritetty, mutta asiakasryhmä- ja maksujen viitetietoja ei ole Common Data Service -järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="61959-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla ei ole järjestelmänvalvojan oikeuksia](media/verify_fin_ops_2.png)

<span data-ttu-id="61959-114">Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Finance and Operations -sovelluksissa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="61959-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="61959-115">Varmista, että kaksoiskirjoitus on määritetty Common Data Service -sovelluksissa</span><span class="sxs-lookup"><span data-stu-id="61959-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="61959-116">Kun luot tietoja, voit määrittää kaksoiskirjoituksen, jos Common Data Service -lomakkeen sivulla näkyy **Yritys**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="61959-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Common Data Service -yhteyden tarkistaminen](media/verify_cds.png)

<span data-ttu-id="61959-118">Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Common Data Servicessa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="61959-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="61959-119">Lisätietoja virhetietojen katsomisesta, jos virheitä syntyy luodessasi tietoja Common Data Servicessä on kohdassa [Ota käyttöön ja tarkastele laajennuksen jäljityslokia Common Data Servicessä nähdäksesi virhetiedot](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="61959-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
