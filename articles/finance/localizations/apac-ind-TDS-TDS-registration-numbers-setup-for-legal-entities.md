---
title: TDS-rekisteröintinumeroiden lisääminen yrityksille
description: Tässä aiheessa kuvataan, miten Vero vähennettynä lähteissä (TDS) -rekisteröintinumerot määritetään yrityksille.
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
ms.openlocfilehash: 3550b2b7b305702ffc337ba0a9bb79f60a9de120
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023205"
---
# <a name="set-up-tds-registration-numbers-for-legal-entities"></a><span data-ttu-id="ab97a-103">TDS-rekisteröintinumeroiden lisääminen yrityksille</span><span class="sxs-lookup"><span data-stu-id="ab97a-103">Set up TDS registration numbers for legal entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab97a-104">Tässä aiheessa kuvataan, miten Vero vähennettynä lähteissä (TDS) -rekisteröintinumerot määritetään yrityksille.</span><span class="sxs-lookup"><span data-stu-id="ab97a-104">This topic explains how to set up Tax Deducted at Source (TDS) registration numbers for legal entities.</span></span>

1. <span data-ttu-id="ab97a-105">Valitse **Organisaation hallinto \> Organisaatiot \> Yritykset**.</span><span class="sxs-lookup"><span data-stu-id="ab97a-105">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

    <span data-ttu-id="ab97a-106">[![Yritykset-sivu](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span><span class="sxs-lookup"><span data-stu-id="ab97a-106">[![Legal entities page](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span></span>

2. <span data-ttu-id="ab97a-107">Syötä **Verotiedot**-pikavälilehden **Pysyvä tilinumero** -kenttään yrityksen pysyvä tilinumero (PAN).</span><span class="sxs-lookup"><span data-stu-id="ab97a-107">On the **Tax information** FastTab, in the **Permanent account number** field, enter the permanent account number (PAN) of the legal entity.</span></span>
3. <span data-ttu-id="ab97a-108">Kirjoita **Ympyrän numero** -kenttään TDS-viranomaisen ympyrän numero.</span><span class="sxs-lookup"><span data-stu-id="ab97a-108">In the **Circle number** field, enter the circle number of the TDS authority.</span></span>
4. <span data-ttu-id="ab97a-109">Kirjoita **Osaston numero** -kenttään TDS-viranomaisen osaston numero.</span><span class="sxs-lookup"><span data-stu-id="ab97a-109">In the **Ward number** field, enter the ward number of the TDS authority.</span></span>
5. <span data-ttu-id="ab97a-110">Kirjoita **Arvioiva johtaja** -kenttään TDS-viranomaisen arvioivan johtajan tiedot.</span><span class="sxs-lookup"><span data-stu-id="ab97a-110">In the **Assessing officer** field, enter the details of the assessing officer for the TDS authority.</span></span>
6. <span data-ttu-id="ab97a-111">Valitse **Vähennyksen tyyppi** -kentästä yrityksen vähennystyypin luokka.</span><span class="sxs-lookup"><span data-stu-id="ab97a-111">In the **Type of deductor** field, select the deductor type category for the legal entity.</span></span>
7. <span data-ttu-id="ab97a-112">Valitse toimintoruudussa **Rekisteröintitunnukset** avataksesi **Hallitse osoitteita** -sivu.</span><span class="sxs-lookup"><span data-stu-id="ab97a-112">On the Action Pane, select **Registration IDs** to open the **Manage addresses** page.</span></span>
8. <span data-ttu-id="ab97a-113">Valitse **Verotiedot**-pikavälilehdellä **Lisää** tai **Muokkaa** avataksesi **Verotietojen hallinta** -sivun, jossa voit ylläpitää verorekisteröintimerkintää.</span><span class="sxs-lookup"><span data-stu-id="ab97a-113">On the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>

    <span data-ttu-id="ab97a-114">[![Osoitteiden hallinta -sivu](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span><span class="sxs-lookup"><span data-stu-id="ab97a-114">[![Manage addresses page](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span></span>

9. <span data-ttu-id="ab97a-115">Kirjoita **Ennakonpidätys**-välilehden **Verotilin numero (TAN)** -kenttään rekisteröintinumero.</span><span class="sxs-lookup"><span data-stu-id="ab97a-115">On the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the registration number.</span></span> <span data-ttu-id="ab97a-116">Tässä numerossa on oltava neljä aakkosmerkkiä, sitten viisi numeromerkkiä ja yksi aakkosmerkki.</span><span class="sxs-lookup"><span data-stu-id="ab97a-116">This number must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="ab97a-117">Tässä on esimerkki: **AXDF87645F**.</span><span class="sxs-lookup"><span data-stu-id="ab97a-117">Here is an example: **AXDF87645F**.</span></span>
10. <span data-ttu-id="ab97a-118">Kirjoita **Nimi tai kuvaus** -kenttään nimikkeen arvonlisävero rekisteröintinumeron kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ab97a-118">In the **Name or description** field, enter a description of the withholding tax registration number.</span></span>

    <span data-ttu-id="ab97a-119">[![Verotietojen hallinta -sivu](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span><span class="sxs-lookup"><span data-stu-id="ab97a-119">[![Manage tax information page](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span></span>

11. <span data-ttu-id="ab97a-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ab97a-120">Close the page.</span></span>
