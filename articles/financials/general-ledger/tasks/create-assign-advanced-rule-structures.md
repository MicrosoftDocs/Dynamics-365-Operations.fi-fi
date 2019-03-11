---
title: Luo ja määritä lisäsääntörakenteet
description: Tässä tehtäväopastuksessa käsitellään lisäsääntörakenteen luomista ja sen määrittämistä tilirakenteeseen.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "367038"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Luo ja määritä lisäsääntörakenteet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä tehtäväopastuksessa käsitellään lisäsääntörakenteen luomista ja sen määrittämistä tilirakenteeseen. Opastuksessa käytetään USMF-demoyritystä.


## <a name="create-an-advanced-rule-structure"></a>Luo kehittynyt sääntörakenne
1. Valitse Kirjanpito > Tilikartta > Rakenteet > Lisäsääntörakenteet.
2. Avaa valintaikkuna valitsemalla Uusi.
3. Kirjoita Lisäsääntörakenteet-kenttää sääntörakennetta kuvaava nimi.
4. Kirjoita Kuvaus-kenttään rakennetta kuvaava arvo.
5. Valitse OK.
6. Valitse Lisää segmentti.
7. Valitse taloushallinnon dimensio segmenttiluettelosta.
    * Esimerkki: myymälä.  
8. Valitse Lisää segmentti.
9. Avaa lisäsääntörakenne napsauttamalla luettelossa sen linkkiä.
10. Valitse Aktivoi.
11. Valitse Aktivoi.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Käytä lisäsääntörakennetta tilirakenteeseen
1. Sulje lomake.
2. Sulje sivu.
3. Valitse Kirjanpito > Tilikartta > Rakenteet > Määritä tilirakenteet.
4. Etsi ja valitse luettelossa tilirakenne, johon haluat käyttää lisäsääntöä.
5. Avaa tilirakenne napsauttamalla sen nimeä.
6. Valitse Muokkaa.
    * Voit myös valita Lisäsäännöt, jolloin sinua pyydetään asettamalla tilirakenne luonnostilaan.  
7. Valitse Lisäsäännöt.
8. Avaa valintaikkuna valitsemalla Uusi.
9. Kirjoita arvo Lisäsääntö-kenttään.
10. Kirjoita arvo Nimi-kenttään.
11. Valitse Luo.
12. Valitse Lisää uusia kriteerejä.
13. Valitse Missä-kentässä päätili tai taloushallinnon dimensio.
14. Valitse Käyttäjä-kentässä vaihtoehto, kuten on välillä ja sisältää.
15. Kirjoita arvo Arvo-kenttään.
16. Kirjoita kautta-kenttään arvo.
17. Avaa valintaikkuna valitsemalla Lisää.
18. Etsi luettelosta lisäsääntörakenne, jota haluat käyttää, kun antamasi ehdot täyttyvät.
19. ValitseLisää.
20. Sulje sivu.
21. Valitse Aktivoi.
22. Valitse Aktivoi.

