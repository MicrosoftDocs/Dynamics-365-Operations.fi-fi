---
title: Sähköisen kaupankäynnin käyttäjien ja roolien hallinta
description: Tässä ohjeaiheessa kerrotaan, kuinka voit myöntää käyttäjille Microsoft Dynamics 365 Commerce -sivuston muokkausympäristön käyttöoikeudet.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 44b02f262136c0d970ca9eee3e5e63ef6dc8ccb7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794280"
---
# <a name="manage-e-commerce-users-and-roles"></a>Sähköisen kaupankäynnin käyttäjien ja roolien hallinta


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit myöntää käyttäjille Microsoft Dynamics 365 Commerce -sivuston muokkausympäristön käyttöoikeudet.

Sivuston muokkausympäristössä käytetään Microsoft Azure Active Directoryssä (Azure AD) luomiasi käyttöoikeusryhmiä, joiden avulla voit hallita käyttäjien käyttöoikeuksia ja myöntää käyttäjille oikeuden suorittaa tiettyjä tehtäviä. Määritä ensin uusi tai olemassa oleva käyttöoikeusryhmä Azure AD:sta jokaiselle muokkausympäristön roolille. Tämän jälkeen voit myöntää käyttöoikeudet yksittäisille käyttäjille tai peruuttaa ne lisäämällä kyseiset käyttäjät asianmukaiseen käyttöoikeusryhmään tai poistamalla heidät käyttöoikeusryhmästä.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Tietoja muokkausympäristön rooleista

Dynamics 365 for Commercen muokkausympäristö tukee seuraavia rooleja.

| Rooli                 | Kuvaus |
|----------------------|-------------|
| Järjestelmänvalvoja | Käyttäjillä, joilla on tämä rooli, on kaikki oikeudet kaikkiin työkaluihin sekä kaikkiin luokituksiin ja arvosteluihin. He voivat myös luoda sivustoja. |
| Järjestelmänvalvoja   | Käyttäjillä, joilla on tämä rooli, on kaikki tietyn sivuston rakenteen työkalujen ja RnR:n oikeudet. |
| Verkon tuottaja         | Käyttäjät, joilla on tämä rooli, voivat luoda sivuja, osia ja malleja, ladata ja hallita resursseja sekä täydentää tuotteita ja luokkia. |
| Lukija               | Käyttäjät, joilla on tämä rooli, voivat tarkastella sivuja, malleja, resursseja, osia, asetteluja ja asetuksia, mutta he eivät välttämättä voi tehdä muutoksia. |
| RnR-valvoja        | Käyttäjät, joilla on tämä rooli, voivat valvoa tuotearvosteluita. |

## <a name="system-administrator-role"></a>Järjestelmänvalvojan rooli

Kun Dynamics 365 Commerce valmistellaan Microsoft Dynamics Lifecycle Services (LCS) -ympäristössä, sinua pyydetään antamaan käyttöoikeusryhmä **järjestelmänvalvojan** roolille. Tämän jälkeen tätä roolia käytetään automaattisesti kaikissa sivustoissa, jotka luot määritettävässä ympäristössä. Tämän roolin käyttöoikeusryhmän voi päivittää vain LCS:ssä. Se näkyy **Sivuston hallinta** -sivuilla kaikissa sivustoissa vain luku -muodossa. Se on tarkoitettu vain tiedoksi.

## <a name="administrator-role"></a>Valvojan rooli

Kun luotu uuden sivuston Commercessa, sinua pyydetään antamaan käyttöoikeusryhmä **valvojan** roolille. Tämän roolin myöntämien oikeuksien yleiskatsaus on tämän ohjeaiheen aiemmassa taulukossa.

## <a name="add-or-update-security-groups"></a>Käyttöoikeusryhmien lisääminen tai päivittäminen

Kun sivusto on määritetty, vain käyttöoikeusryhmään kuuluvat käyttäjät, jotka on liitetty **järjestelmänvalvojan** ja **valvojan** rooleihin, voivat käyttää sivuston muokkausympäristöä. Jos haluat määrittää käyttäjät **verkon tuottajan**, **RnR-valvojan** ja **lukijan** rooleille, sinun on liitettävä näille rooleille käyttöoikeusryhmät. Voit lisätä käyttöoikeusryhmän rooliin tai päivittää käyttöoikeusryhmän, joka on tällä hetkellä määritetty roolille, seuraavasti.

1. Siirry päivitettävälle sivustolle.
1. Avaa **sivuston hallinnassa** **Suojaus**-sivu.
1. Valitse muokattava rooli.
1. Lisää käyttöoikeusryhmät rooleihin tai poista ne rooleista.

## <a name="additional-resources"></a>Lisäresurssit

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)

[Sivuston hakukoneoptimointia (SEO) koskevia tietoja](search-engine-optimization-considerations.md)

[Sisällön suojauskäytännön (CSP) hallinta](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]