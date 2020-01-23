---
title: Logon lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914616"
---
# <a name="add-a-logo"></a>Logon lisääminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten logo lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Kun rakennat sivustoasi, yksi ensimmäisistä asioista, jonka luultavasti teet, on lisätä yrityksesi tai brändin logo sivuston otsikkoon. Dynamics 365 Commerce -online-aloituspakkaus tarjoaa moduulin, joka tekee tästä tehtävästä helppoa.

Voit lisätä logon suoraan malliin, asetteluun tai sivulle. Tällä tavoin voit helposti muuttaa tietyillä sivuilla tai sivuryhmillä näkyvää logoa. Tämä ohjeaihe kattaa kuitenkin yleisimmät skenaariot, joissa lisäät logon otsikon osioihin, joita voidaan käyttää uudelleen kaikilla sivustosi sivuilla.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit lisätä logon sivustosi kaikille sivuille, sinun on suoritettava nämä tehtävät.

1. Lataa logosi digitaaliseen resurssinhallintaan, jota voit käyttää **Resurssit**-sivulla.
1. Luo otsikko-osa. Lisätietoja osien luomisesta ja käyttämisestä on kohdassa [osien käyttäminen](work-with-fragments.md).
1. Sisällytä otsikon osa malliin, jota sivustosi sivut käyttävät asettelu- ja moduulivaihtoehtoihin. Lisätietoja malleista on osiossa [Mallien avulla työskentely](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Logon lisääminen otsikko-osaan

Jos haluat lisätä logon sivustosi otsikko-osaan, toimi seuraavasti.

1. Valitse vasemmalla olevasta siirtymisruudusta **osat** ja valitse sitten luomasi ylätunnisteen osa.
2. Valitse **Kirjaa ulos**.
3. Laajenna **Otsikkopaikka** ja **Logopaikka**.
4. Valitse kolmen pisteen painike (**...**) **Logopaikalle** ja valitse sitten **Lisää moduuli**.
5. Valitse logomoduuli.
6. Määritä oikeanpuoleisessa ominaisuusruudussa logomoduuli, niin, että logosi näkyy siinä.
7. Tallenna ylätunnisteosa, kirjaa se sisään ja julkaise se.

Kun olet julkaissut päivitetyn otsikon osan, kaikki ylätunnisteosan sisältävää mallia käyttävät sivuston sivut näyttävät logon.

## <a name="additional-resources"></a>Lisäresurssit

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Tervetuloviestin lisääminen](add-welcome-message.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)
