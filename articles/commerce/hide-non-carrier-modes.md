---
title: Muiden kuin rahdinkuljettajien toimitustapojen piilotus POS:n lähetysvalinnoissa
description: Tässä aiheessa kuvataan määritysvaihtoehto, jolla estetään muiden kuin rahdinkuljettajien toimitustapojen valittavuus, kun lähetystilauksia luodaan myyntipistesovelluksessa (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 38d57ed5f8d2b8725cd11156f0135988bb76e047
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412058"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="d0709-103">Muiden kuin rahdinkuljettajien toimitustapojen piilotus POS:n lähetysvalinnoissa</span><span class="sxs-lookup"><span data-stu-id="d0709-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d0709-104">Tässä aiheessa kuvataan määritysvalinta, joka on käytettävissä myyntipistesovelluksessa (POS).</span><span class="sxs-lookup"><span data-stu-id="d0709-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="d0709-105">Tämä määritysvalinta muuttaa toimintatapaa lähetystavan valinnassa, kun tilauksia luodaan POS:ssä.</span><span class="sxs-lookup"><span data-stu-id="d0709-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="d0709-106">Kun käyttäjät luovat mukautettuja lähetystilauksia POS:ssä, he voivat valita lähetykselle toimitustavan.</span><span class="sxs-lookup"><span data-stu-id="d0709-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="d0709-107">Tämä toiminto on käytettävissä riippumatta siitä, lähetetäänkö koko tilaus vai vain valittuja rivejä.</span><span class="sxs-lookup"><span data-stu-id="d0709-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="d0709-108">Oletusarvoisesti toimitustavan valintaikkunassa näkyvät kaikki kanavan, nimikkeen ja toimitusosoitteen yhdistelmälle soveltuvat toimitustavat.</span><span class="sxs-lookup"><span data-stu-id="d0709-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="d0709-109">Nämä toimitustavat määritetään **Toimitustavat**-sivulla Headquartersissa (**Myynti ja markkinointi \> Asetukset \> Jakelu \> Toimitustavat**).</span><span class="sxs-lookup"><span data-stu-id="d0709-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="d0709-110">Valintaikkunassa voi näkyä myös muita kuin rahdinkuljettajan toimitustapoja, kuten **Nouto liikkeestä** tai **Nouto**.</span><span class="sxs-lookup"><span data-stu-id="d0709-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="d0709-111">Nyt on kuitenkin lisätty toiminto, jolla voit piilottaa valintaikkunassa muut kuin rahdinkuljettajan toimitustavat.</span><span class="sxs-lookup"><span data-stu-id="d0709-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="d0709-112">Voit ottaa tämän toiminnon käyttöön asettamalla **Asiakastilaukset**-välilehden **Commercen parametrit** -sivun asetuksen **Näytä lähetystilauksissa vain rahdinkuljettajien toimitustavat** arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d0709-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="d0709-113">Kun olet ottanut tämän toiminnon käyttöön ja suoritat asianmukaiset jakelutyöt synkronoidaksesi tiedot kanavatietokantaan, muita kuin rahdinkuljettajien toimitustapoja ei enää ole valittavissa, kun lähetystilauksia luodaan POS:ssä.</span><span class="sxs-lookup"><span data-stu-id="d0709-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
