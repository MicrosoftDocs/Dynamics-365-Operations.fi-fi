---
title: Vapaatekstilasku-sivun laskujen TDS-laskenta
description: Tässä aiheessa kerrotaan, miten laskujen Vero vähennettynä lähteissä (TDS) lasketaan vapaatekstilaskusivua käyttäen.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023214"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="511df-103">Vapaatekstilasku-sivun laskujen TDS-laskenta</span><span class="sxs-lookup"><span data-stu-id="511df-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="511df-104">Tässä aiheessa kerrotaan, miten laskujen Vero vähennettynä lähteissä (TDS) lasketaan **Vapaatekstilasku**-sivua käyttäen.</span><span class="sxs-lookup"><span data-stu-id="511df-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="511df-105">Siirry kohtaan **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**.</span><span class="sxs-lookup"><span data-stu-id="511df-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="511df-106">[![Vapaatekstilaskun sivu](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="511df-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="511df-107">Luo vapaatekstilasku valitsemalla **Uusi** ja kirjoita tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="511df-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="511df-108">Valitse **Lasku**-välilehti. **Ennakonpidätysryhmä**-osiossa **Arvioitavan kohteen luonne** -kentässä näkyy asiakkaan arvioitavan kohteen luonteen luokka.</span><span class="sxs-lookup"><span data-stu-id="511df-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="511df-109">**TDS-ryhmä**-kentässä tarkastele tai muuta TDS-ryhmän oletusryhmää, joka on määritetty asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="511df-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="511df-110">Kun valitset arvon **TDS-ryhmä**-kentässä, **TCS-ryhmä**-kenttä ei ole enää käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="511df-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="511df-111">TDS lasketaan vain, jos **Laske ennakonpidätys** -vaihtoehdon asetuksena on **Kyllä** asiakkaalle **Kaikki asiakkaat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="511df-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="511df-112">Valitse **Verotiedot**-välilehden **Yritystiedot**-osan **Nimi**-kentästä yritykselle määritettävän vaihtoehtoisen osoitteen yrityksen nimi.</span><span class="sxs-lookup"><span data-stu-id="511df-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="511df-113">**Ennakonpidätys**-osassa **Verotilin numero (TAN)** -kentässä näkyy valitun yrityksen verotilin numero (TAN).</span><span class="sxs-lookup"><span data-stu-id="511df-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="511df-114">Luo laskurivit **Laskurivit**-välilehdessä ja syötä tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="511df-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="511df-115">**Ennakonpidätysryhmä**-osiossa **Verotilin numero (TAN)** -kentässä näkyy TAN, ja **TDS-ryhmä**-kentässä näkyy TDS-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="511df-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="511df-116">Valitse **Ennakonpidätys** avataksesi **Väliaikaiset ennakonpidätystapahtumat** -sivun.</span><span class="sxs-lookup"><span data-stu-id="511df-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="511df-117">Sivun yläosassa on seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="511df-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="511df-118">**Ennakonpidätyksen summa yhteensä** – TDS-kokonaissumma, joka on laskettu tapahtumalle TDS-ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="511df-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="511df-119">**Arvo** – Tapahtuman TDS:n laskemiseen käytettävä kokonaisprosentti.</span><span class="sxs-lookup"><span data-stu-id="511df-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="511df-120">Kokonaisprosentti perustuu kaavaan, joka on määritetty TDS-verokoodeille ja liitetty TDS-ryhmään.</span><span class="sxs-lookup"><span data-stu-id="511df-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="511df-121">**Oikaistu ennakonpidätyksen summa yhteensä** – Kaikkien TDS-ryhmän verokoodien oikaistu kokonaissumma.</span><span class="sxs-lookup"><span data-stu-id="511df-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="511df-122">**TDS** – Valittu valintaruutu ilmaisee, että tapahtumaan on liitetty TDS-ryhmä.</span><span class="sxs-lookup"><span data-stu-id="511df-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="511df-123">**Yhteenveto**-, **Yleinen**- ja **Oikaisu**-välilehdissä näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.</span><span class="sxs-lookup"><span data-stu-id="511df-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="511df-124">Valitse **Raja** avataksesi **Raja**-sivun, jolla voit tarkistaa tiettyyn TDS-verokoodiin liitetylle TDS-verokomponentille määritetyn raja-arvon.</span><span class="sxs-lookup"><span data-stu-id="511df-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="511df-125">Valitse **Kaavan suunnittelutoiminto** avataksesi **Kaavan suunnittelutoiminto** -sivun, jossa voit tarkistaa tietylle TDS-verokoodille määritetyn kaavan.</span><span class="sxs-lookup"><span data-stu-id="511df-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="511df-126">Kirjaa vapaatekstilasku.</span><span class="sxs-lookup"><span data-stu-id="511df-126">Post the free text invoice.</span></span> <span data-ttu-id="511df-127">Vapaatekstilaskulle laskettu TDS-summa kirjataan myyntireskontratilille, joka on määritetty kullekin TDS-verokoodille TDS-ryhmässä.</span><span class="sxs-lookup"><span data-stu-id="511df-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="511df-128">TDS-verokoodien myyntireskontran tilit määritetään **Ennakonpidätyskoodit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="511df-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="511df-129">Valitse **Kirjattu ennakonpidätys** avataksesi **Ennakonpidätystapahtumat**-sivun.</span><span class="sxs-lookup"><span data-stu-id="511df-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="511df-130">**Arvo**-kenttä näyttää tapahtuman TDS:n laskemiseen käytettävän kokonaisprosentin.</span><span class="sxs-lookup"><span data-stu-id="511df-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="511df-131">**Yhteenveto**-, **Yleinen**- ja **Summa**-välilehtien kentissä on näkyvissä laskuriveille lasketut TDS-summat.</span><span class="sxs-lookup"><span data-stu-id="511df-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="511df-132">Tarkastele kunkin TDS-ryhmään liitetyn TDS-verokoodin TDS-laskentatietoja.</span><span class="sxs-lookup"><span data-stu-id="511df-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
