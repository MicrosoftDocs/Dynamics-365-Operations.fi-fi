---
title: Toimittajan laskun automatisoinnin tulosten näyttäminen (esiversio)
description: Tässä ohjeaiheessa käsitellään niiden toimittajan laskujen tilan näyttämistä, jotka ovat automatisoidussa työnkulkuun lähettämisprosessissa.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 872ec404da0cce41c4ea0f882a3fa8af56316ce3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837222"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="0a8f4-103">Toimittajan laskujen automaatiotulosten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="0a8f4-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a8f4-104">Tässä ohjeaiheessa käsitellään niiden toimittajan laskujen tilan näyttämistä, jotka ovat automatisoidussa työnkulkuun lähettämisprosessissa.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="0a8f4-105">Kunkin tuodun toimittajan laskun automatisoinnin historiatiedot säilytetään.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="0a8f4-106">Automatisoidun prosessin mukaan **Odottavat toimittajan laskut** -sivulla näkyy **Automatisoidun vastaanoton täsmäytyksen tila**- ja **Automatisoidun työnkulkuun lähettämisen tila** -arvot.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="0a8f4-107">Voit tarkastella tietoja ja päättää suunnitelmasta, joka keskittyy automatisointivaiheessa epäonnistuneisiin laskuihin.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="0a8f4-108">Sen jälkeen kun ongelma on korjattu, voit jatkaa tuotujen laskujen automatisointiprosessia.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="0a8f4-109">Ennen kuin lähetettyä laskua voi muokata, automatisoitu käsittely on keskeytettävä.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="0a8f4-110">Jos automatisoidussa työnkulkuun lähetysprosessissa oleva lasku on keskeytettävä, määritä **Sisällytä automatisoituun käsittelyyn** -kentän arvoksi **Ei** **Toimittajan laskut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="0a8f4-111">Automatisointia ei sitten suoriteta, ennen kuin **Sisällytä automatisoituun käsittelyyn** -arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="0a8f4-112">Laskun lisäautomatisointi voidaan keskeyttää, jos se ei ole vielä työnkulkujärjestelmässä ja jos automatisoitu prosessi ei käytä sitä.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="0a8f4-113">Jos tuotu lasku on työnkulkuun lähettämisprosessissa, sen **Automatisoinnin tila** -arvon voi tarkistaa **Toimittajan laskut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="0a8f4-114">Seuraavat tiloja seurataan:</span><span class="sxs-lookup"><span data-stu-id="0a8f4-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="0a8f4-115">**Sisällytetty** – **Ostoreskontran parametrit** -sivulla määritetyt automatisoidut prosessit ovat käynnissä, mutta ne eivät ole vielä valmiita.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="0a8f4-116">**Keskeytetty** – **Ostoreskontran parametrit** -sivulla määritetyt automatisoidut prosessit on suoritettu, mutta ainakin yksi prosessin vaihe epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="0a8f4-117">**Keskeytetty**-tila on käytössä myös silloin, jos **Sisällytä automatisoituun käsittelyyn** -kentän arvo on **Ei**.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="0a8f4-118">Voit tarkastella epäonnistuneita vaiheita valitsemalla **Näytä viimeisimmät tulokset**.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="0a8f4-119">**Työnkulussa** – tuotu lasku on lähetetty työnkulkujärjestelmään joko automatisoidussa työnkulkuun lähettämisprosessissa tai manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="0a8f4-120">**Työnkulku valmis** – tuodun laskun työnkulkuprosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="0a8f4-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]