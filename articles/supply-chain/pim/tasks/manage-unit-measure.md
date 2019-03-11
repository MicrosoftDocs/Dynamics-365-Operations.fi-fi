---
title: Mittayksikön hallinta
description: Tässä menettelyssä kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e208b7f1faab77f2b97ff7b440a228656684fca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "358919"
---
# <a name="manage-unit-of-measure"></a>Mittayksikön hallinta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään. Voit käydä tämän menettelyn läpi esittelytietojen avulla tai käyttää omia tietojasi.

1. Siirry Vapautetun tuotteen ylläpito -kohtaan.
2. Valitse Yksiköt.

## <a name="create-a-unit-of-measure"></a>Mittayksikön luominen
1. Valitse Uusi.
2. Kirjoita arvo Yksikkö-kenttään.
    * Syötä mittayksikköön viitatessa käytettävä tunnus tai symboli.  
3. Kirjoita arvo Kuvaus-kenttään.
    * Syötä mittayksikölle kuvaava nimi järjestelmän kielellä.  
4. Valitse Yksikköluokka-kentässä vaihtoehto.
    * Yksikköluokka määrittää, mihin loogiseen ryhmittelyyn, kuten alue, paino tai määrä, mittayksikkö kuuluu.  
5. Syötä Desimaalitarkkuus-kenttään numero.
    * Määritä, miten paljon mittayksikön desimaaleja pyöristetään laskelman valmistuessa.  
6. Valitse Tallenna.

## <a name="define-unit-translations"></a>Yksikkökäännösten määrittäminen
1. Valitse Yksikön tekstit.
2. Valitse Uusi.
    * Käytä yksikön tekstiä, kun luot mittayksikköä kuvaavan tunnuksen tai symbolin käännöksen. Tätä käytetään asiakas- tai toimittajakohtaisten kielten ulkoisissa asiakirjoissa.  
3. Syötä tai valitse arvo Kieli-kentässä.
4. Kirjoita arvo Teksti-kenttään.
5. Valitse Tallenna.
6. Sulje sivu.
7. Valitse Käännetyt yksiköiden kuvaukset.
8. Valitse Uusi.
    * Määritä mittayksikön kielikohtaiset kuvaukset.  
9. Syötä tai valitse arvo Kieli-kentässä.
10. Kirjoita arvo Kuvaus-kenttään.
11. Valitse Tallenna.
12. Sulje sivu.

## <a name="define-unit-conversion-rules"></a>Yksikön muunnössääntöjen määrittäminen
1. Valitse Yksikön muunnokset.
    * Määritä mittayksikön muuntamisen säännöt valitussa yksikköluokassa.  
2. Avaa valintaikkuna valitsemalla Uusi.
3. Syötä Kerroin-kenttään numero.
    * Muuntokerroin Yksiköstä- ja Yksikköön-kohdan välillä. Esimerkiksi senttimetrien muuntokerroin metreiksi on 100, koska metri sisältää 100 senttimetriä.  
4. Syötä tai valitse Yksikköön-kentän arvo.
5. Valitse vaihtoehto Pyöristys-kentässä.
    * Määritä, miten muunnettu arvo pyöristetään.  
6. Valitse OK.
7. Sulje sivu.

