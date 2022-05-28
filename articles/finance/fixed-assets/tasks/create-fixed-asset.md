---
title: Luo käyttöomaisuuserä
description: Tässä ohjeaiheessa käsitellään uuden käyttöomaisuustietueen luontia käyttöomaisuuden luettelosivulta.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9394c0c7a5e2d9b417cbaee9f4e67f36ae124fb
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714282"
---
# <a name="create-a-fixed-asset"></a>Luo käyttöomaisuuserä

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa käsitellään uuden käyttöomaisuustietueen luontia **Käyttöomaisuus**-luettelosivulta.

Järjestelmä määrittää käyttöomaisuuserän numeron käyttöomaisuusryhmällä määritetyn numerosarjan perusteella. Jos käyttöomaisuuseriä tuodaan Microsoft Excel -apuohjelman avulla käyttöomaisuusmalleja käyttämällä tai jos käytössä on toinen tuontityö, järjestelmä luo automaattisesti käyttöomaisuustietueet ja kasvattaa käyttöomaisuuserän numeroa.

Käyttöomaisuustietue luodaan manuaalisesti seuraavasti:

1. Valitse **Siirtymisruutu \> Moduulit \> Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**.
2. Valitse **toimintoruudussa** **Uusi**.
3. Syötä tai valitse arvo **Käyttöomaisuusryhmä**-kentässä. **Numero**-kenttään määritetään oletusarvo, jos **käyttöomaisuusparametrien** ja **käyttöomaisuusryhmän** **Käyttöomaisuuserien automaattinen numerointi** -toiminto on käytössä. Jos se ei ole käytössä, syötä käyttöomaisuuden yksilöivä numero.
4. Anna **Nimi**-kenttään arvo. Syötä käyttöomaisuuserää koskevat lisätiedot, joita yritys tarvitsee.
5. Valitse **toimintoruudussa** **Kirjat**.
6. Kirjoita päivämäärä **Hankintapäivämäärä**-kenttään.
7. Syötä **Hankintahinta**-kenttään numero.

    - Anna käyttöomaisuuserää koskevat lisätiedot, joita kirja tarvitsee.
    - Anna poistokirjoja koskevat lisätiedot, joita jäljellä olevat kirjat tarvitsevat.

8. Sulje sivu.

Käyttöomaisuuseriä voi luoda myös Excel-apuohjelmalla tai suorittamalla tuontityön **Tiedonhallinta**-työtilassa. Annan arvot mallin pakollisiin kenttiin ennen tuonnin suorittamista.

Jos Excel-apuohjelman mallissa tai tiedonhallinnassa ei määritetty käyttöomaisuuserän numeroa, järjestelmä luo käyttöomaisuuserän numeron kullekin tuodulle käyttöomaisuudelle ja kasvattaa numerosarjaa automaattisesti kunkin kohdalla. Jos käyttöomaisuuserät tuodaan ja niiden numerot määritetään mallissa, järjestelmä **ei** kasvata numerosarjaa automaattisesti. Siinä tapauksessa järjestelmänvalvojan on ehkä päivitettävä numerosarja manuaalisesti. Jos määritit käyttöomaisuuserän numero Excel-apuohjelman mallissa, järjestelmä käyttää määritettyä käyttöomaisuuserän numero ja kasvattaa numerosarjaa.

> [!NOTE]                                                                                                         
> Poiston kirjaamisen jälkeen **Käyttöönotto**- ja **Poiston suorituspäivä** -kentät lukitaan **Kirja**-sivulla. Kumpaakaan kenttää ei myöskään päivitetä tietoentiteetistä.

> [!WARNING]
> Käyttöomaisuustietuetta ei poisteta, jos tapahtumat kirjattiin siihen liittyvään kirjaan tai jos juuri luotu käyttöomaisuuserä syötetään kirjauskansioriville, mutta sitä ei kirjata. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
