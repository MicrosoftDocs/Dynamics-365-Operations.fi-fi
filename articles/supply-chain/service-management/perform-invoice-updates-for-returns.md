---
title: Laskun päivitysten suorittaminen palautuksille
description: Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d3b884d1ed11d2f79e968a5a099860486ef600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810651"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="14958-103">Laskun päivitysten suorittaminen palautuksille</span><span class="sxs-lookup"><span data-stu-id="14958-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="14958-104">Palautustilaus on sellaisen myyntitilauksen tyyppi, joka on merkitty palautetuksi tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="14958-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="14958-105">Siksi palautustilausten laskut luodaan **Kaikki myyntitilaukset**-luettelosivulla **Palautustilaukset** -lomakkeen sijaan.</span><span class="sxs-lookup"><span data-stu-id="14958-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="14958-106">Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.</span><span class="sxs-lookup"><span data-stu-id="14958-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="14958-107">Koska palautettavan nimikkeen laskussa on negatiivinen summa, sitä kutsutaan hyvityslaskuksi.</span><span class="sxs-lookup"><span data-stu-id="14958-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="14958-108">Kun määrität laskupäivityksen eräkäsittelyä varten, **Palautettu tilaus** -tyypin myyntitilauksen palautusrivin tilan pitää olla **Vastaanotettu**. Tämä tila ilmaisee, että tilauksen pakkausluettelo on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="14958-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="14958-109">Palautustilauksen laskun kirjaus</span><span class="sxs-lookup"><span data-stu-id="14958-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="14958-110">Napsauta **Myyntireskontra** \> **Yleinen** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="14958-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="14958-111">Valitse myyntitilaus, jossa **Palautettu tilaus** näkyy **Tilauksen tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="14958-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="14958-112">Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="14958-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="14958-113">Valitse **Parametrit**-välilehdellä **Kirjaus**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="14958-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="14958-114">Tarkista lomakkeen tiedot ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="14958-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="14958-115">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="14958-115">Click **OK**.</span></span> <span data-ttu-id="14958-116">Hyvityslasku kirjataan.</span><span class="sxs-lookup"><span data-stu-id="14958-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="14958-117">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="14958-117">See also</span></span>

[<span data-ttu-id="14958-118">Palautusten pakkausluettelopäivitykset</span><span class="sxs-lookup"><span data-stu-id="14958-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]