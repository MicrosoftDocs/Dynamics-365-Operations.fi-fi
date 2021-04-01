---
title: Ennakonpidätys ostotapahtumissa
description: Ennakonpidätyksen alaisille toimittajille voit määrittää **ennakonpidätysryhmän** oletusarvon **Kaikki toimittajat** -sivulla.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256664"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="3d902-103">Ennakonpidätys ostotapahtumissa</span><span class="sxs-lookup"><span data-stu-id="3d902-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="3d902-104">Ennakonpidätyksen alaisille toimittajille voit määrittää **ennakonpidätysryhmän** oletusarvon **Kaikki toimittajat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3d902-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="3d902-105">Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra > Toimittajat > Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="3d902-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="3d902-106">Valitse haluttu toimittajatili ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="3d902-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="3d902-107">Määritä **Lasku ja toimitus** -välilehdessä **Laske ennakonpidätys** -kentän arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3d902-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="3d902-108">Ennakonpidätystä ei lasketa, jos tämän toimittajan **Laske ennakonpidätys** -asetusta ei ole otettu käyttöön tiedoissa.</span><span class="sxs-lookup"><span data-stu-id="3d902-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="3d902-109">Valitse ennakonpidätysryhmä kohdassa **Ennakonpidätysryhmä**.</span><span class="sxs-lookup"><span data-stu-id="3d902-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="3d902-110">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3d902-110">Click **Save**.</span></span>

<span data-ttu-id="3d902-111">Voit määrittää ennakonpidätyksen alaisille nimikkeille/palveluille oletusarvoisen **Nimikkeen ennakonpidätysryhmän** kohdassa **Julkaistut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="3d902-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="3d902-112">Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="3d902-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="3d902-113">Valitse haluttu nimikenumero ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="3d902-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="3d902-114">Valitse **Osto**-välilehdestä **Laske ennakonpidätys**.</span><span class="sxs-lookup"><span data-stu-id="3d902-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="3d902-115">Ennakonpidätystä ei lasketa, jos **Laske ennakonpidätys** -asetuksena ei ole **Kyllä** tälle nimikkeelle **Julkaistu tuote** -sivun **Osto**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="3d902-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="3d902-116">Valitse nimikkeen ennakonpidätysryhmä **Nimikkeen ennakonpidätysryhmä** -luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3d902-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="3d902-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3d902-117">Click **Save**.</span></span>

<span data-ttu-id="3d902-118">Ennakonpidätysryhmät ja nimikkeen ennakonpidätysryhmät voidaan sivuilla.</span><span class="sxs-lookup"><span data-stu-id="3d902-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="3d902-119">**Ostotilaus**</span><span class="sxs-lookup"><span data-stu-id="3d902-119">**Purchase order**</span></span>
- <span data-ttu-id="3d902-120">**Toimittajan lasku**</span><span class="sxs-lookup"><span data-stu-id="3d902-120">**Vendor invoice**</span></span>
- <span data-ttu-id="3d902-121">**Laskukirjauskansio**</span><span class="sxs-lookup"><span data-stu-id="3d902-121">**Invoice journal**</span></span>

<span data-ttu-id="3d902-122">Ennakonpidätysryhmän ja nimikkeen ennakonpidätysryhmän oletusarvo tulee riveille, kun luot **ostotilauksia** ja/tai **odottavia toimittajan laskuja**.</span><span class="sxs-lookup"><span data-stu-id="3d902-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="3d902-123">Voit ottaa **toimittajan laskukirjauskansion** osalta käyttöön **Laske ennakonpidätys** -asetuksen ja valita kirjauskansion **Yleiset**-välilehdestä **Nimikkeen ennakonpidätysryhmän**.</span><span class="sxs-lookup"><span data-stu-id="3d902-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="3d902-124">Ennakonpidätyksen väliaikainen summa on käytettävissä **Ostotilaus**-sivun **Summat**-välilehden **Oikaistu ennakonpidätys** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="3d902-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Ennakonpidätys sisältyy ostotilaukseen](media/withholding-tax-adjusted.png)

<span data-ttu-id="3d902-126">Ennakonpidätys lasketaan **toimittajan maksukirjauskansiossa**.</span><span class="sxs-lookup"><span data-stu-id="3d902-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="3d902-127">Voit oikaista sovellettavia ennakonpidätyskoodeja sekä todellisia ennakonpidätyksen summia manuaalisesti **Ennakonpidätys** -välilehdessä **Tapahtumien selvitys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3d902-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Ennakonpidätyksen voi muuttaa manuaalisesti Tapahtumien selvitys -sivulla](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="3d902-129">Johdettu ennakonpidätyksen summa vähennetään toimittajan maksusta ja kirjataan **ennakonpidätystilille** liittyvässä tositteessa.</span><span class="sxs-lookup"><span data-stu-id="3d902-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Ennakonpidätystili, jossa näkyy liittyvä tosite](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]