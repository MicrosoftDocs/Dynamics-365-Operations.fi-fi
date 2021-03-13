---
title: Ajoitettu suoritus
description: Tässä ohjeaiheessa käsitellään ajoitettua suoritusta resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a6d1761202697f62421bbf288c7e22efe559a986
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022404"
---
# <a name="scheduled-execution"></a><span data-ttu-id="4c4d1-103">Ajoitettu suoritus</span><span class="sxs-lookup"><span data-stu-id="4c4d1-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4c4d1-104">Voit määrittää ajoitetun suorituksen työtilauksen palvelutasojen avulla.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="4c4d1-105">(Lisätietoja työtilauksen palvelutasoista on kohdassa [Palvelutaso ja kuvaus](service-level-and-description.md).) Ajoitettu suorittaminen mahdollistaa kunnossapitotyöntekijöiden työsuunnittelun joustavuuden, sillä voit määrittää yksityiskohtaisempia tai vähemmän yksityiskohtaisia vaatimuksia sille aikavälille, jonka aikana työtilaus tulee suorittaa.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="4c4d1-106">Esimerkiksi huoltotyöntekijä, joka suorittaa työn valmiiksi odotettua nopeammin tuotantolaitoksessa, voi ehkä siirtyä toiseen läheiseen työhön, joka suunniteltiin nykyiselle viikolle, mutta ei välttämättä nykyiselle päivälle.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="4c4d1-107">Tämä lähestymistapa mahdollistaa työntekijöiden suunnittelun ja työn valmistumisen optimoinnin.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="4c4d1-108">Työtilauksiin liittyvät ajoitetut suoritusmääritykset voivat olla yleisiä tai erityisiä.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="4c4d1-109">Voit määrittää yleisiä rivejä, jotka eivät rajoitu tiettyihin työtilaustyyppeihin, resursityyppeihin ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="4c4d1-110">Vaihtoehtoisesti voit luoda ajoitettuja suoritusrivejä, jotka koskevat tiettyä työtilaustyyppiä, käyttöomaisuuden tyyppiä, kunnossapitotöiden tyyppiä jne.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="4c4d1-111">Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Ajoitettu suoritus**.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="4c4d1-112">Luo ajoitettu suoritusrivi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="4c4d1-113">Valitse haluamasi arvot kentissä **Toiminnallinen sijainti**, **Työtilaustyyppi**, **Resurssin tyyppi**, **Valmistaja**, **Malli**, **Ylläpitotyön tyypin luokka**, **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Toimiala**.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="4c4d1-114">Valitse **Palvelutaso**-kentässä työtilauksen palvelutaso.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="4c4d1-115">Jos jätät tämän kentän tyhjäksi, voit määrittää yleisen ajoitetun suorituksen rivityypin.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="4c4d1-116">Esimerkiksi yleisestä rivistä, on seuraavan kuvan ensimmäisessä tietueessa.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="4c4d1-117">Tämä rivi mahdollistaa sen, että kaikki työtilaukset, joilla ei ole työtilauksen palvelutasoa, ajoitetaan tietylle päivämäärälle ja kellonaikaan.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="4c4d1-118">Valitse **Ajoitettu suoritus** -kentässä aikaväli.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="4c4d1-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4c4d1-119">Select **Save**.</span></span>

![Ajoitettu suoritus](media/20-setup-for-work-orders.png)
