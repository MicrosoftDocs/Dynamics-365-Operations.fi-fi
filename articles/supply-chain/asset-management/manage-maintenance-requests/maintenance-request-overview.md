---
title: Ylläpitopyynnöt
description: Tässä aiheessa on yleiskatsaus ylläpitopyyntöjen hallintaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e0071ae745987a1217525b2841e3320933a9242
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019626"
---
# <a name="maintenance-requests"></a>Ylläpitopyynnöt

[!include [banner](../../includes/banner.md)]

 

Ylläpitopyynnöt ovat muistiinpanoja tai ilmoituksia, jotka on luotu ilmoittamaan esimiehlle tai suunnittelijalle, että resurssi voi edellyttää huolto- tai korjaustyötä, mutta luomatta työtilausta. Jos ylläpitopyynnön sisältö katsotaan kelvolliseksi, työtilaus voidaan luoda ylläpitopyynnön perusteella.

Ylläpitopyyntöjä voi luoda mille tahansa resurssille resurssien hallinnassa. Erilaisia ylläpitopyyntöjä voidaan luoda sen mukaan, miten yrityksesi käyttää ylläpitopyyntöjä. Seuraavassa on muutamia esimerkkejä:

- Ylläpitopyynnöt
- Muistiinpanot
- Korjaukset tai parannukset
- Investoinnit
- Varastokorjaus (tätä tyyppiä käytetään, kun vastaanotat resursseja toisesta sijainnista, jotta voit tehdä huolto- tai korjaus työn, ja palautat sitten resurssin sen jälkeen, kun työ on suoritettu loppuun.)

## <a name="view-maintenance-requests"></a>Näytä ylläpitopyynnöt

Näet ylläpitopyynnöt valitsemalla **resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt**, **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**. Kullakin luettelosivulla näkyy joitakin ylläpitopyyntöön liittyviä tietoja.

![Ylläpitopyyntöjen katselu](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Käytä **Omat toiminnallisen sijainnin ylläpitopyynnöt** -luettelosivua, kun haluat tarkastella luetteloa ylläpitopyynnöistä, jotka sisältävät joko toiminnallisia sijainteja, joihin olet yhteydessä työntekijänä tai resursseja, jotka on asennettu toiminnallisiin sijainteihin, joihin olet liittynyt työntekijänä. (Lisätietoja toiminnalisten sijainiten määrittämisestä kunnossapitotyöntekijöille on kohdassa [huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Vaikka asiakastilin tiedot ovat käytettävissä resurssien palvelujen hallinnassa (ulkoinen kunnossapito), se ei ole käytettävissä resurssien hallinnassa (sisäinen kunnossapito).

Voit avata tietueen tietonäkymän valitsemalla **Kaikki ylläpitopyynnöt** -luettelosivun ruudukkonäkymässä **Ylläpitopyyntö**-sarakkeesta linkin.

![Ylläpitopyynnön tietojen avaaminen](media/02-manage-maintenance-requests.png)

Toimintoruudun painikkeet on järjestetty välilehtiin. Seuraavassa taulukossa kuvataan lyhyesti resurssien hallintaan liittyvät painikkeet.

| Painikkeen nimi                      | Kuvaus |
|----------------------------------|-------------|
| Muokkaa                             | Muokkaa valittua ylläpitopyyntöä. |
| Uusi                              | luo uusi ylläpitopyyntö. |
| Poista                           | Poista valittu ylläpitopyyntö. |
| Työtilauspooli                  | Yhdistä valittu huoltopyyntö työtilauspooliin. |
| Työtilaus                       | Luo työtilaus valitun huoltopyynnön perusteella. |
| Resurssin vika                      | Valitse **Resurssin viat**, jossa voit luoda vikarekisteröinnin valittuun ylläpitopyyntöön. |
| Työtilaukset                      | Näytä luettelo kaikista työtilauksista, jotka on yhdistetty valittuun ylläpitopyyntöön. |
| Päivitä ylläpitopyynnön tila. | Päivitä ylläpitopyynnön tila. |
| Elinkaaren tilan loki              | Tarkastele lokia, joka näyttää valitun ylläpitopyynnön elinkaaritilat. |
| Ylläpitopyynnön tiedot      | Tulosta raportti, joka sisältää valitun ylläpitopyynnön tiedot. |
| Lähetä lainattu resurssi                  | Valitse lainaresurssi, jonka pitäisi olla väliaikainen korvaava resurssi, joka on valittu valitulle ylläpitopyynnölle. |
| Palauta lainaresurssi                | Rekisteröi lainaresurssi palautetuksi. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]