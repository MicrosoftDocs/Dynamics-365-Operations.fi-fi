---
title: Matkan tilan määritys
description: Tässä artikkelissa kuvataan, miten määritetään tila-arvot, joita käyttäjät voivat määrittää matkoille.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1cec728f2fa49175c063818ee7f188b441945647
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907316"
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
