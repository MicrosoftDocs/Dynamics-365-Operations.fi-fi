---
title: Luo kulukoodeja
description: Tässä aiheessa kerrotaan, miten sekä ostoreskontran että myyntireskontran kulukoodit määritetään.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 034be190890a67fd0921d40fffdc704b9d6d5df7
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014047"
---
# <a name="create-charges-codes"></a>Luo kulukoodeja

Tässä aiheessa kerrotaan, miten sekä ostoreskontran että myyntireskontran kulukoodit määritetään. Jos organisaatio edellyttää, että myynti- tai ostosummia seurataan myyntitilauksen tai ostotilauksen rivinimikkeiden lisäksi, voit käyttää kulukoodeja tässä tarkoituksessa. Esimerkiksi rahti- ja vakuutusmaksut maksetaan ostotilauksesta, ja summat eritellaan ostotilauksessa erikseen. Tässä tapauksessa voit määrittää, kirjataanko summat kulutileille vai lisätäänkö summat nimikkeiden kustannuksiin.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Määritä myyntireskontran kulukoodit

Toimi seuraavasti, kun haluat luoda myyntireskontran kulukoodit.

1. Valitse **Myyntireskontra** &gt; **Kulujen määritys** &gt; **Kulujen koodi**.
2. Valitse **Uusi**.
3. Anna **Kulukoodi** -kentässä kulun koodi.
3. Anna kulun kuvaus **Kuvaus**-kentässä.
4. Valinnainen: Valitse **Nimikkeen arvonlisäveroryhmä** -kentässä arvonlisäveroryhmä.
5. Määritä **Kirjaus**-pikavälilehdessä, miten kulu veloitetaan ja hyvitetään automaattisesti.
6. Jos olet valinnut **kirjanpitotilin** veloitus- tai hyvitystyypiksi, määritä kirjaustyyppi **Kirjaus**-kenttiin ja määritä päätili **Tili**-kenttiin.

### <a name="example"></a>Esimerkki

Asiakas maksaa kulun. Näin ollen se lisätään myyntitilauksen loppusummaan. Määrität seuraavat kirjaustiedot:

- Lisää laskun kulu asiakkaan tilille valitsemalla **Veloitus**-osan **Tyyppi**-kentästä **Asiakas/Toimittaja**.
- Valitse **Hyvitys**-osan **Tyyppi**-kentästä **Kirjanpitotili**. Valitse sitten **Tili**-kentässä päätili laskutusmaksutuloille.

> [!NOTE]
> Jos valitun koodin debet- tai kredit-tyyppi on joko **Kirjanpitotili** tai **Tuote**, voit syöttää veloitustapahtumalle toisen valuutan.

Voit tulostaa kulujen tekstin asiakkaalle tai toimittajalle määritetyllä kielellä. Voit määrittää kulukoodin tekstin muilla kielillä valitsemalla **Käännökset**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Määritä ostoreskontran kulukoodit

Toimi seuraavasti, kun haluat luoda ostoreskontran kulukoodit.

1. Noudata seuraavia ohjeita:

    - Valitse **Myyntireskontra** &gt;**Kulut** **määritys** &gt; **Kulujen koodi**.
    - Siirry kohtaan **Hankinta** &gt; **Asetukset** &gt; **Kulut** &gt; **Kulukoodit**.

2. Valitse **Uusi**.
3. Anna **Kulukoodi** -kentässä kulun koodi.
3. Anna kulun kuvaus **Kuvaus**-kentässä.
4. Valinnainen: Valitse **Nimikkeen arvonlisäveroryhmä** -kentässä arvonlisäveroryhmä.
5. Valinnainen: Syötä **Enimmäissumma**-kentässä suurin kulujen koodille sallittu summa.

    Tämän kentän avulla vahvistetaan toimittajan laskujen kulut. Voit ottaa kulujen oikeellisuustarkistuksen käyttöön valitsemalla **Ostoreskontran parametrit** -sivun **Laskun oikeellisuustarkistus** -välilehden **Ota laskun täsmäytyksen oikeellisuustarkistus käyttöön** -valintaruudun.

    > [!IMPORTANT]
    > Tarkistaaksesi laskujen kuluja sinun on luotava myös käytäntösääntötyypin esiintymä, joka perustuu tietyn toimittajan laskukäytännön kuluihin.

6. Määritä **Kirjaus**-pikavälilehdessä, miten kulu veloitetaan ja hyvitetään automaattisesti.
7. Jos valitsit veloitustyypiksi tai hyvitystyypiksi **Kirjanpitotili**, määritä kirjaustyyppi kenttiin **Veloituskirjaus** ja **Luottokirjaus** ja määritä päätilin **Debit-tili** ja **Kredit-tili** -kentät.
8. Voit ottaa käyttöön kuluarvojen vertailun laskulle, joka sisältää vastaavat ostotilauksen otsikon tai vastaavien rivien kulut, valitsemalla **Vertaa ostotilauksen ja laskun arvoja** -valintaruudun.

### <a name="example"></a>Esimerkki

Voit kirjata kulut kuluna ostotilauksen tai toimittajan laskun kokonaissummaan. Määritä kirjaustiedot noudattamalla näitä ohjeita. 

- Lisää laskun kulu asiakkaan tilille valitsemalla **Hyvitys**-osan **Tyyppi**-kentästä **Asiakas/Toimittaja**.
- Valitse **Veloitus**-osan **Tyyppi**-kentästä **Kirjanpitotili**. Valitse sitten **Tili**-kentässä päätili laskutusmaksukuluille.

Seuraavia ohjeita noudattamalla voit määrittää kirjaustiedot niin, että yksikkökulut lisätään nimikkeen kustannuksiin.

- Lisää laskun kulu asiakkaan tilille valitsemalla **Hyvitys**-osan **Tyyppi**-kentästä **Asiakas/Toimittaja**.
- Valitse **Veloitus**-osan **Tyyppi**-kentästä **Nimike**, kun haluat lisätä kulun nimikkeen kustannukseen.

> [!NOTE]
> Voit käyttää valuuttaa, joka poikkeaa ostotilauksessa tai laskussa määritetystä valuutasta. Voit antaa eri valuutan, jos valitun kulukoodin veloitus- tai hyvitystyypiksi on määritetty **Kirjanpitotili** tai **Nimike**.

Voit tulostaa kulujen tekstin asiakkaalle tai toimittajalle määritetyllä kielellä. Voit määrittää kulukoodin tekstin muilla kielillä valitsemalla **Käännökset**.
