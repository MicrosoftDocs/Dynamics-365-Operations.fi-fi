---
title: Yleinen ennakonpidätys
description: Tässä ohjeaiheessa on tietoja yleisestä ennakonpidätystoiminnosta ja sen määrittämisestä. Toimittaja- ja asiakastapahtumien yleistä ennakonpidätystoimintoa on parannettu siten, että ennakonpidätys lasketaan nimiketasolla.
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
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075735"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="c16e6-104">Yleinen ennakonpidätys</span><span class="sxs-lookup"><span data-stu-id="c16e6-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c16e6-105">Tässä ohjeaiheessa on tietoja yleisestä ennakonpidätystoiminnosta ja sen määrittämisestä.</span><span class="sxs-lookup"><span data-stu-id="c16e6-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="c16e6-106">Uusi toiminnallisuus on käytettävissä versioissa 10.0.17 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="c16e6-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="c16e6-107">Toimittaja- ja asiakastapahtumien yleistä ennakonpidätystoimintoa on parannettu siten, että ennakonpidätys lasketaan nimiketasolla.</span><span class="sxs-lookup"><span data-stu-id="c16e6-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="c16e6-108">Ostotapahtumien ennakonpidätystilin saldo voidaan selvittää suorittamalla ennakonpidätyksen maksutyö ennakonpidätyksen tilitystiliä vasten.</span><span class="sxs-lookup"><span data-stu-id="c16e6-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="c16e6-109">Yleinen ennakonpidätys ei tue ostotilaus-, toimittajalasku- ja myyntitilaussivujen **Kulujen ylläpito** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="c16e6-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="c16e6-110">Yleisen ennakonpidätyksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="c16e6-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="c16e6-111">Valitse **Ominaisuuksien hallinta** -työtilassa luettelosta **Yleinen ennakonpidätys** ja valitse sitten **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="c16e6-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="c16e6-112">Siirry kohtaan **Vero \> Asetukset \> Parametrit \> Kirjanpitoparametrit** ja määritä **Ennakonpidätys**-välilehden **Ota yleinen ennakonpidätys käyttöön** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c16e6-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="c16e6-113">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c16e6-113">Select **Save**.</span></span>
4. <span data-ttu-id="c16e6-114">Päivitä sivu verkkoselaimessa.</span><span class="sxs-lookup"><span data-stu-id="c16e6-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="c16e6-115">Yleisiä ennakonpidätystoimintoja ei voi ottaa käyttöön maissa tai alueilla, joissa on jo olemassa paikallisia ennakonpidätysratkaisuja.</span><span class="sxs-lookup"><span data-stu-id="c16e6-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="c16e6-116">Näitä alueita ovat muun muassa Intia, Brasilia, Thaimaa, Saudi-Arabia, Irlanti, Yhdistynyt kuningaskunta ja Yhdysvallat.</span><span class="sxs-lookup"><span data-stu-id="c16e6-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
