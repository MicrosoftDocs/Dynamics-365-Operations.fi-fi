---
title: Matkan tilan määritys
description: Tässä aiheessa kuvataan, miten määritetään tila-arvot, joita käyttäjät voivat määrittää matkoille.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500883"
---
# <a name="voyage-status-setup"></a>Matkan tilan määritys

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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
