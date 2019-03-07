---
title: Kulujen työnkulku
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmää käytetään kuluraporttien tarkastusprosessien luomiseen kulujenhallinnassa.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 037a6ae00b7d559f79860901f0cb2ad6ddddd7aa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "310113"
---
# <a name="expense-workflow"></a>Kulujen työnkulku

[!include [banner](../includes/banner.md)]

Voit käyttää Microsoft Dynamics 365 for Finance and Operationsin työnkulkujärjestelmää kuluraporttien tarkastusprosessien luomiseen kulujenhallinnassa. Voit määrittää työnkulun, joka määrittelee kuluraporttien hyväksyjät seuraavien ehtojen perusteella:

- Työntekijän raportointihierarkia ja ennalta määritellyt hyväksyntärajat
- Monitasoinen hyväksyntä, joka tukee väliaikaisia hyväksyjiä ja lopullista hyväksyjää
- Taloushallinnon dimensiot ja projektin vastuualueet
- Määrittäminen tietyille käyttäjille tai käyttäjäryhmille

Työnkulun hyväksynnät voidaan luoda kuluraporteille, matkustusehdotuksille, käteisennakoille ja arvonlisäveron (ALV) palautuksille.

**Esimerkki**

Seuraava prosessi on esimerkki kulujenhallinnan työnkulusta kuluraporttia varten.

1. Työntekijä luo ja tallentaa kuluraportin.
2. Työntekijä lähettää kuluraportin toiselle työntekijälle hyväksyttäväksi. Hyväksyjä päätetään työnkulkua määritellessä luotujen sääntöjen mukaan.
3. Hyväksyjä saa ilmoituksen kuluraportista, joka on valmis hyväksyttäväksi. Hyväksyjä tarkistaa kuluraportin ja varmistaa, että seuraavat ehdot täyttyvät:

    - Kulut eivät riko mitään kulukäytäntöjä. Jos kulu rikkoo käytäntöä, hyväksyjä varmistaa, että kuluraportissa on hyväksyttävä liiketoiminnallinen peruste.
    - Kuluraporttiin on liitetty sähköisiä kuitteja.

4. Hyväksyjä hyväksyy kuluraportin.
5. Kuluraportti annetaan ostoreskontran koordinaattorille kirjattavaksi.
6. Jokin seuraavista vaiheista toteutuu, riippuen siitä, onko automaattinen kirjaus määritetty:

    - Jos automaattinen kirjaus on määritetty, kuluraportti käsitellään maksettavaksi ja kuluraportin tila päivitetään.
    - Jos automaattista kirjausta ei ole määritetty, jos ostoreskontran koodrinaattori varmistaa, että alkuperäiset kuitit on lähetetty ja että kuitit on kohdistettu kuluraportin kuluihin. Kaikki kuluraportille kirjatut verokoodit on myös varmistettava.

Kun nämä vaatimukset on varmistettu, kuluraportti kirjataan.

Kun kuluraportti on kirjattu, sen maksaminen hyväksytään ja työntekijää hyvitetään.
