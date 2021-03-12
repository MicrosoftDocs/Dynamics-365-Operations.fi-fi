---
title: Ostoehdotukset
description: Tässä aiheessa käsitellään ostoehdotusten tukemista suunnittelun optimoinnissa.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8075f8d7c3868c6d6012edbce17dbbb4749209ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992341"
---
# <a name="purchase-requisitions"></a>Ostoehdotukset

Pääsuunnittelu voi täydentää hyväksyttyjä ostoehdotuksia. Niinpä käyttäjien ei tarvitse käyttää työnkulkua ostoehdotuksia koskevien ostotilausten luontiin. Ostoehdotukset voidaan siis käsitellä pääsuunnittelussa. Tämän toiminnon ansiosta ostoehdotuksesta voidaan luoda ostotilaus, siirtotilaus tai tuotantotilaus sen mukaan, mikä **Suunniteltu tilaustyyppi** -arvo on määritetty liittyvälle tuotteelle.

## <a name="enable-master-plans-to-include-requisitions"></a>Ehdotusten sisällyttämisen ottaminen käyttöön pääsuunnitelmissa

Ehdotukset sisällytetään pääsuunnittelun kattavuuslaskentaan seuraavasti:

1. Valitse **Pääsuunnittelu** \> **Määritykset** \> **Suunnitelmat** \> **Pääsuunnitelmat**.
1. Luo tai valitse pääsuunnitelma.
1. Määritä **Yleinen**-pikavälilehdessä **Sisällytä ehdotukset** -asetukseksi *Kyllä*.
1. Toista vaiheet 2 ja 3 jokaiselle muulle pääsuunnitelmalle, johon ehdotukset halutaan sisällyttää.

## <a name="approved-requisitions-time-fence"></a>Hyväksyttyjen ehdotusten aikaraja

*Hyväksytty ehdotusten aikaraja* määrittää, mistä lähtien (päivinä) pääsuunnittelu sisällyttää kysynnän hyväksytyistä täydennysehdotuksista. Hyväksyttyjen ehdotusten aikarajan voi määrittää sekä kattavuusryhmätasolla että pääsuunnittelutasolla.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Kattavuusryhmän hyväksyttyjen ehdotusten aikarajan määrittäminen

1. Valitse **Pääsuunnittelu** \> **Määritys** \> **Kattavuus** \> **Kattavuusryhmä**.
1. Luo tai valitse kattavuusryhmä.
1. Määritä **Muu**-pikavälilehden **Hyväksyttyjen ehdotusten aikaraja (päivää)** -kenttään aikarajaan sisällytettävien päivien määrä.
1. Toista vaiheet 2 ja 3 jokaisessa kattavuusryhmässä, jossa halutaan määrittää hyväksyttyjen ehdotusten aikaraja.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Yksittäisten pääsuunnitelmien hyväksyttyjen ehdotusten aikarajan määrittäminen

Kun hyväksyttyjen ehdotusten aikaraja määritetään yksittäiselle pääsuunnitelmalle, asetus ohittaa minkä tahansa käytettävän kattavuusryhmän aikaraja-asetuksen.

1. Valitse **Pääsuunnittelu** \> **Määritykset** \> **Suunnitelmat** \> **Pääsuunnitelmat**.
1. Luo tai valitse pääsuunnitelma.
1. Määritä **Aikarajat päivinä** -pikavälilehden **Hyväksyttyjen ehdotusten aikaraja (päivää)** -kenttään aikarajaan sisällytettävien päivien määrä.
1. Toista vaiheet 2 ja 3 jokaisessa pääsuunnitelmassa, jossa halutaan määrittää hyväksyttyjen ehdotusten aikaraja.

> [!IMPORTANT]
> **Tulossa pian:** Hyväksyttyjen ehdotusten aikarajoja ei tueta vielä suunnittelun optimoinnissa. Niin kauan kun niitä ei tueta, kaikki **Hyväksyttyjen ehdotusten aikaraja (päivää)** -kenttään annetut arvot ohitetaan.

## <a name="independent-supply-regardless-of-coverage-code"></a>Kattavuuskoodista riippumaton erillinen toimitus

Erilliset suunnitellut tilaukset kattavat aina ostoehdotukset kattavuuskoodista riippumatta. Tämä toiminta varmistaa selkeän jäljitettävyyden sekä ostoehdotusten ja täydennystilausten väliset työnkulut.

### <a name="example-1"></a>Esimerkki 1

Tuote määritetään siten, että sen **Kattavuuskoodi**-arvo on *Min./Maks.*

- Käytettävissä olevan varaston määrä = 10.
- Varaston vähimmäismäärä = 15.
- Varaston enimmäismäärä = 20.
- Aiemmin luotu yhden kappaleen ostoehdotus. Sen pyydetty päivämäärä on kuluva päivä.

Pääsuunnittelua suoritettaessa luodaan kaksi suunniteltua tilausta: yksi 10 kpl:n tilaus täydentämään varasto maksimimäärään ja toinen 1 kpl:n tilaus täydentämään ostoehdotus.

### <a name="example-2"></a>Esimerkki 2

Tuote määritetään siten, että sen **Kattavuuskoodi**-arvo on *Min./Maks.*

- Käytettävissä olevan varaston määrä = 17.
- Varaston vähimmäismäärä = 15.
- Varaston enimmäismäärä = 20.
- Aiemmin luotu yhden kappaleen ostoehdotus. Sen pyydetty päivämäärä on kuluva päivä.

Pääsuunnittelua suoritettaessa luodaan yksi yhden kappaleen tilaus täydentämään ostoehdotus.

### <a name="example-3"></a>Esimerkki 3

Tuote määritetään siten, että sen **Kattavuuskoodi**-arvo on *Kausi* ja kauden pituus on seitsemän päivää. Siinä on seuraavat varaston, myyntitilauksen ja ehdotuksen tilat:

- Käytettävissä olevan varaston määrä = 0.
- Aiemmin luotu viiden kappaleen myyntitilaus. Sen odotettu lähetyspäivä on kuluva päivä + yksi päivä.
- Aiemmin luotu kolmen kappaleen ostoehdotus. Sen pyydetty päivämäärä on kuluva päivä + kolme päivää.

Pääsuunnittelua suoritettaessa luodaan kaksi suunniteltua tilausta: yksi kolmen kappaleen tilaus täydentämään ostoehdotus ja yksi viiden kappaleen tilaus täydentämään myyntitilauksen kysyntä.

> [!NOTE]
> Kun ostoehdotukseen tarvekohdistettu suunniteltu tilaus on vahvistettu, suunnittelumoduuli säilyttää tarvekohdistuksen ostoehdotukseen. Jos myöhemmin huomataan, että vahvistetusta tilauksesta puuttuu jokin määrä, joka tarvitaan ostoehdotuksen täyttämiseen, järjestelmä luo eron kattavan uuden suunnitellun tilauksen.

Lisätietoja ostoehdotuksista on kohdassa [Ostoehdotusten yleiskatsaus](../../procurement/purchase-requisitions-overview.md).
