---
title: Huoltotilausten luominen manuaalisesti
description: Voit luoda huoltotilauksia manuaalisesti huoltosopimuksen tai **Huoltotilaukset**-lomakkeen avulla.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51cfdb94a368df9e7082af3c768c79df44000342
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427100"
---
# <a name="create-service-orders-manually"></a>Huoltotilausten luominen manuaalisesti    

[!include [banner](../includes/banner.md)]


Voit luoda huoltotilauksia manuaalisesti huoltosopimuksen tai **Huoltotilaukset**-lomakkeen avulla. Voit luoda huoltotilauksen myös projektista.

> [!TIP]
> <P>Voit luoda huoltotilauksia automaattisesti. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Huoltotilauksen luominen manuaalisesti huoltosopimuksesta

1.  Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.

2.  Valitse huoltosopimus tai luo uusi huoltosopimus.

3.  Napsauta **Toimita**-välilehteä ja valitse sitten **Luo**-ryhmässä **Suunnitellut huoltotilaukset** avataksesi **Luo huoltotilaukset** -lomakkeen.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Huoltotilauksen luominen manuaalisesti Huoltotilaukset-lomakkeessa

1.  Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  Luo uusi huoltotilaus painamalla CTRL+N.

3.  Luo huoltotilauksen huoltotilausrivit.

> [!NOTE]
> <P>Jos <STRONG>Salli ilman huoltosopimusta</STRONG> -valintaruutu on valittuna <STRONG>Huoltohallintaparametrit</STRONG>-lomakkeessa, voit kirjata huoltotilausrivien tapahtumat liittämättä huoltotilausta huoltosopimukseen. Jos valintaruutu ei ole valittuna, sinun on liitettävä manuaalisesti luotu huoltotilaus projektiin ennen huoltotilausrivien kirjaamista.</P>

## <a name="create-a-service-order-from-a-project"></a>Huoltotilauksen luominen projektista

1.  Valitse **Projektinhallinta ja kirjanpito** \> **Yleinen** \> **Projektit** \> **Kaikki projektit**.

2.  Valitse **Projektit**-lomakkeen **toimintoruudun** **Hallinta**-välilehdessä \> **Huolto** \> **Huoltotilaukset**.

3.  Noudata aiempia ohjeita, jotka koskevat huoltotilauksen luomista manuaalisesti **Huoltotilaukset**-lomakkeen avulla. **Projektitunnus**-kentässä näkyy projektin viite.

> [!NOTE]
> <P>Jos <STRONG>Salli ilman huoltosopimusta</STRONG> -valintaruutu on valittuna <STRONG>Huoltohallintaparametrit</STRONG>-lomakkeessa, voit kirjata huoltotilausrivien tapahtumat liittämättä huoltotilausta huoltosopimukseen. Jos valintaruutu ei ole valittuna, sinun on liitettävä manuaalisesti luotu huoltotilaus projektiin ennen huoltotilausrivien kirjaamista.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Huoltotilauksen luominen myyntitilauslomakkeesta

Voit luoda huoltotilauksen **Myyntitilaukset**-lomakkeesta käyttämällä **Luo uusi huoltotilaus myyntitilauksen perusteella** -ohjattua toimintoa.

1.  Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Myyntitilaukset** \> **Kaikki myyntitilaukset**.

2.  Avaa asianmukainen myyntitilaus.

3.  **Myyntitilaus**-välilehdellä napsauta **Huoltotilaus** aloittaaksesi **Luo uusi huoltotilaus myyntitilauksen perusteella** -ohjatun toiminnon.

4.  Valitse **Seuraava \>**, ja noudata seuraavia ohjeita **Valitse sopimus huoltotilaukselle** -sivulla:
    
      - Valitse **Huoltosopimus**-kentässä huoltosopimus, johon uusi huoltotilaus liittyy.
    
      - Valinnainen: Liitä huoltotilaus tiettyyn projektiin käyttämällä **Projektin tunnus** -kenttää.

5.  Valitse **Seuraava \>**, ja noudata seuraavia ohjeita **Luo huoltotilaus** -sivulla:
    
      - Määritä huoltokutsun alkamispäivämäärä ja -aika **Ensisijainen huoltoaika** -kentässä.
    
      - Valinnainen: Muokkaa **Kuvaus**-kentässä olevaa tekstiä. Oletusarvon mukaan teksti on kuvaus edellisellä sivulla valitsemastasi huoltosopimuksesta.
    
      - Valitse **Vastuuhenkilö**-kentässä sen työntekijän tunnus, joka vastaa sopimuksesta. Valitse myös asiakkaan ensisijainen huoltoteknikko, jos se on tiedossasi.
    
      - Valitse **Yhteystunnus**-kentässä sitä asiakasyrityksen työntekijää edustava tunnus, johon tätä huoltotilausta koskevissa asioissa tulee ottaa yhteyttä.

6.  Valitse **Seuraava \>** ja sitten **Valmis**.


## <a name="see-also"></a>Lisätietoja

[Huoltotilaukset](service-orders.md)

[Automaattisesti luodut huoltotilaukset](create-service-orders-automatically.md)

[Huoltotilausten luominen (luokkalomake)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]