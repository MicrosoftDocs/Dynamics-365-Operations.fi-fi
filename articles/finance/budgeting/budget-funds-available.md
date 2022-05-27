---
title: Käytettävissä olevat budjettivarat
description: Tässä aiheessa esitellään saatavilla olevat budjettivarat -toiminto ja tietoja, joiden avulla voit määrittää budjetin hallinnan organisaation taloudellisten resurssien hallinnan optimoimiseksi.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 1e7b2bf7ef7bd1bca6db27371f87dfddcdceef89
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710246"
---
# <a name="budget-funds-available"></a>Käytettävissä olevat budjettivarat

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä aiheessa esitellään saatavilla olevat budjettivarat -toiminto ja tietoja, joiden avulla voit määrittää budjetin hallinnan organisaation taloudellisten resurssien hallinnan optimoimiseksi.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Käytettävissä olevien budjettivarojen parannettu laskentatoiminto

**Seuraa vain käytettävissä olevien budjettivarojen laskentaa** -ominaisuuden avulla voit seurata taustalla olevia budjetin ohjaustaulukoita asiakirjatyypeille ja -tiloille **Määritä budjetin hallinnan parametrit** -sivun asetusten perusteella.

Joillakin budjetin hallinnan konfigurointivaihtoehdoilla on oltava tietyt asetukset, jotta toiminto toimisi oikein. Nämä vaihtoehdot valitaan tai tyhjennetään **Saatavilla olevat budjetin varat** -välilehden **Määritä budjetin hallintaparametrit** -sivulla. Seuraavassa taulukossa näkyvät käytettävissä olevien budjettivarojen ominaisuuden edellyttämät asetukset.

| Jos tämä vaihtoehto valitaan | Tämä vaihtoehto on myös valittava |
| ------------------------- | -------------------------------- |
| Alustavien varausten budjettivaraukset | Varausten *ja* toteutuneiden kulujen budjettivaraukset |
| Varausten budjettivaraukset | Toteutuneet kulut |
| Varausten budjettivaraukset, joissa on ostoehdotustyyppisiä asiakirjoja | Alustavien varausten budjettivaraukset |

Tämä toiminto vaikuttaa vain uusiin tiedostoihin. Aiemmin luotujen tiedostojen summia seurataan ja näytetään budjetin hallinnan tilastokyselyssä, kunnes budjettisummia muutetaan ja uusi budjetin hallinnan konfiguraatio aktivoidaan. Budjettien seurantatiedot poistetaan tässä vaiheessa asiakirjoissa, jotka on poistettu käytettävissä olevien budjettivarojen laskelmasta.

On suositeltavaa jättää **kirjaamattomat todelliset kulut** -valinta tyhjäksi. Jos se on valittuna, kirjaamattomista asiakirjoista, kuten odottavista toimittajan laskuista, tehdään aikaa vievä budjetin hallinnan laskenta.
