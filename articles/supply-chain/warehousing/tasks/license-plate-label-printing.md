---
title: Rekisterikilven etiketin tulostuksen ottaminen käyttöön
description: Tässä aiheessa näytetään, miten sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd79abfc1029c4e0ef41d0e9b0f33ff524f50e36b70cf4fa3ed50dcdc4cb7f03
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751669"
---
# <a name="enable-license-plate-label-printing"></a>Rekisterikilven etiketin tulostuksen ottaminen käyttöön

[!include [banner](../../includes/banner.md)]

Tässä aiheessa näytetään, miten sarjatoimitusyksikkökoodin (SSCC) etiketti voidaan tulostaa automaattisesti varastosta viimeksi kerätyn nimikkeen jälkeen myynnin keräystyöprosessissa. Voit suorittaa tämän menettelyn esittely-yrityksessä USMF. Jos suoritit menettelyn omien tietojen avulla, rekisterikilville on määritettävä numerosarja. Määritä etikettitulostin, ennen kuin aloitat tämän tehtävän. Valitse Organisaation hallinta > Asetukset > Verkkotulostimet. Valitse toimintoruudussa Asetukset ja valitse sitten Lataa asiakirjan reititysagentin asennusohjelma -painike. Suorita asennusohjelma ja varmista, että toimiva verkkotulostin on määritetty aktiiviseksi, ennen kuin jatkat.


## <a name="set-up-the-gs1-company-prefix"></a>Yrityksen GS1-etuliitteen määrittäminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varastonhallinnan parametrit**.
2. Syötä **yrityksen GS1-etuliite** -kenttään GS1-yritysnumeron 7 numeroa.
3. Valitse **Tallenna**.
4. Sulje sivu.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SSCC-rekisterinumeron järjestyksen määrittäminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Organisaation hallinta > Numerosarjat > Numerosarjat**.
2. Valitse **Alue**-kentässä vaihtoehto.
3. Valitse **Viite**-kentässä vaihtoehto.
4. Kirjoita arvo **Yritys**-kenttään.
5. Laajenna **Segmentit**-osa.
6. Valitse **Muokkaa**.
7. Valitse **Segmentit**-taulukon ensimmäinen rivi.
8. Valitse **Poista**.
9. Valitse **Poista**.
10. Valitse **Tallenna**.
11. Sulje sivu.

## <a name="create-the-document-route-layout"></a>Asiakirjan reittiasettelun luominen
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta >> Asetukset > Asiakirjan reititys > Asiakirjan reititysasettelut**. Ota SSCC-asettelu käyttöön.  
2. Valitse **Uusi**.
3. Kirjoita **Asettelun tunnus** -kenttään arvo.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Lisää tekstin loppuun**.
6. Valitse **Tallenna**.
7. Sulje sivu.

## <a name="set-up-the-document-routing"></a>Asiakirjan reitityksen määrittäminen
1. Valitse **Siirtymisruutu > Moduulit > Varastonhallinta >> Asetukset > Asiakirjan reititys > Asiakirjan reititys**.
2. Valitse **Työtilauksen tyyppi** -kentässä vaihtoehto.
3. Valitse **Uusi**.
4. Kirjoita arvo **Varasto**-kenttään.
5. Kirjoita arvo **Nimi**-kenttään.
6. Valitse **Uusi**.
7. Syötä tai valitse arvo **Asettelun tunnus** -kenttään.
8. Valitse **Nimi**-kentästä tulostin, jota haluat käyttää.
9. Valitse **Tallenna**.
10. Sulje sivu.

## <a name="create-mobile-device-menu"></a>Mobiililaitteen valikon luominen
1. Siirry siirtymisruudussa kohtaan **Moduulit > Varastonhallinta > Asetukset > mobiililaite > Mobiililaitteen valikkovaihtoehdot**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Valikkovaihtoehdon nimi** -kenttään.
4. Kirjoita **Otsikko**-kenttään arvo.
5. Valitse **Tapa**-kentässä vaihtoehto.
6. Valitse **Käytä nykyistä työtä** -kentässä **Kyllä**.
7. Valitse **Muodosta rekisterikilpi** -kentässä **Kyllä**.
8. Laajenna **Työluokat**-osa.
9. Valitse **Uusi**.
10. Kirjoita **Työluokan tunnus** -kenttään arvo.
11. Valitse **Tallenna**.
12. Sulje sivu.
13. Siirry siirtymisruudussa kohtaan **Moduulit > Varastonhallinta > Asetukset > mobiililaite > Mobiililaitteen valikko**.
14. Valitse puusta aiemmin luotu valikkovaihtoehto.
15. Valitse **Muokkaa**.
16. Lisää valikkovaihtoehto valikkoon nuolen avulla.
17. Valitse **Tallenna**.
18. Sulje sivu.

## <a name="update-a-work-template"></a>Työmallin päivittäminen
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Työ > Työmallit**.
2. Valitse **Muokkaa**.
3. Valitse **Uusi**.
4. Valitse **Työtyyppi**-kentässä **Tulosta**.
5. Syötä tai valitse arvo **Työluokan tunnus** -kenttään.
6. Valitse **Siirrä ylös**.
7. Valitse **Tallenna**.
8. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]