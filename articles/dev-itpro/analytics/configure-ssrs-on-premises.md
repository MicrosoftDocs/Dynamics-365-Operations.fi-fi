---
title: "SQL Server Reporting Servicesin määrittäminen paikallisessa käyttöönotossa"
description: "Tässä ohjeaiheessa on tietoja SQL Server Reporting Servicesin (SSRS) määrittämisestä paikallista käyttöönottoa varten."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a1f11641a2ec055cfaa0157ac9a40525daa4006
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>SQL Server Reporting Servicesin määrittäminen paikallisessa käyttöönotossa

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten SQL Server Reporting Services (SSRS) määritetään Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin paikallista käyttöönottoa varten.

1. Avaa Reporting Services -määritystenhallintasovellus
2. Jätä oletusarvoinen **Palvelimen nimi**, jonka pitäisi olla nykyisen laitteen nimi, ja **Report Server -esiintymä**, **MSSQLSERVER**. 
3. Valitse **Yhdistä**.
   
   [![Reporting Servicesin määritysyhteys](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. Valitse **Palvelutili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![Palvelutili-välilehti](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. Valitse **Internet-palvelun URL**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa. 

    [![Internet-palvelun URL -välilehti](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. Valitse **Tietokanta**-välilehti ja tarkista, että **Tietokannan nimi** ja **Tunnistetietojen asetukset** ovat samat kuin seuraavassa kuvassa. **Huomautus:** Sinun on luotava uusi tietokanta. Tee se valitsemalla **Muuta tietokantaa** ja tarkista sitten, että uuden tietokannan nimi on **DynamicsAxReportServer**.

    [![tietokanta-välilehti](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. Valitse **Internet-portaalin URL** -välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa. **Huomautus:** sinun on valittava **Käytä**, jotta voit luoda ja määrittää portaalin oikein.

    [![Internet-portaalin url -välilehti](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  Kun portaali on määritetty, **Internet-portaali**-välilehden on vastattava seuraavaa kuvaa.
    [![Internet-portaali-välilehti](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. Avaa SQL Server Reporting Services -verkkoportaali napsauttamalla raporttien URL-osoitetta. 
9.  Luo portaalissa uusi **Dynamics**-niminen kansio.

    [![dynamics-kansio](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. Valitse **Reporting Servicesin määritystenhallinnassa** **Sähköpostiasetukset**-välilehti ja varmista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![sähköpostiasetukset-välilehti](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. Valitse **Toimeenpanotili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![toimeenpanotili-välilehti](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  Älä muuta **Salausavaimet**-välilehden oletusasetuksia. [![salausavaimet-välilehti](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. Valitse **Tilausasetukset**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![tilausasetukset-välilehti](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  Älä muuta **Skaalauskäyttöönotto**-välilehden oletusasetuksia. [![skaalauskäyttöönotto-välilehti](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  Älä muuta **Power BI -integrointi** -välilehden oletusasetuksia. [![power bi -integrointi -välilehti](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. Sulje **Reporting Services -määritystenhallintasovellus** valitsemalla **Lopeta**.

    [![reporting Servicesin määritystenhallinnan sulkeminen](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    


