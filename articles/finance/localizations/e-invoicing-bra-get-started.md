---
title: Brasilian sähköisen laskutuksen käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa Brasilian sähköisen laskutuksen käytön Financessa ja Supply Chain Managementissa.
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
ms.openlocfilehash: f8caaa6417365a131da0565cbc4a9f79425d0c7e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840265"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Brasilian sähköisen laskutuksen käytön aloittaminen 

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja, joiden avulla voit aloittaa Brasilian sähköisen laskutuksen käytön. Ohjeaihe ohjaa sinua niissä konfigurointivaiheissa, jotka ovat maa-/aluekohtaisia Regulatory Configuration Services (RCS) -palveluissa ja täydentävät seuraavassa ohjeaiheessa kuvattuja vaiheita: [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Sähköisen laskutuksen maakohtainen konfigurointi Brasilian NF-e (BR) – sähköinen laskutus -ominaisuudelle

Osa **Brasilian NF-e (BR) – sähköinen laskutus** -ominaisuuden parametreista julkaistaan oletusarvoilla. Tarkista ja päivitä tarvittaessa arvot liiketoimintasi tarpeisiin sopivaksi, ennen kuin otat sähköisen laskutuksen käyttöön ominaisuuden palveluympäristössä.

Tämä os täydentää **Sähköisen laskutuksen maa-/aluekohtainen konfigurointi sähköisen laskutuksen ominaisuudelle** -osaa ohjeaiheessa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

1. Valitse RCS:ssä **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
2. Varmista **Sähköisen laskutuksen ominaisuudet** -sivulla, että luomasi sähköisen laskutuksen **Brasilian NF-e (BR)** -ominaisuus on valittuna.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
4. Valitse **Asetukset**-välilehden ruudukosta **Lähetä** ja valitse sitten **Muokkaa**.
5. Valitse **Toiminnot**-välilehden **Toiminnot**-kenttäryhmästä **(Esiversio) Allekirjoita XML-tiedosto** -toiminto.
6. Valitse **Parametrit**-kenttäryhmässä **Varmenteen nimi** ja kirjoita **Arvo**-kenttään avainsäilön parametriin liittyvän varmenteen nimi.
7. Valitse **Toiminnot**-välilehden **Toiminnot**-kenttäryhmästä **(Esiversio) Kutsu Brasilian SEFAZ-palvelua** -toiminto.
8. Valitse **Parametrit**-kenttäryhmästä **URL-osoite**-parametri.
9. Tarkista ja päivitä tarvittaessa **Arvo**-kentässä osavaltiosi SEFAZ-dokumentaatiossa julkaisemien Internet-palveluiden URL-osoite ja valitse sitten **Tallenna**.
10. Tarkista ja päivitä **Sovellettavuussäännöt**-välilehden **Sovellettavuussäännön määritys** -kenttäryhmän **Osavaltio**-kentän ehdot tarpeen mukaan samalle osavaltiolle, johon Internet-palveluiden URL-osoitteessa viitataan.
11. Valitse **Tallenna** ja sulje sivu.
12. Lisätietoja sähköisen laskutuksen ominaisuuden käyttöönotosta palveluympäristössä on kohdassa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Sovellusmäärityksen sähköisen laskutuksen maakohtainen konfigurointi Brasilian NF-e (BR) – sähköinen laskutus -ominaisuudelle

Suorita nämä vaiheet, ennen kuin otat sovelluksen määritykset käyttöön yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa.

Tämä os täydentää **Sovellusetusten maa-/aluekohtainen konfigurointi** -osaa ohjeaiheessa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

1. Valitse RCS:ssä **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus* -ruutu.
2. Varmista **Sähköisen laskutuksen ominaisuudet** -sivulla, että sähköisen laskutuksen **Brasilian NF-e (BR)** -ominaisuus on valittuna.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
4. Valitse **Asetukset**-välilehden **Sovelluksen asetukset** -vaihtoehto ja valitse **Yhdistetty sovellus** -kentästä sovellus, jossa haluat ottaa käyttöön.
5. Tarkista **Taulukon nimi** -kentässä, onko **Veroasiakirjan otsikko** valittuna.
6. Valitse **Vastaustyypit** ja valitse sitten **Uusi**.
7. Kirjoita **Vastaustyyppi**-kenttään "Response" kiinteänä arvona ja kirjoita **Kuvaus**-kenttään "Description".
8. Valitse **Lähetystila**-kentässä **Odottaa**.
9. Valitse **Mallin yhdistämismääritys** -kentässä **Mallin yhdistämismääritys vastaussanomasta** ja **(Esiversio) Vastaussanoman tuontimuoto** ja valitse sitten **Tallenna**.
10. Valitse **Uusi** ja kirjoita **Vastaustyyppi**-kenttään "ResponseData" kiinteänä arvona ja kirjoita **Kuvaus**-kenttään "Description".
11. Valitse **Lähetystila**-kentässä **Odottaa**.
12. Valitse **Mallin yhdistämismääritys** -kentässä **Vastaustietojen tuonti** ja **(Esiversio) NFe-vastaustietojen tuontimuoto (BR)** ja valitse sitten **Tallenna**.
13. Jos haluat ottaa sovelluksen asetukset käyttöön yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa, katso ohjetta [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Sähköisen laskutuksen maakohtainen konfigurointi Brasilian NFS-e ABRASF Curitiba (BR) – sähköinen laskutus -ominaisuudelle

Osa **Brasilian NFS-e ABRASF Curitiba (BR) – sähköinen laskutus** -ominaisuuden parametreista julkaistaan oletusarvoilla. Tarkista ja päivitä tarvittaessa arvot liiketoimintasi tarpeisiin sopivaksi, ennen kuin otat sähköisen laskutuksen käyttöön ominaisuuden palveluympäristössä.

Tämä os täydentää **Sähköisen laskutuksen maa-/aluekohtainen konfigurointi sähköisen laskutuksen ominaisuudelle** -osaa ohjeaiheessa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

1. Valitse RCS:ssä **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
2. Varmista **Sähköisen laskutuksen ominaisuudet** -sivulla, että luomasi sähköisen laskutuksen **Brasilian NFS-e ABRASF Curitiba (BR)** -ominaisuus on valittuna.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittu ja valitse **Asetukset**-välilehden ruudukosta **Lähetä**.
4. Valitse **Muokkaa** ja valitse **Toiminnot**-välilehden **Toiminnot**-kenttäryhmästä **(Esiversio) Allekirjoita XML-tiedosto** -toiminnon ensimmäinen esiintymä.
5. Valitse **Parametrit**-kenttäryhmästä **Varmenteen nimi**.
6. Kirjoita **Arvo**-kenttään avainsäilöparametreihin liittyvän varmenteen nimi.
7. Valitse **Toiminnot**-kenttäryhmästä toinen **(Esiversio) Allekirjoita XML-tiedosto** -esiintymä.
8. Valitse **Parametrit**-kenttäryhmästä **Varmenteen nimi**.
9. Kirjoita **Arvo**-kenttään avainsäilöparametreihin liittyvän varmenteen nimi.
10. Valitse **Toiminnot**-välilehden **Toiminnot**-kenttäryhmästä **(Esiversio) Kutsu Brasilian SEFAZ-palvelua** -toiminto.
11. Valitse **Parametrit**-kenttäryhmästä **URL-osoite**-parametri.
12. Tarkista ja päivitä tarvittaessa **Arvo**-kentässä osavaltiosi Curitiban kaupungin vero-osaston julkaisemien Internet-palveluiden URL-osoite ja valitse sitten **Tallenna**.
13. Valitse **Asetukset**-välilehden ruudukosta **Kohdista kysely** ja valitse sitten **Muokkaa**.
14. Valitse **Toiminnot**-välilehden **Toiminnot**-kenttäryhmästä **(Esiversio) Kutsu Brasilian SEFAZ-palvelua** -toiminto.
15. Valitse **Parametrit**-kenttäryhmästä **URL-osoite**-parametri.
16. Tarkista ja päivitä tarvittaessa **Arvo**-kentässä osavaltiosi Curitiban kaupungin vero-osaston julkaisemien Internet-palveluiden URL-osoite.
17. Valitse **Tallenna** ja sulje sitten sivu.
18. Lisätietoja sähköisen laskutuksen ominaisuuden käyttöönotosta palveluympäristössä on kohdassa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Sovellusmäärityksen sähköisen laskutuksen maakohtainen konfigurointi Brasilian NFS-e ABRASF Curitiba (BR) – sähköinen laskutus -ominaisuudelle

Suorita nämä vaiheet, ennen kuin otat sovelluksen määritykset käyttöön yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa.

Tämä os täydentää **Sovellusetusten maa-/aluekohtainen konfigurointi** -osaa ohjeaiheessa [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

1. Valitse RCS:ssä **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
2. Varmista **Sähköisen laskutuksen ominaisuudet** -sivulla, että sähköisen laskutuksen **Brasilian NFS-e ABRASF Curitiba (BR)** -ominaisuus on valittuna.
3. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittu ja valitse **Asetukset**-välilehdestä **Sovellusmääritys**.
4. Valitse **Yhdistetty sovellus** -kentästä sovellus, jossa haluat ottaa käyttöön.
5. Tarkista **Taulukon nimi** -kentässä, onko veroasiakirjan otsikko valittuna.
6. Valitse **Vastaustyypit** ja valitse **Uusi**.
7. Kirjoita **Vastaustyyppi**-kenttään "ABRASFCuritibaSubmitResponse" kiinteänä arvona ja kirjoita **Kuvaus**-kenttään "Description".
8. Valitse **Lähetystila**-kentässä **Odottaa**.
9. Valitse **Mallin yhdistämismääritys** -kentässä **Vastausviestien tuonti** ja **(Esiversio) NFS-e ABRASF Curitiba -vastausviestien tuonti (BR)** ja valitse sitten **Tallenna**.
10. Valitse **Uusi** ja kirjoita **Vastaustyyppi**-kenttään "ABRASFCuritibaSubmitResponseData" kiinteänä arvona ja kirjoita **Kuvaus**-kenttään "Description".
11. Valitse **Lähetystila**-kentässä **Odottaa**.
12. Valitse **Mallin yhdistämismääritys** -kentässä **Vastaustietojen tuonti** ja **(Esiversio) NFS-e ABRASF -vastaustietojen tuontimuoto (BR)** ja valitse sitten **Tallenna**.
13. Valitse **Uusi** ja kirjoita **Vastaustyyppi**-kenttään "ABRASFCuritibaInquireResponse" kiinteänä arvona ja kirjoita **Kuvaus**-kenttään "Description".
14. Valitse **Lähetystila**-kentässä **Odottaa**.
15. Valitse **Mallin yhdistämismääritys** -kentässä **Vastausviestien tuonti** ja **(Esiversio) NFS-e ABRASF Curitiba -vastausviestien tuonti (BR)**.
16. Valitse **Tallenna** ja sulje sivu.
17. Jos haluat ottaa sovelluksen asetukset käyttöön yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa, katso ohjetta [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Tietosuojatiedot
**NF-e Federal - Brasilian sähköinen lasku (BR)**- ja **NFS-e - Brasilian palvelun (kaupunki) sähköinen lasku** -ominaisuuksien ottaminen käyttöön saattaa edellyttää rajoitettujen tietojen lähettämistä, mukaan lukien organisaation verorekisteröintitunnus. Tiedot välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten siinä esimääritetyssä muodossa, jota integrointi valtion verkkopalveluun edellyttää. Järjestelmänvalvojana voit ottaa käyttöön tai poistaa käytöstä **NF-e Federal - Brasilian sähköinen lasku (BR)**- ja **NFS-e - Brasilian palvelun (kaupunki) sähköinen lasku** -ominaisuuden. Toimi seuraavasti: 

1. Siirry kohtaan **Organisaation hallinta** > **Määritys** > **Sähköisten asiakirjojen parametrit**. 
2. Valitse **Ominaisuudet**-välilehdestä rivi, joka sisältää **NF-e Federal - Brasilian sähköinen lasku (BR)** or the **NFS-e - Brasilian palvelun (kaupunki) sähköinen lasku** -ominaisuuden ja valitse ominaisuus. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md)
- [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
