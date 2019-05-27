---
title: Määritä cross-kurssi
description: Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Finance and Operationsin ristikursseista.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546061"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="5d6a7-103">Määritä cross-kurssi</span><span class="sxs-lookup"><span data-stu-id="5d6a7-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d6a7-104">Tässä ohjeaiheessa kuvataan ristikurssin tarkoitus ja kuinka ristikurssi määritetään, kun täsmäytät maksun laskun kanssa.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="5d6a7-105">Käytä ristikurssia, kun kaikki seuraavat kriteerit täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="5d6a7-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="5d6a7-106">Selvität maksua laskun kanssa.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="5d6a7-107">Maksurivi ja laskurivi käyttävät eri valuuttoja.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="5d6a7-108">Kumpikaan valuutta ei ole kirjanpitovaluuttaa.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="5d6a7-109">Ristikursseja ei käytetä laskettaessa maksutapahtuman valuutan muuntamista maksun kirjanpitovaluuttaan.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="5d6a7-110">Sen sijaan vaihtokurssitaulusta noudetaan vaihtokurssit, joilla lasketaan maksutapahtuman valuuttasumman ja maksun kirjanpitovaluuttasumman arvo.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="5d6a7-111">Esimerkiksi kirjanpitovaluutta on USD, laskutusvaluutta on CAD ja maksuvaluutta on EUR.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="5d6a7-112">Ristikurssin avulla voit kirjoittaa vaihtokurssin, jonka avulla voit muuntaa suoraan Kanadan dollarit euroiksi, eikä sinun tarvitse muuntaa Yhdysvaltain dollareiden kautta.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="5d6a7-113">Kun valitset laskun ja ensisijaisen maksun, voit syöttää ristikurssin laskuriville.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="5d6a7-114">Ristikurssi on näiden tapahtumien valuuttojen vaihtokurssi selvityspäivänä.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="5d6a7-115">Valitse jokin seuraavista sivuista:</span><span class="sxs-lookup"><span data-stu-id="5d6a7-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="5d6a7-116">**Myyntireskontra > Yleinen > Asiakkaat > Kaikki asiakkaat.**</span><span class="sxs-lookup"><span data-stu-id="5d6a7-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="5d6a7-117">**Ostoreskontra > Yleiset > Toimittajat > Kaikki toimittajat.**</span><span class="sxs-lookup"><span data-stu-id="5d6a7-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="5d6a7-118">**Hankinta > Yleinen > Toimittajat > Kaikki toimittajat**</span><span class="sxs-lookup"><span data-stu-id="5d6a7-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="5d6a7-119">Valitse asiakas tai toimittaja, jonka avoimia tapahtumia selvität.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="5d6a7-120">Jos kyse on asiakkaasta, valitse **Kaikki asiakkaat** -luettelosivulla **Perintä > Tilitä avoimet tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="5d6a7-121">Jos kyse on toimittajasta, valitse **Kaikki toimittajat** -luettelosivulla **Lasku > Tilitä avoimet tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="5d6a7-122">Valitse tapahtuma, joka on ensisijainen maksu, ja valitse sitten **Merkitse maksu**.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="5d6a7-123">**Merkitse**-sarakkeen valintaruutu on valittu ja tietokuvake näkyy **Ensisijainen maksu** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="5d6a7-124">Anna **Ristikurssi**-kentässä laskun valuutan ja maksun valuutan vaihtokurssi selvityspäivänä.</span><span class="sxs-lookup"><span data-stu-id="5d6a7-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
