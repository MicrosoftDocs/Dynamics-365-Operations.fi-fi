---
title: Osittaisten vapautusten ja osalähetysten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun osittaisia vapautuksia ja osittaisia lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 33323a8aed44cf19db6c2c937abcb09f7e05b6c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993942"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="71abd-103">Osittaisten vapautusten ja osalähetysten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="71abd-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71abd-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun osittaisia vapautuksia ja osittaisia lähetyksiä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="71abd-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="71abd-105">Myyntitilauksen vapautustilaksi jää Osittain vapautettu myös myyntitilauksen laskutuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="71abd-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="71abd-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="71abd-106">Issue description</span></span>

<span data-ttu-id="71abd-107">Myyntilaus on toimitustilaus, mutta ainakin yhdellä nimikkeellä on erilainen toimitustila.</span><span class="sxs-lookup"><span data-stu-id="71abd-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="71abd-108">Kun tilaus on laskutettu, sen vapautustila on edelleen *Osittain vapautettu*.</span><span class="sxs-lookup"><span data-stu-id="71abd-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="71abd-109">Esimerkiksi myyntitilauksessa on kaksi nimikettä: yksi toimitusta varten ja toinen noutoa varten.</span><span class="sxs-lookup"><span data-stu-id="71abd-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="71abd-110">Sekä toimitus että nouto ovat valmiita.</span><span class="sxs-lookup"><span data-stu-id="71abd-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="71abd-111">Tämän vuoksi molemmat rivit on laskutettu.</span><span class="sxs-lookup"><span data-stu-id="71abd-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="71abd-112">Vapautustilana on kuitenkin edelleen *Osittain vapautettu*, mikä on harhaanjohtavaa.</span><span class="sxs-lookup"><span data-stu-id="71abd-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="71abd-113">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="71abd-113">Issue resolution</span></span>

<span data-ttu-id="71abd-114">Vapautustila koskee vain tilausrivejä, joiden nimikkeissä varastonhallinta on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="71abd-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="71abd-115">Tämän vuoksi vapautustilaksi jää *Osittain vapautettu* tässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="71abd-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="71abd-116">Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus.</span><span class="sxs-lookup"><span data-stu-id="71abd-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="71abd-117">Laajennus voitaisiin lisätä pakkausluettelon ja laskutusprosessin osana päivittämään vapautustila.</span><span class="sxs-lookup"><span data-stu-id="71abd-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
