---
title: Luo vapaatekstilaskumalli
description: Tässä menettelyssä näytetään miten luodaan vapaan tekstin laskumalli.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182506"
---
# <a name="create-a-free-text-invoice-template"></a>Luo vapaatekstilaskumalli

[!include [banner](../includes/banner.md)]

Tässä esittelyssä käytetään USMF-demoyritystä. Menettely on tarkoitettu käyttäjälle, joka on vastuussa myyntireskontran laskujen hallinnasta ja käsittelemisestä.

## <a name="create-a-template"></a>Luo malli

1. Siirry kohtaan **Myyntireskontra > Laskut > Toistuvat laskut > Vapaatekstilaskun mallit**.
    * Tämän sivun avulla voit luoda vapaatekstilaskun malleja, jotka sisältävät laskurivejä, veloituksia, kirjanpidollisen jaon mallin ja kirjanpitotilin tiedot.  
2. Luo uusi vapaatekstilaskun malli valitsemalla **Uusi**.
3. Syötä **Mallin nimi** -kenttään arvo.
    * Mallin nimi yksilöi vapaatekstilaskun mallin. Kahdelle mallille ei voi määrittää samaa mallin nimeä.  
4. Syötä **Kuvaus**-kenttään mallin kuvaus.
5. Laajenna **Laskurivit**-välilehti.
6. Kirjoita **Kuvaus**-kenttään laskurivin kuvaus.
7. Valitse **Päätili**-kentässä tuottotili.
    * Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle **Asiakkaan kirjausprofiilit** -sivulla.  
8. Avaa haku valitsemalla **Arvonlisäveroryhmä**-kentässä avattavan valikon painike.
    * Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.  
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Valitse **Nimikkeen veroryhmä** -kentässä nykyisen laskurivin nimikkeen arvonlisäveroryhmä.
11. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
12. Syötä **Yksikköhinta**-kenttään laskurivin yksikkökohtainen hinta tai tarkastele sitä.
    * Tämä summa kerrotaan **Määrä**-kentän arvolla laskurivin summan määrittämiseksi.  
13. Lisää vapaatekstilaskun malliin uusi rivi.
14. Kirjoita **Kuvaus**-kenttään laskurivin kuvaus.
15. Valitse **Päätili**-kentässä tuottotili.
    * Voit valita asiakkaan luoton vastatapahtumatilin laskun kokonaissummalle **Asiakkaan kirjausprofiilit** -sivulla.  
16. Avaa haku valitsemalla **Arvonlisäveroryhmä**-kentässä avattavan valikon painike.
    * Nykyisen laskurivin arvonlisäveroryhmä, joka on asiakastilin oletusarvonlisäveroryhmä.  
17. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
18. Avaa haku valitsemalla **Nimikkeen arvonlisäveroryhmä** -kentässä avattavan valikon painike.
    * Valitun laskurivin nimikkeen arvonlisäveroryhmä.  
19. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
20. Yksiköiden määrän syöttäminen laskuriville tai määrän tarkasteleminen.
    * Tämä numero kerrotaan Yksikköhinta-kentän arvolla laskurivin summan määrittämiseksi.  
21. Syötä laskurivin yksikkökohtainen hinta tai tarkastele sitä. 
    * Tämä summa kerrotaan **Määrä**-kentän arvolla laskurivin summan määrittämiseksi.  
22. Tarkastele ja muokkaa yksittäisen rivin ja alatason rivien kirjanpidollisia jakoja.
    * Kirjanpidolliset jaot määrittävät, miten summa käsitellään, esimerkiksi miten tuotto, vero tai maksu käsitellään vapaatekstilaskussa.  
23. Päivitä valitun laskurivin kirjanpidolliset jaot.
24. Valitse **Sulje**.

## <a name="save-a-free-text-invoice-as-a-template"></a>Tallenna vapaatekstilaskumalli
Voit myös tallentaa aiemman vapaatekstilaskun mallina. Kun valitset **Tallenna malliin** **Lasku**-välilehdellä, anna sille nimi ja liitä mallin kuvaus. Jos mallin nimi on jo käytössä, näyttöön tulee ilmoitus, että malli on jo olemassa. Voit kuitenkin napsauttaa **Ok** ja korvata sen. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
