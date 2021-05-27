---
title: Ennakonpidätyksen veroviranomaisten määrittäminen TDS-verotyypille
description: Tässä aiheessa kerrotaan, miten Vero vähennettynä lähteissä (TDS) -viranomaiset määritetään.
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023200"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="1698b-103">Ennakonpidätyksen veroviranomaisten määrittäminen TDS-verotyypille</span><span class="sxs-lookup"><span data-stu-id="1698b-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1698b-104">Tässä aiheessa kerrotaan, miten Vero vähennettynä lähteissä (TDS) -viranomaiset määritetään.</span><span class="sxs-lookup"><span data-stu-id="1698b-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="1698b-105">Valitse **Vero \> Välilliset verot \> Ennakonpidätysviranomaiset**.</span><span class="sxs-lookup"><span data-stu-id="1698b-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="1698b-106">[![Ennakonpidätysviranomaiset-sivu](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="1698b-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="1698b-107">Valitse **Verotyyppi**-kentässä **TDS**, jos haluat määrittää ennakonpidätysviranomaiset TDS-verotyypille.</span><span class="sxs-lookup"><span data-stu-id="1698b-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="1698b-108">Valitse toimintoruudussa **Uusi** ja luo rivi.</span><span class="sxs-lookup"><span data-stu-id="1698b-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="1698b-109">Kirjoita **Ennakonpidätysviranomainen**-kenttään TDS-viranomaisen nimi.</span><span class="sxs-lookup"><span data-stu-id="1698b-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="1698b-110">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="1698b-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1698b-111">Valitse **Yleiset**-pikavälilehdessä **Toimittajatili**-kentässä TDS-viranomaisen toimittajatili.</span><span class="sxs-lookup"><span data-stu-id="1698b-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1698b-112">Määritä sen pankin nimi, johon TDS-viranomaiselle velkana olevat varat talletetaan.</span><span class="sxs-lookup"><span data-stu-id="1698b-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="1698b-113">Pankin nimi määritetään **Pankkitilit** -sivulla (**Ostoreskontra \> Kaikki toimittajat \> Toimittaja \> Asetukset \> Pankkitilit**).</span><span class="sxs-lookup"><span data-stu-id="1698b-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="1698b-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1698b-114">Close the page.</span></span>
