---
title: Raportointivaihtoehdot
description: Tässä artikkelissa kerrotaan, miten voidaan ratkaista ongelma, kun asiakas haluaa mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008955"
---
# <a name="reporting-options"></a><span data-ttu-id="e65a8-103">Raportointivaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="e65a8-103">Reporting options</span></span>

<span data-ttu-id="e65a8-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="e65a8-104">**Environment details**</span></span>

<span data-ttu-id="e65a8-105">Tämä ongelma koskee kaikkia ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="e65a8-105">This issue applies to all environments.</span></span>

<span data-ttu-id="e65a8-106">**Oire**</span><span class="sxs-lookup"><span data-stu-id="e65a8-106">**Symptom**</span></span>

<span data-ttu-id="e65a8-107">Asiakas halua mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.</span><span class="sxs-lookup"><span data-stu-id="e65a8-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="e65a8-108">**Varasto-otto**</span><span class="sxs-lookup"><span data-stu-id="e65a8-108">**Issue**</span></span>

<span data-ttu-id="e65a8-109">Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="e65a8-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="e65a8-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="e65a8-110">**Solution**</span></span>

- <span data-ttu-id="e65a8-111">Common Data Serviceen siirtyvät Human Resources -tiedot voidaan raportoida Power Apps Common Data Service -liittimen välityksellä Power BI Desktopiin.</span><span class="sxs-lookup"><span data-stu-id="e65a8-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="e65a8-112">Huomaa, että Common Data Service sisältää Human Resources -tietojen alijoukon.</span><span class="sxs-lookup"><span data-stu-id="e65a8-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="e65a8-113">Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen Power Apps Common Data Servicen avulla](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="e65a8-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="e65a8-114">Sähköistä raportointia (ER) voi käyttää joissakin Human Resourcesin raporteissa.</span><span class="sxs-lookup"><span data-stu-id="e65a8-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="e65a8-115">Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="e65a8-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="e65a8-116">Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Human Resourcesin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="e65a8-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="e65a8-117">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="e65a8-117">**Long-term solution**</span></span>

<span data-ttu-id="e65a8-118">Käyttöön tulee lisää Power BI -asetuksia, ja Common Data Serviceen tulee sisältymään entistä enemmän tietoja ja yksiköitä.</span><span class="sxs-lookup"><span data-stu-id="e65a8-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>