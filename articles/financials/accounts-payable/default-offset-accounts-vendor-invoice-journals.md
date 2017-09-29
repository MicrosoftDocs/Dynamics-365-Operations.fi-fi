---
title: "Toimittajan laskujen ja laskujen hyväksymisten kirjauskansioiden oletusvastatilit"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="af077-102">Toimittajan laskujen ja laskujen hyväksymisten kirjauskansioiden oletusvastatilit</span><span class="sxs-lookup"><span data-stu-id="af077-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="af077-103">Oletusvastatilejä käytetään seuraavilla toimittajan laskun kirjauskansion sivuilla:</span><span class="sxs-lookup"><span data-stu-id="af077-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="af077-104">Laskukirjauskansio</span><span class="sxs-lookup"><span data-stu-id="af077-104">Invoice journal</span></span>
-   <span data-ttu-id="af077-105">Hyväksyttyjen laskujen kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="af077-105">Invoice approval journal</span></span>

<span data-ttu-id="af077-106">Seuraavan taulukon avulla voit päättää, mihin oletustilit ja vastatilit määritetään laskujen kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="af077-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af077-107">Määritä oletustilit täällä</span><span class="sxs-lookup"><span data-stu-id="af077-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="af077-108">Missä oletustilit tarjotaan</span><span class="sxs-lookup"><span data-stu-id="af077-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="af077-109">Tämän asetuksen vaikutus käsittelyyn</span><span class="sxs-lookup"><span data-stu-id="af077-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="af077-110">Milloin asetusta tulisi käyttää</span><span class="sxs-lookup"><span data-stu-id="af077-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af077-111"><strong>Toimittajaryhmä</strong> – Määritä toimittajaryhmien oletusvastatilit <strong>Oletustilin määritys</strong> -sivulla, jonka voit avata <strong>Toimittajaryhmät</strong>-sivulta.</span><span class="sxs-lookup"><span data-stu-id="af077-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="af077-112">Toimittajatili</span><span class="sxs-lookup"><span data-stu-id="af077-112">Vendor account</span></span></li>
<li><span data-ttu-id="af077-113">Kirjauskansioviennit toimittajatileille toimittajaryhmässä, jos toimittajatileille ei ole määritetty oletustilejä</span><span class="sxs-lookup"><span data-stu-id="af077-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="af077-114">Toimittajaryhmien oletusvastatilit näytetään toimittajien oletusvastatileinä <strong>Oletustilin määritys</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="af077-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="af077-115">Voit avata sivun <strong>Kaikki toimittajat</strong> -luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="af077-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="af077-116">Käytä tätä vaihtoehtoa, jos yleensä maksat samantyyppisistä asioista samoille toimittajaryhmille ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="af077-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af077-117"><strong>Toimittajan tili</strong> – Määritä toimittajan tilien oletusvastatilit <strong>Oletustilin määritys</strong> -sivulla, jonka voit avata <strong>Toimittajat</strong>-sivulta.</span><span class="sxs-lookup"><span data-stu-id="af077-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="af077-118">Kirjauskansioviennit toimittajatilille</span><span class="sxs-lookup"><span data-stu-id="af077-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="af077-119">Toimittajatilien oletusvastatilit näytetään oletusvastatileinä toimittajatilin kirjauskansiomerkinnöille.</span><span class="sxs-lookup"><span data-stu-id="af077-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="af077-120">Käytä tätä vaihtoehtoa, jos yleensä maksat samantyyppisistä asioista samoille toimittajille ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="af077-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af077-121"><strong>Kirjauskansioiden nimet</strong> – Määritä kirjauskansioiden oletusvastatilit <strong>Kirjauskansioiden nimet</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="af077-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="af077-122">Valitse <strong>Kiinteä vastatili</strong> -asetus.</span><span class="sxs-lookup"><span data-stu-id="af077-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="af077-123">Huomaa, että et voi määrittää kirjauskansioiden nimille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</span><span class="sxs-lookup"><span data-stu-id="af077-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="af077-124">Kirjauskansion otsikko, joka käyttää kirjauskansion nimeä.</span><span class="sxs-lookup"><span data-stu-id="af077-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="af077-125">Kirjauskansioviennit kirjauskansionimeä käyttävissä kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="af077-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="af077-126">Jos <strong>Kiinteä vastatili</strong> -valintaruutu on valittuna <strong>Kirjauskansioiden nimet -sivulla</strong>, kirjauskansion nimen vastatili ohittaa toimittajan tai toimittajaryhmän oletusvastatilin.</span><span class="sxs-lookup"><span data-stu-id="af077-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="af077-127">Käytä tätä vaihtoehtoa kirjauskansioiden määrittämiseen tietyille kuluille tai kustannuksille, jotka veloitetaan tietyiltä tileiltä siitä riippumatta, kuka toimittaja on tai mihin toimittajaryhmään toimittaja kuuluu.</span><span class="sxs-lookup"><span data-stu-id="af077-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af077-128"><strong>Kirjauskansioiden nimet</strong> – Määritä kirjauskansioiden oletusvastatilit <strong>Kirjauskansioiden nimet</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="af077-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="af077-129">Poista <strong>Kiinteä vastatili</strong> -asetus.</span><span class="sxs-lookup"><span data-stu-id="af077-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="af077-130">Huomaa, että et voi määrittää kirjauskansioiden nimille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</span><span class="sxs-lookup"><span data-stu-id="af077-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="af077-131">Kirjauskansion otsikko</span><span class="sxs-lookup"><span data-stu-id="af077-131">Journal header</span></span></li>
<li><span data-ttu-id="af077-132">Kirjauskansioviennit kirjauskansionimeä käyttävissä kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="af077-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="af077-133">Näitä oletusarvoisia merkintöjä käytetään kirjauskansion otsikkosivuilla ja kirjauskansion otsikkosivun vastatiliä käytetään oletusmerkintänä kirjauskansion tositesivuilla.</span><span class="sxs-lookup"><span data-stu-id="af077-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="af077-134"><strong>Kirjauskansioiden nimet</strong> -lomakkeen oletustilejä käytetään vain, jos toimittajan tilille ei ole määritetty oletustilejä.</span><span class="sxs-lookup"><span data-stu-id="af077-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="af077-135">Tätä vaihtoehtoa käyttämällä voidaan määrittää käytettävät oletustilit, kun toimittajan oletusvastatiliä ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="af077-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af077-136"><strong>Kirjauskansion otsikko</strong> – Määritä kirjauskansion oletusvastatili käytettäväksi oletusmerkintänä kirjauskansion tositesivuilla.</span><span class="sxs-lookup"><span data-stu-id="af077-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="af077-137">Huomaa, että et voi määrittää kirjauskansioiden otsikoille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</span><span class="sxs-lookup"><span data-stu-id="af077-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="af077-138">Kirjauskansioviennit kirjauskansiossa</span><span class="sxs-lookup"><span data-stu-id="af077-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="af077-139">Kirjauskansion oletusvastatiliä käytetään oletusmerkintänä kirjauskansion tositesivuilla.</span><span class="sxs-lookup"><span data-stu-id="af077-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="af077-140">Tämän vaihtoehdon avulla voit nopeuttaa tietojen kirjaamista, jos useimmilla kirjauskansion kirjauksilla on sama vastatili.</span><span class="sxs-lookup"><span data-stu-id="af077-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






