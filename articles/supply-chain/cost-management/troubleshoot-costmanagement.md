---
title: Kustannusten hallinnan vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita kustannusten hallinnan käytössä voi esiintyä.
author: AndersGirke
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: fc6a48a44a529c82c2a9ee818af95569d9bcb249
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834286"
---
# <a name="troubleshoot-cost-management"></a>Kustannusten hallinnan vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita kustannusten hallinnan käytössä voi esiintyä.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Varastoarvon ja erääntymisraporttien sekä niiden tallennusversioiden väliset toiminnalliset aukot

[Varaston erääntymisraportin tallennus](inventory-aging-report-storage.md)- ja [Varaston arvon tallennusraportti](inventory-value-report-storage.md) -toimintojen avulla Supply Chain Management voi näyttää suuria määriä varastotapahtumia. Kussakin tapauksessa raporttitulokset tallennetaan selausta ja vientiä varten toisin kuin näiden raporttien ei-tallennettavat versiot. Näiden raporttien ei-tallennusversioissa on kuitenkin toimintoja, joita ei ole tallennusversioissa. Seuraavissa aliosissa on erojen yhteenveto ja niiden kiertotavat.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Tallennusraportit eivät sisällä välisummia, vaikka ne olisi otettu käyttöön raporttiasettelussa.

Välisummat voivat aiheuttaa ongelmia, kun tulos viedään, etenkin jo käyttäjät muuttavat tietuejärjestystä.

Välisummat voi tarkistaa viemällä tulokseen Microsoft Exceliin. Vaihtoehtoisesti välisummat voidaan tarkistaa Supply Chain Managementissa ottamalla *Uusi ruudukon ohjausobjekti*- ja *Ryhmittely ruudukoissa* -toiminnot käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tällä tavoin voidaan tarkastella joustavasti minkä tahansa ryhmän välisumman sarakekohtaisesti. Lisätietoja on aiheessa [Ruudukon ominaisuudet](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Varastoarvon tallennusraportti ei tue kirjanpitotilin tietoja

Varastotilien saldo saadaan suorittamalla pääkirja, ja tätä saldoa voidaan verrata **Varastoarvon tallennus** -raporttiin.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Varoitusten tai virheiden näyttäminen muutettaessa kirjanpitokauden tilaa varastoa sulkematta

Microsoft otti seuraavat vahvistukset käyttöön estämään ongelmat, joita kustannuslaskennan virheellinen kauden lopetusprosessi aiheuttaa. Jos jokin seuraavista virhesanomista avautuu, lisätietoja näiden ongelmien ratkaisemisesta on tietoartikkelissa [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3).

- Olet suorittamassa uudelleenlaskennan päivämäärällä %1 (10-02-2019). Viimeksi rekisteröity uudelleenlaskenta suorittiin edellisellä kaudella päivämäärällä %2 (20-01-2019). Varaston sulkemista ei suoriteta päivämäärällä %3 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa varaston sulkeminen alkaen päivämäärästä %3 (31-01-2019), jolloin kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

- Olet muuttamassa kirjanpitokauden tila %1 tilaksi %2. Varaston sulkemista ei suoriteta päivämäärällä %3, jolla kohdistuskauden loppu on rekisteröity. Suorita varaston sulkeminen alkaen %3 kohdistuskauden lopusta ennen tilan muuttamista. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu. Raportoidaan yrityksestä %4. Toistaiseksi tämä on vain tiedoksi, mutta vastaisuudessa sinun on suoritettava tällainen toiminto.

- Tilirakennetta %1on muutettu. Vähintään yhtä päätiliä %2 ei enää ole. %3 tarvitsee näitä päätilejä päivämäärällä %4. Lisää nämä päätilit tilirakenteeseen %1 ennen työn %3 jatkamista. Toistaiseksi tämä on vain tiedoksi, mutta vastaisuudessa sinun on suoritettava tällainen toiminto.

- Olet sulkemassa varaston päivämäärällä %1(31-01-2019). Jälkikustannuslaskentaa ei suoriteta päivämäärällä %2 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa jälkikustannuslaskentaa päivämäärällä %3 (31-01-2019), jolla kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

- Olet suorittamassa jälkikustannuslaskennan päivämäärällä %1 (28-02-2019). Viimeksi rekisteröity jälkikustannuslaskenta suorittiin edellisellä kaudella päivämäärällä %2 (31-01-2019). Varaston sulkemista ei suoriteta päivämäärällä %3 (31-01-2019), jolla kohdistuskauden loppu on rekisteröity.
Muista suorittaa varaston sulkeminen alkaen %3 (31-01-2019), jolloin kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes varaston sulkeminen on suoritettu.

## <a name="inventory-aging-report-discrepancies"></a>Varaston erääntymisraportin ristiriidat

**Varaston erääntymisraportissa** on eri arvot, kun tarkasteltavana on eri varastodimensioita (kuten toimipaikka tai varasto): Lisätietoja raportointilogiikasta on kohdassa [Varaston erääntymisraporttien esimerkkejä ja logiikka](inventory-aging-report.md).

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Päivitysristiriita tapahtuu, kun varaston arvostusmenetelmä on joko standardikustannus tai liukuva keskiarvo

Kun asiakirjoja, kuten varastokirjauskansioita, ostotilauslaskuja tai myyntitilauslaskuja, kirjataan rinnakkain skaalautuvuuden ja suorituskyvyn vuoksi, tuloksena voi olla virhesanoma päivitysristiriidasta eikä kaikkia asiakirjoja ehkä kirjata. Tämä ongelma voi tapahtua, kun varaston arvostusmenetelmä on joko *standardikustannus* tai *liukuva keskiarvo*. Kumpikin menetelmä on jatkuva kustannuslaskentamenetelmä. Lopullinen kustannus määritetään siis kirjauksen aikana.

Jos käytössä on *Liukuva keskiarvo* -menetelmä, virhesanoma muistuttaa seuraavaa esimerkkiä:

> Varaston arvoa xx.xx ei odoteta suhteellisen kululaskelman jälkeen

Jos käytössä on *Standardikustannus* -menetelmä, virhesanoma muistuttaa seuraavaa esimerkkiä:

> Standardikustannus ei vastaa kirjanpitovaraston arvoa päivityksen jälkeen. Arvo = xx.xx, Määrä = yy.yy, Vakiokustannus = zz.zz

Nämä virheet voidaan välttää tai niitä voidaan vähentää käyttämällä seuraavia kiertotapoja siihen saakka, kunnes Microsoft julkaisee ongelman korjaavan ratkaisun:

- Kirjaa epäonnistuneet asiakirjat uudelleen.
- Luo asiakirjoja, joissa on vähemmän rivejä.
- Vältä desimaaliarvojen käyttämistä standardikustannuksissa. Yritä määrittää vakiokustannus siten, että **Hintamäärä**-kentän arvoksi on määritetty *1*. Jos **Hintamäärä**-arvoksi on määritettävä arvo, joka on suurempi kuin *1*, yritä käyttää yksikön standardikustannuksessa mahdollisimman vähän desimaaleja. (Parhaassa tapauksessa desimaaleja on vähemmän kuin kaksi.) Yritä välttää standardikustannuksen asetuksina esimerkiksi seuraavia: **Hinta** = *10* ja **Hintamäärä** = *3*. Tässä tapauksessa yksikön vakiokustannukseksi tulee nimittäin 3,333333 (jossa desimaaliarvo toistuu).
- Useimmissa asiakirjoissa kannattaa välttää sama tuotannon ja varaston taloushallinnon dimensioyhdistelmän käyttämistä useilla riveillä.
- Vähennä rinnakkaisuutta. (Tässä tapauksessa järjestelmä voi nopeutua, koska päivitysristiriitoja ja uudelleenyrityksiä on vähemmän.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]