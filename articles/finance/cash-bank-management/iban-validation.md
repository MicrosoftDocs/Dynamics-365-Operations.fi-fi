---
title: Kansainvälisen tilinumero (IBAN) tarkistuksen hallinta
description: Tässä ohjeaiheessa käsitellään kansainvälisen tilinumero (IBAN) tarkistuksen hallintaa.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e44b855165752baeb42d3c9952c35982ef24b0f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815857"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="bb7fe-103">Kansainvälisen tilinumero (IBAN) tarkistuksen hallinta</span><span class="sxs-lookup"><span data-stu-id="bb7fe-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb7fe-104">Kansainvälisen tilinumeron (IBAN) tarkistus täydentää tarkistusta, joka tehdään, kun lisäät IBAN-numeron pankkitiliin.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="bb7fe-105">Microsoft Dynamics 365 Financeen on tallennettu tietoja IBAN-rakenteesta.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="bb7fe-106">Nämä tiedot ladataan automaattisesti, kun käytät IBAN-numeroa ensimmäisen kerran pankkitileissä.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="bb7fe-107">Tiedot sisältävät IBAN-numeron pituuden, tilinumeron ja pankkikoodin aloituskohdat sekä tilinumeron ja pankkikoodin pituuden.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="bb7fe-108">IBAN-rakenteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bb7fe-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="bb7fe-109">Valitse **Maksuliikenteen hallinta \> Asetukset \> IBAN-rakenteet**.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="bb7fe-110">Huomaa, että kunkin maan tai alueen IBAN-rakenteet on määritetty automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="bb7fe-111">Jos haluat mukauttaa tietyn maan tai alueen rakenteita, voit muokata niitä.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="bb7fe-112">Rakenteen määritykset sisältyvät jokaiseen uuteen julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="bb7fe-113">Voit ladata uusimmat määritelmät kunkin päivityksen jälkeen **Palauta rakenteet** -valikosta.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="bb7fe-114">Pankkitilin IBAN-rakenteen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="bb7fe-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="bb7fe-115">Valitse **Maksuliikenteen hallinta \> Pankkitilit \> Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="bb7fe-116">Luo pankkitili.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-116">Create a bank account.</span></span>
3. <span data-ttu-id="bb7fe-117">Anna IBAN-numero **Lisätiedot**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="bb7fe-118">Jos IBAN-numeron pituus ei vastaa kullekin maalle tai alueelle määritettyä pituutta, saat siitä ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="bb7fe-119">Et voi jatkaa, jos IBAN-numeron pituus ei vastaa IBAN-rakenteessa määritettyä pituutta.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="bb7fe-120">Tarkistus vahvistaa myös, että pankkitilin numero vastaa IBAN-numeron pankkitilin numeroa vastaavaa osaa.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="bb7fe-121">Jos pankkitilin numero ei vastaa sitä, siitä varoitetaan.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="bb7fe-122">Tämä sanoma on vain varoitus.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-122">This message is only a warning.</span></span> <span data-ttu-id="bb7fe-123">Voit jatkaa, vaikka ei pankkitilin numero ei vastaa IBAN-numeroa.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="bb7fe-124">Tarkistus vahvistaa myös, että pankkikoodi vastaa IBAN-numeron pankkikoodia vastaavaa osaa.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="bb7fe-125">Pankkikoodi sisältää pankin numeron ja usein myös toinen pankin konttori.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="bb7fe-126">Jos pankkikoodi numero ei vastaa sitä, siitä varoitetaan.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="bb7fe-127">Tämä sanoma on vain varoitus.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-127">This message is only a warning.</span></span> <span data-ttu-id="bb7fe-128">Voit jatkaa, vaikka pankkikoodi ei vastaa IBAN-numeroa.</span><span class="sxs-lookup"><span data-stu-id="bb7fe-128">You can continue even if the bank routing number doesn't match.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]