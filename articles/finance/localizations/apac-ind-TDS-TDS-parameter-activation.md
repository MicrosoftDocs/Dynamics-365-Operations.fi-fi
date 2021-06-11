---
title: Määritä TDS-parametrit
description: Tässä aiheessa kuvataan, kuinka määritetään parametrit, jotka aktivoivat Vero vähennettynä lähteissä (TDS) -toiminnon määritetyissä tapahtumissa. Tämä on tarpeellinen vaihe, kun haluat käyttää Vero vähennettynä lähteissä (TDS) -toimintoa.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023206"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="c288f-104">Määritä TDS-parametrit</span><span class="sxs-lookup"><span data-stu-id="c288f-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c288f-105">Tässä aiheessa kuvataan, kuinka määritetään parametrit, jotka aktivoivat Vero vähennettynä lähteissä (TDS) -toiminnon määritetyissä tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="c288f-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="c288f-106">Tämä on tarpeellinen vaihe, kun haluat käyttää Vero vähennettynä lähteissä (TDS) -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="c288f-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="c288f-107">Siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpitoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="c288f-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="c288f-108">Määritä **Suorat verot** -välilehden **Vero vähennettynä lähteissä** -osiossa **Aktivoi TDS** -asetuksen arvoksi **Kyllä** aktivoidaksesi TDS-toiminnon sekä siihen käytettävät sivut ja kentät.</span><span class="sxs-lookup"><span data-stu-id="c288f-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="c288f-109">Valitse **Lasku**-asetuksen arvoksi **Kyllä**, jos haluat ottaa käyttöön kentät, joita käytetään TDS:n laskentaan ja vähennykseen laskutasolla.</span><span class="sxs-lookup"><span data-stu-id="c288f-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="c288f-110">Valitse **Maksu**-asetuksen arvoksi **Kyllä**, jos haluat ottaa käyttöön kentät, joita käytetään TDS:n laskentaan ja vähennykseen maksutasolla.</span><span class="sxs-lookup"><span data-stu-id="c288f-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="c288f-111">[![Suorat verot -välilehti](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="c288f-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="c288f-112">Etsi **Numerosarjat**-välilehdestä rivi, jonka **Viite**-kentän arvoksi on määritetty **Ennakonpidätysmaksu**.</span><span class="sxs-lookup"><span data-stu-id="c288f-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="c288f-113">Valitse numerosarjan koodi rivin **Numerosarjan koodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c288f-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="c288f-114">Numerosarjan koodin avulla luodaan tositenumerot kausittaista TDS-tilitysprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="c288f-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c288f-115">Voit suorittaa kausittaisen TDS-tilitysprosessin valitsemalla **Vero \> Ilmoitukset \> Ennakonpidätys \> Ennakonpidätysmaksu**.</span><span class="sxs-lookup"><span data-stu-id="c288f-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="c288f-116">[![Numerosarjat-välilehti](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="c288f-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="c288f-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="c288f-117">Close the page.</span></span>