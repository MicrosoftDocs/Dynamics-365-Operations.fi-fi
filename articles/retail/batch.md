---
title: Eräseurannassa olevien nimikkeiden parannettu käsitteleminen
description: Tässä aiheessa kuvataan parannuksia, jotka on tehty eräseurannassa olevien nimikkeiden vähittäismyynnin laskelman kirjausprosessin aikana tehtävää erien käsittelyä varten.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5bbddf649f66ded9588cdb1e3f43c75630dc248a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770160"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Eräseurannassa olevien nimikkeiden parannettu käsitteleminen


[!include [banner](includes/banner.md)]


Retail Point of Sale (POS) -sovelluksen myyntipisteen eränumeroita ei voi tallentaa eräseurannassa oleville nimikkeille myynnin aikana. Kun myynti kirjataan pääkonttorissa asiakastilausten tai laskelman kirjauksen avulla, Microsoft Dynamics -järjestelmä kuitenkin odottaa, että tietyissä määrityksissä on sallitut eränumerot eräseurannassa oleville nimikkeille ja että niitä käytetään laskutusprosessin aikana.

Jos tuotteilla on sallitut eränumerot, laskelman kirjauksen asiakastilauksen ja myyntitilauksen laskutusprosessi käyttää niitä. Muussa tapauksessa asiakastilauksen laskutusprosessi ei voi tehdä kirjausta, ja myyntipisteen käyttäjälle lähetetään virhesanoma. Tällöin laskelman kirjaus siirtyy virhetilaan. Tämä virhetila ilmenee, vaikka tuotteille olisi otettu käyttöön negatiivinen varasto.

Retail-sovelluksen versioon 10.0.4 ja uudempiin versioihin tehdyt parannukset varmistavat sen, että negatiivisen varaston ollessa käytössä eräseurannassa oleville nimikkeille, asiakastilausten ja myyntitilausten laskutusta laskelman kirjauksen kautta ei estetä nimikkeille, jos varasto on 0 (nolla) tai eränumeroa ei ole saatavilla. Uusi toiminto käyttää myyntiriveissä oletuserätunnusta, kun eränumerot eivät ole saatavilla.

Voit määrittää asiakastilauksissa käytettävän oletuserätunnuksen **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Vähittäismyynnin parametrit** -sivun **Oletuserätunnus**-kenttään.

Voit määrittää laskelman kirjauksen myyntitilauksen laskutuksessa käytettävän oletuserätunnuksen **Varaston päivitys** -pikavälilehden **Kirjaus**-välilehden **Vähittäismyynnin parametrit** -sivun **Oletuserätunnus**-kentässä.

> [!NOTE]
> Tämä toiminto on käytettävissä vain, kun edistyksellinen varastotoiminto on käytössä tietyn myymälän varastoa ja nimikkeitä varten. Myöhemmässä versiossa toimintoa tuetaan myös skenaarioissa, joissa edistyksellistä varastonhallintaa ei käytetä.

> [!NOTE]
> Parannetun eräseurannassa olevien nimikkeiden käsittelyn tuki laskelman kirjaamisen aikana muissa kuin edistyksellisen varastonhallinnan skenaarioissa sisältyi Retail-sovelluksen versioon 10.0.5.
