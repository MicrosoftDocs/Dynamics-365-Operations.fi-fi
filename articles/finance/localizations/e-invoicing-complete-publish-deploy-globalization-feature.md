---
title: Globalisaatio-ominaisuuden valmiiksi saattaminen, julkaiseminen ja käyttöönottaminen
description: Tässä artikkelissa on tietoja globalisaatio-ominaisuuksien elinkaaresta.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 11378991a24e1a5f5e213d64f0f414db2e5c2573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279897"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Globalisaatio-ominaisuuden suorittaminen, julkaiseminen ja käyttöönottaminen

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Sähköisen laskutuksen ominaisuuden versiot

Sähköisen laskutuksen ominaisuuksilla on versiot. Kun uusi versio luodaan, versionumero kasvaa automaattisesti.

Sähköiset laskutusominaisuusversiot seuraavat elinkaarta, jossa voi olla kolme tilaa:

- **Luonnos** – Kun toimintoversio on tässä tilassa, voit muokata sen konfigurointimääritteitä ja sen artefakteja (esimerkiksi tiedostomuodon konfiguraatioita).
- **Valmis** – Tämä tila ilmaisee, että olet lopettanut toimintoversion muokkaamisen etkä aio tehdä siihen enää päivityksiä. Kun toimintoversiolla on tämä tila, et voi enää muokata toimintoversiota tai sen komponentteja.
- **Julkaistu** – Tämä tila ilmaisee, että toimintoversio on julkaistu organisaatioosi liittyvässä yleisessä tietovarastossa. Kun toimintoversiolla on tämä tila, et voi enää muokata toimintoversiota tai sen komponentteja.

Voit määrittää **voimaantulopäivän** uudelle sähköisen laskutusominaisuuden versiolle. Näin voidaan määrittää oletusversio, jota voidaan käyttää tai joka voidaan korvata, kun ominaisuus otetaan käyttöön palveluympäristössä.

Voit muuttaa sähköisen laskutusominaisuuden version tilaa noudattamalla seuraavia ohjeita.

1. Kirjaudu sisään Regulatory Configuration Service (RCS) -tilillesi.
2. Valitse **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Sähköisen laskutuksen toiminnot**-sivun vasemmassa reunassa sähköisen laskutuksen toiminto.
4. Valitse versio sivun oikeanpuoleinen **Versiot**-välilehdestä.
5. Valitse **Muuta tila** ja valitse sitten **Valmis** (jos nykyinen tila on **Luonnos**) tai **Julkaistu** (jos nykyinen tila on **Valmis**).
6. Valitse sanomaikkunassa **Kyllä** vahvistaaksesi pyynnön.

Manuaalinen muutos **Valmis**-tilasta **Julkaistu**-tilaan on valinnainen. Sähköisen laskutuksen toimintoversiot päivitetään automaattisesti **Julkaistu**-tilaan, kun ne otetaan käyttöön palveluympäristössä.

Voit seurata tilaa **Toimintoversion tila** -sarakkeessa **Versiot**-välilehdessä.

## <a name="deploy-feature-versions"></a>Toimintoversioiden käyttöönotto

RCS:ssä käytetään **Ota käyttöön** -komentoa sähköisen laskutusominaisuuden version julkaisemiseen kohdepalveluympäristössä tai liitetyssä sovelluksessa.

1. Valitse **Sähköisen laskutuksen toiminnot**-sivun vasemmassa reunassa sähköisen laskutuksen toiminto.
2. Valitse sivun oikeanpuoleisesta **Versiot**-välilehdestä sähköinen laskutusominaisuusversio, jonka haluat ottaa käyttöön palveluympäristössä tai liitetyssä sovelluksessa. Valitun version tilan täytyy olla **Valmis** tai **Julkaistu**.
3. Valitse **Ota käyttöön** ja määritä käyttöönoton kohde valitsemalla yksi tai molemmat seuraavista vaihtoehdoista:

    - **Liitetty sovellus** – Sovelluksen asetusten konfiguraatio on kirjoitettu Microsoft Dynamics 365 Financeen tai Dynamics 365 Supply Chain Managementin esiintymään, joka oli aiemmin liitetty siihen.
    - **Palveluympäristö** – Sähköisen laskutuksen ominaisuusversio otetaan käyttöön palveluympäristössä. Sähköinen laskutus on tämän jälkeen valmis vastaanottamaan ja käsittelemään sähköisiä asiakirjoja, jotka Finance tai Supply Chain Management lähettää.

> [!NOTE]
> Tavallisesti muutat sen sähköisen raportoinnin (ER) ominaisuuden parametreja, joka on otettava käyttöön palveluympäristössä. Liitetyn sovelluksen muutokset ovat harvinaisia. Ota uudet versiot käyttöön liitetyssä sovelluksessa vain, kun muutat sovelluksen vastaavia parametreja.

Jos haluat määrittää, onko tietty sähköisen laskutusominaisuuden versio käytössä tietyssä ympäristössä, tarkista **Ympäristöt**-välilehden tiedot.

## <a name="remove-feature-versions"></a>Toimintoversioiden poistaminen

RCS:ssä käytetään **Peruuta** -komentoa tietyn sähköisen laskutusominaisuuden version poistamiseen palveluympäristöstä, jos se oli siellä käytössä.

> [!IMPORTANT]
> **Peruuta**-painike toimii vain palveluympäristöissä. Se ei poista mitään nykyisen sähköisen laskutusominaisuuden yhdistetystä sovelluksesta.

## <a name="rebase-electronic-invoicing-features"></a>Sähköisten laskutuksenominaisuuksien pohjustaminen

Kun sähköinen laskutusominaisuus johdetaan toisesta ominaisuudesta, **Pohjusta**-komennon avulla voit päivittää johdettuun toimintoon muutokset, jotka on tehty alkuperäisessä (ylätason) ominaisuudessa.

Voit pohjustaa luomasi ominaisuuden johdetun version noudattamalla seuraavia ohjeita.

1. Hanki ominaisuuden viimeisin versio tuomalla se yleisestä tietovarastosta. Lisätietoja on kohdassa [Ominaisuuden tuonti yleisestä tietovarastosta](e-invoicing-import-feature-global-repository.md).
2. Valitse ominaisuuksien luettelosta uudelleenperustoiminto.
3. Luo luonnosversio valitsemalla **Versiot**-välilehdestä **Uusi**.
4. Valitse **Pohjusta**.
5. Valitse **Pohjusta**-valintaikkunassa se toiminnon versio, johon haluat pohjustaa uudelleen.
6. Valitse **OK**.
7. Tarkista ominaisuuden komponentit ja tee tarvittavat muutokset.
8. Viimeistele pohjustettu toiminto valitsemalla **Muuta tilaa**. Kun pohjustus on saatu valmiiksi, voit suorittaa lisätoimenpiteitä.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Sähköisen laskutuksen ominaisuuksien tietyn version hankkiminen

Kun luot uuden version sähköisestä laskutusominaisuudesta, järjestelmä luo kopion uusimmasta ominaisuuden versiosta. Jos haluat käyttää ominaisuuden aiempaa versiota uuden version pohjana, valitse versio ja valitse sitten **Hae tämä versio -komento**. Luodaan ominaisuuden uusi luonnosversio, joka on kopio valitusta versiosta.
