---
title: Alareskontran siirto pääkirjanpitoon
description: Tässä ohjeaiheessa kuvataan, miten Microsoft Dynamics 365 Finance voi käsitellä kirjanpidon alakirjanpitoon liittyviä siirtoprosesseja.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: aec68b9389ee2ef28e8119087392ac5f18ec5dd2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204782"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="04996-103">Alareskontran siirto pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="04996-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04996-104">Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Finance -ominaisuuksia, jotka liittyvät alareskontran kirjauskansiomerkintöjen erien siirtämisen sääntöihin.</span><span class="sxs-lookup"><span data-stu-id="04996-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="04996-105">Versioon 8.1 tehtiin muutoksia, joiden avulla voitiin siirtää sääntöjä. Tämä syrjäytti **Synkroninen**-vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="04996-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="04996-106">Lisätietoja on kohdassa [Finance and Operationsin poistetut tai vanhentuneet ominaisuudet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="04996-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="04996-107">Alireskontraerien siirtoon on käytettävissä seuraavat vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="04996-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="04996-108">Asynkroninen – Tämä vaihtoehto ajoittaa välittömästi alakirjanpidon kirjanpitomerkintöjen siirron kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="04996-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="04996-109">Kirjanpidon tosite kirjataan heti, kun resurssit ovat vapaana käsittelemään tätä pyyntöä palvelimessa.</span><span class="sxs-lookup"><span data-stu-id="04996-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="04996-110">Ajoitettu erä – Tämä vaihtoehto lisää kirjanpidon käsittelyjonoon siirrettävät alareskontran tapahtumat, joissa tapahtumat käsitellään tilauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="04996-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="04996-111">Kirjanpidon tosite kirjataan ajoitettuna aikana, jos resurssit ovat vapaana käsittelemään tätä erätyötä palvelimessa.</span><span class="sxs-lookup"><span data-stu-id="04996-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="04996-112">Versioon 10.0.8 tehtiin parannuksia, jotka parantavat Asynkroninen-vaihtoehdon suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="04996-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="04996-113">Tämä toiminto on otettu käyttöön ominaisuuden nimen **alareskontran siirrossa kirjanpidon suorituskyvyn optimointiin**.</span><span class="sxs-lookup"><span data-stu-id="04996-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="04996-114">Tämä toiminto tehostaa tietojen siirtämistä alareskontrasta pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="04996-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="04996-115">Se mahdollistaa prosessin tehokkuuden, ja se ryhmittelee yhdessä pienempien tapahtumien joukon siirrettäväksi.</span><span class="sxs-lookup"><span data-stu-id="04996-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="04996-116">Tämä mahdollistaa eräpalvelimen tehokkaamman käytön.</span><span class="sxs-lookup"><span data-stu-id="04996-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="04996-117">Tämä toiminto edellyttää, että eräpalvelin on määritetty, verkossa ja toimiva, jotta asynkroninen siirtovaihtoehto toimisi.</span><span class="sxs-lookup"><span data-stu-id="04996-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]