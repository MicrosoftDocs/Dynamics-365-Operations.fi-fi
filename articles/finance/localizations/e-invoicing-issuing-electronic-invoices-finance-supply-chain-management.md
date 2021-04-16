---
title: Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen kautta lähetetään sähköisiä laskuja Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: 8d6ef59b64a96e13bdc2e5ddf299ef7ab98e105c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840073"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Sähköisten laskujen luominen Financessa ja Supply Chain Managementissa

[!include [banner](../includes/banner.md)]

Tässä aiheessa selitetään, miten sähköisen laskutuksen kautta lähetetään sähköisiä laskuja Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.


## <a name="feature-activation"></a>Ominaisuuden aktivointi

Sähköisten laskujen lähettämiseksi sähköisen laskutuksen kautta on aktivoitava Financen ja Supply Chain Managementin toiminto.

Jokainen toiminto vastaa tiettyä sähköistä laskutustoimintoa, joka vastaa maan/alueen sähköisen laskutuksen vaatimuksia.

Seuraavassa taulukossa on luettelo toiminnoista, joita sähköinen laskutus tukee.

| Nimi                                              | Maa tai alue |
|---------------------------------------------------|----------------|
|Itävallan sähköinen lasku                        |Itävalta         |
|Belgian sähköinen lasku                         |Belgia         |
|NF-e Federal – Brasilian sähköinen lasku       |Brasilia          |
|NFS-e – Brasilian kaupungin sähköinen lasku|Brasilia          |
|Tanskan sähköinen lasku                          |Tanska         |
|Egyptin sähköinen lasku                        |Egypti           |
|Viron sähköinen lasku                        |Viro         |
|Suomen sähköinen lasku                         |Suomi         |
|Ranskan sähköinen lasku                          |Ranska          |
|Saksan sähköinen lasku                          |Saksa         |
|PEPPOL – yleinen sähköinen lasku                 |Yleinen          |
|Italian sähköinen lasku                         |Italia           |
|CFDI – Meksikon sähköinen lasku                  |Meksiko          |
|Hollannin sähköinen lasku                           |Alankomaat     |
|Norjan sähköinen lasku                       |Norja          |
|Espanjan sähköinen lasku                         |Espanja           |

Kun käytössä on vanha sähköinen laskutustoiminto, jota maan tai alueen maakohtainen laajuus tukee, yhden toiminnon aktivoiminen ottaa vanhan ominaisuuden pois käytöstä ja ottaa käyttöön sähköisten laskujen toimituksen sähköisen laskutuksen kautta.

> [!IMPORTANT]
> Kun sähköisen laskutuksen integrointiominaisuus on otettu käyttöön, uusi sähköinen laskutuskokemus on oletusarvon mukaan poissa käytöstä. Toimintokäsite mahdollistaa uusien kokemusten valikoivan käyttöönoton yrityksille, jotka käyttävät maa-/aluekohtaista toiminnallisuutta. **Yleinen**-vaihtoehto ohjaa muiden kuin taulussa lueteltujen maiden/alueiden uutta käyttökokemusta.

## <a name="submit-electronic-documents"></a>Lähetä sähköiset asiakirjat

Sähköisten asiakirjojen lähettämisen prosessi edustaa Financen ja Supply Chain Managementin sekä sähköisen laskutuksen välistä yhden yhteyspisteen viestintää. Viestintä kulkee kunkin lähetystapahtuman aikana molempiin suuntiin:

- **Financesta ja Supply Chain Managementista sähköiseen laskutukseen** – Finance ja Supply Chain Management lähettää abstraktit laskut sähköiseen laskutukseen. Tarvittaessa ohjelma lähettää myös niiden muuttujien sisällön, jotka on konfiguroitu osana sähköisen laskutuksen ominaisuuksia.
- **Sähköisestä laskutuksesta Financeen ja Supply Chain Managementiin** – Finance ja Supply Chain Management saa aiemmin lähetettyjen laskujen käsittelyn tuloksia koskevat päivitykset sähköisestä laskutuksesta sähköisen laskutuksen toiminnosta riippuen. Ne myös vastaanottavat niiden muuttujien sisällön, jotka on konfiguroitu osana sähköisen laskutuksen ominaisuuksia.

Sähköisten tiedostojen lähettäminen sähköiseen laskutukseen siirry Financessa ja Supply Chain Managementissa kohtaan **Organisaation hallinto &gt; Kausittainen &gt; Sähköiset asiakirjat &gt; Lähetä sähköiset asiakirjat**.

Lähtökohtana on kirjattu lasku. Lasku voi olla peräisin eri lähteistä, esimerkiksi myyntitilauksista, projektilaskuista tai vapaatekstilaskuista.

Lähetysprosessi voidaan suorittaa manuaalisesti tai taustalla.

- **Manuaalinen suoritus** – Manuaaliseen suoritukseen on käytettävä **Suodatus**-asetusta, kun määritetään toimitettavat tiedostot. Voit määrittää **Suodatus**-sivulla oman kyselysi valitsemaan kirjatut laskut, jotka on toimitettava. Kun valinta on tehty, käsittely on aloitettava manuaalisesti ja odotettava sen suorittamista. Kun käsittely on valmis, toimintokeskuksen sanomassa näkyy onnistuneesti lähetettyjen sähköisten tiedostojen määrä.
- **Suoritus taustalla** – Taustasuoritus suorittaa ilman, että sinun on kirjauduttava sisään tai pitää lähetysvalintaikkunaa avoinna. Voit ajoittaa suoritettavan prosessin ja määrittää suoritustiheyden.

## <a name="view-the-submission-logs"></a>Lähetyslokien tarkastelu

Financessa ja Supply Chain Managementissa voit lähetyslokien avulla tarkastella sähköiseen laskutukseen lähettämisen käsittelyn tuloksia. Siirry kohtaan **Organisaation hallinto &gt; Kausittainen &gt; Sähköiset asiakirjat &gt; ESähköisen asiakirjan lähetys** ja valitse sitten **Asiakirjatyyppi**-kentässä arvo, jola suodatetaan lokien näyttämien laskujen tyyppi.

Lähetystiloja voi olla kolme:

- **Ajoitettu** – Sähköinen laskutus vastaanotti lähetyksen Financesta ja Supply Chain Managementista, ja sähköisen laskutuksen toiminto on käynnissä.
- **Valmis** – Sähköinen laskutus on käsitellyt sähköisen laskutuksen ominaisuuden onnistuneesti siinä muodossa, jossa se on määritetty suoritettavaksi.
- **Epäonnistunut** – Sähköinen laskutus kohtasi virheen tai se pysäytettiin poikkeuksesta käsiteltäessä sähköistä laskutustoimintoa.

> [!IMPORTANT]
> Lähetyksen tila viittaa sen käsittelyn tilaan, jota sähköinen laskutus tekee sähköisessä laskutusominaisuudessa. Se ei viittaa itse sähköisen laskun lopulliseen tilaan.
>
> Jos esimerkiksi sähköinen lasku on toimitettava ulkoiseen verkkopalveluun hyväksyttäväksi, lähetyksen tila voi olla **Valmis**, mutta sähköisen laskun tila voi olla **Hylätty**. Tässä tapauksessa sähköinen laskutus pystyi käsittelemään sähköisen laskutuksen ominaisuuden onnistuneesti siinä muodossa, jossa se on määritetty käsittelemään kyseistä ominaisuutta. Sähköinen lasku on kuitenkin hylätty, koska se ei täytä laskun hyväksyntää varten määritetyn verkkopalvelun ehtoja.

Lähetyslokit sisältävät seuraavat lisätoiminnot:

- **Lähetystiedot** – Tarkastele päälähetyksen tietoja. Visualisoinnissa näkyy sähköisessä laskutusominaisuudessa konfiguroitujen toimintojen täydellinen suoritusloki. Lisäksi käyttäjät voivat ladata käsittelyn aikana luodut tiedostot. Jos ulkoisen verkkopalvelun on hyväksyttävä lasku, käyttäjät voivat tarkastella laskun tilaa.
- **Liittyvät lähetykset** – Tarkastele alilähetysten tietoja.
- **Peruuta lähetyksiä** – Tämä toiminto mahdollistaa erityisen lähetysprosessin tilanteissa, joissa ulkoisen verkkopalvelun on hyväksyttävä sähköinen lasku. Se ohjeistaa sähköistä laskutusta lähettämään verkkopalveluun tietyn sanoman, joka on tarkoitettu hyväksytyn sähköisen laskun tilan peruuttamiseen verkkopalvelun tietokannassa.
- **Lähetä asiakirja uudelleen** – Lähetä uudelleen sähköinen asiakirja, joka on jo lähetetty sähköiseen laskutukseen. **Lähetyksen tiedot** -sivulla luodaan uusi loki.
- **Lähetä liittyvä lähetys**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
