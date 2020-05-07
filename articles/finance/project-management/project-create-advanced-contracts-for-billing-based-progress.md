---
title: Tilaan perustuvien edistyksellisten laskutussopimusten luominen
description: Tässä ohjeaiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttiosuuden perusteella.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282823"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Tilaan perustuvien edistyksellisten laskutussopimusten luominen
[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttiosuuden perusteella. Laskusummat lasketaan automaattisesti projektissa määritetyn työn budjettiluokkia varten. Laskujen ajoitus määritetään, kun projektisopimus neuvotellaan asiakkaan kanssa.

Näiden ohjeaiheiden avulla voit määrittää sopimuksen, liittyvän projektin ja laskutussäännöt, joita käytetään projektia varten määritetyn työn budjettiluokkien laskujen summien laskentaan.

Kun sopimus ja projekti on luotu, voit määrittää projektin tiedot. Voit esimerkiksi määrittää toiminnot ja projektin työntekijät.

## <a name="example"></a>Esimerkki

Organisaatiosi on ohjelmistokehitysyritys. Sitoudut kehittämään asiakkaalle palkanlaskennan kirjanpitopaketin 20 000 dollarin (USD) kokonaismaksua vastaan. Organisaatiosi sitoutuu lähettämään asiakkaalle laskun, kun projektista on valmiina määritetty prosenttiosuus. Voit määrittää työlle seuraavat projektiluokat, jotta voit käyttää niitä laskutusprosessissa:

- Konsultointi
- Suunnittelu
- Asentaminen

Määrität myös laskutussäännöt, jotka laskevat automaattisesti laskujen summat kunkin luokan projektitöiden valmistumisprosentin mukaan.

Budjettipäällikkö luo budjetin projektiluokkia varten. Valmiin työn määrä lasketaan automaattisesti verrattuna todellisen työn prosenttiosuutta budjetoituihin määriin.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin luot projektin, joka käyttää laskutussääntöjä, sinun on määritettävä laskutussääntöjen numerosarjat sekä maksukirjauskansio, jota käytetään edistymisen kirjaamiseen.

1. Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**.
2. Määritä **Projektinhallinnan ja kirjanpidon parametrit** -sivun **numerosarjat**-välilehdessä numerosarja, jota haluat käyttää laskutussääntöjen luonnin yhteydessä.
3. Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Kirjauskansiot** \> **Maksu**.
4. Valitse **Maksukirjauskansio**-sivulla **Uusi** ja kirjoita kirjauskansion nimi.

## <a name="create-a-contract-for-progress-billings"></a>Sopimuksen luominen edistymiseen perustuvaa laskutusta varten

Tämän toiminnon avulla voit luoda projektisopimuksen kiinteähintaista projektia varten. Luot projektilaskun, kun projektin työstä valmistunut osuus saavuttaa määritetyn prosenttiosuuden.

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Projektisopimukset**.
2. Valitse **Projektisopimukset**-sivulla **Uusi**.
3. Määritä **Uusi projektisopimus** -valintaikkunassa seuraavat kentät:

    - **Nimi**
    - **Rahoitustyyppi**
    - **Rahoituslähde**
    - **Myyntivaluutta** – Tätä valuuttaa käytetään oletusarvoisesti asiakkaan laskuille, jotka on liitetty projektisopimukseen. Voit kuitenkin muuttaa tietyn myyntilaskun myyntivaluuttaa.

4. Valitse **OK**. Tiedot kopioidaan **Projektisopimukset**-sivun otsikkoon.
5. Täytä **Projektisopimukset**-sivulla loput projektin pakolliset tiedot.

## <a name="create-a-project-for-progress-billings"></a>Projektin luominen edistymiseen perustuvaa laskutusta varten

Näiden ohjeiden avulla voit luoda projektin ja projektisopimukseen liittyvät aliprojektit.

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.
2. Valitse **Kaikki projektit** -sivulla **Uusi**.
3. Valitse **Uusi projekti** -valintaikkunan **Projektityyppi**-kentässä**Aika ja materiaali**.
4. Valitse projektiryhmä. Projektiryhmä määrittää ryhmään liitettyjen projektien kirjaustiedot.
5. Valitse **Luo projekti**.
6. Kun projekti on luotu, määritä projektin vaiheeksi **Käsittelyssä** .

## <a name="create-a-budget-for-a-project"></a>Budjetin luominen projektia varten

Budjettiluokkien avulla lasketaan automaattisesti laskusummat, jotka laskutetaan asiakkaalta kunkin luokan valmistuneesta työstä. Seuraavia vaiheita noudattamalla voit luoda arvioituja kustannuksia koskevia budjettiluokkia.

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.
2. Valitse ja avaa haluamasi projekti **Kaikki projektit** -sivulla.
3. Valitse **Projektit**-sivulla Toimintoruudun **Suunnitelma**-välilehden **Budjetti**-ryhmässä **Projektibudjetti**.
4. Anna **Projektibudjetti**-sivulla arvioitu kustannus projektin jokaista luokkaa varten.

## <a name="create-billing-rules-for-progress-billings"></a>Laskutussääntöjen luominen työn edistymiseen perustuvaa laskutusta varten

1. Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Projektisopimukset**.
2. Valitse **Projektisopimukset** -sivulla projektisopimus ja avaa se.
3. Valitse projektisopimus-sivun **Laskutussäännöt**-pikavälilehdessä **Lisää**.
4. Valitse **Laskutussääntö**-sivun **Rivityyppi**-kentässä **Edistyminen**.
5. Kirjoita sopimuksen kokonaisarvo **Laskutussäännön rivitiedot** -pikavälilehden **Sopimuksen arvo** -kenttään.
6. Valitse **Luokka**-kentässä luokka, johon maksutapahtuma kirjataan.
7. Valitse **Projekti**-kentässä projekti tai tehtävä, joka käyttää laskutussääntöä.
8. Valinnainen: Määritä laskutussääntö lisäprojekteihin. Valitse **Projekti**-pikavälilehden **Käytettävissä olevat projektit** -osasta ja lisää sitten projekti **Valitut projektit** -osaan valitsemalla oikea nuolipainike.
9. Valinnainen: Laske prosenttimäärä, jonka asiakas pidättää laskun maksuista. Valitse rahoituslähde **Maksun pidätysehto** -pikavälilehdeltä ja kirjoita sitten **Pidätysprosentti**-kenttään.
10. Toista tämä vaiheet, jos haluat luoda lisää projektisopimuksen laskutussääntöjä.
