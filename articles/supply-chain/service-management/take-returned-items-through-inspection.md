---
title: Palautettujen nimikkeiden vastaanottaminen tarkastuksen kautta
description: Palautettujen nimikkeiden vastaanottaminen tarkastuksen kautta.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa85bf4262216c780c3da523f65baf980fdc200f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206562"
---
# <a name="take-returned-items-through-inspection"></a>Palautettujen nimikkeiden vastaanottaminen tarkastuksen kautta 

[!include [banner](../includes/banner.md)]


1.  Valitse **Varastonhallinta** \> **Kausittainen** \> **Laadunhallinta** \> **Karanteenitilaukset**.

2.  Etsi tilausrivi, joka vastaa tarkastettavaa palautettua nimikettä.

    > [!NOTE]
    > <P>Karanteenitilaus voidaan liittää vain yhteen nimiketunnukseen. Jos kymmenen nimikettä palautetaan samasta lähetyksestä ja lähetetään karanteeniin ja nimikkeillä on eri nimiketunnukset, luodaan kymmenen erillistä karanteenitilausta.</P>

3.  Kun olet tutkinut nimikkeen, valitse **Käsittelykoodi**-kentässä, mitä nimikkeelle tehdään ja miten nimikkeeseen liittyvä kirjanpitotapahtuma käsitellään. Esimerkkejä: nimike voidaan palauttaa varastoon ja asiakkaalle voidaan maksaa palautus, nimike voidaan hävittää ja asiakkaalle voidaan lähettää korvaava nimike tai nimike voidaan palauttaa asiakkaalle ilman hyvitystä.
    
    > [!NOTE]
    > <P>Jos saman nimiketunnuserän useille palautetuille nimikkeille ei voi määrittää samaa käsittelykoodia, karanteenitilaus on jaettava (<STRONG>Toiminnot</STRONG> &gt; <STRONG>Jako</STRONG>). Tällöin kullekin osaerälle voidaan määrittää eri käsittelykoodi.</P>


4.  Kun tarkistus on valmis, vapauta palautetut nimikkeet ja luo nimikkeen saapumisen kirjauskansion merkintä valitsemalla **Ilmoita valmiiksi**. Nimikkeen vastaanottanut työntekijä tai osasto käsittelee tämän jälkeen varastoon palautettavien nimikkeiden kirjauskansion.
    
    –TAI–
    
    Päätä karanteenitilaus ja siirrä nimikkeet suoraan takaisin varastoon käyttämällä yhtä **Varasto**-painikkeista.

5.  Tallenna muutokset sulkemalla lomake.

## <a name="see-also"></a>Lisätietoja

[Palautettujen nimikkeiden poistotavan määrittäminen](specify-how-to-dispose-of-returned-items.md)

  


