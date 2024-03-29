---
title: Kuormien ja lähetysten suunnittelu kuormasuunnittelun työtilassa
description: Tässä artikkelissa kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla.
author: Mirzaab
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e53b7667dd4589a7c6c14b8aaf8ba51017eee0d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068327"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Kuormien ja lähetysten suunnittelu kuormasuunnittelun työtilassa

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten myyntitilaukselle luodaan kuorma kuormasuunnittelun työtilan avulla. Ensimmäiseksi luodaan edellytyksenä oleva myyntitilaus. Tämä menettely on osa kuljetuskoordinaattorin päivittäistä työtä. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-a-sales-order"></a>Luo myyntitilaus
1. Siirry siirtymisruudussa kohtaan **Moduulit > Myyntireskontra > Tilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Avaa haku valitsemalla **Asiakastili**-kentässä avattavan valikon painike.
4. Valitse tili **US-004**.
5. Valitse **OK**.
6. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.
7. Valitse nimike **A0001**. **A0001** on kuljetustenhallinnan käytössä.  
8. Avaa haku valitsemalla **Toimipaikka**-kentässä avattavan valikon painike ja valitse nimike.
9. Anna **Määrä**-kentässä numero.
10. Kirjoita tässä esimerkissä **Varasto**-kenttään 24. Kuljetuksenhallinta ja varastonhallintaprosessit (WMS) ovat tässä varastossa käytössä.  
11. Valitse **Tallenna**.
12. Sulje sivu.

## <a name="create-a-new-load"></a>Uuden kuorman luominen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila**.
2. Valitse **Myyntirivit**-välilehti. Muodostetaan nyt juuri luodulle myyntitilaukselle kuorma. Kuormat voidaan muodostaa tarjonnan ja kysynnän perusteella ostotilauksista, siirtotilauksista ja myyntitilauksista.  
3. Valitse toimintoruudussa **Tarjonta ja kysyntä**.
4. Valitse **Uuteen kuormaan**.
5. Avaa haku valitsemalla **Kuorman mallitunnus** -kentässä avattavan valikon painike. Kuormamalli määrittää koko kuorman painon ja tilavuuden enimmäismitat. Kuormamalli voi esittää esimerkiksi kontin tai kuorma-auton koon. Valitse nimike.
6. Valitse **OK**.

## <a name="rate-and-route-the-load"></a>Kuorman hinnan ja reitityksen määrittäminen
1. Valitse **Hinnoittelu ja reititys**.
2. Valitse **Hinnan ja reitin työtila**.
3. Valitse **Hintavertailu**.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse **Määritä**.
6. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]