---
title: SQL Server Reporting Servicesin määrittäminen paikallisissa käyttöönotoissa
description: Tässä ohjeaiheessa on tietoja SQL Server Reporting Servicesin (SSRS) määrittämisestä paikallista käyttöönottoa varten.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 88e6d5470ff7808a9b6263b6426e19f6ea11493d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755521"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>SQL Server Reporting Servicesin määrittäminen paikallisissa käyttöönotoissa

[!include [banner](../includes/banner.md)]

Määritä Microsoft Dynamics 365 Finance + Operationsin (paikallinen) käyttöönoton SQL Server Reporting Services (SSRS) tämän ohjeaiheen ohjeiden mukaisesti.

1. Avaa Reporting Services -määritystenhallintasovellus
2. Jätä oletusarvoinen **Palvelimen nimi**, jonka pitäisi olla nykyisen laitteen nimi, ja **Report Server -esiintymä**, **MSSQLSERVER**.
3. Valitse **Yhdistä**.

    [![Reporting Servicesin määritysyhteys](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Valitse **Palvelutili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![Palvelutili-välilehti](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Valitse **Internet-palvelun URL**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![Internet-palvelun URL -välilehti](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Valitse **Tietokanta**-välilehti ja tarkista, että **Tietokannan nimi** ja **Tunnistetietojen asetukset** ovat samat kuin seuraavassa kuvassa.

    > [!NOTE]
    > Sinun on luotava uusi tietokanta. Tee se valitsemalla **Muuta tietokantaa** ja tarkista sitten, että uuden tietokannan nimi on **DynamicsAxReportServer**.

    [![tietokanta-välilehti](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Valitse **Internet-portaalin URL** -välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    > [!NOTE]
    > Sinun on valittava **Käytä**, jotta voit luoda ja määrittää portaalin oikein.

    [![Internet-portaalin url -välilehti](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Kun portaali on määritetty, **Internet-portaali**-välilehden on vastattava seuraavaa kuvaa.

    [![Internet-portaali-välilehti](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Avaa SQL Server Reporting Services -verkkoportaali napsauttamalla raporttien URL-osoitetta.
9. Luo portaalissa uusi **Dynamics**-niminen kansio.

    [![dynamics-kansio](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Valitse **Reporting Servicesin määritystenhallinnassa** **Sähköpostiasetukset**-välilehti ja varmista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![sähköpostiasetukset-välilehti](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Valitse **Toimeenpanotili**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![toimeenpanotili-välilehti](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Älä muuta **Salausavaimet**-välilehden oletusasetuksia.

    [![salausavaimet-välilehti](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Valitse **Tilausasetukset**-välilehti ja tarkista, että asetukset ovat samat kuin seuraavassa kuvassa.

    [![tilausasetukset-välilehti](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Älä muuta **Skaalauskäyttöönotto**-välilehden oletusasetuksia.

    [![skaalauskäyttöönotto-välilehti](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Älä muuta **Power BI -integrointi** -välilehden oletusasetuksia.

    [![power bi -integrointi -välilehti](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Sulje **Reporting Services -määritystenhallintasovellus** valitsemalla **Lopeta**.

    [![reporting Servicesin määritystenhallinnan sulkeminen](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
