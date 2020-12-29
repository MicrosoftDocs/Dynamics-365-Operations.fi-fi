---
title: Saapuvien varastotoimintojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645969"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="5f498-103">Saapuvien varastotoimintojen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="5f498-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f498-104">Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="5f498-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="5f498-105">Seuraava virhesanoma avautui: Laatutilaus %1 on luotu.</span><span class="sxs-lookup"><span data-stu-id="5f498-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="5f498-106">Klusteriprofiilia ei löytynyt. Tarkista konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="5f498-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f498-107">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="5f498-107">Issue description</span></span>

<span data-ttu-id="5f498-108">Tämä virhesanoma liittyy vastaanottoprosessiin, jossa laadunhallinta on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="5f498-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="5f498-109">Ympäristön määritysten mukaan virhesanoman luovan tapahtuman lisätiedot voivat auttaa korjaamaan ongelman.</span><span class="sxs-lookup"><span data-stu-id="5f498-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f498-110">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5f498-110">Issue resolution</span></span>

<span data-ttu-id="5f498-111">Tarkista ensimmäiseksi [klusterikeräilyn](set-up-cluster-picking.md) määritys ja varmista, että klusteriprofiilit on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="5f498-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="5f498-112">Et voi käyttää mobiililaitteen klusterikeräilyn valikkokohdetta, ellei klusteriprofiileja ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="5f498-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="5f498-113">Ympäristön mukaan on ehkä tarkistettava myös liittyvät määritykset.</span><span class="sxs-lookup"><span data-stu-id="5f498-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="5f498-114">Yhdistelmärekisterikilven vastaanottoa ei voi käyttää muussa kuin hyvityksen jakelukoodissa.</span><span class="sxs-lookup"><span data-stu-id="5f498-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f498-115">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="5f498-115">Issue description</span></span>

<span data-ttu-id="5f498-116">Kun jakelukoodin **Toiminto**-kentän määrityksenä on *Hyvitys* tai *Hävikki*, voit käyttää [Yhdistelmärekisterikilven vastaanotto](mixed-license-plate-receiving.md) -valikkovaihtoehtoa palautettujen nimikkeiden käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="5f498-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f498-117">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5f498-117">Issue resolution</span></span>

<span data-ttu-id="5f498-118">Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus.</span><span class="sxs-lookup"><span data-stu-id="5f498-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="5f498-119">Tällä hetkellä yhdistelmärekisterikilven vastaanotossa tuetaan vain [jakelukoodeja](../service-management/set-up-disposition-codes.md), joissa **Toiminto**-kentän asetuksena on *Hyvitys* tai *Hävikki*.</span><span class="sxs-lookup"><span data-stu-id="5f498-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="5f498-120">Kun kausittainen tuotteen vastaanottojen päivitystehtävä suoritetaan, vahvistamattomat ostotilaukset vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="5f498-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5f498-121">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="5f498-121">Issue description</span></span>

<span data-ttu-id="5f498-122">Kun olet suorittanut kausittaisen *Päivitä tuotteen vastaanotot* -tehtävän, järjestelmä vahvistaa automaattisesti vahvistamattomat ostotilaukset, joiden varastotapahtuman tila on *Rekisteröity*.</span><span class="sxs-lookup"><span data-stu-id="5f498-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5f498-123">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="5f498-123">Issue resolution</span></span>

<span data-ttu-id="5f498-124">Uusi saapuvan kuorman käsittelyominaisuus *Kuormamäärien ylivastaanottaminen* korjaa tämän ongelman.</span><span class="sxs-lookup"><span data-stu-id="5f498-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="5f498-125">Ota tämä ominaisuus käyttöön siirtymällä [ominaisuuksien hallintaan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ottamalla seuraavat ominaisuudet käyttöön (alla olevassa järjestyksessä):</span><span class="sxs-lookup"><span data-stu-id="5f498-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="5f498-126">Liitä ostotilauksen varastotapahtumat kuorman kanssa</span><span class="sxs-lookup"><span data-stu-id="5f498-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="5f498-127">Kuormamääriä vastaanotettu liikaa</span><span class="sxs-lookup"><span data-stu-id="5f498-127">Over receipt of load quantities</span></span>

<span data-ttu-id="5f498-128">Lisätietoja on kohdassa [Kirjattujen tuotemäärien kirjaaminen ostotilauksiin](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="5f498-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>
