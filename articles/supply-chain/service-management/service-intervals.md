---
title: Huoltovälit
description: Huoltoväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5766d8ce1fa382f3f014e160d311b2dfab2bf774
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216272"
---
# <a name="service-intervals"></a>Huoltovälit

[!include [banner](../includes/banner.md)]

Huoltosopimusväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan automaattisesti.

Kun luot huoltotilauksia automaattisesti, huoltotilausrivit luodaan huoltosopimusriville määrittämäsi aikavälin mukaisesti sopimusrivin aloituspäivämäärästä lähtien.

Jos **Huoltosopimus**-sivun **Väli**-kenttä on tyhjä, rivi on vain kerran tapahtuva tapahtuma eikä sitä käytetä toistuvien huoltotilausten luomiseen.

## <a name="example"></a>Esimerkki

Tämä esimerkki osoittaa, miten huoltoväli vaikuttaa huoltotilauksen huoltosopimuksen riveihin ja huoltotilauksen riveihin.

### <a name="create-a-service-agreement"></a>Huoltosopimuksen luominen

Luo ensiksi huoltosopimus ja valitse **Yhdistä huoltotilaukset** -asetukseksi **Huoltosopimuksen mukaan**.

1. Valitse **Huoltosopimukset**
2. Luo uusi huoltosopimus valitsemalla **toimintoruudun** **Huoltosopimus**-välilehden **Uusi**-ryhmässä **Huoltosopimus**.
3. Kirjoita kuvaus, valitse projekti **Projektitunnus**-kentässä anna päivämäärä **Alkamispäivä**-kenttä.
4. Valitse **Yhdistä huoltotilaukset** -kentässä **Huoltosopimuksen mukaan**.

Nyt olet luonut seuraavan huoltosopimuksen:

| Project      | Aloituspäivämäärä                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Oma projekti | Projektille määritetty päivämäärä. Tässä esimerkissä käytetään kuluvaa päivämäärää. |

### <a name="create-a-service-agreement-line"></a>Huoltosopimusrivin luominen

Seuraavaksi luot huoltosopimusrivin, jonka tapahtumalajina on **Tunti**.

Esimerkin tämän osan viimeistely edellyttää, että luot 10 päivän huoltovälin **Huoltovälit**-sivulla. 

1. Valitse juuri luomasi huoltosopimus. 
2. Luo **Huoltosopimukset**-sivun alaruutuun uusi rivi valitsemalla **Rivit**-pikavälilehdessä **Lisää**-painike.
3. Valitse **Tapahtumalaji**-kentässä **Tunti**.
4. Valitse **Työntekijä**-kentässä työntekijä, joka toimittaa huollon.
5. Valitse **Huoltoväli**-kentässä 10 päivän väli.

Olet nyt luonut huoltosopimusrivin, jossa on seuraavat tiedot:

| Tapahtumalaji | Aloituspäivämäärä                               | Huoltoväli |
|------------------|------------------------------------------|------------------|
| Tunti             | Nykyinen päivämäärä.                        | Joka 10. päivä    |
| Työntekijä           | Huollon suorittava työntekijä. |                  |

Riville ei ole määritetty aikaikkunaa. 

### <a name="create-planned-service-orders"></a>Suunniteltujen huoltotilausten luominen

Voit nyt luoda tulevan kuukauden suunnitellut huoltotilaukset ja huoltotilausrivit.

1. Valitse **Huoltosopimukset**-sivun **toimintoruudun** **Toimita**-välilehdessä **Suunnitellut huoltotilaukset**.
2. Anna **Huoltotilausten luominen** -sivulla kuluva päivämäärä **Päivämäärästä**-kentässä ja kuukauden päässä kuluvasta päivästä oleva päivämäärä **Päivämäärään**-kentässä.
3. Siirrä **Tunti**-liukusäädin **Kyllä**-kohtaan. 
4. Napsauta **OK**.

Koska huoltotilausta ei ole ryhmitelty (jonka määrittää **Yhdistä huoltotilaukset** -kentän **Huoltosopimuksen mukaan** -asetus), kullekin huoltotilaukselle luodaan yksi huoltotilausrivi.

### <a name="service-orders-created"></a>Luodut huoltotilaukset

**Luo huoltotilaukset** -valintaikkunassa määritetylle aikavälille on luotu kolme huoltotilausriviä. Voit tarkastella huoltotilausrivejä **Huoltosopimukset**-sivulla (**toimintoruutu** \> **Toimita**-välilehti \>**Näytä**-painike).

## <a name="related-topics"></a>Liittyvät aiheet

[Huoltovälien määrittäminen](set-up-service-intervals.md)  

