---
title: Noudon tiedot -moduuli
description: Tässä ohjeaiheessa käsitellään noutotietojen moduulia ja sen lisäämistä kassasivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9428eda880d534c700646b52310c6b8befdebaf2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353801"
---
# <a name="pickup-information-module"></a>Noudon tiedot -moduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään noutotietojen moduulia ja sen lisäämistä kassasivuille Microsoft Dynamics 365 Commercessa.

Noutotietomoduulia voidaan käyttää kassamoduulissa tilauksen noutotietojen näyttämiseen. Asiakkaat voivat tarkastella käytettävissä olevia noutopäivämääriä ja aikavälejä ja valita sitten tilauksen noutoa varten sopivan ajan. Esimerkiksi asiakas voi halutessaan noutaa tilauksen 21.3. klo 15.00 San Franciscon myymälästä.

Soveltuvien myymälöiden noutoajat on konfiguroitava Commerce-pääkonttorisovelluksessa. Lisätietoja: [Asiakasnoudon ajankohtien luominen ja päivittäminen](dev-itpro/pickup-timeslots.md).

Jos noutotietomoduuli luodaan kassasivulla, mutta valitulle noutomyymälälle ei ole määritetty aikavälejä, moduulissa näytetään tiedot, mutta käyttäjä ei voi valita aikavälejä. Aikavälit ovat valinnaisia, eikä tilauksen tekeminen edellytä niitä.

Jos useista myymälöistä noutoa varten on valittu useita nimikkeitä, noudon tiedot -moduulin avulla käyttäjä voi valita kullekin myymälälle aikavälin, jos käytettävissä on aikavälejä.

> [!NOTE]
> Aikavälien ja kassasivun noutotietomoduulin tuki on saatavana Dynamics 365 Commerce -versiossa 10.0.15 ja sitä uudemmissa versioissa.

Seuraavassa kuvassa on esimerkki aikavälin valinnasta kassasivun noutotietomoduulin kautta.

![Esimerkki noutotietomoduulista kassasivulla.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

- **Otsikko** – Anna moduuliin otsikko.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Aikavälin tietojen näyttäminen tilauksen tekemisen jälkeen

Kun tilaus on tehty, valittua aika paikkaa koskevia tietoja voi tarkastella [tilausvahvistusmoduulissa](order-confirmation-module.md) ja [tilaustiedot-moduulissa](account-management.md#order-details-page). Molemmissa moduuleissa on **Näytä aikavälin tiedot** -ominaisuus. Ennen kuin ne voivat näyttää valitun aikavälin tilausprosessin aikana, tämän ominaisuuden arvoksi on asetettava **Tosi**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Lisää kassan noutotietomoduuli sivulle

Lisätietoja noutotietomoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli](add-checkout-module.md).

Seuraavassa kuvassa on esimerkki sähköisen kaupankäynnin kassasivusta, joka sisältää aikavälit noudettaville rivinimikkeille.

![Esimerkki sähköisen kaupankäynnin kassasivusta, joka sisältää aikavälit noudettaville rivinimikkeille.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Lisäresurssit

[Asiakasnoudon ajankohtien luominen ja päivittäminen](dev-itpro/pickup-timeslots.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Tilauksen tiedot -moduuli](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]