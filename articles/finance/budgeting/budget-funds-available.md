---
title: Käytettävissä olevat budjettivarat
description: Tässä artikkelissa esitellään saatavilla olevat budjettivarat -toiminto ja tietoja, joiden avulla voit määrittää budjetin hallinnan organisaation taloudellisten resurssien hallinnan optimoimiseksi.
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
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898237"
---
# <a name="budget-funds-available"></a>Käytettävissä olevat budjettivarat

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa esitellään saatavilla olevat budjettivarat -toiminto ja tietoja, joiden avulla voit määrittää budjetin hallinnan organisaation taloudellisten resurssien hallinnan optimoimiseksi.

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
