---
title: "Alusta Retail-ympäristössä alkutiedot"
description: "Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Microsoft Dynamics 365 for Retailin alustusprosessia."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 0ee002d733882734c9f5a21e0467cacd1b3ff318
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017



---

# Alusta Retail-ympäristössä alkutiedot
<a id="initialize-seed-data-in-a-new-retail-environment" class="xliff"></a>

[!include[banner](includes/banner.md)]


Tässä artikkeli kerrotaan tiedoista, jotka on luotu osana Microsoft Dynamics 365 for Retailin alustusprosessia.

Kun Retail-sovellus on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta, sinun on alustettava vähittäismyyntikonfiguraatio luodaksesi peruskonfiguraation tiedot. **Tärkeää:** Ennen kuin alustat vähittäismyyntikonfiguraation, varmista, että olet määrittänyt kielen ja postiosoitteen kullekin yritykselle, jolle määrität vähittäismyyntiliikkeitä. Tämä vaihe on suoritettava kullekin yritykselle, jota käytät vähittäismyyntiin. Alusta vähittäismyyntikonfiguraatio noudattamalla seuraavia vaiheita:

1.  Käynnistä Dynamics 365 for Retail -asiakasohjelma
2.  Valitse **Vähittäismyynti** &gt; **Pääkonttorin asetukset** &gt; **Parametrit** &gt; **Vähittäismyyntiparametrit**.
3.  Napsauta **Alusta**.

Alustaminen luo seuraavat oletusmääritystiedot:

-   Retail-ajastuksen työt ja alityöt
-   Vähittäismyyntikanavan skeema
-   Vähittäismyyntijakelun aikataulut
-   Oletusmuotoiset näyttöasettelut, mukaan lukien painikeruudukot, kuvat ja teemat
-   Aikavyöhyketiedot
-   Myyntipisteen (POS) toiminnot:
-   Myyntipisteen käyttöoikeudet
-   Kanavaraportit
-   Määritteen metatiedot
-   Yksikön tarkistusmallit
-   Komentojonotyö Commerce Data Exchange -palvelun historiatietojen tyhjentämiseen

Lisäksi maksukorttiyrityksiin (PCI) liittyvät lokiinkirjaukset ovat käytössä Dynamics 365 for Retailin tietokannassa. **Huomautus:** Retail-ajastus voidaan määrittää erikseen. Tämä vaihtoehto mahdollistaa Retail-ajastuksen määrityksen sen oletusasetuksille. Kun alustus on valmis, sinun määritettävä vähittäismyynnin lisätiedot. Seuraavassa on muutamia esimerkkejä:

-   Vähittäismyynnin parametrit
-   Retail-ajastuksen parametrit
-   Vähittäismyyntikanavat
-   Kassakoneet ja laitteet
-   Valikoimat





