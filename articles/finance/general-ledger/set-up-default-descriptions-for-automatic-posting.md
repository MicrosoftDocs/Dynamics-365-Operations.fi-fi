---
title: Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille
description: Tämä artikkeli kuvaa, kuinka voit määrittää oletustekstin, jota käytetään kuvaamaan niitä kirjanpitomerkintöjä, jotka kirjataan kirjanpitoon automaattisesti. Voit määrittää kuvaavan oletustekstin käyttämällä vapaamuotoista tekstiä tai valitsemalla kiinteitä muuttujia.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71982a7d5b1bb08d3e238646ea0b15f17260bdcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904496"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Aseta oletusarvoiset kuvaukset automaattiselle tiliöinnille

[!include [banner](../includes/banner.md)]

Tämä artikkeli kuvaa, kuinka voit määrittää oletustekstin, jota käytetään kuvaamaan niitä kirjanpitomerkintöjä, jotka kirjataan kirjanpitoon automaattisesti. Voit määrittää kuvaavan oletustekstin käyttämällä vapaamuotoista tekstiä tai valitsemalla kiinteitä muuttujia.

> [!NOTE]
> Eräiden maiden tai alueiden tapahtumatyyppien kohdalle voit myös lisätä kenttien tekstejä, jotka liittyvät kyseisiin tapahtumatyyppeihin. Luettelo tapahtumatyypeistä, maista ja alueista esitetään myöhemmin tässä artikkelissa kohdassa [Valinnainen: Lisää muuta tekstiä oletuskuvauksiin](#optional-add-other-text-to-default-descriptions).

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

Kun olet suorittanut aiemmin tässä artikkelissa kuvatun osan [Oletuskuvausten määrittäminen](#set-up-default-descriptions) vaiheet, lisää tekstiä oletuskuvauksiin tekemällä seuraavat toimet.

1. Valitse **Parametrit**-pikavälilehdessä **Lisää**.
2. Valitse **Viitetaulukko**-kentästä tietokantataulukko, josta parametritietoja lisätään kuvaukseen.
3. Valitse **Viitekenttä**-kentästä kenttä, josta parametritietoja lisätään kuvaukseen.
4. Voit lisätä muita parametrejä tekemällä kohtien 1–3 toimet uudelleen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
