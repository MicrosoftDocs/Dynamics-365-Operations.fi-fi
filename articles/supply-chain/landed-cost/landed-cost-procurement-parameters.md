---
title: Aiheutuneen kustannuksen Hankkiminen ja hankinta -parametrit
description: Tässä artikkelissa kuvataan, miten määritetään tarvittavat Hankkiminen- ja hankintaparametrit, kun käytät Aiheutunut kustannus -moduulia.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905976"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Aiheutuneen kustannuksen Hankkiminen ja hankinta -parametrit

[!include [banner](../../includes/banner.md)]

**Hankkiminen ja hankinta -parametrien** sivulla on muutamia asetuksia, jotka ovat erityisen tärkeitä käytettäessä **Aiheutunut kustannus** -moduulia. **Hankkiminen ja hankinta -parametrit** -sivulla avatun **Päivitä tilausrivit** -valintaikkunan avulla voit määrittää, päivitetäänkö ostotilausrivit automaattisesti, kun ostotilauksen otsikkoon tehdään muutoksia.

Viimeiste määritys noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Hankkiminen ja hankinta \> Asetukset \> Hankkiminen ja hankinta -parametrit**.
1. Valitse **Yleiset**-välilehdestä **Päivitä tilausrivit** -linkki.
1. **Päivitä tilausrivit** -valintaikkunassa näkyvät tilausotsikon kentät, jotka voivat myös päivittää tilausrivien kenttiä automaattisesti. Määritä luettelon kullekin kentälle jokin seuraavista arvoista:

    - **Aina** – Tilausrivien pitäisi päivittyä automaattisesti, kun tilauksen otsikkotiedot päivitetään.
    - **Ei koskaan** – Tilausrivien ei pitäisi päivittyä koskaan, kun tilauksen otsikkotiedot päivitetään.
    - **Kehote** – Käyttäjää pyydetään valitsemaan, päivitetäänkö tilausrivit.
