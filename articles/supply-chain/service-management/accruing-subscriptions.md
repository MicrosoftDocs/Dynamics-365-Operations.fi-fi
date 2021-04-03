---
title: Ylläpitosopimusten jaksottaminen
description: Huollon ylläpitosopimuksissa tuotot jaksotetaan manuaalisesti maksutapahtuman laskutuspäivämäärää seuraaville kausille.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a1b955d200afa7474eb8940a118118cfc2f8904
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232155"
---
# <a name="accruing-subscriptions"></a>Ylläpitosopimusten jaksottaminen 

[!include [banner](../includes/banner.md)]


Huollon ylläpitosopimuksissa tuotot jaksotetaan manuaalisesti maksutapahtuman laskutuspäivämäärää seuraaville kausille.

Jaksotuskaudet luodaan ylläpitosopimusmaksulle määrittämällesi laskutuskaudelle, ja ne perustuvat ylläpitosopimuksen kausikoodiin.

Jaksotetun tuoton voi palauttaa.

## <a name="reverse-accruals-of-credit-amounts"></a>Palauta hyvitysten jaksotukset

Jos hyvität laskutettuja ylläpitosopimuksen summia, voit palauttaa jaksotetut summat kahden eri menetelmän avulla.

  - Kukin jaksotetun tuoton tapahtuma on palautettava erikseen ennen hyvityslaskuehdotuksen luomista tapahtumalle. Tämä on manuaalinen menetelmä. (manuaalinen)

  - Voit valita jaksotetun summan palautuksen hyvityslaskun kirjauspäivänä tai jaksotuksen alkuperäisenä kirjauspäivämääränä.

Lisätietoja on kohdassa [Ylläpitosopimuksen parametrit (lomake)](https://technet.microsoft.com/library/aa619615.aspx).

## <a name="setup-requirements"></a>Määritä edellytykset

Jotta tuoton voi jaksottaa, varmista, että seuraavat tietovaatimukset täyttyvät:

## <a name="account-setup"></a>Tiliasetukset

**KET - ylläpitosopimus**- ja **Jaksotettu tuotto - ylläpitosopimus** -tilit on määritettävä **Projekti**-moduulissa.

Kun jaksotettu tuotto kirjataan, jaksotetulla summalla veloitetaan **KET - tilaus** -tiliä ja hyvitetään **Jaksotettu tuotto - ylläpitosopimus** -tiliä.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Tilien määrittäminen ylläpitosopimuksen tuoton jaksottamisen

1.  Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Kirjaus** \> **Kirjanpidon asetukset**.

2.  Valitse **Tuottotilit**-välilehti ja valitse **KET - yYlläpitosopimus** tai **Jaksotettu tuotto - ylläpitosopimus** tilien määrittämiseksi.

## <a name="subscription-group-setup"></a>Ylläpitosopimusryhmän asetukset

**Jaksota tuotot** -valintaruudun on oltava valittuna, jotta ylläpitosopimuksen tuotto voidaan jaksottaa. Valintaruutu on **Ylläpitosopimusryhmät**-lomakkeessa ryhmälle, joka on liitetty ylläpitosopimukseen. Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Tuoton jaksottamisen käyttöönotto ylläpitosopimusryhmälle

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Ylläpitosopimusryhmät**.

## <a name="periods"></a>Kaudet

Laskutuskauden koodi on määritettävä. Jos et halua käyttää tuottojen jaksotukseen samoja aikavälejä kuin laskutukseen, myös jaksotuskausi on määritettävä.

Seuraavassa taulukossa on yhteenveto siitä, mitä jaksotuskausia voi määrittää millekin laskutuskausille:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Laskutuskausi</p></th>
<th><p>Jaksotuskaudet</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Vuosia</strong></p></td>
<td><ul>
<li><p><strong>Vuosia</strong></p></li>
<li><p><strong>Vuosineljännes</strong></p></li>
<li><p><strong>Kuukausi</strong></p></li>
<li><p><strong>Päivä</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Vuosineljännes</strong></p></td>
<td><ul>
<li><p><strong>Vuosineljännes</strong></p></li>
<li><p><strong>Kuukausi</strong></p></li>
<li><p><strong>Päivä</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Kuukausi</strong></p></td>
<td><ul>
<li><p><strong>Kuukausi</strong></p></li>
<li><p><strong>Päivä</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Viikko</strong></p></td>
<td><ul>
<li><p><strong>Päivä</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Päivä</strong></p></td>
<td><ul>
<li><p><strong>Päivä</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Laskutuskauden määrittäminen on pakollinen osa ylläpitosopimusryhmän asetuksia. Voit määrittää myös ylläpitosopimusryhmän jaksotuskauden. Jos määrität ylläpitosopimusryhmälle jaksotuskauden, ohjelma ehdottaa tätä kautta **Kausikoodi**-kentässä. Tämä kenttä sisältyy **Ylläpitosopimuksen tuoton jaksottaminen** -lomakkeeseen ylläpitosopimuksen tuottoa jaksotettaessa. Jaksotuskausi kuuluu kuitenkin ylläpitosopimusryhmän valinnaisiin tietoihin.


> [!NOTE]
> <P>Avaa <STRONG>Ylläpitosopimuksen tuoton jaksottaminen</STRONG> -lomake käyttämällä seuraavaa polkua. Valitse <STRONG>Huoltohallinta</STRONG> &gt; <STRONG>Kausittainen</STRONG> &gt; <STRONG>Huoltotilaukset</STRONG> &gt; <STRONG>Jaksota ylläpitosopimuksen tuotto</STRONG>.</P>


## <a name="transactions"></a>Tapahtumat

Voit määrittää, kuinka monta kirjanpitotapahtumaa luodaan, kun jaksotettu tuotto kirjataan. Määritä ylläpitosopimuksissa, luodaanko kirjanpidon tapahtumat kokonaissummana vai riveittäin.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Jaksotetuille tapahtumille näytettävien kirjaustietojen tason määrittäminen

1.  Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**.

2.  Valitse **Taloushallinto**-välilehden **Laskutus**-kentästä **Yhteensä** tai **Rivi**.


## <a name="see-also"></a>Lisätietoja

[Jaksota ylläpitosopimuksen tuotto](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]