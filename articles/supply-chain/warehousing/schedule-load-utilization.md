---
title: "Ajoita kuormituksen käyttöaste"
description: "Tässä ohjeaiheessa kerrotaan, miten voit määrittää ja ajoittaa varaston kuormituksen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d52ad452c615a61739582431fcd100a7efa3d93a
ms.openlocfilehash: 350666cee8f2643c53e9eed8ee73299bbea1e757
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2018

---

# <a name="schedule-load-utilization"></a>Ajoita kuormituksen käyttöaste

[!include[banner](../includes/banner.md)]

Voit ajoittaa valittujen sijaintityyppien kuormituksen sekä arvioida nykyistä ja tulevaa kuormitusta. Voit arvioida yhden tai usean toimipaikan kuormituksen, varaston tai vyöhykkeen kuormitusyksiköt tai vyöhykkeen ja varaston yhdistetyn kuormituksen.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Varaston tai toimipaikan kuormituksen ajoittaminen ja tarkastelu

Ajoittamalla toimipaikkojen, varastojen tai vyöhykkeiden kuormituksen voit luoda tilan käytön asetukset ja liittää ne pääsuunnitelmaan.

Tilan käytön asetuksissa voit käyttää sijaintityyppejä, kuten **Bulkkisijainti** ja **Keräilysijainti**, jotka määrittävät, miten tilan käyttö suunnitellaan. Voit myös määrittää varastokuormituksen tilan, kuten **Vyöhyke**.

Tilan tulevan käyttöasteen projektio perustuu tietoihin, jotka on laskettu liitetyn pääsuunnitelman perusteella. Pääsuunnitelmat ennakoivat tuotannon ja toimintojen saapuvien ja lähtevien tilausten resurssisuunnittelua. Käytettävissä olevan tilan projektio perustuu tilan käytön asetuksen ja valitun pääsuunnitelman väliseen suhteeseen.

Käyttämällä tilan käytön asetuksissa kuormitustilaa voit määrittää, arvioidaanko kuormitus kullekin varastolle tai vyöhykkeelle vai sisältävätkö projektiot tietoja jokaisesta varastosta tai vyöhykkeestä vai tietoja sekä varastoista että vyöhykkeistä. Voit myös määrittää, jätetäänkö estetyt sijainnit pois kuormituksen käyttölaskelmista.

Voit suunnitella tilan käyttöä luomalla **Varastokuormituksen käyttöaste** -raportin. Kun luot tämän raportin, voit määrittää, arvioidaanko kunkin toimipaikan kuormituksen käyttöaste erikseen vai yhdessä vai arvioidaanko se valitun kuormitusyksikön, kuten vyöhykkeen tai varaston, mukaan.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Varaston tilan käytön asetusten luominen

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Varaston valvonta** \> **Tilan käyttö**.
2. Luo tilan käytön asetukset valitsemalla **Uusi**. Määritä uuden asetuksen tunnus ja nimi.
3. Valitse **Varaston kuormitustila** -kentässä, näytetäänkö tilan käyttöaste varaston, vyöhykkeen vai varaston ja vyöhykkeen mukaan.
4. Määritä **Jätä estetyt sijainnit pois** -asetukseksi **Kyllä** jättääksesi estetyt varastosijainnit pois käytettävissä olevan tilan laskennasta. Voit estää saapuvien ja lähtevien varastosijainnin määrittämällä sijainnin eston syyn **Syöttö estetty**- tai **Tuloste estetty** -kentissä **Muut**-välilehdellä **Varastosijainnit**-sivulla.
5. Valitse **Sijainnin tyyppi** -pikavälilehdessä tilan käyttöastetta laskettaessa käytettävät sijaintityypit. Sinun on valittava projektiolle vähintään yksi sijaintityyppi.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Tilan käytön asetuksen liittäminen pääsuunnitelmaan

1. Valitse **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Ajoita kuormituksen käyttöaste**.
2. Valitse **Pääsuunnitelma**-kentässä pääsuunnitelma.
3. Määritä **Päivien määrä** -kentässä, kuinka monta päivää nykyisten ja tulevien kuormitusten projektioon sisällytetään.
4. Valitse **Tilan käyttö** -kentässä nykyisten ja tulevien kuormitusten projektiossa käytettävät tilan käytön asetukset.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Kuormituksen käyttöasteprojektion määrittäminen ja tietojen näyttäminen

1. Valitse **Varastonhallinta** \> **Kyselyt ja raportit** \> **Fyysiset varastoraportit** \> **Varastokuormituksen käyttöaste**.
2. Valitse **Näyttöperuste**-kentässä tilan käyttöasteen projektio:

    - **Toimipaikka** – Arvioi kunkin toimipaikan tilan käyttöaste. Tämä on kätevä projektio esimerkiksi silloin, kun haluat tarkastella toimipaikan kaikkia varastoja ja tasoittaa varastojen välistä käyttöastetta.
    - **Kuormitusyksikkö** – Arvioi vyöhykkeiden tai varastojen käyttöaste. Käytettävissä oleva tila arvioidaan niiden arvojen mukaan, jotka olet valinnut **Varaston kuormitustila** -kentässä **Tilan käyttö** -sivulla tilan käytön asetusten luonnin yhteydessä.

3. Noudata yhtä näitä vaiheita sen arvo mukaan, jonka valitsit edellisessä vaiheessa:

    - Jos valitsit **Toimipaikka**-arvon **Näyttöperuste**-kentässä, **Toimipaikka**-kenttä on käytettävissä. Valitse vähintään yksi projektioon sisällytettävä toimipaikka.
    - Jos valitsit **Kuormitusyksikkö**-arvon **Näyttöperuste**-kentässä, **Kuormitusyksikkö**-kenttä on käytettävissä. Valitse kuormitusyksikkö.

4. Määrittämällä **Kuormitustyyppi**-kentässä **Tilavuus** tai **Paino** osoitat, mille varastotoimintayksikölle tilaa arvioidaan.
5. Valitse **Tilan käytön asetukset** -kentässä ne tilan käytön asetukset, joihin projektio perustuu.

