---
title: Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksissa ja Dataversessä
description: Tässä ohjeaiheessa kerrotaan, miten voit määrittää, onko Finance and Operations -sovelluksissa ja Dataverse -moduulissa määritetty kaksoiskirjoitus.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685536"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="6f6c6-103">Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksissa ja Dataversessä</span><span class="sxs-lookup"><span data-stu-id="6f6c6-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="6f6c6-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="6f6c6-105">Erityisesti se selittää miten voit määrittää, onko Finance and Operations -sovelluksissa ja Dataverse -moduulissa määritetty kaksoiskirjoitus.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="6f6c6-106">Varmista, että kaksoiskirjoitus on määritetty Finance and Operations -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="6f6c6-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="6f6c6-107">Jos haluat määrittää, näytetäänkö kaksoiskirjoitusvirheet, kun yrität tallentaa rivejä päivitystä varten, varmista ensin, että kaksoiskirjoitus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="6f6c6-108">Jos sinulla on Finance and Operations -sovelluksen järjestelmänvalvojan oikeudet, siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="6f6c6-109">Jos linkitettyjen ympäristöjen tiedot ja käytössä olevien taulukarttojen luettelo näytetään, kaksoiskirjoitus on määritetty.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla on järjestelmänvalvojan oikeudet](media/verify_fin_ops_1.png)

+ <span data-ttu-id="6f6c6-111">Jos sinulla ei ole järjestelmänvalvojan oikeuksia, näyttöön avautuu virhesanoma *Tietoja ei voi kirjoittaa yksikköön \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="6f6c6-112">Seuraavassa esimerkissä asiakasriviä ei voi luoda Finance and Operations -sovelluksessa, koska kaksoiskirjoitus on määritetty, mutta asiakasryhmä- ja maksujen viitetietoja ei ole Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Finance and Operations -sovellusyhteyden tarkistaminen, kun sinulla ei ole järjestelmänvalvojan oikeuksia](media/verify_fin_ops_2.png)

<span data-ttu-id="6f6c6-114">Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Finance and Operations -sovelluksissa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="6f6c6-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="6f6c6-115">Varmista, että kaksoiskirjoitus on määritetty Dataverse -sovelluksissa</span><span class="sxs-lookup"><span data-stu-id="6f6c6-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="6f6c6-116">Kun luot tietoja, voit määrittää kaksoiskirjoituksen, jos Dataverse -lomakkeen sivulla näkyy **Yritys**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="6f6c6-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![Dataverse -yhteyden tarkistaminen](media/verify_cds.png)

<span data-ttu-id="6f6c6-118">Lisätietoja ongelmien korjaamisesta, kun tietoja luodaan Dataversessa, on kohdassa [Suorasynkronointiongelmien vianmääritys](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="6f6c6-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="6f6c6-119">Lisätietoja virhetietojen katsomisesta, jos virheitä syntyy luodessasi tietoja Dataversessä on kohdassa [Ota käyttöön ja tarkastele laajennuksen jäljityslokia Dataversessä nähdäksesi virhetiedot](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="6f6c6-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
