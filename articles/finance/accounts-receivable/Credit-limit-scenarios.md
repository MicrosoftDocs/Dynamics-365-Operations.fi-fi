---
title: Luottorajaskenaariot
description: Tässä artikkelissa käsitellään asiakkaan luottorajan tarkistamista, kun asiakas kuuluu asiakasluottorajaryhmään.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130254"
---
# <a name="credit-limit-scenarios"></a>Luottorajaskenaariot

Luottoraja vodaan määrittää asiakkaille luotonhallinnassa asiakastasolla. Kukin asiakas määritetään *asiakasluottorajaryhmään*, ja kullakin ryhmällä on luottoraja. Niinpä luottoraja voidaan määrittää asiakkaille myös ryhmätasolla. Kaikilla samaan asiakasluottoryhmään määritetyillä asiakkailla on sama luottoraja.

Ryhmän luottorajat tarkistetaan yleensä ennen yksittäisiä luottorajoja. Yksittäin luottoraja ei aina ohita ryhmän luottorajaa.

Tässä artikkelissa käsitellään viittä skenaariota, jotka liittyvät asiakkaan luottoryhmiin ja yksittäisiin luottorajoihin.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Asiakasryhmän luottoraja on suurempi kuin yksittäinen luottoraja

Asiakkaan yksittäinen luottoraja on esimerkiksi 10 000 $. Asiakas määritetään asiakasluottoryhmään ja ryhmän luottoraja on 15 000 $. Tässä tapauksessa asiakkaan todellinen luottoraja on 10 000 $, koska kyseinen summa on pienempi kuin ryhmän raja. Estosäännöt tarkistavat ensin ryhmän rajan. Sen jälkeen tarkistetaan yksittäinen raja. Jos myyntitilaus on yli 10 000 $, se estetään.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Yksittäinen luottoraja on suurempi kuin asiakasryhmän luottoraja

Asiakkaan yksittäinen luottoraja on esimerkiksi 20 000 $. Asiakas määritetään asiakasluottoryhmään ja ryhmän luottoraja on 15 000 $. Tässä tapauksessa asiakkaan todellinen luottoraja on 15 000 $, koska estosäännöt tarkistavat aina ryhmän rajan ensin. Jos myyntitilaus on yli 15 000 $, se estetään.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Yksittäinen luottoraja on 0,00 ja Pakollinen luottoraja -asetuksena on Kyllä

Jos asiakkaan yksittäiseksi luottorajaksi on määritetty **0,00** ja **Pakollinen luottoraja** -asetuksena on **Kyllä**, asiakkaan todellinen luottoraja on 0,00, vaikka asiakas olisi määritetty asiakasluottoryhmään. Tällä tavoin asiakas voi olla ryhmän jäsen, mutta kaikki tilaukset siirtyvät luotonhallintaan.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Yksittäinen luottoraja on 0,00 ja Rajoittamaton luottoraja -asetuksena on Kyllä

Jos asiakkaan yksittäiseksi luottorajaksi on määritetty **0,00** mutta **Rajoittamaton luottoraja** -asetuksena on **Kyllä**, asiakkaalla on käytössä rajoittamaton luotto, vaikka tämä olisi määritetty asiakasluottoryhmään.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Yksittäinen luottoraja on 0,00 ja asiakas on osa asiakasluottoryhmää

Asiakkaan yksittäiseksi luottorajaksi on esimerkiksi määritetty **0,00**, **Rajoittamaton luottoraja** -asetuksena on **EI** ja **Pakollinen luottoraja** -asetuksena on **Ei**. Asiakas määritetään asiakasluottoryhmään ja ryhmän luottoraja on 15 000 $. Tässä tapauksessa asiakkaan todellinen tuottoraja on ryhmän raja 15 000 $. Tämän vuoksi kyseisen rajan ylittävät myyntitilaukset estetään. Tällä tavoin luottorajaa voidaan hallita asiakasluottoryhmän tasolla eikä yksittäisen asiakkaan tasolla. Kaikilla samaan ryhmään määritetyillä asiakkailla on sama luottoraja.
