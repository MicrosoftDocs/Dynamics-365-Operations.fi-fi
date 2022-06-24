---
title: Sähköisen laskutuksen yleiskatsaus
description: Tässä artikkelissa on yleiskuvaus sähköisestä laskutuksesta Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 4ce5776216855fc664b9beba68036d41920ae602
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861293"
---
# <a name="electronic-invoicing-overview"></a>Sähköisen laskutuksen yleiskatsaus

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin sähköinen laskutus on lisäosa on äärimmäisen skaalautuva usean vuokraajan palvelu, joka mahdollistaa sähköisten laskujen määritettävän prosessoinnin sekä määritettävän sähköisten asiakirjojen vaihdon. Käsittely- ja integrointisäännöt ovat täysin määritettävissä, ja logiikka suoritetaan Financen ja Supply Chain Managementin ulkopuolella. Palvelu on tarkoitettu lähinnä sähköisten laskuasiakirjojen käsittelyyn yritysten ja valtionhallinnon välillä. Sen voi kuitenkin määrittää mukautettuna muita tarkoituksia varten, esimerkiksi yritysten välisiin skenaarioihin eri tyyppisille tiedostoille.

Sähköinen laskutus voi auttaa seuraavien tavoitteiden saavuttamisessa:

- Nopea ja helppo maa-/aluekohtaisten määritysten käyttöönotto
- Sähköisen laskutuksen ratkaisun vakioidut toimeenpanot
- Parannettu asiakirjahistorian jäljitettävyys
- Lyhyempi täytäntöönpanosykli
- Pienemmät kokonaiskustannukset (TCO)
- Helposti muokattavat määritykset, jotka eivät edellytä muutoksia koodiin
- Yksinkertaistettu määrityksen pakkaus
- Sisäänrakennettu vienti, tuonti ja integrointi sekä helppo laajennettavuus sähköisten laskuasiakirjojen käsittelyssä
- Samojen vienti-, tuonti-ja integrointimääritysten helppo uudelleenkäyttö eri yrityksissä

## <a name="service-availability"></a>Palvelun käytettävyys

Sähköiset laskutustoiminnot ovat tällä hetkellä käytettävissä Finance- ja Supply Chain Management -asiakkaille. Lisätietoja saat sovelluksesi käyttöoikeusehdoista.

Koska maa-/aluekohtaisia vaatimuksia koskevat toiminnot saattavat olla rajoitettuja julkaisun eri vaiheissa, kannattaa aina tarkistaa ajantasaisin dokumentaatio, joka käsittelee tuettujen maa-/aluekohtaisten ratkaisujen kattavuutta ja laajuutta.

Sähköinen laskutus otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla:

- Yhdysvallat
- Eurooppa
- Aasia

> [!NOTE]
> Sähköinen laskutus ei tue paikallisia käyttöönottoja.

## <a name="feature-highlights"></a>Toiminnon tärkeimmät ominaisuudet

- Käyttövalmis integrointi Financeen ja Supply Chain Managementiin
- Yhdenmukainen käyttökokemus kaikkien maiden tai alueiden sähköisen laskutusprosessin määrittämiseen ja seuraamiseen
- Nopeampi, helpompi ja edullisempi sähköisen laskutuksen ratkaisujen käyttöönotto uusissa maissa tai uusilla alueilla
- Palvelun määrittäminen Regulatory Configuration Servicen (RCS) ja globalisointitoimintojen määrityksen kautta
- Liiketoimintatietojen muuntaminen useisiin sähköisen laskutuksen muotoihin (XML, JavaScript Object Notation \[JSON\], TXT ja pilkuin erotetut arvot \[CSV\]) käyttämällä RCS:ssä määritettyjä määrityksiä:

    - Sähköisen raportoinnin (ER) muotoja, jotka ovat käytettävissä maille ja alueille, joissa sähköisen laskutuksen muuntamisen määritettävyys ei ole käytettävissä

- Sähköisten laskujen määritettävä lähettäminen ulkoisiin verkkopalveluihin, varmenteiden käsittely digitaalisten allekirjoitusten avulla mukaan luettuna:

    - Sisäänrakennettu, helposti laajennettava ja määritettävä integrointi lisäsisältöön useissa maissa ja alueilla

- Verkkopalveluiden vastausten käsittely, mukaan lukien määritettävä poikkeussanomien käsittely
- Sähköisten allekirjoitusten tuki (esimerkiksi XMLDSig-allekirjoitusalgoritmia käyttävät sähköiset allekirjoitukset)
- Kyky lähettää asiakirjoja sähköpostiin ja tallentaa ne SharePointiin
- Sähköisten laskujen sanomien eräkäsittely
- Konfiguroitava saapuvien tiedostojen muuntaminen ja näiden tiedostojen käsitteleminen Financessa ja Supply Chain Managementissa
- Mahdollisuus vastaanottaa saapuvia tiedostoja eri kanavista, esimerkiksi sähköpostilla tai SharePointista

## <a name="privacy-notice"></a>Tietosuojatiedot

Sähköisen laskun ottaminen käyttöön ja käyttö saattaa edellyttää, että rajoitetut tiedot lähetetään. Tietoihin sisältyy organisaation verorekisteröintitunnus. Ne välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten niissä esimääritetyssä muodoissa, jota integrointi valtion verkkopalveluihin edellyttää. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maa-/aluekohtaisten toimintodokumentaatioiden tietosuojaosista.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
