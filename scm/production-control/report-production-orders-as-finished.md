---
title: Tuotantotilausten ilmoittaminen valmiiksi
description: "Valmiiksi ilmoittaminen tapahtuu tuotantovaiheessa. Tässä vaiheessa valmis tuote raportoidaan ja siirretään tuotantotilauksesta varastoon."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8adcbcc2157058151c26179eb2eb925b0092d2d
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="70d40-104">Tuotantotilausten ilmoittaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="70d40-104">Report production orders as finished</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="70d40-105">Valmiiksi ilmoittaminen tapahtuu tuotantovaiheessa.</span><span class="sxs-lookup"><span data-stu-id="70d40-105">Report as finished is a production stage.</span></span> <span data-ttu-id="70d40-106">Tässä vaiheessa valmis tuote raportoidaan ja siirretään tuotantotilauksesta varastoon.</span><span class="sxs-lookup"><span data-stu-id="70d40-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="70d40-107">Kun tuotantotilaukseen kuuluvien valmiiden tavaroiden määrä ilmoitetaan valmiiksi, ne päivitetään käytettäviksi varastossa.</span><span class="sxs-lookup"><span data-stu-id="70d40-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="70d40-108">Osittainen määrä alunperin suunnitellusta tilausmäärästä voidaan ilmoittaa valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="70d40-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="70d40-109">Määrien valmiiksi ilmoittamisen yhteydessä on myös mahdollista ilmoittaa virhemäärät liittyvällä virhesyyllä.</span><span class="sxs-lookup"><span data-stu-id="70d40-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="70d40-110">Kun tuotantotilauksen tilaksi päivitetään Ilmoitettu valmiiksi, tuotantotilaukselle ei raportoida enempää määriä.</span><span class="sxs-lookup"><span data-stu-id="70d40-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="70d40-111">Myös seuraavat ominaisuudet liittyvät **Ilmoitettu valmiiksi** -prosessiin:</span><span class="sxs-lookup"><span data-stu-id="70d40-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="70d40-112">Voit määrittää raaka-aineiden ja ajan kulutuksen suhteessa ilmoitettuun määrään (jälkipoisto)</span><span class="sxs-lookup"><span data-stu-id="70d40-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="70d40-113">Nimikkeille, joiden käyttö on mahdollista varastoinnin prosesseissa, voi luoda poispanotyöt.</span><span class="sxs-lookup"><span data-stu-id="70d40-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="70d40-114">Valmiiden tavaroiden suunnitellun tai vakiokustannusarvon voi määrittää raportoitavaksi kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="70d40-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="70d40-115">Ilmoitetulle määrälle voidaan luoda laatutilaus, laatuliitoksen määritykseen perustuen.</span><span class="sxs-lookup"><span data-stu-id="70d40-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="70d40-116">Määrä ilmoitetaan tuotossijaintiin.</span><span class="sxs-lookup"><span data-stu-id="70d40-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="70d40-117">Sen jälkeen luodaan varastotyön, jossa määrä siirretään tuotossijainnista lopulliseen kohteeseen, joka määritellään poispanotyön sijaintidirektiivissä.</span><span class="sxs-lookup"><span data-stu-id="70d40-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="70d40-118">Laatutilauksen voi luoda, kun tuotantotilaus ilmoitetaan valmiiksi, jos sille on asetettu laatuliitos.</span><span class="sxs-lookup"><span data-stu-id="70d40-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="70d40-119">Tuotantotilauksen asettaminen Ilmoitettu valmiiksi -tilaan</span><span class="sxs-lookup"><span data-stu-id="70d40-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="70d40-120">Voit asettaa tuotantotilauksen tilaksi **Ilmoitettu valmiiksi** normaalin tuotantotilauksen päivitystoiminnon avulla, reititys- ja työkorttikirjauskansioiden avulla tai **Ilmoita valmiiksi** -kirjauskansion avulla.</span><span class="sxs-lookup"><span data-stu-id="70d40-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="70d40-121">Voit myös päivittää vaiheen **Ilmoitettu valmiiksi** -tilaan työkortinpäätteen ja työkorttilaitteen sivuilta, kun ilmoitat tuotantotilauksen viimeisen työn tiedot.</span><span class="sxs-lookup"><span data-stu-id="70d40-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="70d40-122">Viimeiseksi, voit ottaa **Ilmoita valmiiksi** -asetuksen käyttöön prosessina varaston käsipäätelaiteratkaisulle.</span><span class="sxs-lookup"><span data-stu-id="70d40-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




