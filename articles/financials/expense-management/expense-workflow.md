---
title: "Kulujen työnkulku"
description: "Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin työnkulkujärjestelmää käytetään kuluraporttien tarkastusprosessien luomiseen kulujenhallinnassa."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c2e01d4da04cd24c2df1690e6e354e1c03cb50d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="expense-workflow"></a>Kulujen työnkulku

[!include[banner](../includes/banner.md)]

Voit käyttää Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin työnkulkujärjestelmää kuluraporttien tarkastusprosessien luomiseen kulujenhallinnassa. Voit määrittää työnkulun, joka määrittelee kuluraporttien hyväksyjät seuraavien ehtojen perusteella:

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

