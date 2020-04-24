---
title: Varastotyön peruutus poikkeusten käsittelyä varten
description: Tässä aiheessa kuvaillaan Peruuta työ -toiminto, jonka avulla varastojen esimiehet voivat käsitellä estynyttä työtä.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cb725885fb48293a08915f13a4fb14085e930444
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205802"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="affa4-103">Varastotyön peruutus poikkeusten käsittelyä varten</span><span class="sxs-lookup"><span data-stu-id="affa4-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="affa4-104">Microsoft Dynamics 365 Supply Chain Managementin Peruuta työ -toiminnon avulla järjestelmänvalvoja voi peruuttaa tietyn käynnissä olevan varastotyön, jonka järjestelmä on estänyt tai jota ei voida suorittaa loppuun erityisolosuhteiden vuoksi.</span><span class="sxs-lookup"><span data-stu-id="affa4-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="affa4-105">Tämä toiminto on houkutteleva ja turvallinen vaihtoehto korjaaville SQL-komentosarjoille, jotka korjaavat epäyhtenäisiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="affa4-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="affa4-106">Vaikka näitä komentosarjoja pyydetään yleensä IT-ammattilaisilta, Peruuta työ -toimintoa voivat käyttää yrityksen käyttäjät, joilla on järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="affa4-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="affa4-107">Voit käyttää Peruuta työ -toimintoa kohdassa **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Puhdista \> Peruuta työ**.</span><span class="sxs-lookup"><span data-stu-id="affa4-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="affa4-108">Määritä peruutettavan työn työtunnus **Peruuta työ** -valintaikkunassa ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="affa4-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="affa4-109">Varastotyöt, jotka voidaan peruuttaa</span><span class="sxs-lookup"><span data-stu-id="affa4-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="affa4-110">Varaston keräilytoimien yhteydessä työntekijä voi kohdata tilanteita, jossa hän on rekisteröinyt määriä kerätyksi varastointipaikasta käyttäjäpaikkaansa, mutta ei voi rekisteröidä asetustoimea.</span><span class="sxs-lookup"><span data-stu-id="affa4-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="affa4-111">Epäyhtenäiset varastotiedot ovat usein, mutta eivät aina, syynä työn estymiseen.</span><span class="sxs-lookup"><span data-stu-id="affa4-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="affa4-112">Toisin kuin tavanomainen Peruuta-toiminto, jota voidaan käyttää työotsikon **Peruuta**-painikkeella, Peruuta työ -toiminto ei edellytä, että viimeinen valmis työrivi on **Astus**-tyypin työrivi.</span><span class="sxs-lookup"><span data-stu-id="affa4-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="affa4-113">Toisin sanoen peruutuslogiikka voidaan suorittaa Peruuta työ -toiminnon osalta, vaikka työrivin nimikemäärä on käyttäjäsijainnissa.</span><span class="sxs-lookup"><span data-stu-id="affa4-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="affa4-114">Toiminnallisista syistä peruutettavassa työssä varaston käyttäjien on edelleen käytettävä työsivun tavallista Peruuta-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="affa4-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="affa4-115">Peruuta työ -toimintoa voidaan käyttää vain tyyppien **Myynti**, **Siirtovarasto-otto**, **Raaka-aineiden keräily** tai **Täydennys** työn peruuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="affa4-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="affa4-116">Peruutuslogiikka ei suoriteta jäädytettyjen raaka-aineiden keräilytöiden osalta eikä sellaisten töiden osalta, jotka voidaan peruuttaa tavallisella Peruuta-toiminnolla (katso edellinen huomautus).</span><span class="sxs-lookup"><span data-stu-id="affa4-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="affa4-117">Saadakseen työn jatkumaan järjestelmä peruuttaa jäljellä olevat työrivit ja korjaa käyttäjän määrittämään työtunnukseen liittyvät varastotiedot.</span><span class="sxs-lookup"><span data-stu-id="affa4-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="affa4-118">Tämän jälkeen tavalliset varaston käsittelytoimet, jotka kohdistuvat aiemmin estyneeseen nimikemäärään, voivat jatkua.</span><span class="sxs-lookup"><span data-stu-id="affa4-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="affa4-119">Asettaakseen aiemmin estyneen nimikkeen tiettyyn sijaintiin työn peruuttamisen jälkeen käyttäjän on käytettävä varaston siirtotapahtumaa tai määrän oikaisua mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="affa4-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
