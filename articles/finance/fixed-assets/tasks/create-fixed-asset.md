---
title: Luo käyttöomaisuuserä
description: Tässä ohjeaiheessa käsitellään uuden käyttöomaisuustietueen luontia käyttöomaisuuden luettelosivulta.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000240"
---
# <a name="create-a-fixed-asset"></a>Luo käyttöomaisuuserä

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään uuden käyttöomaisuustietueen luontia **Käyttöomaisuus** -luettelosivulta.

Järjestelmä määrittää käyttöomaisuuserän numeron käyttöomaisuusryhmällä määritetyn numerosarjan perusteella. Jos käyttöomaisuuseriä tuodaan Microsoft Excel -apuohjelman avulla käyttöomaisuusmalleja käyttämällä tai jos käytössä on toinen tuontityö, järjestelmä luo automaattisesti käyttöomaisuustietueet ja kasvattaa käyttöomaisuuserän numeroa.

Käyttöomaisuustietue luodaan manuaalisesti seuraavasti:

1. Valitse **Siirtymisruutu \> Moduulit \> Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**.
2. Valitse **toimintoruudussa** **Uusi**.
3. Syötä tai valitse arvo **Käyttöomaisuusryhmä** -kentässä. **Numero** -kenttään määritetään oletusarvo, jos **käyttöomaisuusparametrien** ja **käyttöomaisuusryhmän** **Käyttöomaisuuserien automaattinen numerointi** -toiminto on käytössä. Jos se ei ole käytössä, syötä käyttöomaisuuden yksilöivä numero.
4. Anna **Nimi** -kenttään arvo. Syötä käyttöomaisuuserää koskevat lisätiedot, joita yritys tarvitsee.
5. Valitse **toimintoruudussa** **Kirjat**.
6. Kirjoita päivämäärä **Hankintapäivämäärä** -kenttään.
7. Syötä **Hankintahinta** -kenttään numero.

    - Anna käyttöomaisuuserää koskevat lisätiedot, joita kirja tarvitsee.
    - Anna poistokirjoja koskevat lisätiedot, joita jäljellä olevat kirjat tarvitsevat.

8. Sulje sivu.

Käyttöomaisuuseriä voi luoda myös Excel-apuohjelmalla tai suorittamalla tuontityön **Tiedonhallinta** -työtilassa. Annan arvot mallin pakollisiin kenttiin ennen tuonnin suorittamista.

Jos Excel-apuohjelman mallissa tai tiedonhallinnassa ei määritetty käyttöomaisuuserän numeroa, järjestelmä luo käyttöomaisuuserän numeron kullekin tuodulle käyttöomaisuudelle ja kasvattaa numerosarjaa automaattisesti kunkin kohdalla. Jos käyttöomaisuuserät tuodaan ja niiden numerot määritetään mallissa, järjestelmä **ei** kasvata numerosarjaa automaattisesti. Siinä tapauksessa järjestelmänvalvojan on ehkä päivitettävä numerosarja manuaalisesti. Jos määritit käyttöomaisuuserän numero Excel-apuohjelman mallissa, järjestelmä käyttää määritettyä käyttöomaisuuserän numero ja kasvattaa numerosarjaa.
