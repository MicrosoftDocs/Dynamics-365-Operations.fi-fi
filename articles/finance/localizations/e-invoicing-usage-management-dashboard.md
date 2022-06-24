---
title: Käyttöhallinnan raporttinäkymä
description: Tässä artikkelissa on tietoja sähköisen laskutuksen palvelun käyttöhallinnan raporttinäkymän käytöstä ja yhteensopivana pysymisestä.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3fad2acea373e96092208ce06edb31f1a862912d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875968"
---
# <a name="usage-management-dashboard"></a>Käyttöhallinnan raporttinäkymä

[!include [banner](../includes/banner.md)]

**Käyttöhallinta**-raporttinäkymän avulla voit valvoa sähköisen laskutuksen palvelun käyttöä ja näin ollen auttaa organisaatiota pysymään yhteensopivana sen kuukausittaisen käytön kannalta. Yhteensopivuus määräytyy lähetysvolyymien laskennan avulla ja vertaamalla sitä lähetysten hankittuun volyymiin. Näin määritetään kaikki hankitun volyymin ja käytetyn volyymin väliset poikkeamat.

Raporttinäkymä sisältää seuraavat mittarit:

- Yksi kustannusmittari, jonka avulla voit valvoa kulutusta lisenssien noudattamiseksi:

    - Käyttö kuukausittain (vienti)

- Kolme operatiivista mittaria, joiden avulla seurataan sähköisen laskutuksen palvelun käyttöä hallintatarkoituksissa:

    - Käyttö ominaisuuksien mukaan
    - Käyttö ympäristön mukaan
    - Käyttö kuukausittain (tuonti)

## <a name="measurement-scope"></a>Mittareiden vaikutusalue

- Mittayksikkö: 

    **Käyttöhallinta**-raporttinäkymä laskee liiketoimintatiedostojen lähetykset ja tuodut sähköiset laskut.

- Organisaatio: 

    Laskenta tehdään organisaatiosi vuokraajatunnuksen perusteella riippumatta Microsoft Dynamics 365 Financen tai Dynamics 365 Supply Chain Managementin esiintymien lukumäärästä tai niiden yksiköiden lukumäärästä, joissa sähköinen laskutuspalvelu on käytössä.


## <a name="indicator-usage-per-month-export"></a>Mittari: Käyttö kuukaudessa (vienti)

Tässä mittarissa on tietoja sähköisistä laskuista, joita organisaatio lähettää määritetyn kauden aikana.

### <a name="scope"></a>Alue
- Financesta ja Supply Chain Managementista sähköiselle laskutuspalvelulle lähetettyjen liiketoiminta-asiakirjojen määrä riippumatta siitä, kuinka monta riviä nämä liiketoiminta-asiakirjat sisältävät.
- Lähetettyjen liiketoiminta-asiakirjojen määrä, jonka sähköinen laskutuspalvelu käsittelee onnistuneesti. Asiakirjaa käsitellään onnistuneesti, kun toimintoasetuksissa määritettyjen toimenpiteiden työnkulku on valmis.

> [!NOTE]
> Kun sähköinen lasku lähetetään ulkoiseen Internet-palveluun, laskenta ei riipu Internet-palvelun käsittelyn tuloksista (hyväksytty, hylätty tai skeeman oikeellisuustarkistusvirhe). Jos Internet-palvelu on vastaanottanut sähköisen laskutuksen palvelun vastaanottaneen ja vastannut pyyntöön, lähetys lasketaan kelvolliseksi.

- **Poikkeus:** Yritysasiakirjoja ei lasketa, jos ne lähetetään uudelleen Financesta tai Supply Chain Managementista sähköiseen laskutuspalveluun esimerkiksi tilanteissa, joissa saman liiketoiminta-asiakirjan uudelleenlähetys vaaditaan sähköisen laskun tilan muuttamiseksi. Esimerkiksi Brasilian sähköisen laskutuksen (veroasiakirjan) lähetys lasketaan kelvolliseksi, mutta sen peruutuspyyntöä ei lasketa.


### <a name="calculation"></a>Laskelma

Saldo lasketaan seuraavasti:

Saldo = Maksuton + Ostettu - Käytetty

Jossa:

- Maksuton:
  
    Maksuton määrä liikeasiakirjoja, jotka asiakas voi lähettää kuukausittain. Mukana on 100 liiketoiminta-asiakirjan paketti, joka voidaan lähettää sähköiseen laskutuspalveluun. Maksuton määrä ei ole kumulatiivinen, eikä jäljelle jäävä saldoa siirretä seuraavalle jaksolle.
  
- Ostettu:
  
    1 000 liiketoiminta-asiakirjan paketti, joka voidaan lähettää sähköiseen laskutuspalveluun. Tämä paketti on hankittava organisaatiollesi kuukausittain. Ostettu määrä ei ole kumulatiivinen, eikä jäljelle jäävä saldoa siirretä seuraavalle jaksolle.
  
- Käytetty: 

    Sähköisen laskutuksen palveluun lähetettyjen liiketoimintatiedostojen määrä määritettyjen ehtojen mukaisesti.
   
> [!IMPORTANT]
> Jos organisaatiosi aikoo ylittää 100 maksuttoman lähetyksen kuukausittaisen määrän, osta suurin volyymi varmistaaksesi, että olet edelleen Microsoftin sähköisen laskutuksen lisenssikäytännön mukainen.
>
> Tällä hetkellä ostetut volyymit on syötettävä manuaalisesti hankintapäivämäärän mukaan useassa 1 000:n lähetyksen paketissa.

## <a name="indicator-usage-by-feature"></a>Mittari: Käyttö ominaisuuden mukaan

Tässä mittarissa näkyy sähköisten laskutusominaisuuksien käyttö sähköisten laskujen lähettämiseksi määritettynä ajanjaksona.

- Laskenta:
  
    Käytetty = kuinka monta kertaa kutakin sähköistä laskutustoimintoa on käytetty, kun liikeasiakirjoja on lähetetty sähköiseen laskutuspalveluun.

## <a name="indicator-usage-by-environment"></a>Mittari: Käyttö ympäristön mukaan

Tässä mittarissa näkyy sähköisen laskutuksen palveluympäristöjen käyttö määritettynä aikana.

- Laskenta:
    
    Käytetty = kuinka monta kertaa kutakin sähköisen laskutuksen palveluympäristöä on käytetty, kun liikeasiakirjoja on lähetetty sähköiseen laskutuspalveluun.

## <a name="indicator-usage-per-month-import"></a>Mittari: Käyttö kuukaudessa (tuonti)

Tässä mittarissa näkyy, kuinka paljon sähköisiä laskuja on tuotu sähköisen laskutuksen kautta Financeen ja Supply Chain Managementiin määritetyllä kaudella.

- Alue:

    Financeen ja Supply Chain Managementiin tuodut sähköiset laskut riippumatta kyseisten sähköisten laskujen rivien lukumäärästä.

- Laskenta:

    Vastaanotettu = Financeen ja Supply Chain Managementiin tuotujen sähköisten laskujen määrä.

## <a name="functions"></a>Funktiot
### <a name="purchase"></a>Osto

Valitse **Kuukausittainen käyttö (vienti)** -välilehdessä **Osto**, jos haluat rekisteröidä hankittujen lähetysten määrän manuaalisesti.

Valitse jollekin päivälle **Uusi** ja määritä tuona päivänä hankittujen **pakettien** määrä.

**Määrä** lasketaan seuraavasti:

Määrä = Paketit * 1 000

Laskettu **Määrä** vastaa **Ostettu**-arvoa **Käyttö kuukaudessa (vienti)** -mittarissa.

### <a name="update"></a>Päivitys

Päivitä laskelma ja päivitä sivulla ja kaaviossa näkyvät tiedot valitsemalla toimintoruudussa **Päivitä**.

### <a name="reset-history-data"></a>Palauta historiatiedot

Valitse toimintoruudussa **Nollaa historiatiedot** ja päivitä tietokanta, josta mittarit lasketaan.




> [!NOTE]
> **Käyttöhallinta**-koontinäyttö ei näytä rahasummia. Sen sijaan siinä näkyy vain laskettujen lähetysten ja tuotujen tiedostojen määrä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
