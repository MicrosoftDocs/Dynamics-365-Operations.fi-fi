---
title: Laadunhallinnan testin mittavälineet
description: Tässä aiheessa kuvataan, kuinka luodaan testin mittavälineitä, joita voidaan käyttää laatutilausten testeissä Microsoft Dynamics 365 Supply Chain Managementissa.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956640"
---
# <a name="quality-management-test-instruments"></a>Laadunhallinnan testin mittavälineet

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka luodaan testin mittavälineitä, joita voidaan käyttää laatutilausten testeissä Microsoft Dynamics 365 Supply Chain Managementissa.

**Testin mittavälineet** -sivulla voit määrittää ja tarkastella tietoja laitteista, joita käytetään laatutilausten testien suorittamiseen. Testin mittavälineet ovat valinnaisia. Ne voivat kuitenkin auttaa laatutyöntekijöitä tietämään, mitä laitetta tai työkalua heidän tulee käyttää tietyn testin suorittamiseen.

## <a name="test-instrument-example"></a>Esimerkki testin mittavälineestä

Suoritat useita sähkökomponenttien testejä. Jotkut testit koskevat komponenttien jännitelähtöä, yksi testi niiden lämpötilaa ja yksi testi niiden painoa. Testien suorittamiseen käytetään erilaisia työkaluja, laitteita tai laitteistoja. Esimerkiksi jännitemittaria käytetään jännitteen mittaamiseen, lämpömittaria lämpötilan mittaamiseen ja vaakaa painon mittaamiseen. Voit konfiguroida kunkin näistä laitteista testin mittavälineenä ja määrittää mittayksikön, jolla testitulokset on kirjattava. Esimerkiksi jännitemittarin tulokset tallennetaan voltteina, lämpömittarin tulokset kirjataan Fahrenheit-asteina tai Celsius-asteina ja vaa'an tulokset kirjataan paunoina tai kilogrammoina.

## <a name="create-a-test-instrument"></a>Uuden testin mittavälineen luominen

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testin mittavälineet**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Testin mittaväline** – Määritä testin mittavälineen yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna testin mittavälineen yksityiskohtainen kuvaus.
    - **Yksikkö** – Valitse yksikkö, jossa mittaväline mittaa tuloksia. **Tarkkuus**-kenttä määritetään automaattisesti valitsemaani yksikköön perustuen.

1. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan testi](quality-tests.md)
- [Laadunhallinnan testiryhmät](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
