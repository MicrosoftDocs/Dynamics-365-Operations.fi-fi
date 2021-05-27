---
title: Päivitä sertifikaattinumerot ja päivämäärät TDS-tapahtumille
description: Tässä aiheessa kuvataan, kuinka palautustodistuksen numerot ja päivämäärät, jotka on tallennettu toimittajalle, asiakkaalle tai kirjanpitotileille Vero vähennettynä lähteissä (TDS) -tapahtumille.
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023204"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="4a6fa-103">Päivitä sertifikaattinumerot ja päivämäärät TDS-tapahtumille</span><span class="sxs-lookup"><span data-stu-id="4a6fa-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a6fa-104">Tässä aiheessa kuvataan, kuinka palautustodistuksen numerot ja päivämäärät, jotka on tallennettu toimittajalle, asiakkaalle tai kirjanpitotileille Vero vähennettynä lähteissä (TDS) -tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="4a6fa-105">Voit tarkastella TDS-tapahtumien todistuksia **Palautustodistukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="4a6fa-106">Voit päivittää todistukset **Päivitä todistukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="4a6fa-107">Päivitä TDS-tapahtumien todistusnumerot ja -päivämäärät noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="4a6fa-108">Valitse **Vero \> Ilmoitukset \> Ennakonpidätys \> Päivitä todistus**.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="4a6fa-109">[![Päivitä todistus -sivu](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="4a6fa-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="4a6fa-110">Valitse **Päivitä todistus** -sivun **Valitse**-osassa **Verotyyppi**-kentässä **TDS**.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="4a6fa-111">Valitse **Todistusnumero**-kentässä asiakkaan tai toimittajan TDS-todistuksen numero.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4a6fa-112">**Todistusnumero**-kentässä luetellaan vain ne TDS-todistusten numerot, joissa **Suljettu**-valintaruudun valinta on poistettu **Palautustodistukset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="4a6fa-113">**Todistuspäivämäärä**-kentässä on näkyvissä todistuspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="4a6fa-114">**Tilityyppi**-kentässä näkyy tilityyppi, jota varten TDS-todistusnumero vastaanotetaan, ja nimikentässä näkyy tilin **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="4a6fa-115">Valitse **Päivämäärästä**- ja **Päivämäärään**-kentissä sen kauden alkamis- ja päättymispäivät, joille TDS-tapahtumat näytetään.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="4a6fa-116">Valitse **Näytä tiedot**, jos haluat tarkastella valitulla kaudella kirjattuja TDS-tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="4a6fa-117">Yläruudun **Yhteenveto**-välilehdessä näkyy seuraavat tiedot kaikista toimittajalle tai asiakkaalle valitun kauden aikana kirjatuista TDS-tapahtumista:</span><span class="sxs-lookup"><span data-stu-id="4a6fa-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="4a6fa-118">**Tosite** – TDS-tapahtuman tositenumero.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="4a6fa-119">**Päivämäärä** – TDS-tapahtuman päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="4a6fa-120">**Summa** – Laskun summa, jonka perusteella TDS laskettiin.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="4a6fa-121">**Veron summa** – Tapahtumalle laskettu TDS-veron summa.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="4a6fa-122">Jos haluat siirtää tiettyjä TDS-tapahtumia ylemmästä ruudukosta alempaan ruudukkoon, valitse tapahtumat ja valitse sitten **Sisällytä**.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="4a6fa-123">Vaihtoehtoisesti voit siirtää kaikki TDS-tapahtumat ylemmästä ruudukosta alempaan ruudukkoon valitsemalla **Sisällytä kaikki**.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="4a6fa-124">Jos haluat siirtää tiettyjä TDS-tapahtumia tai kaikki TDS-tapahtumat alemmasta ruudukosta yläruudukkoon, käytä **Sulje pois**- tai **Sulje pois kaikki** -painiketta.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="4a6fa-125">Valitse **Päivitä** päivittääksesi **Todistusnumero**- ja **Todistuspäivämäärä**-kentät TDS-tapahtumille alemmassa ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="4a6fa-126">Valitse **Vero \> Välilliset verot \> Ennakonpidätys \> Palautustodistus** ja valitse **Kysely**, jos haluat tarkastella päivitettyjä tapahtumarivejä, joissa on uudet todistusnumerot **Todistustapahtumat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4a6fa-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="4a6fa-127">[![Todistustapahtumat-sivu](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="4a6fa-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
