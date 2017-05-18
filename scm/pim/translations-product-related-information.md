---
title: "Tuotteeseen liittyvien käännösten usein kysytyt kysymykset"
description: "Tässä ohjeaiheessa kuvataan, kuinka tuotteiden, tuotteen dimensioarvojen ja tuotemääritteiden käännöksiä hallitaan."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 809b853634aa4a44b8aa3aebea317f6bc47da697
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="product-related-translations-faq"></a>Tuotteeseen liittyvien käännösten usein kysytyt kysymykset

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kuvataan, kuinka tuotteiden, tuotteen dimensioarvojen ja tuotemääritteiden käännöksiä hallitaan. 

<a name="what-product-related-data-can-be-translated"></a>Mitä tuotteisiin liittyviä tietoja voidaan kääntää?
--------------------------------------------

Voit luoda käännökset seuraaville tuotteeseen liittyville tiedoille:
-   Tuotteiden nimet ja kuvaukset.
-   Tuotemääritearvojen kuvaukset, kutsumanimet ja ohjeteksti.
-   Tuotedimensioarvojen nimet ja kuvaukset.

Voit kääntää tuotteeseen liittyvät tiedot mille tahansa kielelle, joka on käytettävissä **Tekstin käännös** -sivulla. Lisätietoja on seuraavassa osassa **"Tuotekohtaisten tietojen käännösten luominen"**.

## <a name="where-can-i-view-the-translated-information"></a>Missä näen käännetty tietoja?
Voit tarkastella minkä tahansa ulkoisen lähdeasiakirjan, kuten laskun, tuotteisiin liittyvien tietojen käännöksiä, jos asiakirja käyttää kieltä, jonka käännökset ovat käytettävissä.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Tuotteeseen liittyvien tietojen käännösten luominen
Luo tuotteelle käännöksiä noudattamalla seuraavia ohjeita:
1.  Valitse **Tuotetietojen hallinta** &gt; **Yleinen** &gt; **Vapautetut tuotteet**.
2.  Valitse tuote ja sitten Toimintoruutu, **Kielet** -ryhmässä valitse **Kielet**.
3.  **Tekstin käännös** -sivulta **kieli** , valitse kieli. Voit lisätä lisää kieliä laajentamalla **Language** -kentän ja napsauttamalla sitten **OK**.
4.  **Käännetty teksti** -ryhmässä kirjoita käännökset **Kuvaus** ja **Tuotteen nimi** -kenttiin.

Luo tuotemääritteille käännöksiä noudattamalla seuraavia ohjeita:
1.  Valitse **Tuotetietojen hallinta** &gt; **Yleinen** &gt; **Vapautetut tuotteet**.
2.  Valitse **asetukset**, valitse **määritteet**, ja valitse sitten **määritteet**.
3.  Valitse **määritteet** -sivulta **Käännä**.
4.  **Tekstin käännös** -sivulta **kieli** , valitse kieli. Voit lisätä lisää kieliä laajentamalla **Language** -kentän ja napsauttamalla sitten **OK**.
5.  **Käännetty teksti** -ryhmässä kirjoita käännökset **Kuvaus** ja **Tuotteen nimi** ja and **Ohjeteksti** -kenttiin.

Luo tuotedimensioiden arvoille käännöksiä noudattamalla seuraavia ohjeita:
1.  Valitse **Tuotetietojen hallinta** &gt; **Yleinen** &gt; **Vapautetut tuotteet**.
2.  Valitse tuote ja valitse sitten **Tuotedimensiot** .
3.  Valitse jokin tuotemallin dimensioiden linkeistä: **Konfiguroinnit** **Koot**, **Värit** tai **Tyyli**.
4.  Valitse dimensioarvo ja sitten **Käännä**.
5.  **Tekstin käännös** -sivulta **kieli** , valitse kieli. Voit lisätä lisää kieliä laajentamalla **Language** -kentän ja napsauttamalla sitten **OK**.
6.  **Käännetty teksti** -ryhmässä kirjoita käännökset **Nimi** ja **Kuvaus** -kenttiin.

## <a name="can-the-names-of-product-variants-be-translated"></a>Voidaan tuotevarianttien nimet kääntää?
Tuotevariantit perustuvat vapautettujen tuotteiden dimensioihin. Tuotevarianttien nimet perustuvat tuotedimensioarvoiden yhdistelmään. Kun tuotevarianttiin liittyvät dimensioarvot käännetään, tuotevariantin nimi näkyy käännetyssä versiossa.  

**Esimerkki**  

Tuote on t-paita, jota on saatavilla kolmessa eri koossa ja värissä ja varianttien nimet perustuvat seuraaviin tietoihin:
-   Tuotenumero: \#3
-   Mitat: Koko ja väri
-   Kokodimension arvot: pieni, keskisuuri, suuri
-   Dimensioarvojen värin: punainen, vihreä, musta

Dimensioarvoihin ja Pieni ja Punainen perustuvan tuotevariantin nimi on **\#3:Pieni:Punainen**.  

Asiakas haluaa ostaa pienikokoisia, punaisia T-paitoja, ja T-paidan nimi on merkittävä laskuun ranskan kielellä. Käännät dimensioarvot pieni ja punainen ranskaksi ja tuotevariantin nimi on **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Vihje</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Määritä asiakkaan ensisijainen kieli seuraavien ohjeiden avulla:
<ol>  
<li>Valitse <strong>Myynti ja markkinointi</strong> &gt; <strong>Yleinen</strong> &gt; <strong>Asiakkaat</strong> &gt; <strong>Kaikki</strong>  <strong>asiakkaat</strong>.</li>
<li>Avaa <strong>Asiakkaat</strong>-lomake kaksoisnapsauttamalla asiakasta. Valitse <strong>Yleinen</strong>-välilehdestä <strong>Kieli</strong> -kentän <strong>kieli</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Mitä tapahtuu, jos asiakkaalla on ensisijainen kieli, jolle ei ole saatavilla käännöksiä?
Jos käännökset eivät ole käytettävissä asiakkaan ensisijaisella kielellä, nimet ja kuvaukset näytetään oman yrityksen yleisellä kielellä.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Voinko hallita dimensioarvojen sarjojen tapahtumia samalla kertaa?
Dimensioarvot ovat tuotekohtaisia ja voit hallita jokaisen tuotteen dimensioarvojen käännöksiä. Jos luot dimensioarvoryhmän ja arvoryhmässä olevien arvojen käännökset arvojen ryhmässä, on käännökset helpompi hallita.   

**Esimerkki**  

Yrityksesi valmistaa eri tyylisiä t-paitoja ja kaikki ovat saatavilla S-, M- ja L-koossa. Koot kootaan yhteen dimensioarvoryhmään. Kun uusi T-paidan malli lisätään, voit liittää sen dimension arvoryhmään, jota käytetään ko'oille niin, että koot ovat käytettävissä tuotteelle. Voit lisätä tai muuttaa tapahtumien kokoja milloin tahansa arvon dimensioryhmässä.  

Dimensioarvo, joka on liitetty tuotteeseen dimensiovariantin ryhmän välityksellä on ylläpidettävä tuotevariantin ryhmästä.   
Luo dimension arvoryhmä noudattamalla seuraavia ohjeita:
1.  Valitse **tuotetietojen hallinta** &gt; **asetukset** &gt; **muuttujaryhmät**.
2.  Valitse **koon** **ryhmät**, **väriryhmät**, tai **tyyliryhmät**.
3.  Valitse **Uusi**, ja kirjoita sitten ryhmän nimi **Koko****ryhmä**, **Väriryhmä**, tai **Tyyliryhmä**-kentässä. Valitse **Koot**, **Värit** tai **Tyylit** jos haluat luoda rivit ryhmille.
4.  **Koon** **ryhmän** rivit, **värin** **ryhmän** **rivit**, tai **tyyliryhmän rivit** -sivulla valitse **uusi**, ja luo koot, värit ja tyylit ryhmille.

Hallinnoi dimension arvoryhmän arvojen käännöksiä noudattamalla seuraavia ohjeita:
1.  Noudata edellisten kohtien toimintaohjeita arvodimensioryhmän luomiseen ja avaa **Kokoryhmän rivit**, **Väriryhmän rivit** tai **Tyyliryhmän rivit** -sivu.
2.  Valitse **Tekstin käännös**. **Tekstin käännös** -sivun **Käännetty teksti** -ryhmässä kirjoita käännökset **Nimi** ja **Kuvaus** -kenttiin.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Milloin voidaan tuotteisiin liittyvien tietojen käännöksiä hallinnoida?
Tuotteisiin liittyvien tietojen käännöksiä voidaan hallinnoida milloin tahansa. Kun tapahtumat päivitetään dimension arvolla, joka on liitetty tuotteeseen, tuotteen tiedot päivitetään, riippumatta siitä, onko tuotteella tapahtumia.






