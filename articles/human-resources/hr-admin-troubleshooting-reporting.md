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
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431012"
---
# <a name="reporting-options"></a><span data-ttu-id="532cf-103">Raportointivaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="532cf-103">Reporting options</span></span>

<span data-ttu-id="532cf-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="532cf-104">**Environment details**</span></span>

<span data-ttu-id="532cf-105">Tämä ongelma koskee kaikkia ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="532cf-105">This issue applies to all environments.</span></span>

<span data-ttu-id="532cf-106">**Oire**</span><span class="sxs-lookup"><span data-stu-id="532cf-106">**Symptom**</span></span>

<span data-ttu-id="532cf-107">Asiakas halua mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.</span><span class="sxs-lookup"><span data-stu-id="532cf-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="532cf-108">**Varasto-otto**</span><span class="sxs-lookup"><span data-stu-id="532cf-108">**Issue**</span></span>

<span data-ttu-id="532cf-109">Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="532cf-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="532cf-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="532cf-110">**Solution**</span></span>

- <span data-ttu-id="532cf-111">Common Data Serviceen siirtyvät Human Resources -tiedot voidaan raportoida Power Apps Common Data Service -liittimen välityksellä Power BI Desktopiin.</span><span class="sxs-lookup"><span data-stu-id="532cf-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="532cf-112">Huomaa, että Common Data Service sisältää Human Resources -tietojen alijoukon.</span><span class="sxs-lookup"><span data-stu-id="532cf-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="532cf-113">Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen Power Apps Common Data Servicen avulla](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="532cf-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="532cf-114">Sähköistä raportointia (ER) voi käyttää joissakin Human Resourcesin raporteissa.</span><span class="sxs-lookup"><span data-stu-id="532cf-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="532cf-115">Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="532cf-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="532cf-116">Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Human Resourcesin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="532cf-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="532cf-117">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="532cf-117">**Long-term solution**</span></span>

<span data-ttu-id="532cf-118">Käyttöön tulee lisää Power BI -asetuksia, ja Common Data Serviceen tulee sisältymään entistä enemmän tietoja ja yksiköitä.</span><span class="sxs-lookup"><span data-stu-id="532cf-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
