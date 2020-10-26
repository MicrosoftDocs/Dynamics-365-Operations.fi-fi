---
title: Palautettujen nimikkeiden vastaanoton rekisteröiminen
description: Voit rekisteröidä palautetut nimikkeet vastaanotetuiksi Saapumisten yleiskatsaus -lomakkeella tai Rekisteröinti-lomakkeella.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42ca1d4d2d9b45d79cf479833f83e498e3b73540
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975629"
---
# <a name="register-the-receipt-of-returned-items"></a>Palautettujen nimikkeiden vastaanoton rekisteröiminen 

[!include [banner](../includes/banner.md)]


Järjestelmässä on kaksi tapaa rekisteröidä palautettujen nimikkeiden vastaanotto. Ensimmäinen menetelmä on vastaanottavan varaston prosessi, joka käyttää **Saapumisten yleiskatsaus** -lomaketta. Toinen käyttää **Rekisteröinti**-lomaketta.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Rekisteröi palautettujen nimikkeiden vastaanotto Saapumisten yhteenveto -lomakkeella

Voit käyttää **Saapumisten yleiskatsaus** -lomaketta tunnistamaan palautuslähetyksen palautusnumeron (RMA) perusteella. Jos kirjauskansion nimi on määritetty **Määritys**-välilehdellä ja kirjauskansiorivit, jotka vastaavat **Saapumisten yleiskatsaus** -lomakkeella valittuja rivejä ovat olemassa, uuden kirjauskansion otsikko luodaan, kun valitset **Aloita saapuminen**.

1.  Napsauta **Varastonhallinta** \> **Kausittainen** \> **Saapumisten yhteenveto**.

2.  Valitse **Asetusten nimi** -kentässä **Palautustilaus**, ja napsauta sitten **Päivitä**.
    

    > [!TIP]
    > <P>Voit kaventaa hakutuloksia <STRONG>Alue</STRONG>-kenttien avulla. Voit kirjoittaa tai valita palautusnumeron <STRONG>Palautusnumero</STRONG>-kentässä, kun haluat saada tarkan tuloksen. Määritä ja tallenna suodatinjoukko, joka rajaa näytettäviä saapumisia, napsauttamalla <STRONG>Määritys</STRONG>-välilehteä. Käytettävissä on suodattimet tyyppien, varastojen ja laiturien mukaan.</P>

    

    > [!WARNING]
    > <P>Palautustilauksia ei voi sekoittaa muiden saapumistyyppien kanssa <STRONG>Saapumisten yleiskatsaus</STRONG> -lomakkeella. Tämän vuoksi viitteenä on aina oltava myyntitilaus, mutta myyntitilauksen tunnusta ei määritetä kirjauskansion otsikkoon.</P>



3.  Etsi **Kuitit**-ruudukossa rivi, joka vastaa palautettavaa nimikettä ja valitse sitten **Valitse saapumiseen** -sarakkeen valintaruutu.

4.  Jos haluat sulkea tietyt rivit, kuten alkuperäisen tilauksen palautuslähetyksestä poissuljetut rivit, pois palautuksen vastaanotosta, poista liittyvien **Valitse saapumiseen** -ruutujen valinnat lomakkeen alaosan **Rivit**-taulusta.

5.  Valitse **Aloita saapuminen** -painike ja luo saapumisen kirjauskansio.
    

    > [!NOTE]
    > <P>Voit valita useita palautustilauksia ja sisällyttää ne kaikki yhteen saapumisprosessiin. Jokainen palautustilausrivi kopioidaan vastaavan nimikkeen saapumisen kirjauskansion riville.</P>

    

    > [!NOTE]
    > <P>Voit luoda saapumisen kirjauskansion myös manuaalisesti <STRONG>Nimikkeen saapuminen</STRONG> -lomakkeen avulla. 



6.  Napsauta **Varastonhallinta** \> **Kirjauskansiot** \> **Nimikkeen saapuminen** \> **Nimikkeen saapuminen**.

7.  Valitse juuri luomasi saapumisen kirjauskansio ja valitse sitten **Rivit** avataksesi **Kirjauskansion rivit, sijainnit** -lomakkeen.

8.  Säädä **Yleinen**-välilehdessä numeroa **Määrä**-kentässä, jos tämä on tarpeen, ja määritä sitten käsittelykoodi **Käsittelykoodi**-kentässä.
    
    Vaihtoehtoisesti voit valita **Karanteeninhallinta**-valintaruudun, joka asettaa palautetut nimikkeet lähetettäväksi tarkastusprosessin kautta karanteenitilauksen kontekstissa.
    

    > [!NOTE]
    > <P>Jos lähetät palautetut nimikkeet karanteenissa kautta, et voi määrittää käsittelykoodia.</P>



9.  Valitse **Vahvista**-painike.

10. Jos oikeellisuustarkistuksessa ei ole virheitä, valitse **Kirjaa**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Rekisteröi palautettujen nimikkeiden vastaanotto rekisteröintilomakkeella

**Saapumisten yleiskatsaus** -lomakkeen sijasta voit käyttää palautettujen nimikkeiden saapumisten rekisteröimiseen **Rekisteröinti**-lomaketta.

1.  Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**. Luo uusi palautustilaus tai avaa palautustilaus luettelosta. Valitse palautustilausrivi **Rivit**-pikavälilehdessä. Valitse **Päivitä rivi**, ja valitse sitten **Rekisteröinti**.

2.  Määritä käsittelykoodi **Käsittelykoodi**-kenttään ja valitse sitten **OK**.
    

    > [!NOTE]
    > <P>Nimikkeen lähettäminen tarkastettavaksi karanteenitilauksena ei ole mahdollista <STRONG>Rekisteröinti</STRONG>-lomakkeen avulla.</P>



3.  Valitse **Tapahtumat**-ruudukossa rekisteröitävä tapahtuma.

4.  Valitse **Rekisteröi nyt** -ruudukossa **Lisää**. Toista kaksi aiempaa vaihetta, kunnes kaikki palautetut nimikkeet näkyvät **Rekisteröi nyt** -ruudukossa.

5.  Napsauta **Kirjaa kaikki**.

## <a name="see-also"></a>Lisätietoja

[Saapumisten yhteenveto (lomake)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  


