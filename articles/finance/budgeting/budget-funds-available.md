---
title: Käytettävissä olevat budjettivarat
description: Tässä aiheessa esitellään saatavilla olevat budjettivarat -toiminto ja tietoja, joiden avulla voit määrittää budjetin hallinnan organisaation taloudellisten resurssien hallinnan optimoimiseksi.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891310"
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
