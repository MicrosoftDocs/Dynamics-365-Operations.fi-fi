---
title: Talentin raportointivaihtoehdot
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, kun asiakas haluaa mukauttaa Microsoft Dynamics 365 Talent -raportteja tai luoda uusia raportteja.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897945"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="15cd3-103">Talentin raportointiasetukset</span><span class="sxs-lookup"><span data-stu-id="15cd3-103">Reporting options in Talent</span></span>

<span data-ttu-id="15cd3-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="15cd3-104">**Environment details**</span></span>

<span data-ttu-id="15cd3-105">Tämä ongelma koskee kaikkia ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="15cd3-105">This issue applies to all environments.</span></span>

<span data-ttu-id="15cd3-106">**Oire**</span><span class="sxs-lookup"><span data-stu-id="15cd3-106">**Symptom**</span></span>

<span data-ttu-id="15cd3-107">Asiakas halua mukauttaa Microsoft Dynamics 365 Talent -raportteja tai luoda uusia raportteja.</span><span class="sxs-lookup"><span data-stu-id="15cd3-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="15cd3-108">**Varasto-otto**</span><span class="sxs-lookup"><span data-stu-id="15cd3-108">**Issue**</span></span>

<span data-ttu-id="15cd3-109">Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="15cd3-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="15cd3-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="15cd3-110">**Solution**</span></span>

- <span data-ttu-id="15cd3-111">Common Data Serviceen siirtyvät Core HR -tiedot voidaan raportoida Power Apps Common Data Service -liittimen välityksellä Power BI Desktopiin.</span><span class="sxs-lookup"><span data-stu-id="15cd3-111">The Core HR data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="15cd3-112">Huomaa, että Common Data Service sisältää Core HR -tietojen alijoukon.</span><span class="sxs-lookup"><span data-stu-id="15cd3-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="15cd3-113">Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen Power Apps Common Data Servicen avulla](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="15cd3-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="15cd3-114">Sähköistä raportointia (ER) voi käyttää joissakin Talentin raporteissa.</span><span class="sxs-lookup"><span data-stu-id="15cd3-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="15cd3-115">Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="15cd3-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="15cd3-116">Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Talentin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="15cd3-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="15cd3-117">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="15cd3-117">**Long-term solution**</span></span>

<span data-ttu-id="15cd3-118">Käyttöön tulee lisää Power BI -asetuksia, ja Common Data Serviceen tulee sisältymään entistä enemmän tietoja ja yksiköitä.</span><span class="sxs-lookup"><span data-stu-id="15cd3-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
