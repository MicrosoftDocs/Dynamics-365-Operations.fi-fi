---
title: Aiheutuneen kustannuksen Hankkiminen ja hankinta -parametrit
description: Tässä aiheessa kuvataan, miten määritetään tarvittavat Hankkiminen- ja hankintaparametrit, kun käytät Aiheutunut kustannus -moduulia.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833926"
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
