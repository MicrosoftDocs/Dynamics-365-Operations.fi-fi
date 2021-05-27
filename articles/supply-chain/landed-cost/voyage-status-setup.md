---
title: Matkan tilan määritys
description: Tässä aiheessa kuvataan, miten määritetään tila-arvot, joita käyttäjät voivat määrittää matkoille.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022105"
---
# <a name="voyage-status-setup"></a>Matkan tilan määritys

[!include [banner](../../includes/banner.md)]

**Matkan tilat** -sivulla voit määrittää niiden tila-arvojen joukon, jotka käyttäjät voivat määrittää matkoille. Käyttäjät voivat määrittää matkan tila-arvoja kaikille matkan tasoille: matkat, kuljetuskontti, pakkaus, ostotilaus ja nimike (ostorivit ja siirtotilausrivit). Niitä käytetään kahteen tarkoitukseen:

- Matkan, kuljetuskontin, pakkauksen, ostotilauksen tai nimikkeen (ostorivit ja siirtotilausrivit) tilan ilmoittaminen käyttäjälle.
- Voit rajoittaa kustannusalueen käyttöä estämällä muokkauksen tai poiston.

Voit määrittää matkojen tilat valitsemalla **Aiheutunut kustannus \> Määritys \> Matkojen tilat**. Tällöin voit lisätä, poistaa ja muokata tiloja käyttämällä toimintoruudun painikkeita.

Kullakin kustannusalueella on oma matkatilojen joukkonsa ja hierarkiansa. Siksi **Matkojen tilat** -sivun **Kustannusalue**-kentässä on ensin valittava se kustannusalue, jota halutaan tarkastella tai jolle halutaan luoda matkojen tiloja. Määritä sitten kullekin matkan tilalle tarpeen mukaan seuraavassa taulukossa kuvatut kentät. Huomaa, että myös järjestelmätapahtumat voivat muuttaa automaattisesti matkojen tiloja. Tällaisia tapahtumia ovat esimerkiksi säännöt, jotka on luotu jäljityksen hallintakeskuksella.

| Kenttä | kuvaus |
|---|---|
| Matkan tila | Määritä matkan tilan nimi. |
| kuvaus | Anna matkan tilan kuvaus. |
| Muokkaa | Valitse tämä valintaruutu, jos käyttäjät saavat muokata matkoja, joilla on tämä tila. |
| Delete-näppäin | Valitse tämä valintaruutu, jos käyttäjät saavat poistaa matkoja, joilla on tämä tila. |
| Pakollinen | Valitse tämä valintaruutu, jos haluat tehdä matkan tilasta pakollisen siten, että sitä ei voi ohittaa. |
| Ylärakenne | Tämän kentän avulla voit luoda hierarkian tila-arvoille. Matkojen tiloja voidaan siirtää (joko manuaalisesti tai automaattisesti) vain alaspäin hierarkiasta eli päätilasta johonkin sen alitilaan.

> [!NOTE]
> Sinun tarvitsee määrittää vain ne tietyt matkojen tilat, joita organisaatiosi käyttää. Tyypillisiä matkojen tiloja ovat esimerkiksi *Vahvistettu*, *Tuotteet kuljetettavana*, *Vastaanotettu*, *Valmiina kustannuslaskentaan* ja *Kustannukset laskettu*. Muitakin tiloja saattaa kuitenkin olla käytössä.
