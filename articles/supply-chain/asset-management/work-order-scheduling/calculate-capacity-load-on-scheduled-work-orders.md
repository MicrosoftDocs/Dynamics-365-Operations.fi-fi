---
title: Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen
description: Tässä ohjeaiheessa selitetään, kuinka voit laskea kapasiteettikuormituksen ajoitetuille työtilauksille käyttöomaisuuden hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215352"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="83307-103">Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen</span><span class="sxs-lookup"><span data-stu-id="83307-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="83307-104">Voit laskea ajoitettujen työtilausten kapasiteetin kuormituksen, jolloin saat yleiskuvan resurssien työkuormituksesta tietyltä kaudelta.</span><span class="sxs-lookup"><span data-stu-id="83307-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="83307-105">Voit tehdä laskelmia seuraavista resursseista: Kunnossapitotyöntekijät, työntekijäryhmät, työkalut ja resurssit.</span><span class="sxs-lookup"><span data-stu-id="83307-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="83307-106">Valitse **Resurssien hallinta** > **Kyselyt** > **Ajoitus** > **Kapasiteetin kuormitus**.</span><span class="sxs-lookup"><span data-stu-id="83307-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="83307-107">Valitse **Laske kapasiteetin kuormitus** -valintaikkunan **Näytä**-kentässä, minkä kuormitustyypin haluat laskea: **Kapasiteetti**, **Varattu** vai **Jäljellä oleva määrä**.</span><span class="sxs-lookup"><span data-stu-id="83307-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="83307-108">Valitse **Kyllä** **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa on nolla.</span><span class="sxs-lookup"><span data-stu-id="83307-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="83307-109">Valitse resurssityypit, joille haluat laskea kapasiteetin kuormituksen, valitsemalla **Kyllä** asiaankuuluvissa vaihtopainikkeissa: **Työntekijä**, **Ylläpitotyöntekijäryhmä**, **Työkalu** ja **Resurssi**.</span><span class="sxs-lookup"><span data-stu-id="83307-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="83307-110">Valitse aloituspäivämäärä laskennalle **Aloituspäivämäärä**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="83307-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="83307-111">Valitse **Välityyppi**-kentästä laskutoimitusten väli: **Päivä**, **Viikko**, **Kuukausi** tai **Vuosineljännes**.</span><span class="sxs-lookup"><span data-stu-id="83307-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="83307-112">Lisää **Jakson frekvenssi** -kenttään, kuinka monta aikaväliä haluat laskea.</span><span class="sxs-lookup"><span data-stu-id="83307-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="83307-113">Jos esimerkiksi olet valinnut aika välityypiksi **Päivä** ja lisäät tähän kenttään numeron "5", aloituspäivämäärästä lasketaan viisi päivää eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="83307-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="83307-114">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="83307-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="83307-115">Alla oleva kuva näyttää tuloksen, joka kattaa kolme viikkoa kuormitustyypistä **Varattu**.</span><span class="sxs-lookup"><span data-stu-id="83307-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Kuva 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="83307-117">Jos laskennalle valitaan kuormitustyypit **Kapasiteetti** tai **Jäljellä oleva määrä**, sama tulos tulee näkyviin, jos valitun kauden resursseille ei ole tehty varauksia.</span><span class="sxs-lookup"><span data-stu-id="83307-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="83307-118">Lisätietoja ylläpitoaikataulurivien kapasiteetin kuormituksen laskemisesta ja ajoittamattomista työtilauksista on kohdassa [Kapasiteetin kuormituksen laskeminen](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="83307-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

