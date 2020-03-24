---
title: Asiakkaan luotonhallinta
description: Asiakkaan luotonhallinnan avulla voit hallita luottorajoja ja hallita myyntitilausten siirtymistä kirjausprosessissa luotujen luottosääntöjen perusteella.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e7d3325587d7cfc876e8f8c7b9207d44046ccd4
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124274"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="bcec6-103">Asiakkaan luotonhallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bcec6-103">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcec6-104">Asiakkaan luotonhallinnan avulla voit hallita luottorajoja ja hallita myyntitilausten siirtymistä kirjausprosessissa luotujen luottosääntöjen perusteella.</span><span class="sxs-lookup"><span data-stu-id="bcec6-104">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="bcec6-105">Luotonhallinnan käyttö voi sisältää osan tai kaikki seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="bcec6-105">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="bcec6-106">Lisätietoja asiakkaan luottokelpoisuudesta antavien luottomääritteiden päivittäminen</span><span class="sxs-lookup"><span data-stu-id="bcec6-106">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="bcec6-107">Luottorajojen luonti asiakkaille käyttämällä luottorajan oikaisuja</span><span class="sxs-lookup"><span data-stu-id="bcec6-107">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="bcec6-108">Väliaikaisten luottorajojen luonti asiakkaille käyttämällä luottorajan oikaisuja, kun luottorajaa halutaan nostaa tai laskea väliaikaisesti liiketoimintatarpeiden perusteella</span><span class="sxs-lookup"><span data-stu-id="bcec6-108">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="bcec6-109">Luottorajaan mahdollisesti vaikuttavien lisätietojen, kuten vakuuden tai takauksien, lisääminen</span><span class="sxs-lookup"><span data-stu-id="bcec6-109">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="bcec6-110">Asiakkaat yhteen liittävien asiakkaan luottoryhmien luominen siten, että ne voivat jakaa yhden luottorajan</span><span class="sxs-lookup"><span data-stu-id="bcec6-110">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="bcec6-111">Riskipisteiden määrittäminen asiakkaille ja näiden pistemäärien käyttäminen luomaan luottorajoja asiakkaille automaattisesti luottorajan oikaisujen avulla</span><span class="sxs-lookup"><span data-stu-id="bcec6-111">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="bcec6-112">Estosääntöjen luominen asettamaan tilaus pitoon jonkin kirjausprosessin aikana esimerkiksi seuraavien seikkojen perusteella: riski, maksuehdot, luottorajat, erääntyneet summat ja käytetyn luottorajan prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="bcec6-112">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="bcec6-113">Pidossa olevien myyntitilausluettelon hallinta, pitosyiden tarkastelu ja ongelmien ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="bcec6-113">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="bcec6-114">Myyntitilausten vapauttaminen ja niiden jatkaminen kirjausprosessin läpi</span><span class="sxs-lookup"><span data-stu-id="bcec6-114">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="bcec6-115">Työnkulun määrittäminen hallitsemaan luottorajan muutosten ja myyntitilausten vapauttamisen hyväksymistä</span><span class="sxs-lookup"><span data-stu-id="bcec6-115">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="bcec6-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bcec6-116">Additional resources</span></span>
--------
[<span data-ttu-id="bcec6-117">Asiakkaan luotonhallinnan parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bcec6-117">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="bcec6-118">Asiakkaan luotonhallinnan määritystiedot</span><span class="sxs-lookup"><span data-stu-id="bcec6-118">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="bcec6-119">Asiakkaan luotonhallintatietojen lisääminen</span><span class="sxs-lookup"><span data-stu-id="bcec6-119">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="bcec6-120">Asiakasluottoryhmät</span><span class="sxs-lookup"><span data-stu-id="bcec6-120">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="bcec6-121">Asiakkaan luottorajan oikaisut</span><span class="sxs-lookup"><span data-stu-id="bcec6-121">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="bcec6-122">Myyntitilausten luottorajapidot</span><span class="sxs-lookup"><span data-stu-id="bcec6-122">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="bcec6-123">Asiakkaan luotonhallinnan kausittaiset tehtävät</span><span class="sxs-lookup"><span data-stu-id="bcec6-123">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


