---
title: Toimitustavan muuttaminen myyntipisteessä
description: Tässä ohjeaiheessa kuvataan, miten voit määrittää ja käyttää myyntipisteen toimitustilan toimintoa.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 26e798c664844b575de6f019ad8f5349ed92be98
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/10/2020
ms.locfileid: "3114401"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="4f560-103">Toimitustavan muuttaminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="4f560-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4f560-104">Tässä ohjeaiheessa kerrotaan, miten myyntipisteympäristön toimitustilan muutostoiminto määritetään ja miten sitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="4f560-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="4f560-105">Dynamics 365 Commercen versiossa 10.0.10 ja myöhemmissä versioissa **Muuta toimitustilaa** -toiminto (647) on käytettävissä ja lisättävissä myyntipisteen näyttöjen asetteluihin.</span><span class="sxs-lookup"><span data-stu-id="4f560-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="4f560-106">Muuta toimitustilaa -toiminnon avulla voit muuttaa toimitustilaa yhdellä tai usealla lähetyksen määrittämällä myyntirivillä myyntipisteen tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="4f560-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="4f560-107">Commercen edellisissä versioissa piti käyttää koko **Lähetä kaikki**- tai **Lähetä valitut** -konfigutointityönkulkuja, jos toimitustilaa haluttiin muuttaa lähetykselle määritetyllä olemassa olevalla rivillä.</span><span class="sxs-lookup"><span data-stu-id="4f560-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="4f560-108">Tämä prosessi vei paljon aikaa ja tuloksena saattoi olla tahattomia muutoksia rivin toimituksen alkuperään tai toimituspäiviin.</span><span class="sxs-lookup"><span data-stu-id="4f560-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="4f560-109">Uusi toiminto tarjoaa vaihtoehtoisen tavan näiden myyntirivien toimitustilan tehokkaaseen päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="4f560-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="4f560-110">Lisätietoja toiminnon lisäämisestä painikkeeseen myyntipisteen painikeruudukossa on kohdassa [Myyntipisteen näyttöjen asettelut](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="4f560-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="4f560-111">Kun tämä toiminto on määritetty myyntipisteessä ja valitset **Muuta toimitustilaa**, näyttöön tulee luettelosivu, jonka avulla voit valita sen tapahtuman rivit, joiden toimitustilaa haluat muuttaa.</span><span class="sxs-lookup"><span data-stu-id="4f560-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="4f560-112">Voit valita osan riveistä tai kaikki rivit tai poistua tekemättä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="4f560-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="4f560-113">Myyntirivit, jotka määritettiin aiemmin lähetykselle, ovat luettelon ainoat muutettavissa olevat rivit.</span><span class="sxs-lookup"><span data-stu-id="4f560-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="4f560-114">Jos haluat muuttaa riviä, joka on määritetty keräykseen tai liikkeestä noudettavaksi, käytä **Lähetä kaikki**- tai **Lähetä valitut** -toimintoja.</span><span class="sxs-lookup"><span data-stu-id="4f560-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="4f560-115">Vastaavasti jos haluat muuttaa riviä, joka on määritetty kerättäväksi tai liikkeestä noudettavaksi lähetykseksi, käytä **Kerää kaikki**-, **Kerää valitut**-, **Nouda kaikki**- tai **Nouda valitut** -toimintoja.</span><span class="sxs-lookup"><span data-stu-id="4f560-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="4f560-116">Kun olet valinnut muutettavan rivin, valitse **Muuta toimitustilaa**. Tällöin sinua pyydetään valitsemaan toimitustilavaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="4f560-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="4f560-117">Jos valitsit useita muutettavia rivejä, myyntipiste näyttää vain toimitustilat, jotka on määritetty sallituksi kaikille valituille tuotteille.</span><span class="sxs-lookup"><span data-stu-id="4f560-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="4f560-118">Toimitustilat voidaan määrittää tukemaan tiettyjä tuotteita ja toimitusosoitteita.</span><span class="sxs-lookup"><span data-stu-id="4f560-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="4f560-119">Jos olemassa on toimitustila, joka on sallittu yhdelle tuotteen ja osoitteen yhdistelmälle, mutta ei toiselle valitun tuotteen ja osoitteen yhdistelmälle, toimitustila ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4f560-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="4f560-120">Sinun on ehkä valittava rivit yksitellen ja muutettava toimitustila jokaiselle riville erikseen, jos haluat valita toimitustilan yhdelle tuotteelle, jota toinen tuote ei tue.</span><span class="sxs-lookup"><span data-stu-id="4f560-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="4f560-121">Kun olet valinnut uuden toimitustilan, näkyviin tulee tapahtumasivu.</span><span class="sxs-lookup"><span data-stu-id="4f560-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="4f560-122">Voit tarkistaa uudet toimitustilavalinnat valitsemalla tapahtumaluettelosta **Toimitus**-välilehden.</span><span class="sxs-lookup"><span data-stu-id="4f560-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>   
