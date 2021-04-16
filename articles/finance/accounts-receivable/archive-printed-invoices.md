---
title: Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla
description: Tässä aiheessa kuvataan, kuinka arkistointi otetaan käyttöön, jotta tulostetut asiakaslaskut voidaan tallentaa hajautusnumeroilla.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5b0305381ee709ce52b18d171a1ea274e2126cce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827695"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="f7a01-103">Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla</span><span class="sxs-lookup"><span data-stu-id="f7a01-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f7a01-104">Joissakin maissa on lakisääteinen vaatimus tallentaa järjestelmään joidenkin tiedostojen tulosteet sekä lasketut hajautusnumerot.</span><span class="sxs-lookup"><span data-stu-id="f7a01-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="f7a01-105">Hajautusnumeroita voidaan käyttää viranomaisille raportoitaessa ja auditoinnissa.</span><span class="sxs-lookup"><span data-stu-id="f7a01-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="f7a01-106">Tässä aiheessa kuvataan, kuinka arkistointi määritetään, jotta tulostetut asiakaslaskut voidaan tallentaa hajautusnumeroilla.</span><span class="sxs-lookup"><span data-stu-id="f7a01-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7a01-107">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f7a01-107">Prerequisites</span></span>

- <span data-ttu-id="f7a01-108">Ota **ominaisuuden hallinta**-työtilassa käyttöön toiminto **Arkistoi tulostetut myyntilaskut hajautusarvonumeroilla**.</span><span class="sxs-lookup"><span data-stu-id="f7a01-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="f7a01-109">Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f7a01-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="f7a01-110">Tarvittavien tiedostojen tulostettavat muodot konfiguroidaabn **tulostuksenhallinnassa**.</span><span class="sxs-lookup"><span data-stu-id="f7a01-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="f7a01-111">Tämä toiminto koskee seuraavia asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="f7a01-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="f7a01-112">**Myyntireskontra**</span><span class="sxs-lookup"><span data-stu-id="f7a01-112">**Accounts receivable**</span></span>
- <span data-ttu-id="f7a01-113">Myyntilasku</span><span class="sxs-lookup"><span data-stu-id="f7a01-113">Customer invoice</span></span>
- <span data-ttu-id="f7a01-114">Asiakkaan hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="f7a01-114">Customer credit note</span></span>
- <span data-ttu-id="f7a01-115">Vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="f7a01-115">Free text invoice</span></span>
- <span data-ttu-id="f7a01-116">Vapaamuotoinen hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="f7a01-116">Free text credit note</span></span>

<span data-ttu-id="f7a01-117">**Projektinhallinta ja kirjanpito**</span><span class="sxs-lookup"><span data-stu-id="f7a01-117">**Project management and accounting**</span></span>
- <span data-ttu-id="f7a01-118">Projektilasku</span><span class="sxs-lookup"><span data-stu-id="f7a01-118">Project invoice</span></span>
- <span data-ttu-id="f7a01-119">Projektin hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="f7a01-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="f7a01-120">Asiakkaan päätietojen määritys</span><span class="sxs-lookup"><span data-stu-id="f7a01-120">Configure customer master data</span></span>
<span data-ttu-id="f7a01-121">Seuraavia ohjeita noudattamalla voit konfiguroida asiakastiedot ja ottaa käyttöön mahdollisuuden tallentaa tulostetut laskut automaattisesti liitteinä.</span><span class="sxs-lookup"><span data-stu-id="f7a01-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="f7a01-122">Siirry kohtaan **Myyntireskontra** > **Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="f7a01-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="f7a01-123">Valitse asiakas ja valitse **E-INVOCE**-osan **eInvoice-liite**-kentästä **Lasku ja toimitus** -pikavälilehdestä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f7a01-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="f7a01-124">Tulosta laskut</span><span class="sxs-lookup"><span data-stu-id="f7a01-124">Print invoices</span></span>
<span data-ttu-id="f7a01-125">Voit kirjata ja tulostaa minkä tahansa edellisessä menettelyssä määritetyn asiakkaan vapaateksti-, asiakas- ja projektilaskun tai hyvityslaskun.</span><span class="sxs-lookup"><span data-stu-id="f7a01-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="f7a01-126">Avaa tulostetun laskun **Liitteet**-sivu.</span><span class="sxs-lookup"><span data-stu-id="f7a01-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="f7a01-127">Etsi tulostetulle laskulle laskettu hajautusnumero **Liite**-pikavälilehden **Lisätiedot**-kenttäryhmän **Asiakirjan hajautusnumero** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="f7a01-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Liitteen hajautusnumero](media/attach-hash-num.jpg)

