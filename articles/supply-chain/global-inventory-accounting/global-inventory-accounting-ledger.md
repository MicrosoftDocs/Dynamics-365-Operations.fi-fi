---
title: Yleisen varastokirjanpidon tapahtumarekisteri
description: Tässä aiheessa kuvataan yleisiä varastokirjanpidon pääkirjoja, jotka on määritetty valuutan, kalenterin, kirjanpidon ja yrityksen liitoksen avulla.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273148"
---
# <a name="global-inventory-accounting-ledger"></a>Yleisen varastokirjanpidon tapahtumarekisteri

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Yleisessä varastokirjanpidossa on omat pääkirjansa. Aina kun asiaankuuluvan yrityksen varastoon liittyvä tapahtuma käsitellään, järjestelmä voi tarvittaessa ottaa tapahtuman huomioon missä tahansa määrässä yleisiä varastokirjanpitoja.

Kirjanpito on debet- ja kredit-mittarien luettelo. Nämä toimenpiteet luokitellaan kustannuselementtien ja alareskontran tilien avulla. Yleisiä varastokirjanpidon pääkirja määritetään valuutan, kalenterin, kirjanpidon ja yrityksen liitoksen avulla.

Voit määrittää yleiset varastokirjanpitotilit pääkirjoissa seuraavasti **Yleinen varastokirjanpito \> Asennus \> Yleinen varastokirjanpidon pääkirjat**. Määritä kullekin kirjanpidolle seuraavat kentät:

- **Nimi** – Anna kirjanpidon nimi.
- **Kuvaus** – anna kirjanpitojen kuvaus.
- **Tilikausikalenteri** – Määritä kirjanpidon tilikausikalenteri.
- **Valuutan ja vaihtokurssin tyyppi** – Tämän pikavälilehden kenttien avulla voit valita kirjanpidon valuutan sekä vaihtokurssityypin. Valittava valuutta voi olla eri kuin valuutta, jota yritys käyttää. Yleisessä varastokirjanpidossa käyttäjät voivat määrittää niin monta kustannuslaskentakirjanpitoa kuin ne edellyttävät. Yleinen varastokirjanpito tukee varastolaskentaa useina valuuttoina ja useina arvostuksena. Määritä seuraavat kentät:

    - **Valuutta** – Valitse kustannuslaskentavaluutta, jota varastoon liittyviä arvoja ylläpidetään. Arvoja ovat varastoarvo, myytyjen tuotteiden kustannukset, kuljetettava varasto ja kaikenlaiset poikkeamat.
    - **Vaihtokurssityyppi** – Valitse valuuttakurssi, jota järjestelmän tulisi käyttää tapahtuman määrän muuntamiseen tapahtumavaluutassa ja tuotteiden vakiokustannukset laskentavaluutaksi.

- **Käytännön nimi** – Määritä käytäntö. Kokous on kokoelma käytäntöjä, jotka määrittävät, miten kustannukset otetaan huomioon tässä kirjanpidossa.
- **Yritys** – Kirjanpito ottaa huomioon valitulle yritykselle kirjatut asiakirjat.
- **Pohjustus** – Valitse, käsitelläänkö ennen kirjanpidon luomista luodut varastotapahtumat kirjanpidon valuutan ja tapahtuman mukaan. Valitse jokin seuraavista:

    - **Käytössä** – Kirjanpidon tulisi käsitellä tapahtumat, jotka on luotu ennen kirjanpidon luomista.
    - **Poissa käytöstä** – Kirjanpidon tulisi käsitellä vain tapahtumat, jotka on luotu kirjanpidon luomisen jälkeen.

    > [!IMPORTANT]
    > **Et** voi palata käyttämään tätä kenttää uusien tiedostojen lisäämisen jälkeen.

- **Tila** – Järjestelmä määrittää vasta luotujen kirjanpitojen tilaksi automaattisesti *Valmis*.
