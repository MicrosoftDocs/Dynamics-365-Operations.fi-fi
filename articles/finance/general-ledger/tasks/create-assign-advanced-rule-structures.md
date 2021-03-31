---
title: Luo ja määritä lisäsääntörakenteet
description: Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja määrittää lisäsääntörakenteen tilirakenteeseen.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a7b9d0c20a49996b4c8d45b030d9e587818de3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216542"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Luo ja määritä lisäsääntörakenteet

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja määrittää lisäsääntörakenteen tilirakenteeseen. Opastuksessa käytetään USMF-demoyritystä.

## <a name="create-an-advanced-rule-structure"></a>Luo kehittynyt sääntörakenne
1. Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Rakenteet > Lisäsääntörakenteet**.
2. Avaa valintaikkuna valitsemalla **Uusi**.
3. Kirjoita **Lisäsääntörakenteet**-kenttää sääntörakennetta kuvaava nimi.
4. Valitse **OK**.
5. Valitse **Lisää segmentti**.
6. Valitse taloushallinnon dimensio segmenttiluettelosta. Esimerkki: **Myymälä**.  
7. Valitse **Lisää segmentti**.
8. Valitse **Aktivoi**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Käytä lisäsääntörakennetta tilirakenteeseen
1. Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Rakenteet > Tilirakenteiden konfigurointi**.
2. Etsi ja valitse luettelossa tilirakenne, johon haluat käyttää lisäsääntöä.
3. Valitse **Muokkaa**. Voit myös valita **Lisäsäännöt**, jolloin sinua pyydetään asettamalla tilirakenne **Luonnos**-tilaan.  
4. Valitse **Lisäsäännöt**.
5. Avaa valintaikkuna valitsemalla **Uusi**.
6. Kirjoita arvo **Lisäsääntö**-kenttään.
7. Kirjoita arvo **Nimi**-kenttään.
8. Valitse **Luo**.
9. Valitse **Lisää uusia kriteerejä**.
10. Valitse **Missä**-kentässä päätili tai taloushallinnon dimensio.
11. Valitse **Käyttäjä**-kentässä vaihtoehto, kuten **on välillä** ja **sisältää**.
12. Kirjoita arvo **Arvo**-kenttään.
13. Kirjoita **kautta**-kenttään arvo.
14. Avaa valintaikkuna valitsemalla **Lisää**.
15. Etsi luettelosta lisäsääntörakenne, jota haluat käyttää, kun antamasi ehdot täyttyvät.
16. Valitse **Lisää**.
17. Sulje sivu.
18. Valitse **Aktivoi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]