---
title: Tallenna TDS-palautustodistuksen numerot
description: Tässä aiheessa kuvataan, kuinka Palautustodistukset-sivulla tallennetaan todistusnumerot ja -päivämäärät tietylle toimittajalle, asiakkaalle tai kirjanpitoon vastaanotettavat Vero vähennettynä lähteissä (TDS) -todistuksista.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023194"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="e904e-103">Tallenna TDS-palautustodistuksen numerot</span><span class="sxs-lookup"><span data-stu-id="e904e-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e904e-104">Tässä aiheessa kuvataan, kuinka **Palautustodistukset**-sivulla tallennetaan todistusnumerot ja -päivämäärät tietylle toimittajalle, asiakkaalle tai kirjanpitoon vastaanotettavat Vero vähennettynä lähteissä (TDS) -todistuksista.</span><span class="sxs-lookup"><span data-stu-id="e904e-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="e904e-105">Voit päivittää tälle sivulle TDS-tapahtumiin tallennetut TDS-todistusnumerot ja -päivämäärät valitsemalla **Päivitä sertifikaatti** -sivu (**Kirjanpito \> Kausittainen \> Ennakonpidätys \> Päivitä sertifikaatti**).</span><span class="sxs-lookup"><span data-stu-id="e904e-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="e904e-106">Kun olet lopettanut TDS-sertifikaattien numeroiden päivittämisen, sulje ne.</span><span class="sxs-lookup"><span data-stu-id="e904e-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="e904e-107">Tallenna TDS-todistusnumerot ja -päivämäärät noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="e904e-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="e904e-108">Siirry kohtaan **Vero \> Välillinen vero \> Ennakonpidätys \> Palautustodistukset**.</span><span class="sxs-lookup"><span data-stu-id="e904e-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="e904e-109">[![Palautustodistukset-sivu](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="e904e-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="e904e-110">Valitse **Palautustodistukset**-sivun **Verotyyppi**-kentässä valitse **TDS**.</span><span class="sxs-lookup"><span data-stu-id="e904e-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="e904e-111">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e904e-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="e904e-112">Kirjoita **Todistusnumero**-kenttään TDS-huojennustodistuksen numero.</span><span class="sxs-lookup"><span data-stu-id="e904e-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="e904e-113">Valitse **Tilityyppi**-kentässä tilityyppi, jota varten TDS-todistus vastaanotetaan: **Toimittaja**, **Asiakas** tai **Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="e904e-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="e904e-114">Valitse **Tili**-kentässä toimittaja-, asiakas- tai kirjanpitotilinumero valitsemasi tilityypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="e904e-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="e904e-115">**Nimi**-kentässä näkyy toimittajan, asiakkaan tai kirjanpitotilin nimi.</span><span class="sxs-lookup"><span data-stu-id="e904e-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="e904e-116">Syötä **Todistuksen summa** -kenttään TDS-todistuksen summa.</span><span class="sxs-lookup"><span data-stu-id="e904e-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="e904e-117">Kirjoita **Päivämäärä**-kenttään todistusnumeron todistuspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e904e-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="e904e-118">Avaa **Todistustapahtumat**-sivu valitsemalla **Kyselyt**. Sivulla voit tarkastella TDS-tapahtumia, joille TDS-sertifikaatin numero ja päivämäärä päivitetään.</span><span class="sxs-lookup"><span data-stu-id="e904e-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="e904e-119">Nämä tiedot voidaan päivittää **Päivitä sertifikaatti** -sivulla (**Vero \> Ilmoitukset \> Ennakonpidätys \> Päivitä sertifikaatti**).</span><span class="sxs-lookup"><span data-stu-id="e904e-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="e904e-120">**Päivitä sertifikaatti** -sivulla näkyvät seuraavat tiedot kutakin TDS-tapahtumaa varten:</span><span class="sxs-lookup"><span data-stu-id="e904e-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="e904e-121">**Päivämäärä** – TDS-tapahtuman kirjauspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e904e-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="e904e-122">**Tosite** – TDS-tapahtuman tositenumero.</span><span class="sxs-lookup"><span data-stu-id="e904e-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="e904e-123">**Lähde** – Moduuli, jolle TDS-tapahtuma luotiin.</span><span class="sxs-lookup"><span data-stu-id="e904e-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="e904e-124">**Tili** – Toimittajan, asiakkaan tai kirjanpitotilin numero, jota varten TDS-tapahtuma luotiin.</span><span class="sxs-lookup"><span data-stu-id="e904e-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="e904e-125">**Nimi** – Toimittajan, asiakkaan tai kirjanpitotilin nimi, jota varten TDS-tapahtuma luotiin.</span><span class="sxs-lookup"><span data-stu-id="e904e-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="e904e-126">**Summa** – Laskun summa, jonka perusteella TDS laskettiin.</span><span class="sxs-lookup"><span data-stu-id="e904e-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="e904e-127">**Veron summa** – Tapahtumalle laskettu TDS-veron summa.</span><span class="sxs-lookup"><span data-stu-id="e904e-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="e904e-128">**Todistuspäivämäärä** – TDS-todistuksen päivämäärä, joka päivitettiin TDS-tapahtumaa varten.</span><span class="sxs-lookup"><span data-stu-id="e904e-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="e904e-129">**Todistusnumero** – TDS-todistuksen numero, joka päivitettiin TDS-tapahtumaa varten.</span><span class="sxs-lookup"><span data-stu-id="e904e-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="e904e-130">Valitse **Palautustodistukset** -sivulla **Suljettu**-valintaruutu, jos haluat sulkea TDS-todistuksen numeron sen jälkeen, kun olet päivittänyt sen TDS-tapahtumille **Päivitä sertifikaatti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e904e-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="e904e-131">Voit valita sivun kaikkien tietueiden **Suljettu**-valintaruudun valitsemalla **Merkitse kaikki**.</span><span class="sxs-lookup"><span data-stu-id="e904e-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e904e-132">TDS-todistuksen numerot, joille **Suljettu**-valintaruutu on valittuna, eivät ole käytettävissä **Päivitä sertifikaatti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e904e-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
