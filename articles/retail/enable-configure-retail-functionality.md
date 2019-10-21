---
title: Alusta Retail-ympäristöissä alkutiedot
description: Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Retailin alustusprosessia.
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
ms.openlocfilehash: 49b21d81437ebd7cc55076444ee71ae1143bfac0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025513"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Alkutietojen alustaminen uusissa Retail-ympäristöissä

[!include [banner](includes/banner.md)]

Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Dynamics 365 Retailin alustusprosessia.

Kun Retail-sovellus on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta, sinun on alustettava vähittäismyyntikonfiguraatio luodaksesi peruskonfiguraation tiedot.

> [!IMPORTANT]
> Ennen kuin alustat vähittäismyyntikonfiguraation, varmista, että olet määrittänyt kielen ja postiosoitteen kullekin yritykselle, jolle määrität vähittäismyyntiliikkeitä. Tämä vaihe on suoritettava kullekin yritykselle, jota käytät vähittäismyyntiin.

Alusta vähittäismyyntikonfiguraatio noudattamalla seuraavia vaiheita:

1. Käynnistä Retail-asiakasohjelma.
2. Valitse **Vähittäismyynti** &gt; **Pääkonttorin asetukset** &gt; **Parametrit** &gt; **Vähittäismyyntiparametrit**.
3. Napsauta **Alusta**.

Alustaminen luo seuraavat oletusmääritystiedot:

- Retail-ajastuksen työt ja alityöt
- Vähittäismyyntikanavan skeema
- Vähittäismyyntijakelun aikataulut
- Oletusmuotoiset näyttöasettelut, mukaan lukien painikeruudukot, kuvat ja teemat
- Aikavyöhyketiedot
- Myyntipisteen (POS) toiminnot:
- Myyntipisteen käyttöoikeudet
- Kanavaraportit
- Määritteen metatiedot
- Yksikön tarkistusmallit
- Erätyö Commerce Data Exchange -palvelun historiatietojen tyhjentämiseen

Lisäksi maksukorttiyrityksiin (PCI) liittyvät lokiinkirjaukset ovat käytössä Retailin tietokannassa.

> [!NOTE]
> Retail-ajastus voidaan määrittää erikseen. Tämä vaihtoehto mahdollistaa Retail-ajastuksen määrityksen sen oletusasetuksille.

Kun alustus on valmis, sinun määritettävä vähittäismyynnin lisätiedot. Seuraavassa on muutamia esimerkkejä:

- Vähittäismyynnin parametrit
- Retail-ajastuksen parametrit
- Vähittäismyyntikanavat
- Kassakoneet ja laitteet
- Valikoimat
