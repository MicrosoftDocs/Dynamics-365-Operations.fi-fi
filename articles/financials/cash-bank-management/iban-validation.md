---
title: "Kansainvälisen tilinumero (IBAN) tarkistuksen hallinta"
description: "Tässä ohjeaiheessa käsitellään kansainvälisen tilinumero (IBAN) tarkistuksen hallintaa."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: fi-fi
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="113db-103">Kansainvälisen tilinumero (IBAN) tarkistuksen hallinta</span><span class="sxs-lookup"><span data-stu-id="113db-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="113db-104">Kansainvälisen tilinumeron (IBAN) tarkistus täydentää tarkistusta, joka tehdään, kun lisäät IBAN-numeron pankkitiliin.</span><span class="sxs-lookup"><span data-stu-id="113db-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="113db-105">IBAN-numeron rakenne on tallennettu Microsoft Dynamics 365 for Finance and Operationsiin, ja se ladataan automaattisesti, kun käytät IBAN-numeroa ensimmäisen kerran pankkitileillä.</span><span class="sxs-lookup"><span data-stu-id="113db-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="113db-106">Pankkitilin numero on osa IBAN-numeron määritettyä rakennetta.</span><span class="sxs-lookup"><span data-stu-id="113db-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="113db-107">Jos IBAN-numerossa olevan tilinumeron sijainti tai pituus ei tämän rakenteen perusteella vastaa sijaintia, joka on määritetty kunkin maan tai alueen rakenteessa, saat varoitussanoman.</span><span class="sxs-lookup"><span data-stu-id="113db-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="113db-108">IBAN-rakenteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="113db-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="113db-109">Valitse **Maksuliikenteen hallinta \> Asetukset \> IBAN-rakenteet**.</span><span class="sxs-lookup"><span data-stu-id="113db-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="113db-110">Huomaa, että kunkin maan tai alueen IBAN-rakenteet on määritetty automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="113db-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="113db-111">Jos tietyn maan tai alueen rakenteita on mukautettava, voit muokata niitä.</span><span class="sxs-lookup"><span data-stu-id="113db-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="113db-112">Rakenteen määritykset sisältyvät jokaiseen uuteen julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="113db-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="113db-113">Voit ladata uusimmat määritelmät kunkin päivityksen jälkeen **Palauta rakenteet** -valikosta.</span><span class="sxs-lookup"><span data-stu-id="113db-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="113db-114">Pankkitilin IBAN-rakenteen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="113db-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="113db-115">Valitse **Maksuliikenteen hallinta \> Pankkitilit \> Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="113db-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="113db-116">Luo pankkitili.</span><span class="sxs-lookup"><span data-stu-id="113db-116">Create a bank account.</span></span>
3. <span data-ttu-id="113db-117">Anna IBAN-numero **Lisätiedot**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="113db-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="113db-118">Jos IBAN-numerossa olevan tilinumeron sijainti tai pituus ei vastaa sijaintia, joka on määritetty kunkin maan tai alueen rakenteessa, saat ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="113db-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="113db-119">Et voi jatkaa, jos IBAN-numeron pituus ei vastaa IBAN-rakenteessa olevaa pituutta.</span><span class="sxs-lookup"><span data-stu-id="113db-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="113db-120">Tarkistus vahvistaa myös, että pankkitilin numero vastaa IBAN-numeron pankkitilin numeroa vastaavaa osaa.</span><span class="sxs-lookup"><span data-stu-id="113db-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="113db-121">Jos pankkitilin numero ei vastaa sitä, näyttöön avautuu varoitussanoma.</span><span class="sxs-lookup"><span data-stu-id="113db-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="113db-122">Tämä sanoma on vain varoitus.</span><span class="sxs-lookup"><span data-stu-id="113db-122">This message is only a warning.</span></span> <span data-ttu-id="113db-123">Voit jatkaa, vaikka ei pankkitilin numero ei vastaa IBAN-numeroa.</span><span class="sxs-lookup"><span data-stu-id="113db-123">You can continue even if the bank account number doesn't match.</span></span>

