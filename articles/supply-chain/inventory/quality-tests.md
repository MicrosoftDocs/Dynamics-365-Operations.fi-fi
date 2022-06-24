---
title: Laadunhallinnan testit
description: Tässä artikkelissa kuvataan, kuinka luodaan testejä, joita voidaan käyttää laatutilauksissa Microsoft Dynamics 365 Supply Chain Managementissa.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac67ee97a4890c646daefa6b09feae25c4f15d0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857602"
---
# <a name="quality-management-tests"></a>Laadunhallinnan testit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka luodaan testejä, joita voidaan käyttää laatutilauksissa Microsoft Dynamics 365 Supply Chain Managementissa.

Voit määrittää ja tarkastella **Testit**-sivulla yksittäisiä testejä, joiden mukaan määräytyy, ovatko tuotteet laatuvaatimusten mukaisia. Voit määrittää testiryhmälle vähintään yhden yksittäisen testin. Siinä tapauksessa määrität myös testikohtaiset tiedot, kuten hyväksyttävät mitta-arvot. Mitta-arvoja käytetään määrällisissä testeissä. Laadullisia testejä varten käytetään testimuuttujia.

- Määrällisissä testeissä **Tyyppi**-kentän arvoksi on määritetty *Kokonaisluku* tai *Murtoluku*. Myös mittayksikkö määritetään. Laatumääritykset ja testitulokset ilmaistaan numeroina.
- Laadullisissa testeissä **Tyyppin**-kentän asetuksena on *Asetus*. Laadullista testiä varten tarvitaan lisätietoja mitattavasta testimuuttujasta ja sen numeroiduista vaihtoehdoista. Laatumääritykset ja testitulokset ilmaistaan tuloksen perusteella.

Voit määrittää testille myös testin mittavälineen. Testin mittavälineitä ei kuitenkaan tarvita laatutilausten testien luomiseen ja käyttöön. Lisätietoja on kohdassa [Laadunhallinnan testin mittavälineet](quality-test-instruments.md).

Voit myös halutessasi määrittää testille yksikön, joka ilmaisee, missä mittayksikössä testitulokset kirjataan. Esimerkiksi lämpötilatesti voi sisältää yksikön joko Fahrenheit- tai Celsius-asteina.

## <a name="example-of-a-test"></a>Esimerkki testistä

Teollisuusyritys suorittaa ostamalleen materiaalille kaksi testiä: materiaalin laatua koskevan määrällisen testin ja pakkausvahinkoja koskevan laadullisen testin. Yritys määrittää laadullisen testin lisätiedoiksi testimuuttujan (esimerkiksi vioittunut pakkaus) ja sen mahdolliset tulokset. Yritys määrittää **Testiryhmät**-sivulla kaksi testiä testiryhmään. Lisäksi testikohtaiset tiedot määritetään. Testiryhmä määritetään laatutilaukseen, jotta yritys voi raportoida näiden kahden testin testitulokset.

## <a name="create-a-test"></a>Testin luominen

Luo testi seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testit**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Testi** – Määritä testin yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna testin yksityiskohtainen kuvaus.
    - **Tyyppi** – Valitse testin tuottamien tulosten tyyppi. Valitse määrällisissä testeissä *Murtoluku* tai *Kokonaisluku*. Valitse laadullisia testejä varten *Asetus*.
    - **Testin mittaväline** – Valitse [testin mittaväline](quality-test-instruments.md), jota testissä on käytettävä.
    - **Yksikkö** – Jos valitsit **Tyyppi**-kentässä *Murtoluku* tai *Kokonaisluku* (jos testi on määrällinen testi), valitse mittayksikkö, jossa testitulokset kirjataan.

1. Sulje sivu.

> [!NOTE]
> Kun olet tallentanut testin, et voi enää muokata ruudukon **Tyyppi**-kenttää. Jos testille tallennettavan testin tulosten tyyppiä on muutettava, valitse toimintoruudusta **Muuta laatutestin tyyppiä**. Määritä **Muuta laatutestin tyyppiä** -valintaikkunassa haluamasi tyyppinen **Uusi tyyppi** -kenttä ja sulje valintaikkuna valitsemalla **OK**.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan testin mittavälineet](quality-test-instruments.md)
- [Laadunhallinnan testiryhmät](quality-test-groups.md)
- [Laadunhallinnan testimuuttujat](quality-test-variables.md)
- [Laatuliitokset](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
