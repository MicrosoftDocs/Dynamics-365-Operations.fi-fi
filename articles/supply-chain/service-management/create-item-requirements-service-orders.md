---
title: Nimiketarpeiden luominen huoltotilauksiin
description: Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia.
author: ShylaThompson
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
ms.openlocfilehash: 650d02d2160757d9629e4deb1e9217c85e9d01df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831623"
---
# <a name="create-item-requirements-for-service-orders"></a>Nimiketarpeiden luominen huoltotilauksiin 

[!include [banner](../includes/banner.md)]


Voit luoda huoltotilauksen seurataksesi ja hallitaksesi palveluita, joita tarjoat asiakkaillesi. Jos sinun pitää varata tiettyjä nimiketarpeita huoltotilaukselle, voit luoda sille varastonimikevaatimuksia. Nimiketarve voidaan kuluttaa suoraan varastosta tai se voi käynnistää nimikkeen tuotantotilauksen.

Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.

Palvelutilausten nimikevaatimukset käsitellään projektin kautta. Jos huoltotilaukselle luodaan nimiketarve, projektille pitää olla määritettynä huoltotilaus. Kun olet luonut huoltotilaukselle nimiketarpeen, voit tarkastella sitä valitun projektin **Projektit**-lomakkeessa.

## <a name="create-an-item-requirement-for-a-service-order"></a>Luo nimiketarve huoltotilaukselle

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  Valitse huoltotilaus, jolle haluat luoda nimiketarpeen.

3.  Napsauta **toimintoruudun** **Lähetys**-välilehdellä **Nimiketarve**.

4.  Kirjoita **Nimiketarve**-lomakkeeseen tarvittavat nimikkeen tiedot. Lisätietoja kentistä on kohdassa [Nimiketarpeet (lomake)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Luo nimiketarve huoltosopimukselle

1.  Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.

2.  Valitse huoltosopimus, jolle haluat luoda nimiketarpeen.

3.  Luo uusi rivi napsauttamalla **Rivit**-pikavälilehdellä **Lisää**.

4.  Valitse **Tapahtumalaji**-kentästä **Nimike**.

5.  Valitse **Nimikeasetukset**-kentässä **Nimiketarve**.

6.  Valitse **Nimikenumero**-kentästä nimike, joka on tarpeen huoltosopimuksessa.

7.  **Rivin tiedot** -pikavälilehdessä **Nimikedimensiot**-välilehdellä **Toimipaikka**-kentässä valitse nimikkeen varastotoimipaikkaa.

8.  Luodaksesi huoltotilauksen sopimusriviltä, mene **Rivit**-pikavälilehdelle, napsauta **Luo huoltotilauksia**, ja syötä sitten tarvittava tieto **Luo huoltotilauksia** -lomakkeella. 


## <a name="see-also"></a>Lisätietoja

[Automaattisesti luodut huoltotilaukset](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]