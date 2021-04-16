---
title: Ennakonpidätys myyntitapahtumissa
description: Tässä ohjeaiheessa on luettelo vaiheista valittujen asiakkaiden ennakonpidätyksen laskennan välttämiseksi. Voit määrittää oletusennakonpidätysryhmän asiakkaille, jotka määrittävät ennakonpidätyksen maksuissaan.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842341"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="3647b-104">Ennakonpidätys myyntitapahtumissa</span><span class="sxs-lookup"><span data-stu-id="3647b-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="3647b-105">Tässä ohjeaiheessa on luettelo vaiheista valittujen asiakkaiden ennakonpidätyksen laskennan välttämiseksi.</span><span class="sxs-lookup"><span data-stu-id="3647b-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="3647b-106">Voit **Asiakkaat**-sivulla määrittää oletusarvoisen **Ennakonpidätysryhmä**-ryhmän asiakkaille, jotka määrittävät ennakonpidätyksen maksuissaan.</span><span class="sxs-lookup"><span data-stu-id="3647b-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="3647b-107">Siirry kohtaan **Siirtymisruutu > Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="3647b-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="3647b-108">Valitse haluttu asiakastili ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="3647b-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="3647b-109">Määritä **Lasku ja toimitus** -välilehdessä **Laske ennakonpidätys** -kentän arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3647b-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="3647b-110">Ennakonpidätystä ei lasketa, jos tämän asiakkaan **Laske ennakonpidätys** -asetusta ei ole otettu käyttöön päätiedoissa.</span><span class="sxs-lookup"><span data-stu-id="3647b-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="3647b-111">Valitse ennakonpidätysryhmä kohdassa **Ennakonpidätysryhmä**.</span><span class="sxs-lookup"><span data-stu-id="3647b-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="3647b-112">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3647b-112">Click **Save**.</span></span>

<span data-ttu-id="3647b-113">Voit määrittää nimikkeelle/palvelulle, josta pitää maksaa ennakonpidätys, oletusarvoisen **Nimikkeen ennakonpidätysryhmän** kohdassa **Julkaistut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="3647b-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="3647b-114">Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="3647b-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="3647b-115">Valitse haluttu nimikenumero ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="3647b-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="3647b-116">Valitse **Myynti**-välilehdestä **Laske ennakonpidätys**.</span><span class="sxs-lookup"><span data-stu-id="3647b-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="3647b-117">Ennakonpidätystä ei lasketa, jos **Laske ennakonpidätys** -asetuksena ei ole **Kyllä** tälle nimikkeelle **Julkaistu tuote** -sivun **Myynti**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="3647b-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="3647b-118">Valitse nimikkeen ennakonpidätysryhmä **Nimikkeen ennakonpidätysryhmä** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3647b-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="3647b-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3647b-119">Click **Save**.</span></span>

<span data-ttu-id="3647b-120">Ennakonpidätysryhmät ja nimikkeen ennakonpidätysryhmät voidaan määrittää **Myyntitilaus**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="3647b-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="3647b-121">Kun luot uuden myyntitilauksen, käytetään ennakonpidätysryhmän ja nimikkeen ennakonpidätysryhmän oletusarvoja myyntitilausriveillä.</span><span class="sxs-lookup"><span data-stu-id="3647b-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="3647b-122">Ennakonpidätys lasketaan ja kirjataan **asiakkaan maksukirjauskansiossa**.</span><span class="sxs-lookup"><span data-stu-id="3647b-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="3647b-123">Voit oikaista sovellettavaa ennakonpidätyskoodia sekä todellista ennakonpidätyksen summaa manuaalisesti **Ennakonpidätys** -välilehdessä **Tapahtumien selvitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3647b-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="3647b-124">Laskettu ennakonpidätyksen summa vähennetään asiakasmaksusta ja kirjataan **ennakonpidätyksen vastatilille** liittyvässä tositteessa.</span><span class="sxs-lookup"><span data-stu-id="3647b-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]