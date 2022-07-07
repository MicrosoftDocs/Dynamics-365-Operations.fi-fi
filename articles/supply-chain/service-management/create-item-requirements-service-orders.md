---
title: Nimiketarpeiden luominen huoltotilauksiin
description: Tässä artikkelissa käsitellään huoltotilausten nimiketarpeiden luontia.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f21cda0abb334432d22cc7e0ccfdab724253d91e
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016946"
---
# <a name="create-item-requirements-for-service-orders"></a>Nimiketarpeiden luominen huoltotilauksiin

[!include [banner](../includes/banner.md)]

Voit luoda huoltotilauksen seurataksesi ja hallitaksesi palveluita, joita tarjoat asiakkaillesi. Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia. Nimiketarve voidaan kuluttaa suoraan varastosta tai se voi käynnistää nimikkeen tuotantotilauksen.

Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.

Palvelutilausten nimikevaatimukset käsitellään projektin kautta. Jos huoltotilaukselle luodaan nimiketarve, projektille pitää olla määritettynä huoltotilaus. Kun olet luonut huoltotilaukselle nimiketarpeen, voit tarkastella sitä valitun projektin **Projektit**-lomakkeessa.

## <a name="create-an-item-requirement-for-a-service-order"></a>Luo nimiketarve huoltotilaukselle

1. Siirry kohtaan **Palveluiden hallinta** \> **Huoltotilaukset** \> **Huoltotilaukset**.
1. Valitse huoltotilaus, jolle haluat luoda nimiketarpeen.
1. Valitse **toimintoruudun** **Lähetys**-välilehdessä **Nimiketarve**.
1. Kirjoita **Nimiketarve**-lomakkeeseen tarvittavat nimikkeen tiedot. Lisätietoja kentistä on kohdassa [Nimiketarpeet (lomake)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Luo nimiketarve huoltosopimukselle

1. Siirry kohtaan **Palvelujen hallinta** \> **Huoltosopimukset** \> **Huoltosopimukset**.
1. Valitse huoltosopimus, jolle haluat luoda nimiketarpeen.
1. Luo uusi rivi valitsemalla **Tunnit**-pikavälilehdessä **Rivit**.
1. Valitse **Tapahtumalaji**-kentästä **Nimike**.
1. Valitse **Nimikeasetukset**-kentässä **Nimiketarve**.
1. Valitse **Nimikenumero**-kentästä nimike, joka on tarpeen huoltosopimuksessa.
1. **Rivin tiedot** -pikavälilehdessä **Nimikedimensiot**-välilehdellä **Toimipaikka**-kentässä valitse nimikkeen varastotoimipaikkaa.
1. Luo huoltotilaus sopimusriviltä valitsemalla **Rivit**-pikavälilehdessä **Luo huoltotilauksia** ja antamalla sitten tarvittavat tiedot **Luo huoltotilauksia** -lomakkeessa.

## <a name="see-also"></a>Lisätietoja

[Automaattisesti luodut huoltotilaukset](create-service-orders-automatically.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
