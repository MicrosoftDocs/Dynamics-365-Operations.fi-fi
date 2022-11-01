---
title: Rivin nettosummien laskeminen uudelleen myyntitilausten ja tarjousten tuomisen aikana
description: Tässä artikkelissa kuvaillaan, laskeeko järjestelmä uudelleen rivien nettosummat myyntitilauksia ja tarjouksia tuodessaan ja miten se tehdään. Osassa on myös tietoja siitä, miten Microsoft Dynamics 365 Supply Chain Managementin eri versioiden toimintatapaa voidaan ohjata.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719331"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Rivin nettosummien laskeminen uudelleen myyntitilausten ja tarjousten tuomisen aikana

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvaillaan, laskeeko järjestelmä uudelleen rivien nettosummat myyntitilauksia ja tarjouksia tuodessaan ja miten se tehdään. Osassa on myös tietoja siitä, miten Microsoft Dynamics 365 Supply Chain Managementin eri versioiden toimintatapaa voidaan ohjata.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Rivin nettosummien päivitysten laskeminen tuonnin aikana

Supply Chain Management -versio 10.0.23 otettu käyttöön [ohjelmakorjaus 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Tämä ohjelmakorjaus muutti ehtoja, joiden täyttyessä rivin **Nettosumma**-kenttä voidaan päivittää tai laskea uudelleen, kun aiemmin luotujen myyntitilausten ja tarjousten päivitykset tuodaan. Versiossa 10.0.29 voit korvata tämän ohjelmakorjauksen ottamalla *Laske rivin nettosumma tuonnin yhteydessä* -ominaisuuden käyttöön. Ominaisuudella on sama vaikutus, mutta se sisältää yleisen asetuksen, jonka avulla voit tarvittaessa palata vanhaan toimintoon. Vaikka uuden toiminnan ansiosta järjestelmä toimii intuitiivisemmin, se voi tuottaa odottamattomia tuloksia tietyissä tilanteissa, joissa kaikki seuraavat ehdot täyttyvät:

- Aiemmin luotuja tietueita päivittävät tiedot tuodaan *myyntitilausrivien V2*, *myyntitarjousrivien V2* tai *palautustilausrivien* entiteetin kautta ODataa (Open Data Protocol) käyttäen. Tällaisia ovat tilanteet, joissa käytät kaksoiskirjoitusta, tuontia tai vientiä Excelin kautta sekä joitakin kolmannen osapuolen integrointeja.
- Käytössä olevat [kauppasopimuksen arviointikäytännöt](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) rajoittavat myyntitilausrivien, myyntitarjousrivien ja/tai palautustilausrivien **Nettosumma**-kentän päivityksiä. Ota huomioon, että palautustilausrivien **Nettosumma**-kenttä lasketaan aina. Sitä ei voi määrittää manuaalisesti.
- Tuotavat tiedot sisältävät rivien **Nettosumma**-kenttään tehtyjä muutoksia tai muutoksia (kuten yksikköhinta, määrä tai alennus), jotka aiheuttavat rivien **Nettosumma**-kentän arvon uudelleenlaskennan yhtä tai useita rivitietueita varten.

Näissä erityisskenaarioissa kauppasopimuksen arviointikäytännön vaikutuksena on rajoittaa rivin **Nettosumma**-kentän päivityksiä. Tätä rajoitusta kutsutaan *muutoskäytännöksi*. Tämän käytännön vuoksi järjestelmä pyytää vahvistamaan, haluatko tehdä muutoksen, kun muokkaat kenttää käyttöliittymän avulla tai lasket sen uudelleen. Kun tuot tietueen, järjestelmän on kuitenkin tehtävä valinta puolestasi. Järjestelmä on aina jättänyt rivin nettosumman ennalleen ennen versiota 10.0.23, ellei saapuvan rivin nettosumma ole 0 (nolla). Uusissa versioissa järjestelmä päivittää tai laskee nettosumman aina uudelleen tarpeen mukaan, ellei sitä ole nimenomaisesti kehotettu olla tekemättä niin. Vaikka uusi toiminta on loogisempaa, se saattaa aiheuttaa ongelmia, jos olet jo suorittamassa prosesseja tai integrointeja, joissa oletuksena on vanhempi toiminto. Tässä artikkelissa kuvaillaan, miten vanha toiminta tarvittaessa palautetaan.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Rivin nettosummien laskelmien hallinta versioissa 10.0.29 ja sitä myöhemmissä versioissa

Supply Chain Managementin versio 10.0.29 on ottanut käyttöön ominaisuuden nimeltä *Laske rivin nettosumma tuonnin yhteydessä*. Tämä ominaisuus lisää **Myyntireskontran parametrit** -sivulle asetuksen, jonka nimi on **Laske rivin nettosumma**. Tämän vaihtoehdon avulla voit valita uusien ja vanhojen toimintojen välillä rivin nettosummien laskemista varten tuonnin aikana.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Laske rivin nettosumma tuonnin yhteydessä -ominaisuuden käyttöön ottaminen tai käytöstä poistaminen

Kun päivität versioon 10.0.29, *Laske rivin nettosumma tuonnin yhteydessä* -ominaisuus on oletusarvon mukaan käytössä ja uusi **Laske rivin nettosumma** -asetus on aluksi arvossa *Kyllä*. *Kyllä*-asetus vastaa uutta normaalia toimintaa. Se vastaa järjestelmän toimintatapaa, kun toiminto on poistettu käytöstä, lukuun ottamatta [CalculateLineAmount-parametrin](#CalculateLineAmount) toimintoja, kuten jäljempänä tässä artikkelissa on kuvattu. *Ei*-asetus vastaa järjestelmän toimintatapaa ennen versiota 10.0.23, ja se on tarkoitettu lähinnä vanhojen integrointiskenaarioiden tueksi.

Järjestelmänvalvojat voivat ottaa *Laske rivin nettosumma tuonnin yhteydessä* -ominaisuuden käyttöön tai poistaa sen käytöstä [Ominaisuuksien hallinta -työtilassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Laske rivin nettosumma -asetuksen määrittäminen

Kun *Laske rivin nettosumma* -toiminto on käytössä, voit määrittää **Laske rivin nettosumma** -asetuksen seuraavien vaiheiden mukaisesti.

1. Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
1. **Hinnat**-välilehden **Rivin nettosumman laskenta integroinnin avulla** -pikavälilehdessä määritä **Laske rivin nettosumma** -asetukseksi jokin seuraavista arvoista:

    - *Kyllä* – Järjestelmä laskee rivisummat aina uudelleen ja päivittää ne tarvittaessa. (Näin ollen se ohittaa kauppasopimuksen arviointikäytännön.)
    - *Ei* – Jos jonkin rivin nykyinen tai saapuva nettosumma on 0 (nolla), rivin arvo lasketaan uudelleen muiden arvojen (kuten yksikköhinta, määrä ja alennus) perusteella. Jos nykyinen tai saapuva nettosumma eroaa nollasta ja rivin **Nettosumma**-kentässä on määritetty muutoskäytäntö, kenttää ei lasketa uudelleen tai päivitetä silloinkaan, kun rivin hintaan, määrään ja/tai alennukseen tulee muutoksia, jolloin rivin kokonaissumma laskettaisiin uudelleen. Käyttäytyminen vastaa version 10.0.22 käyttäytymistä.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>Laske rivin nettosumma tuonnin yhteydessä -ominaisuuden vaikutus CalculateLineAmount-parametriin

Kun *Laske rivin nettosumma tuonnin yhteydessä* -toiminto on käytössä, parametrin `CalculateLineAmount` `SalesLine`- ja `SalesQuotationLine`-taulukoilla ei ole vaikutusta. Sen sijaan toimintaa hallitaan yleisesti **Laske rivin nettosumma** -asetuksella, joka on kuvattuna edellisessä osassa. Siksi kun toiminto on käytössä, `CalculateLineAmount`-arvoon ei saa ottaa riippuvuutta.

Kun *Laske rivin nettosumma tuonnin yhteydessä* -toiminto on poistettu käytöstä, `CalculateLineAmount`-parametri `SalesLine`- ja `SalesQuotationLine`-taulukoille toimii kuten Supply Chain Managementin versioissa 10.0.23–10.0.28, kuten seuraavassa osassa kuvataan.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Rivin nettosummien laskelmien hallinta versioissa 10.0.28 ja sitä aiemmissa versioissa

[Kun ohjelmakorjaus 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) otettiin käyttöön versiossa 10.0.23, oli mahdollista valita, miten kukin asianmukainen tietoyksikkö käyttäytyy, kun rivin nettosummaa muokataan tai se piti laskea uudelleen muiden muutosten (esimerkiksi päivitetyn nimikkeen hinnan) vuoksi. Voit ohjata tätä toimintatapaa määrittämällä kullekin riville uuden `CalculateLineAmount`-parametrin joksikin seuraavista tuodun tiedoston arvoista:

- **`CalculateLineAmount` = *1*** – Rivin **Nettosumma**-kenttä lasketaan ja päivitetään aina uudelleen riippumatta siitä, onko kentälle määritetty muutoskäytäntö, saapuvan tai aiemmin luodun rivin nettosumman arvosta riippumatta.
- **`CalculateLineAmount` = *0*** – Jos jonkin rivin nykyinen tai saapuva nettosumma on 0 (nolla), rivin arvo lasketaan uudelleen muiden arvojen (kuten yksikköhinta, määrä ja alennus) perusteella. Jos nykyinen tai saapuva nettosumma on eri kuin 0 (nolla) ja rivin **Nettosumma**-kentän muutoskäytäntö on määritetty, kenttää ei lasketa uudelleen eikä päivitetä.  

Järjestelmä käyttäytyy Supply Chain Managementin version mukaan:

- Versiossa 10.0.22 ja sitä aiemmissa versioissa järjestelmä käyttäytyy aina kuin `CalculateLineAmount`-parametrin määrityksenä olisi *0*, eikä sitä voi muokata käyttäytymään ikään kuin `CalculateLineAmount`-parametrin asetuksena olisi *1*.
- Versioissa 10.0.23–10.0.28 järjestelmä käyttäytyy kuin `CalculateLineAmount`-parametrin asetuksena olisi *1* kaikilla riveillä, joilla sitä ei ole nimenomaisesti määritetty arvoon *0* tuontitiedostossa.
