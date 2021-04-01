---
title: Vuokrakirjauskansioiden nimien määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten vuokrakirjauskansioiden nimet määritetään. Vuokrakirjauskansioiden nimien määrittävät kirjauskansiot, joihin resurssin vuokrauksen viennit kirjataan.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 98595848593e3abd63701b52c7a67ec61288a96e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249626"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="5d9ff-104">Vuokrakirjauskansioiden nimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5d9ff-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d9ff-105">Vuokrakirjauskansioiden nimien määrittävät kirjauskansiot, joihin resurssin vuokrauksen tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="5d9ff-106">Vain **Resurssin vuokraus** -kirjauskansiotyypin kirjauskansioiden nimet näkyvät **Alkuperäinen tuloutus**- ja **Kuukausittaisen kirjauskansion nimi** -kentissä **Resurssin vuokraparametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="5d9ff-107">Vain **Toimittajan laskun tallentaminen** -kirjauskansiotyyppi voidaan liittää **Laskukirjauskansion nimi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="5d9ff-108">Voit määrittää vuokrakirjauskansioiden nimet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="5d9ff-109">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Resurssin vuokrausparametrit**.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="5d9ff-110">Valitse **Yleistiedot**-välilehden **Alkuperäisen tuloutuksen kirjauskansion nimi** -kentässä kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="5d9ff-111">Kaikki alkuperäisen tuloutuksen kirjauskansioviennit kirjataan tähän kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="5d9ff-112">Valitse **Laskukirjauskansion nimi** -kentässä kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="5d9ff-113">Jos **Maksa toimittajalle** -vaihtoehdon arvoksi on määritetty **Kyllä** vuokrasopimuskirjassa, vuokrasopimuksen ja kulun maksujen laskut kirjataan tähän kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="5d9ff-114">Valitse **Vuokrakirjauskansion nimi** -kentässä kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="5d9ff-115">Kaikki poistot, korot ja lyhytaikaiset uudelleenluokitusviennit kirjataan tähän kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="5d9ff-116">Jos **Maksa toimittajalle** -vaihtoehdon arvoksi on määritetty **Ei** vuokrasopimuskirjassa, vuokrien ja kulun maksujen viennit kirjataan myös tähän kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]