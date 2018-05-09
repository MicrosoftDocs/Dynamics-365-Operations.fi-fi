---
title: "Toimittajan laskujen ja laskujen hyväksynnän kirjauskansioiden oletusvastatilit"
description: "Tämän ohjeaiheen avulla voit päättää, mihin oletustilit ja vastatilit määritetään laskujen kirjauskansioissa."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 45a066ff5b884e8cc78b0fc16d1f1eab9cb0f5f3
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="ef986-103">Toimittajan laskujen ja laskujen hyväksynnän kirjauskansioiden oletusvastatilit</span><span class="sxs-lookup"><span data-stu-id="ef986-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef986-104">Oletusvastatilejä käytetään seuraavilla toimittajan laskun kirjauskansion sivuilla:</span><span class="sxs-lookup"><span data-stu-id="ef986-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="ef986-105">Laskukirjauskansio</span><span class="sxs-lookup"><span data-stu-id="ef986-105">Invoice journal</span></span>
-   <span data-ttu-id="ef986-106">Hyväksyttyjen laskujen kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="ef986-106">Invoice approval journal</span></span>

<span data-ttu-id="ef986-107">Seuraavan taulukon avulla voit päättää, mihin oletustilit ja vastatilit määritetään laskujen kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="ef986-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef986-108">Määritä oletustilit täällä</span><span class="sxs-lookup"><span data-stu-id="ef986-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="ef986-109">Missä oletustilit tarjotaan</span><span class="sxs-lookup"><span data-stu-id="ef986-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="ef986-110">Tämän asetuksen vaikutus käsittelyyn</span><span class="sxs-lookup"><span data-stu-id="ef986-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="ef986-111">Milloin asetusta tulisi käyttää</span><span class="sxs-lookup"><span data-stu-id="ef986-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef986-112"><strong>Toimittajaryhmä</strong> – Määritä toimittajaryhmien oletusvastatilit <strong>Oletustilin määritys</strong> -sivulla, jonka voit avata <strong>Toimittajaryhmät</strong>-sivulta.</span><span class="sxs-lookup"><span data-stu-id="ef986-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="ef986-113">Toimittajatili</span><span class="sxs-lookup"><span data-stu-id="ef986-113">Vendor account</span></span></li>
<li><span data-ttu-id="ef986-114">Kirjauskansioviennit toimittajatileille toimittajaryhmässä, jos toimittajatileille ei ole määritetty oletustilejä</span><span class="sxs-lookup"><span data-stu-id="ef986-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="ef986-115">Toimittajaryhmien oletusvastatilit näytetään toimittajien oletusvastatileinä <strong>Oletustilin määritys</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ef986-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="ef986-116">Voit avata sivun <strong>Kaikki toimittajat</strong> -luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="ef986-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="ef986-117">Käytä tätä vaihtoehtoa, jos yleensä maksat samantyyppisistä asioista samoille toimittajaryhmille ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="ef986-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef986-118"><strong>Toimittajan tili</strong> – Määritä toimittajan tilien oletusvastatilit <strong>Oletustilin määritys</strong> -sivulla, jonka voit avata <strong>Toimittajat</strong>-sivulta.</span><span class="sxs-lookup"><span data-stu-id="ef986-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="ef986-119">Kirjauskansioviennit toimittajatilille</span><span class="sxs-lookup"><span data-stu-id="ef986-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="ef986-120">Toimittajatilien oletusvastatilit näytetään oletusvastatileinä toimittajatilin kirjauskansiomerkinnöille.</span><span class="sxs-lookup"><span data-stu-id="ef986-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="ef986-121">Käytä tätä vaihtoehtoa, jos yleensä maksat samantyyppisistä asioista samoille toimittajille ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="ef986-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef986-122"><strong>Kirjauskansioiden nimet</strong> – Määritä kirjauskansioiden oletusvastatilit <strong>Kirjauskansioiden nimet</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ef986-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="ef986-123">Valitse <strong>Kiinteä vastatili</strong> -asetus.</span><span class="sxs-lookup"><span data-stu-id="ef986-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="ef986-124">Huomaa, että et voi määrittää kirjauskansioiden nimille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef986-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="ef986-125">Kirjauskansion otsikko, joka käyttää kirjauskansion nimeä.</span><span class="sxs-lookup"><span data-stu-id="ef986-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="ef986-126">Kirjauskansioviennit kirjauskansionimeä käyttävissä kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="ef986-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="ef986-127">Jos <strong>Kiinteä vastatili</strong> -valintaruutu on valittuna <strong>Kirjauskansioiden nimet -sivulla</strong>, kirjauskansion nimen vastatili ohittaa toimittajan tai toimittajaryhmän oletusvastatilin.</span><span class="sxs-lookup"><span data-stu-id="ef986-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="ef986-128">Käytä tätä vaihtoehtoa kirjauskansioiden määrittämiseen tietyille kuluille tai kustannuksille, jotka veloitetaan tietyiltä tileiltä siitä riippumatta, kuka toimittaja on tai mihin toimittajaryhmään toimittaja kuuluu.</span><span class="sxs-lookup"><span data-stu-id="ef986-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef986-129"><strong>Kirjauskansioiden nimet</strong> – Määritä kirjauskansioiden oletusvastatilit <strong>Kirjauskansioiden nimet</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ef986-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="ef986-130">Poista <strong>Kiinteä vastatili</strong> -asetus.</span><span class="sxs-lookup"><span data-stu-id="ef986-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="ef986-131">Huomaa, että et voi määrittää kirjauskansioiden nimille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef986-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="ef986-132">Kirjauskansion otsikko</span><span class="sxs-lookup"><span data-stu-id="ef986-132">Journal header</span></span></li>
<li><span data-ttu-id="ef986-133">Kirjauskansioviennit kirjauskansionimeä käyttävissä kirjauskansioissa.</span><span class="sxs-lookup"><span data-stu-id="ef986-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="ef986-134">Näitä oletusarvoisia merkintöjä käytetään kirjauskansion otsikkosivuilla ja kirjauskansion otsikkosivun vastatiliä käytetään oletusmerkintänä kirjauskansion tositesivuilla.</span><span class="sxs-lookup"><span data-stu-id="ef986-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="ef986-135"><strong>Kirjauskansioiden nimet</strong> -lomakkeen oletustilejä käytetään vain, jos toimittajan tilille ei ole määritetty oletustilejä.</span><span class="sxs-lookup"><span data-stu-id="ef986-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="ef986-136">Tätä vaihtoehtoa käyttämällä voidaan määrittää käytettävät oletustilit, kun toimittajan oletusvastatiliä ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="ef986-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef986-137"><strong>Kirjauskansion otsikko</strong> – Määritä kirjauskansion oletusvastatili käytettäväksi oletusmerkintänä kirjauskansion tositesivuilla.</span><span class="sxs-lookup"><span data-stu-id="ef986-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="ef986-138">Huomaa, että et voi määrittää kirjauskansioiden otsikoille oletusvastatilejä, jos kirjauskansioiden nimien kirjauskansiotyyppi on <strong>Laskurekisteri</strong> tai <strong>Hyväksyntä</strong>.</span><span class="sxs-lookup"><span data-stu-id="ef986-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="ef986-139">Kirjauskansioviennit kirjauskansiossa</span><span class="sxs-lookup"><span data-stu-id="ef986-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="ef986-140">Kirjauskansion oletusvastatiliä käytetään oletusmerkintänä kirjauskansion tositesivuilla.</span><span class="sxs-lookup"><span data-stu-id="ef986-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="ef986-141">Tämän vaihtoehdon avulla voit nopeuttaa tietojen kirjaamista, jos useimmilla kirjauskansion kirjauksilla on sama vastatili.</span><span class="sxs-lookup"><span data-stu-id="ef986-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






