---
title: Toimittajan laskun automatisoinnin tulosten näyttäminen (esiversio)
description: Tässä ohjeaiheessa käsitellään niiden toimittajan laskujen tilan näyttämistä, jotka ovat automatisoidussa työnkulkuun lähettämisprosessissa.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec49a621e24b6373532497b499e8b9d45c9bed14
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022610"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="aa2c2-103">Toimittajan laskujen automaatiotulosten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="aa2c2-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa2c2-104">Tässä ohjeaiheessa käsitellään niiden toimittajan laskujen tilan näyttämistä, jotka ovat automatisoidussa työnkulkuun lähettämisprosessissa.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="aa2c2-105">Kunkin tuodun toimittajan laskun automatisoinnin historiatiedot säilytetään.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="aa2c2-106">Automatisoidun prosessin mukaan **Odottavat toimittajan laskut** -sivulla näkyy **Automatisoidun vastaanoton täsmäytyksen tila** - ja **Automatisoidun työnkulkuun lähettämisen tila** -arvot.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="aa2c2-107">Voit tarkastella tietoja ja päättää suunnitelmasta, joka keskittyy automatisointivaiheessa epäonnistuneisiin laskuihin.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="aa2c2-108">Sen jälkeen kun ongelma on korjattu, voit jatkaa tuotujen laskujen automatisointiprosessia.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="aa2c2-109">Ennen kuin lähetettyä laskua voi muokata, automatisoitu käsittely on keskeytettävä.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="aa2c2-110">Jos automatisoidussa työnkulkuun lähetysprosessissa oleva lasku on keskeytettävä, määritä **Sisällytä automatisoituun käsittelyyn** -kentän arvoksi **Ei** **Toimittajan laskut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="aa2c2-111">Automatisointia ei sitten suoriteta, ennen kuin **Sisällytä automatisoituun käsittelyyn** -arvoksi on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="aa2c2-112">Laskun lisäautomatisointi voidaan keskeyttää, jos se ei ole vielä työnkulkujärjestelmässä ja jos automatisoitu prosessi ei käytä sitä.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="aa2c2-113">Jos tuotu lasku on työnkulkuun lähettämisprosessissa, sen **Automatisoinnin tila** -arvon voi tarkistaa **Toimittajan laskut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="aa2c2-114">Seuraavat tiloja seurataan:</span><span class="sxs-lookup"><span data-stu-id="aa2c2-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="aa2c2-115">**Sisällytetty** – **Ostoreskontran parametrit** -sivulla määritetyt automatisoidut prosessit ovat käynnissä, mutta ne eivät ole vielä valmiita.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="aa2c2-116">**Keskeytetty** – **Ostoreskontran parametrit** -sivulla määritetyt automatisoidut prosessit on suoritettu, mutta ainakin yksi prosessin vaihe epäonnistui.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="aa2c2-117">**Keskeytetty** -tila on käytössä myös silloin, jos **Sisällytä automatisoituun käsittelyyn** -kentän arvo on **Ei**.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="aa2c2-118">Voit tarkastella epäonnistuneita vaiheita valitsemalla **Näytä viimeisimmät tulokset**.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="aa2c2-119">**Työnkulussa** – tuotu lasku on lähetetty työnkulkujärjestelmään joko automatisoidussa työnkulkuun lähettämisprosessissa tai manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="aa2c2-120">**Työnkulku valmis** – tuodun laskun työnkulkuprosessi on valmis.</span><span class="sxs-lookup"><span data-stu-id="aa2c2-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
