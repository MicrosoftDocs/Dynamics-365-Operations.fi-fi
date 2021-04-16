---
title: Puolivuotiskauden poistomenetelmä -metodologia
description: Tässä ohjeaiheessa kuvataan menetelmä, jota käyttöomaisuus käyttää poiston laskennassa puolivuotisen sopimuksen avulla. Se laskee kuuden kuukauden poiston käyttöomaisuuserän ensimmäisen ja viimeisen vuoden huollon aikana.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d0e33128c37e970ebf5af87bd601ae30aef96952
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818580"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="afade-103">Puolivuotiskauden poistomenetelmä -metodologia</span><span class="sxs-lookup"><span data-stu-id="afade-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="afade-104">Tässä ohjeaiheessa kuvaillaan menetelmää, jota käytetään käyttöomaisuudessa laskettaessa poistot puolivuotisen sopimuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="afade-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="afade-105">Puolivuotinen sopimus laskee kuuden kuukauden poiston käyttöomaisuuserän ensimmäisen ja viimeisen vuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="afade-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="afade-106">Lisätietoja poistomenetelmistä kohdassa [Poistomenetelmät ja -käytännöt](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="afade-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="afade-107">Kun käytät kuuden kuukauden poistomenetelmää, järjestelmä käyttää hankintavuotta tai vuotta, jolloin käyttö omaisuuserä on otettu käyttöön, laskee sen jälkeen viiden vuoden poiston kyseiselle vuodelle ja lisää summaan kuusi kuukautta.</span><span class="sxs-lookup"><span data-stu-id="afade-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="afade-108">Tämän prosessin havainnollistamiseksi on otettava huomioon käyttöomaisuus, jonka hankintahinta on 50 000 ja joka on otettu käyttöön vuoden 2020 huhtikuussa.</span><span class="sxs-lookup"><span data-stu-id="afade-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="afade-109">Oletetaan myös, että käyttöomaisuuserän käyttöikä on viisi vuotta.</span><span class="sxs-lookup"><span data-stu-id="afade-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="afade-110">Ensimmäinen huoltovuosi päättyy joulu kuussa 2020, mikä tarkoittaa, että käyttöomaisuuserän viiden vuoden käyttöikä päättyy vuoden 2024 joulukuussa.</span><span class="sxs-lookup"><span data-stu-id="afade-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="afade-111">Puolen vuoden poistomenetelmä lisää käyttöomaisuuserän käyttöikään kuusi kuukautta, mikä tarkoittaa, että sen käyttöikä päättyy vuoden 2025 kesäkuussa.</span><span class="sxs-lookup"><span data-stu-id="afade-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="afade-112">Vuosittainen poisto 50 000/5 = 10 000 kuukauden poisto 10 000/12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="afade-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="afade-113">Ensimmäisen vuoden poisto 10 000/2 = 5 000 ja sitä seuraava kuukausittainen poisto 5 000/9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="afade-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="afade-114">[![Puolen vuoden poistomenetelmän poistoaikataulu](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="afade-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="afade-115">Puolivuotisen sopimuksen lisäämät laajennetut poistokaudet lisäävät poistojen täsmällisempää jakautumista.</span><span class="sxs-lookup"><span data-stu-id="afade-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="afade-116">Kuuden kuukauden menetelmä edustaa poistokuluja tasaisemmin. Se on hyödyllinen tuloslaskelman raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="afade-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]