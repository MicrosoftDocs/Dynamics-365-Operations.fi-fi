---
title: Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille
description: Tämä ohjeaihe kuvaa, kuinka voit määrittää oletustekstin, jota käytetään kuvaamaan niitä kirjanpitomerkintöjä, jotka kirjataan kirjanpitoon automaattisesti. Voit määrittää kuvaavan oletustekstin käyttämällä vapaamuotoista tekstiä tai valitsemalla kiinteitä muuttujia.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442600"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe kuvaa, kuinka voit määrittää oletustekstin, jota käytetään kuvaamaan niitä kirjanpitomerkintöjä, jotka kirjataan kirjanpitoon automaattisesti. Voit määrittää kuvaavan oletustekstin käyttämällä vapaamuotoista tekstiä tai valitsemalla kiinteitä muuttujia.

> [!NOTE]
> Eräiden maiden tai alueiden tapahtumatyyppien kohdalle voit myös lisätä Microsoft Dynamics AX -tietokannan kenttien tekstejä, jotka liittyvät kyseisiin tapahtumatyyppeihin. Luettelo tapahtumatyypeistä, maista ja alueista esitetään myöhemmin tässä aiheessa kohdassa [Valinnainen: Lisää muuta tekstiä oletuskuvauksiin](#optional-add-other-text-to-default-descriptions).

## <a name="set-up-default-descriptions"></a>Oletuskuvausten määrittäminen

1. Siirty kohtaan **Organisaation hallinta** \> **Asetukset** \> **Oletuskuvaukset**
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Kuvaus**-kentästä tapahtumatyyppi, jolle haluat luoda oletuskuvauksen.
4. Valitse **Kieli**-kentässä kieli, jota tämä kuvaus koskee.
5. Kirjoita **Teksti**-kenttään oletuskuvaus. Voit kirjoittaa tekstiä kenttään, tai voit käyttää yhtä tai useita seuraavista vapaan tekstin muuttujista:

    - **%1** – Lisää tapahtumapäivä.
    - **%2** – Lisää tunniste, joka vastaa kirjanpitoon kirjattavan asiakirjan tyyppiä. Esimerkiksi laskuihin liittyviin tapahtumatyyppeihin **%2**-muuttuja lisää laskunumeron.
    - **%3** – Lisää tunniste, joka liittyy kirjanpitoon kirjattavan asiakirjan tyyppiin. Esimerkiksi laskuihin liittyviin tapahtumatyyppeihin **%3**-muuttuja lisää asiakkaan tilinumeron.

## <a name="optional-add-other-text-to-default-descriptions"></a>Valinnainen: Lisää muuta tekstä oletuskuvauksiin

Joissakin tapahtumatyypeissä joissakin maissa tai joillakin alueilla oletuskuvaukset voivat sisältää tekstiä, joka perustuu kyseisten tapahtumatyyppien tietojen kenttiin. Seuraavassa luettelossa näkyvät tapahtumatyypit ja maat tai alueet, joissa tämä vaihtoehto on käytettävissä.

**Tapahtumatyypit**

Voit lisätä tekstiä oletuskuvauksiin tapahtumatyypeille, jotka liittyvät seuraavat asiakirjamalleja:

- Myyntilaskut
- Asiakkaan hyvityslaskut
- Asiakkaan käteismaksut
- Toimittajan maksut
- Myyntitilaukset
- Ostotilaukset
- Varastokirjauskansiot
- Pääsuunnittelu
- Käyttöomaisuuserät

**Maat ja alueet**

Tämä vaihtoehto on käytettävissä seuraavissa maissa ja seuraavilla alueilla:

- Brasilia
- Kiina
- Tšekin tasavalta
- Itä-Eurooppa
- Unkari
- Intia
- Japani
- Liettua
- Latvia
- Puola
- Venäjä

### <a name="add-text-to-default-descriptions"></a>Lisää tekstiä oletuskuvauksiin

Kun olet suorittanut aiemmin tässä ohjeaiheessa kuvatun kohdan [Oletuskuvausten määrittäminen](#set-up-default-descriptions) vaiheet, lisää tekstiä oletuskuvauksiin tekemällä seuraavat toimet.

1. Valitse **Parametrit**-pikavälilehdessä **Lisää**.
2. Valitse **Viitetaulukko**-kentästä tietokantataulukko, josta parametritietoja lisätään kuvaukseen.
3. Valitse **Viitekenttä**-kentästä kenttä, josta parametritietoja lisätään kuvaukseen.
4. Voit lisätä muita parametrejä tekemällä kohtien 1–3 toimet uudelleen.
