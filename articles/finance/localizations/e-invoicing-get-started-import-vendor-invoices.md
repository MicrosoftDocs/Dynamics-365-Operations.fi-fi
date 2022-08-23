---
title: Toimittajan laskujen tuominen sähköisen laskutuspalvelun avulla
description: Tässä artikkelissa on tietoja toimittajan laskujen toimisesta sähköisen laskutuspalvelun avulla.
author: gionoder
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: c98f33345b37a72c4099f01e37c82e27002ac687
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283142"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Toimittajan laskujen tuominen sähköisen laskutuspalvelun avulla

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä artikkelissa on tietoja, joiden avulla voidaan aloittaa toimittajan laskujen tuominen sähköisen laskutuspalvelun avulla. Aiheessa on ohjeet Regulatory Configuration Servicesin (RCS), Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin määrittämiseen, ja näitä ohjeita noudattamalla voidaan vastaanottaa toimittajan sähköisiä laskuja toimittajilta.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Toimittajan laskujen tuonnin määrittäminen RCS:ssä
Toimittajan laskun tuonti määritetään RCS:ssä seuraavasti:

1. Tutustu luetteloon [yleisesti saatavana olevista sähköisen laskutuksen ominaisuuksista](e-invoicing-configuration-rcs.md#generally-available-features).
2. Valitse ja tuo sähköisen laskutuksen ominaisuus. Lisätietoja on kohdassa [Sähköisen laskutusominaisuuden tuominen Microsoftin määrityspalvelusta](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Luo organisaatioon sähköinen laskutusominaisuus. Lisätietoja on kohdassa [Sähköisen laskutusominaisuuden luominen organisaatiopalveluun](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Sähköpostitilikanavan määrittäminen

Määritä sähköpostitilikanava, jos luotu sähköinen laskutusominaisuus tuo toimittajan sähköisiä laskuja sähköpostiin vastaanotetuista liitetiedostoista.

1. Valitse RCS:ssä luotu sähköinen laskutusominaisuus. Varmista, että valittavan version tila on **Luonnos**.
2. Valitse **Asetukset**-välilehden ruudukossa ominaisuusmääritys ja valitse sitten **Muokkaa**.
3. Anna kanavan nimi **Tietokanava**-välilehden **Parametrit**-kenttäryhmän **Tietokanava**-kentässä. Kanavan nimi saa olla enintään 10 merkin pituinen.
4. Kirjoita **Palvelimen osoite** -kenttään sähköpostitilin tarjoajan nimi. Esimerkiksi palvelun **https://outlook.live.com/** palvelinosoite on **imap-mail.outlook.com**.
5. Anna **Palvelimen portti** -kentässä sähköpostitilipalvelun käyttämä portti. Esimerkiksi palvelun **https://outlook.live.com/** palvelimen portti on **993**.
6. Anna **Käyttäjänimen salainen koodi** -kentässä sen avainsäilön salaisen koodi nimi, joka sisältää sähköpostin käyttäjätilin tunnuksen. Salaisen koodin täytyy olla luotu Azure Key Vaultissa ja määritetty palveluympäristössäsi. 
7. Anna **Käyttäjäsalasanan salainen koodi** -kentässä sen avainsäilön salaisen koodi nimi, joka sisältää sähköpostin käyttäjätilin salasanan.
8. Valinnainen – Kirjoita arvot kenttiin **Lähettäjäsuodatin**, **Aihesuodatin** ja **Päivämääräsuodatin**.
9. Kirjoita niiden postilaatikkokansioiden nimet, jossa sähköpostiviestejä tulee olemaan:

    - Tuotu kohteesta: **Pääkansio**
    - Tallennettu onnistuneen käsittelyn jälkeen: **Arkistokansio**
    - Tallennettu onnistuneen käsittelyn jälkeen: **Virhekansio** Näitä kansioita ei tarvitse luoda postilaatikossa. Kansiot luodaan automaattisesti ensimmäisen sähköisen laskun tuonnin ja käsittelyn jälkeen. 
   
10. Lisää tiedostojen suodatustiedot **Liitesuodatin**-kenttäryhmään. Vain määritetyn suodattimen täyttävät liitteet käsitellään. Voit esimerkiksi tehdä määrityksen \*.xml liitteille, joiden tiedostotunniste on xml. Liitteen nimeä käytetään määrityksen aikana Dynamics 365 Financessa tai Dynamics 365 Supply Chain Managementissa. 
11. Tarkista ja päivitä ehdot tarvittaessa **Soveltuvuussäännöt**-välilehdessä. **Kanava**-kentän on oltava sama kuin aiemmin annettu **Tietokanava**. Lisätietoja on kohdassa [Soveltuvuussäännöt](e-invoicing-configuration-rcs.md#applicability-rules).
12. Valitse **Tallenna** ja sulje sivu.

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

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Toimittajan laskun tuonnin määrittäminen Financessa tai Supply Chain Managementissa
Erityyppisten toimittajan laskujen tuonti määritetään seuraavassa kahdessa osassa annettujen ohjeiden avulla.

### <a name="import-brazilian-nf-e-from-email"></a>Brasilialaisen NF-e-lomakkeen tuonti sähköpostista

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
2. Luo johdettu määritys valitsemalla **Asiakaslaskun kontekstimalli** ja sitten **Luo määritys** > **Johda nimestä: Asiakaslaskun kontekstimalli, Microsoft**.
3. Valitse **Luonnos**-versiossa **Suunnitteluohjelma** ja **Tietomalli**-puussa **Yhdistä malli tietolähteeseen**.
4. Valitse **Määritelmät**-puussa **DataChannel** ja valitse sitten **Suunnitteluohjelma**.
5. Laajenna **Tietolähteet**-puussa kontti **$Context\_Kanava**. Valitse **Arvo**-kentässä **Muokkaa** ja anna tietokanavan nimi. Tämä on sen kanavan nimi, joka on annettu tietokanavan määrityksessä RSC:n sähköisessä laskutusominaisuudessa. 
7. Valitse **Tallenna** ja sulje sivu.
8. Sulje sivu.
9. Valitse johdettu määritys, jonka olet juuri luonut **Asiakaslaskun kontekstimalli** -arvon perusteella, ja **Versiot**-pikavälilehdessä **Muuta tilaa** > **Valmis**.
10. Valitse **Organisaation hallinta** > **Määritys** > **Sähköisen asiakirjan parametrit** ja varmista **Ominaisuudet**-välilehdessä, että **PEPPOL – yleinen sähköinen lasku** on valittu. 
11. Valitse **Ulkoiset kanavat** -välilehden **Kanavat**-kenttäryhmässä **Lisää**.
12. Anna **Kanava**-kentässä tietokanavan nimi ja **Kuvaus**-kentässä kuvaus.
13. Valitse yritys kentässä **Yritys**. 
14. Valitse **Asiakirjan konteksti**-kentässä uusi johdettu määritys kohdasta **Asiakaslaskun kontekstimalli**. Yhdistämismäärityksen kuvauksen pitäisi olla **Tietokanavakonteksti**.
15. Valitse **Tuontilähteet**-kenttäryhmässä **Lisää**.
16. Kirjoita **Nimi**-kenttään **Liitesuodattimen nimi** ja **Tietoyksikön nimi**-kentässä valitse **Toimittajan laskutusotsikko**.
17. Valitse **Malliyhdistämismääritys**-kentässä **Toimittajalaskun tuonti – tuo toimittajalasku**.
18. Valitse **Tallenna** ja sulje sitten sivu.


## <a name="receive-electronic-invoices"></a>Sähköisten laskujen vastaanottaminen

Sähköinen laskutuspalvelu suorittaa kaksi vaihetta laskujen tietokanavista tuonnissa:

1. Käyttää postilaatikkoa ja lukee sähköpostia.
2. Käsittelee sähköpostiviestit. 
    
Näiden kahden vaiheen suorittamista varten asiakasohjelman pitäisi kutsua palvelua manuaalisesti kunkin vaiheen osalta. On kuitenkin suositeltavaa määrittää erä sähköisten tiedostojen vastaanottamista varten.

Sähköisiä laskuja vastanotetaan seuraavasti:

1. Valitse **Organisaation hallinta** > **Säännölliset** > **Sähköiset asiakirjat** > **Vastaanota sähköisiä asiakirjoja**.
2. Valitse **OK** ja sulje sitten sivu.


## <a name="view-receive-logs-for-electronic-invoices"></a>Sähköisten laskujen vastaanottolokien näyttäminen

Sähköisten laskujen vastaanottolokeja voi tarkastella valitsemalla **Organisaation hallinta** > **Säännölliset** > **Sähköiset asiakirjat** > **Sähköisen asiakirjan vastaanottoloki**.
Jos et näe onnistuneesti käsiteltyjä laskuja, poista taulukkosuodatin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
