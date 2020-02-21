---
title: Vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen sääntöjen käytöstäpoisto
description: Tässä aiheessa kuvataan vähittäismyyntitapahtumien yhdenmukaisuuden tarkistussääntöjen käytöstäpoistotoiminto Microsoft Dynamics 365 Commerce -sovelluksessa.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: b11b901fafc3907e9d3cae5cd554cc9a868a414c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004340"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="3d8f4-103">Vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen sääntöjen käytöstäpoisto</span><span class="sxs-lookup"><span data-stu-id="3d8f4-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="3d8f4-104">Jälleenmyyjillä voi olla yksilöllisiä liiketoimintaskenaarioita ja -prosesseja.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="3d8f4-105">Tämän vuoksi kaikki kauppatapahtumien yhdenmukaisuuden tarkistukseen oletusarvoisesti sisältyvät säännöt eivät ole kaikkien jälleenmyyjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="3d8f4-106">Microsoft Dynamics 365 Commerce sisältää myös toiminnon, jonka avulla voi poistaa käytöstä säännöt, jotka eivät ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="3d8f4-107">Saat näkyviin ympäristösi vähittäismyyntitapahtuman yhdenmukaisuuden tarkistuksen käytettävissä olevien sääntöjen luettelon ja kunkin säännön tilan siirtymällä kohtaan **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan parametrit \> Vähittäismyynnin parametrit** ja valitsemalla **Tapahtuman tarkistus** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="3d8f4-108">Kunkin säännön tilaksi on oletusarvoisesti määritetty **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="3d8f4-109">Tämän vuoksi kaikkia sääntöjä käytetään tarkistettaessa vähittäismyyntitapahtumat ennen niiden noutamista kauppalaskelmiin.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="3d8f4-110">Jos haluat poistaa säännön käytöstä, muuta sen tilaksi **Ei käytössä**.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="3d8f4-111">Käytöstä poistettuja sääntöjä ei käytetä kauppatapahtumien tarkistuksessa laskelman laskentaprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="3d8f4-112">Jos haluat ohittaa koko tarkistusprosessin käytössä olevista säännöistä huolimatta, siirry kohtaan **Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Kaupan parametrit**. Määritä sitten **Tapahtuman tarkistus** -välilehdessä **Poista kauppatapahtumien yhdenmukaisuuden tarkistus käytöstä** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="3d8f4-113">Kun tämän asetuksen arvoksi on määritetty **Ei**, arvoksi ei voi enää määrittää **Kyllä** käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="3d8f4-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
