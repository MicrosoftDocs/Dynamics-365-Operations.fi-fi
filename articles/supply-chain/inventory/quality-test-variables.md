---
title: Laadunhallinnan testimuuttujat
description: Tässä aiheessa kuvataan, kuinka luodaan testimuuttujia, joita voidaan käyttää laadullisissa testeissä Microsoft Dynamics 365 Supply Chain Managementissa.
author: rachel-profitt
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
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021705"
---
# <a name="quality-management-test-variables"></a>Laadunhallinnan testimuuttujat

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka luodaan testimuuttujia, joita voidaan käyttää laadullisissa testeissä Microsoft Dynamics 365 Supply Chain Managementissa.

Jokaiselle **Testit**-sivulla määritetylle laadulliselle testille on määritettävä testimuuttuja ja mahdolliset tulokset. (Laadullisten testien kohdalla **Tyyppi**-kentän asetuksena **Testit**-sivulla on *Asetus*.)

Voit määrittää, muokata ja tarkastella **Testimuuttujat**-sivulla laadulliseen testiin liittyvän testimuuttujan mahdollisia tuloksia. Määritä kunkin tuloksen tulostilaksi joko *Hyväksytty* tai *Epäonnistuminen*. Näin ilmaistaan, hyväksytäänkö tai hylätäänkö testi, kun tulos valitaan testitulokseksi. Määritä yksittäisen laadullisen testin testimuuttuja ja oletustulos **Testiryhmät**-sivulla.

Jokaiselle testimuuttujalle on suositeltavaa määrittää vähintään kaksi tulosta: yksi, jonka tulostilana on *Hyväksytty*, ja yksi, jonka tulostilana on *Epäonnistuminen*. Määritettävien muuttujien tai tulosten kokonaismäärää ei ole rajoitettu. Lisäksi useat testit voivat käyttää samoja testimuuttujia tulosten kirjaamiseksi.

## <a name="examples-of-test-variables"></a>Esimerkkejä testimuuttujista

### <a name="example-1"></a>Esimerkki 1

Teollisuusyritys suorittaa kaksi testiä valmistetuille materiaaleille. Yhdessä testissä pH-taso liitetään värinauhaan. Hyväksyttävät pH-tasot ovat vaaleampia, ja hylätyt pH-tasot ovat tummempia. Toisessa testissä suoritetaan useita visuaalisia tarkastuksia, ja laatutyöntekijät määrittävät, läpäiseekö nimike visuaalisen tarkastuksen vai ei.

### <a name="example-2"></a>Esimerkki 2

Pikkuleipiä valmistava teollisuusyritys tarkastaa lopputuotteen testillä. Tarkastuksessa on useita muuttujia. Ensimmäinen muuttuja on maku, jonka mahdollisia tuloksia ovat hyvä ja paha. Toinen muuttuja on väri, jonka mahdollisia tuloksia ovat liian tumma, liian vaalea ja oikea.

## <a name="create-a-test-variable"></a>Testimuuttujan luominen

Voit luoda testimuuttujan seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Testimuuttujat**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Muuttuja** – Määritä muuttujan yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna muuttujan yksityiskohtainen kuvaus.

1. Kun uusi rivi on vielä valittuna, valitse **Tulokset** toimintoruudusta.
1. Valitse **Testimuuttujien tulokset** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Tulos** – Määritä tuloksen yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna tuloksen yksityiskohtainen kuvaus.
    - **Tuloksen tila** – Valitse joko *Hyväksytty* tai *Epäonnistuminen*. Näin ilmaistaan, hyväksytäänkö tai hylätäänkö testi, kun tulos valitaan testitulokseksi.

1. Toista edellinen vaihe kullekin lisätulokselle. Varmista, että vähintään yhden tuloksen tilana on *Hyväksytty* ja vähintään yhden tilana on *Epäonnistuminen*.
1. Sulje sivut.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan testin mittavälineet](quality-test-instruments.md)
- [Laadunhallinnan testit](quality-tests.md)
- [Laadunhallinnan testiryhmät](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
