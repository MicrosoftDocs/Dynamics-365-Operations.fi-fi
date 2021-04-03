---
title: Taloushallinnon raportointi
description: Talousraportoinnin avulla rahoitus- ja liiketoiminta-asiantuntijat voivat luoda ja ylläpitää raportteja sekä ottaa niitä käyttöön ja tarkastella niitä.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b6682295aa53acd5d3d6964c56ff7bcfcd59379d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568796"
---
# <a name="financial-reporting"></a><span data-ttu-id="bad9a-103">Taloushallinnan raportointi</span><span class="sxs-lookup"><span data-stu-id="bad9a-103">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bad9a-104">Sovelluksen talousraportoinnilla rahoitus- ja liiketoiminta-asiantuntijat voivat luoda ja ylläpitää raportteja sekä ottaa niitä käyttöön ja tarkastella niitä.</span><span class="sxs-lookup"><span data-stu-id="bad9a-104">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="bad9a-105">Koska perinteisen raportoinnin rajoitukset eivät päde, voit suunnitella tehokkaasti erilaisia raportteja.</span><span class="sxs-lookup"><span data-stu-id="bad9a-105">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="bad9a-106">Dimensiotuki sisältyy talousraportointiin.</span><span class="sxs-lookup"><span data-stu-id="bad9a-106">Financial reporting includes dimension support.</span></span> <span data-ttu-id="bad9a-107">Niinpä tilisegmentit tai -dimensiot ovat heti käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bad9a-107">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="bad9a-108">Lisätyökaluja tai -määrityksiä ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="bad9a-108">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="bad9a-109">Taloushallinnon raportoinnin asetukset</span><span class="sxs-lookup"><span data-stu-id="bad9a-109">Financial reporting setup</span></span>
<span data-ttu-id="bad9a-110">**Taloushallinnon raportoinnin asetukset** -sivulla on järjestelmän kaikkien taloushallinnon dimensioiden luettelo.</span><span class="sxs-lookup"><span data-stu-id="bad9a-110">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="bad9a-111">**Kirjanpito** \> **Kirjanpidon asetukset** \> **Taloushallinnon raportoinnin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="bad9a-111">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="bad9a-112">**Taloushallinnon raportoinnin asetukset** -sivulla on kaksi osaa, jotka määrittävät raportin tiedot taloushallinnon raportoinnissa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="bad9a-112">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="bad9a-113">**Dimensiot-välilehti** – Yrityksillä on käytössä erilaisia dimensioita ja tilirakenteita. Tämän vuoksi raporttien kaikkien taloushallinnon dimensioiden tarkastelujärjestystä ei voi määrittää.</span><span class="sxs-lookup"><span data-stu-id="bad9a-113">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="bad9a-114">Tällä sivulla voit määrittää järjestyksen, jossa taloushallinnon dimensiot näkyvät, kun raportti muodostetaan ja kun sitä tarkastellaan talousraportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="bad9a-114">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="bad9a-115">**Määritteet-välilehdessä** voit määrittää, käytetäänkö **toimittajia** ja **asiakkaita** määritteinä suodatuksessa ja raportin rakenteessa.</span><span class="sxs-lookup"><span data-stu-id="bad9a-115">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="bad9a-116">Toimittajan ja asiakkaan raportoinnista tulee arvokasta vain, jos et syötä useita toimittajia tai asiakkaita yhteen tositteeseen tapahtumien kirjaamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="bad9a-116">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="bad9a-117">Toimittajan ja/tai asiakkaan valitseminen pidentää integrointiin kuluvaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="bad9a-117">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="bad9a-118">Talousraportoinnin osat</span><span class="sxs-lookup"><span data-stu-id="bad9a-118">Financial reporting components</span></span>
<span data-ttu-id="bad9a-119">Raporttien luominen, tarkasteleminen ja ajoittaminen on helppoa seuraavien talousraportoinnin osien avulla.</span><span class="sxs-lookup"><span data-stu-id="bad9a-119">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="bad9a-120">Komponentti</span><span class="sxs-lookup"><span data-stu-id="bad9a-120">Component</span></span>        | <span data-ttu-id="bad9a-121">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="bad9a-121">Functions</span></span> | <span data-ttu-id="bad9a-122">Lisätiedot</span><span class="sxs-lookup"><span data-stu-id="bad9a-122">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="bad9a-123">Report Designer</span><span class="sxs-lookup"><span data-stu-id="bad9a-123">Report Designer</span></span>  | <span data-ttu-id="bad9a-124">Luo raportin rakenneosia, joita yhdistämällä voidaan määrittää ja luoda raportti.</span><span class="sxs-lookup"><span data-stu-id="bad9a-124">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="bad9a-125">Ohjattu raportin luominen ohjaa kokemattomampia käyttäjiä suunnitteluprosessissa.</span><span class="sxs-lookup"><span data-stu-id="bad9a-125">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="bad9a-126">Kokeneet käyttäjät voivat luoda tarvittaessa uusia raportin rakenneosia tai muokata aiemmin luotuja rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="bad9a-126">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="bad9a-127">Raportin aikataulut</span><span class="sxs-lookup"><span data-stu-id="bad9a-127">Report schedules</span></span> | <span data-ttu-id="bad9a-128">Ajoita yksi raportti tai raporttiryhmä siten, että se luodaan säännöllisesti.</span><span class="sxs-lookup"><span data-stu-id="bad9a-128">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="bad9a-129">Raporttien luonti</span><span class="sxs-lookup"><span data-stu-id="bad9a-129">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="bad9a-130">Ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="bad9a-130">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="bad9a-131">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="bad9a-131">Feature</span></span></th>
<th><span data-ttu-id="bad9a-132">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="bad9a-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bad9a-133">Raportin suunnitteluohjelman joustavuus</span><span class="sxs-lookup"><span data-stu-id="bad9a-133">Report design flexibility</span></span></td>
<td><span data-ttu-id="bad9a-134">Report Designerissa on seuraavat raportin suunnittelussa käytettävät raportointivaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="bad9a-134">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="bad9a-135">Tallenna dimensioyhdistelmät ja käytä dimensioista useissa raporteissa.</span><span class="sxs-lookup"><span data-stu-id="bad9a-135">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="bad9a-136">dimension kuvausten muotoilun ja näyttämisen hallinta</span><span class="sxs-lookup"><span data-stu-id="bad9a-136">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="bad9a-137">raportin rakenneosista pois jätettyjen tilien tai dimensioiden tunnistaminen</span><span class="sxs-lookup"><span data-stu-id="bad9a-137">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="bad9a-138">juoksevien ennusteiden otsikoiden muotoileminen.</span><span class="sxs-lookup"><span data-stu-id="bad9a-138">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="bad9a-139">Talousraporttiyhteistyö</span><span class="sxs-lookup"><span data-stu-id="bad9a-139">Financial report collaboration</span></span></td>
<td><span data-ttu-id="bad9a-140">Raportteja voi luoda ja jakaa seuraavien ominaisuuksien avulla.</span><span class="sxs-lookup"><span data-stu-id="bad9a-140">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="bad9a-141">Ajoita raportit niin, että luodaan automaattisesti päivittäin, viikoittain, kuukausittain tai vuosittain.</span><span class="sxs-lookup"><span data-stu-id="bad9a-141">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="bad9a-142">Vie vain luku -muodossa oleva XPS-muoto, sillä se parantaa asiakirjan suojausta digitaalisten allekirjoitusten avulla.</span><span class="sxs-lookup"><span data-stu-id="bad9a-142">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="bad9a-143">Vie Microsoft Excelin laskentataulukkoon.</span><span class="sxs-lookup"><span data-stu-id="bad9a-143">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="bad9a-144">Voit jakaa raportteja luomalla raporttien linkkejä sisältäviä sähköpostiviestejä.</span><span class="sxs-lookup"><span data-stu-id="bad9a-144">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="bad9a-145">Vuorovaikutteisen raportin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="bad9a-145">Interactive report viewing</span></span></td>
<td><span data-ttu-id="bad9a-146">Vuorovaikutteisten ominaisuuksien avulla voi suorittaa seuraavia tehtäviä:</span><span class="sxs-lookup"><span data-stu-id="bad9a-146">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="bad9a-147">Vaihda tarkastelemasi raportin päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="bad9a-147">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="bad9a-148">Vaihda tarkastelemasi raportin valuutta.</span><span class="sxs-lookup"><span data-stu-id="bad9a-148">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="bad9a-149">Näytä raportti joko yhteenvetonäkymässä tai yksityiskohtaisessa näkymässä.</span><span class="sxs-lookup"><span data-stu-id="bad9a-149">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="bad9a-150">Lisää dimensiosuodattimia rajoittamaan raportin sisältö tiettyyn dimensioon tai dimensioyhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="bad9a-150">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="bad9a-151">Lisää määritesuodattimia rajoittamaan raportin sisältö tiettyyn määritteeseen tai määriteyhdistelmään.</span><span class="sxs-lookup"><span data-stu-id="bad9a-151">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="bad9a-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bad9a-152">Additional resources</span></span>
[<span data-ttu-id="bad9a-153">Raporttien luonti</span><span class="sxs-lookup"><span data-stu-id="bad9a-153">Generate financial reports</span></span>](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]