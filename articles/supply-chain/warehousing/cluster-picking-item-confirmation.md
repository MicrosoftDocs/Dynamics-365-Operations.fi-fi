---
title: Tuotteen vahvistus klusterikeräilyä varten
description: Tässä ohjeaiheessa käsitellään nimikkeen tarkistusta yhdessä klusterikeräilyn kanssa.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8f81d760e8c181891aeba92834577e8869fbdd8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001121"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="613ea-103">Tuotteen vahvistus klusterikeräilyä varten</span><span class="sxs-lookup"><span data-stu-id="613ea-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="613ea-104">Klusterikeräilyssä voi kerätä usean tilauksen nimikkeitä samalla kertaa.</span><span class="sxs-lookup"><span data-stu-id="613ea-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="613ea-105">Kun klusterikeräily on käytössä, nimikkeen vahvistaminen on ehdottoman tärkeää, jotta klustereihin lisättävät nimikkeet voidaan tarkistaa.</span><span class="sxs-lookup"><span data-stu-id="613ea-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="613ea-106">Voit tarkistaa klusterikeräilyn nimikkeet klusterikeräilyn aikana.</span><span class="sxs-lookup"><span data-stu-id="613ea-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="613ea-107">Käyttö</span><span class="sxs-lookup"><span data-stu-id="613ea-107">Where it applies</span></span>

<span data-ttu-id="613ea-108">Klusterikeräilyn nimiketarkistus toimii samalla tavalla kuin nimikkeen tarkistaminen ei-klusterikeräilyprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="613ea-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="613ea-109">Määritys perustuu tuotteen viivakoodin asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="613ea-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="613ea-110">Nimiketarkistuksen määrittäminen klusterikeräilyssä</span><span class="sxs-lookup"><span data-stu-id="613ea-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="613ea-111">Avaa mobiililaitteen valikossa työn vahvistuksen määrityslomake: **Varastonhallinta** > **Varastonhallinta** > **Asetukset** > **Mobiililaite** > **Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="613ea-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="613ea-112">Avaa mobiililaitteen valikossa **Työn vahvistusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="613ea-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="613ea-113">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="613ea-113">Option</span></span>        |                                    <span data-ttu-id="613ea-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="613ea-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="613ea-115">Tuotteen vahvistus</span><span class="sxs-lookup"><span data-stu-id="613ea-115">Product confirmation</span></span> | <span data-ttu-id="613ea-116">Voit skannattaessa tarkistaa kunkin varastokappaleen mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="613ea-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |
