---
title: TaxTrans-tietuetta ei luoda
description: Tämä ohjeaihe sisältää vianmääritystietoja, jotka voivat auttaa, kun TaxTrans-tietuetta ei luoda.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947631"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="63ee6-103">TaxTrans-tietuetta ei luoda</span><span class="sxs-lookup"><span data-stu-id="63ee6-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63ee6-104">Jos valitset tapahtumalle **Kirjattu arvonlisävero** ja **Kirjattu arvonlisävero** -sivulla ei ole verorivejä tai verorivi puuttuu, **TaxTrans**-tietuetta ei ehkä ole luotu.</span><span class="sxs-lookup"><span data-stu-id="63ee6-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="63ee6-105">[![Kirjattu arvonlisävero -sivu, jolla ei ole rivinimikkeitä](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="63ee6-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="63ee6-106">Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="63ee6-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="63ee6-107">Tarkista arvonlisävero ennen tapahtuman kirjaamista</span><span class="sxs-lookup"><span data-stu-id="63ee6-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="63ee6-108">Tarkista laskelma ennen tapahtuman kirjausta valitsemalla **Laskun kirjaus** -sivulla **Arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="63ee6-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="63ee6-109">[![Arvonlisävero-painike Laskun kirjaus -sivulla](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="63ee6-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="63ee6-110">Tarkista **Tilapäiset arvonlisäverotapahtumat** -sivulla laskelman tulos.</span><span class="sxs-lookup"><span data-stu-id="63ee6-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="63ee6-111">Jos veroa ei lasketa, katso kohta [Veroa ei lasketa tai veron summa on nolla](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="63ee6-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="63ee6-112">TaxTrans-tietueen etsiminen kaikista kirjatuista arvonlisäveroista</span><span class="sxs-lookup"><span data-stu-id="63ee6-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="63ee6-113">Valitse **Vero** \> **Kyselyt ja raportit** \> **Arvonlisäverokyselyt** > **Kirjattu arvonlisävero**.</span><span class="sxs-lookup"><span data-stu-id="63ee6-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="63ee6-114">Valitse **Tosite**-sarakeotsikossa suodatussymboli etsiäksesi **TaxTrans**-tietueen.</span><span class="sxs-lookup"><span data-stu-id="63ee6-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="63ee6-115">Jos löydät etsimäsi arvonlisäverotietueen, tarkista päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="63ee6-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="63ee6-116">Jos päivämäärä on eri kuin kirjauskansion otsikon päivämäärä, luo Microsoftin huoltopyyntö lisätuen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="63ee6-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="63ee6-117">[![Kirjattu arvonlisävero -sivu](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="63ee6-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="63ee6-118">Tarkista suorittamalla virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="63ee6-118">Debug to check details</span></span>

1. <span data-ttu-id="63ee6-119">Lisätietoja virheenkorjauksesta ja siitä, luodaanko **TmpTaxWorkTrans** ja **TaxUncommitted** oikein on kohdassa [TaxTrans-kentän arvo on virheellinen](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="63ee6-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="63ee6-120">Jos **TaxTmpWorkTrans** tai **TaxUncommitted** on luotu oikein, lisää keskeytyskohta kohteisiin **TaxPost::SaveAndPost()** ja **Tax::SaveAndPost** suorittaaksesi virheenkorjauksen syylle, miksi **TaxTrans**-kohdetta ei lisätä.</span><span class="sxs-lookup"><span data-stu-id="63ee6-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="63ee6-121">[![Koodiin lisätyt keskeytyskohdat](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="63ee6-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="63ee6-122">[![Lisättyjen keskeytyskohtien tulokset](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="63ee6-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="63ee6-123">Määritä, onko mukautus olemassa</span><span class="sxs-lookup"><span data-stu-id="63ee6-123">Determine whether customization exists</span></span>

<span data-ttu-id="63ee6-124">Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa.</span><span class="sxs-lookup"><span data-stu-id="63ee6-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="63ee6-125">Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="63ee6-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
