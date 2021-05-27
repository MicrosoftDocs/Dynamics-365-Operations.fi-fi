---
title: Määritä myyntireskontran ja ostoreskontran TDS-parametrit
description: Tässä ohjeaiheessa on tietoja ostoreskontran ja myyntireskontran parametrien määrittämisestä niin, että ne tukevat Vero vähennettynä lähteissä (TDS) -vähennyksiä.
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023208"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="d7430-103">Määritä myyntireskontran ja ostoreskontran TDS-parametrit</span><span class="sxs-lookup"><span data-stu-id="d7430-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7430-104">Tässä ohjeaiheessa on tietoja ostoreskontran ja myyntireskontran parametrien määrittämisestä niin, että ne tukevat Vero vähennettynä lähteissä (TDS) -vähennyksiä.</span><span class="sxs-lookup"><span data-stu-id="d7430-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="d7430-105">Valitse **Vero \> Asetukset \> Parametrit \> Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="d7430-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="d7430-106">Valitse **Päivitykset**-välilehdessä **Päivitä tilausrivit** avataksesi **Päivitä tilausrivit** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="d7430-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="d7430-107">Määritä **TDS-ryhmä**-osan **Päivitä TDS-ryhmä** -kentässä menetelmä, jolla TDS-ryhmä päivitetään rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="d7430-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="d7430-108">Tätä asetusta käytetään, kun TDS-ryhmä päivitetään tilauksen otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="d7430-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="d7430-109">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="d7430-109">The following options are available:</span></span>

    - <span data-ttu-id="d7430-110">**Ei koskaan** – TDS-ryhmää ei päivitetä tilausriveille, kun se päivitetään tilauksen otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="d7430-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="d7430-111">**Aina** – TDS-ryhmä päivitetään automaattisesti tilausriveille, kun se päivitetään tilauksen otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="d7430-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="d7430-112">**Kehote** – Käyttäjät saavat sanoman, joka kehottaa heitä päivittämään TDS-ryhmän tilausriveille.</span><span class="sxs-lookup"><span data-stu-id="d7430-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="d7430-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7430-113">Select **OK**.</span></span>

    <span data-ttu-id="d7430-114">[![Päivitä tilausrivit -valintaikkuna](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="d7430-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="d7430-115">Valitse **Vero \> Asetukset \> Parametrit \> Ostoreskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="d7430-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="d7430-116">**Yleiset**-välilehdessä **Jako toimitustietojen perusteella** -pikavälilehdessä määritä **Tuotteen vastaanotto** -kohdan asetukseksi **Kyllä**, kun haluat kirjata ja jakaa tuotteen vastaanoton, jolla on eri toimitusosoitteet ja verotilien numerot (TAN).</span><span class="sxs-lookup"><span data-stu-id="d7430-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="d7430-117">Jos tämän asetuksen arvoksi on määritetty **Ei**, et voi kirjata oston pakkausluetteloa, jolla on eri toimitusosoitteet ja TAN-numerot.</span><span class="sxs-lookup"><span data-stu-id="d7430-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="d7430-118">Määritä **Lasku**-asetuksen arvoksi **Kyllä**, jos haluat kirjata ja jakaa ostolaskun, jolla on eri toimitusosoitteet ja TAN-numerot.</span><span class="sxs-lookup"><span data-stu-id="d7430-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="d7430-119">[![Jako toimitustietojen perusteella -pikavälilehti](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="d7430-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="d7430-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="d7430-120">Close the page.</span></span>
