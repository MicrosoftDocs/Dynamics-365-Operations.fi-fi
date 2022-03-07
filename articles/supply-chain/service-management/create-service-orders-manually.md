---
title: Huoltotilausten luominen manuaalisesti
description: Voit luoda huoltotilauksia manuaalisesti huoltosopimuksen tai **Huoltotilaukset**-lomakkeen avulla.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05c03cd07599c5ee2e739a785896888c8cfe8822e57529f7603783a2f011c97c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740644"
---
# <a name="create-service-orders-manually"></a>Huoltotilausten luominen manuaalisesti    

[!include [banner](../includes/banner.md)]


Voit luoda huoltotilauksia manuaalisesti huoltosopimuksen tai **Huoltotilaukset**-lomakkeen avulla. Voit luoda huoltotilauksen myös projektista.

> [!TIP]
> <P>Voit luoda huoltotilauksia automaattisesti. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Huoltotilauksen luominen manuaalisesti huoltosopimuksesta

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltosopimukset** \> **Huoltosopimukset**.

2.  Valitse huoltosopimus tai luo uusi huoltosopimus.

3.  Valitse **Toimita**-välilehteä ja valitse sitten **Luo**-ryhmästä **Suunnitellut huoltotilaukset** avataksesi **Luo huoltotilaukset** -lomakkeen.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Huoltotilauksen luominen manuaalisesti Huoltotilaukset-lomakkeessa

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  Valitse **Uusi** luodaksesi uuden palvelutilauksen.

3.  Luo huoltotilauksen huoltotilausrivit.

> [!NOTE]
> <P>Jos <STRONG>Salli ilman huoltosopimusta</STRONG> -valintaruutu on valittuna <STRONG>Huoltohallintaparametrit</STRONG>-lomakkeessa, voit kirjata huoltotilausrivien tapahtumat liittämättä huoltotilausta huoltosopimukseen. Jos valintaruutu ei ole valittuna, sinun on liitettävä manuaalisesti luotu huoltotilaus projektiin ennen huoltotilausrivien kirjaamista.</P>

## <a name="create-a-service-order-from-a-project"></a>Huoltotilauksen luominen projektista

1.  Avaa **Projektinhallinta ja kirjanpito** \> **Yleinen** \> **Projektit** \> **Kaikki projektit**.

2.  Valitse **Projektit**-lomakkeen **Toimintoruutu**-osiosta **Hallinta**-välilehti \> valitse **Huolto** \> **Huoltotilaukset**.

3.  Noudata aiempia ohjeita, jotka koskevat huoltotilauksen luomista manuaalisesti **Huoltotilaukset**-lomakkeen avulla. **Projektitunnus**-kentässä näkyy projektin viite.

> [!NOTE]
> <P>Jos <STRONG>Salli ilman huoltosopimusta</STRONG> -valintaruutu on valittuna <STRONG>Huoltohallintaparametrit</STRONG>-lomakkeessa, voit kirjata huoltotilausrivien tapahtumat liittämättä huoltotilausta huoltosopimukseen. Jos valintaruutu ei ole valittuna, sinun on liitettävä manuaalisesti luotu huoltotilaus projektiin ennen huoltotilausrivien kirjaamista.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Huoltotilauksen luominen myyntitilauslomakkeesta

Voit luoda huoltotilauksen **Myyntitilaukset**-lomakkeesta käyttämällä **Luo uusi huoltotilaus myyntitilauksen perusteella** -ohjattua toimintoa.

1.  Avaa **Myynti ja markkinointi** \> **Yleinen** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.

2.  Avaa asianmukainen myyntitilaus.

3.  Valitse **Myyntitilaus**-välilehdestä **Huoltotilaus** käynnistääksesi ohjatun **Luo uusi huoltotilaus myyntitilauksen perusteella** -toiminnon.

4.  Valitse **Seuraava \>** ja noudata sitten seuraavia ohjeita **Valitse sopimus huoltotilaukselle** -sivulla:
    
      - Valitse **Huoltosopimus**-kentässä huoltosopimus, johon uusi huoltotilaus liittyy.
    
      - Valinnainen: Liitä huoltotilaus tiettyyn projektiin käyttämällä **Projektin tunnus** -kenttää.

5.  Valitse **Seuraava \>** ja noudata sitten seuraavia ohjeita **Luo huoltotilaus** -sivulla:
    
      - Määritä huoltokutsun alkamispäivämäärä ja -aika **Ensisijainen huoltoaika** -kentässä.
    
      - Valinnainen: Muokkaa **Kuvaus**-kentässä olevaa tekstiä. Oletusarvon mukaan teksti on kuvaus edellisellä sivulla valitsemastasi huoltosopimuksesta.
    
      - Valitse **Vastuuhenkilö**-kentässä sen työntekijän tunnus, joka vastaa sopimuksesta. Valitse myös asiakkaan ensisijainen huoltoteknikko, jos se on tiedossasi.
    
      - Valitse **Yhteystunnus**-kentässä sitä asiakasyrityksen työntekijää edustava tunnus, johon tätä huoltotilausta koskevissa asioissa tulee ottaa yhteyttä.

6.  Valitse **Seuraava \>** ja sitten **Valmis**.


## <a name="see-also"></a>Lisätietoja

[Huoltotilaukset](service-orders.md)

[Huoltotilausten luominen automaattisesti](create-service-orders-automatically.md)

[Huoltotilausten luominen (luokkalomake)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]