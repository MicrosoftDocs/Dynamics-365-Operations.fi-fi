---
title: Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Commercesta.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335273"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="b3a15-103">Poistetut tai vanhentuneet Dynamics 365 Commerce -ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b3a15-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3a15-104">Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Commercesta.</span><span class="sxs-lookup"><span data-stu-id="b3a15-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="b3a15-105">*Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.</span><span class="sxs-lookup"><span data-stu-id="b3a15-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b3a15-106">*Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="b3a15-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b3a15-107">Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.</span><span class="sxs-lookup"><span data-stu-id="b3a15-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="b3a15-108">Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="b3a15-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="b3a15-109">Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="b3a15-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="b3a15-110">Commercen version 10.0.10 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b3a15-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="b3a15-111">Myyntipistetoiminto 803 - Keräys ja vastaanotto</span><span class="sxs-lookup"><span data-stu-id="b3a15-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b3a15-112">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="b3a15-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b3a15-113">Keräilyn ja vastaanoton toimintoja ollaan poistamassa, koska uusi uudelleensuunnittelu on käytössä.</span><span class="sxs-lookup"><span data-stu-id="b3a15-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="b3a15-114">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="b3a15-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b3a15-115">Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b3a15-115">Yes.</span></span> <span data-ttu-id="b3a15-116">Se korvataan kahdella uudella myyntipistetoiminnolla: saapuva työvaihe (804) ja lähtevä työvaihe (805).</span><span class="sxs-lookup"><span data-stu-id="b3a15-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="b3a15-117">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="b3a15-117">**Product areas affected**</span></span>         | <span data-ttu-id="b3a15-118">Myyntipiste (POS) -sovellus</span><span class="sxs-lookup"><span data-stu-id="b3a15-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="b3a15-119">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="b3a15-119">**Deployment option**</span></span>              | <span data-ttu-id="b3a15-120">Kaikki</span><span class="sxs-lookup"><span data-stu-id="b3a15-120">All</span></span> |
| <span data-ttu-id="b3a15-121">**Tila**</span><span class="sxs-lookup"><span data-stu-id="b3a15-121">**Status**</span></span>                         | <span data-ttu-id="b3a15-122">Vanhentunut: kun kyseessä on julkaisuversio 10.0.10, keräily- ja vastaanottotoiminto ei enää vastaanota uusia ominaisuuspäivityksiä.</span><span class="sxs-lookup"><span data-stu-id="b3a15-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="b3a15-123">Vain kriittiset ohjelmakorjaukset tehdään tämän toiminnon yhteydessä tulevissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="b3a15-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="b3a15-124">Kaikkia asiakkaita kannustetaan siirtymään uusiin [saapuviin työvaiheisiin](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ja [lähteviin toimintoihin](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), jotka ovat jatkossakin osa pitkän aikavälin tuotesuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="b3a15-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="b3a15-125">Commercen version 10.0.7 poistetut tai vanhentuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b3a15-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="b3a15-126">Commerce GetProductAvailabilities- ja GetAvailableInventoryNearby ohjelmointirajapintaliittymät</span><span class="sxs-lookup"><span data-stu-id="b3a15-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b3a15-127">**Poiston tai vanhentumisen syy**</span><span class="sxs-lookup"><span data-stu-id="b3a15-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b3a15-128">Uudet optimoidut ohjelmointirajapinnat on luotu korvaamaan GetProductAvailabilities- ja GetAvailableInventoryNearby-ohjelmointirajapinnat.</span><span class="sxs-lookup"><span data-stu-id="b3a15-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="b3a15-129">**Onko toinen ominaisuus korvannut?**</span><span class="sxs-lookup"><span data-stu-id="b3a15-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b3a15-130">Kyllä: sen tilalle tulee GetEstimatedAvailabilty ja GetEstimatedProductWarehouseAvailability -ohjelmointirajapinnat.</span><span class="sxs-lookup"><span data-stu-id="b3a15-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="b3a15-131">**Tuotealueet, joihin vaikutetaan**</span><span class="sxs-lookup"><span data-stu-id="b3a15-131">**Product areas affected**</span></span>         | <span data-ttu-id="b3a15-132">e-Commerce-sovellus-SDK</span><span class="sxs-lookup"><span data-stu-id="b3a15-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="b3a15-133">**Käytön asetukset**</span><span class="sxs-lookup"><span data-stu-id="b3a15-133">**Deployment option**</span></span>              | <span data-ttu-id="b3a15-134">Kaikki</span><span class="sxs-lookup"><span data-stu-id="b3a15-134">All</span></span> |
| <span data-ttu-id="b3a15-135">**Tila**</span><span class="sxs-lookup"><span data-stu-id="b3a15-135">**Status**</span></span>                         | <span data-ttu-id="b3a15-136">Vanhentunut: Julkaisuversiosta 10.0.7 alkaen kohteille GetProductAvailabilities ja GetAvailableInventoryNearby ei tehdä enää teknisiä investointeja.</span><span class="sxs-lookup"><span data-stu-id="b3a15-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="b3a15-137">Organisaatiot, jotka käyttävät näitä ohjelmointirajapintaliittymiä verkkokaupan käyttöönotoissa, on muunnettava uuteen GetEstimatedAvailabilty- ja GetEstimatedProductWarehouseAvailability-ohjelmointirajapintaliittymiin ja otettava käyttöön [Optimoitu tuotteen saatavuuden laskentaominaisuus](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="b3a15-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="b3a15-138">Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="b3a15-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="b3a15-139">Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b3a15-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
