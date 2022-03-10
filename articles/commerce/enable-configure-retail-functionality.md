---
title: Alkutietojen alustaminen uusissa Commerce-ympäristöissä
description: Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercen alustusprosessia.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 14d56636b48d8f8ff15863bb04c762e398f8c370664fbd52f80ed5f05f0e4895
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718728"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Alkutietojen alustaminen uusissa Commerce-ympäristöissä

[!include [banner](includes/banner.md)]

Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Commercen alustusprosessia.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]