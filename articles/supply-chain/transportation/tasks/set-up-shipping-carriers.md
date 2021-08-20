---
title: Lähetyksen rahdinkuljettajien määrittäminen
description: Tässä aiheessa kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta.
author: ShylaThompson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 480fb7cdc99cd83ba881d626e3c45427f7554681630766aff82457ac11a9eb0b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750999"
---
# <a name="set-up-shipping-carriers"></a>Lähetyksen rahdinkuljettajien määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta. Kuljetuskoordinaattori voi sitten määrittää lähtevälle tai saapuvalle kuormalle rahdinkuljettajan.


## <a name="create-a-new-shipping-carrier"></a>Uuden lähetyksen rahdinkuljettajan luominen
1. Valitse **Siirtymisruutu > Moduulit > Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat**.
2. Valitse toimintoruudussa **Uusi**.
3. Syötä **Lähetyksen rahdinkuljettaja** -kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **Tila**-kentästä vaihtoehto avattavasta valikosta.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Lähetyksen rahdinkuljettajan yleistietojen täyttäminen
1. Ota käyttöön **Yleiskuvaus**-osan laajennus.
2. Valitse **Aktivoi lähetyksen rahdinkuljettaja** -valintaruutu tai poista sen valinta.
3. Valitse **Toimittajan tili**-kentästä vaihtoehto avattavasta valikosta. Valitse toimittajan tili, johon lähetyksen rahdinkuljettaja liitetään.  
4. Valitse vaihtoehto **Kuljetuksen maksuvälineen tyyppi** -kentässä. Valitse **Manuaalinen** käyttääksesi Kuljetuksen maksuväline -sivua tai valitse **EDI**, kun haluat päivittää maksuvälineen sähköistä tiedonsiirtoa (EDI = Electronic Data Interchange) käyttäen.  
5. Valitse **Aktivoi rahdinkuljettajan luokitus** -valintaruutu tai poista sen valinta.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Lähetyksen rahdinkuljettajan tarvitsemien palveluiden luominen
1. Ota käyttöön **Palvelut**-osan laajennus.
2. Valitse **Uusi**.
3. Syötä **Rahdinkuljettajan palvelu** -kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **Kuljetusmenetelmä**-kentästä vaihtoehto avattavasta valikosta.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Rahdinkuljettajan osoitteen määrittäminen (valinnainen)
1. Ota käyttöön **Osoitteet**-osan laajennus.
2. Valitse **Uusi**.
3. Kirjoita **Nimi tai kuvaus** -kenttään arvo.
4. Valitse **Maa/alue**-kentästä vaihtoehto avattavasta valikosta.
5. Valitse **Postinumero**-kentästä vaihtoehto avattavasta valikosta.
6. Kirjoita arvo **Katuosoite**-kenttään.
7. Valitse **OK**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Lähetyksen rahdinkuljettajan luokituksen profiilin määrittäminen
1. Ota **Luokituksen profiilit** -osan laajennus käyttöön.
2. Valitse **Uusi**.
3. Syötä **Luokituksen profiili** -kenttään arvo.
4. Kirjoita arvo **Nimi**-kenttään.
5. Valitse **Toimipaikka**-kentästä vaihtoehto avattavasta valikosta.
6. Valitse **Varasto**-kentästä vaihtoehto avattavasta valikosta.
7. Valitse **Hinnan laskenta**-kentästä vaihtoehto avattavasta valikosta. Valitse hinnan laskenta rahdinkuljettajan yhteystietojen perusteella.  
8. Valitse **Hinnan päätiedot**-kentästä vaihtoehto avattavasta valikosta.
9. Valitse **Siirtoajan laskenta**-kentästä vaihtoehto avattavasta valikosta.
10. Valitse **Tallenna**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]