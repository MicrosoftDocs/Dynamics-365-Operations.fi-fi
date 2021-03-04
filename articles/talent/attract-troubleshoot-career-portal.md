---
title: Attract-käyttäjät eivät voi hakea töitä uraportaalista
description: Tässä ohjeaiheessa kerrotaan, miten ratkaistaan ongelma, jossa Attract-käyttäjät eivät voi hakea uraportaalin töitä.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461009"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract-käyttäjät eivät voi hakea töitä uraportaalista

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Varasto-otto

Attract-käyttäjät eivät voi hakea töitä uraportaalista. Kun he yrittävät hakea Dynamics 365 Talent: Attractissa luotua työtä, selain lataa sivua jatkuvasti ilman toiminnon suorittamista.

## <a name="cause"></a>Syy

Tämä ongelma ilmenee, kun Talentin suhderyhmällä ei ole Talentin käyttäjäroolia.

## <a name="resolution"></a>Ratkaisu

Määritä Talentin käyttäjärooli Talentin suhderyhmälle.

1. Kirjaudu sisään [Power Platformin hallintakeskukseen](https://admin.powerplatform.microsoft.com) jollakin seuraavista järjestelmänvalvojan valtuustiedoista:

   - Dynamics 365:n järjestelmänvalvoja
   - Yleinen järjestelmänvalvoja
   - Power Platformin järjestelmänvalvoja

2. Valitse siirtymisruudussa **Ympäristöt** ja valitse sitten ympäristö, jossa Talentin käyttäjäryhmä liitetään Talentin suhderyhmään.

   ![Ympäristön valitseminen](./media/attract-troubleshoot-career-portal-select-environment.png)

3. Valitse **Ympäristöt**-ruudussa **Ympäristön URL-osoite** ja kirjaudu sisään ympäristön hallintaportaaliin (esimerkiksi https:<orgname>.crm.dynamics.com).

4. Valitse **Asetukset**. Valitse **Järjestelmä** ja valitse sitten **Suojaus**.

   ![Siirtyminen kohtaan Suojaus](./media/attract-troubleshoot-career-portal-security.png)

5. Valitse **Ryhmät**.

   ![Ryhmien valitseminen](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Hae **Talentin suhderyhmää** hakuruudun avulla ja valitse ryhmä hakutuloksista.

7. Valitse **HALLINNOI ROOLEJA** valintanauhasta.

8. Valitse **Hallinnoi ryhmän rooleja** -valintaikkunassa **Talentin käyttäjä** käytettävissä olevista rooleista ja kohdista sitten rooli valitsemalla **OK**.

   ![Roolin kohdistaminen](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Testaa muutokset seuraavasti:

   1. Kirjaudu uraportaaliin uudesta selainikkunasta.
   2. Hae työtä uraportaalista. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]