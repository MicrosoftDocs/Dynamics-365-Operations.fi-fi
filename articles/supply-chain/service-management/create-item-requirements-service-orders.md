---
title: Nimiketarpeiden luominen huoltotilauksiin
description: Tässä aiheessa käsitellään huoltotilausten nimiketarpeiden luontia.
author: kamaybac
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75a05147883f1592b3a09e02e238661f6c20cf27
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575288"
---
# <a name="create-item-requirements-for-service-orders"></a>Nimiketarpeiden luominen huoltotilauksiin

[!include [banner](../includes/banner.md)]

Voit luoda huoltotilauksen seurataksesi ja hallitaksesi palveluita, joita tarjoat asiakkaillesi. Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia. Nimiketarve voidaan kuluttaa suoraan varastosta tai se voi käynnistää nimikkeen tuotantotilauksen.

Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.

Palvelutilausten nimikevaatimukset käsitellään projektin kautta. Jos huoltotilaukselle luodaan nimiketarve, projektille pitää olla määritettynä huoltotilaus. Kun olet luonut huoltotilaukselle nimiketarpeen, voit tarkastella sitä valitun projektin **Projektit**-lomakkeessa.

## <a name="create-an-item-requirement-for-a-service-order"></a>Luo nimiketarve huoltotilaukselle

1. Avaa **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.
1. Valitse huoltotilaus, jolle haluat luoda nimiketarpeen.
1. Valitse **toimintoruudun** **Lähetys**-välilehdessä **Nimiketarve**.
1. Kirjoita **Nimiketarve**-lomakkeeseen tarvittavat nimikkeen tiedot. Lisätietoja kentistä on kohdassa [Nimiketarpeet (lomake)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Luo nimiketarve huoltosopimukselle

1. Avaa **Huoltohallinta** \> **Yleinen** \> **Huoltosopimukset** \> **Huoltosopimukset**.
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
