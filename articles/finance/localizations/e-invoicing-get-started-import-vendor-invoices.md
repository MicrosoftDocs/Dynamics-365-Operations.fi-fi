---
title: Toimittajan laskujen tuominen sähköisen laskutuspalvelun avulla
description: Tässä aiheessa on tietoja toimittajan laskujen toimisesta sähköisen laskutuspalvelun avulla.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751249"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Toimittajan laskujen tuominen sähköisen laskutuspalvelun avulla

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä aiheessa on tietoja, joiden avulla voidaan aloittaa toimittajan laskujen tuominen sähköisen laskutuspalvelun avulla. Aiheessa on ohjeet Regulatory Configuration Servicesin (RCS), Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin määrittämiseen, ja näitä ohjeita noudattamalla voidaan vastaanottaa toimittajan sähköisiä laskuja toimittajilta.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Toimittajan laskujen tuonnin määrittäminen RCS:ssä
Toimittajan laskun tuonti määritetään RCS:ssä seuraavasti:

1. Tutustu luetteloon [yleisesti saatavana olevista sähköisen laskutuksen ominaisuuksista](e-invoicing-configuration-rcs.md#generally-available-features).
2. Valitse ja tuo sähköisen laskutuksen ominaisuus. Lisätietoja on kohdassa [Sähköisen laskutusominaisuuden tuominen Microsoftin määrityspalvelusta](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Luo organisaatioon sähköinen laskutusominaisuus. Lisätietoja on kohdassa [Sähköisen laskutusominaisuuden luominen organisaatiopalveluun](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Sähköpostitilikanavan määrittäminen

Määritä sähköpostitilikanava, jos luotu sähköinen laskutusominaisuus tuo toimittajan sähköisiä laskuja sähköpostiin vastaanotetuista liitetiedostoista.

1. Valitse RCS:ssä luotu sähköinen laskutusominaisuus. Varmista, että valittavan version tila on **Luonnos**.
2. Valitse **Asetukset**-välilehden ruudukossa ominaisuusmääritys ja valitse sitten **Muokkaa**.
3. Valitse **Tietokanava**-välilehden **Parametrit**-kenttäryhmässä **Palvelimen osoite** ja anna sähköpostitilipalvelu.
4. Valitse **Palvelimen portti** ja anna sähköpostitilipalvelun käyttämä portti.
5. Valitse **Käyttäjänimen salaisuus** ja anna sen avainsäilön salaisen koodi nimi, joka sisältää sähköpostin käyttäjätilin tunnuksen.
6. Valitse **Käyttäjän salasanan salaisuus** ja anna sen avainsäilön salaisen koodi nimi, joka sisältää sähköpostin käyttäjätilin salasanan.
7. Valitse **Aihesuodatin**. Tarkista ja päivitä merkkijono, jonka sisältämällä sähköpostin oletusaiheella tunnistetaan tuotava toimittajan sähköinen lasku.
8. Tarkista ja päivitä ehdot tarvittaessa **Soveltuvuussäännöt**-välilehdessä. Lisätietoja on kohdassa [Soveltuvuussäännöt](e-invoicing-configuration-rcs.md#applicability-rules).
9. Valitse **Tallenna** ja sulje sivu.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Microsoft SharePoint -kanavan määrittäminen

Microsoft SharePoint -kanava määritetään, jos sähköinen laskutusominaisuus tuo toimittajan sähköisiä laskuja SharePoint-kansioihin sijoitetuista tiedostoista.

1. Valitse RCS:ssä luotu sähköinen laskutusominaisuus. Varmista, että valittavan **version** tila on **Luonnos**.
2. Valitse **Asetukset**-välilehden ruudukossa ominaisuusmääritys ja valitse sitten **Muokkaa**.
3. Valitse **Tietokanava**-välilehden **Parametrit**-kenttäryhmässä **SharePoint-osoite** ja anna SharePointin URL-osoite.
4. Valitse **Palvelimen portti** ja anna sähköpostitilipalvelun käyttämä portti.
5. Valitse **Sovelluksen tunnus** ja anna sen avainsäilön salaisen koodi nimi, joka sisältää SharePoint-asiakasohjelman tunnuksen.
6. Valitse **Sovelluksen salainen koodi** ja anna sen avainsäilön salaisen koodi nimi, joka sisältää SharePoint-asiakasohjelman salasanan.
7. Valitse **Tiedostosuodatin**. Tarkista ja päivätä peite suodattamaan tiedosto, joka sisältää toimittajan tuotavan sähköisen laskun.
8. Tarkista ja päivitä ehdot tarvittaessa **Soveltuvuussäännöt**-välilehdessä. Lisätietoja on kohdassa [Soveltuvuussäännöt](e-invoicing-configuration-rcs.md#applicability-rules).
9. Valitse **Tallenna** ja sulje sivu.

### <a name="deploy-an-electronic-invoicing-feature"></a>Sähköisen laskutusominaisuus ottaminen käyttöön

Lisätietoja sähköisen laskutusominaisuuden käyttöönotosta on kohdassa [Sähköisen laskutusominaisuuden ottaminen käyttöön palveluympäristössä](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Toimittajan laskun tuonnin määrittäminen Financessa ja Supply Chain Managementissa
Erityyppisten toimittajan laskujen tuonti määritetään seuraavassa kahdessa osassa annettujen ohjeiden avulla.

### <a name="import-vendor-invoices-from-email"></a>Toimittajan laskujen tuominen sähköpostista

1. Kirjaudu Finance- tai Supply Chain Management -ympäristöön ja varmista, että olet oikeassa yrityksessä.
2. Siirry kohtaan **Organisaation hallinta** > **Määritys** > **Sähköisten asiakirjojen parametrit**.
3. Varmista **Ominaisuudet**-välilehdessä, että **NF-e Federal – Brasilian sähköinen lasku** on valittu.
4. Valitse **Ulkoiset kanavat** -välilehden **Kanavat**-kenttäryhmässä **Lisää**.
5. Anna **Kanava**-kenttään **NFe** (sen kanavan nimi, joka on annettu tietokanavan määrityksessä RSC:n sähköisessä laskutusominaisuudessa).
6. Syötä **Kuvaus**-kenttään kuvaus. Valitse yritys kentässä **Yritys**.
7. Valitse **Asiakirjan konteksti** -kentässä **Veroasiakirjan konteksti – myyntilaskun kontekstimalli**.
8. Valitse **Tuontilähteet**-kenttäryhmässä **Lisää**.
9. Anna **Nimi**-kenttään **XmlFile** (sen **liitesuodattimen** nimi, joka on annettu tietokanavan määrityksessä RSC:n sähköisessä laskutusominaisuudessa).
10. Anna **Kuvaus**-kenttään kuvaus ja valitse **Tietoyksikön nimi** -kentässä **Vastaanotetut NF-e-XML-tiedostot**.
11. Valitse **Mallin määritys** -kentässä **NF-e-sähköpostin tuonti – NF-e-sähköpostin tuonti (BR)** ja valitse sitten **Tallenna**.
12. Valitse **Sähköinen asiakirja** -tiedoston **Sähköinen raportointi** -kenttäryhmässä **Lisää** ja **Taulukon nimi** -kentässä **Vastaanotettu NF-e-XML-asiakirja**.
13. Valitse **Asiakirjan konteksti** -kentässä **Veroasiakirjan kontekstikysely – myyntilaskun kontekstimalli**.
14. Valitse **Sähköisen asiakirjan mallin määritys**-kentässä **Määrityskysely – veroasiakirjan määritys**.
15. Valitse **Vastaustyypit** ja valitse sitten **Uusi**.
16. Anna **Vastaustyyppi**-kentässä **Vastaus**. Anna **Lähetystila**-kentässä **Ajastettu**.
17. Valitse **Mallin määritys** -kentässä **Mallin määritys vastaussanomasta – vastaussanoman tuontimuoto**.
18. Valitse **Tallenna** ja sulje sitten sivu.

### <a name="import-peppol-electronic-vendor-invoices"></a>Toimittajan sähköisten laskujen PEPPOL-tuonti

1. Valitse **sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
2. Valitse **Myyntilaskun kontekstimalli** ja luo johdettu määritys.
3. Valitse **Luonnos**-versiossa **Suunnitteluohjelma**.
4. Valitse **Tietomalli**-puussa **Myyntilasku** ja valitse sitten **Yhdistä malli tietolähteeseen**.
5. Valitse **Määritelmät**-puussa **CustomerInvoice** ja valitse sitten **Suunnitteluohjelma**.
6. Valitse **Tietolähteet**-puussa **Context\_Channel**. Valitse **Arvo**-kentässä **PEPPOL**. Tämä on sen kanavan nimi, joka on annettu tietokanavan määrityksessä RSC:n sähköisessä laskutusominaisuudessa. 
7. Valitse **Tallenna** ja sulje sivu.
8. Sulje sivu.
9. Valitse **Myyntilaskun kontekstimalli** ja valitse sitten **Versiot**-pikavälilehdessä **Muuta tila** > **Valmis**.
10. Valitse **Organisaation hallinta** > **Määritys** > **Sähköisen asiakirjan parametrit** ja varmista **Ominaisuudet**-välilehdessä, että **PEPPOL – yleinen sähköinen lasku** on valittu. 
11. Valitse **Ulkoiset kanavat** -välilehden **Kanavat**-kenttäryhmässä **Lisää**.
12. Anna **Kanava**-kenttään **PEPPOL**. Syötä **Kuvaus**-kenttään kuvaus.
13. Valitse yritys kentässä **Yritys**. Valitse **Asiakirjan konteksti** -kentässä **Myyntilaskun konteksti – myyntilaskun kontekstimalli**.
14. Valitse **Tallenna** ja sulje sitten sivu.


## <a name="receive-electronic-invoices"></a>Sähköisten laskujen vastaanottaminen
Sähköisiä laskuja vastanotetaan seuraavasti:

1. Valitse **Organisaation hallinta** > **Säännölliset** > **Sähköiset asiakirjat** > **Vastaanota sähköisiä asiakirjoja**.
2. Valitse **OK** ja sulje sitten sivu.

## <a name="view-receive-logs-for-electronic-invoices"></a>Sähköisten laskujen vastaanottolokien näyttäminen

Sähköisten laskujen vastaanottolokeja voi tarkastella valitsemalla **Organisaation hallinta** > **Säännölliset** > **Sähköiset asiakirjat** > **Sähköisen asiakirjan vastaanottoloki**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
