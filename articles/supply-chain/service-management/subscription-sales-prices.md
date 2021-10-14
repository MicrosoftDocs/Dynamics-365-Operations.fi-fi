---
title: Ylläpitosopimuksen myyntihinnat
description: Kun ylläpitosopimus luodaan, myyntihinta saadaan Myyntihinta (ylläpitosopimus) -lomakkeessa luoduista myyntihinta-asetuksista.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd63fc290263babafabd6e29441f008d0cf10e13
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569982"
---
# <a name="subscription-sales-prices"></a>Ylläpitosopimuksen myyntihinnat

[!include [banner](../includes/banner.md)]

Kun ylläpitosopimus luodaan, myyntihinta saadaan **Myyntihinta (ylläpitosopimus)** -lomakkeessa luoduista myyntihinta-asetuksista.

**Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda myyntihintoja tietylle ylläpitosopimukselle tai laajemmin käytettäviä myyntihintoja. Jotta myyntihintaa voidaan käyttää ylläpitosopimuksessa, ylläpitosopimuksen kausikoodin ja valuutan on oltava identtiset myyntihinnan kausikoodin ja valuutan kanssa.

Jos ylläpitosopimuksen ja myyntihinnan kausikoodi ja valuutta ovat identtiset, ylläpitosopimuksen myyntihinnat valitaan seuraavassa taulukossa lueteltujen prioriteettien perusteella. Tyhjä solu taulussa merkitsee tyhjää kenttää ja X merkitsee samaa arvoa kuin ylläpitosopimuksessa, josta tapahtuma luodaan.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Prioriteetti </p></th>
<th><p><strong>Luokka</strong></p></th>
<th><p><strong>Projektin tunnus</strong></p></th>
<th><p><strong>Ylläpitosopimus</strong></p></th>
<th><p><strong>Myyntivaluutta</strong></p></th>
<th><p><strong>Kausikoodi</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>

Kun ylläpitosopimusmaksu luodaan, tarkimmin määritetty myyntihinta (kuten yllä olevasta taulukosta ilmenee) valitaan ylläpitosopimuksen myyntihinnaksi.

## <a name="update-and-index-subscription-sales-prices"></a>Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen

Ylläpitosopimuksen myyntihinnan voi päivittää päivittämällä lähtöhinnan tai indeksin. Voit päivittää hintaa prosenttiluvulla tai päivittää sen uuteen arvoon.

## <a name="subscription-fee-sales-prices"></a>Ylläpitosopimusmaksun myyntihinnat

Kun ylläpitosopimusmaksu luodaan, myyntihinta perustuu ylläpitosopimuksen myyntihinta-asetuksiin. Voit joko käyttää ylläpitosopimuksen hinta-asetusten lähtöhintaa tai luoda indeksoituja myyntihintoja.

## <a name="example"></a>Esimerkki

Haluat määrittää uuden projektin 9030 ylläpitosopimukselle 500 euron myyntihinnat. **Myyntihinta (ylläpitosopimus)** -lomakkeessa voit luoda ylläpitosopimuksen myyntihinnan rivin seuraavassa taulukossa esitetyllä tavalla.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Voimassaolo alkaa</p></th>
<th><p>Luokka</p></th>
<th><p>Project</p></th>
<th><p>Ylläpitosopimus</p></th>
<th><p>Kausikoodi</p></th>
<th><p>Myyntivaluutta</p></th>
<th><p>Myyntihinta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.8.2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Kuukausi</p></td>
<td><p>Euro</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Huomaa, että **Luokka**- ja **Ylläpitosopimus**-kentät ovat tyhjät.

Sitten luot seuraavat ylläpitosopimukset.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Huollon ylläpitosopimus</p></th>
<th><p>Project</p></th>
<th><p>Ylläpitosopimusryhmä</p></th>
<th><p>Luokka</p></th>
<th><p>Valuutta</p></th>
<th><p>Kausikoodi</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p>Euro</p></td>
<td><p>Kuukausittain</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat2</p></td>
<td><p>Euro</p></td>
<td><p>Kuukausittain</p></td>
</tr>
</tbody>
</table>


Seuraavaksi luot ylläpitosopimusmaksut molemmille Sub1-ylläpitosopimusryhmän ylläpitosopimuksille:

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.

2.  Valitse **Ylläpitosopimusryhmät**-lomakkeessa **Toiminto** \> **Luo ylläpitosopimusmaksu**.

3.  Kirjoita **Luo ylläpitosopimusmaksu** -lomakkeeseen tarvittavat tiedot. Lisätietoja on kohdassa [Ylläpitosopimuksen maksutapahtumien luominen](create-subscription-fee-transactions.md).

Molemmille ylläpitosopimuksille luodaan ylläpitosopimusmaksut, joiden myyntihinta on 500 euroa, seuraavassa taulukossa esitetyllä tavalla.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Projektipäiväys</p></th>
<th><p>Huollon ylläpitosopimus</p></th>
<th><p>Project</p></th>
<th><p>Luokka</p></th>
<th><p>Aloituspäivämäärä</p></th>
<th><p>Päättymispäivä</p></th>
<th><p>Myyntivaluutta</p></th>
<th><p>Myyntihinta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.8.2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>1.1.2007</p></td>
<td><p>31.3.2007</p></td>
<td><p>Euro</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.8.2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>1.1.2007</p></td>
<td><p>31.3.2007</p></td>
<td><p>Euro</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Myöhemmin päätät, että haluat määrittää myyntihinnat SubCat1-luokalle projektissa 9030. Luot siksi uuden myyntihintarivin, jonka myyntihinta on 550 euroa projektin 9030 ja maksuluokan SubCat1 yhdistelmälle. Projektille 9030 on nyt kaksi ylläpitosopimuksen myyntihintariviä, seuraavassa taulukossa esitetyllä tavalla.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Voimassaolo alkaa</p></th>
<th><p>Luokka</p></th>
<th><p>Project</p></th>
<th><p>Ylläpitosopimus</p></th>
<th><p>Kausikoodi</p></th>
<th><p>Valuutta</p></th>
<th><p>Myyntihinta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.8.2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Kuukausi</p></td>
<td><p>Euro</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.8.2007</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Kuukausi</p></td>
<td><p>Euro</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>

Toistat yllä kuvatun menettelyn ja luot ylläpitosopimusmaksut molemmille ylläpitosopimusryhmän Sub1 ylläpitosopimuksille. Seuraava taulukko osoittaa, että tapahtumat on luotu kullekin ylläpitosopimusryhmään liitetylle ylläpitosopimukselle.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Projektipäiväys</p></th>
<th><p>Ylläpitosopimus</p></th>
<th><p>Project</p></th>
<th><p>Luokka</p></th>
<th><p>Aloituspäivämäärä</p></th>
<th><p>Päättymispäivämäärä</p></th>
<th><p>Myyntivaluutta</p></th>
<th><p>Myyntihinta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.7.2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>1.1.2008</p></td>
<td><p>31.3.2008</p></td>
<td><p>Euro</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28.7.2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>1.1.2008</p></td>
<td><p>31.3.2008</p></td>
<td><p>Euro</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>

Ylläpitosopimukseen 00020\_135 liittyvässä ensimmäisessä tapahtumassa 550 euron myyntihinta on peräisin tietyn projektin ja luokan yhdistelmälle määritetystä ylläpitosopimuksen myyntihinnasta. Ylläpitosopimukseen 00021\_135 liittyvässä toisessa tapahtumassa 500 euron myyntihintaa käytetään projektin ylläpitosopimuksen myyntihintana, koska projektin 9030 ja luokan SubCat2 yhdistelmälle ei ole määritetty hintaa.

## <a name="see-also"></a>Lisätietoja

[Ylläpitosopimuksen myyntihintojen päivittäminen ja indeksoiminen](update-and-index-subscription-sales-prices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
