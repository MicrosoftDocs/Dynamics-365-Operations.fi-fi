---
title: Tuotemääritysmallien laskelmat – usein kysytyt kysymykset
description: Tässä artikkelissa kuvataan laskutoimitukset tuotekonfiguraatiomalleille ja laskentojen käyttäminen yhdessä rajoitteiden kanssa.
author: t-benebo
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 593f6a8e28c789a378515ddc8e4163c331442e8b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890941"
---
# <a name="calculations-for-product-configuration-models-faq"></a>Tuotemääritysmallien laskelmat – usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan laskutoimitukset tuotekonfiguraatiomalleille ja laskentojen käyttäminen yhdessä rajoitteiden kanssa.

Laskutoimituksia on mahdollista käyttää aritmeettisiin tai loogisiin toimintoihin. Ne täydentävät lausekkeiden rajoituksia tuotemääritysmalleissa. Voit määrittää laskutoimituksia **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla ja luoda laskutoimituksille lausekkeita lauseke-editorilla. Lisätietoja on kohdassa Laskelmien luominen.

## <a name="what-is-a-calculation"></a>Mikä on laskelma?
Laskutoimitus on elementti, jota voit käyttää tuotteen kokoonpanomallissa. Laskelmat täydentävät rajoituksia mahdollistamalla arvojen laskemisen käyttämällä desimaalilukuja tuotetta määrittäessäsi. Lisäksi laskelmilla on suurempi määrä operaattoreita käytettävissä kuin rajoituksilla.  

Vastaavasti kuin rajoitus, laskenta liitetään tiettyyn tuotekonfiguraatiomallin komponenttiin, eikä sitä voi käyttää uudelleen tai jakaa toisen komponentin kanssa. Tärkeä ero laskelmien ja rajoitusten välillä on, että laskelmat ovat pakottavia (yksisuuntaisia), kun taas rajoitukset ovat määrittäviä (kaksisuuntaisia). Lisätietoja rajoituksista on kohdassa [Tuotteen määritysmallien lausekerajoitukset ja taulukkorajoitukset](expression-constraints-table-constraints-product-configuration-models.md).  

Laskenta koostuu kohdemääritteestä ja laskentakaavasta.

## <a name="what-is-a-target-attribute"></a>Mikä on kohdemäärite?
Kohdemäärite on määrite, joka saa laskennan tuloksen lausekkeesta.  

Seuraavassa lausekkeessa kohdemäärite on tablecloth-mitta:  

**Lauseke:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** on taulukon pituus ja **decimalAttribute2** on pöytäliinan pituus. Tämä lauseke palauttaa kohdemääritteeseen arvon **Tosi**, jos **decimalAttribute2** on suurempi tai yhtä suuri kuin **decimalAttribute1**. Muussa tapauksessa lauseke palauttaa arvon **Epätosi**. Siten pöytäliinan mitta on hyväksyttävä, jos pöytäliinan pituus vastaa pöydän pituutta tai ylittää sen.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Mitä määritetyyppejä voidaan asettaa kohdemääritteiksi?
Kaikki tuotekonfiguroinnin tukemat määritetyypit voidaan asettaa kohdemääritteiksi lukuun ottamatta tekstiä, jolla ei ole kiinteää luetteloa.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Voiko kohdemääritteen arvo rajoittaa syöttömääritteiden arvoja laskennassa?
Ei, kohdemääritteen arvo ei voi rajoittaa syöttömääritteiden arvoja laskennassa, koska laskelmat ovat yksisuuntaisia. Kohdemääritteen arvo on siis asetettu syöttömääritteiden arvojen muutosten perusteella, mutta muutos kohteen arvossa ei vaikuta syöttömääritteisiin. Toiminta tältä osin eroaa rajoitteista. Rajoitukset toimivat kaksisuuntaisesti.

### <a name="example"></a>Esimerkki

Seuraavassa lausekkeessa laskennan kohde on virtajohdon pituus ja syöttöarvo on väri:  

**Lauseke:** \[If Color == "Green", 1.5, 1.0\]  

Nimikettä määrittäessäsi laskenta luo **1,5**-kertaisen pituuden virtajohdon, jos määrität värimääreeksi **Green**. Jos määrität muita värejä, pituudeksi asetetaan **1,0**. Koska laskelmat ovat kuitenkin yksisuuntaisia, laskenta ei määritä väriarvomääritettä **vihreäksi** määrittäessäsi pituudeksi **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Mitä tapahtuu, jos laskelmalla on kokonaislukutyyppinen kohdemäärite, mutta laskenta tuottaa desimaaliluvun?
Jos kohdemääritteen tietotyyppi on kokonaisluku, mutta laskenta tuottaa desimaaliluvun, palautetaan ainoastaan tuloksen kokonaislukuosa. Desimaaliosa poistetaan, eikä tulosta pyöristetä. Esimerkiksi tulos 12,70 näytetään arvona 12.

## <a name="when-do-calculations-occur"></a>Milloin laskelmia esiintyy?
Laskelmat tehdään, kun kaikille syöttöattribuuteille on annettu arvo.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Voit korvata arvon, joka lasketaan kohteen määritteeseen?
Voit korvata arvon, joka lasketaan kohteen määritteelle, ellei kohteen määritteen arvo ole piilotettu tai vain luku-muotoinen.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a>Kohdemääritteen määrittäminen piilotetuksi tai vain luettavaksi?
Aseta määrite piilotetuksi tai vain luku -tilaan noudattamalla seuraavia ohjeita.

1.  Napsauta **Tuotetietojen hallinta** &gt; **Yleinen** &gt; **Tuotekonfiguraation mallit**.
2.  Valitse tuotemallin konfiguraatio ja napsauta toimintoruudulta **Muokkaa**-toimintoa.
3.  Valitse kohdemääritteenä käytettävä määrite **Rajoituspohjaisen tuotemääritysmallin tiedot** -sivulla.
4.  Valitse **Määritteet** -pikavälilehdeltä **Piilotettu** tai **Vain luku-**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Voiko laskenta korvata asettamani arvot?
Ei. Tuotteen konfiguroinnin yhteydessä asettamasi arvot ovat käytettävät arvot. Laskelma, joka suoritetaan, kun laskelman muuttuvat syötearvot eivät pysty korvaamaan tietylle määritteelle annettuja arvoja.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Mitä tapahtuu, jos poistan laskelmasta syöttöarvon?
Jos poistat syötetyn arvon laskennassa, kohteen määritteen arvo poistetaan.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Miksi näyttöön tulee virhesanoma, jonka mukaan mallissa on ristiriita?
Tämä sanoma tulee näkyviin, kun laskelma sisältää virheen tai vähintään yhdessä rajoituksessa on ristiriita. Lisätietoja ristiriidoista on kohdassa [Tuotteen määritysmallien lausekerajoitukset ja taulukkorajoitukset](expression-constraints-table-constraints-product-configuration-models.md). Tässä esitellään muutama tilanne, joissa laskelmavirheitä voi tapahtua:

-   Arvo jaetaan nollalla.
-   Seuraavien kahden elementin välillä on ristiriita:
    -   Määritteen käytettävissä olevat arvot, joita rajoitetaan rajoitteella
    -   Arvo, joka luodaan laskutoimituksessa
-   Laskelman palauttamat arvot ovat määritteen toimialueen ulkopuolella. Esimerkki on kokonaisluku \[1..10\], joka lasketaan nollaan.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Miksi näyttöön tulee virhesanoma, vaikka tuotemallini on vahvistettu onnistuneesti?
Oikeellisuustarkistukseen ei sisällytetä laskentaa. Sinun on testattava tuotemääritysmalli laskelmien virheiden löytämiseksi. Seuraavat vaiheet kuvaavat tuotekonfiguraatiomallin testaamisen.

1.  Napsauta **Tuotetietojen hallinta** &gt; **Yleinen** &gt; **Tuotekonfiguraation mallit**.
2.  Valitse tuotemallin konfiguraatio ja napsauta toimintoruudun **Suorita**-ryhmästä **Testi**-toimintoa.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]