---
title: Sähköinen laskutus – usein kysytyt kysymykset
description: Tässä ohjeaiheessa on tietoja sähköistä laskutusta koskevista usein kysytyistä kysymyksistä.
author: gionoder
ms.date: 03/17/2021
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
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 41cddcdad5043ec314a94dda67f4f2e9de406cac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840169"
---
# <a name="electronic-invoicing-faq"></a>Sähköinen laskutus – usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on vastauksia sähköistä laskutusta koskeviin usein kysyttyihin kysymyksiin. Sähköinen laskutus laajentaa Dynamics 365 Financen, Dynamics 365 Supply Chain Managementin ja Dynamics 365 Project Operationsin sähköisen laskutuksen ominaisuuksia. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Mikä on tärkeää sähköisessä laskutuksessa ja miksi se on tärkeää organisaatiolleni?

Toiminnan monimutkaisuus ja riskit kasvavat edelleen, kun organisaatiot laajentavat toimintaansa alueiden välillä. Yhteensopivuuden ylläpitäminen ja mukautuminen usein muuttuviin määräyksiin on kasavava haaste, ja se on erityisen tärkeää laskutettaessa. Laskutus on ollut perinteisesti kallista ja virhealtista, kun yritykset ovat riippuvaisia paperiasiakirjoista ja manuaalisista prosesseista.  

Organisaatiot ovat alkaneet siirtyä pois paperilaskuista kustannusten ja päästä päähän -prosessin nopeuttamiseksi. Julkishallinnon organisaatiot ovat siirtymässät sähköisen laskutuksen käyttöön verotuksen digitalisoinnin osana. Kun organisaatioiden edellytetään lähettävän digitaalisesti reaaliaikaisia verotietoja veroviranomaisille, viranomaiset voivat vähentää verojen välttelyä ja manipulointia sekä vähentää petoksia. 

Koko maailma on siirtymässä paperittomaan asiakirjakäsittelyyn ja ilman sähköistä laskutusta asiakkaat voivat ottaa riskiä yhteensopivuusongelmista, tarpeettomista kustannuksista ja kilpailijoiden jälkeen jäämisestä. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Eikö Financessa, Supply Chain Managementissa ja Project Operationsissa ole jo sähköinen laskutustoiminto? Mikä arvo tällä on minulle asiakkaana? 

Sähköinen laskutus laajentaa Financen, Supply Chain Managementin ja Project Operationsin sähköisiä laskutustoimintoja. Toiminnot myös yksinkertaistavat uusimpien sähköisten laskutusstandardien noudattamista, ja se tarjoaa yhtenäiset kokemukset eri alueilla sähköisen laskujen käsittelyn ja vaihdon suhteen. Sähköisen laskutuksen toiminnot tuovat monenlaisia etuja, joita ovat esimerkiksi seuraavat: 

   - Nopeampi ja helpompi maa-/aluekohtaisten määritysten käyttöönotto.
   - Sähköisen laskutusratkaisun käyttöönottojen standardointi. 
   - Parannettu sähköisen laskutuksen jäljitettävyys.  
   - Helpottaa lakisääteisten vaatimusten ja paikallisten liiketoimintakäytäntöjen noudattamisen ylläpitoa. 
   - Yksinkertainen ratkaisun pakkaus.
   - Skaalausominaisuudet suurille lähetettyjen tiedostojen määrälle, mikä nopeuttaa asiakirjojen kiertoa.
   - Mahdollisuus jakaa ratkaisut muiden yritysten kanssa.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Tukeeko sähköinen laskutus Financen, Supply Chain Managementin jan Project Operationsin paikallisia asennuksia? 

Nykyinen alusta ei salli paikallisen version käyttöä, eikä sitä ole suunnitelmia tukea tulevaisuudessa.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Käyttääkö sähköinen laskutusliittymä toimittajan tuonnin automaatio-ominaisuutta?

Et voi. Tätä käyttöliittymää varten on suunnitelmia, mutta suunniteltua aikajanaa ei ole. Kun niitä suunnitellaan, päivämäärät ilmoitetaan [julkaisusuunnitelmissa](https://docs.microsoft.com/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Miten sähköinen laskutus käsittelee sähköiseen laskuun liittyvät tiedostoliitteet? Tarvitaanko SharePoint-palvelin, kun PDF-tiedostoja upotetaan XML-tiedostoon?

Sähköiseen laskuun liitettyjä tiedostoja käsitellään XML-elementtiin upotettuina binaaritietoina. SharePoint-palvelinta ei tarvita PDF-tiedostojen upottamiseen, mutta liite on tallennettava Financen, Supply Chain Managementin tai Project Operationsin tiedostohallintajärjestelmään.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Onko sähköinen laskutus käytettävissä maani/alueeni säännösten mukaan?

Sähköinen laskutus on mikropalvelualusta, joka on käytettävissä maailmanlaajuisesti.

Microsoft aikoo julkaista sähköiset laskumuodot ja integroinnit niille maille ja alueille, joiden toiminnallisuuden Microsoft on lokalisoinut. Lisätietoja on kohdassa [Sähköisten laskutusominaisuuksien saatavuus](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Jos maasi/alueesi sähköistä laskutusmuotoa ei ole lueteltu, alusta pyrkii tukemaan tätä skenaariota tulevaisuudessa. Voit edelleen hyödyntää sähköisen laskutuksen konfiguraatiotoimintoja ja konfiguroida sähköisen laskutusmuodon itse tai voit konfiguroida organisaatiosi ominaisuudet yhdessä yhteistyökumppanin/ISV:n kanssa.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Onko Dynamics 365 for Regulatory Services uusi moduuli, kuten Human Resources tai Project Operations, joka on linkitetty Financeen tai Supply Chain Managementiin? Liittyykö tähän lisäkustannuksia?

Dynamics 365 for Regulatory Services (RCS) on pilvipalvelu globalisointiresurssien konfigurointiin. RCS on maksuton kaikille Financen, Supply Chain Managementin ja Project Operationsin lisenssin haltijoille.

Rekisteröidy RCS:sään osoitteessa <https://marketing.configure.global.dynamics.com/>.

Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Tarvitseeko rekisteröityä, jotta saan sähköisen laskutuksen, vai otanko sen vain käyttöön toiminnonhallinnassa?

Jos sinulla on Financen, Supply Chain Managementin tai Project Operationsin käyttöoikeus, rekisteröidy sähköiseen laskutukseen kohdassa [Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md).

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Toimiiko sähköinen laskutus tason 1 virtuaalikoneiden kanssa? Mikä on edellytetty vähimmäisympäristö?

Sähköisen laskutuksen integrointi edellyttää vähintään tason 2 virtuaalikonetta Financen tai Supply Chain Managementin isännöintiin. Lisätietoja ympäristöjen suunnittelusta on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Onko sähköisessä laskutuksessa testitila laskun lähetyksen testaamista varten?

Tämä voidaan saavuttaa konfiguraation avulla. Voit testata laskun lähettämistä muodostamalla yhteyden Financeen tai Supply Chain Managementiin käyttäjän hyväksynnän testiympäristöstä (UAT) ja lähettää testilaskut. Sähköinen laskutus tukee digitaalisten testisertifikaattien konfigurointia ja digitaalista hyväksyntää edellyttävissä sähköisissä laskuissa veroviranomaisten julkaisemien testiverkkopalveluiden URL-osoitteiden määritystä.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Onko olemassa dokumentaatiota sähköisistä laskutuksen käyttövalmiista maa-/aluekohtaisista ominaisuuksista?

Kyllä. Tietoja sähköisten laskutusominaisuuksien saatavuudesta ja niiden tukemista muodoista on kohdassa [Sähköisten laskutusominaisuuksien käytettävyys](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Jos et löydä etsimääsi vastausta, lähetä kysymyksesi tuotekehitystiimille osoitteeseen <D365EInvoicePreview@microsoft.com>. Microsoft joko ottaa yhteyttä tai parantaa näiden usein kysyttyjen kysymysten kattavuutta.
