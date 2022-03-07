---
title: Myyntireskontran erääntymisraportti
description: Myyntireskontran erääntymisraportissa näkyy asiakkaiden erääntymissaldot päivämäärävälin tai erääntymiskauden mukaan lajiteltuna.
author: JodiChristiansen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33bee60a3807c92cc97f0f5e6d660a67cdd7f297
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595086"
---
# <a name="customer-aging-report"></a>Myyntireskontran erääntymisraportti 

**Myyntireskontran erääntyminen** -raportissa näkyy asiakkaiden erääntymissaldot päivämäärävälin tai erääntymiskauden mukaan lajiteltuna.

Seuraavat oletusparametrit näytetään, kun tämä raportti luodaan. Voit käyttää näitä parametreja suodattamaan raportissa näkyvät tiedot. Lisätietoja on kohdassa [Valikoimien määrittäminen](set-up-collections.md).

<table>
<colgroup>
<col>
<col>
</colgroup>
<thead>
<tr class="header">
<th><p>Kenttä</p></th>
<th><p>kuvaus</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Laskutusluokka</strong></p></td>
<td><p>Valitse vähintään yksi raporttiin sisällytettävä laskutusluokka.</p>
<div class="alert">

**Huomautus:** Tämä ohjausobjekti on käytettävissä vain, jos <STRONG>Julkinen sektori</STRONG> -määritysavain on valittu.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Sisällytä tapahtumat, joilla ei ole laskutusluokkaa</strong></p></td>
<td><p>Jos tämä valintaruutu on valittu, kaikki tapahtumat, joihin ei ole määritetty laskutusluokkaan, näytetään raportissa.</p>
<div class="alert">

**Huomautus:** Tämä ohjausobjekti on käytettävissä vain, jos <STRONG>Julkinen sektori</STRONG> -määritysavain on valittu.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Erääntyy</strong></p></td>
<td><p>Anna nykyisessä erääntymisjakaumassa käytetty päivämäärä.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tilanne</strong></p></td>
<td><p>Anna päivämäärä, jonka asiakkaan saldoa tarkastellaan. Tätä kutsutaan myös tapahtumien katkaisupäivämääräksi.</p></td>
</tr>
<tr class="even">
<td><p><strong>Aloituspäivä</strong></p></td>
<td><p>Anna päivämäärä, joka kuuluu raporttiin sisällytettävään ensimmäiseen aikaväliin tai erääntymiskauteen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Kriteeri</strong></p></td>
<td><p>Valitse päivämäärätyyppi, johon raportti perustuu.</p>
<ul>
<li><p><strong>Tapahtumapäivä</strong> – Tapahtumien kirjauspäivämäärä. Se voi olla esimerkiksi laskun päiväys, johon eräpäivän laskenta perustuu.</p></li>
<li><p><strong>Eräpäivä</strong> – tapahtumien eräpäivä, joka perustuu maksuehtoihin.</p></li>
<li><p><strong>Asiakirjan päivämäärä</strong> – käyttäjän määrittämä tiedoston päivämäärä, jota käytetään eräpäivän laskennan perusteena.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Erääntymiskausimääritys</strong></p></td>
<td><p>Valitse erääntymiskausimääritys. <strong>Väli</strong>-kenttä ei ole käytettävissä, jos valitset erääntymiskauden määritelmän.</p>
<p>Tulostetussa raportissa ei voi käyttää erääntymiskausimäärityksiä, joissa on yli kuusi erääntymiskautta.</p>
<div class="alert">

**Huomautus:** erääntymiskaudet voidaan määrittää <STRONG>Erääntymiskausimääritykset</STRONG>-sivulla.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Tulosta erääntymiskauden kuvaus</strong></p></td>
<td><p>Valitse <strong>Kyllä</strong>, jos haluat sisällyttää raporttiin erääntymiskauden sarakkeiden yläosissa olevat kuvaukset. Tulosta raportti ilman sarakeotsikoita valitsemalla <strong>Ei</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Väli</strong></p></td>
<td><p>Määritä käytettävä aikaväli kirjoittamalla kunkin kauden päivä tai kuukausi. Voit esimerkiksi tarkastella erääntymistietoja viikoittain kirjoittamalla tähän kenttään 7 ja valitsemalla <strong>Pv/kk</strong>-kentässä <strong>Päivä</strong>.</p>
<div class="alert">

**Huomautus::** Tähän kenttään kirjoittamaasi tietoa käytetään vain, jos et ole valinnut erääntymiskausimääritystä. Muussa tapauksessa tulostuksen suunta määritetään erääntymiskausimäärityksessä.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Pv/kk</strong></p></td>
<td><p>Valitse yksiköksi joko <strong>Päivä</strong> tai <strong>Kuukausi</strong>. Tämä yksikön avulla määritetään <strong>Väli</strong>-kentän kausi.</p></td>
</tr>
<tr class="even">
<td><p><strong>Suunta</strong></p></td>
<td><p>Valitse, lasketaanko menneiden vai tulevien kausien saldot ja kumman erääntymisraportti tulostetaan. Päivämäärät lasketaan suhteessa <strong>Saldo per</strong> -kentässä valitun päivämäärän mukaan. Valitse <strong>Taaksepäin</strong>, jos haluat näyttää menneiden kausien tiedot. Valitse <strong>Eteenpäin</strong>, jos haluat näyttää tulevien kausien tiedot.</p>
<div class="alert">
  
<STRONG>Huomautus::</STRONG> Tähän kenttään kirjoittamaasi tietoa käytetään vain, jos et ole valinnut erääntymiskausimääritystä.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Tietoja</strong></p></td>
<td><p>Valitse luetteloon tapahtumat, jotka sisällytetään raportissa näytettäviin saldoihin.</p></td>
</tr>
<tr class="even">
<td><p><strong>Sisällytä summat tapahtumavaluutassa</strong></p></td>
<td><p>Valitse summien sisällyttäminen tapahtumavaluutassa kirjanpitovaluuttana olevien summien lisäksi. Jos valintaruutua ei ole valittu, raportin summat näytetään vain kirjanpitovaluuttana.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Negatiivinen saldo</strong></p></td>
<td><p>Valitse niiden asiakastilien sisällyttäminen, joilla on negatiivinen saldo.</p></td>
</tr>
<tr class="even">
<td><p><strong>Jätä nollasaldoiset tilit pois</strong></p></td>
<td><p>Valitse niiden asiakastilien pois jättäminen, joilla on nollasaldo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Maksujen positiointi</strong></p></td>
<td><p>Valitse selvittämättömien maksujen näyttäminen. Ne näytetään raportin ensimmäisessä sarakkeessa.</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]