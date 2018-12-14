---
title: Talentin raportointivaihtoehdot
description: "Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, kun asiakas haluaa mukauttaa Microsoft Dynamics 365 for Talent -raportteja tai luoda uusia raportteja."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="b2dff-103">Talentin raportointivaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="b2dff-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2dff-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="b2dff-104">**Environment details**</span></span>

<span data-ttu-id="b2dff-105">Tämä ongelma koskee kaikkia ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="b2dff-105">This issue applies to all environments.</span></span>

<span data-ttu-id="b2dff-106">**Oire**</span><span class="sxs-lookup"><span data-stu-id="b2dff-106">**Symptom**</span></span>

<span data-ttu-id="b2dff-107">Asiakas halua mukauttaa Microsoft Dynamics 365 for Talent -raportteja tai luoda uusia raportteja.</span><span class="sxs-lookup"><span data-stu-id="b2dff-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="b2dff-108">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="b2dff-108">**Issue**</span></span>

<span data-ttu-id="b2dff-109">Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="b2dff-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="b2dff-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="b2dff-110">**Solution**</span></span>

- <span data-ttu-id="b2dff-111">Sovellusten Common Data Serviceen siirtyvät Core HR -tiedot voidaan raportoida PowerApps CDS -liittimen välityksellä Power BI Desktopiin.</span><span class="sxs-lookup"><span data-stu-id="b2dff-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="b2dff-112">Huomaa, että sovellusten Common Data Service sisältää Core HR -tietojen alijoukon.</span><span class="sxs-lookup"><span data-stu-id="b2dff-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="b2dff-113">Lisätietoja Power BI:sta ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen PowerApps Common Data Servicen avulla](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="b2dff-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="b2dff-114">Sähköistä raportointia (ER) voi käyttää joissakin Talentin raporteissa.</span><span class="sxs-lookup"><span data-stu-id="b2dff-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="b2dff-115">Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="b2dff-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="b2dff-116">Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Talentin Microsoft Office -integraation avulla tarjoamia erilaisia tietoyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="b2dff-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="b2dff-117">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="b2dff-117">**Long-term solution**</span></span>

<span data-ttu-id="b2dff-118">Käyttöön tulee lisää Power BI -asetuksia, ja sovellusten Common Data Serviceen tulee sisältymään entistä enemmän tietoja ja yksiköitä.</span><span class="sxs-lookup"><span data-stu-id="b2dff-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>

