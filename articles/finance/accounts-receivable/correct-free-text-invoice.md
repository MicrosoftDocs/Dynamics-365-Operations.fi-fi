---
title: Vapaatekstilaskun korjaus
description: Tässä artikkelissa kerrotaan, miten kirjattu vapaatekstilasku korjataan ja luodaan uudelleen korjattuna laskuna.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3896a8574f7910ee09b360deb3ede10f061290bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991204"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="1584f-103">Vapaatekstilaskun korjaus</span><span class="sxs-lookup"><span data-stu-id="1584f-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1584f-104">Tässä artikkelissa kerrotaan, miten kirjattu vapaatekstilasku korjataan ja luodaan uudelleen korjattuna laskuna.</span><span class="sxs-lookup"><span data-stu-id="1584f-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="1584f-105">Voit korjata kirjatun vapaatekstilaskun avaamalla kirjatun vapaatekstilaskun.</span><span class="sxs-lookup"><span data-stu-id="1584f-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="1584f-106">Valitse **Lasku**-sivulla **Peruuta** ja sitten **Korjaa lasku**.</span><span class="sxs-lookup"><span data-stu-id="1584f-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="1584f-107">Valitse syykoodi, lisää kommentit ja valitse päivämäärä uudelle korjatulle laskulle.</span><span class="sxs-lookup"><span data-stu-id="1584f-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="1584f-108">Voit muokata korjattua laskua ja kirjata sen.</span><span class="sxs-lookup"><span data-stu-id="1584f-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="1584f-109">Kun kirjaat korjatun laskun, hyvityssummalle luodaan alkuperäisen laskun suuruinen peruutuslasku.</span><span class="sxs-lookup"><span data-stu-id="1584f-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="1584f-110">Alkuperäisen laskun ja peruutuslasku yhteissaldo onkin tämän vuoksi 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="1584f-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="1584f-111">Peruutuslasku tilitetään alkuperäiseen laskuun.</span><span class="sxs-lookup"><span data-stu-id="1584f-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="1584f-112">Korjatun laskun kirjaamisen jälkeen sinulla on kolme laskua:</span><span class="sxs-lookup"><span data-stu-id="1584f-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="1584f-113">**Alkuperäinen lasku** – lasku, joka sisältää korjattavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="1584f-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="1584f-114">**Peruutuslasku** – järjestelmän luoma hyvityslasku, joka on luotiin peruuttamaan viimeksi korjattu lasku.</span><span class="sxs-lookup"><span data-stu-id="1584f-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="1584f-115">**Korjattu lasku** – lasku, joka sisältää korjatut laskutiedot.</span><span class="sxs-lookup"><span data-stu-id="1584f-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="1584f-116">Peruutuslaskun ja korjaavan laskun voi tunnistaa kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="1584f-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="1584f-117">**Kaikki vapaamuotoiset laskut** -sivulla on **Korjaus**-sarake, josta näet, mitkä laskut ovat peruutuslaskuja ja mitkä korjattuja laskuja.</span><span class="sxs-lookup"><span data-stu-id="1584f-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="1584f-118">Vapaatekstilaskun otsikon tila on joko **Peruutuslasku \[laskunumero\]** tai **Korjattu lasku \[laskunumero\]**.</span><span class="sxs-lookup"><span data-stu-id="1584f-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="1584f-119">Tämä toiminto on käytettävissä vain, jos **Tekstimuotoisen laskun korjaus** -määritysavain on valittu.</span><span class="sxs-lookup"><span data-stu-id="1584f-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="1584f-120">Lisätietoja määritysavainten käyttöönotoista on aiheen [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) Ota käyttöön (tai poista käytöstä) määritysavaimia -osassa.</span><span class="sxs-lookup"><span data-stu-id="1584f-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) topic.</span></span> 



