---
title: Ota käyttöön yleisen ennakonpidätyksen valuutan vaihtokurssin tyypin ja päivämäärätyypin asetukset
description: Tässä artikkelissa kerrotaan, miten ennakonpidätyksen valuutan vaihtokurssin tyypin ja päivämäärätyypin yleiset asetukset otetaan käyttöön.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573221"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Ota käyttöön yleisen ennakonpidätyksen valuutan vaihtokurssin tyypin ja päivämäärätyypin asetukset

[!include[banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten ennakonpidätyksen valuutan vaihtokurssin tyypin ja päivämäärätyypin yleiset asetukset otetaan käyttöön. Voit nyt valita ennakonpidätyksen valuutalle käyttöönotettavan vaihtokurssityypin ja vaihtokurssin laskentapäivätyypin. Nämä valinnat määrittävät ennakonpidätyksen summan laskennassa käytettävän ulkomaan valuutan vaihtokurssin ennakonpidätyksen valuuttana maksutapahtumissa.

Tämä toiminto on käytettävissä Microsoft Dynamics 365 Finance -versiossa 10.0.29 ja uudemmissa.

1. Valitse **Vero** \> **Asetukset** \> **Parametrit** \> **Kirjanpitoparametrit**.
2. Määritä **Ennakonpidätys**-välilehdessä **Ota ennakonpidätyksen ennakon valuutta käyttöön** -asetukseksi **Kyllä**.
3. Valitse **Vaihtokurssi**-kentässä ennakonpidätyksen valuutan vaihtokurssityyppi.
4. Valitse **Laskentapäivätyyppi**-kentässä laskentapäivän tyyppi, joka määrittää ennakonpidätyksen valuutan vaihtokurssin:

    - **Maksupäivä** – Määritä vaihtokurssi maksukirjauskansion kirjauspäivämäärän perusteella.
    - **Laskupäivä** – Määritä vaihtokurssi laskukirjauskansion laskupäivämäärän perusteella. Jos tositteen laskun päivämäärä on tyhjä, käytetään laskun kirjauspäivämäärää. 
    - **Asiakirjan päivämäärä** – Määritä vaihtokurssi maksukirjauskansion asiakirjan päivämäärän perusteella. Jos tositteen asiakirjan päivämäärä on tyhjä, käytetään maksupäivämäärää.

5. Valitse **Tallenna**.

Jos tapahtuman valuutta eroaa ennakonpidätyskoodissa määritetystä ennakonpidätyksen valuutasta, ennakonpidätyksen valuuttana oleva summa lasketaan tapahtuman valuutasta edellisten asetusten mukaan ja kirjataan kirjattuihin ennakonpidätystapahtumiin.
