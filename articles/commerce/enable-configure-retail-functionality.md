---
title: Alusta Retail-ympäristöissä alkutiedot
description: Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercein alustusprosessia.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022431"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Alkutietojen alustaminen uusissa Retail-ympäristöissä

[!include [banner](includes/banner.md)]

Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercein alustusprosessia.

Kun Commerce-ratkaisu on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta, sinun on alustettava Commerce-määritys luodaksesi peruskonfiguraation tiedot.

> [!IMPORTANT]
> Ennen kuin alustat kauppamäärityksen, varmista, että olet määrittänyt kielen ja postiosoitteen kullekin yritykselle, jolle määrität myymälöitä. Tämä vaihe on suoritettava kullekin yritykselle, jota käytät kauppaan.

Alusta määritys noudattamalla seuraavia vaiheita:

1. Käynnistä Commerce-asiakasohjelma.
2. Valitse **Retail ja Commerce** &gt; **Pääkonttorin asetukset** &gt; **Parametrit** &gt; **Commerce-parametrit**.
3. Napsauta **Alusta**.

Alustaminen luo seuraavat oletusmääritystiedot:

- Commerce-ajastuksen työt ja alityöt
- Kaupankäyntikanavan skeema
- Commercen jakeluaikataulut
- Oletusmuotoiset näyttöasettelut, mukaan lukien painikeruudukot, kuvat ja teemat
- Aikavyöhyketiedot
- Myyntipisteen (POS) toiminnot:
- Myyntipisteen käyttöoikeudet
- Kanavaraportit
- Määritteen metatiedot
- Yksikön tarkistusmallit
- Erätyö Commerce Data Exchange -palvelun historiatietojen tyhjentämiseen

Lisäksi maksukorttiyrityksiin (PCI) liittyvät lokiinkirjaukset ovat käytössä Commercen tietokannassa.

> [!NOTE]
> Commerce-ajastus voidaan määrittää erikseen. Tämä vaihtoehto mahdollistaa Commerce-ajastuksen määrityksen sen oletusasetuksille.

Kun alustus on valmis, sinun määritettävä kaupan lisätiedot. Seuraavassa on muutamia esimerkkejä:

- Kaupankäynnin parametrit
- Kaupankäynnin ajoitustyökalun parametrit
- Commerce-kanavat
- Kassakoneet ja laitteet
- Valikoimat
