---
title: Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen lisäosan kautta lähetetään sähköisiä laskuja Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104374"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä aiheessa selitetään, miten sähköisen laskutuksen lisäosan kautta lähetetään sähköisiä laskuja Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.


## <a name="feature-activation"></a>Ominaisuuden aktivointi

Sähköisten laskujen lähettämisen aloittaminen sähköisen laskutuksen lisäosan kautta on aktivoitava Financen ja Supply Chain Managementin toimintoviite.

Jokainen toimintoviite vastaa tiettyä sähköistä laskutustoimintoa, joka vastaa maan/alueen sähköisen laskutuksen vaatimuksia.

Seuraavassa taulukossa on luettelo toimintoviitteistä, joita sähköisen laskutuksen lisäosa tukee.

| Ominaisuuden viite | Nimi                                              | Maa tai alue |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e Federal – Brasilian sähköinen lasku       | Brasilia         |
| BR-00095          | NFS-e Brasilian sähköiset laskut               | Brasilia         |
| DK-00001          | Sähköinen laskutus julkiselle sektorille (OIOUBL) – DK    | Tanska        |
| EG-00008          | Egyptin e-laskutus                             | Egypti          |
| ES-00025          | Sähköinen lasku julkiselle sektorille           | Espanja          |
| EUR-00023         | Euroopan unionin sähköinen laskutus julkiselle sektorille       | Eurooppa         |
| ITA-00036         | IT – Sähköinen laskutus julkiselle sektorille (FatturaPA) | Italia          |
| MX-00010          | Sähköisen laskutuksen CFDI                                  | Meksiko         |
| MX-00016          | Sähköisen laskutuksen CFDI – peruutusprosessi           | Meksiko         |

Kun käytössä on vanha sähköinen laskutustoiminto, jota maan tai alueen maakohtainen laajuus tukee, toimintoviittauksen aktivoiminen ottaa käyttöön sähköisten laskujen toimituksen sähköisen laskutuksen lisäosan kautta ja ottaa vanhan ominaisuuden pois käytöstä.

## <a name="submit-electronic-documents"></a>Lähetä sähköiset asiakirjat

Sähköisten asiakirjojen lähettämisen prosessi edustaa Financen ja Supply Chain Managementin sekä sähköisen laskutuksen lisäosan välistä yhden yhteyspisteen viestintää. Viestintä kulkee kunkin lähetystapahtuman aikana molempiin suuntiin:

- **Financesta ja Supply Chain Managementista sähköisen laskutuksen lisäosaan** – Finance ja Supply Chain Management lähettää abstraktit laskut sähköiseen laskutuksen lisäosaan. Tarvittaessa ohjelma lähettää myös niiden muuttujien sisällön, jotka on konfiguroitu osana sähköisen laskutuksen ominaisuuksia.
- **Sähköisen laskutuksen lisäosasta Financeen ja Supply Chain Managementiin** – Finance ja Supply Chain Management saa aiemmin lähetettyjen laskujen käsittelyn tuloksia koskevat päivitykset sähköisen laskutuksen lisäosasta sähköisen laskutuksen toiminnosta riippuen. Ne myös vastaanottavat niiden muuttujien sisällön, jotka on konfiguroitu osana sähköisen laskutuksen ominaisuuksia.

Sähköisten tiedostojen lähettäminen sähköisen laskutuksen lisäosaan: siirry Financessa ja Supply Chain Managementissa kohtaan **Organisaation hallinto &gt; Kausittainen &gt; Sähköiset asiakirjat &gt; Lähetä sähköiset asiakirjat**.

Lähtökohtana on kirjattu lasku. Lasku voi olla peräisin eri lähteistä, esimerkiksi myyntitilauksista, projektilaskuista tai vapaatekstilaskuista.

Lähetysprosessi voidaan suorittaa manuaalisesti tai taustalla.

- **Manuaalinen suoritus** – Manuaaliseen suoritukseen on käytettävä **Suodatus**-asetusta, kun määritetään toimitettavat tiedostot. Voit määrittää **Suodatus**-sivulla oman kyselysi valitsemaan kirjatut laskut, jotka on toimitettava. Kun valinta on tehty, käsittely on aloitettava manuaalisesti ja odotettava sen suorittamista. Kun käsittely on valmis, toimintokeskuksen sanomassa näkyy onnistuneesti lähetettyjen sähköisten tiedostojen määrä.
- **Suoritus taustalla** – Taustasuoritus suorittaa ilman, että sinun on kirjauduttava sisään tai pitää lähetysvalintaikkunaa avoinna. Voit ajoittaa suoritettavan prosessin ja määrittää suoritustiheyden.

## <a name="view-the-submission-logs"></a>Lähetyslokien tarkastelu

Financessa ja Supply Chain Managementissa voit lähetyslokien avulla tarkastella sähköisen laskutuksen lisäosaan lähettämisen käsittelyn tuloksia. Siirry kohtaan **Organisaation hallinto &gt; Kausittainen &gt; Sähköiset asiakirjat &gt; ESähköisen asiakirjan lähetys** ja valitse sitten **Asiakirjatyyppi**-kentässä arvo, jola suodatetaan lokien näyttämien laskujen tyyppi.

Lähetystiloja voi olla kolme:

- **Ajoitettu** – Sähköisen laskutuksen lisäosa vastaanotti lähetyksen Financesta ja Supply Chain Managementista, ja sähköisen laskutuksen toiminto on käynnissä.
- **Valmis** – Sähköisen laskutuksen lisäosa on käsitellyt sähköisen laskutuksen ominaisuuden onnistuneesti siinä muodossa, jossa se on määritetty suoritettavaksi.
- **Epäonnistunut** – Sähköisen laskutuksen lisäosa kohtasi virheen tai se pysäytettiin poikkeuksesta käsiteltäessä sähköistä laskutustoimintoa.

> [!IMPORTANT]
> Lähetyksen tila viittaa sen käsittelyn tilaan, jota sähköisen laskutuksen lisäosa tekee sähköisessä laskutusominaisuudessa. Se ei viittaa itse sähköisen laskun lopulliseen tilaan.
>
> Jos esimerkiksi sähköinen lasku on toimitettava ulkoiseen verkkopalveluun hyväksyttäväksi, lähetyksen tila voi olla **Valmis**, mutta sähköisen laskun tila voi olla **Hylätty**. Tässä tapauksessa sähköisen laskutuksen lisäosa pystyi käsittelemään sähköisen laskutuksen ominaisuuden onnistuneesti siinä muodossa, jossa se on määritetty käsittelemään kyseistä ominaisuutta. Sähköinen lasku on kuitenkin hylätty, koska se ei täytä laskun hyväksyntää varten määritetyn verkkopalvelun ehtoja.

Lähetyslokit sisältävät seuraavat lisätoiminnot:

- **Lähetystiedot** – Tarkastele päälähetyksen tietoja. Visualisoinnissa näkyy sähköisessä laskutusominaisuudessa konfiguroitujen toimintojen täydellinen suoritusloki. Lisäksi käyttäjät voivat ladata käsittelyn aikana luodut tiedostot. Jos ulkoisen verkkopalvelun on hyväksyttävä lasku, käyttäjät voivat tarkastella laskun tilaa.
- **Liittyvät lähetykset** – Tarkastele alilähetysten tietoja.
- **Peruuta lähetyksiä** – Tämä toiminto mahdollistaa erityisen lähetysprosessin tilanteissa, joissa ulkoisen verkkopalvelun on hyväksyttävä sähköinen lasku. Se ohjeistaa sähköistä laskutusta lähettämään verkkopalveluun tietyn sanoman, joka on tarkoitettu hyväksytyn sähköisen laskun tilan peruuttamiseen verkkopalvelun tietokannassa.
- **Lähetä asiakirja uudelleen** – Lähetä uudelleen sähköinen asiakirja, joka on jo lähetetty sähköisen laskutuksen lisäosaan. **Lähetyksen tiedot** -sivulla luodaan kokonaan uusi loki.
- **Lähetä liittyvä lähetys**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]