---
title: "Alusta Retail-ympäristössä alkutiedot"
description: "Tässä artikkeli kuvaa tietoja, jotka on luotu osana Microsoft Dynamics 365 for Operations - Retail -sovelluksen alustusprosessia."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Alusta Retail-ympäristössä alkutiedot

[!include[banner](includes/banner.md)]


Tässä artikkeli kuvaa tietoja, jotka on luotu osana Microsoft Dynamics 365 for Operations - Retail -sovelluksen alustusprosessia.

Kun Retail-sovellus on otettu käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) kautta, sinun on alustettava vähittäismyyntikonfiguraatio luodaksesi peruskonfiguraation tiedot. **Tärkeää:** Ennen kuin alustat vähittäismyyntikonfiguraation, varmista, että olet määrittänyt kielen ja postiosoitteen kullekin yritykselle, jolle määrität vähittäismyyntiliikkeitä. Tämä vaihe on suoritettava kullekin yritykselle, jota käytät vähittäismyyntiin. Alusta vähittäismyyntikonfiguraatio noudattamalla seuraavia vaiheita:

1.  Käynnistä Dynamics 365 for Operations -asiakasohjelma
2.  Valitse **Vähittäismyynti ja kauppa** &gt; **Pääkonttorin asetukset** &gt; **Parametrit** &gt; **Vähittäismyyntiparametrit**.
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

Lisäksi maksukorttiyrityksiin (PCI) liittyvät lokiinkirjaukset ovat käytössä Dynamics 365 for Operationsin tietokannassa. **Huomautus:** Retail-ajastus voidaan määrittää erikseen. Tämä vaihtoehto mahdollistaa Retail-ajastuksen määrityksen sen oletusasetuksille. Kun alustus on valmis, sinun määritettävä vähittäismyynnin lisätiedot. Seuraavassa on muutamia esimerkkejä:

-   Vähittäismyynnin parametrit
-   Retail-ajastuksen parametrit
-   Vähittäismyyntikanavat
-   Kassakoneet ja laitteet
-   Valikoimat





