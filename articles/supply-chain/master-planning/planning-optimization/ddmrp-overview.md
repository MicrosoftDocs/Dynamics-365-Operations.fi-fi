---
title: Kysyntäperustainen materiaalitarvesuunnittelu (DDMRP)
description: Tässä artikkelissa on tietoja kysyntäperustainen materiaalitarvesuunnittelusta (DDMRP). Se on menetelmä, joka perustuu kysynnän ja tarjonnan erottamiseen.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cf5ca3996a882111b840e3acb5e2a4f3f26ec4b7
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740847"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Kysyntäperustainen materiaalitarvesuunnittelu (DDMRP)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Yritykset ovat käyttäneet vuosien ajan tarvelaskentaa (MRP:tä) tuotteen valmistamiseen tarvittavien materiaalien ja komponenttien laskentajärjestelmänä. Toimitusketjut ovat kuitenkin nykyisin erilaisia. Osien läpimenoajat ovat pidentyneet, sillä niiden alkuperä on enenevässä määrin ulkomailla. Monet yritykset ovatkin ilmoittaneet varaston loppumisesta tai liian suurista varastoista, sillä varaston kokoa ei osata arvioida oikein. Myös markkinoilla on vaihtelua (jota ennakoidaan joskus virheellisesti), minkä lisäksi asiakkaat edellyttävät, että tuotteiden läpimenoaika on lyhyt. Tämän vuoksi toimitusketjuissa esiintyy puutteita kaikkialla maailmassa. Tämän lisäksi MRP-työkalut antavat usein suunnittelijoille valtavasti tehtäviä toimintoja. Se taas hankaloittaa keskittymistä oleelliseen. Usein monet näistä ongelmista voidaan ratkaista siirtymällä kysyntäperustainen materiaalitarvesuunnitteluun (DDMRP:hen).

DDMRP on kysynnän ja tarjonnan erotteluun perustuva menetelmä. Tämä erottelu tehdään määrittämällä erotuspistenimikkeitä. Kyseisille nimikkeille ylläpidetään puskureita, joilla varmistetaan, että varaston koko pysyy sopivana. Kysynnän ja tarjonnan erottaminen auttaa estämään piiskavaikutuksen, sillä vaihtuvuus ei pääse etenemään toimitusketjussa. (*Piiskavaikutuksella* tarkoitetaan tilannetta, jossa pienet vähittäismyyntitason kysynnän vaihtelut aiheuttavat vähitellen suurenevaa kysynnän vaihtelua tukkumyynti-, jakelu-, valmistaja- ja raaka-ainetoimittajatasoilla.) Kunkin puskurin tarkoituksena on kattaa osan keskimääräinen käyttö, ja se voidaan oikaista kattamaan myös kysyntäpiikit.

DDMRP:n on todistettu olevan arvokas suunnittelumenetelmä muuttuvissa ympäristöissä, joissa asiakkaan toleranssiajat ovat lyhyempiä kuin kumulatiiviset läpimenoajat.

## <a name="the-five-components-of-ddmrp"></a>DDMRP:n viisi komponenttia

DDMRP:ssä on viisi peräkkäistä komponenttia (vaihetta). Kolme ensimmäistä komponenttia käytännössä määrittävät kysyntäperustaisen materiaalitarvesuunnittelumallin ensimmäiset ja kehittyvät määritykset. Kaksi viimeistä komponenttia määrittävät menetelmän päivittäisen toiminnan.

1. **[Varaston strateginen asemointi](ddmrp-inventory-positioning.md)** – Määrittää toimitusketjuverkoston erotuspisteet. Erotuspisteet ovat tiettyjä toimitusketjun pisteitä, joihin lisätään seurattava ja täydennettävä varastopuskuri.
2. **[Puskuriprofiilit ja -tasot](ddmrp-buffer-profile-and-levels.md)** – kullekin erotuspisteelle määritetään puskurin koko (vähimmäismäärä, enimmäismäärä ja uudelleentilauspiste) ja uudelleentilausmäärä.
3. **[Puskurin dynaamiset oikaisut](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – puskuritason oikaistaan erilaisten toimintoparametrien tai suunniteltujen tulevien tapahtumien perusteella.
4. **[Kysyntäperustainen suunnittelu](ddmrp-planning.md)** – Toimitustilausten luonti tarpeen mukaan. Nämä toimitustilaukset sisältävät valmistustilaukset, ostotilaukset ja varastosiirtotilaukset.
5. **[Visualisoinnin ja yhteistyön toteutus](ddmrp-visual-and-collaborative-execution.md)** – visualisointeja käytetään apuna toimitustilausten suorittamisessa.

DDMRP:tä käyttävät yleensä valmistajat, joilla monitasoisia tuoterakenteita. Sitä voidaan kuitenkin hyödyntää myös jakelu- ja vähittäismyyntiverkostoissa.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP Dynamics 365 Supply Chain Managementissa

DDMRP sisältyy Microsoft Dynamics 365 Supply Chain Managementiin, eikä sen käyttö aiheuta lisäkäyttöoikeusmaksuja. Supply Chain Managementin DDMRP-toiminto on lisätty nykyiseen **Pääsuunnittelu**-moduuliin. Sen käyttöä varten tarvitaan kuitenkin Suunnittelu optimointi -apuohjelma.

DDMRP on integroitu Supply Chain Managementin nykyisiin suunnittelumäärityksiin, ja yhdessä niiden kanssa käytettynä sen avulla saadaan liiketoimintaan sopivat suunnittelumääritykset. Sitä hallitaan uudella kattavuuskoodilla, joka eroaa täysin esimerkiksi kauden, suurimman ja pienimmän tai tarpeen käytöstä. Se ei ole uusi moduuli, eikä se korvaa nykyistä suunnittelutoimintoa. Sen avulla saadaan kuitenkin käyttöön enemmän toimintoja.
