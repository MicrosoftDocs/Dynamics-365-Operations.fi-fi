---
title: Mittayksikön hallinta
description: Tässä menettelyssä kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.
author: sorenva
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 966e189e7395bec15d2c62735c6df3df2ab34b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817962"
---
# <a name="manage-unit-of-measure"></a>Mittayksikön hallinta

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään. Voit käydä tämän menettelyn läpi esittelytietojen avulla tai käyttää omia tietojasi.

1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetun tuotteen ylläpito**.
2. Valitse **Yksiköt**.

## <a name="create-a-unit-of-measure"></a>Mittayksikön luominen
1. Valitse **Uusi**.
2. Kirjoita arvo **Yksikkö**-kenttään. Syötä mittayksikköön viitatessa käytettävä tunnus tai symboli.  
3. Kirjoita **Kuvaus**-kenttään arvo. Syötä mittayksikölle kuvaava nimi järjestelmän kielellä.  
4. Valitse **Yksikköluokka**-kentässä vaihtoehto. Yksikköluokka määrittää, mihin loogiseen ryhmittelyyn, kuten alue, paino tai määrä, mittayksikkö kuuluu.  
5. Syötä **Desimaalitarkkuus**-kenttään numero. Määritä, miten paljon mittayksikön desimaaleja pyöristetään laskelman valmistuessa.  
6. Valitse **Tallenna**.

## <a name="define-unit-translations"></a>Yksikkökäännösten määrittäminen
1. Valitse **toimintoruudussa** **Yksikön tekstit**.
2. Valitse **Uusi**. Käytä yksikön tekstiä, kun luot mittayksikköä kuvaavan tunnuksen tai symbolin käännöksen. Tätä käytetään asiakas- tai toimittajakohtaisten kielten ulkoisissa asiakirjoissa.  
3. Syötä tai valitse arvo **Kieli**-kentässä.
4. Kirjoita arvo **Teksti**-kenttään.
5. Valitse **Tallenna**.
6. Sulje sivu.
7. Valitse **toimintoruudussa** **Käännetyt yksiköiden kuvaukset**.
8. Valitse **Uusi**. Määritä mittayksikön kielikohtaiset kuvaukset.  
9. Syötä tai valitse arvo **Kieli**-kentässä.
10. Kirjoita **Kuvaus**-kenttään arvo.
11. Valitse **Tallenna**.
12. Sulje sivu.

## <a name="define-unit-conversion-rules"></a>Yksikön muunnössääntöjen määrittäminen
1. Valitse **toimintoruudussa** **Yksikkömuunnokset**. Määritä mittayksikön muuntamisen säännöt valitussa yksikköluokassa.  
2. Avaa valintaikkuna valitsemalla **Uusi**.
3. Syötä **Kerroin**-kenttään numero. Muuntokerroin Yksiköstä- ja Yksikköön-kohdan välillä. Esimerkiksi senttimetrien muuntokerroin metreiksi on 100, koska metri sisältää 100 senttimetriä.  
4. Syötä tai valitse **Yksikköön**-kentän arvo.
5. Valitse vaihtoehto **Pyöristys**-kentässä. Määritä, miten muunnettu arvo pyöristetään.  
6. Valitse **OK**.
7. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]