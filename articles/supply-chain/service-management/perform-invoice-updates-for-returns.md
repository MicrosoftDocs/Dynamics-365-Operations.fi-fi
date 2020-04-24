---
title: Laskun päivitysten suorittaminen palautuksille
description: Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec803aaa2f750c43a1865c9536730b275e6ef1d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202134"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="4c9a2-103">Laskun päivitysten suorittaminen palautuksille</span><span class="sxs-lookup"><span data-stu-id="4c9a2-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4c9a2-104">Palautustilaus on sellaisen myyntitilauksen tyyppi, joka on merkitty palautetuksi tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="4c9a2-105">Siksi palautustilausten laskut luodaan **Kaikki myyntitilaukset**-luettelosivulla **Palautustilaukset** -lomakkeen sijaan.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="4c9a2-106">Tämä toiminto tukee myös liiketoimintaprosesseja organisaatioissa, joissa palautustilaukset ja myyntitilauksen on päätetty laskuttaa samanaikaisesti ja laskutuksen suorittaa sama henkilö.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="4c9a2-107">Koska palautettavan nimikkeen laskussa on negatiivinen summa, sitä kutsutaan hyvityslaskuksi.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="4c9a2-108">Kun määrität laskupäivityksen eräkäsittelyä varten, **Palautettu tilaus** -tyypin myyntitilauksen palautusrivin tilan pitää olla **Vastaanotettu**. Tämä tila ilmaisee, että tilauksen pakkausluettelo on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="4c9a2-109">Palautustilauksen laskun kirjaus</span><span class="sxs-lookup"><span data-stu-id="4c9a2-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="4c9a2-110">Napsauta **Myyntireskontra** \> **Yleinen** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="4c9a2-111">Valitse myyntitilaus, jossa **Palautettu tilaus** näkyy **Tilauksen tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="4c9a2-112">Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="4c9a2-113">Valitse **Parametrit**-välilehdellä **Kirjaus**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="4c9a2-114">Tarkista lomakkeen tiedot ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="4c9a2-115">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-115">Click **OK**.</span></span> <span data-ttu-id="4c9a2-116">Hyvityslasku kirjataan.</span><span class="sxs-lookup"><span data-stu-id="4c9a2-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c9a2-117">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4c9a2-117">See also</span></span>

[<span data-ttu-id="4c9a2-118">Palautusten pakkausluettelopäivitykset</span><span class="sxs-lookup"><span data-stu-id="4c9a2-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


