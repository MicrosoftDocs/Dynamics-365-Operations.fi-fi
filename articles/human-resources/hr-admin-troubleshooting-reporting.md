---
title: Raportointivaihtoehdot
description: Tässä artikkelissa kerrotaan, miten voidaan ratkaista ongelma, kun asiakas haluaa mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 66581331dceacc1c0fa1816bf336339693db5339
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463283"
---
# <a name="reporting-options"></a><span data-ttu-id="918cc-103">Raportointivaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="918cc-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="918cc-104">**Ympäristön tiedot**</span><span class="sxs-lookup"><span data-stu-id="918cc-104">**Environment details**</span></span>

<span data-ttu-id="918cc-105">Tämä ongelma koskee kaikkia ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="918cc-105">This issue applies to all environments.</span></span>

<span data-ttu-id="918cc-106">**Oire**</span><span class="sxs-lookup"><span data-stu-id="918cc-106">**Symptom**</span></span>

<span data-ttu-id="918cc-107">Asiakas halua mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.</span><span class="sxs-lookup"><span data-stu-id="918cc-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="918cc-108">**Varasto-otto**</span><span class="sxs-lookup"><span data-stu-id="918cc-108">**Issue**</span></span>

<span data-ttu-id="918cc-109">Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.</span><span class="sxs-lookup"><span data-stu-id="918cc-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="918cc-110">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="918cc-110">**Solution**</span></span>

- <span data-ttu-id="918cc-111">Dataverseen siirtyvät Human Resources -tiedot voidaan raportoida Power Apps Dataverse -liittimen välityksellä Power BI Desktopiin.</span><span class="sxs-lookup"><span data-stu-id="918cc-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="918cc-112">Huomaa, että Dataverse sisältää Human Resources -tietojen alijoukon.</span><span class="sxs-lookup"><span data-stu-id="918cc-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="918cc-113">Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen Power Apps Common Data Servicen avulla](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="918cc-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="918cc-114">Sähköistä raportointia (ER) voi käyttää joissakin Human Resourcesin raporteissa.</span><span class="sxs-lookup"><span data-stu-id="918cc-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="918cc-115">Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="918cc-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="918cc-116">Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Human Resourcesin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.</span><span class="sxs-lookup"><span data-stu-id="918cc-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="918cc-117">**Pitkäaikainen ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="918cc-117">**Long-term solution**</span></span>

<span data-ttu-id="918cc-118">Käyttöön tulee lisää Power BI -asetuksia, ja Dataverseen tulee sisältymään entistä enemmän tietoja ja yksiköitä.</span><span class="sxs-lookup"><span data-stu-id="918cc-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]