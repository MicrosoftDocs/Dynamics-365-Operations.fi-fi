---
title: Pankin tiliotteen tiedoston tuomisen vianmääritys
description: On tärkeää, että pankin tiliotetiedosto vastaa asetteluja, jotka ovat tuettuja Microsoft Dynamics 365 Financessa. Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein. Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia. Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa. Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 612ded1f68cc8e1b26b8046501bae1707175e23a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188323"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Pankin tiliotteen tiedoston tuomisen vianmääritys

[!include [banner](../includes/banner.md)]

On tärkeää, että pankin tiliotetiedosto vastaa asetteluja, jotka ovat tuettuja Microsoft Dynamics 365 Financessa. Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein. Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia. Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa. Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.

<a name="what-is-the-error"></a>Mikä virhe on kyseessä?
------------------

Kun tiliotetiedoston tuontia on yritetty, siirry Tietojen hallinnan työhistoriaan ja sen suoritustietoihin löytääksesi virheen. Virhe voi auttaa osoittamalla tiliotteeseen, saldoon tai tiliotteen riviin. Se ei kuitenkaan todennäköisesti anna riittävästi tietoa, jotta ongelman aiheuttavan kentän tai elementin voisi tunnistaa.

## <a name="what-are-the-differences"></a>Mitä ovat erot?
Vertaa pankkitiedoston asettelumääritystä Financen tuontimääritykseen ja kiinnitä huomiota kenttien ja elementtien eroihin. Vertaa tiliotetiedostoa liittyvään Finance-näytetiedostoon. ISO20022-tiedostoissa on erot helppo nähdä.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Tuotujen tililaskelmien aikavyöhyke-erot
Tuontitiedoston päivämäärän ja ajan arvot voivat poiketa Finance and Operationsin päivämäärä- ja aika-arvoista. Voit estää tämän ristiriidan määrittämällä aikavyöhykeasetukset **Määritä tietolähteet** -sivulla. Lisätietoja aikavyöhyke asetusten määrittämisestä on kohdassa [Pankin täsmäytyksen lisätuontiprosessin määrittäminen](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Muunnokset
Yleensä muutokset on tehtävä johonkin kolmesta muunnoksesta. Jokaisen muunnos on kirjoitettu tiettyyn standardiin.

| Resurssin nimi                                         | Tiedostonimi                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Muunnosten virheenkorjaus
### <a name="adjust-the-bai2-and-mt940-files"></a>Oikaise BAI2- ja MT940-tiedostot

BAI2- ja MT940-tiedostot ovat tekstiin perustuvia tiedostoja ja ne on oikaistava, jotta Extensible Stylesheet Language Transformation -kielen (XSLT) virheenkorjauksen voi ottaa käyttöön. Ohjelma tekee oikaisun, kun tiedosto tuodaan.

1.  Luo XML-tiedosto ja kopioi siihen seuraava tekstinkatkelma.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopioi tiliotetiedoston sisältö ja liitä se XML-tiedostoon niin, että ne korvaavat **PASTESTATEMENTFILEHERE**-kohdan.

### <a name="debug-the-xslt"></a>XSLT-virheenkorjaus

Lisätietoja on kohdassa <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Käynnistä Microsoft Visual Studio.
2.  Luo konsolisovellus.
3.  Avaa haluamasi XSLT-muoto.
4.  Valitse XSLT-muotoa ja sen ominaisuussivua.
5.  Aseta syötteeksi tiliotetiedoston sijainti.
6.  Määritä tulosteelle sijainti ja tiedostonimi.
7.  Määritä tarvittavat katkaisukohdat.
8.  Valitse valikosta **XML** &gt; **Aloita XSLT-virheenkorjaus**.

### <a name="format-the-xslt-output"></a>Muotoile XSLT-tuloste

Kun muunnos ajetaan, se luo tiedoston, jonka voi avata Visual Studiossa. Voit muotoilla tiedoston nopeasti Ctrl+A, Ctrl+K ja Ctrl+D -näppäinkomennoilla.

### <a name="adjust-the-transformation"></a>Muunnoksen oikaiseminen

Oikaise muunnos saadaksesi haluamasi kentän tai elementin tiliotetiedostoon. Määritä sitten kyseinen kenttä tai elementti asiaankuuluvaan Finance-elementtiin.

### <a name="debitcredit-indicator"></a>Debet/kredit-ilmaisin

Toisinaan on mahdollista, että veloitukset on tuotu hyvityksinä ja hyvitykset veloituksina. Tämän ongelman ratkaisemiseksi on muutettava asiaankuuluvaa XSLT:tä. Jos tiliotteet ovat peräisin useasta pankista, varmista, että kaikissa käytetään samaa debet-/kredit-lähestymistapaa tai luo niille erilliset muunnokseet.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator -malli
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit -malli
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator -malli

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Esimerkkejä tiliotteiden muodoista ja teknisistä asetteluista
Seuraavassa taulukossa on esimerkkejä tuonnin lisäasetuksista pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa: Voit ladata esimerkkitiedostot ja tekniset asettelut täällä: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Tekninen asettelumääritys                             | Esimerkkitiliotetiedosto          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





