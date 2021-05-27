---
title: Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen
description: Tässä aiheessa kerrotaan, miten vähittäismyyntitapahtumien taloushallinnon dimensioita muokataan Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381d8bb0939f6c4c163477990e49382201487375
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019904"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="e759f-103">Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e759f-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e759f-104">Tässä aiheessa kerrotaan, miten vähittäismyyntitapahtumien taloushallinnon dimensioita muokataan Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="e759f-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="e759f-105">Taloushallinnon dimensioiden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e759f-105">Edit financial dimensions</span></span>

<span data-ttu-id="e759f-106">Voit muokata vähittäismyyntitapahtumien taloushallinnon dimensioita Commerce-pääkonttorisovelluksessa seuraamalla alla olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e759f-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e759f-107">Avaa **Integrointisovellusten taloushallinnon dimension määritykset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="e759f-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="e759f-108">Valitse aktiivinen **Oletusdimensioiden integrointi** -tietue.</span><span class="sxs-lookup"><span data-stu-id="e759f-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="e759f-109">Varmista **Taloushallinnon dimensiot** -pikavälilehdessä, että Excel-laskentataulukon kaikki muokattavat dimensiot löytyvät **Valitut**-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e759f-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="e759f-110">Lisätietoja on kohdassa [Tietoentiteetit](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span><span class="sxs-lookup"><span data-stu-id="e759f-110">For more information, see [Data entities](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span></span>
1. <span data-ttu-id="e759f-111">Lataa ja avaa Excel-tiedosto **Laskelmat**-sivulla, **Vähittäismyyntitapahtumat**-sivulla tai **Tapahtuman tarkistusvirheet** -ruudussa **Myymälän taloustiedot** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="e759f-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="e759f-112">Jos haluat muuttaa tapahtuman taloushallinnon dimensiota, valitse **Rakenne** ja valitse sitten **Tapahtuma (tarkistettavissa)** -rivin vieressä oleva kynäsymboli.</span><span class="sxs-lookup"><span data-stu-id="e759f-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="e759f-113">Etsi ja valitse **FinancialDimensionDisplayValue**-kenttä, valitse Excel-laskentataulukon otsikon osan solu ja valitse sitten **Lisää selite**.</span><span class="sxs-lookup"><span data-stu-id="e759f-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="e759f-114">Valitse edellisessä vaiheessa valitun solun alla oleva solu. Valitse **Lisää arvo** ja valitse sitten **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="e759f-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="e759f-115">Taloushallinnon dimensiot lisätään Excel-laskentataulukkoon, ja niitä voi muokata ja julkaista.</span><span class="sxs-lookup"><span data-stu-id="e759f-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="e759f-116">Voit muuttaa tapahtumarivien dimensioita valitsemalla **Myyntitapahtumat (tarkistettavissa)** -rivin, valitsemalla sitten kynäsymbolin ja toistamalla vaiheet 6 ja 7.</span><span class="sxs-lookup"><span data-stu-id="e759f-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="e759f-117">Voit muuttaa maksurivien dimensioita valitsemalla **Maksutapahtumat (tarkistettavissa)** -rivin, valitsemalla sitten kynäsymbolin ja toistamalla vaiheet 6 ja 7.</span><span class="sxs-lookup"><span data-stu-id="e759f-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e759f-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e759f-118">Additional resources</span></span>

[<span data-ttu-id="e759f-119">Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen</span><span class="sxs-lookup"><span data-stu-id="e759f-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="e759f-120">Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e759f-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="e759f-121">Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="e759f-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="e759f-122">Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten</span><span class="sxs-lookup"><span data-stu-id="e759f-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]