---
title: Yleisen varastokirjanpidon tukemat yritysasiakirjat
description: Tässä aiheessa luetellaan liiketoiminta-asiakirjat, joita yleinen varastokirjanpito tukee. Se sisältää myös yksityiskohtaisen esimerkin ostotilausasiakirjoista.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 311c894d709985d0d053b0ec3a317142aa582c39
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273151"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Yleisen varastokirjanpidon tukemat yritysasiakirjat

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Kun Yleinen varastokirjanpito -lisäosa on määritetty kokonaan, voit käsitellä Microsoft Dynamics 365 Supply Chain Managementiin syötettyjä varastoon liittyviä asiakirjoja.

## <a name="supported-business-documents"></a>Tuetut liiketoiminta-asiakirjat

Yritysasiakirjoja on kahta eri tyyppiä:

- **Asiakirjat, joissa on kirjauskansio** – Näitä asiakirjoja ovat tuotteen vastaanotto, ostolasku, pakkausluettelo ja myyntilaskuasiakirjat.
- **Asiakirjat, joihin ei ole kirjauskansiota** – Näitä asiakirjoja ovat inventointi-, siirto- ja varasto-oikaisuasiakirjat.

Ostotilauksia käytetään myöhemmin tässä ohjeaiheessa prosessin havainnollistamisena.

Seuraavassa taulukossa luetellaan tiedostot, joita nykyinen versio tukee.

| Tiedostotyyppi      | Tiedosto        |
|--------------------|-----------------|
| Ostotilaus     | Tuotteen vastaanotto |
| Ostotilaus     | Lasku         |
| Myyntitilaus        | Pakkausluettelo    |
| Myyntitilaus        | Lasku         |
| Varastokirjauskansiot | Siirto        |
| Varastokirjauskansiot | Oikaisu      |
| Varastokirjauskansiot | Inventointi        |
| Varastokirjauskansiot | Tapahtumien siirto        |
| Siirtotilaus     | Lähetys        |
| Siirtotilaus     | Vastaanotto         |

> [!IMPORTANT]
> Yleinen varastokirjanpito käsittelee asynkronisesti Supply Chain Managementiin syötetyt tiedostot. Ongelmallisille asiakirjoille ei tule virhesanomia.

## <a name="example-purchase-order"></a>Esimerkki: Ostotilaus

### <a name="product-receipt"></a>Tuotteen vastaanotto

Kirjaa tuotteen vastaanotot tavalliseen tapaan. Valitse **Kaikki ostotilaukset** -sivulla ostotilaus ja avaa sitten **Tuotteen vastaanottokirjauskansio** -sivu valitsemalla toimintoruudun **Vastaanotto**-välilehdestä **Tuotteen vastaanotto**. Kullekin riville luodaan työvaihetapahtuma ja yleisen varastokirjanpidon tapahtuma. Valitse siis **Rivit**-välilehti ja avaa **Tapahtumat ja mittaukset** -sivu valitsemalla **Varasto \> Tapahtumat ja mittaukset**.

Yleinen varastokirjanpito on tapahtumiin ja mittauksiin perustuva kirjanpitojärjestelmä. **Tapahtumat ja mittaukset** -sivun mittausrivien ruudukossa näkyy mittausluettelo. Jokaisella mittauksella on dimensioiden luettelo.

Kutakin työvaihetapahtumaa varten on kahdenlaisia mittaustyyppejä:

- **Työvaiheiden mittaukset** – Nämä mittaukset kuvaavat yleisesti liiketoiminta-asiakirjoja. Yksi mittaus on asiakirjassa käytettävä tuotemäärä asiakirjan mittayksikköä käyttäen. Siellä on myös varastoarvoon vaikuttavia mittauksia, kuten laajennettu hinta, alennus, alennusprosentti ja rivikulu.
- **Resurssilaskennan mittaukset** – Nämä mittaukset ovat varastorekisterin näkökulmasta. Ne kuvaavat asiakirjan vaikutusta varastoon varaston mittayksikköinä. Jos varastorekisteröintejä on useita, resurssilaskennan mittauksia on useita rivejä.

Dimensiot on järjestetty seuraavasti:

- **Kaksinaisuus** – Kaksinaisuus kuvaa toimijoita, jotka osallistuvat taloustapahtumiin. Ulkoisia liikeasiakirjoja varten dimensiot kuvaavat oikeushenkilöä, johon asiakirja syötetään, kun taas kaksoisdimensiot kuvaavat toimittajaa, asiakasta ja niin edelleen. Sisäisten liiketoiminta-asiakirjojen (esimerkiksi siirtotilausten) kaksoisdimensiot kuvaavat vastaavaa varastoa.
- **Dimensiotyyppi** – Dimensiotyypit luokittelevat dimensiot.
- **Dimensio** – dimension nimi.
- **Dimension arvo** – dimension arvo.

### <a name="global-inventory-accounting-event"></a>Yleinen varastokirjanpitotapahtuma

Yleinen varastokirjanpito vie toiminnalliset tapahtumat ja mittaukset syötteenä. Sen jälkeen se tekee kullekin liittyvälle tapahtumalle kirjanpidon liittyvän valuutan ja käytännön perusteella. Voit valita **Yleisen varastokirjanpidon tapahtumat ja mittaukset** nähdäksesi yleisen varastokirjanpitotapahtuman. Yleinen varastokirjanpitotapahtuma noudattaa samoja menetelmiä kuin toimintotapahtumat, mutta siinä käytetään erilaisia mittauksia. Mittatyyppejä on kolme: tuotteen kustannusmäärä, tuotekustannus ja varianssi.

Alareskontran tilejä käytetään mittausten lisäluokituksissa. Kirjanpitoja voi olla useita. Nämä kirjanpitotapahtumat linkitetään yritykseen, johon asiakirja syötetään. Voit tarkastella kunkin kirjanpidon tapahtumia ja mittauksia muuttamalla **Kirjanpito**-kentän arvoa.

### <a name="cost-element"></a>Kustannustaso

Kirjanpitoon liitetyn kustannuselementin käytännön mukaan järjestelmä liittää kustannuselementin jokaiseen kirjattuun työvaihetapahtuman mittaukseen, joka vaikuttaa varastokustannuksiin. Mittauksiin kuuluvat laajennettu hinta, alennus, alennusprosentti ja rivikulu.

### <a name="measurement-line-details"></a>Mittarivin tiedot

**Yhteenveto**-välilehdessä näkyvät liitettyjen käytäntöjen tiedot. Kustannuskohteen dimensiot näyttävät kustannuskohteen kustannuskohteen käytännön perusteella. Tietyt tunnusdimensiot näyttävät eränumeron, jos kustannusvirtaoletuksena on *Tietty - erä*.

### <a name="purchase-invoice"></a>Ostolasku

Kirjaa lasku tavalliseen tapaan. Avaa sitten laskukirjauskansio valitsemalla toimintoruudun **Lasku**-välilehden **Kirjauskansiot**-ryhmästä **Lasku**. Kullekin riville luodaan työvaihetapahtuma ja yleisen varastokirjanpidon tapahtuma. Valitse siis **Rivit**-välilehti ja avaa **Tapahtumat ja mittaukset** -sivu valitsemalla **Varasto \> Tapahtumat ja mittaukset**. **Tapahtumat ja mittaukset** -sivulla näkyy sama mittatyyppi. Koska sivulla näkyy eri mittarin rooli ja mittarin määre, vaikutus toimijaan (oikeushenkilö) poikkeaa toisistaan.

Valitse **Yleisen varastokirjanpidon tapahtumat ja mittaukset** nähdäksesi yleisen varastokirjanpitotapahtuman. Varastomäärä ja -kustannukset virtaavat nyt *Vastaanotetut, ei-laskutetut tavarat* -alareskontratililtä ja *Ostettujen tavaroiden kustannukset* -alareskontratilille.
